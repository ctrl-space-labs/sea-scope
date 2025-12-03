



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD44W.006 Terra Land Water Mask Derived From MODIS and SRTM Yearly Global 250m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2015\-01\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MOD44W.006)



Earth Engine Snippet


`ee.ImageCollection("MODIS/006/MOD44W")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_006_MOD44W)





Cadence
1 Year
Tags


[geophysical](/earth-engine/datasets/tags/geophysical)
[mod44w](/earth-engine/datasets/tags/mod44w)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[srtm](/earth-engine/datasets/tags/srtm)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[usgs](/earth-engine/datasets/tags/usgs)
[water\-mask](/earth-engine/datasets/tags/water-mask)








#### Description



The MOD44W V6 land/water mask 250m product is derived using a
decision tree classifier trained with MODIS data and validated with the
MOD44W V5 product. A series of masks are applied to address known issues
caused by terrain shadow, burn scars, cloudiness, or ice cover in oceans.





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Description |
| --- | --- |
| `water_mask` | Land\-water mask |
| Bitmask for water\_mask * Bit 0: Land\-water mask 	+ 0: Land 	+ 1: Water | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `water_mask_QA` | Quality assurance (QA) |
| Bitmask for water\_mask\_QA * Bits 0\-3: Quality assurance (QA) 	+ 1: High confidence observation 	+ 2: Lower confidence water, but MOD44W V5 is water 	+ 3: Lower confidence land 	+ 4: Ocean mask 	+ 5: Ocean mask, but no water detected 	+ 6: Burned area (MCD64A1\) 	+ 7: Urban or impervious surface 	+ 8: No water detected, Version 5 MOD44W shows inland water 	+ 10: No data (outside of projected area) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MOD44W.006](https://doi.org/10.5067/MODIS/MOD44W.006)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/006/MOD44W')
.filter(ee.Filter.date('2015-01-01','2015-05-01'));
varwaterMask=dataset.select('water_mask');
varwaterMaskVis={
min:0,
max:1,
palette:['bcba99','2d0491'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(waterMask,waterMaskVis,'Water Mask');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_006_MOD44W)


[MOD44W.006 Terra Land Water Mask Derived From MODIS and SRTM Yearly Global 250m](/earth-engine/datasets/catalog/MODIS_006_MOD44W)

The MOD44W V6 land/water mask 250m product is derived using a decision tree classifier trained with MODIS data and validated with the MOD44W V5 product. A series of masks are applied to address known issues caused by terrain shadow, burn scars, cloudiness, or ice cover in oceans.

 MODIS/006/MOD44W,
 geophysical,mod44w,modis,nasa,srtm,surface\-ground\-water,usgs,water\-mask

2000\-01\-01T00:00:00Z/2015\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MOD44W.006](https://doi.org/https://doi.org/10.5067/MODIS/MOD44W.006)
* [https://doi.org/10\.5067/MODIS/MOD44W.006](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD44W)









