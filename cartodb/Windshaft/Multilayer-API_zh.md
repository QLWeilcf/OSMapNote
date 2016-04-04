该文档描述管理和使用windshaft图层的API.

其目标是在多个瓦片或网格请求之间减少配置项的重复，同时使用较短的url获取“配置图层组(configured layer group)”的副产品.


# 介绍

该API用于在切图程序中创建一个新端点(endpoint)，使得根据SQL查询和CartoCSS定义的图层组能够获取瓦片或交互网格.

# 快速开始

为了创建一个新的能够为地图提供瓦片服务的图层组端点，图层组需要使用POST方法传给服务器.

一个简单的图层组配置类似于:

```json
{
    "version": "1.0.1",
    "layers": [
        {
            "type": "cartodb",
            "options": {
                "cartocss_version": "2.1.1",
                "cartocss": "#layer { polygon-fill: #FFF; }",
                "sql": "select * from european_countries_e"
            }
        }
    ]
}
```

根据该配置我们创建了一个`layergroup.json`文件，该文件遵循[地图配置规范](MapConfig-specification_zh.md).

请求示例(documentation应替换为cartodb用户名):

```shell
curl 'http://documentation.cartodb.com/api/v1/map' \
    -H 'Content-Type: application/json' \
    -d @layergroup.json
```


该请求返回一个JSON，包括图层组的令牌ID和数据修改的最新时间戳:

```json
{
    "layergroupid": "c01a54877c62831bb51720263f91fb33:0",
    "last_updated": "1970-01-01T00:00:00.000Z"
}
```

根据`layergroupid`可以创建访问其瓦片的url模板:

```
http://documentation.cartodb.com/api/v1/map/c01a54877c62831bb51720263f91fb33:0/{z}/{x}/{y}.png
```

# 配置

`base_url_mapconfig`配置参数将决定图层组以及其他与`layergroupid`关联的的端点(endpoint).

在前面的快速开始例子中，`base_url_mapconfig`的值配置为`/api/v1/map`.


# 图层组(Layergroup) API
根据`base_url_mapconfig`的配置参数进行路由(Routes)，见前文.

注解: 图层索引从0开始，`N`层索引是从`0`到`N-1`.

## 跨域资源共享(Cross-origin resource sharing - CORS)
OPTIONS :base_url_mapconfig


## 创建一个图层组
`GET :base_url_mapconfig` 或 `POST :base_url_mapconfig`

应当是一个指向`:base_url_mapconfig`的POST，主体中带有图层组定义(content-type application/json) 
或一个来自`:base_url_mapconfig`的GET，在`config`参数中指定[图层组定义](MapConfig-specification_zh.md).

举例来说:

```json
{
    "version": "1.0.1",
    "layers": [
        {
            "type": "cartodb",
            "options": {
                "cartocss_version": "2.1.1",
                "cartocss": "#layer { polygon-fill: #FFF; }",
                "sql": "select * from european_countries_e"
            }
        }
    ]
}
```

切图程序将创建一个临时的mapnik配置，为其分配一个令牌(token),
验证其合法性(尝试获取一个瓦片和一个网格)并返回令牌. 同样的配置将得到同样的令牌.
客户端可使用该令牌获取瓦片或网格数据. 不能保证令牌仍然可用，因此客户端访问瓦片时应注意处理404错误.

服务端响应将包括一个时间戳，以标识图层相关的表格最新变化的时间.

响应JSON示例:

```
{
    // {String} 图层组标识符，用于请求资源
    "layergroupid": ":TOKEN",
    // {Object} 图层组相关联的元数据
    "metadata": {
        // {Array} 每个图层的元数据列表
        "layers": [
            {
                // 必须参数
                // {String} 图层组中要渲染的图层类型
                // Windshaft中的合法类型包括: "mapnik", "torque", "http", "plain"
                "type": "mapnik",
                // 必须参数
                // {Object} 永远存在即使为空
                "meta": {
                    // 地图渲染特定的JSON键值对
                }
            }
        ],
        // torque元数据(至少有一个torque图层)
        "torque": {
            // torque图层在图层组中的索引
            "1": {
                // {Number} 时间字段的最小值(毫秒)
                "start": 1325372640000,
                // {Number} 时间字段的最大值(毫秒). 必须大于开始时间
                "end": 1356994560000,
                // {Number} 数据聚合的步骤数
                "data_steps": 145571,
                // {String} 时间字段类型说明, "date" 或 "number"
                "column_type": "date"
            }
        }
    }
}
```

出现错误时的JSON示例:

```json
{
    "errors": [
        "sql errors (syntax errors)",
        "cartodcss errors (syntax)",
        "runtime errors (no permissions)"
    ]
}
```


## 访问地图瓦片

`GET :base_url_mapconfig/:TOKEN/{z}/{x}/{y}.png` 或
`GET :base_url_mapconfig/:TOKEN/{z}/{x}/{y}@{resolution}x.png` 或
`GET :base_url_mapconfig/:TOKEN/:LAYER/{z}/{x}/{y}.png` (向后兼容).

根据指定顺序渲染所有的`cartodb`/`mapnik`图层,根据CartoCSS进行图层的合并.

### 高清屏(Retina)支持

`@{resolution}x`参数支持高清屏图片渲染,默认值={1,2}, 为`@2x`时图片是512x512像素，而非常用的256x256像素.


## 获取某个图层的地图瓦片
`GET :base_url_mapconfig/:TOKEN/:LAYER/{z}/{x}/{y}.{format}`

此处 `{format}` 可以是:

  - png
  - grid.json
  - torque.json, torque.bin

当前指定的`:LAYER`必须支持请求的`{format}`要求,如请求`torque.json`时，`:LAYER`必须定义为torque图层类型.

### grid.json示例

`GET :base_url_mapconfig/:TOKEN/:LAYER/{z}/{x}/{y}.grid.json`


## 获取一组图层合并后的地图瓦片

`GET :base_url_mapconfig/:TOKEN/:LAYER_FILTER/{z}/{x}/{y}.png`

图层过滤器(`:LAYER_FILTER`)支持两种格式:

 - **all**: 合并图层组中的所有图层.
 示例: `GET :base_url_mapconfig/:TOKEN/all/{z}/{x}/{y}.png`
 - **根据图层索引号过滤** 使用逗号分割: 类似`0,3,4`会合并图层号0,3,4.
 示例: `GET :base_url_mapconfig/:TOKEN/0,3,4/{z}/{x}/{y}.png`
 关于过滤的几点注意事项:
  * 非法的图层索引值或索引号越界会产生`Invalid layer filtering`错误.
  * 一旦一个mapnik图层被选中，则所有的mapnik图层会被合并. 这部分内容在将来可能会被修改，**推荐**总是选择所有mapnik图层.
  * 当前未考虑排序. 0,3,4和3,4,0是一样的. 这部分内容在将来也可能会被修改，**推荐**采用升序以兼容未来.

**重要事项**: 当前格式是`png`，图层组中所有的渲染器都必须支持该格式才能进行合并.

## 获取静态图片

### 通过地图中心点(center) + 缩放级别(zoom) + 图片尺寸
`GET :base_url_mapconfig/static/center/:TOKEN/:Z/:LAT/:LNG/:WIDTH/:HEIGHT.:format`

### 通过外接矩形(bounding box) + 图片尺寸
`GET :base_url_mapconfig/static/bbox/:TOKEN/:WEST,:SOUTH,:EAST,:NORTH/:WIDTH/:HEIGHT.:format`


## 获取属性

`GET :base_url_mapconfig/:TOKEN/:LAYER/attributes/:FID`

grid.json 瓦片包括交互的内容，根据图层配置指定.

如果未指定交互项，返回错误.

见 [Windshaft-cartodb extension](https://github.com/CartoDB/Windshaft-cartodb/blob/master/docs/MultiLayer-API.md).


# 内部逻辑

## 图层组存储
图层组临时存储在redis中，由grainstore模块负责管理

## 缓存管理
根据时间配置(秒)，在最后一次访问多少秒后过期

## 公有/私有
安全由postgresql层进行处理，在获取瓦片时进行检查
