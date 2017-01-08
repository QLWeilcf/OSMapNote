# 开源软件列表

## Saas
### 开源公司
- [Mapbox](https://www.mapbox.com/) - Helping you design your own map and presenting your data 提供地图瓦片服务、路径规划服务、地名搜索服务、在线制图服务以及私有地图服务器解决方案
	- [Mapbox GL](https://github.com/mapbox/mapbox-gl-native) -  Render Mapbox styles in mobile, desktop, and node applications using C++ and OpenGL 采用[矢量瓦片技术](https://github.com/phdbrianlee/OSMapNote/blob/master/mapbox/awesome-vector-tiles.md)
	- [Mapbox GL JS](https://github.com/mapbox/mapbox-gl-js) - Render Mapbox styles in the browser using JavaScript and WebGL 
	- [RasterIO](https://github.com/mapbox/rasterio) - 基于python的栅格数据读写/要素提取的库
	- [tile-reduce](https://github.com/mapbox/tile-reduce) - TileReduce: Distributed Spatial Data Processing in JavaScript across CPU cores, mapreduce vector tile processing, nodejs 
	- ......
- [Cartodb](http://cartodb.com/) - The easiest way to map and analyze your location data
	- [CartoDB](https://github.com/CartoDB/cartodb) - Location Intelligence & Data Visualization tool 
	- [CartoDB-SQL-API](https://github.com/CartoDB/CartoDB-SQL-API)
	- [Windshaft-cartodb](https://github.com/CartoDB/Windshaft-cartodb) 
	- [cartodb-pgsql](https://github.com/CartoDB/cartodb-postgresql) - PostgreSQL extension for CartoDB
	- [Cartodb data services api](https://github.com/CartoDB/dataservices-api) -  CartoDB Data Services SQL API (server and client FTM)
	- [Cartodb.js](https://github.com/CartoDB/cartodb.js) - CartoDB javascript library 
	- [Torque.js](https://github.com/CartoDB/torque) - Temporal mapping for CartoDB 
	- [odyssey.js](https://github.com/CartoDB/odyssey.js) - Making it easy to merge map and narrative 基于地图讲故事的Js库
	- [cartodb-qgis](https://github.com/gkudos/qgis-cartodb) - CartoDB Plugin for QGis
	- [cartodb-arcgis](https://github.com/gkudos/cartodb-toolbox) - CartoDB Toolbox for Arcgis
	- [cartodb-python](https://github.com/CartoDB/cartodb-python) - cartodb python client
	- [deepInsight.js](https://github.com/CartoDB/deep-insights.js) - Create powerful dashboards using CartoDB
	- [CartoDB Yeoman Generator](https://github.com/nerik/generator-cartodb) - [Yeoman](https://github.com/yeoman/yo) allows front-end developers to start new projects with a scaffolding to build on: a set of files, tools, and configuration adapted to every kind of website and app
	- [CartoDB Static Map](https://github.com/silverbiology/cartodb-staticmap-php) - CartoDB Static/printable Map is a PHP library that is used along with ImageMagick to merge individual tiles into one png image. 
	- [cartodb-publishing-templates](https://github.com/cartodb/cartodb-publishing-templates/) - CartoDB publishing templates: Editorial template, Sidepanel template, Double Map template.
	- [demo](https://github.com/CartoDB/cartodb-splunk) - A Splunk app for map visualizations using CartoDB by python
- [Mapzen](https://mapzen.com/) - an open, sustainable, and accessible mapping platform 开放的制图平台
- [Azavea](http://www.azavea.com/) - Azavea - Beyond dots on a map. Advanced GIS solutions	提供大数据和高级GIS分析解决方案

### 国外做地图比较好的公司
- [stamen](http://stamen.com/) - Data visualization to tell compelling stories for some of the world's most visible companies
- [thunder forest](http://www.thunderforest.com/) - Maps for your apps from United Kingdom
- [GIS Cloud](http://www.giscloud.com/) - A next generation platform for apps that manage location information
- [SpaceTimeInsight](http://www.spacetimeinsight.com/) - 大数据 + 数据可视化 + 地图 LBS 服务
- [MapLarge](http://www.maplarge.com/) - MAPPING PLATFORM FOR BIG DATA VISUALIZATION, ANALYTICS, & PUBLISHING
- [moonshadow mobile](http://www.moonshadowmobile.com/) - Big Data meets blazing-fast geospatial visualization

### 国内类似公司
- [Geohey](https://geohey.com) - A geographic online one-stop solution 
- [GeoQ](http://www.geoq.cn/) - A location intelligence platform 
- [地图慧](http://www.dituhui.com/) - A self-designed map server for customs
- [地图无忧](http://www.dituwuyou.com/) - A enterprise-level map service 

### 地图门户
- [worldmap](http://worldmap.harvard.edu/) - Building your own mapping portal and publish it to the world
- [MapStore]( http://mapstore2.geo-solutions.it/) - MapStore 2 is developed to create, save and share in a simple and intuitive way maps and mashup created selecting contents by server like Google Maps, OpenStreetMap, MapQuest or specific servers provided by your organization or third party. [MapStore后端](https://github.com/geosolutions-it/vibi) - VIBI - MapStore application and server backend code. [MapStore2](https://github.com/geosolutions-it/MapStore2) - Modern webmapping with OL3, Leaflet and React. [MapStoreMobile](https://github.com/geosolutions-it/MapStoreMobile)  an Android Application for mobile mapping. 
- [Maphubs](maphubs.com) - map for everyone, share data, tell map story. [maphub-portal](https://github.com/maphub/maphub-portal) - An online application for exploring and annotating digitized, high-resolution historic maps 高分辨率历史地图在线标注.
- [Map2Net](http://www.map2net.com/index_en.php) - Customize your own Geographical Information System thanks to Map2Net. Based on Cloud Technology, Map2Net allows you to create and personnalize your maps, import and visualize your data 
- [Maptube](http://maptube.org/) - MapTube is a free resource for viewing, sharing, mixing and mashing maps online. 


## 地名搜索服务
- Geocoding backend
	- [Nominatim](http://wiki.openstreetmap.org/wiki/Nominatim) - openstreetmap的地名搜索服务, [demo](http://nominatim.openstreetmap.org/), [docker镜像](https://github.com/nisaacson/nominatim-docker).  
	- [CartoDB geocoder](https://github.com/CartoDB/data-services) - CartoDB internal geocoder 已被CartoDB放弃
	- [Mapzen Search Pelias](https://github.com/pelias/pelias) - Pelias is a modular open-source geocoder using ElasticSearch for fast geocoding. Pelias地名搜索解决方案目前是比较好的一个实现，CartoDB公司2016年放弃自己的Geocode服务，使用了Mapzen的search服务, helvalius 开发了一个[Pelias docker](https://github.com/helvalius/pelias-docker) - Docker repository for the pelias geocoder. It is based on [pelias-data-container](https://github.com/HSLdevcom/pelias-data-container).  
	- [Twofishes](http://twofishes.net/) - A coarse(city/neighborhood/poi level, not street level) forward & reverse geocoder in scala. [git link](https://github.com/foursquare/twofishes).  
	- [Data Science Toolkit](http://www.datasciencetoolkit.org/) - 提供了数据科学的一些接口和数据, 如Street Address to Coordinates(英美), Google-style Geocoder, Coordinates to Political Areas, Text to Sentiment, Coordinates to Statistics, Geodict(从英文文本中识别地名并返回坐标), IP Address to Coordinates, Text to Sentences, HTML to Text, HTML to Story, Text to People(提取人名), Text to Times(提取时间), File to Text(PDF/Word/Excel-->txt).  [Git link](https://github.com/petewarden/dstk) 是 A collection of the best open data sets and open-source tools for data science, wrapped in an easy-to-use REST/JSON API with command line, Python and Javascript interfaces
	- [geocode.xyz](http://geocode.xyz/) - This API provides forward/reverse geocoding, batch geocoding and geoparsing for Europe.
	It geoparses locations from text, then geocodes each parsed location on a Map or in CSV, XML, JSON . 
	- [OpenCageData](https://geocoder.opencagedata.com/)提供了易用的geocoding API, 其后端由[Perl语言](https://github.com/OpenCageData/perl-Geo-Coder-OpenCage)开发 - Perl module for the OpenCage Geocoder 
- Geocoding Client 
	- [geopy] (https://github.com/geopy/geopy) - geopy is a Python 2 and 3 client for several popular geocoding web services. 支持调用OpenStreetMap Nominatim, ESRI ArcGIS, Google Geocoding API (V3), Baidu Maps, Bing Maps API, Mapzen Search, Yandex, IGN France, GeoNames, NaviData, OpenMapQuest, What3Words, OpenCage, SmartyStreets, geocoder.us, and GeocodeFarm geocoder services.
	- [node-geocoder](http://nchaulet.github.io/node-geocoder/) - Node library for geocoding and reverse geocoding.  支持调用google, here, freegeoip, datasciencetoolkit(IPv4 geocoding and address geocoding), OpenStreetMapGeocoder, mapquest, openmapquest, agol(ArcGis Online Geocoding service), tomtom, nominatimmapquest, opencage, smartyStreet, geocodio,yandex, teleport, opendata france等geocoding service. 

- Geocoding之上	
	- [Geoparser](https://github.com/memex-explorer/GeoParser) - Geoparser by python
	The Geoparser is a software tool that can process information from any type of file, extract geographic coordinates, and visualize locations on a map. Users who are interested in seeing a geographical representation of information or data can choose to search for locations using the Geoparser, through a search index or by uploading files from their computer. The Geoparser will parse the files and visualizes cities or latitude-longitude points on the map. After the information is parsed and points are plotted on the map, users are able to filter their results by density, or by searching a key word and applying a "facet" to the parsed information. On the map, users can click on location points to reveal more information about the location and how it is related to their search.
	- [GeoParser-lib](https://metacpan.org/pod/Geo::Parser::Text) - Geo::Parser::Text - Perl extension for parsing and geocoding locations from free form text.)
	- [geodict](https://github.com/petewarden/geodict) - A simple Python library/command-line tool for pulling location information from unstructured text

	
## 路径规划服务
- [Open Source Routing Machine](http://project-osrm.org/) - 基于OSM数据的导航计算引擎,目前由Mapbox主导开发
	- [osrm-backend](https://github.com/Project-OSRM/osrm-backend) - high performance routing engine written in C++11 designed to run on OpenStreetMap data. LUA. 包括docker file
	- [node-osm](https://github.com/Project-OSRM/node-osrm) - nodejs bindings
	- [frontend](https://github.com/Project-OSRM/osrm-frontend) - builds ontop of [Leaflet Routing Machine](https://github.com/perliedman/leaflet-routing-machine).
	- [isochrones](https://github.com/mapbox/osrm-isochrone) - Generate drivetime isochrones from OpenStreetMap data using OSRM	
	- [docker](https://github.com/acroca/osrm-docker) - 已测试过
	- [osrm.js](https://github.com/Project-OSRM/osrm.js) - REST client for the OSRM server API
- Mapzen Turn-by-Turn
	- [Mapzen Turn-by-Turn/Valhalla](https://mapzen.com/projects/valhalla/) -an Open Source Multimodal Routing engine and accompanying libraries for use with OpenStreetMap data. 
	- [Thor](https://github.com/valhalla/thor) - serves as a routing engine backed by tiled open source routing data. 
	- [docker镜像](https://github.com/valhalla/valhalla-docker)
	- [map match](https://github.com/valhalla/meili)
	- [map_matching](https://github.com/mapillary/map_matching) - map_matching is a Python library that associates locations to the underlying road network. work nicely with PostGIS and OSM road network to build real-world applications.
	- [Mjolnir](https://github.com/valhalla/mjolnir) serves as a set of applications suited to creating tiled routing data for use in the routing and searching projects under the valhalla organization
	- [loki](https://github.com/valhalla/loki) - Algorithms used to associate location information to an underlying graph
- GraphHopper 
	- [GraphHopper](https://graphhopper.com/) - GraphHopper is a fast and memory efficient Java road routing engine
	- [map match](https://github.com/graphhopper/map-matching) - Map Matching based on GraphHopper i.e. 'snap' GPX records to digital roads
	- [graphhopper-web-android](https://github.com/graphhopper/directions-api-java-client) - Java and Android client for the GraphHopper Directions API
	- [graphhopper-android](https://github.com/mayfourth/graphhopper-android) - Offline road routing example for Android using GraphHopper, Mapsforge and OpenStreetMaps 
- [pgRouting](http://pgrouting.org/)

## 地理大数据处理和可视化
- [GIS Tools for Hadoop](https://github.com/Esri/gis-tools-for-hadoop) - The GIS Tools for Hadoop are a collection of GIS tools that leverage the Spatial Framework for Hadoop for spatial analysis of big data. The tools make use of the Geoprocessing Tools for Hadoop toolbox, to provide access to the Hadoop system from the ArcGIS Geoprocessing environment. 
	- [spatial framework](https://github.com/Esri/spatial-framework-for-hadoop) - spatial analysis of big data
	- [geoprocessing](https://github.com/Esri/geoprocessing-tools-for-hadoop) -  to provide access to the Hadoop system from the ArcGIS Geoprocessing environment.
- [GeoMesa](https://github.com/locationtech/geomesa) - GeoMesa 是一个分布式时空数据库和计算框架，基于Apache Accumulo列式存储, GeoMesa在大规模数据集上实现了标准的Geotools接口,通过标准OGC的HTTP服务提供存储在Accumulo中的空间上数据,通过GeoServer管理界面监控集群. Geomesa之于Accumulo正如PostGIS之于PostgreSQL, 内核基于GeoHash索引, 采用scala语言开发, 支持集成GeoWave, 支持Spark/GeoTrellis框架
	- GeoMesa提供了[在线教程](https://github.com/geomesa/geomesa-tutorials). 
	- [Geoserver Docker-Image for GeoMesa](https://github.com/nik-ffm/docker-geoserver-geomesa) - This Container contains: GeoServer 2.8.2, WPS-Plugin, GeoMesa Extension. on top of geomesa 1.2.0, accumulo 1.6.2, hadoop 2.7.2, thrift 0.9.1, zookeeper 3.4.5 .
- [GeoTrellis](https://github.com/geotrellis/geotrellis) - 面向高性能应用的地理大数据处理引擎, 基于Scala开发, 支持各种空间操作，提供多种方式与地理空间数据交互,支持多核硬件和分布式服务器加速地理数据处理任务， 可以作为可安装的软件包部署，嵌入其他软件，或是部署到云环境中, 提供RestFul服务
	- [geotrellis-demo](https://github.com/geotrellis/geotrellis-chatta-demo) - Demo of GeoTrellis - weighted overlay and zonal summary
	-[Priority Places](https://github.com/geotrellis/priority-places)	- Asheville Priority Places application using GeoTrellis
	-[travelshed](https://github.com/geotrellis/geotrellis-transit) - API and libraries for generating travelsheds from OSM & GTFS data
	-[USACE analysis](https://github.com/azavea/usace-program-analysis-geoprocessing) and [flood model](https://github.com/azavea/usace-flood-geoprocessing) - USACE Program Analysis Geoprocessing, [spray](https://github.com/spray/spray) based.
	-[viewer](https://github.com/dwins/geotrellis-viewer) - Viewer is a tool for GeoTrellis administrators and developers to inspect ingested datasets in GeoTrellis.
	-[vagrant for geotrellis](https://github.com/geotrellis/vagrant.geotrellis) - A vagrant environment for doing GeoTrellis development.
	-[spark job server](https://github.com/spark-jobserver/spark-jobserver) - 用于提交和管理Apache Spark作业(job)、jar文件和作业上下文（SparkContext）的RESTful接口
- [GeoWave](https://github.com/ngageoint/geowave) - 基于Accumulo的多维时空索引、地理数据分布式处理, 是地理信息软件和分布式系统的桥梁, GeoServer 插件支持共享和可视化Accumulo中的地理数据; PDAL插件支持点云数据; Mapnik插件生成地图瓦片. 基于Java开发
	- [vagrant开发环境](https://github.com/ngageoint/geowave-vagrant) 		
	- [geowave osm](https://github.com/ngageoint/geowave-osm) - OSM Data processing for GeoWave 
	- [geowave docker](https://github.com/jamesmcclain/GeoWaveDocker) - A GeoWave Docker Image
	- [demo](https://github.com/venicegeo/geowave-demo-ui) - Simple demonstration app for showing off what GeoWave can do.
	- [geowave-geotrellis](https://github.com/radiantbluetechnologies/geowave-geotrellis) - 集成geowave and geotrellis 的尝试
	- [geowave-compare-geomesa](https://github.com/azavea/geowave-geomesa-comparative-analysis) - GeoWave/GeoMesa comparative analysis, aims to publish the results of this analysis in fall of 2016.
- [MrGeo](https://github.com/ngageoint/mrgeo) - MrGeo基于Hadoop和Spark的栅格数据计算套件, 支持可伸缩的栅格数据存储和处理，支持栅格地图代数运算，第三代数据存储模型(基于空间索引的分治；抽象层支持HDFS、Accumulo、HBASE), 支持TMS和WMS访问. [MrGeo related Docker版本](https://github.com/ericwood73/mrgeo-Docker).

- [Scale](https://github.com/ngageoint/scale) -算法容器化处理框架 Containerized processing framework for algorithms focused on remote sensing. Scale enables on-demand, near real-time, automated processing of large datasets (satellite, medical, audio, video, ...) using a dynamic bank of algorithms. Algorithm execution is seamlessly distributed across thousands of CPU cores. Docker provides algorithm containerization. Apache Mesos enables optimum resource utilization. With Scale you can:
    - Rapidly integrate algorithms written in Java, Python, IDL, Matlab, C/C++, ...
    - Compose complex algorithms using Recipes for advanced data processing
    - Increase your agility as an organization by running containerized developmental algorithms on the same cluster as operational algorithms
    - Adjust algorithm prioritization to ensure the most critical data is processed first
	
- [Nanocubes](http://www.nanocubes.net/) - 时空数据立方体 An in-memory data structure for spatiotemporal data cubes. [Github Link](https://github.com/laurolins/nanocube) Nanocubes provides you with real-time visualization of large datasets. Slice and dice your data with respect to space, time, or some of your data attributes, and view the results in real-time on a web browser over heatmaps, bar charts, and histograms. We've used it for tens of billions of data points: maybe you can push it even farther!

- [Lumify](http://lumify.io/) - open source big data analysis and visualization platform 大数据分析和可视化平台
- [Tessera](http://tessera.io/) - Open source environment for deep analysis of large complex data. There are three Tessera packages: [datadr](http://github.com/tesseradata/datadr)( support in-memory, local disk / multicore, and Hadoop back ends, with experimental support for Apache Spark), [Trelliscope](http://github.com/tesseradata/trelliscope)(D&R visualization tool), and [RHIPE](http://github.com/tesseradata/RHIPE)(R and Hadoop Integrated Programming Environment). 


- [MR4C](https://github.com/google/mr4c) - Map Reduce for C. [据称](https://gigaom.com/2015/02/18/google-open-sources-a-mapreduce-framework-for-c/)比Hadoop更快. 由卫星影像公司Skybox Imaging开发，被Google收购, 现更名为[Terra Bella](https://terrabella.google.com/). 包括了一些影像处理的算法. 

### 深度学习
- [docker-deep-learning](https://github.com/azavea/docker-deep-learning) - An environment for deep learning containing the following software packages: OpenBLAS, NumPy/SciPy, Theano, Keras, TensorFlow



## Storage/filesystem
- [glusterfs](https://github.com/gluster/glusterfs) - [GlusterFS](http://www.gluster.org/) is a scalable network filesystem. 
	- [glusterfs-deploy](https://github.com/gluster/gdeploy) - Tool to deploy glusterfs 
	- [Docker volume plugin for GlusterFS](https://github.com/calavera/docker-volume-glusterfs) - This plugin uses GlusterFS as distributed data storage for containers.
	- [Heketi](https://github.com/heketi/heketi) - Heketi provides a RESTful management interface which can be used to manage the life cycle of GlusterFS volumes. It support OpenStack Manila, Kubernetes, and OpenShift, supports any number of GlusterFS clusters. 
- [Torus](https://github.com/coreos/torus) - distributed storage coordinated through etcd for Kubernetes/container by CoreOS, see [oschina intro](http://www.oschina.net/p/torus). 
- [Ceph](https://github.com/ceph/ceph) - [Ceph](http://ceph.com) is a distributed object store and file system designed to provide excellent performance, reliability and scalability.
	- [Ceph-deploy](https://github.com/ceph/ceph-deploy) - Deploy Ceph with minimal infrastructure, using just SSH access
- [QFS](http://quantcast.github.io/qfs/) - Quantcast File System (QFS) is a high-performance, fault-tolerant, distributed file system developed to support MapReduce processing, or other applications reading and writing large files sequentially. [据称](https://gigaom.com/2012/09/27/quantcast-releases-bigger-faster-stronger-hadoop-file-system/)比HDFS更大、更快(读速度提高47%，写速度提高75%)、更强壮. 


## 数据库
- PostgreSQL and PostGIS
	- [PostGIS](http://postgis.net/) - 开源世界使用最多的空间数据库 PostgreSql [spatial extension](https://github.com/postgis/postgis).
	- [cartodb-postgresql](https://github.com/CartoDB/cartodb-postgresql) PostgreSQL的CartoDB拓展
	- [crankshaft](https://github.com/CartoDB/crankshaft) CartoDB的PostgreSQL空间分析拓展.
	- [Pointcloud](https://github.com/pgpointcloud/pointcloud) PostgreSQL的点云数据(LIDAR)存储拓展.
	- [3D City Database](https://github.com/3dcitydb/3dcitydb) 三维城市模型存储和表达，基于Oracle Spatial 或 PostGIS的CityGML存储.
	- [PostGIS Vector Tile Utils] (https://github.com/mapbox/postgis-vt-util) - 创建矢量瓦片数据源的系列PostgreSQL函数.
	- [lukasmartinelli/postgis-editor](https://github.com/lukasmartinelli/postgis-editor) - An accessible PostGIS query editor and visualizer, MapboxGL powered, 基于nodejs的桌面应用，适于学习PostGIS函数.
	- [NYCPlanning/postgis-preview](https://github.com/NYCPlanning/postgis-preview) - A lightweight express app and leaflet frontend for previewing PostGIS queries
	- [PostGIS tools](https://github.com/gacarrillor/postgis-layer-viewer) - A PostGIS layer viewer for pgAdmin3, based on PyQt4 and PyQGIS libs.

- SQLite and Spatialite
	- [SpatiaLite](http://www.gaia-gis.it/gaia-sins) - 轻量级的SQLite空间拓展.
    - [libspatialite](https://www.gaia-gis.it/fossil/libspatialite/index)
	- [python for Spatialite](https://github.com/lokkju/pyspatialite) 
	- [spatialite-android](https://github.com/geopaparazzi/libjsqlite-spatialite-android) 支持移动终端上使用Spatialite的库
    - [SpatiaLite Command Line Tools](https://www.gaia-gis.it/fossil/spatialite-tools/index)
    - [SpatiaLite Admin Tool](https://www.gaia-gis.it/fossil/spatialite_gui/index)
    - [MBtiles](https://github.com/mapbox/mbtiles-spec) - 基于SQlite的瓦片地图数据存储规范
- [Neo4j Spatial](https://github.com/neo4j-contrib/spatial) - Neo4j的空间操作库.
- [GeoCouch] (https://github.com/couchbase/geocouch) - Couchbase and Apache CouchDB的空间拓展.


## 网络地图瓦片地图服务器
### 栅格地图瓦片地图服务器(Raster map tile only)
- [gopnik](https://github.com/sputnik-maps/gopnik) - Gopnik is a high performance tile server and a render for slippy map based on mapnik library. It support 2.x and 3.x mapnik branches with distributed render balance and pluggable storage modules. 
- [GeoWebCache](https://github.com/GeoWebCache/geowebcache)- 基于Java的瓦片缓存服务器,支持WMS-C, TMS, WMTS, Google Maps, MS Bing. 
- [TileStream](https://github.com/cutting-room-floor/tilestream) - TileStream is a Node.js high-performance map tile server powered by [MBTiles](https://www.mapbox.com/help/an-open-platform/#mbtiles).
- [tilelite](https://github.com/springmeyer/tilelite) - A lightweight, multi-process, python wsgi tile-server using Mapnik. A gateway tool to TileStache or TileCache.
- [TileCache-Web Map Tile Caching](http://tilecache.org/) - a Python-based CGI [WMS-C/TMS server](https://github.com/cornel-iordache/tilecache), with pluggable caching mechanisms and rendering backends.
- [Tilestorm](https://github.com/cwygoda/tilestorm) - A Flask based tile server



### 矢量地图瓦片地图服务器
- [Tilelive](https://github.com/mapbox/tilelive) - Tilelive is a node.js map tile server, 是一个生态系统.tilelive源定义了读写瓦片的接口，有很多实现,used by mapbox. 
	- [node-mbtiles](https://github.com/mapbox/node-mbtiles) [mbtiles](http://mbtiles.org/) renderer and storage backend for tilelive
	- [node-tilejson](https://github.com/mapbox/node-tilejson) A javascript implementation of [tilejson spec](https://github.com/mapbox/tilejson-spec)
	- [tilelive-mapnik](https://github.com/mapbox/tilelive-mapnik) Mapnik Renderer backend for [tilelive.js](http://github.com/mapbox/tilelive.js) that uses [node-mapnik](http://github.com/mapnik/node-mapnik) to render tiles and grids from a Mapnik XML file.
	- [tilelive-vector](https://github.com/mapbox/tilelive-vector) Implements the tilelive API for rendering mapnik vector tiles to raster images.
	- [tilelive-bridge](https://github.com/mapbox/tilelive-bridge) Implements the tilelive API for generating mapnik vector tiles from traditional mapnik datasources.
	- 其他详见[Tilelive](https://github.com/phdbrianlee/OSMapNote/blob/master/mapbox/mapbox-tilelive.md). 
- [tilestrata](https://github.com/naturalatlas/tilestrata) - A pluggable Node.js map tile server, 插件式网络瓦片服务器
	- [tilestrata-mapnik](https://github.com/naturalatlas/tilestrata-mapnik) – Render tiles with [mapnik](http://mapnik.org/).
	- [tilestrata-disk](https://github.com/naturalatlas/tilestrata-disk) – Cache map tiles to the filesystem (or serve from it)
	- [tilestrata-dependency](https://github.com/naturalatlas/tilestrata-dependency) – Fetch tiles from other layers.
	- [tilestrata-sharp](https://github.com/naturalatlas/tilestrata-sharp) – Compress, resize, transcode tiles (jpg, png, webp) using [libvips](https://www.npmjs.com/package/sharp).
	- [tilestrata-gm](https://github.com/naturalatlas/tilestrata-gm) – Perform all sorts of image operations on tiles using [GraphicsMagick](https://www.npmjs.com/package/gm).
	- [tilestrata-headers](https://github.com/naturalatlas/tilestrata-headers) – Set/override response headers.
	- [tilestrata-blend](https://github.com/naturalatlas/tilestrata-blend) – Stack multiple layers together.
	- [tilestrata-jsonp](https://github.com/naturalatlas/tilestrata-jsonp) – Serve utfgrids (and other JSON) as JSONP.
	- [tilestrata-datadog](https://github.com/naturalatlas/tilestrata-datadog) – Send timing information to [Datadog](https://www.datadoghq.com/).
	- [tilestrata-utfmerge](https://github.com/naturalatlas/tilestrata-utfmerge) – Merge UTF interactivity grids from mapnik.
	- [tilestrata-vtile](https://github.com/naturalatlas/tilestrata-vtile) – Outputs mapnik vector tiles (protobufs).
	- [tilestrata-vtile-raster](https://github.com/naturalatlas/tilestrata-vtile-raster) – Renders mapnik vector tiles into raster images.
	- [tilestrata-vtile-composite](https://github.com/naturalatlas/tilestrata-vtile-composite) – Merge multiple vector tiles.
	- [tilestrata-proxy](https://github.com/naturalatlas/tilestrata-proxy) – Fetches tiles from other servers
	- [tilestrata-lru](https://github.com/naturalatlas/tilestrata-lru) – Caches tiles in memory (LRU)
	- [tilestrata-etag](https://github.com/naturalatlas/tilestrata-etag) – Configurable Conditional GET support (with ETags)
	- [tilestrata-bing](https://github.com/naturalatlas/tilestrata-bing) – Provider for Bing Maps tiles	
- [tessera](https://github.com/mojodna/tessera) - 基于[tilelive](https://github.com/mapbox/tilelive.js)的瓦片服务器
- [tileserver-php](https://github.com/klokantech/tileserver-php) - 支持MBTiles(支持栅格瓦片和矢量瓦片), TileJSON, OGC WMTS, UTFGrid interaction. 
- 基于PG数据库的矢量瓦片地图服务
	* [TileStache](https://github.com/mapzen/TileStache/) - 基于Python的瓦片地图服务器，支持动态生成瓦片，支持矢量栅格瓦片，支持多种矢量数据源（包括PG）.
	* [PGRestAPI] (https://github.com/spatialdev/PGRestAPI) - 从PostGIS数据库中生成矢量瓦片并提供服务 Node.js REST API.
	* [tilesplash](https://github.com/faradayio/tilesplash) - a light and quick nodejs webserver for serving topojson vector tiles from a postgis backend
	* [utilery] (https://github.com/tilery/utilery) - 从PostGIS数据库中生成矢量瓦片并提供服务. python 3.4 
	* [aiovectortiler](https://github.com/shongololo/aiovectortiler) - An asynchronous micro vector tile application that serves geojson and MVT compatible vector tiles from PostGIS.
	* [Tegola](https://github.com/terranodo/tegola) - Tegola is a high performance vector tile server delivering Mapbox Vector Tiles leveraging PostGIS as the data provider in pure Go.
	
- 基于Mapbox GL Native引擎的瓦片地图服务器
	* [tileserver-gl](https://github.com/klokantech/tileserver-gl) - Map hosting software for vector tiles, able to rasterize on server side. The same map style (JSON GL) served to web (MapBox GL JS), mobile apps (Android/iOS), and rendered on server into traditional mapping services (raster tiles, WMTS, Static Maps API) using MapBox GL Native. docker support. 
	* [tileserver-gl-light](https://github.com/osm2vectortiles/tileserver-gl-light) - A trimmed down fork of [tileserver-gl](https://github.com/klokantech/tileserver-gl) for serving MBTiles and predefined Mapbox GL styles. Built to support serving vectortiles from OSM2VectorTiles.
	* [docker-tileserver-gl-light](https://github.com/stirringhalo/docker-tileserver-gl-light) - Dockerfile for deploying tileserver-gl-light from osm2vectortiles. a containerized [tileserver-gl-light](https://github.com/osm2vectortiles/tileserver-gl-light)!	
	
### DEM瓦片服务 - Terrain(DEM) Tile
- [Cesium地形服务器](https://github.com/geo-data/cesium-terrain-server) - A basic server for serving up filesystem based tilesets representing Cesium.js terrain models. 
- [Cesium Terrain Builder](https://github.com/geo-data/cesium-terrain-builder) - a C++ library and associated command line tools designed to create terrain tiles for use with the Cesium JavaScript library. and also [GDAL2Cesium](https://github.com/giohappy/gdal2cesium) by python.

### 分布式瓦片地图渲染之队列式解决方案
- [Tile Squirrel - nodejs](https://github.com/trailbehind/tile-squirrel) - Tile Squirrel is designed to render map tiles in bulk across multiple hosts. Tiles are added to a queue, and then one or more workers can read from the queue and render tiles. RabbitMQ is used for queuing, and tilelive is used for sources and destinations for tiles.
- [TileQueue](https://github.com/mapzen/tilequeue) - 基于python的瓦片渲染队列操作-Queue operations to manage the processes surrounding tile rendering using redis.
- [celery-tiles](https://github.com/fladi/celery-tiles) - celery-tiles is a distributed tile renderer using celery tasks. It provides a CLI interface and Django command integration to validate and reproject raster input that can be read by GDAL. It using [GlusterFS](http://www.gluster.org/) as shared storage. 
- [Pyler](https://github.com/keyz182/Pyler) - A python distributed tile rendering server using Tornado, Celery, redis and mapnik

### 分布式瓦片地图渲染之Hadoop/Spark解决方案
- [Tilebrute - hadoop](https://github.com/ndimiduk/tilebrute) - Tilebrute is an experiment in rendering map tiles using Hadoop. It's built in Python with a touch of Java. It leans heavily on GDAL and Mapnik. 
- [MrGeo - spark](https://github.com/ngageoint/mrgeo) - MrGeo is an open source geospatial toolkit designed to provide raster-based geospatial processing capabilities performed at scale. MrGeo enables global geospatial big data image processing and analytics.
MrGeo is built upon the Apache Spark distributed processing frarmework to leverage the storage and processing of 100’s of commodity computers. Functionally, MrGeo stores large raster datasets as a collection of individual tiles stored in Hadoop to enable large-scale data and analytic services. Used by digital globe company. 
- [MR4C – 类hadoop](https://github.com/google/mr4c) - MR4C is a framework for running C/C++ libraries on an Hadoop Cluster using Yarn. MR4C enables large-scale deployment of advanced image data processing applications using gdal.
- [Geotrellis - spark] 

### 瓦片地图配套服务
- [Scoville](https://github.com/tilezen/scoville) - A simple little script to collect tile statistics.
- [ericfischer/tile-stitch](https://github.com/ericfischer/tile-stitch) - Stitch together and crop map tiles for a specified bounding box using C. 
- [TileCloud](https://github.com/sbrunner/tilecloud) - A powerful python utility for generating, managing, transforming, and visualizing map tiles in multiple formats. It can create, read update, delete tiles in multiple back ends, called TileStores. 
- [Tile Tracking](https://github.com/Erodenberg/TileTracking10.2) - Tile Tracking allows organizations to use Tile Analysis Modeling to track tile usage using ArcGIS Server and Geoprocessing.
	
	
## 各种OGC和类似服务
- OGC WMS
	- [Ogcserver] (https://github.com/mapnik/OGCServer) - Python WMS implementation using Mapnik( >= 0.7.0).	
	- [landspeed.js](https://github.com/mapbox/landspeed.js) - WMS server using node-mapnik
	- [Eoxserver](https://github.com/EOxServer/eoxserver) - EOxServer is a Python application and framework for presenting Earth Observation (EO) data and metadata. [EOxServer](http://eoxserver.org)实现了OGC EO-WCS 和EO-WMS规范, EOxServer基于MapServer, Django/GeoDjango, GDAL, SpatiaLite, or PostGIS, and PROJ.4构建.
	- [onearth](https://github.com/nasa-gibs/onearth) - High-performance web services for tiled raster imagery using c and python, apache-based. 

- OGC CSW	
	- [pycsw](https://github.com/geopython/pycsw) - [pycsw](http://pycsw.org/) is an OGC CSW server implementation written in Python.  Started in 2010 (more formally announced in 2011), pycsw allows for the publishing and discovery of geospatial metadata, providing a standards-based metadata and catalogue component of spatial data infrastructures. 	
	- [Geonetwork](http://geonetwork-opensource.org/) - GeoNetwork is a catalog application to manage spatially referenced resources. It provides powerful metadata editing and search functions as well as an interactive web map viewer. It is currently used in numerous Spatial Data Infrastructure initiatives across the world. Java-based. 支持本地和分布式地理数据目录搜索，支持上传、下载数据、文档等，具有基于WMS的交互式Web Map Viewer, 元数据在线修改与同步, 支持OGC-CSW 2.0.2 , OAI-PMH, Z39.50 protocols, 权限控制和多语言UI.
- OGC WFS-T
	- [TinyOWS](https://github.com/mapserver/tinyows) - TinyOWS is a simple WFS-T server based on PostGIS spatial database
- RESTful Feature Services
	- [FeatureServer](https://github.com/iocast/featureserver) - [FeatureServer](http://featureserver.org/) is an implementation of a RESTful Geographic Feature Service. Using standard HTTP methods, you can fetch a representation of a feature or a collection of features, add new data to the service, or delete data from the service. Use it as an aggregator -- post your GeoRSS feeds to it, and then browse them using WFS. Use it as a translator: use the OGR DataSource to load a shapefile and open it in Google Earth.
	- [tobinbradley/dirt-simple-postgis-http-api](https://github.com/tobinbradley/dirt-simple-postgis-http-api) - Dirt Simple PostGIS HTTP API is an easy way to expose geospatial functionality to your applications. It takes simple requests over HTTP and returns JSON, JSONP, or protobuf (Mapbox Vector Tile) to the requester. This release uses Node. The previous release, based on PHP, is available in the v1 branch. The [Docker container for dirt-simple-postgis-http-api](https://github.com/sttts/docker-postgis-restful-web-service) version is based on php. Here is also a [fork - neverrun/backend](https://github.com/neverrun/backend) of php version.
- OGC WPS
	- [PyWPS](http://pywps.org/) is an implementation of the Web Processing Service standard from the Open Geospatial Consortium. [PyWPS](https://github.com/geopython/pywps) is written in Python. [PyWPS-Demo](http://geopython.github.io/pywps-demo/docs/_build/html/) using flask framework.
	- [Zoo project](http://zoo-project.org/) - [ZOO](https://github.com/kalxas/zoo-project) is an WPS (Web Processing Service) Platform. It provides an OGC WPS compliant developer-friendly framework to create and chain WPS Web services. 
	- [52 north wps](https://github.com/52North/WPS) - 52°North Web Processing Service enables the deployment of geo-processes on the web in a standardized way. Java-based. 支持WPS1.0.0，插件式算法框架，基于JTS、GeoTools等库，支持WPS-T. 支持多种地理计算后端: WPS4R - R Backend; GRASS; 220+ SEXTANTE Processes; ArcGIS Server Connector; Moving Code backend-Python. 
- OGC Sensor	
	- [OGC SOS](https://github.com/52North/SOS) - 52°North Sensor Observation Service (SOS)
	- [sos-js](https://github.com/52North/sos-js) - Javascript library to browse, visualise, and access, data from an OGC Sensor Observation Service.
	- [Open Sensor Search](https://github.com/52North/OpenSensorSearch) - is a platform for sensor discovery across all sensor web supporting major specifications (OGC SWE) and popular IoT websites
	- [OGC SPS](https://github.com/52North/SensorPlanningService) - 52°North Sensor Planning Service (SPS)
	- [istSOS](http://www.istsos.org/) - istSOS is an OGC SOS server implementation. Easily manage your sensor network and distribute your data in a standard way. It is [open source](https://github.com/istSOS) and written in Python. 遵循OGC标准，具有管理界面，提供Restful API. 
	
- OGC基础库和服务状态检查	
	- [OWSLib](https://github.com/geopython/OWSLib) - OWSLib is a Python package for client programming with Open Geospatial Consortium (OGC) web service (hence OWS) interface standards, and their related content models.
	- [pygeometa](https://github.com/geopython/pygeometa) - pygeometa is a Python package to generate metadata for geospatial datasets
	- [GeoHealthCheck](https://github.com/geopython/GeoHealthCheck) - Service Status Checker for OGC Web Services. 服务状态检查

## 地图数据共享解决方案
- [geonode](http://geonode.org/)  地理空间数据创建、共享和协作平台
	- [GeoNode](https://github.com/GeoNode/geonode) is an open source platform that facilitates the creation, sharing, and collaborative use of geospatial data. GeoNode is an Open Source Geospatial Content Management System. GeoNode is a web-based application and platform for developing geospatial information systems (GIS) and for deploying spatial data infrastructures (SDI). Developed with Django.
	- [cga-WorldMap](https://github.com/cga-harvard/cga-worldmap) - [WorldMap](http://cga.harvard.edu) is being made available by Harvard's Center for Geographic Analysis to lower the barrier for scholars and others who wish to explore, visualize, edit, collaborate with, and publish geospatial information. It is based on [GeoNode](https://github.com/GeoNode/geonode).  	
- [cga-harvard/HHypermap](https://github.com/cga-harvard/HHypermap) - 地图服务注册、正常运行时间统计 HHypermap (Harvard Hypermap) Registry is an application that manages OWS, Esri REST, and other types of map service harvesting, and maintains uptime statistics for services and layers. HHypermap Registry will publish to HHypermap Search (based on Lucene) which provides a fast search and visualization environment for spatio-temporal materials. 

## 地图瓦片在线纠正服务
- [Map Warper](https://github.com/timwaters/mapwarper) - Mapwarper is an open source map geo-rectification, warping and georeferencing application. It enables a user to upload an image, a scanned map or aerial photo for example, and by placing control points on a reference map and the image, to warp it, to stretch it to fit. The application can be seen in use at http://mapwarper.net for public use. Ruby and Rails. 
- [纽约市时空目录](http://spacetime.nypl.org/) is turning historical maps and other geographic sources into a digital time-travel service for New York City
	* [NYPL Map Warper](https://github.com/nypl-spacetime/nypl-warper) - by Topomancy LLC for the New York Public Library. You can see this code in action at http://maps.nypl.org/. it is also based on [Map Warper](https://github.com/timwaters/mapwarper).  Ruby and Rails.  
	* [the NYPL Map Vectorizer](https://github.com/nypl-spacetime/map-vectorizer) - An open-source map vectorizer, Map polygon and feature extractor, Like OCR for maps, 地图多边形要素提取, based on [opencv](http://opencv.org/) and [PIL](http://pythonware.com/products/pil/). 
	* [mask-to-geojson](https://github.com/nypl-spacetime/mask-to-geojson) - Converts Mapwarper GML masks to GeoJSON polygons
	* [CRF Classify](https://github.com/nypl-spacetime/crf-classify) - Simple crowdsourcing tool for classifying and labeling training data for a conditional random field model (CRF) - used in Space/Time Directory project to extract data from digitized New York City city directories.
	* [Histograph](http://histograph.io/) - geocoding places of the past, 基于图数据库的今古地名链接. Histograph uses Neo4j and Elasticsearch to expose a web of interlinked toponyms - in space and time. These are made searchable through an API; and web applications enable geo-temporal search, visualization and analysis for librarians and archivists. Histograph consists of [more than 20 repositories](https://github.com/histograph/histograph). nodejs. 
	* [oldnyc](https://github.com/nypl-spacetime/oldnyc) - Mapping photos of Old New York, Live site: http://www.oldnyc.org
- [Maptcha Version 2](https://github.com/stamen/maptcha-v2) - Maptcha Version 2 is a map warping tool based on Maptcha and Stamen's previous work with NYPL/Stanford. Stamen has developed an independent application tailored to the needs of map collections, focusing on both the rectification interface and the old map selection process. python based. 
- [MapKnitter](http://github.com/publiclab/mapknitter) - [Make maps from aerial photos](http://mapknitter.org).  Use Public Lab's MapKnitter to upload your own aerial photographs (for example those from [balloon or kite mapping](http://publiclab.org/wiki/balloon-mapping) ) and combine them into web "slippy maps" like Google Maps, GeoTiff, TMS, high resolution JPEG. share via web or composite and export for print. Ruby on Rails apps. 
- [Map-georeferencer](https://github.com/Viglino/Map-georeferencer) - A proof of concept to georeference maps with OpenLayer3 based on [Helmert](https://en.wikipedia.org/wiki/Helmert_transformation) or affine transform..
- Georeferencer plugin for QGIS
	* [mmassing/georeferencer](https://github.com/mmassing/georeferencer) - Georeferencer plugin for QuantumGIS	
	* [FreehandRasterGeoreferencer plugin for QGIS](https://github.com/gvellut/FreehandRasterGeoreferencer) - Interactive georeferencing of rasters for QGIS
	* [lynx-r1/georeferencer](https://github.com/lynx-r1/georeferencer) 
	* [pyarchinit/vector_georeferencer_plugin](https://github.com/pyarchinit/vector_georeferencer_plugin)
- python script for Georeferencer	
	* [GeoRef](https://github.com/karimbahgat/GeoRef) - A pure-Python offline georeferencer
	* [autogeoreferencer](https://github.com/willcodeforfoo/autogeoreferencer) - An automated georeferencer based on Li and Briggs' 2006 paper "Automated Georeferencing Based on Topological Point Pattern Matching"
- 古地图变形分析服务
	* [MapAnalyst](http://mapanalyst.org/) - MapAnalyst is a software application for the accuracy analysis of old maps. Its main purpose is to compute distortion grids and other types of visualizations that illustrate the geometrical accuracy and distortion of old maps. It is based on Java. [Source code here](http://mapanalyst.org/MapAnalystSrc.zip). 
	* [mapanalyst.mzk.cz](https://github.com/moravianlibrary/mapanalyst.mzk.cz) - dockerized Web service for map analysis. It is based on MapAnalyst software. The running instance listens on url http://mapanalyst.mzk.cz
	
 
## 地图渲染引擎和工具
- [mapnik及其bindings](http://mapnik.org/) - Mapnik combines pixel-perfect image output with lightning-fast cartographic algorithms, and exposes interfaces in C++, Python, Ruby, and Node
	* [mapnik-node](https://github.com/mapnik/node-mapnik) - Bindings to mapnik for node.js
	* [mapnik-python](https://github.com/mapnik/python-mapnik) - Python bindings for mapnik 
	* [mapnik-ruby](https://github.com/mapnik/Ruby-Mapnik) - Ruby bindings for mapnik 
	* [mapnik-golang](https://github.com/fawick/go-mapnik) - Go bindings for mapnik 2.2 and Mapnik 3.0. and [omniscale-mapnik-go](https://github.com/omniscale/go-mapnik)
	* [mapnik-geowave-input-plugin](https://github.com/mapnik/geowave-plugin) - GeoWave(>= 0.8.7) Plugin is an open source input plugin for Mapnik(>= 3.0.8). 
    * [mapnik-docs](https://github.com/mapnik/documentation) -  A home Mapnik-related documentation
	* [mapnik-reference](https://github.com/mapnik/mapnik-reference) -  JSON specification of Mapnik styling and datasources
	* [mapnik-pool](https://github.com/mapbox/mapnik-pool) - manage a pool of mapnik map instances node.js
- [WebGL-based Map Engine]
	* [Mapbox GL Native] (https://github.com/mapbox/mapbox-gl-native) - Render Mapbox styles in mobile, desktop, and node applications using C++ and OpenGL.
	* [Mapzen Tangram-ES] (https://github.com/tangrams/tangram-es) - C++ library for rendering 2D and 3D maps using OpenGL ES 2 with custom styling and interactions
- [Windshaft map tiler](https://github.com/CartoDB/Windshaft) - A Node.js highspeed map tile library for PostGIS and torque.js, with CartoCSS styling, use redis to store the Layergroups configuration.
	- [cartochet](https://github.com/frensley/cartochet) - Windshaft and Leaflet, Simple client server example using Windshaft layer groups
	- [Steven-Tiler-docker](https://github.com/TerraSeer/steven-tiler) - A rock-solid map tiling server based on Windshaft. with docker compose supported. 
	- Docker for Windshaft, See [terraSeer/docker-windshaft](https://github.com/TerraSeer/docker-windshaft) and [azavea/docker-windshaft](https://github.com/azavea/docker-windshaft).  
- [Mapnik-based Map Design Tools]	
	* [TileMill](http://tilemill.com) the github code [link](https://github.com/mapbox/tilemill) - Creating beautiful interactive maps with CartoCSS
	* [Mapbox Studio classic] (https://github.com/mapbox/mapbox-studio-classic) - Desktop application for vector tile driven map design.
	* [Kosmtik] (https://github.com/kosmtik/kosmtik) - Very lite but extendable mapping framework to create Mapnik ready maps with OpenStreetMap data (and more), nodejs.
- [Map Styles Tools]
	* [Magnacarto](https://github.com/omniscale/magnacarto) - Magnacarto is a CartoCSS map style processor that generates Mapnik XML and MapServer map files. Go 语言. 	
	* [Grainstore](https://github.com/CartoDB/grainstore) - Grainstore is an opinionated Carto MML style store for PostGIS tables, views or sql queries that outputs Mapnik XML stylesheets. It is used to generate a Mapnik map from a dynamic PostGIS table.
    * [stirringhalo/mapbox-gl-style-editor](https://github.com/stirringhalo/mapbox-gl-style-editor) - A simple editor for Mapbox gl styles. Allows you to open an style file and edit the raw json data and see how the changes affects the map. Useful if you have exported a style from Mapbox Studio and want to edit it. And a [dockerized version here](https://github.com/stirringhalo/docker-mapbox-gl-style-editor).
	* [tobinbradley/mapbox-gl-style-editor](https://github.com/tobinbradley/mapbox-gl-style-editor) - A basic code editor for Mapbox Gl Styles using node. Support for font processing via [genfontgl](https://github.com/sabas/genfontgl); Support for SVG processing via [spritezero-cli](https://github.com/mapbox/spritezero-cli). 


## 全功能网络地图服务器
- [MapServer](http://www.mapserver.org/) - Publishing spatial data and interactive mapping applications to the web
- [GeoServer](http://geoserver.org/) - An open source server for sharing geospatial data
- [deegree](http://www.deegree.org/) - An open source software for spatial data infrastructures and the geospatial web
- [GeoDjango](http://geodjango.org/) - A GIS server built with python web framework -- django
- [geomajas](http://www.geomajas.org/) - An open source platform to create Web GIS applications 
- [GeoMOOSE](http://www.geomoose.org/) - A Web Client JavaScript Framework for displaying distributed cartographic data
- [MapFish](http://www.mapfish.org/) - A framework for building rich web-mapping applications built with Pylons Python web framework
- [MapGuide ](http://mapguide.osgeo.org/) - A Web Client JavaScript Framework for displaying distributed cartographic data



## web前端开发框架
### 2D web地图前端开发框架
- 基于Canvas和SVG
	- [Leaflet](http://leafletjs.com/) - Open-source javaScript library for mobile-friendly interactive maps
	- [Leaflet-MapboxVectorTile](https://github.com/SpatialServer/Leaflet.MapboxVectorTile) - 支持矢量切片的Canvas渲染
	- [OpenLayer3](http://openlayers.org/) - Open-source javascript map viewing library
	- [Polymaps](http://polymaps.org/) - A JavaScript library for image- and vector-tiled maps using SVG
	- [D3.js](https://d3js.org/) - A javascript library for manipulating documents based on data
	- [d3-carto-map](https://github.com/emeeks/d3-carto-map) - A library for creating layer-based maps using D3
	- mapsense.co -- data driven mapping based on D3.js, 已被苹果公司收购
	- [Echarts](http://echarts.baidu.com/) - A user-friendly data visualisation library supported by Baidu

- 基于WebGL
	- [Mapbox GL](https://github.com/mapbox/mapbox-gl-js) - 根据Mapbox GL Style规范从Mapbox矢量瓦片渲染交互地图的JavaScript库
	- [TangramJS](https://github.com/tangrams/tangram) - 实时渲染2D & 3D地图的JavaScript库- Real-Time WebGL Maps
- 一些库
	- [geojson-vt] (https://github.com/mapbox/geojson-vt) - A highly efficient JavaScript library for slicing GeoJSON data into vector tiles on the fly.
	- [Leaflet.MapboxVectorTile] (https://github.com/SpatialServer/Leaflet.MapboxVectorTile) - A Leaflet Plugin that renders Mapbox Vector Tiles on HTML5 Canvas.

	
### 2D web地图前端部分库
- [turf.js](http://turfjs.org/) - Advanced geospatial analysis for browsers and node supported by Mapbox, talks see [here](https://github.com/morganherlocker/talks).
- [JSTS] (https://github.com/bjornharrtell/jsts) - Port of the Java JTS library.
- [Heatmap.js] (https://www.patrick-wied.at/static/heatmapjs/) - A heatmap implementation for Javascript.
- [Thermo.js] (https://github.com/dazuma/thermo.js) - Another heatmap implementation for Javascript.
- [Heatcanvas.js] (https://github.com/sunng87/heatcanvas) - Yet another heatmap implementation for Javascript.
- [Dropchop](dropchop.io) - Developed by Sam Matthews of Code for America and powered by Mapbox.js and Turf.js, it’s a browser-based application that enables users to simply drag-and-drop shapefiles into the browser and execute spatial analysis tools without the need for desktop GIS. Dropchop is meant to be a data-first tool, as opposed to operation-first (traditionally most desktop GIS software) in that the spatial analysis operations are contextually based what can be done with the data.



### 3D web前端开发框架
- Library
	- [three.js](http://threejs.org/) - A javascript 3D library which makes WebGL simpler
	- [vizicities](https://github.com/vizicities/vizicities) - 3D city and data visualisation platform based on three.js 
	- [cesiumjs](https://cesiumjs.org/) - An open-source JavaScript library for world-class 3D globes and maps
	- [TerriaJS](https://github.com/TerriaJS/TerriaJS) 二三维一体化 is a library for building rich, web-based geospatial data explorers. It uses Cesium for a full 3D experience. Think Google Earth, except it runs in a web browser without a plugin. It also uses Leaflet for a basic 2D experience on systems that can't run Cesium. [Terria](terria.io) is a spatial data platform that provides spatial predictive analytics. It is closed-source. 	
	- [cesium-vr](https://github.com/NICTA/cesium-vr) - A plugin for Cesium WebGL Virtual Globe to support VR devices using a VR-enabled browser.
- Apps  
	- [卫星过境](https://github.com/nasa-gibs/data-curtains) - Exploring data curtains using Cesium
	- [Australian national map](http://nationalmap.gov.au) 

### 街景web前端开发框架
- [mapillary](https://github.com/mapillary/mapillary-js)

	
## Mobile Development
- [Mapbox Android SDK] (https://www.mapbox.com/android-sdk/) - An open source toolset for building mapping applications for Android devices.
- [Mapbox iOS SDK] (https://www.mapbox.com/ios-sdk/) - An open source toolset for building mapping applications for iPhone and iPad devices.
- [WhirlyGlobe/Maply] (http://mousebird.github.io/WhirlyGlobe/) - Objective C code that is able to read and render vector tiles(and style with mapnik xml) on iOS/Android devices.
- [Mapzen Android](https://github.com/mapzen/android) -  Mapzen Android SDK is a thin wrapper that packages up everything you need to use Mapzen services in your Android applications.

	
## 地理空间数据处理的基础库-Library
- C/C++
	- [GDAL](http://www.gdal.org/) - A translator library for raster and vector geospatial data formats. [Cheat sheet for GDAL/OGR command-line tools](https://github.com/dwtkns/gdal-cheat-sheet) and [recipes for using the Python GDAL/OGR bindings](https://github.com/pcjericks/py-gdalogr-cookbook).
	- [GEOS] (https://trac.osgeo.org/geos/) - GEOS (Geometry Engine - Open Source) is a C++ port of the Java Topology Suite (JTS).
	- [Proj.4](https://github.com/OSGeo/proj.4) - A library for cartographic projection
	- [libspatialindex] (https://github.com/libspatialindex/libspatialindex) - C++ implementation of R*-tree, an MVR-tree and a TPR-tree with C API. [python wrapper by Toblerity](https://github.com/Toblerity/Rtree)
	- [Spatial] (https://sourceforge.net/projects/spatial/) - Spatial is a generic header-only C++ library providing multi-dimensional in-memory containers, iterators and functionals.
	- [GeoTools](http://www.geotools.org/) - An open source Java library that provides tools for geospatial data
	- [Orfeo toolbox](https://www.orfeo-toolbox.org/) - An open-source C++ library for remote sensing images processing
	- [Terralib] (http://www.terralib.org/) - TerraLib is a GIS classes and functions open source library.
	- [GeographicLib] (http://geographiclib.sourceforge.net/) - For solving geodesic problems. Implemented in C, C++, Java, Javascript, Fortran, Python and Matlab. 
	- [Geolib] (http://www.geolib.co.uk/) - GeoLib is a fast, efficient, computational geometry library available in C++, C# and Java.
	- [Mapnik Vector Tile] (https://github.com/mapbox/mapnik-vector-tile) - Mapnik C++ implemention of Mapbox Vector Tile specification.
- Python
	- [Shapely](https://github.com/Toblerity/Shapely) - A library for manipulation and analysis of geometric objects in the Cartesian plane
	- [Fiona](http://github.com/toblerity/fiona/) - IO for GIS Data writted by Python
	- [Cartopy] (http://scitools.org.uk/cartopy/) - A library providing cartographic tools for python for plotting spatial data.
	- [Rasterio] (https://github.com/mapbox/rasterio) - Rasterio employs GDAL under the hood for file I/O and raster formatting.
	- [GeoPandas] (https://github.com/geopandas/geopandas) - 整合了pandas,shapely,fiona,descartes,pyproj和rtrees可以直接用于数据处理
	- [Rasterstats] (https://github.com/perrygeo/python-rasterstats/) - Python module for summarizing geospatial raster datasets based on vector geometries.
	- [PySAL] (http://pysal.readthedocs.io/en/latest/) - For all your spatial econometrics needs.
	- [PyShp] (https://code.google.com/archive/p/pyshp/) - For reading and writing shapefiles.
	- [PyProj] (https://github.com/jswhit/pyproj) - For conversions between projections.
	- [Folium] (https://github.com/python-visualization/folium) - Python Data. Leaflet.js Maps.

- [Kartograph](http://kartograph.org/) is a simple and lightweight framework for building interactive map applications without Google Maps or any other mapping service. It was created with the needs of designers and data journalists in mind. Kartograph is two libraries. 
	- [Kartograph.py](https://github.com/kartograph/kartograph.py) - A powerful Python library for generating beautiful, Illustrator-friendly SVG maps.
	- [Kartograph.js](https://github.com/kartograph/kartograph.js) - A JavaScript library for creating interactive maps based on Kartograph.py SVG maps.


## 桌面GIS软件
- [QGIS](http://qgis.org/en/site/) - A cross-platform free and open-source desktop GIS software
- [GRASS GIS](https://grass.osgeo.org/) - Used for geospatial data management and analysis, as a founding member of OSGEO
- [uDig](http://udig.refractions.net/) - An open source desktop application framework built with Eclipse
- [gvSIG](http://www.gvsig.com/en) - A powerful, user-friendly, interoperable geomatics professionals
- [Whitebox GAT](http://www.uoguelph.ca/~hydrogeo/Whitebox/) - Software package for geospatial analysis and data visualization


## Geographic Data Mining
- [Weka] (http://www.cs.waikato.ac.nz/ml/weka/) - Weka is a collection of machine learning algorithms for data mining tasks written in Java.
- [GeoDMA] (https://sourceforge.net/projects/geodma/) - GeoDMA is a plugin for TerraView software, used for geographical data mining.


## OpenStreetMap	
- [openstreetmap官网](https://github.com/openstreetmap/openstreetmap-website) - Mirror of the Rails application powering [OSM](http://www.openstreetmap.org) . geodata提供了一个[osm-website镜像](https://github.com/geo-data/openstreetmap-website-docker). 

- OpenStreetMap Editors
	- [IDeditor](https://github.com/openstreetmap/iD) - The easy-to-use OpenStreetMap editor in JavaScript.
	- [JOSM](http://josm.openstreetmap.de/) - JOSM is an extensible editor for ​OpenStreetMap (OSM), [Git links](https://github.com/openstreetmap/josm) with a lot of [plugins](https://github.com/openstreetmap/josm-plugins). 
	- [ArcGIS Editor for OSM](http://esriosmeditor.codeplex.com/) is a toolset for GIS users to access and contribute to OpenStreetMap through their Desktop or Server environment. [Git links](https://github.com/Esri/arcgis-osm-editor). 

- OpenStreetMap Data
	-[osm planet](planet.openstreetmap.org) - 原始数据下载
	-[openstreetmapdata](http://openstreetmapdata.com/) - The OpenStreetMap project has collected an amazing amount of geodata and made it available to the world for free. But the raw OpenStreetMap data is hard to use. On this web site you'll find some of that OpenStreetMap data, but it has been pre-processed and formatted for easier use.
	- [Geofabrik](http://www.geofabrik.de/) - 可以下载[分大洲的数据](http://download.geofabrik.de/) 

- OpenStreetMap Data Tools
	- [Osmosis](https://github.com/openstreetmap/osmosis) - Osmosis is a command line Java application for processing OSM data. 
	- [OSMembrane](https://github.com/openstreetmap/OSMembrane) - OSMembrane is a GUI front-end for “Osmosis” used by the OpenStreetMap project.
	- [Osmium](osmcode.org) - Osmium is a highly flexible and performant C++ library for working with OpenStreetMap data. Built on top of this library are a command line tool, a Node.JS module and a Python module. This suite of software can be used for many tasks, from keeping history planets current, to creating statistics, to converting OSM data in many different GIS formats. 开发语言：c++ 支持node，支持python. [Osmium Library](http://osmcode.org/libosmium/) - A fast and flexible C++ library for working with OpenStreetMap data. [PyOsmium](http://osmcode.org/pyosmium/) - Python bindings to Osmium Library
	- [Imposm](http://imposm.org/) - 将OSM数据导入到PostgreSQL/PostGIS databases. 
	- [Imposm 2](https://github.com/omniscale/imposm) reads XML and PBF files and can import the data into PostgreSQL/PostGIS databases.Imposm 2 is the current stable version of Imposm. It is mature, flexible and many cases faster then osm2pgsql.
	- [imposm.parser](https://github.com/omniscale/imposm-parser) - OpenStreetMap XML/PBF parser for Python. 支持多CPU和多核
	- [Imposm 3](https://github.com/omniscale/imposm3) reads PBF files and imports the data into PostgreSQL/PostGIS. It can also update the DB from diff files. It is designed to create databases that are optimized for rendering (i.e. generating tiles or for WMS services). Imposm 3 is written in Go and it is a complete rewrite of the previous Python implementation.	
	- [HOOTENANNY](https://github.com/ngageoint/hootenanny) - high-performance conflation software. Hootenanny is an open source conflation tool developed to facilitate automated and semi-automated conflation of critical Foundation GEOINT features in the topographic domain, namely roads (polylines), buildings (polygons), and points-of-interest (POI’s) (points). Conflation occurs at the dataset level, where the user’s workflow determines the best reference dataset and source content, geometry and attributes, to transfer to the output map. Hootenanny internal processing leverages the key value pair structure of OpenStreetMap (OSM) for improved utility and applicability to broader user groups, e.g. normalized attributes can be used to aid in feature matching and OSM’s free tagging system allows the map to include an unlimited number of attributes describing each feature.
	- [Hootenanny UI ](https://github.com/ngageoint/hootenanny-ui) - Hootenanny UI is a submodule of the Hootennany vector conflation project. It provides the web interface for translation, conflation, editing, and export of vector datasets. Hoot UI is built on [iD](https://github.com/openstreetmap/iD) - friendly JavaScript editor for OpenStreetMap
	- [OSM-Analytics Tool](http://osm-analytics.org/) lets you analyse interactively how specific OpenStreetMap features are mapped in a specific region. [OSM-Analytics git link](https://github.com/hotosm/osm-analytics) and [backend server](https://github.com/hotosm/osm-analytics-cruncher). 
	- [Geofabrik Map Compare Tools](http://tools.geofabrik.de/mc/) - OpenStreetMap与google map比较side by side
	- [Geofabrik Map debug tools](http://tools.geofabrik.de/map/) - A full-screen slippy map with several different map views, a tile grid for debugging, and links to many other maps.
	- [Geofabrik OSM Inspector tools](http://tools.geofabrik.de/osmi/) - This tool offers different views on the OpenStreetMap data. It can be used to get a better idea how the data in the database looks like and it can point out omissions or errors. The OSM Inspector has already become an invaluable tool for many in fixing relations, addressing, geometry or strange tagging errors. Its feature set grows with the project's demands - if something is hot in OSM, it will be on the Inspector.
	- [Geofabrik OSM Tile Calculator](http://tools.geofabrik.de/calc/) - This tool can calculate the estimated size of tiles in an area, allows to obtain bounding boxes from a specific area or calculate print margins.

- OpenStreetMap Tile Server	
	- [osm-tiles-docker](https://github.com/geo-data/openstreetmap-tiles-docker) - OpenStreetMap Tile Server Container

## 空间数据处理引擎
### 空间数据ETL
- [GeoKettle ETL](http://www.geokettle.org/) - [GeoKettle](http://www.spatialytics.org/projects/geokettle/) is a powerful, metadata-driven spatial ETL (Extract, Transform and Load) tool dedicated to the integration of different data sources for building and updating geospatial databases, data warehouses and services. GeoKettle enables the Extraction of data from data sources, the Transformation of data in order to correct errors, make some data cleansing, change the data structure, make them compliant to defined standards, and the Loading of transformed data into a target DataBase Management System (DBMS) in OLTP or OLAP/SOLAP mode, GIS file or Geospatial Web Service.
- [Koop](https://github.com/koopjs/koop) - An Open Geospatial ETL Engine - Node.js, Leave geospatial data where it lives and transform it into GeoJSON, CSV, KML, a Shapefile, or a Feature Service dynamically.


### 新型空间数据
- [点云PDAL](http://www.pdal.io/) - [Point Data Abstraction Library](https://github.com/pdal/pdal) is a C++ BSD library for translating and manipulating point cloud data.
- [PCL](https://github.com/pointcloudlibrary/pcl) - The Point Cloud Library (PCL) is a C++-based standalone, large scale, open project for 2D/3D image and point cloud processing.
- [Entwine](https://entwine.io/#/data/chambbj/FortAncient) - Entwine is a data organization library for massive point clouds, designed to conquer datasets of hundreds of billions of points as well as desktop-scale point clouds. Entwine can index anything that is [PDAL](http://pdal.io/)-readable, and can read/write to a variety of sources like S3 or Dropbox. 

- [Voxel Globe Docker](https://github.com/ngageoint/voxel-globe) - Calibrates aerial camera models and constructs 3D models from video sequences as well applications for 3D models such as change detection. 



## docker镜像(Library/Service/Tools)
### docker tools
- [clusterhq/flocker](https://github.com/ClusterHQ/flocker) -  Container data volume manager for your Dockerized application 
- [shipyard](https://github.com/shipyard/shipyard) - Composable Docker Management
### docker images
- [docker-mapnik](https://github.com/jawg/docker-mapnik3) - Latest Mapnik3 docker container build, Mapnik from 3.0.0 ->3.0.10, download the image [here](https://hub.docker.com/r/mapsquare/mapnik3/). 
- [docker-mapnik-python-debian](https://github.com/kherrala/docker-mapnik-python) - mapnik(v3.0.5) docker image with [python bindings](https://github.com/mapnik/python-mapnik/), debian based.
- [mapnik-docker-centos](https://github.com/garrettrayj/mapnik-docker) - Docker image for Mapnik 3.0.10 Based on CentOS 7. 
- [mapnik-docker-python-ubuntu](https://github.com/hixi/docker-mapnik) - Mapnik(v3.0.9) Docker image with Python bindings included based on ubuntu:14.04. see feature/0.1 branch. 
- [docker-mapnik-vector-tile](https://github.com/InstaGIS/docker-mapnik-vector-tile) - Docker image for [mapnik-vector-tile](https://github.com/mapbox/mapnik-vector-tile), it is Mapnik implemention of Mapbox Vector Tile specification, download the image [here](https://hub.docker.com/r/instagis/mapnik-vector-tile/) .
- [docker-Tippecanoe](https://github.com/topopotamus/docker-tippecanoe) - Tippecanoe [Dockerfile](https://registry.hub.docker.com/u/apburnes/tippecanoe/) for vector tile processing. 
- [GeographicaGS/Docker-GDAL2](https://github.com/GeographicaGS/Docker-GDAL2/) - A Dockerfile compiling the latest GDAL github checkout with a broad range of drivers
- [GRASS Docker Images](https://github.com/geo-data/grass-docker) - Ubuntu derived image containing GRASS GIS software.
- [PostGIS docker images](https://github.com/appropriate/docker-postgis) - Docker image for PostGIS, see [here](https://registry.hub.docker.com/u/mdillon/postgis/) for Postgres 9(9.1-9.5) with PostGIS 2.2. 

- [docker-geoserver](https://github.com/kartoza/docker-geoserver) - docker container that runs [Geoserver](http://geoserver.org/).  
- [docker-geoserver/geofence](https://github.com/Terranex/docker-geoserver-geofence) 

- [docker-qgis-server](https://github.com/kartoza/docker-qgis-server) - A dockerfile that contains a running QGIS server, pull the latest trusted build from [docker hub](https://registry.hub.docker.com/u/kartoza/docker-qgis-server/) . [another docker-qgis-server](https://github.com/pvalsecc/docker-qgis-server). 
- [ubuntugis-docker](https://github.com/javimarlop/ubuntugis-docker) - VM using Docker for Geospatial Analysis, download the image [here](https://registry.hub.docker.com/u/javimarlop/ubuntugis-docker/) .

- [turf-cli-docker](https://github.com/topopotamus/turf-cli-docker) - Dockerized TurfJS CLI


## docker镜像(Solutions)

- [docker-cartodb](https://github.com/sverhoeven/docker-cartodb/) - fully working Dockerized CartoDB, download the image [here](https://hub.docker.com/r/sverhoeven/cartodb/) .
- [vagrant-cartodb](https://github.com/azavea/vagrant-cartodb) - Ansible role to build a multi-machine vagrant setup for CartoDB 
- [docker-mapnik-tilestache](https://github.com/srounet/docker-mapnik) - Mapnik + Tilestache UTFGrid ready for Docker, mapnik 3.0.9 and TileStache
- [docker-openMAINT](https://github.com/rsilva4/docker-openmaint) - docker image for openMAINT. It is a fully functional openMAINT docker image with docker-compose for integrating with Postgres, BIMServer and GeoServer. [openMAINT](http://www.openmaint.org/en) is an open source solution for the Property & Facility Management; an application for the management of buildings, installations, movable assets and related maintaining activities. [BIMServer](http://bimserver.org/) (i.e. Building Information Model Server, Git repo [here](https://github.com/opensourceBIM/BIMserver) ) enables you to centralize and manage the information of a construction (or other building related) project. 
- [docker-geoserver-gdal](https://github.com/DenisCarriere/Geoserver-Docker) - GeoServer Docker with GDAL (ECW JP2k & MrSID) with Nginx



## 其他微服务docker镜像
- [Piazza - 20+微服务](http://pz-swagger.venicegeo.io/) - Enabling Government Teams to Share and Access Data in the Cloud in 2016
	- [pizza documentation](https://github.com/venicegeo/venice) - Piazza documentation in both HTML and PDF
	- [Piazza Devops](https://github.com/venicegeo/pz-docs) 
- qgis, postgres/postGIS, geoserver, mapserver, geogig, tileserver-mapnik, osm2vectortiles, mapsherpa, mapcache, geoblacklight, orfeo, imagemagick, gdal, pdal, saga, grass, opticks, cartodb, nominatim, osmtools, orsm, osmosis, osm2pgsql, r-spatial, neo4j-spatial, ckan-spatial, ubuntugis-docker, geotriples, elasticsearch, mongodb, couchdb, mapnik, sahana, geonode, geosuite, landsat-base, cesium terrain server, geonetwork, shapely, fiona, landsat, geomesa, opendronemap, geodocker-cluster


# 几个生态系统
## 1. Mapbox GL ecosystem 
## 2. 3D
## 3. OSM



