# CartoDB -Location Intelligence & Data Visualization tool

## [CartoDB-Editor](https://github.com/CartoDB/cartodb)

### [CartoDB.js](https://github.com/CartoDB/cartodb.js)
CartoDB javascript library allows to embed visualizations created with CartoDB in your map or website in a simple way.

### [Windshaft](https://github.com/CartoDB/Windshaft) 云上的空间数据库
Windshaft is a library used by cartodb.com, an Open Source Geospatial Database on the Cloud.
Windshaft map tiler - A Node.js map tile library for PostGIS and torque.js, with CartoCSS styling.
- Can render all data, or data restricted by SQL queries
- Generates image and UTFGrid interactivity tiles
- Accepts, stores, serves, and applies map styles written in CartoCSS
- Supports re-projections
- Serves Infowindow information
- Pluggable routing to provide customisable tile API URL endpoints
- Focus on handling concurrent requests
Windshaft is a simple, high speed and decoupled map tile server to generate maps from PostGIS.

#### [Windshaft-cartodb](https://github.com/CartoDB/Windshaft-cartodb) powers [CartoDB Map API](http://docs.cartodb.com/cartodb-platform/maps-api/quickstart/)
This is the CartoDB Maps API tiler. It extends Windshaft with some extra functionality and custom filters for authentication.
- reads dbname from subdomain and cartodb redis for pretty tile urls
- configures windshaft to publish cartodb_id as the interactivity layer
- gets the default geometry type from the cartodb redis store
- allows tiles to be styled individually
- provides a link to varnish high speed cache
- provides a template maps API

#### Docker for Windshaft
[docker-windshaft](https://github.com/TerraSeer/docker-windshaft) - A Docker image with Windshaft and its dependencies preinstalled.
[docker-windshaft2](https://github.com/azavea/docker-windshaft) - A Dockerfile based off of node:0.10-slim that installs CartoDB's Windshaft.

#### windshaft is used by
* Natural History Museum
https://github.com/NaturalHistoryMuseum/nhm-windshaft-utils
https://github.com/NaturalHistoryMuseum/nhm-windshaft-chef 安装指南
https://github.com/NaturalHistoryMuseum/nhm-windshaft-app 瓦片服务
https://github.com/NaturalHistoryMuseum/ckanext-map Map visualisation for NHM CKAN
https://github.com/NaturalHistoryMuseum/ckanext-dataspatial Ckan Datastore Spatial extension
https://github.com/NaturalHistoryMuseum/inselect 博物馆样本图片半自动分割标引
* iNaturalist博物学家社交网络
https://github.com/inaturalist/Windshaft-inaturalist
Wrapper around Windshaft to provide a map tiler for iNaturalist.
https://github.com/inaturalist/elasticmaps
Map tileserver based on node-mapnik and elasticsearch

### [CartoDB SQL API](https://github.com/CartoDB/CartoDB-SQL-API) powers CartoDB SQL API
Provides a node.js based API for running SQL queries against CartoDB.
- Users are authenticated over OAuth or via an API KEY.
- Authenticated requests to this API should always be made over SSL.
CartoDB’s SQL API allows you to interact with your tables and data inside CartoDB as if you were running SQL statements against a normal database. You can use the SQL API to insert, update or delete data (i.e., insert a new column with a latitude and longitude data) or to select data from public tables in order to use it on your website or application (i.e., display the 10 closest records to a particular location).

#### [CartoDB/cartodb-postgresql](https://github.com/CartoDB/cartodb-postgresql)
PostgreSQL extension for CartoDB
It is a module to load into each CartoDB user database to perform cartodb-specific security and functionality checks.

### [deep-insights](https://github.com/CartoDB/deep-insights.js)
[Deep Insights](https://cartodb.com/deep-insights) - CartoDB’s solution to make the invisible visible, and allow you to discover unseen correlations and patterns at an unprecedented scale.
CartoDB’s Deep Insights technology enables the visualization, exploration, dynamic filtering, and drill-down of data to unforeseen granular levels. Additionally, CartoDB’s Deep Insights is equipped with dashboards that come with a complete set of widgets that allow you to pan and zoom to different locations on your map, updating values for the area you are currently viewing, in real time!
To know more, please check the [The Mighty Location Intelligence Solution for Big Data Analysis and Actionable Decision Making: Deep Insights](http://blog.cartodb.com/deep-insights/).

### [bigmetadata](https://github.com/CartoDB/bigmetadata)
Bigmetadata comprises four parts: 支持docker
ETL | Observatory | Metadata | Catalog

## Torque
### [Torque](https://github.com/CartoDB/torque)-Temporal mapping for CartoDB
Render big, timeseries data in the client. Uses CartoDB to generate a datacube format. Torque have been used to visualize human movement, Twitter activity, biodiversity data, and many more large-scale datasets. 支持CartoDB及任何符合TileCube规范的服务。

### [torque-TileCubes](https://github.com/CartoDB/torque-tiles) 地图瓦片立方体规范
TileCubes is a specification for transferring temporal or categorical geospatial data. TileCubes have been used in a number of production projects since 2011.
TorqueTiles are JSON representations of multidimensional data with geospatial coordinates. TorqueTiles are broken into two document types, the Metadata and the Tiles. The Metadata document describes the shared information across the TileCube dataset. For each tile requested there is a Tile document returned that describes the data on that tile.
TorqueTiles are referenced on the Tile Map Service Specification and are currently restricted to global-mercator. Coordinates within a TileCube are measured in pixel offsets from the border and assume 256x256 pixel tiles.
Metadata
The TorqueMap Metadata document describes key tileset information, it includes:
- start: start time, in steps or unix timestamp
- end: end time, in steps or unix timestamp
- resolution: pixel resolution power of two (1/4, 1/2,... 2, 4, 16); the scale from 256x256 pixels
- data_steps: number of steps (integer)
- column_type: "integer" or "date", default "integer"
- minzoom: minimum zoom level, optional
- maxzoom: max zoom level, optional
- tiles: tile array for this set, required
- bounds: bounding box for tileset, optional


### [CartoDB/torque-gen](https://github.com/CartoDB/torque-gen)动态地图瓦片导出脚本
The torque.py script lets you export Torque tilecubes to static files for storage and use. This script can be useful for storage and backup of your Torque visualizations as well as using the Torque library offline or where the CartoDB backend isn't needed.

### [torque.histogram](https://github.com/CartoDB/torque.histogram)
widget to see a histogram of a torque map

### [CartoQlik](https://github.com/CartoDB/CartoDB-for-Qlik)
CartoDB's Torque maps on Qlik
CartoQlik allows you to use CartoDB's Torque map rendering library on Qlik Sense.
Features
- Static and animated maps, including heatmaps and category maps.
- Integrates with Qlik's data, and can also be used for data filtering.
- Easily change map layout, basemaps or animation parameters.
- Works nicely with even hundred thousand points.

### [torque-reference](https://github.com/CartoDB/torque-reference)
Torque-reference is a JSON specification of the CartoCSS vendor style options that Torque provides. Inspired by mapnik-reference, it is useful for building parsers, tests, compilers, and syntax highlighting/checking for languages.

## base maps by CartoDB
### [CartoDB basemaps](https://github.com/CartoDB/CartoDB-basemaps)
This is the source code and styles for the CartoDB Basemaps, designed by Stamen.
The code and styles here are intended for serving the basemaps on your own local CartoDB instance.
see [talks](http://zen.itram.es/talks/basemaps/#/)

## Library by CartoDB

### [Leaflet.CanvasLayer](https://github.com/CartoDB/Leaflet.CanvasLayer)
Leaflet.CanvasLayer is a full map canvas layer that allows you to render stuff on top of a map with HTML5 canvas element. Leaflet provides a tiled canvas layer which provides one canvas per tile to render.

### [VECNIK](https://github.com/CartoDB/VECNIK) - 客户端GeoJSON渲染试验库
Veknik is a JS library that render features from CartoDB using HTML5 on top of Modestmaps + Leaflet. It includes an implementation of the Carto language for dynamically styling features using its CSS language.
This is a prototype implementation to showcase the use of Carto for rendering maps on the client, not on the server. The library retrieves vector data from CartoDB using the SQL API on geojson format.

## CartoDB Labs
### [labs-carbontool2](https://github.com/CartoDB/labs-carbontool2)
Revisit to the Carbon Calculator using updated libraries and styling guide
demo: http://cartodb.github.io/labs-carbontool2/ 需要翻墙

### [labs-cloudant](https://github.com/CartoDB/labs-cloudant)
IBM cloudant的一款NoSQL数据库，一款专为云而构建的DBaaS平台，敏捷、高效。CartoDB/labs-cloudant是URL proxy for cloudant。

### [CartoDB/labs-pepsicoca](https://github.com/CartoDB/labs-pepsicoca)
Twitter real-time PoC

## CartoDB Apps
### [omnibus-cartodb](https://github.com/CartoDB/omnibus-cartodb) 一个全栈平台和服务包项目
This omnibus project has both a full-stack platform-specific package named cartodb AND individual services packages.

### [CartoDB splunk](https://github.com/CartoDB/cartodb-splunk)
[A Splunk app for map visualizations using CartoDB](https://hurricanelabs.com/blog/splunk-cartodb/)
A Splunk app for map visualizations using HERE maps https://github.com/pvanisacker/heremaps

[CartoDB-Pecan](https://github.com/CartoDB/pecan)
This library aims to help render better maps, based on statistics from a described table column.

[CartoDB Generator for Yeoman](https://github.com/nerik/generator-cartodb)
a yeoman generator that will quickly set up the perfect dev environment to make maps and visualizations with CartoDB APIs and client-side library.
