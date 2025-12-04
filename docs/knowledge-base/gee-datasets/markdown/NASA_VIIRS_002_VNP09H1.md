



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP09H1: VIIRS Surface Reflectance 8\-Day L3 Global 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================================








Dataset Availability
2012\-01\-19T00:00:00Z–2025\-06\-18T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/VIIRS/VNP09H1.002)



Earth Engine Snippet


`ee.ImageCollection("NASA/VIIRS/002/VNP09H1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP09H1)





Cadence
1 Day
Tags


[daily](/earth-engine/datasets/tags/daily)
[nasa](/earth-engine/datasets/tags/nasa)
[noaa](/earth-engine/datasets/tags/noaa)
[npp](/earth-engine/datasets/tags/npp)
[reflectance](/earth-engine/datasets/tags/reflectance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sr](/earth-engine/datasets/tags/sr)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The 8\-day Visible Infrared Imaging Radiometer Suite (VIIRS) Surface
Reflectance (VNP09H1\) Version 1 composite product provides an estimate of
land surface reflectance from the Suomi National Polar\-orbiting Partnership
(Suomi NPP) VIIRS sensor for three imagery bands (I1, I2, I3\) at nominal
500m resolution (\~463m). The 500m dataset is derived through resampling the
native 375m VIIRS resolution in the L2 input product. The data are corrected
for atmospheric conditions such as the effects of molecular gases, including
ozone and water vapor, and for the effects of atmospheric aerosols. Each
pixel represents the best possible Level 2G observation during an 8\-day
period, which is selected on the basis of high observation coverage, low
sensor angle, the absence of clouds or cloud shadow, and aerosol loading.
The three reflectance bands, this product includes a state quality assurance
(QA) layer and a reflectance band quality layer.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/1657/VNP09_User_Guide_V2.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/122/VNP09_ATBD.pdf)
* [General Documentation](https://lpdaac.usgs.gov/products/vnp09h1v002/)
* [Land Product Quality Assessment website](https://landweb.modaps.eosdis.nasa.gov/browse?sensor=VIIRS&sat=SNPP)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `SurfReflect_I1` | \-100 | 16000 | 500 m Surface Reflectance Band I1 |
| `SurfReflect_I2` | \-100 | 16000 | 500 m Surface Reflectance Band I2 |
| `SurfReflect_I3` | \-100 | 16000 | 500 m Surface Reflectance Band I3 |
| `SurfReflect_QC_500m` | Surface Reflectance Band Quality Control (QC) |
| Bitmask for SurfReflect\_QC\_500m * Bits 0\-1: MODLAND QA bits 	+ 0: Corrected product produced at ideal quality all bands 	+ 1: Corrected product produced at less than ideal quality some 	or all bands 	+ 2: Corrected product not produced due to cloud effects all 	bands 	+ 3: Corrected product not produced due to other reasons some or 	all bands may be fill value \[Note that a value of (11\) 	overrides a value of (01\)]. * Bits 2\-3: Cloud State 	+ 0: Clear 	+ 1: Cloudy 	+ 2: Mixed 	+ 3: Not set, assumed clear * Bits 4\-7: Band 1 data quality four bit range 	+ 0: Highest quality 	+ 1: Noisy detector 	+ 2: Dead detector, data interpolated in L1B 	+ 3: Solar zenith \>\= 86 degrees 	+ 4: Solar zenith \>\= 85 and \< 86 degrees 	+ 5: Missing input 	+ 6: Internal constant used in place of climatological data for 	at least one atmospheric constant 	+ 7: Correction out of bounds, pixel constrained to extreme 	allowable value 	+ 8: L1B data faulty 	+ 9: Not processed due to deep ocean or clouds * Bits 8\-11: Band 2 data quality four bit range 	+ 0: Highest quality 	+ 1: Noisy detector 	+ 2: Dead detector, data interpolated in L1B 	+ 3: Solar zenith \>\= 86 degrees 	+ 4: Solar zenith \>\= 85 and \< 86 degrees 	+ 5: Missing input 	+ 6: Internal constant used in place of climatological data for 	at least one atmospheric constant 	+ 7: Correction out of bounds, pixel constrained to extreme 	allowable value 	+ 8: L1B data faulty 	+ 9: Not processed due to deep ocean or clouds * Bit 12: Atmospheric correction performed 	+ 0: No 	+ 1: Yes * Bit 13: Adjacency correction performed 	+ 0: No 	+ 1: Yes * Bit 14: Different orbit from 500m 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `SurfReflect_State_500m` | Surface Reflectance State Quality Assurance (QA) |
| Bitmask for SurfReflect\_State\_500m * Bits 0\-1: Cloud state 	+ 0: Clear 	+ 1: Cloudy 	+ 2: Mixed 	+ 3: Not set, assumed clear * Bit 2: Cloud shadow 	+ 0: No 	+ 1: Yes * Bits 3\-5: Land/water flag 	+ 0: Shallow ocean 	+ 1: Land 	+ 2: Ocean coastlines and lake shorelines 	+ 3: Shallow inland water 	+ 4: Ephemeral water 	+ 5: Deep inland water 	+ 6: Continental/moderate ocean 	+ 7: Deep ocean * Bits 6\-7: Aerosol quantity 	+ 0: Climatology 	+ 1: Low 	+ 2: Average 	+ 3: High * Bits 8\-9: Cirrus detected 	+ 0: None 	+ 1: Small 	+ 2: Average 	+ 3: High * Bit 10: Cloud shadow 	+ 0: No cloud 	+ 1: Cloud * Bit 11: Internal fire algorithm flag 	+ 0: No Fire 	+ 1: Fire * Bit 12: Snow/ice flag 	+ 0: No 	+ 1: Yes * Bit 13: Pixel is adjacent to cloud 	+ 0: No 	+ 1: Yes * Bit 14: BRDF correction performed 	+ 0: No 	+ 1: Yes * Bit 15: Internal snow flag 	+ 0: No snow 	+ 1: Snow | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


LP DAAC NASA data are freely accessible; however, when an author
publishes these data or works based on the data, it is requested that the
author cite the datasets within the text of the publication and include a
reference to them in the reference list.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)





### DOIs


* [https://doi.org/10\.5067/VIIRS/VNP09H1\.002](https://doi.org/10.5067/VIIRS/VNP09H1.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/VIIRS/002/VNP09H1')
.filter(ee.Filter.date('2017-05-01','2017-06-30'));
varrgb=dataset.select(['SurfReflect_I1','SurfReflect_I2','SurfReflect_I3']);
varrgbVis={
min:0.0,
max:1.0,
};
Map.setCenter(17.93,7.71,2);
Map.addLayer(rgb,rgbVis,'RGB');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP09H1)


[VNP09H1: VIIRS Surface Reflectance 8\-Day L3 Global 500m](/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP09H1)

The 8\-day Visible Infrared Imaging Radiometer Suite (VIIRS) Surface Reflectance (VNP09H1\) Version 1 composite product provides an estimate of land surface reflectance from the Suomi National Polar\-orbiting Partnership (Suomi NPP) VIIRS sensor for three imagery bands (I1, I2, I3\) at nominal 500m resolution (\~463m). The 500m dataset is derived through …

 NASA/VIIRS/002/VNP09H1,
 daily,nasa,noaa,npp,reflectance,satellite\-imagery,sr,viirs

2012\-01\-19T00:00:00Z/2025\-06\-18T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP09H1\.002](https://doi.org/https://doi.org/10.5067/VIIRS/VNP09H1.002)
* [https://doi.org/10\.5067/VIIRS/VNP09H1\.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP09H1)









