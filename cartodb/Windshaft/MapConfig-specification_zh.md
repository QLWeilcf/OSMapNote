MapConfig用于在Windshaft中创建地图，通过[多层API](Multilayer-API_zn.md)进行。

最新版本: [MapConfig-1.4.0](MapConfig-1.4.0_zh.md)

创建地图的标识继而被用于获取不同的资源（依赖地图配置）:

  - 瓦片(Tiles)
    - 由 {z}/{x}/{y} 路径标识
    - 可能的额外标识: LAYER_NUMBER
    - 支持多种格式:
        * png
        * grid.json
        * torque.json
  - 静态图片/预览
    - 地图中心点(center)或外接矩形
  - Attributes
    - 由LAYER_NUMBER和FEATURE_ID标识
