



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD19A2\.061: Terra \& Aqua MAIAC Land Aerosol Optical Depth Daily 1km


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-12T23:55:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD19A2.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD19A2_GRANULES")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD19A2_GRANULES)





Cadence
1 Day
Tags


[aerosol](/earth-engine/datasets/tags/aerosol)
[aod](/earth-engine/datasets/tags/aod)
[aqua](/earth-engine/datasets/tags/aqua)
[atmosphere](/earth-engine/datasets/tags/atmosphere)
[daily](/earth-engine/datasets/tags/daily)
[global](/earth-engine/datasets/tags/global)
[maiac](/earth-engine/datasets/tags/maiac)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[terra](/earth-engine/datasets/tags/terra)
[usgs](/earth-engine/datasets/tags/usgs)
mcd19a2








#### Description



The MCD19A2 V6\.1 data product is a MODIS Terra and Aqua combined Multi\-angle
Implementation of Atmospheric Correction (MAIAC) Land Aerosol Optical Depth
(AOD) gridded Level 2 product produced daily at 1 km resolution. For more
information see the [MAIAC user guide](https://lpdaac.usgs.gov/documents/1500/MCD19_User_Guide_V61.pdf).


NOTE: This product has been released with the caveat that the reprocessing
for the full mission is expected to continue through summer 2023\.





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `Optical_Depth_047` | None | \-100 | 8000 | 0\.001 | Aerosol optical depth over land retrieved in the MODIS Blue band (0\.47 μm). AOD is not received at high altitude (greater than 4\.2 km) except when smoke or dust is detected; rather, we report a static value of 0\.02 used for atmospheric correction. |
| `Optical_Depth_055` | None | \-100 | 8000 | 0\.001 | Aerosol optical depth over land retrieved in the MODIS Green band (0\.55 μm). |
| `AOD_Uncertainty` | None | 0 | 30000 | 0\.0001 | AOD uncertainty based on blue\-band surface brightness (reflectance) |
| `FineModeFraction` | None | 0 | 1000 |  | Fine mode fraction for ocean and large inland lakes |
| `Column_WV` | cm | 0 | 30000 | 0\.001 | Column water vapor over land, retrieved from MODIS near\-IR bands at 0\.94 μm. When reported for cloudy pixels, it represents water vapor above the cloud. |
| `AOD_QA` | None |  | AOD QA |
| Bitmask for AOD\_QA * Bits 0\-2: Cloud mask 	+ 0: Undefined 	+ 1: Clear 	+ 2: Possibly cloudy (detected by AOD filter) 	+ 3: Cloudy (detected by cloud mask algorithm) 	+ 5: Cloud shadow 	+ 6: Hot spot of fire 	+ 7: Water sediments * Bits 3\-4: Land water snow/ice mask 	+ 0: Land 	+ 1: Water 	+ 2: Snow 	+ 3: Ice * Bits 5\-7: Adjacency mask 	+ 0: Normal condition/Clear 	+ 1: Adjacent to clouds 	+ 2: Surrounded by more than 4 cloudy pixels 	+ 3: Adjacent to a single cloudy pixel 	+ 4: Adjacent to snow 	+ 5: Snow was previously detected in this pixel * Bits 8\-11: QA for AOD 	+ 0: Best quality 	+ 1: Water Sediments are detected (water) 	+ 3: There is 1 neighbor cloud 	+ 4: There is \>1 neighbor clouds 	+ 5: No retrieval (cloudy, or whatever) 	+ 6: No retrievals near detected or previously detected snow' 	+ 7: Climatology AOD \- altitude above 3\.5km (water) and 4\.2km 	(land)' 	+ 8: No retrieval due to sun glint (water) 	+ 9: Retrieved AOD is very low (\<0\.05\) due to glint (water) 	+ 10: AOD within \+\-2km from the coastline is replaced by nearby 	AOD 	+ 11: Land, research quality: AOD retrieved but CM is possibly 	cloudy * Bit 12: Glint mask 	+ 0: No glint 	+ 1: Glint (glint angle \< 40°) * Bits 13\-14: Aerosol model 	+ 0: Background model (regional) 	+ 1: Smoke model (regional) 	+ 2: Dust model * Bit 15: Reserved 	+ 0: Reserved for future use 	+ 1: Reserved for future use | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `Injection_Height` | m | 0 | 10000 |  | Smoke injection height |
| `AngstromExp_470-780` | None | 0\.0001 | Angstrom exponent 470\-780nm over the ocean |
| `cosSZA` | None | 0 | 10000 | 0\.0001 | Cosine of solar zenith angle (5 km resolution) |
| `cosVZA` | None | 0 | 10000 | 0\.0001 | Cosine view zenith angle (5 km resolution) |
| `RelAZ` | None | \-18000 | 18000 | 0\.01 | Relative azimuth angle (5 km resolution) |
| `Scattering_Angle` | None | \-18000 | 18000 | 0\.01 | Scattering angle (5 km resolution) |
| `Glint_Angle` | None | \-18000 | 18000 | 0\.01 | Glint angle (5 km resolution) |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD19A2\.061](https://doi.org/10.5067/MODIS/MCD19A2.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcollection=ee.ImageCollection('MODIS/061/MCD19A2_GRANULES')
.select('Optical_Depth_047')
.filterDate('2023-01-01','2023-01-15');

varband_viz={
min:0,
max:1100,
palette:['black','blue','purple','cyan','green','yellow','red']
};

Map.addLayer(collection.mean(),band_viz,'Optical Depth 047');
Map.setCenter(76,13,6);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD19A2_GRANULES)


[MCD19A2\.061: Terra \& Aqua MAIAC Land Aerosol Optical Depth Daily 1km](/earth-engine/datasets/catalog/MODIS_061_MCD19A2_GRANULES)

The MCD19A2 V6\.1 data product is a MODIS Terra and Aqua combined Multi\-angle Implementation of Atmospheric Correction (MAIAC) Land Aerosol Optical Depth (AOD) gridded Level 2 product produced daily at 1 km resolution. For more information see the MAIAC user guide. NOTE: This product has been released with the caveat …

 MODIS/061/MCD19A2\_GRANULES,
 aerosol,aod,aqua,atmosphere,daily,global,maiac,modis,nasa,terra,usgs

2000\-02\-24T00:00:00Z/2025\-07\-12T23:55:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD19A2\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD19A2.061)
* [https://doi.org/10\.5067/MODIS/MCD19A2\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD19A2_GRANULES)









