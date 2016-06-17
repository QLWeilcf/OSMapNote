# awesome-vector-tiles [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

This document is forked from [awesome-vector-tiles](https://github.com/mapbox/awesome-vector-tiles).

The [Mapbox Vector Tile spec](https://www.mapbox.com/developers/vector-tiles/) is an efficient encoding for map
data into vector tiles that can be rendered dynamically.

## Parsers & Generators

- [OGR Vector Tile Driver](https://github.com/Universefei/ogr_vector_tile_driver) - OGR Vector Tile Driver
- [vector-tile-js](https://github.com/mapbox/vector-tile-js) - Parses vector tiles with JavaScript.
- [mapnik-vector-tile](https://github.com/mapbox/mapnik-vector-tile) - C++ vector tile read/write implementation on top of Mapnik.
- [vector-tile-py](https://github.com/mapbox/vector-tile-py) - Python vector tile decoder implementation
- [node-mapnik](https://github.com/mapnik/node-mapnik) - Node.js API for vector tiles which depends on `mapnik-vector-tile`
- [mapbox-vector-tile-cs](https://github.com/bertt/mapbox-vector-tile-cs) - Parses vector tiles with C#.
- [tilelive-bridge](https://github.com/mapbox/tilelive-bridge) - Implements [Tilelive API](https://github.com/mapbox/tilelive.js/blob/master/API.md) for creating vector tiles from traditional Mapnik datasources in Node.js.
- [tilelive-vector](https://github.com/mapbox/tilelive-vector) - Implements [Tilelive API](https://github.com/mapbox/tilelive.js/blob/master/API.md) for reading vector tiles and rendering to image tiles in Node.js.
- [mapbox-vector-tile](https://github.com/mapzen/mapbox-vector-tile) is a Python package for vector tile encoding maintained by Mapzen. (It is used in Mapzen's [vector tile service](http://mapzen.com/vector)).
- [geojson-vt](https://github.com/mapbox/geojson-vt) - Slice GeoJSON into vector tiles on the fly in the browser.
- [vt-geojson](https://github.com/developmentseed/vt-geojson) - Extract GeoJSON from Mapbox vector tiles.
- [vt2geojson](https://github.com/mapbox/vt2geojson) - Dump vector tiles to GeoJSON using node
- [vt-dumper](https://github.com/rclark/vt-dumper) - dump vector tiles to GeoJSON using node
- [java-vector-tile](https://github.com/ElectronicChartCentre/java-vector-tile) - A java encoder and decoder for vector tiles.
- [vector-tile in Scala](https://github.com/mraad/vector-tiles) - Heuristic Experiment on Encoding Mapbox Vector Tiles In Scala
- [MMT-Vector-Tiles](https://github.com/glob3mobile/mmt-vector-tiles) - A Tile-Vector generation library.


## Parsers & Generators in Practice
- [OSM2VectorTiles](https://github.com/osm2vectortiles/osm2vectortiles) - OSM2VectorTiles makes is possible to create vector tiles from OpenStreetMap data. [MBTi1es(PBF) download](http://osm2vectortiles.org/downloads).


## Clients

- [Mapbox GL Native](https://github.com/mapbox/mapbox-gl-native) - C++/OpenGL vector maps library.
- [Mapbox GL JS](https://github.com/mapbox/mapbox-gl-js) - JavaScript/WebGL vector maps library.
- [OpenLayers 3](https://github.com/openlayers/ol3/pull/4219) - JavaScript vector & raster library.
- [Leaflet.VectorGrid](https://github.com/IvanSanchez/Leaflet.VectorGrid) - Display gridded vector data (sliced GeoJSON or protobuf vector tiles) in Leaflet 1.0.0
- [WhirlyGlobe/Maply](https://github.com/mousebird/WhirlyGlobe/blob/master/WhirlyGlobeSrc/WhirlyGlobe-MaplyComponent/src/MaplyMapnikVectorTiles.mm) - Objective C code that is able to read and render vector tiles(and style with mapnik xml) on iOS devices.
- [Leaflet.MapboxVectorTile](https://github.com/SpatialServer/Leaflet.MapboxVectorTile) is able to read PBF MapboxVectorTiles from a REST endpoint and render them as a TileLayer on a Leaflet Map. Use this option if you want to utilize vector tiles on a standard Leaflet web map without needing WebGL.
- [Nutiteq Maps SDK 3.x](https://developer.nutiteq.com) - C++ maps library for iOS, Android, Windows Phone and Xamarin with bindings for Java, ObjectiveC and C#
- [Mapzen Tangram](https://github.com/tangrams/tangram) - JavaScript library for rendering 2D & 3D maps live in a web browser with WebGL, supports MVT, GeoJSON, TopoJSON
- [Mapzen Tangram-es](https://github.com/tangrams/tangram-es) - C++ library for rendering 2D and 3D maps using OpenGL ES 2 with custom styling and interactions
* [mapbox-gl-leaflet](https://github.com/mapbox/mapbox-gl-leaflet) - Create Mapbox GL layers in Leaflet
* [react-native-mapbox-gl](https://github.com/mapbox/react-native-mapbox-gl) - Render Mapbox GL maps from React applications
* [hoverbord](https://github.com/devTristan/hoverboard) - Render vector tiles on canvas with Leaflet (supports GeoJSON, TopoJSON, and protobuf)
- [d3-vector-tiles](https://github.com/hkrishna/d3-vector-tiles) - Adapting d3.geo.tile to show Mapzen vector tiles
- [arcgis-vectortile-style-editor](https://github.com/Esri/arcgis-vectortile-style-editor) - A simple Vector Tile Style Editor to update the styles of Esri Vector Basemaps
- [Vector-Tiles-Reader-QGIS-Plugin](https://github.com/geometalab/Vector-Tiles-Reader-QGIS-Plugin) - GIS Python plugin which reads Mapbox vector tiles from a local MBTiles file.



## Applications / Command line tools

- [Mapbox Studio](https://github.com/mapbox/mapbox-studio) - Desktop design studio for both creating vector tiles from raw geodata and for rendering them on-the-fly into image tiles. Internally uses `tilelive.js` modules to handle vector tiles (see `tilelive-bridge` and `tilelive-vector`)
- [kosmtik](https://github.com/kosmtik/kosmtik) - Design maps with CartoCSS and Mapnik.

## CLI Utilities
- [tippecanoe](https://github.com/mapbox/tippecanoe) - Build vector tilesets from large collections of GeoJSON features using c++.  reads GeoJSON output .mbtiles
- [tilemaker](https://github.com/systemed/tilemaker) - Command line tool to produce vector tiles directly from an .osm.pbf extract without an intermediate database. output to individual files, or to a SQLite (.mbtiles) database.
- [Datamaps](https://github.com/ericfischer/datamaps) C application that can be used to create vector tiles and store them in an mbtiles. See the `render-vector` command.
- [vector-tiles-producer](https://github.com/vross/vector-tiles-producer) Command line tool in C++ to creates vector tiles for a given area at chosen zoom levels using a Mapnik XML.
- [vt-geojson](https://github.com/developmentseed/vt-geojson) - decodes vector tiles to GeoJSON FeatureCollections
- [tl](https://github.com/mojodna/tl) - An alternate command line interface to tilelive

## Mapbox GL JS Plugins

- [gl-draw](https://github.com/mapbox/gl-draw) - Adds support for drawing and editing features on Mapbox GL JS maps

## Servers

- [tessera](https://github.com/mojodna/tessera) - Supports serving and rendering vector tiles. Uses the same core libraries as Mapbox Studio.
- [tilestrata](https://github.com/naturalatlas/tilestrata) - with tilestrata-vt, can generate vector tiles
- [SpatialServer (PGRestAPI)](https://github.com/spatialdev/PGRestAPI) - A multi-purpose GeoSpatial NodeJS web server created at [SpatialDev](http://spatialdev.com) that not only serves MBTiles stuffed with vector tiles, it can also cut vector tiles on the fly from a PostGIS database.
- [Utilery](https://github.com/tilery/utilery) Utilery serves protobuf vector tiles from a PostGIS database queries. Python based
- [Tilestache](https://github.com/mapzen/TileStache/) Mapzen fork. It supports mvt output tiles.
- [Kartotherian](https://github.com/kartotherian/kartotherian) Wikipedia tile server with [Tilerator](https://github.com/kartotherian/tilerator) backend tile pre-generator
- [TILESPLASH](https://github.com/faradayio/tilesplash) - a light and quick nodejs webserver for serving topojson vector tiles from a postgis backend
- [PostGIS Vector Tile Utils](https://github.com/mapbox/postgis-vt-util) - A set of PostgreSQL functions that are useful when creating vector tile sources. postgis-vt-util.sql or [an NPM module](https://www.npmjs.com/package/postgis-vt-util).
- [node-pgtiles](https://github.com/apburnes/node-pgtiles) - PostgreSQL schema for vector tiles. Modeled from [Mapbox mbtiles](https://github.com/mapbox/node-mbtiles) and [CartoDB postgresql extensions](https://github.com/CartoDB/cartodb-postgresql/tree/9114d4e463c8664c1fb31e3bc538ce96c0dd0771). 
- [tilez](https://github.com/AURIN/tilez) - A Node.js application serving vector tiles in GeoJSON or TopoJSON according to the TMS specification. VTS clips vector tiles from a PostgreSQL/PostGIS data source and stores them in CouchDB (acting as a cache). 
- [Dynamic Vector Tile](https://github.com/mraad/vector-tiles-boot) - Minimal Vector Tile Server for Web Mapping applications 


## Servers in practice
- [Mapbox vector tile service](https://www.mapbox.com/vector-tiles/) - mapbox powers osm street vector tiles in mapbox vector tile format
- [Mapzen vector tile service](https://mapzen.com/projects/vector-tiles/) - mapzen powers osm street vector tiles in geojson, topojson and mapbox vector tile format
- [self-hosted-vector-tiles](https://github.com/miccferr/self-hosted-vector-tiles) - An attempt to self host vt using tilemaker+tessera+tile-live
- [vector-tile-server](https://github.com/oneconcern/Vector-tile-server) - setting up a vector tile server and frontend using TileStache, tilelive and leaflet
- [TerriaJS-Vector-Tile-Server](https://github.com/TerriaJS/vector-tile-server) - sets up a Tessera server for use as a vector tile server for TerriaJS. It contains configuration, data and helper scripts. 
- [wandergis's Practice](https://github.com/wandergis/vector-tiles)
- [Japan GeoJSON vector tile service](https://github.com/gsi-cyberjapan/vector-tile-experiment) - Geospatial Information Authority of Japan (GSI, http://www.gsi.go.jp/ ) provides a vector tile service.

## Low-level utilities

- [mapbox-gl-function](https://github.com/mapbox/mapbox-gl-function) - Mapbox GL style function evaluator
- [mapbox-gl-filter-simplify](https://github.com/mapbox/mapbox-gl-filter-simplify) - Simplifies and complexifies filters in Mapbox GL Styles
- [vt-pbf](https://github.com/anandthakker/vt-pbf) serialize JavaScript objects representing vector tiles into binary Protocol Buffer encodings of vector tiles

## Vector Tiles Research
- [Vector Tiles Research](https://github.com/robpvn/Vector-Tile-Research) - Academic work exploring topology preservation 
- [overzooming/compositing vector tiles](https://github.com/springmeyer/vector-tile-overzoom-demo) - vector-tile-overzoom-demo using nodejs
- [vt-grid](https://github.com/developmentseed/vt-grid) - Build up a pyramid of Mapbox vector tiles by aggregating quantitative data into grids using nodejs.
- [road-diff](https://github.com/mapbox/road-diff) - A Tile Reduce-based script for comparing road networks of two vector tile sources (e.g. OSM and Tiger) based on nodejs.


## License

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Tom MacWright](http://macwright.org) has waived all copyright and related or neighboring rights to this work.
