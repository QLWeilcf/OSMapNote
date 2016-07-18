
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

## Leaflet瓦片数据源
- [Leaflet-providers](https://github.com/leaflet-extras/leaflet-providers) - 免费瓦片数据源
- [中国地图瓦片服务](https://github.com/wandergis/Leaflet.ChineseTmsProviders) - 天地图、高德、MapABC
- [百度地图](https://github.com/sureleo/leaflet-baidu) - leaflet调用百度地图瓦片
- [腾讯地图](https://github.com/kennethhutw/leaflet-qq) - [调用腾讯地图瓦片](http://www.bubuko.com/infodetail-845917.html), 百度和腾讯地图[瓦片规则分析](http://blog.csdn.net/mygisforum/article/details/22997879). 
- [heigeo/leaflet.wms](https://github.com/heigeo/leaflet.wms) - A Leaflet plugin for working with Web Map services, providing: single-tile/untiled/nontiled layers, shared WMS sources, and GetFeatureInfo-powered identify
- [ESRI leaflet plugins](https://github.com/Esri/esri-leaflet) - 使用leaflet调用ArcGIS的基础底图和矢量服务的插件
- [Leaflet.Zoomify](https://github.com/turban/Leaflet.Zoomify) - Display [Zoomify](http://zoomify.com/) tiles with Leaflet. [More information](http://blog.thematicmapping.org/2013/06/showing-zoomify-images-with-leaflet.html).
- [leaflet-iip](https://github.com/astromatic/Leaflet.TileLayer.IIP) - Add [IIP](http://iipimage.sourceforge.net/) layering support to the Leaflet library
- [buche/leaflet-openweathermap](https://github.com/buche/leaflet-openweathermap) - A JavaScript library for including OpenWeatherMap's layers and OWM's current city/station data in leaflet based maps without hassle.
- [leaflet-layerConfig](https://github.com/Norkart/Leaflet-LayerConfig) - Library that communicates with a web service/reads a stored JavaScript object and adds layers to a leaflet map.
		
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
- [leaflet-textpath](https://github.com/makinacorpus/Leaflet.TextPath) - Show text along Polyline with Leaflet			
			
## Leaflet图层效果
- [leaflet-grayscale](https://github.com/Zverik/leaflet-grayscale) - A regular TileLayer with grayscale makeover. 灰度化
- [leaflet-tilefilter](https://github.com/humangeo/leaflet-tilefilter) - Change the appearance of Leaflet map tiles on the fly using a variety of canvas or CSS3 image filters. It's like Instagram for Leaflet map tiles.


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
	
## Leaflet heatmap
- [leaflet-heatmap](https://github.com/Leaflet/Leaflet.heat) - 热力图图层：A tiny, simple and fast heatmap plugin for Leaflet
- [webgl-heatmap-leaflet](https://github.com/ursudio/webgl-heatmap-leaflet) - draw hundreds of thousands of data points to a map using webgl


## Leaflet polyline 
- [leaflet-PolylineDecorator](https://github.com/bbecquet/Leaflet.PolylineDecorator) - 线图层简单符号化, a plug-in for the JS map library Leaflet, allowing to define patterns (like dashes, arrows, icons, etc.) on Polylines. 


## leaflet 动态数据/动画
- [Leaflet.AnimatedMarker](https://github.com/openplans/Leaflet.AnimatedMarker) - 点的沿线动画
- [leaflet-flyto](https://github.com/JackDougherty/leaflet-flyto) - Leaflet flyTo map demo
- [leaflet-realtime](https://github.com/perliedman/leaflet-realtime) - Put realtime data on a Leaflet map: live tracking GPS units, sensor data or just about anything.


## leaflet 功能
- [leaflet-easyButton](https://github.com/CliffCloud/Leaflet.EasyButton) - Easily Add Control Buttons with Font Awesome Icons and Callbacks
- [leaflet-contextmenu](https://github.com/aratcliffe/Leaflet.contextmenu) - 右键菜单：A context menu for Leaflet.
- [leaflet-zoom-extras](https://github.com/stamen/leaflet-zoom-extras) - Extends Leaflet's Zoom controller to allow for extra buttons
- [wandergis/Leaflet.MagnifyingGlass](https://github.com/wandergis/Leaflet.MagnifyingGlass) - 放大镜插件, A plugin to add a customizable magnifying glass tool to a Leaflet map. forked from [bbecquet/Leaflet.MagnifyingGlass](https://github.com/bbecquet/Leaflet.MagnifyingGlass). 
- [leaflet-measure](https://github.com/jtreml/leaflet.measure) - 测量工具：Adds interactive distance measuring to leaflet
- [leaflet-elevation](https://github.com/MrMufflon/Leaflet.Elevation) - 高程剖面
- [leaflet-image](https://github.com/mapbox/leaflet-image) - leaflet导出图片(无需服务端)	
- [leaflet-easyPrint](https://github.com/rowanwins/leaflet-easyPrint) - A leaflet plugin print the map 


## [Leaflet Routing Machine](https://github.com/perliedman/leaflet-routing-machine) - 路径规划, Find the way from A to B on a Leaflet map. The plugin supports multiple backends:
    * OSRM - builtin and used by default
    * GraphHopper - through plugin lrm-graphopper
    * Mapzen Valhalla - through plugin lrm-valhalla
    * Mapbox Directions API - through plugin lrm-mapbox
    * TomTom Online Routing API - through plugin lrm-tomtom by Mathias Rohnstock

## [Leaflet Search](https://github.com/smeijer/L.GeoSearch) - 地名搜索- Adds support for geocoding (address lookup, a.k.a. geoseaching) to Leaflet. contains three providers:
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
- [wq.app](https://github.com/wq/wq.app) - [wq.app](https://wq.io/wq.app) is a suite of Javascript modules and related assets, created to facilitate the rapid deployment of offline-cabable HTML5 mobile and desktop data collection apps for crowdsourcing, citizen science, and volunteered geographic information, as well as professional field data collection.

