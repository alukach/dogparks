# Calgary Dogparks Map

## Data

First step was to head on over to the [City of Calgary's Data Portal][calgary-data-portal]. A search for "Off Leash" yielded the city's "[City Amenities][city-amenities]". I downloaded the data as a Shapefile and, after opening it up in [QGIS][qgis], I was dismayed to find that the data was in Point form.

* [Natural Areas][natural-areas] - Contains polygons of 'non-park' green space
* [Parks Turf][parks-turf] - Contains polygons of city parks
* [City Amenities][city-amenities] - Contains points of a number of city amenities, including off-leash areas.


1. _Filter Data for `"TYPE" = 'Off Leash Dog Area'`_
1. _Find intersecting polygons: ~~[Point in Polygon Query][point-in-polygon]~~ [Spatial Join][spatial-joins]_
1. _Merge files (`ParkTurfs_w_DogParks` & `NaturalAreas_w_DogParks`)_
1. _Find polygons w/o points [TODO]_
1. _[Export to GeoJSON][qgis-export] (whilst [reprojection to epsg:4326](http://gis.stackexchange.com/questions/35590/how-to-reproject-a-vector-layer-in-qgis))_


<!-- Data -->
[calgary-data-portal]: https://data.calgary.ca/ "City of Calgary Data Portal"
[city-amenities]: https://data.calgary.ca/OpenData/Pages/DatasetDetails.aspx?DatasetID=PDC0-99999-99999-00201-P(CITYonlineDefault)  "City Amenities"
[parks-turf]: https://data.calgary.ca/OpenData/Pages/DatasetDetails.aspx?DatasetID=PDC0-99999-99999-00307-P(CITYonlineDefault) "Parks Turf"
[natural-areas]: https://data.calgary.ca/OpenData/Pages/DatasetDetails.aspx?DatasetID=PDC0-99999-99999-00306-P(CITYonlineDefault) "Natural Areas"
[qgis]: http://qgis.org/ "QGIS"

<!-- QGIS -->
[point-in-polygon]: http://maps.cga.harvard.edu/qgis/wkshop/pt_in_pgn.php "Point in Polygon Query"
[spatial-joins]: http://www.qgistutorials.com/en/docs/performing_spatial_joins.html "Performing Spatial Joins"
[qgis-export]: http://maps.cga.harvard.edu/qgis/wkshop/export_GIS.php "Export Data in Vector GIS formats"
