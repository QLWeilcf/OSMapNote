# 交互

瓦片地图服务器可以通过实现两个HTTP端点接口增强瓦片数据的交互性.

* `[base path]/layer.json`: 一个图层清单JSON文件存储交互格式函数和其他可选属性.
* `[base path]/{n}/{n}/{n}.grid.json`: 与瓦片图像关联的一个UTFGrid JSON文件.

`[base path]` 指图层URL中XYZ之前的路径.

示例:

TMS样式的URL地址

    http://example.com/1.0.0/world/0/0/0.png       // tile image for 0/0/0
    http://example.com/1.0.0/world/0/0/0.grid.json // utfgrid for 0/0/0
    http://example.com/1.0.0/world/layer.json      // layer manifest

OSM样式的URL地址

    http://example.com/0/0/0.png       // tile image for 0/0/0
    http://example.com/0/0/0.grid.json // utfgrid for 0/0/0
    http://example.com/layer.json      // layer manifest

## 图层清单layer.json

图层清单应提供下述包含以下键的JSON对象:

* `formatter`: 字符串. 格式化UTFGrid JSON中要素数据的匿名javascript函数. **必需**.
* `legend`: 字符串. 自包含的HTML页面，显示为该图层的图例. **可选**.

`layer.json`示例:

    {
        "formatter": "function(options, data) { return data.NAME; }",
        "legend": "<strong>Countries of the World</strong>"
    }

每个`layer.json`项在`metadata`中表示为1行记录，`key,value` 对应`layer.json`对象的键值.

### 格式化函数(formatter)

UTFGrid规范没有对数据类型和属性做限制，只要求数据是合法的JSON文档. 格式化函数用于提供面向应用的数据表达.

每个瓦片数据集只允许1个格式化函数. 格式化函数可以用于不同的表达中，如悬停、单击等, 给函数传递1个`options` 对象作为第一个参数，第二个参数必须是数据集中的JSON对象.

     function (options, data) {
        ...
        return formatted_output;
     }

`options` 参数有一个标准化的属性 `format`, 它是一个字符串, 所有格式化函数必须支持两个值"teaser" 和 "full".

    function (options, data) {
        if (options.format == 'teaser') {
            return '<h1>' + data.NAME + '</h1>';
        } else if (options.format == 'full') {
            return '<h1>' + data.NAME + '</h1>' + data.AREA;
        }
    }

### 图例

一个瓦片数据集可能提供一个HTML字符串，供客户端渲染为图例. 该字符串应当是自包含的，不包括外部样式、脚本、图片引用. 必要时[Data URI scheme](http://en.wikipedia.org/wiki/Data_URI_scheme) 可用来嵌入图片或其他数据.

    <div><span style='padding:0px 10px; background:#333;'></span> +10% population</div>
    <div><span style='padding:0px 10px; background:#666;'></span> +5% population</div>
    <div><span style='padding:0px 10px; background:#999;'></span> +0% population</div>
    <div><span style='padding:0px 10px; background:#ccc;'></span> -5% population</div>

## grid.json

UTFGrid JSO的格式和存储见 `utfgrid_zh.md`.
