



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP46A2: VIIRS Lunar Gap\-Filled BRDF Nighttime Lights Daily L3 Global 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================================================








Dataset Availability
2012\-01\-19T00:00:00Z–2025\-07\-02T00:00:00Z
Dataset Provider


[NASA LAADS DAAC](https://doi.org/10.5067/VIIRS/VNP46A2.002)



Earth Engine Snippet


`ee.ImageCollection("NASA/VIIRS/002/VNP46A2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP46A2)





Cadence
1 Day
Tags


[brdf](/earth-engine/datasets/tags/brdf)
[daily](/earth-engine/datasets/tags/daily)
[nasa](/earth-engine/datasets/tags/nasa)
[nighttime](/earth-engine/datasets/tags/nighttime)
[noaa](/earth-engine/datasets/tags/noaa)
[population](/earth-engine/datasets/tags/population)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The Suomi National Polar\-orbiting Partnership (SNPP) Visible Infrared
Imaging Radiometer Suite (VIIRS) supports a Day\-Night Band (DNB) sensor that
provides global daily measurements of nocturnal visible and
near\-infrared(NIR) light that are suitable for Earth system science and
applications. The VIIRS DNB's ultra\-sensitivity in lowlight conditions
enable us to generate a new set of science\-quality nighttime products that
manifest substantial improvements in sensor resolution and calibration when
compared to the previous era of Defense Meteorological Satellite
Program/Operational Linescan System's (DMSP/OLS) nighttime lights image
products. Such improvements allow the VIIRS DNB products to better monitor
both the magnitude and signature of nighttime phenomena, and anthropogenic
sources of light emissions.


VNP46A2 is the short\-name for the daily moonlight\- and atmosphere\-corrected
Nighttime Lights (NTL) product called VIIRS/NPP Gap\-Filled Lunar
BRDF\-Adjusted Nighttime Lights Daily L3 Global 500m Linear Lat Lon Grid.


Documentation:


* [User's Guide](https://ladsweb.modaps.eosdis.nasa.gov/api/v2/content/archives/Document%20Archive/Science%20Data%20Product%20Documentation/VIIRS_Black_Marble_UG_v1.3_Sep_2022.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://ladsweb.modaps.eosdis.nasa.gov/api/v2/content/archives/Document%20Archive/Science%20Data%20Product%20Documentation/Product%20Generation%20Algorithms/VIIRS_Black_Marble_ATBD_v1.1_July_2020.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/missions-and-measurements/products/VNP46A2/)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `DNB_BRDF_Corrected_NTL` | 0 | 6553\.4 | BRDF corrected DNB NTL |
| `Gap_Filled_DNB_BRDF_Corrected_NTL` | 0 | 6553\.4 | Gap Filled BRDF corrected DNB NTL |
| `DNB_Lunar_Irradiance` | 0 | 6553\.4 | DNB Lunar Irradiance |
| `Latest_High_Quality_Retrieval` | Latest high quality BRDF corrected DNB radiance retrieval |
| `Mandatory_Quality_Flag` | 0 | 3 | Mandatory quality flag |
| `Snow_Flag` | 0 | 1 | Flag for snow cover |
| `QF_Cloud_Mask` | Quality flag for cloud mask |
| Bitmask for QF\_Cloud\_Mask * Bit 0: Day/Night 	+ 0: Night 	+ 1: Day * Bits 1\-3: Land/Water Background 	+ 0: Land \& Desert 	+ 1: Land no Desert 	+ 2: Inland Water 	+ 3: Sea Water 	+ 5: Coastal * Bits 4\-5: Cloud Mask Quality 	+ 0: Poor 	+ 1: Low 	+ 2: Medium 	+ 3: High * Bits 6\-7: Cloud Detection Results \& Confidence Indicator 	+ 0: Confident Clear 	+ 1: Probably Clear 	+ 2: Probably Cloudy 	+ 3: Confident Cloudy * Bit 8: Shadow Detected 	+ 0: No 	+ 1: Yes * Bit 9: Cirrus Detection (IR) (BTM15 \- BTM16\) 	+ 0: No cloud 	+ 1: Cloud * Bit 10: Snow/Ice Surface 	+ 0: No Snow/Ice 	+ 1: Snow/Ice | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


**Mandatory\_Quality\_Flag Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | High\-quality, Persistent nighttime lights |
| 1 | None | High\-quality, Ephemeral nighttime Lights |
| 2 | None | Poor\-quality, Outlier, potential cloud contamination, or other issues |
| 255 | None | No retrieval, Fill value (masked out on ingestion) |


**Snow\_Flag Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | No Snow/Ice |
| 1 | None | Snow/Ice |




### Terms of Use


**Terms of Use**


LP DAAC NASA data are freely accessible; however, when an author
publishes these data or works based on the data, it is requested that the
author cite the datasets within the text of the publication and include a
reference to them in the reference list.




### Citations



Citations:
* Román, M.O., Wang, Z., Sun, Q., Kalb, V., Miller, S.D., Molthan, A.,
Schultz, L., Bell, J., Stokes, E.C., Pandey, B. and Seto, K.C., et al.
(2018\). NASA's Black Marble nighttime lights product suite.
Remote Sensing of Environment 210, 113\-143\.
[10\.1016/j.rse.2018\.03\.017](https://doi.org/10.1016/j.rse.2018.03.017)





### DOIs


* [https://doi.org/10\.5067/VIIRS/VNP46A2\.002](https://doi.org/10.5067/VIIRS/VNP46A2.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/VIIRS/002/VNP46A2')
.filter(ee.Filter.date('2013-01-01','2013-03-01'));

varnighttime=dataset.select('Gap_Filled_DNB_BRDF_Corrected_NTL');
varnighttimeVis={min:0.0,max:1.0};

Map.setCenter(-77.1056,38.8904,3);
Map.addLayer(nighttime,nighttimeVis,'Nighttime');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP46A2)


[VNP46A2: VIIRS Lunar Gap\-Filled BRDF Nighttime Lights Daily L3 Global 500m](/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP46A2)

The Suomi National Polar\-orbiting Partnership (SNPP) Visible Infrared Imaging Radiometer Suite (VIIRS) supports a Day\-Night Band (DNB) sensor that provides global daily measurements of nocturnal visible and near\-infrared(NIR) light that are suitable for Earth system science and applications. The VIIRS DNB's ultra\-sensitivity in lowlight conditions enable us to generate a …

 NASA/VIIRS/002/VNP46A2,
 brdf,daily,nasa,nighttime,noaa,population,viirs

2012\-01\-19T00:00:00Z/2025\-07\-02T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP46A2\.002](https://doi.org/https://doi.org/10.5067/VIIRS/VNP46A2.002)
* [https://doi.org/10\.5067/VIIRS/VNP46A2\.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP46A2)









