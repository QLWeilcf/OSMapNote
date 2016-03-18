# Intro on CartoDB Repository@Git
Location Intelligence & Data Visualization tool

## CartoDB-Editor
	https://github.com/CartoDB/cartodb

### CartoDB.js
https://github.com/CartoDB/cartodb.js
CartoDB javascript library allows to embed visualizations created with CartoDB in your map or website in a simple way.

### Windshaft 云上的空间数据库
https://github.com/CartoDB/Windshaft
Windshaft is a library used by cartodb.com, an Open Source Geospatial Database on the Cloud.
Windshaft map tiler - A Node.js map tile library for PostGIS and torque.js, with CartoCSS styling.
    Can render arbitrary SQL queries
    Generates image and UTFGrid interactivity tiles
    Accepts, stores, serves, and applies map styles written in CartoCSS
    Supports re-projections

#### Windshaft-cartodb
https://github.com/CartoDB/Windshaft-cartodb
This is the CartoDB Maps API tiler. It extends Windshaft with some extra functionality and custom filters for authentication.
    reads dbname from subdomain and cartodb redis for pretty tile urls
    configures windshaft to publish cartodb_id as the interactivity layer
    gets the default geometry type from the cartodb redis store
    allows tiles to be styled individually
    provides a link to varnish high speed cache
    provides a template maps API
#### Docker for Windshaft
https://github.com/TerraSeer/docker-windshaft
https://github.com/azavea/docker-windshaft

#### windshaft used
* Natural History Museum
https://github.com/NaturalHistoryMuseum/nhm-windshaft-utils
https://github.com/NaturalHistoryMuseum/nhm-windshaft-chef 安装指南
https://github.com/NaturalHistoryMuseum/nhm-windshaft-app 瓦片服务
https://github.com/NaturalHistoryMuseum/ckanext-map Map visualisation for NHM CKAN
https://github.com/NaturalHistoryMuseum/ckanext-dataspatial Ckan Datastore Spatial extension
https://github.com/NaturalHistoryMuseum/inselect 博物馆样本图片半自动分割标引
*iNaturalist博物学家社交网络
https://github.com/inaturalist/Windshaft-inaturalist
Wrapper around Windshaft to provide a map tiler for iNaturalist.
https://github.com/inaturalist/elasticmaps
Map tileserver based on node-mapnik and elasticsearch


### CartoDB basemaps
https://github.com/CartoDB/CartoDB-basemaps
This is the source code and styles for the CartoDB Basemaps, designed by Stamen.
The code and styles here are intended for serving the basemaps on your own local CartoDB instance.



### CartoDB SQL API
https://github.com/CartoDB/CartoDB-SQL-API
Provides a node.js based API for running SQL queries against CartoDB.
    Users are authenticated over OAuth or via an API KEY.
    Authenticated requests to this API should always be made over SSL.
CartoDB’s SQL API allows you to interact with your tables and data inside CartoDB as if you were running SQL statements against a normal database. You can use the SQL API to insert, update or delete data (i.e., insert a new column with a latitude and longitude data) or to select data from public tables in order to use it on your website or application (i.e., display the 10 closest records to a particular location).

###	CartoDB/cartodb-postgresql
https://github.com/CartoDB/cartodb-postgresql
PostgreSQL extension for CartoDB
It is a module to load into each CartoDB user database to perform cartodb-specific security and functionality checks.
Dependencies
    PostgreSQL 9.3+ (with plpythonu extension and xml support)
    PostGIS extension http://postgis.net/
		PostgreSQL 9.3+ Schema Triggers extension https://github.com/CartoDB/pg_schema_triggers
		plpythonu ?

### deep-insights 仪表盘应用？
https://github.com/CartoDB/deep-insights.js
参考blog


###	CartoDB/dataservices-api
https://github.com/CartoDB/dataservices-api
The CartoDB Geocoder SQL API (server and client FTM)


https://github.com/CartoDB/pgbouncer
PgBouncer
Lightweight connection pooler for PostgreSQL.
Homepage
    https://pgbouncer.github.io

### bigmetadata 用途？
https://github.com/CartoDB/bigmetadata
Bigmetadata comprises four parts: 支持docker
ETL | Observatory | Metadata | Catalog


## Torque

### Torque-Temporal mapping for CartoDB
https://github.com/CartoDB/torque
Render big, timeseries data in the client. Uses CartoDB to generate a datacube format. Torque have been used to visualize human movement, Twitter activity, biodiversity data, and many more large-scale datasets. 支持CartoDB及任何符合TileCube规范的服务。

### torque-TileCubes 地图瓦片立方体规范
https://github.com/CartoDB/torque-tiles
TileCubes is a specification for transferring temporal or categorical geospatial data. TileCubes have been used in a number of production projects since 2011.
TorqueTiles are JSON representations of multidimensional data with geospatial coordinates. TorqueTiles are broken into two document types, the Metadata and the Tiles. The Metadata document describes the shared information across the TileCube dataset. For each tile requested there is a Tile document returned that describes the data on that tile.

TorqueTiles are referenced on the Tile Map Service Specification and are currently restricted to global-mercator. Coordinates within a TileCube are measured in pixel offsets from the border and assume 256x256 pixel tiles.
Metadata

The TorqueMap Metadata document describes key tileset information, it includes:
    start: start time, in steps or unix timestamp
    end: end time, in steps or unix timestamp
    resolution: pixel resolution power of two (1/4, 1/2,... 2, 4, 16); the scale from 256x256 pixels
    data_steps: number of steps (integer)
    column_type: "integer" or "date", default "integer"
    minzoom: minimum zoom level, optional
    maxzoom: max zoom level, optional
    tiles: tile array for this set, required
    bounds: bounding box for tileset, optional


### CartoDB/torque-gen动态地图瓦片导出脚本
https://github.com/CartoDB/torque-gen
The torque.py script lets you export Torque tilecubes to static files for storage and use. This script can be useful for storage and backup of your Torque visualizations as well as using the Torque library offline or where the CartoDB backend isn't needed.

### torque.histogram
https://github.com/CartoDB/torque.histogram
widget to see a histogram of a torque map

### CartoQlik
CartoDB's Torque maps on Qlik
https://github.com/CartoDB/CartoDB-for-Qlik
CartoQlik allows you to use CartoDB's Torque map rendering library on Qlik Sense.
Features
    Static and animated maps, including heatmaps and category maps.
    Integrates with Qlik's data, and can also be used for data filtering.
    Easily change map layout, basemaps or animation parameters.
    Works nicely with even hundred thousand points.

### torque-reference
https://github.com/CartoDB/torque-reference
Torque-reference is a JSON specification of the CartoCSS vendor style options that Torque provides. Inspired by mapnik-reference, it is useful for building parsers, tests, compilers, and syntax highlighting/checking for languages.

## Library by CartoDB

### Leaflet.CanvasLayer
https://github.com/CartoDB/Leaflet.CanvasLayer
Leaflet.CanvasLayer is a full map canvas layer that allows you to render stuff on top of a map with HTML5 canvas element. Leaflet provides a tiled canvas layer which provides one canvas per tile to render.

### VECNIK - 客户端GeoJSON渲染试验库
https://github.com/CartoDB/VECNIK
Veknik is a JS library that render features from CartoDB using HTML5 on top of Modestmaps + Leaflet. It includes an implementation of the Carto language for dynamically styling features using its CSS language.
This is a prototype implementation to showcase the use of Carto for rendering maps on the client, not on the server. The library retrieves vector data from CartoDB using the SQL API on geojson format.

## CartoDB Labs
### labs-carbontool2
Revisit to the Carbon Calculator using updated libraries and styling guide
https://github.com/CartoDB/labs-carbontool2
demo: http://cartodb.github.io/labs-carbontool2/ 需要翻墙

### labs-cloudant
https://github.com/CartoDB/labs-cloudant
IBM cloudant的一款NoSQL数据库，一款专为云而构建的DBaaS平台，敏捷、高效。CartoDB/labs-cloudant是URL proxy for cloudant。


### CartoDB/labs-pepsicoca
Twitter real-time PoC
	https://github.com/CartoDB/labs-pepsicoca


## CartoDB Apps
### omnibus-cartodb 一个全栈平台和服务包项目
https://github.com/CartoDB/omnibus-cartodb
This omnibus project has both a full-stack platform-specific package named cartodb AND individual services packages.


### CartoDB splunk
cartodb + splunk
https://hurricanelabs.com/blog/splunk-cartodb/
https://github.com/CartoDB/cartodb-splunk
A Splunk app for map visualizations using CartoDB
A Splunk app for map visualizations using HERE maps https://github.com/pvanisacker/heremaps

https://github.com/CartoDB/pecan
CartoDB-Pecan
This library aims to help render better maps, based on statistics from a described table column.
