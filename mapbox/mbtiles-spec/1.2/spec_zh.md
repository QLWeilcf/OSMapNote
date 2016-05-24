# MBTiles 1.2

# 小节:

* **交互(Interaction)**: 为实现交互查询，需要HTTP端点
* **UTFGrid**: 为实现交互查询，该规范依赖 [UTFGrid 1.2](https://github.com/mapbox/utfgrid-spec).

## 摘要

MBTiles是在[SQLite](http://sqlite.org/)数据库中存储瓦片地图数据的规范，以瓦片应用和传输为目的.
MBTiles文件又称为**瓦片集(tilesets)**, 必须实现以下规范以保证设备兼容性.

## 数据库规范

瓦片集(Tilesets)必须是合法的SQLite数据库[3.0.0](http://sqlite.org/formatchng.html)或以上版本.
仅允许核心的SQLite功能; 瓦片集(Tilesets)**不需要拓展**.

MBTiles数据库也可以使用[官方分配的幻数(magic number)](http://www.sqlite.org/src/artifact?ci=trunk&filename=magic.txt)以标记文件格式.

## 数据库

注: 列出的表格模式以接口方式定义.能够生成兼容结果的SQLite视图也同样合法.
为方便起见，规范将表(table)和视图(view)都视为表.

### 元数据

#### 表结构

数据库要求包括一个名为`metadata`的表或视图.

表`metadata`必须有两个字段，字段名分别为`name`和`value`. 通常创建`metadata`表的语句为:

    CREATE TABLE metadata (name text, value text);

#### 表格内容

元数据表基于键值对(key/value)方式存储一些配置信息. 五个键是**必须的**:

* `name`: 瓦片集名称(纯文本).
* `type`: `overlay` 或 `baselayer`
* `version`: 瓦片集版本(普通数字).
* `description`: 图层描述(纯文本).
* `format`: 瓦片数据中图片文件的格式: `png` 或 `jpg`

`metadata` **建议** 的记录（如存在该记录，能提高性能:

* `bounds`: 地图区域的最大范围. 范围必须定义一个覆盖所有缩放级别的区域. 以`WGS:84`经纬度坐标表示,采用OpenLayers区域范围格式 -
  **left, bottom, right, top**. 整个地球范围示例如下: `-180.0,-85,180,85`.
* `attribution`: 归属字符串, 简要解释数据源和/或地图样式, 支持HTML.

其他的键用于支持瓦片数据集[基于UTFGrid的交互](https://github.com/mapbox/utfgrid-spec).

### 瓦片数据

#### 表结构

数据库要求包括一个名为`tiles`的表或视图.

表`tiles`必须有四个字段，字段名分别为`zoom_level`, `tile_column`, `tile_row`, 和 `tile_data`. 通常创建`tiles`表的语句为:

    CREATE TABLE tiles (zoom_level integer, tile_column integer, tile_row integer, tile_data blob);

#### 表格内容

该表存储了瓦片数据和用于定位瓦片的索引.      
`zoom_level`, `tile_column`, 和 `tile_row` 列在构建时以受限方式遵循[Tile Map Service 规范](http://wiki.osgeo.org/wiki/Tile_Map_Service_Specification):

 ** 假设使用[全球墨卡托(global-mercator)](http://wiki.osgeo.org/wiki/Tile_Map_Service_Specification#global-mercator)模式, 又称为 球体墨卡托(Spherical Mercator). **

`tile_data blob` 列存储二进制的原始图片数据.

目前支持以下图片格式:

* `png`
* `jpg`

### 格网数据

_格网和交互元数据实现细节见[UTFGrid规范](https://github.com/mapbox/utfgrid-spec)，本规范只描述存储._  

#### 表结构

数据库可选表名分别为`grids`, `grid_data`.

表`grids`必须包括4个字段, 字段名分别为`zoom_level`, `tile_column`, `tile_row` 和 `grid`. 通常创建`grids`表的语句为:

    CREATE TABLE grids (zoom_level integer, tile_column integer, tile_row integer, grid blob);

表`grid_data` 必须包括5个字段, 字段名分别为`zoom_level`, `tile_column`, `tile_row`, `key_name` 和 `key_json`. 通常创建`grid_data`表的语句为:

    CREATE TABLE grid_data (zoom_level integer, tile_column integer, tile_row integer, key_name text, key_json text);

#### 表格内容

表`grids`存储UTFGrid数据, 使用gzip压缩.

表`grid_data`存储网格键值映射, 以JSON对象进行编码.
