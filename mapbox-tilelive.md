# Mapbox tilelive.js
The [Tilelive.js](https://github.com/mapbox/tilelive) is a module to help interactions between tilelive source modules. A tilelive source is an interface implemented by node modules that deal with reading and writing map tiles.
Tilelive 是一个生态系统.
## Mapbox官方实现的模块

- [node-mbtiles](https://github.com/mapbox/node-mbtiles) [mbtiles](http://mbtiles.org/) renderer and storage backend for tilelive
- [node-tilejson](https://github.com/mapbox/node-tilejson) A javascript implementation of [tilejson spec](https://github.com/mapbox/tilejson-spec)
- [tilelive-mapnik](https://github.com/mapbox/tilelive-mapnik) Mapnik Renderer backend for [tilelive.js](http://github.com/mapbox/tilelive.js) that uses [node-mapnik](http://github.com/mapnik/node-mapnik) to render tiles and grids from a Mapnik XML file.
- [tilelive-vector](https://github.com/mapbox/tilelive-vector) Implements the tilelive API for rendering mapnik vector tiles to raster images.
- [tilelive-bridge](https://github.com/mapbox/tilelive-bridge) Implements the tilelive API for generating mapnik vector tiles from traditional mapnik datasources.

## Tessera server by mojodna from [Stamen](http://stamen.com/) and tilelive modules
[tessera](https://github.com/mojodna/tessera) is a [tilelive](https://github.com/mapbox/tilelive.js)-based tile
server. Using the power of the tilelive ecosystem, it is capable of serving and
rendering tiles from many sources.
Tessera support many [tilelive-modules](https://github.com/mojodna/tilelive-modules) as following
### Tile datasouce modules
- [tilelive-file](https://github.com/mapbox/tilelive-file) Reads/writes tiles and grids from/to the filesystem.
- [mbtiles](https://github.com/mapbox/node-mbtiles) [mbtiles](http://mbtiles.org/) renderer and storage backend for tilelive
- [tilelive-archive](https://github.com/mojodna/tilelive-archive) Streaming reads from (compressed) tile tar archives
- [tilelive-mapbox](https://github.com/mojodna/tilelive-mapbox) A [tilelive](https://github.com/mapbox/tilelive.js) source for mapbox:// URIs
- [tilelive-fieldpapers](https://github.com/fieldpapers/tilelive-fieldpapers) A [tilelive](https://github.com/mapbox/tilelive.js) source for [Field
Papers](http://fieldpapers.org/) atlases and snapshots.
- [tilelive-http](https://github.com/mojodna/tilelive-http) an HTTP source for [tilelive](https://github.com/mapbox/tilelive).
- [tilelive-tms](https://github.com/oscarfonts/tilelive-tms) Reads tiles from a TMS service.
- [tilelive-arcgis](https://github.com/FuZhenn/tilelive-arcgis) A tilelive.js adapter for reading from tile storage cache of ArcGIS, support file and [Compact Bundle](https://server.arcgis.com/zh-cn/server/latest/publish-services/windows/inside-the-compact-cache-storage-format.htm)
- [tilelive-null](https://github.com/mojodna/tilelive-null) A noop sink for tilelive.
- [tilelive-streaming](https://github.com/mojodna/tilelive-streaming) A tilelive wrapper that transparently adds streaming functionality to providers.
- [tilelive-raster](https://github.com/mojodna/tilelive-raster) a tilelive source for simple rasters, both local and remote.
- [tilelive-rasterpbf](https://github.com/mojodna/tilelive-rasterpbf) a tilelive source for outputting PBF-encoded rasters from PostGIS.
- [tilelive-decorator](https://github.com/mapbox/tilelive-decorator) Load vector tiles from a tilelive source and decorate them with properties from redis. So if you use tilelive-s3 it can load tiles from s3, and add properties to features from redis.
- [tilelive-s3](https://github.com/mapbox/tilelive-s3) Extends node-tilejson for using S3 as a tilejson backend.
- [tilelive-csv](https://github.com/mojodna/tilelive-csv) PBF → CSV with [tilelive](https://github.com/mapbox/tilelive)
- [tilelive-csvin](https://github.com/mojodna/tilelive-csvin) A [tilelive](https://github.com/mapbox/tilelive) provider for CSV inputs that supports streaming reads.
- [tilelive-cartodb](https://github.com/mojodna/tilelive-cartodb) A - [tilelive](https://github.com/mapbox/tilelive) source for [CartoDB](http://cartodb.com/)
- [cdbtiles](https://github.com/vsivsi/cdbtiles) cdbtiles is a [tilelive](https://github.com/mapbox/tilelive) backend (source/sink) plug-in for [CouchDB](https://couchdb.apache.org/).
- [mongotiles](https://github.com/vsivsi/mongotiles) mongotiles is a [tilelive](https://github.com/mapbox/tilelive) backend plug-in for [MongoDB GridFS](http://docs.mongodb.org/manual/core/gridfs/)

### Tile caching modules
- [tilelive-cache](https://github.com/mojodna/tilelive-cache) A caching wrapper for tilelive.js
- [tilelive-multicache](https://github.com/mapbox/tilelive-multicache) Module for adding a caching layer in front a tilelive source. It wraps a tilelive backend providing a new source constructor with cached superpowers!
- [tilelive-redis](https://github.com/mapbox/tilelive-redis) Module for adding a redis-based caching layer in front a node-tilejson tilelive source.
- [tilelive-memcached](https://github.com/mapbox/tilelive-memcached) node-tilejson wrapping source for tilelive.

### Tile render modules
- [tilelive-mapnik](https://github.com/mapbox/tilelive-mapnik) Mapnik Renderer backend for [tilelive.js](http://github.com/mapbox/tilelive.js) that uses [node-mapnik](http://github.com/mapnik/node-mapnik) to render tiles and grids from a Mapnik XML file.
- [tilelive-carto](https://github.com/mojodna/tilelive-carto) A [CartoCSS](https://github.com/mapbox/carto) style(*.mml) source for [tilelive](https://github.com/mapbox/tilelive)
- [tilelive-tmsource](https://github.com/mojodna/tilelive-tmsource) a [tilelive](https://github.com/mapbox/tilelive.js) provider for
[tm2](https://github.com/mapbox/tm2) sources
- [tilelive-tmstyle](https://github.com/mojodna/tilelive-tmstyle) a TileMill style source for tilelive
- [tilelive-utfgrid](https://github.com/mojodna/tilelive-utfgrid) A [tilelive](https://github.com/mapbox/tilelive.js) provider that allows [UTFGrid](https://github.com/mapbox/utfgrid-spec)-generating sources (i.e. those with a `getGrid()` method) to be treated as though they generate data
tiles rather than treating grid output as "special".
- [tilelive-vector](https://github.com/mapbox/tilelive-vector) Implements the tilelive API for rendering mapnik vector tiles to raster images.
- [node-tilejson](https://github.com/mapbox/node-tilejson) A javascript implementation of [tilejson spec](https://github.com/mapbox/tilejson-spec)
- [tilelive-xray](https://github.com/mojodna/tilelive-xray) A [tilelive](https://github.com/mapbox/tilelive.js) provider that uses
[tilelive-vector](https://github.com/mapbox/tilelive-vector)'s xray
functionality to generate visual data tile representations.
- [tilelive-cardboard](https://github.com/mapbox/tilelive-cardboard) Implements the [tilelive API](https://github.com/mapbox/tilelive.js/blob/d7703bbf3a4f7084a4b225bc85c87ecab185ccb9/API.md) for creating mapnik vector tiles from a [cardboard](https://github.com/mapbox/cardboard) datasource. Cardboard is a JavaScript library for managing the storage of GeoJSON features on an AWS backend. It relies on DynamoDB for indexing and small-feature storage, and S3 for large-feature storage.
- [tilelive-omnivore](https://github.com/mapbox/tilelive-omnivore) Implements the tilelive api for a variety of raw data sources like 'csv', 'geojson', 'gpx', 'kml', 'shp', 'tif'
- [tilelive-solid](https://github.com/mojodna/tilelive-solid) A tilelive provider that generates solid colored tiles.Usage: tilelive.load("solid:#fff", ...);
- [tilelive-fractal](https://github.com/kamicut/tilelive-fractal) A tilelive provider that generates fractals. Inspired by [tilelive-solid](https://github.com/mojodna/tilelive-solid)
- [tilelive-overlay](https://github.com/mapbox/tilelive-overlay) add GeoJSON features with simplestyle styles in a tilelive pipeline.

### Tile processing modules
- [tilelive-blend](https://github.com/mojodna/tilelive-blend) A [tilelive](https://github.com/mapbox/tilelive) provider that blends.
- [tilelive-bridge](https://github.com/mapbox/tilelive-bridge) Implements the [tilelive](https://github.com/mapbox/tilelive) API for generating mapnik vector tiles from traditional mapnik datasources.
- [tilelive-merge](https://github.com/mojodna/tilelive-merge) A tilelive source that merges sources.
Overzooming (using part of a lower-zoom tile), masking (falling back to lower-zoom tiles when they're intentionally missing, as in the middle of the ocean), and image layers are all supported and the most conservative upstream values for Last-Modified and Cache-Control are used.
- [tilelive-hybrid](https://github.com/steve9164/tilelive-hybrid) Implements the tilelive API for serving tiles from multiple tilelive sources depending on the requested zoom level. Ideal for vector tile sources where some zoom levels use pre-generated tiles and other zoom levels generate tiles from a mapnik data source
- [tilelive-download](https://github.com/npeihl/tilelive-download-example) An example showing how we can use tilelive to copy from a TileJSON source to an MBTiles database
- [kkaefer/tilelive-oscim](https://github.com/kkaefer/tilelive-oscim) Producing vector tiles compatible with [OpenScienceMap](http://www.opensciencemap.org/)
- [hannesj/tilelive-geojson](https://github.com/hannesj/tilelive-geojson) Tilelive source producing protobuf-encoded vector tiles from GeoJSON data
- [tilelive-vector-composite](https://github.com/tnightingale/tilelive-vector-composite) Tilelive.js module for compositing Mapbox Vector Tiles from any tilelive source.

<img width="1260" alt="localhost_8080__6_16_699_2_988" src="https://cloud.githubusercontent.com/assets/719357/13823125/b291f79a-eb7e-11e5-8718-158507169f7b.png">

## csWeb-tile npm package
[csWeb-tile](https://github.com/TNOCS/csWeb-tile) to offer a simple npm package for serving tile sources. You can run it standalone, as part of the [csWeb(short for common sense Web) server](https://github.com/TNOCS/csWeb), or any other express-based server for that matter. Currently, the following tilelive protocols are supported:
* mbtiles (with raster data). Default location: ```tilesources\mbtiles```.
* mbtiles (with vector tiles). Default location: `tilesources\tm2` (see world.tm2 example)
* tmstyle (or .tm2) projects, i.e. [Mapbox Studio Classic](https://www.mapbox.com/mapbox-studio-classic/#win64) tilemill 2 projects. You can create them using the free Mapbox Studio Classic tool. Default location ```tilesources\tm2```. Currently only tested with geojson source layers. For tmstyle projects, we can also serve UtfGrid files - in that case, you need to edit the project.yml file manually to add the interactivity layer, as explained in [UtfGrid](https://www.mapbox.com/help/style-quickstart/#utfgrid), [How interactivity works](https://www.mapbox.com/blog/how-interactivity-works-utfgrid/) and [here](http://www.macwright.org/2011/08/10/fast-hacky-queries-with-utfgrid.html).
* Mapnik XML projects, e.g. you can create your own map using [TileMill](https://www.mapbox.com/tilemill/), and export it as a Mapnik project. Default location: ```tilelive\mapnik```.   
NOTE: Tests are performed using node 5 and npm 3 on Windows: in principle, everything should also work on Mac and Linux

## TileStream
[cutting-room-floor/tilestream](https://github.com/cutting-room-floor/tilestream) A high-performance map tile server powered by MBTiles files
Features
- MBTiles-based tile server
- Minimal gallery view and map viewer for tiles
- Support for MBTiles interaction using Mapbox.js


