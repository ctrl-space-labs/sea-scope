



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD14A2\.061: Terra Thermal Anomalies \& Fire 8\-Day Global 1km


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================================








Dataset Availability
2000\-02\-18T00:00:00Z–2025\-07\-04T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MOD14A2.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MOD14A2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD14A2)





Cadence
8 Days
Tags


[8\-day](/earth-engine/datasets/tags/8-day)
[fire](/earth-engine/datasets/tags/fire)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[terra](/earth-engine/datasets/tags/terra)
[usgs](/earth-engine/datasets/tags/usgs)
mod14a2








#### Description



The MOD14A2 V6\.1 dataset provides 8\-day fire mask composites
at 1km resolution. It contains the maximum value of the individual
pixel classes over the compositing period. Along with the fire
mask, an associated quality information layer is also provided.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/876/MOD14_User_Guide_v6.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/87/MOD14_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MOD14A2)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Description |
| --- | --- |
| `FireMask` | Confidence of fire |
| Bitmask for FireMask * Bits 0\-3: Fire mask pixel classes 	+ 1: Not processed (obsolete; not used since Collection 1\) 	+ 2: Not processed (other reason) 	+ 3: Non\-fire water pixel 	+ 4: Cloud (land or water) 	+ 5: Non\-fire land pixel 	+ 6: Unknown (land or water) 	+ 7: Fire (low confidence, land or water) 	+ 8: Fire (nominal confidence, land or water) 	+ 9: Fire (high confidence, land or water) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `QA` | Pixel quality indicators |
| Bitmask for QA * Bits 0\-1: Land/water state 	+ 0: Water 	+ 1: Coast 	+ 2: Land 	+ 3: Missing data * Bit 2: Night/day 	+ 0: Night 	+ 1: Day | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MOD14A2\.061](https://doi.org/10.5067/MODIS/MOD14A2.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MOD14A2')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varfireMask=dataset.select('FireMask');
varfireMaskVis={
min:3.0,
max:8.0,
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(fireMask,fireMaskVis,'Fire Mask');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD14A2)


[MOD14A2\.061: Terra Thermal Anomalies \& Fire 8\-Day Global 1km](/earth-engine/datasets/catalog/MODIS_061_MOD14A2)

The MOD14A2 V6\.1 dataset provides 8\-day fire mask composites at 1km resolution. It contains the maximum value of the individual pixel classes over the compositing period. Along with the fire mask, an associated quality information layer is also provided. Documentation: User's Guide Algorithm Theoretical Basis Document (ATBD) General Documentation

 MODIS/061/MOD14A2,
 8\-day,fire,global,modis,nasa,terra,usgs

2000\-02\-18T00:00:00Z/2025\-07\-04T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MOD14A2\.061](https://doi.org/https://doi.org/10.5067/MODIS/MOD14A2.061)
* [https://doi.org/10\.5067/MODIS/MOD14A2\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD14A2)









