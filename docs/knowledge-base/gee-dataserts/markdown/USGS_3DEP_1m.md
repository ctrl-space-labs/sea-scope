



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

USGS 3DEP 1m National Map


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================








Dataset Availability
2015\-01\-01T00:00:00Z–2006\-01\-01T00:00:00Z
Dataset Provider


[United States Geological Survey](https://www.sciencebase.gov/catalog/item/543e6b86e4b0fd76af69cf4c)



Earth Engine Snippet


`ee.ImageCollection("USGS/3DEP/1m")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_3DEP_1m)





Tags


[3dep](/earth-engine/datasets/tags/3dep)
[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[geophysical](/earth-engine/datasets/tags/geophysical)
[topography](/earth-engine/datasets/tags/topography)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



This is a tiled collection of images with 1m pixel size from the 3D
Elevation Program (3DEP). The 3DEP data holdings serve as the elevation
layer of The National Map and provide foundational elevation information for
earth science studies and mapping applications in the United States.


The elevations in this DEM represent the topographic bare\-earth surface.
USGS standard 1m pixel size DEMs are produced exclusively from high
resolution light detection and ranging (lidar) source data of images with 1m
pixel size or higher resolution. 1m pixel size DEM surfaces are seamless
within collection projects but not necessarily seamless across projects.
The spatial reference used for tiles of the 1m pixel size DEM within the
conterminous United States (CONUS) is Universal Transverse Mercator (UTM) in
units of meters and in conformance with the North American Datum of 1983
(NAD83\). All bare earth elevation values are in meters and are referenced to
the North American Vertical Datum of 1988 (NAVD88\). Each tile is distributed
in the UTM Zone in which it lies. If a tile crosses two UTM zones, it is
delivered in both zones.
In this and other cases of image overlaps, elevation values might be
slightly different in different images covering the same area.


The 1m pixel size DEM is the highest resolution standard DEM offered in the
3DEP product suite. The 10m 3DEP dataset is available at
[USGS\_3DEP\_10m](/earth-engine/datasets/catalog/USGS_3DEP_10m).





### Bands


**Bands**




| Name | Units | Pixel Size | Description |
| --- | --- | --- | --- |
| `elevation` | m | Elevation (NAVD88\) |




### Terms of Use


**Terms of Use**


Most U.S. Geological Survey (USGS) information resides
in the public domain and may be used without restriction. Additional
information on [Acknowledging or Crediting USGS as Information
Source](https://www.usgs.gov/information-policies-and-instructions/crediting-usgs)
is available.




### Citations



Citations:
* U.S. Geological Survey, 3D Elevation Program 1\-Meter Resolution Digital
Elevation Model.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('USGS/3DEP/1m');
varvisualization={
min:0,
max:3000,
palette:[
'3ae237','b5e22e','d6e21f','fff705','ffd611','ffb613','ff8b13',
'ff6e08','ff500d','ff0000','de0101','c21301','0602ff','235cb1',
'307ef3','269db1','30c8e2','32d3ef','3be285','3ff38f','86e26f'
],
};
Map.setCenter(-119.0,34.6,10);
Map.addLayer(dataset,visualization,'elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_3DEP_1m)


[USGS 3DEP 1m National Map](/earth-engine/datasets/catalog/USGS_3DEP_1m)

This is a tiled collection of images with 1m pixel size from the 3D Elevation Program (3DEP). The 3DEP data holdings serve as the elevation layer of The National Map and provide foundational elevation information for earth science studies and mapping applications in the United States. The elevations in this …

 USGS/3DEP/1m,
 3dep,dem,elevation,elevation\-topography,geophysical,topography,usgs

2015\-01\-01T00:00:00Z/2006\-01\-01T00:00:00Z



 \-16\.6 \-171 76\.9 164
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








