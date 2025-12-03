



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD14A1\.061: Terra Thermal Anomalies \& Fire Daily Global 1km


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-11T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MOD14A1.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MOD14A1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD14A1)





Cadence
1 Day
Tags


[daily](/earth-engine/datasets/tags/daily)
[fire](/earth-engine/datasets/tags/fire)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[terra](/earth-engine/datasets/tags/terra)
[usgs](/earth-engine/datasets/tags/usgs)
mod14a1








#### Description



The MOD14A1 V6\.1 dataset provides daily fire mask composites
at 1km resolution derived from the MODIS 4\- and 11\-micrometer radiances.
The fire detection strategy is based on absolute detection of a
fire (when the fire strength is sufficient to detect), and on detection
relative to its background (to account for variability of the surface
temperature and reflection by sunlight). The product distinguishes
between fire, no fire and no observation. This information is used
for monitoring the spatial and temporal distribution of fires in
different ecosystems, detecting changes in fire distribution and
identifying new fire frontiers, wild fires, and changes in the
frequency of the fires or their relative strength.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/1005/MOD14_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/87/MOD14_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MOD14A1)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `FireMask` | None |  | Confidence of fire |
| Bitmask for FireMask * Bits 0\-3: Fire mask pixel classes 	+ 1: Not processed (obsolete; not used since Collection 1\) 	+ 2: Not processed (other reason) 	+ 3: Non\-fire water pixel 	+ 4: Cloud (land or water) 	+ 5: Non\-fire land pixel 	+ 6: Unknown (land or water) 	+ 7: Fire (low confidence, land or water) 	+ 8: Fire (nominal confidence, land or water) 	+ 9: Fire (high confidence, land or water) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `MaxFRP` | MW | 0 | 180000 | 0\.1 | Maximum fire radiative power |
| `sample` | None | 0 | 1353 |  | Position of fire pixel within scan |
| `QA` | None |  | Pixel quality indicators |
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


* [https://doi.org/10\.5067/MODIS/MOD14A1\.061](https://doi.org/10.5067/MODIS/MOD14A1.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MOD14A1')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varfireMaskVis={
min:0.0,
max:6000.0,
bands:['MaxFRP','FireMask','FireMask'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(dataset,fireMaskVis,'Fire Mask');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD14A1)


[MOD14A1\.061: Terra Thermal Anomalies \& Fire Daily Global 1km](/earth-engine/datasets/catalog/MODIS_061_MOD14A1)

The MOD14A1 V6\.1 dataset provides daily fire mask composites at 1km resolution derived from the MODIS 4\- and 11\-micrometer radiances. The fire detection strategy is based on absolute detection of a fire (when the fire strength is sufficient to detect), and on detection relative to its background (to account for …

 MODIS/061/MOD14A1,
 daily,fire,global,modis,nasa,terra,usgs

2000\-02\-24T00:00:00Z/2025\-07\-11T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MOD14A1\.061](https://doi.org/https://doi.org/10.5067/MODIS/MOD14A1.061)
* [https://doi.org/10\.5067/MODIS/MOD14A1\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD14A1)









