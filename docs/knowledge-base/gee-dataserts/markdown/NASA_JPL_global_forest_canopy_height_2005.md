



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global Forest Canopy Height, 2005


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================








Dataset Availability
2005\-05\-20T00:00:00Z–2005\-06\-23T00:00:00Z
Dataset Provider


[NASA/JPL](https://earthobservatory.nasa.gov)



Earth Engine Snippet


`ee.Image("NASA/JPL/global_forest_canopy_height_2005")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_JPL_global_forest_canopy_height_2005)





Tags


[canopy](/earth-engine/datasets/tags/canopy)
[forest](/earth-engine/datasets/tags/forest)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[geophysical](/earth-engine/datasets/tags/geophysical)
[jpl](/earth-engine/datasets/tags/jpl)
[nasa](/earth-engine/datasets/tags/nasa)
glas








#### Description



This dataset represents global tree heights based on a fusion of
spaceborne\-lidar data (2005\) from the Geoscience Laser Altimeter
System (GLAS) and ancillary geospatial data. See
[Simard et al. (2011\)](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/2011JG001708)
for details.





### Bands



**Pixel Size**
  
927\.67 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `1` | m | 0\* | 73\* | Tree heights |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


Most materials published on the Earth Observatory, including images, are
freely available for re\-publication or re\-use, including commercial
purposes, except for where copyright is indicated.


NASA's Earth Observatory must be given credit for its original materials;
the only mandatory credit is NASA.


For more information about using NASA imagery visit the [Earth Observatory
Image Use Policy](https://earthobservatory.nasa.gov/ImageUse/) site.




### Citations



Citations:
* Simard, M., Pinto, N., Fisher, J., Baccini, A. 2011\. Mapping forest
canopy height globally with spaceborne lidar. Journal of Geophysical
Research. 116: G04021\.
[doi:10\.1029/2011JG001708](https://doi.org/10.1029/2011JG001708)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('NASA/JPL/global_forest_canopy_height_2005');
varforestCanopyHeight=dataset.select('1');
varforestCanopyHeightVis={
min:0.0,
max:30.0,
palette:[
'ffffff','fcd163','99b718','66a000','3e8601','207401','056201',
'004c00','011301'
],
};
Map.setCenter(-28.1,28.3,1);
Map.addLayer(forestCanopyHeight,forestCanopyHeightVis,'Forest Canopy Height');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_JPL_global_forest_canopy_height_2005)


[Global Forest Canopy Height, 2005](/earth-engine/datasets/catalog/NASA_JPL_global_forest_canopy_height_2005)

This dataset represents global tree heights based on a fusion of spaceborne\-lidar data (2005\) from the Geoscience Laser Altimeter System (GLAS) and ancillary geospatial data. See Simard et al. (2011\) for details.

 NASA/JPL/global\_forest\_canopy\_height\_2005,
 canopy,forest,forest\-biomass,geophysical,jpl,nasa

2005\-05\-20T00:00:00Z/2005\-06\-23T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








