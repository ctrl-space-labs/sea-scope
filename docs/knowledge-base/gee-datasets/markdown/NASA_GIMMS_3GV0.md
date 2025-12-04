



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GIMMS NDVI From AVHRR Sensors (3rd Generation)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================








Dataset Availability
1981\-07\-01T00:00:00Z–2013\-12\-16T00:00:00Z
Dataset Provider


[NASA/NOAA](https://nex.nasa.gov/nex/projects/1349/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GIMMS/3GV0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GIMMS_3GV0)





Cadence
15 Days
Tags


[avhrr](/earth-engine/datasets/tags/avhrr)
[nasa](/earth-engine/datasets/tags/nasa)
[ndvi](/earth-engine/datasets/tags/ndvi)
[noaa](/earth-engine/datasets/tags/noaa)
[vegetation](/earth-engine/datasets/tags/vegetation)
[vegetation\-indices](/earth-engine/datasets/tags/vegetation-indices)
gimms








#### Description



GIMMS NDVI is generated from several NOAA's AVHRR sensors for a global
1/12\-degree lat/lon grid. The latest version of the GIMMS NDVI dataset
is named NDVI3g (third generation GIMMS NDVI from AVHRR sensors).





### Bands



**Pixel Size**
  
9277 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `ndvi` | \-1 | 1 | NDVI |
| `qa` | QA flag |
| Bitmask for qa * Bits 0\-2: QA flag values 	+ 1: Good value 	+ 2: Good value 	+ 3: NDVI retrieved from spline interpolation 	+ 4: NDVI retrieved from spline interpolation, possibly snow 	+ 5: NDVI retrieved from average seasonal profile 	+ 6: NDVI retrieved from average seasonal profile, possibly snow 	+ 7: Missing data | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/GIMMS/3GV0')
.filter(ee.Filter.date('2013-06-01','2013-12-31'));
varndvi=dataset.select('ndvi');
varndviVis={
min:-1.0,
max:1.0,
palette:['000000','f5f5f5','119701'],
};
Map.setCenter(-88.6,26.4,1);
Map.addLayer(ndvi,ndviVis,'NDVI');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GIMMS_3GV0)


[GIMMS NDVI From AVHRR Sensors (3rd Generation)](/earth-engine/datasets/catalog/NASA_GIMMS_3GV0)

GIMMS NDVI is generated from several NOAA's AVHRR sensors for a global 1/12\-degree lat/lon grid. The latest version of the GIMMS NDVI dataset is named NDVI3g (third generation GIMMS NDVI from AVHRR sensors).

 NASA/GIMMS/3GV0,
 avhrr,nasa,ndvi,noaa,vegetation,vegetation\-indices

1981\-07\-01T00:00:00Z/2013\-12\-16T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








