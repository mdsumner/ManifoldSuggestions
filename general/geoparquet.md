Dear Manifold, 
The Apache Arrow project provides a columnar memory format, and the Apache Parquet format provides a complementary columnar file format. 
Apache Arrow:  https://arrow.apache.org/
Apache Parquet: https://parquet.apache.org/
There is an emerging geospatial data specification for Arrow and Parquet "geoarrow", with implementations in Python (GeoPandas) and in R, and in GDAL. 
Geospatial capabilities in the Parquet format show promise to be the cloud-native vector format to match COG-GeoTIFF, with the benefits of speed suited to columnar based spatial tools (like those in R and Python), and a language independent library and format implementation. 
Please consider supporting Parquet and the emerging geoarrow GeoParquet format.  Prototypes in R and Python show that raw read times are several times faster than the by-feature approach currently required by GDAL. 
The geoarrow specification project is here: 
https://github.com/geopandas/geo-arrow-spec
Here are details of developments from GDAL, R, and Python to support Arrow and Parquet for spatial data: 
1) GDAL RFC to support columnar-oriented data: https://github.com/OSGeo/gdal/pull/5830
2) Prototype R package geoarrow: https://github.com/paleolimbot/geoarrow
3) Prototype Python package geoarrow: https://github.com/jorisvandenbossche/python-geoarrow


What follows are recent blog posts for GeoParquet itself, prototypes in R and in Python.  2) and 3)  contextualize the R and Python developments, the first especially shows the speed of raw read compared to use of the GDAL by-feature approach used currently. The section "Reading files" in this first post show the parquet read is several times faster than direct use of current GDAL:  
1) Blog post introducing GeoParquet: https://carto.com/blog/introducing-geoparquet-geospatial-compatibility/
2) https://dewey.dunnington.ca/post/2022/building-bridges-arrow-parquet-and-geospatial-computing/

3) https://cholmes.medium.com/an-overview-of-cloud-native-vector-c223845638e0

Best regards, Mike


