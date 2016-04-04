# 瓦片立方体规范

瓦片立方体(TileCubes)是一个传输时态或分类空间数据的规范.从2011年来，瓦片立方体已被用于很多生产项目，但其实现缺少公开文档.
该规范有意允许任何数据服务提供者提供瓦片立方体服务以在网络上渲染数据.

# 版本

* **发布** - [2.0]
  (https://github.com/CartoDB/tilecubes/blob/master/2.0/spec.md), [2.0中文版]
  (https://github.com/CartoDB/tilecubes/blob/master/2.0/spec.md)
* **开发** - [1.0]
  (https://github.com/andrewxhill/tilecubes/blob/master/1.0/spec.md)


# 变更日志

## 发展路线图

 * 规范
 * 客户端
 * 示例
 * 交互性
 * 灵活的维数
   * 未来,数据可以是多维的
     (如. Month:Gender:AgeGroup), 然而版本V1.x 限于Key:Value(如Month:Gender) 和 重复的Key:Value(如Month:Gender,Month:AgeGroup)

## 1.0



# 概念

瓦片立方体使用客户端的分辨率来渲染以优化地图多维数据的传输.

# 实现

* [GBIF](http://www.gbif.org/occurrence) 其[简要说明](http://blog.cartodb.com/connecting-hbase-hadoop-to-cartodb-to-visualize/)
* CartoDB [torque](https://github.com/CartoDB/torque)

# 作者

* Andrew Hill (andrewxhill)
* Javier Santana (javisantana)
* Javier de la Torre (jatorre)
* Sandro Santilli (strk)
* Tim Robertson (timrobertson100)

作者参考了以下规范来指导瓦片立方体规范(TileCubes)的开发和发布,

* [MBTiles瓦片地图存储规范](https://github.com/mapbox/mbtiles-spec) 
* [OSGeo瓦片地图规范](http://wiki.osgeo.org/wiki/Tile_Map_Service_Specification)
