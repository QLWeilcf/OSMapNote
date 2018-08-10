
# awesome leaflet 

## Leaflet调用方法
使用在线版本
The latest stable Leaflet release is hosted on a CDN — to start using it straight away, place this in the head of your HTML code:
```javascript
<link rel="stylesheet" href="http://cdn.leafletjs.com/leaflet/v0.7.7/leaflet.css" />
<script src="http://cdn.leafletjs.com/leaflet/v0.7.7/leaflet.js"></script>
```    

使用本地版本
 * leaflet.js - This is the minified Leaflet JavaScript code.
 * leaflet-src.js - This is the readable, unminified Leaflet JavaScript, which is sometimes helpful for debugging.
 * leaflet.css - This is the stylesheet for Leaflet.
 * images - This is a folder that contains images referenced by leaflet.css. It must be in the same directory as leaflet.css.
```javascript
<link rel="stylesheet" href="/path/to/leaflet.css" />
<script src="/path/to/leaflet.js"></script> <!-- or use leaflet-src.js --!>
```    
## 官方文档
- [官网](https://leafletjs.com/)  介绍了最基本的用法，并且能直接链接到 Docs & Download & Plugins
- [Leaflet Plugins](https://leafletjs.com/plugins.html) 各种插件的说明介绍，包含了大部分下面的内容，包括瓦片源、叠加数据、交互、第三方工具、自己写插件等

## Leaflet瓦片数据源
- [Leaflet-providers](https://github.com/leaflet-extras/leaflet-providers) - 免费瓦片数据源
- [中国地图瓦片服务](https://github.com/wandergis/Leaflet.ChineseTmsProviders) - 天地图、高德、MapABC
- [中国地图瓦片服务2](https://github.com/htoooth/Leaflet.ChineseTmsProviders) - 天地图、高德、Google、GeoQ
- [百度地图](https://github.com/sureleo/leaflet-baidu) - leaflet调用百度地图瓦片
- [腾讯地图](https://github.com/kennethhutw/leaflet-qq) - [调用腾讯地图瓦片](http://www.bubuko.com/infodetail-845917.html), 百度和腾讯地图[瓦片规则分析](http://blog.csdn.net/mygisforum/article/details/22997879). 
- [heigeo/leaflet.wms](https://github.com/heigeo/leaflet.wms) - A Leaflet plugin for working with Web Map services, providing: single-tile/untiled/nontiled layers, shared WMS sources, and GetFeatureInfo-powered identify
- [ESRI leaflet plugins](https://github.com/Esri/esri-leaflet) - 使用leaflet调用ArcGIS的基础底图和矢量服务的插件
- [Leaflet.Zoomify](https://github.com/turban/Leaflet.Zoomify) - Display [Zoomify](http://zoomify.com/) tiles with Leaflet. [More information](http://blog.thematicmapping.org/2013/06/showing-zoomify-images-with-leaflet.html).
- [leaflet-iip](https://github.com/astromatic/Leaflet.TileLayer.IIP) - Add [IIP](http://iipimage.sourceforge.net/) layering support to the Leaflet library
- [buche/leaflet-openweathermap](https://github.com/buche/leaflet-openweathermap) - A JavaScript library for including OpenWeatherMap's layers and OWM's current city/station data in leaflet based maps without hassle.
- [leaflet-layerConfig](https://github.com/Norkart/Leaflet-LayerConfig) - Library that communicates with a web service/reads a stored JavaScript object and adds layers to a leaflet map.

### 瓦片 Url




## Leaflet矢量图层	
- [JasonSanford/leaflet-vector-layers](https://github.com/JasonSanford/leaflet-vector-layers) - 添加矢量图层(Point, Polyline, Polygon) from multiple geo web services including ArcGIS Server, GeoIQ, Arc2Earth, CartoDB, GIS Cloud, etc.
- [leaflet-tilelayer-geojson](https://github.com/glenrobertson/leaflet-tilelayer-geojson) - 矢量瓦片图层：Leaflet TileLayer for GeoJSON tiles 
- [shramov/leaflet-plugins](https://github.com/shramov/leaflet-plugins) - Tile Providers (layer/tile - Google/Yandex/Bing) & Vector layers (layer/vector - GPX/KML/TOPOJSON).
- [leaflet-UTFGrid](https://github.com/danzel/Leaflet.utfgrid) - A UTFGrid interaction implementation for Leaflet that is super small.
- [leaflet-maskcanvas](https://github.com/domoritz/leaflet-maskcanvas) - Canvas图层， A leaflet canvas layer for displaying large coverage data sets. 
- [leaflet-filelayer](https://github.com/makinacorpus/Leaflet.FileLayer) - 本地文件图层, Loads files locally (GeoJSON, KML, GPX) as layers using HTML5 File API
- [leaflet-fractal](https://github.com/aparshin/leaflet-fractal) -  分形图层JavaScript fractals drawing using Leaflet, HTML5 Canvas and web workers
- [leaflet-photos](https://github.com/turban/Leaflet.Photo) - 显示图片, Plugin to show geotagged photos on a Leaflet map
- [Leaflet circles 2](https://github.com/stamen/leaflet-circles-2) - A leaflet circle layer
- [leaflet-plugins](https://github.com/turban/leaflet-plugins) - L.CartoDB/L.Categorical/L.Choropleth/L.Graticule/L.Wax
- [leaflet-piechart](https://github.com/sashakavun/leaflet-piechart) - Pie chart marker for Leaflet library
	

## Leaflet注记图层
- [leaflet-label](https://github.com/Leaflet/Leaflet.label) - 弹出式注记-adding labels to markers & shapes on leaflet 
- [leaflet-iconlabel](https://github.com/jacobtoye/Leaflet.iconlabel) - Adds support for displaying a label to the right of a Leaflet Icon.
- [umap-project/Leaflet.Label](https://github.com/umap-project/Leaflet.Label) - Leaflet.Label support polygons, polylines and many label direction(center, top and bottom). 加文本标签
- [leaflet-textpath](https://github.com/makinacorpus/Leaflet.TextPath) - Show text along Polyline with Leaflet			
			
## Leaflet图层效果
- [leaflet-grayscale](https://github.com/Zverik/leaflet-grayscale) - A regular TileLayer with grayscale makeover. 灰度化
- [leaflet-tilefilter](https://github.com/humangeo/leaflet-tilefilter) - Change the appearance of Leaflet map tiles on the fly using a variety of canvas or CSS3 image filters. It's like Instagram for Leaflet map tiles.

		
## Leaflet图层对比
- [digidem/leaflet-side-by-side](https://github.com/digidem/leaflet-side-by-side) - A Leaflet control to add a split screen to compare two map overlays, [Live Example Here](http://lab.digital-democracy.org/leaflet-side-by-side/) .
- [tmwdr/map-agis-leaflet-slider](https://github.com/tmwdr/map-agis-leaflet-slider) - Compare two layers in Leaflet using a slider, Inspiration comes from [Mapbox demo](https://www.mapbox.com/mapbox.js/example/v1.0.0/swipe-layers/) .
- [ugent-geography/leaflet-beforeafter](https://github.com/ugent-geography/leaflet-beforeafter) - Add functionality like the jquery BeforeAfter plugin to Leaflet layers.
- [frogcat/leaflet-tilelayer-cmp](https://github.com/frogcat/leaflet-tilelayer-cmp)  and [frogcat/leaflet-control-swipe](https://github.com/frogcat/leaflet-control-swipe) - Swipe control plugin for Leaflet 1.0b & 1.0
- [leaflet-geojson-layer-swipe](https://github.com/mysema/leaflet-layer-swipe) - An example implementation of a before/after swipe overlaid on a Leaflet.js map that works with GeoJSON layers
- [JackDougherty/leaflet-map-sync-zoom](https://github.com/JackDougherty/leaflet-map-sync-zoom) - Leaflet maps with synchronized side-by-side zoom to compare two locations at same scale, 比较同一级别的不同位置(地域对比), inspired from [mapbox](http://jackdougherty.github.io/otl-compare-school-districts/) . 


## Leaflet Marker clusters
- [leaflet-markcluster](https://github.com/Leaflet/Leaflet.markercluster) - 点聚类图层Marker Clustering plugin for Leaflet
- [pruneCluster](https://github.com/SINTEF-9012/PruneCluster) - Fast and realtime marker clustering for Leaflet
- [QCluster](https://github.com/spatialdev/q-cluster) - Quick point clustering code that get sefficiency from ordering points by coordinate notation code.
- [leaflet-canvas-icon](https://github.com/sashakavun/leaflet-canvasicon) - Canvas Icon plugin for Leaflet library
- Leaflet Markers 点状图标库
	- [leaflet-awesome-markers](https://github.com/lvoogdt/Leaflet.awesome-markers) - Markers图标库, Colorful iconic & retina-proof markers for Leaflet, based on the Glyphicons / Font-Awesome icons
	- [leaflet-extraMarkers](https://github.com/coryasilva/Leaflet.ExtraMarkers) - Markers图标库, Custom Markers for Leaflet JS based on Awesome Markers
	- [leaflet-svg-markers](https://github.com/hiasinho/Leaflet.vector-markers) - Vector SVG markers for Leaflet, with an option for Font Awesome/Twitter Bootstrap/Maki icons.
	- [leaflet.makimarkers](https://github.com/jseppi/Leaflet.MakiMarkers) - Leaflet plugin to create map icons using Maki Icons from Mapbox.
	- [leaflet-numbered-marker](https://github.com/Zahidul-Islam/Leaflet.awesome-numbered-marker) - 数字图标
	- [Yii-leaflet](https://github.com/2amigos/yii2-leaflet-awesome-plugin) - [Yii 2](https://github.com/yiisoft/yii2) LeafletJs Plugin to create map icons using Font Awesome and GlyphIcon Icons. 
	- [leaflet-mapkey-icon](https://github.com/mapshakers/leaflet-mapkey-icon) - icon font especially for cartographical use.
	- [leaflet-coordinates](https://github.com/pedroetb/Leaflet-Awesome-Coordinates) - 显示坐标, Leaflet map example using Leaflet-Coordinates with Leaflet.awesome-markers
- [leaflet-search](https://github.com/stefanocudini/leaflet-search) - searching markers/features by attribute on map or remote searching in jsonp/ajax geocoding
- [leaflet-rotatedMarker](https://github.com/bbecquet/Leaflet.RotatedMarker) - Leaflet plugin to enable the rotation of map marker icons
- [OpenLayers-icon-decay](https://github.com/March-hare/decayimage) - Custom OpenLayers functionality for Ushahidi that allows for map icon "decay" and associating category icons with incidents on the map
- [Leaflet.Photo](https://github.com/turban/Leaflet.Photo) 在地图上显示照片，特别适合那种旅游展示或者情侣经历地图；
## Leaflet heatmap
- [leaflet-heatmap](https://github.com/Leaflet/Leaflet.heat) - 热力图图层：A tiny, simple and fast heatmap plugin for Leaflet
- [webgl-heatmap-leaflet](https://github.com/ursudio/webgl-heatmap-leaflet) - draw hundreds of thousands of data points to a map using webgl


## Leaflet polyline 
- [leaflet-PolylineDecorator](https://github.com/bbecquet/Leaflet.PolylineDecorator) - 线图层简单符号化, a plug-in for the JS map library Leaflet, allowing to define patterns (like dashes, arrows, icons, etc.) on Polylines. 


## leaflet 动态数据/动画
- 动画效果
	* [Leaflet.AnimatedMarker](https://github.com/openplans/Leaflet.AnimatedMarker) - 点的沿线动画
	* [leaflet-flyto](https://github.com/JackDougherty/leaflet-flyto) - Leaflet flyTo map demo
- 多时间序列W动态图层 (eg. WMS) 
	* [Leaflet.TimeDimension](https://github.com/socib/Leaflet.TimeDimension) - Add time dimension capabilities on a Leaflet map. 支持WMS, 也支持GeoJSON
	* [Leaflet-WMS-Time-Slider](https://github.com/BobTorgerson/Leaflet-WMS-Time-Slider) - The Leaflet WMS Time Slider enables you to dynamically update a WMS layer based on a dimension such as time.	
- Dynamic Object (eg. GeoJSON) 
	* [leaflet-timeline](https://github.com/skeate/Leaflet.timeline) - Display arbitrary GeoJSON on a map with a timeline slider and play button
	* [LeafletPlayback](https://github.com/hallahan/LeafletPlayback) - Leaflet Playback provides the ability to replay GPS Tracks in the form of GeoJSON objects. Rather than simply animating a marker along a polyline, the speed of the animation is synchroized to a clock. 
	* [leaflet-realtime](https://github.com/perliedman/leaflet-realtime) - Leaflet Realtime reads and displays GeoJSON from a provided source.
	* [mschwarzer/Leaflet.Sim](https://github.com/mschwarzer/Leaflet.Sim) - Leaflet.Sim is a framework for location-based simulations with Leaflet maps that can visualise moving markers, which can change their style, and events over time on a map.
- leaflet-based timeline
	* [timeMapperJS](https://github.com/dutri001/timeMapperJS) - Integrates leaflet and [timelineJS3](https://github.com/NUKnightLab/TimelineJS3), for a time map with narrative



## leaflet 功能
- [leaflet-easyButton](https://github.com/CliffCloud/Leaflet.EasyButton) - Easily Add Control Buttons with Font Awesome Icons and Callbacks
- [leaflet-contextmenu](https://github.com/aratcliffe/Leaflet.contextmenu) - 右键菜单：A context menu for Leaflet.
- [leaflet-zoom-extras](https://github.com/stamen/leaflet-zoom-extras) - Extends Leaflet's Zoom controller to allow for extra buttons
- [wandergis/Leaflet.MagnifyingGlass](https://github.com/wandergis/Leaflet.MagnifyingGlass) - 放大镜插件, A plugin to add a customizable magnifying glass tool to a Leaflet map. forked from [bbecquet/Leaflet.MagnifyingGlass](https://github.com/bbecquet/Leaflet.MagnifyingGlass). 
- [leaflet-measure](https://github.com/jtreml/leaflet.measure) - 测量工具：Adds interactive distance measuring to leaflet
- [umap-project/Leaflet.Measurable](https://github.com/umap-project/Leaflet.Measurable) - 测量工具- Measure control for Leaflet made with Leaflet.Editable
- [leaflet-elevation](https://github.com/MrMufflon/Leaflet.Elevation) - 高程剖面
- [leaflet-image](https://github.com/mapbox/leaflet-image) - leaflet导出图片(无需服务端)	
- [leaflet-easyPrint](https://github.com/rowanwins/leaflet-easyPrint) - A leaflet plugin print the map 


## Leaflet路径规划
- [Leaflet Routing Machine](https://github.com/perliedman/leaflet-routing-machine) - Find the way from A to B on a Leaflet map. The plugin supports multiple backends:    
    * OSRM - builtin and used by default
    * GraphHopper - through plugin lrm-graphopper
    * Mapzen Valhalla - through plugin lrm-valhalla
    * Mapbox Directions API - through plugin lrm-mapbox
    * TomTom Online Routing API - through plugin lrm-tomtom by Mathias Rohnstock

## Leaflet搜索
- [Leaflet Search](https://github.com/smeijer/L.GeoSearch) - 地名搜索- Adds support for geocoding (address lookup, a.k.a. geoseaching) to Leaflet. contains three providers:    
    * L.GeoSearch.Provider.Esri
    * L.GeoSearch.Provider.Google
    * L.GeoSearch.Provider.OpenStreetMap
	
	 
## Leaflet图层编辑
- [leaflet-draw](https://github.com/Leaflet/Leaflet.draw) - Vector drawing and editing plugin for Leaflet
- [leaflet-freedraw](https://github.com/Wildhoney/Leaflet.FreeDraw) - freehand polygon creation using Leaflet.js and D3
- [leaflet-editable](https://github.com/Leaflet/Leaflet.Editable) - Make geometries editable in Leaflet	
- [leaflet-custom-paths](https://github.com/fstoerkle/leaflet-custom-paths) - Draw custom paths with the Leaflet mapping library


## leaflet library/js
- [leaflet&bootstrap](https://github.com/bmcbride/bootleaf) - A simple, responsive template for building web mapping applications with Bootstrap, Leaflet, and typeahead.js.
- [PaulLeCam/react-leaflet](https://github.com/PaulLeCam/react-leaflet) - React components for Leaflet maps
- [AngularJS-leaflet](https://github.com/tombatossals/angular-leaflet-directive) - AngularJS directive for the Leaflet Javascript Library. This software aims to easily embed maps managed by Leaflet on your project.
- [gwt-leaflet](https://github.com/kengu/gwt-leaflet) - GWT library for Leaflet
- [umap-project/Leaflet.Storage](https://github.com/umap-project/Leaflet.Storage) - Manage map and features with Leaflet and expose them for backend storage through an API. known backend is [django-leaflet-storage](https://github.com/yohanboniface/django-leaflet-storage) for now. 

## leaflet library集成
- [kartena/Proj4Leaflet](https://github.com/kartena/Proj4Leaflet) - This Leaflet plugin adds support for using projections supported by Proj4js. Features
    Supports all commonly used projections
    Extends Leaflet with full TMS support even for local projections
    Makes it easy to use GeoJSON data with other projections than WGS84
    Image overlays with bounds set from projected coordinates rather than LatLngs
- [leaflet-dvf](https://github.com/humangeo/leaflet-dvf) - Leaflet Data Visualization Framework - leaflet extension可视化框架
- [leaflet-echarts](https://github.com/wandergis/leaflet-echarts3) - 基于leaflet 扩展echarts，使ECharts的地图可以加到leaflet上, 大数据可视化big data visualization
- [Folium](https://github.com/python-visualization/folium) - Python Data. Leaflet.js Maps. Folium builds on the data wrangling strengths of the Python ecosystem and the mapping strengths of the Leaflet.js library. Manipulate your data in Python, then visualize it in on a Leaflet map via Folium.

## Leaflet开发者相关
- [leaflet-debug](https://github.com/aaronr/Leaflet.debug) - Debug plugin for the Leaflet mapping library
- [leafletjs-kit](https://github.com/jalbertbowden/leafletjs-kit) - LeafletJS Kit - Library, Demos, Tips, and Tools

	
## Leaflet Apps
- [leaflet-地图对比阅读](https://github.com/stamen/side-by-side) - Yet another side-by-side Leaflet viewer.
- [umap-project/umap](https://github.com/umap-project/umap) - uMap lets you create maps with OpenStreetMap layers in a minute and embed them in your site. It uses [django-leaflet-storage](https://github.com/umap-project/django-leaflet-storage) and [Leaflet.Storage](https://github.com/umap-project/Leaflet.Storage), built on top of Django and Leaflet.
- [wq.app](https://github.com/wq/wq.app) - [wq.app](https://wq.io/wq.app) is a suite of Javascript modules and related assets, created to facilitate the rapid deployment of offline-cabable HTML5 mobile and desktop data collection apps for crowdsourcing, citizen science, and volunteered geographic information, as well as professional field data collection.

