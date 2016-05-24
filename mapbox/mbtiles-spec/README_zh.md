# MBTiles 规范

MBTiles是在[SQLite](http://sqlite.org/)数据库中存储瓦片地图数据的规范，以瓦片应用和传输为目的.
MBTiles文件又称为**瓦片集(tilesets)**, 必须实现以下规范以保证设备兼容性.

## UTFGrid

MBTiles规范以前包含
[UTFGrid 规范](https://github.com/mapbox/utfgrid-spec).
在1.2版本时移除为一个单独的规范，版本保持同步 - MBTiles 1.2 与 UTFGrid 1.2兼容.

# 版本

* **开发版** - 不可用: [1.2](https://github.com/mapbox/mbtiles-spec/blob/master/1.2/spec.md)
* **稳定版**: [1.1](https://github.com/mapbox/mbtiles-spec/blob/master/1.1/spec.md)
* [1.0](https://github.com/mapbox/mbtiles-spec/blob/master/1.0/spec.md)

# 更新日志

## 路线图

* 将瓦片排序更改为类似OpenStreetMap流行的XYZ模式，而不采用Tile Map Service规范.

## 1.1

* `name='format'` 表`metadata`必需的行.
* `name='bounds'` 表`metadata`建议的行.
* 可选的基于UTFGrid的交互规范.

# 概念

MBTiles is a compact, restrictive specification. It supports only
tiled data, including image tiles and interactivity grid tiles. Only the
Spherical Mercator projection is supported for presentation - tile display -
and only latitude-longitude coordinates are supported for metadata such
as bounds and centers.

It is a minimum specification - only specifying the ways in which data
must be retrievable. Thus MBTiles files can internally compress and optimize
data, and construct views that adhere to the MBTiles specification.

Unlike [Spatialite](http://www.gaia-gis.it/spatialite/), GeoJSON,
and Rasterlite, MBTiles is not raw data storage - it is storage
for presentational data, like rendered map tiles.

One MBTiles file represents a single tileset, optionally including grids
of interactivity data. Multiple tilesets - layers, or maps in other terms,
can be represented by multiple MBTiles files.

# [实现](https://github.com/mapbox/mbtiles-spec/wiki/Implementations).

# 授权

规范文本遵循
[Creative Commons Attribution 3.0 United States License](http://creativecommons.org/licenses/by/3.0/us/).
However, the use of this spec in products and code is entirely free:
there are no royalties, restrictions, or requirements.

# 作者

* Tom MacWright (tmcw)
* Will White (willwhite)
* Konstantin Kaefer (kkaefer)
* Justin Miller (incanus)
