Please consider support for importing FlatGeoBuf, a GIS file format for storing simple features. 
The format is based on Google's flatbuffers http://google.github.io/flatbuffers/
It is suitable for streaming large volumes of data with bounding box filtering, a competitor to SHP/TAB and more performant than Geopackage and fills a performance/size gap in that interchange space. 
The  home page and specification https://bjornharrtell.github.io/flatgeobuf/
There are sample data sets in test/data/*.fgb
https://github.com/bjornharrtell/flatgeobuf/tree/master/test/data
The GDAL driver is https://gdal.org/drivers/vector/flatgeobuf.html

The format has its own twitter account and has interest in the R community particularly for streaming with {mapview} and {mapdeck} packages: 
https://twitter.com/flatgeobuf

https://twitter.com/search?q=%23rstats%20flatgeobuf%20&src=typed_query
It's otherwise very young though, so there aren't any providers of data in this format yet that I can find. 
