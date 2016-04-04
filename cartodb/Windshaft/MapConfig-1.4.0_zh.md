# 1. 目的

该规范描述[地图配置](MapConfig-specification_zh.md)格式版本 1.4.0.


# 2. 文件格式

图层组(Layergroup)文件使用JSON格式描述，参考[RFC 4627](http://www.ietf.org/rfc/rfc4627.txt).

```javascript
{
    // 可选项
    // 规范的版本号
    // 默认"1.0.0".
    version: "1.4.0",

    // 可选项
    // 默认的地图范围(采用地图投影坐标)
    // (当前仅支持webmercator)
    extent: [-20037508.5, -20037508.5, 20037508.5, 20037508.5],

    // 可选项
    // 地图空间参考唯一标识
    // 默认3857
    srid: 3857,

    // 可选项
    // 渲染的最大级别，大于该级别响应404 
    // 默认：undefined (infinite)
    maxzoom: 18,

    // 可选项
    // minzoom-渲染的最小级别，小于该级别响应404，必须小于最大级别(maxzoom)
    // 默认：0
    minzoom: 3,

    // 必选项
    // 依据渲染顺序定义的图层数组
    // 图层支持不同类型，描述如下
    layers: [
        {
            // 必选项
            // 字符串，设置图层类型，取值:
            //  - 'mapnik'  - 栅格化的瓦片
            //  - 'cartodb' - mapnik别名-向后兼容
            //  - 'torque'  - 以torque格式渲染矢量瓦片
            //  - 'http'    - 基于HTTP加载瓦片
            //  - 'plain'   - 颜色或背景图片url
            type: 'mapnik',

            // 必选项
            // 对象, 为每个图层类型设置不同的选项
            options: {
                // 不同的图层类型对应的选项见下文
                // 注意: 未在图层中定义的选项将被丢弃
            }
        }
    ]
}
```

## 2.1 Mapnik 图层选项

```javascript
{
    // 必选项
    // 字符串，SQL查询语句(获得的数据用于地图渲染).
    //
    // 查询的列应至少包括后文几何字段(``geom_column``),交互字段(``interactivity``) 和属性字段(``attributes``)指定的列
    //
    // 查询能够包括替换标记!bbox!, !pixel_width!, !scale_denominator!,!pixel_height!, 见后文属性字段(``attributes``)配置.
    //
    sql: 'select * from table',

    // 必选项
    // 字符串，渲染瓦片的CartoCSS样式
    //
    // CartoCSS规范依赖图层类型:
    //  Mapnik: https://github.com/mapnik/mapnik-reference/blob/master/2.3.0/reference.json
    cartocss: '#layer { ... }',

    // 必选项
    // 字符串，CartoCSS样式版本号
    //
    // 图层类型对应版本必须是具体的.
    //
    cartocss_version: '2.0.1',

    // 可选项
    // 包括几何数据的列名
    // 默认'the_geom_webmercator'
    geom_column: 'the_geom_webmercator',

    // 可选项
    // 列类型：'geometry' 或 'raster'
    // 默认'geometry'
    geom_type: 'geometry',

    // 可选项
	// 栅格波段(仅当geom_type = 'raster'有效).
    // 如果是0或者未指定，栅格将被解释为灰度(单波段)或RGB(3波段)或RGBA (4波段).
    // 默认0
    raster_band: 0,

    // 可选项
    // 几何字段的地图空间参考唯一标识
    // 默认3857
    srid: 3857,

    // 可选项
    // 字符串数组，包括SQL使用的表名，在影响到的表不能从SQL语句猜出来时使用该配置项
    // (举例来说, plsql函数)
    affected_tables: [ 'table1', 'schema.table2', '"MixedCase"."Table"' ],

    // 可选项
	// 字符串数组，包括在grid.json中渲染的字段
    // 所有的参数都必须暴露在在sql属性查询结果中
    // 注意: 在使用栅格图层(geom_type='raster')时，交互字段(`interactivity`)不起作用.
    interactivity: [ 'field1', 'field2', .. ]

    // 可选项
    // 属性服务返回的值 (如不未指定该配置，则禁用该选项)
    attributes: {
        // 必选项
        // 用作查询的key
        id: 'identifying_column',

        // 必选项
        // 属性服务返回的字段列表字符串
        columns: ['column1', 'column2']
    }
}
```

## 2.2 Torque 图层选项

```javascript
{
    // 必选项
	// 字符串，SQL查询语句(获得的数据用于地图渲染).
    //
    // 查询的列应至少包括后文几何字段(``geom_column``),交互字段(``interactivity``) 和属性字段(``attributes``)指定的列
    //
    sql: 'select * from table',

    // 必选项
	// 字符串，渲染瓦片的CartoCSS样式
    //
    // CartoCSS规范依赖图层类型:
    //  Torque: https://github.com/CartoDB/torque/blob/master/lib/torque/cartocss_reference.js
    cartocss: '#layer { ... }',

    // 必选项
	// 字符串，CartoCSS样式版本号
    //
    // 图层类型对应版本必须是具体的.
    //
    cartocss_version: '1.0.0',

    // 可选项
    // 请求torque.png瓦片时渲染的步速(step)
    // 默认0
    step: 0,
	
	// 可选项
    // 包括几何数据的列名
    // 默认'the_geom_webmercator'
    geom_column: 'the_geom_webmercator',

    // 可选项
    // 几何字段的地图空间参考唯一标识
    // 默认3857
    srid: 3857,
	
	// 可选项
    // 字符串数组，包括SQL使用的表名，在影响到的表不能从SQL语句猜出来时使用该配置项
    // (举例来说, plsql函数)
    affected_tables: [ 'table1', 'schema.table2', '"MixedCase"."Table"' ],

    // 可选项
    // 属性服务返回的值 (如不未指定该配置，则禁用该选项)
    attributes: {
        // 必选项
        // 用作查询的key
        id: 'identifying_column',

        // 必选项
        // 属性服务返回的字段列表字符串
        columns: ['column1', 'column2']
    }
}
```


## 2.3 Http 图层选项

```javascript
{
    // 必选项
    // {String} 获取瓦片的URL地址.
    // {z} — 缩放级别, {x} 和 {y} — 瓦片坐标.
    // {s} - 子域名, {s} 是可选项. 见 `子域名`.
    //
    // 注意: URLs必须包括在配置白名单中才能生效
    urlTemplate: "http://{s}.example.com/{z}/{x}/{y}.png",

    // 可选项
    // {Array<String>} 用于从不同的子域名获取瓦片.
    // 从`urlTemplate`中替换{s}.
    // 当`urlTemplate`中有{s}时生效，默认['a', 'b', 'c'].
    subdomains: ['a', 'b', 'c'],

    // 可选项
    // {Boolean} 瓦片是否遵循TMS服务格式
    // 如果是真，则反转Y轴
    // 默认`false`
    tms: false
}
```

## 2.4 Plain 图层选项

注意事项:
 - `color` 或 `imageUrl`至少要提供1个选项.
 - 如果两者都进行了配置，只使用 `color` 的配置.

```javascript
{
    // 可选项/必选项
    // {String|Array<Number>}
    // 默认null
    // 合法的颜色包括:
    //  - CSS颜色名称(如`'blue'`) 或十六进制颜色字符串(如`'#0000ff'`).
    //  - 整数数组-r,g,b(如`[255,0,0]`)
    //  - 整数数组-r,g,b, a(如`[255,0,0,128]`)
    color: 'blue',

    // 可选项/必选项
    // {String} 图片URL地址.
    // 默认null
    imageUrl: 'http://example.com/background.png'
}
```

# 拓展

该文档为了特定用途可以进行拓展.
举例来说, Windshaft-CartoDB在配置中定义了"stat_tag"元素. 见 https://github.com/CartoDB/Windshaft-cartodb/wiki/MultiLayer-API

关于如何命名拓展该版本的规范尚未予以定义.

# TODO

 - 允许每个图层可以指定几何字段的名称
 - 允许指定图层投影/空间参考标识(srid)以及地图投影/空间参考标识(srid)
 - 允许指定四叉树配置(最大范围, 通常)
 - 指定CartoCSS版本的链接(即: 对torque来说什么是必须的等等.)

# 历史

## 1.4.0

 - 增加'plain'图层类型

## 1.3.0

 - 增加'http'图层类型
 - 在torque图层中增加渲染时的step参数
 - 在mapnik栅格类型的图层(geom_type=raster)中删除交互字段(interactivity)选项 
 - 在torque图层中删除交互字段(interactivity)选项,从未使用.

## 1.2.0

 - 在mapnik图层类型中增加'geom_type'和'raster_band'参数

## 1.1.0

 - 增加'torque'图层类型
 - 增加属性字段('attributes')配置

## 1.0.1

 - Layer.options.interactivity 从字符串改为数组

## 1.0.0

 - 初始版本
 