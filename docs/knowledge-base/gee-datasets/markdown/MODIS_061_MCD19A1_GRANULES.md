



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD19A1\.061: Land Surface BRF Daily L2G Global 500m and 1km


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================================








Dataset Availability
2000\-12\-21T00:00:00Z–2025\-07\-12T23:55:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD19A1.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD19A1_GRANULES")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD19A1_GRANULES)





Cadence
1 Day
Tags


[aerosol](/earth-engine/datasets/tags/aerosol)
[aod](/earth-engine/datasets/tags/aod)
[aqua](/earth-engine/datasets/tags/aqua)
[daily](/earth-engine/datasets/tags/daily)
[global](/earth-engine/datasets/tags/global)
[maiac](/earth-engine/datasets/tags/maiac)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[terra](/earth-engine/datasets/tags/terra)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The MCD19A1 Version 6\.1 data product is a Moderate Resolution Imaging
Spectroradiometer (MODIS) Terra and Aqua combined Land Surface Bidirectional
Reflectance Factor (BRF) gridded Level 2 product produced daily at 500 meter
and 1 kilometer resolution. For more information see the
[MAIAC user guide](https://lpdaac.usgs.gov/documents/1500/MCD19_User_Guide_V61.pdf).





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- |
| `Sur_refl1` | \-100 | 16000 | 0\.0001 | Surface reflectance at 500m for band 1\. |
| `Sur_refl2` | \-100 | 16000 | 0\.0001 | Surface reflectance at 500m for band 2\. |
| `Sur_refl3` | \-100 | 16000 | 0\.0001 | Surface reflectance at 500m for band 3\. |
| `Sur_refl4` | \-100 | 16000 | 0\.0001 | Surface reflectance at 500m for band 4\. |
| `Sur_refl5` | \-100 | 16000 | 0\.0001 | Surface reflectance at 500m for band 5\. |
| `Sur_refl6` | \-100 | 16000 | 0\.0001 | Surface reflectance at 500m for band 6\. |
| `Sur_refl7` | \-100 | 16000 | 0\.0001 | Surface reflectance at 500m for band 7\. |
| `Sur_refl8` | \-100 | 16000 | 0\.0001 | Surface reflectance at 1km for band 8\. |
| `Sur_refl9` | \-100 | 16000 | 0\.0001 | Surface reflectance at 1km for band 9\. |
| `Sur_refl10` | \-100 | 16000 | 0\.0001 | Surface reflectance at 1km for band 10\. |
| `Sur_refl11` | \-100 | 16000 | 0\.0001 | Surface reflectance at 1km for band 11\. |
| `Sur_refl12` | \-100 | 16000 | 0\.0001 | Surface reflectance at 1km for band 12\. |
| `Sigma_BRFn1` | \-100 | 16000 | 0\.0001 | BRFn uncertainty over time at 1km, for band 1 |
| `Sigma_BRFn2` | \-100 | 16000 | 0\.0001 | BRFn uncertainty over time at 1km, for band 2 |
| `Status_QA` |  | QA bits |
| Bitmask for Status\_QA * Bits 0\-2: Cloud mask 	+ 0: Undefined 	+ 1: Clear 	+ 2: Possibly cloudy (detected by AOD filter) 	+ 3: Cloudy (detected by cloud mask algorithm) 	+ 5: Cloud shadow 	+ 6: Hot spot of fire 	+ 7: Water sediments * Bits 3\-4: Land water snow/ice mask 	+ 0: Land 	+ 1: Water 	+ 2: Snow 	+ 3: Ice * Bits 5\-7: Adjacency mask 	+ 0: Normal condition/Clear 	+ 1: Adjacent to clouds 	+ 2: Surrounded by more than 4 cloudy pixels 	+ 3: Adjacent to a single cloudy pixel 	+ 4: Adjacent to snow 	+ 5: Snow was previously detected in this pixel * Bit 8: AOD level 	+ 0: AOD is low (\<\=0\.6\) 	+ 1: AOD is high (\> 0\.6\) or undefined * Bits 9\-10: AOD Type 	+ 0: Background aerosol 	+ 1: Smoke 	+ 2: Dust * Bit 11: BRF retrieved over snow assuming AOD \= 0\.05 	+ 0: no 	+ 1: yes * Bit 12: Altitude \>4\.2km (land)/3\.5km (water), BRF is retrieved using climatology AOD \=0\.02 	+ 0: no 	+ 1: yes * Bits 13\-15: Surface Change Mask 	+ 0: No change 	+ 1: Regular change Green up (Relative change in Red and NIR 	nadir\-normalized BRF is more than 5% but less than 15%). 	+ 2: Big change Green up (Relative change in Red and NIR 	nadir\-normalized BRF is more than 15%). 	+ 3: Regular change Senescence 	+ 4: Big change Senescence | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `cosSZA` | 0 | 10000 | 0\.0001 | Cosine of Solar zenith angle (5 km resulution) |
| `cosVZA` | 0 | 10000 | 0\.0001 | Cosine view zenith angle (5 km resolution) |
| `RelAZ` | \-18000 | 18000 | 0\.01 | Relative azimuth angle (5 km resolution) |
| `Scattering_Angle` | \-18000 | 18000 | 0\.01 | Scattering angle (5 km resolution) |
| `SAZ` | \-18000 | 18000 | 0\.01 | Solar Azimuth Angle (5 km resolution) |
| `VAZ` | \-18000 | 18000 | 0\.01 | View Azimuth Angle (5 km resolution) |
| `Glint_Angle` | \-18000 | 18000 | 0\.01 | Glint angle (5 km resolution) |
| `Fv` | \-100 | 100 |  | RTLS volumetric kernel (5 km resolution) |
| `Fg` | \-100 | 100 |  | RTLS geometric kernel (5 km resolution) |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD19A1\.061](https://doi.org/10.5067/MODIS/MCD19A1.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcollection=ee.ImageCollection('MODIS/061/MCD19A1_GRANULES')
.select('Sur_refl1')
.filterDate('2000-01-01','2000-03-07');

varband_viz={
min:0,
max:1100,
palette:['black','blue','purple','cyan','green','yellow','red']
};

Map.addLayer(collection.mean(),band_viz,'Surface Bidirectional Reflectance Factor');
Map.setCenter(76,13,6);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD19A1_GRANULES)


[MCD19A1\.061: Land Surface BRF Daily L2G Global 500m and 1km](/earth-engine/datasets/catalog/MODIS_061_MCD19A1_GRANULES)

The MCD19A1 Version 6\.1 data product is a Moderate Resolution Imaging Spectroradiometer (MODIS) Terra and Aqua combined Land Surface Bidirectional Reflectance Factor (BRF) gridded Level 2 product produced daily at 500 meter and 1 kilometer resolution. For more information see the MAIAC user guide.

 MODIS/061/MCD19A1\_GRANULES,
 aerosol,aod,aqua,daily,global,maiac,modis,nasa,satellite\-imagery,terra,usgs

2000\-12\-21T00:00:00Z/2025\-07\-12T23:55:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD19A1\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD19A1.061)
* [https://doi.org/10\.5067/MODIS/MCD19A1\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD19A1_GRANULES)









