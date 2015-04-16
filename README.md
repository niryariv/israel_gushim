SHP -> GeoJSON:

ogr2ogr -f GeoJSON -t_srs crs:84 out.geojson in.shp


ITM -> WGS84:

ogr2ogr -a_srs EPSG:2039 -f geojson out.geojson.itm in.geojson
ogr2ogr -t_srs EPSG:4326 -f geojson out.geojson.wgs in.geojson.itm


TopoJSON conversion: 
```topojson --id-property Name -p -q 1e5 -o <output-file> <geojson-file>```

Content accessible at http://niryariv.github.io/israel_gushim/{filename}, eg: http://niryariv.github.io/israel_gushim/arabe.topojson
