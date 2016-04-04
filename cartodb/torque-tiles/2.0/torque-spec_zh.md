# Torque瓦片规范 2.0

## 摘要

Torque瓦片(TorqueTiles)是带地理坐标的多维数据的JSON表达.它被分为两种文档类型,元数据文档和瓦片文档.
元数据文档描述瓦片立方体数据集之间的共享信息. 对于请求的每个瓦片都返回一个瓦片文档，描述该瓦片上的数据.

Torque瓦片参考了[OSGeo的瓦片地图服务规范](http://wiki.osgeo.org/wiki/Tile_Map_Service_Specification)
当前仅支持[全球墨卡托投影](http://wiki.osgeo.org/wiki/Tile_Map_Service_Specification#global-mercator).
在瓦片立方体中，假设瓦片大小为256x256像素，坐标根据像素空间的偏移进行表示.


## 元数据文档

TorqueMap元数据文档描述关键的瓦片数据集信息，它包括:

- **start**: 开始时间, 步数或unix时间戳
- **end**: 结束时间, 步数或unix时间戳
- **resolution**: 像素分辨率，2的幂(1/4, 1/2,... 2, 4, 16); 与256x256像素的比例
- **data_steps**: 步数 (integer)
- **column_type**: "integer" 或 "date", 默认 "integer"
- **minzoom**: 最小缩放级别, 可选项
- **maxzoom**: 最大缩放级别, 可选项
- **tiles**: 该数据的瓦片数组, 必选项
- **bounds**: 瓦片数据集的[外接矩形](http://wiki.openstreetmap.org/wiki/Bounding_Box),可选项

```
{
    start: 0,
    end: 100, 
    resolution: 2           
    # scale: 1/resolution,
    data_steps: 365,
    column_type: "number"
    "minzoom": 0,
    "maxzoom": 11,
    "tiles": [
        'http://a.host.com/{z}/{x}/{y}.torque.json',
        'http://b.host.com/{z}/{x}/{y}.torque.json',
        'http://c.host.com/{z}/{x}/{y}.torque.json',
        'http://d.host.com/{z}/{x}/{y}.torque.json'
    ],
    "bounds": [ -180, -85.05112877980659, 180, 85.0511287798066 ]
}
```

## 元数据文档使用

### 选择分辨率

瓦片立方体通常渲染为256x256像素的瓦片. 因此建议选择一个能够沿256像素瓦片边界完美渲染的比例尺,
否则会出现渲染不好的地方. 可能的像素分辨率如下,
```1, 2, 4, 8, 16, 32, 64, 128, 256```


## 瓦片文档

瓦片用于存储要渲染的核心信息集，这些信息包括数据的像素个数、每个像素的x、y值. 

### 瓦片URL模式

```
http://host.com/{z}/{x}/{y}.torque.[json|bin]
```

### 瓦片格式
每个Torque瓦片都是包含数组的一个JSON文档, 每个元素表示瓦片上的一个点, 以符号表示,遵循下述格式:

 - x: 瓦片坐标系统中的x像素坐标(int)
 - y: 瓦片坐标系统中的y像素坐标(int)
 - steps: 该像素**启用(active)**时的时间槽(time slots), 这时有数据
 - values: 每个时间槽(time slots)对应的数值

```
[
    {
        x: 25,
        y: 77,
        values: [ 1, 10 ],
        steps: [214, 215]
    },
...
]
```

## 瓦片文档的使用

### 提取像素位置

``x`` 和 ``y`` 取值范围是[0, 256/resolution]，为了得到最终的像素坐标(基于256x256瓦片)，需使用下述计算公式:

```
pixel_x = x * resolution
pixel_y = y * resolution
```

Torque瓦片的坐标原点在**左下角(bottom left corner)**.

### 提取当前时间

提取当前时间需要```current step```, ```translate```和```steps```三个参数:

```
current_time = translate.start  + step * (translate.end - translate.start)/data_steps;
```

### 分类编码

```vals``` 列用于存储分类编码.
