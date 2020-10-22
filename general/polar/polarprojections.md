email sent 2015-12-29

---

This is a request to extend Manifold's internal smarts about projection metadata for drawings. My example files were generated with an R script, which I've also attached as an html report, just for the record. Everything attached is in a single .zip file, there are 3 shapefiles and 3 MapInfo files and the .html page. 

I've attached versions of a polygon drawing of Antarctica in MIF and SHP format, in Longitude/Latitude and two polar projections. The files are named "antarctica[_projcode].[mif/shp]", where "projcode" is the PROJ.4 code for the projection family, for the projected files. 

When importing the MIF files the Stereographic projection is not applied, though the Lambert Azimuthal Equal Area and parameters is fine. With the shapefiles the projected drawings don't get the correct details from the .prj. 

Specific problems: 

1) antarctica_laea.shp - the LambertAzimuthal Equal Area projection is correctly chosen, but the Center Longitude and Center Latitude are still defaults, they should be 147 and -90 respectively. 

2) antarctica_stere.shp - there's no application of the Stereographic projection at all, it's in the default Orthographic

3) antarctica_stere.mif - there's no application of the Stereographic projection at all, it's in the default Orthographic


Please investigate and add the right PRJ interpretation to Manifold to fix problems 1) and 2). 

If it's a Manifold read problem with 3) please add that too. (I believe the problem in MIF for 3) may be a limitation of that format, since the metadata doesn't round trip through GDAL anyway.) 

(My R code also makes GeoTIFFs, but there's a longer story for those which I'll write about separately). 
