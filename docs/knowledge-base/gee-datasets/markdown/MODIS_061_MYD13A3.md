



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MYD13A3\.061 Aqua Vegetation Indices Monthly L3 Global 1 km SIN Grid


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================================








Dataset Availability
2002\-07\-01T00:00:00Z–2025\-06\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MYD13A3.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MYD13A3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD13A3)





Cadence
1 Month
Tags


[aqua](/earth-engine/datasets/tags/aqua)
[evi](/earth-engine/datasets/tags/evi)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[monthly](/earth-engine/datasets/tags/monthly)
[nasa](/earth-engine/datasets/tags/nasa)
[ndvi](/earth-engine/datasets/tags/ndvi)
[usgs](/earth-engine/datasets/tags/usgs)
[vegetation](/earth-engine/datasets/tags/vegetation)
[vegetation\-indices](/earth-engine/datasets/tags/vegetation-indices)








#### Description



The Aqua Moderate Resolution Imaging Spectroradiometer (MODIS) Vegetation
Indices (MYD13A3\) Version 6\.1 data are provided monthly at 1 kilometer (km)
spatial resolution as a gridded Level 3 product in the sinusoidal
projection. In generating this monthly product, the algorithm ingests all
the MYD13A2 products that overlap the month and employs a weighted temporal
average.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/621/MOD13_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/104/MOD13_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MYD13A3)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Scale | Wavelength | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `NDVI` | None | \-2000 | 10000 | 0\.0001 | None | Monthly NDVI average |
| `EVI` | None | \-2000 | 10000 | 0\.0001 | None | Monthly EVI average |
| `DetailedQA` | None |  | None | VI Quality indicators |
| Bitmask for DetailedQA * Bits 0\-1: VI quality (MODLAND QA Bits) 	+ 0: VI produced with good quality 	+ 1: VI produced, but check other QA 	+ 2: Pixel produced, but most probably cloudy 	+ 3: Pixel not produced due to other reasons than clouds * Bits 2\-5: VI usefulness 	+ 0: Highest quality 	+ 1: Lower quality 	+ 2: Decreasing quality 	+ 4: Decreasing quality 	+ 8: Decreasing quality 	+ 9: Decreasing quality 	+ 10: Decreasing quality 	+ 12: Lowest quality 	+ 13: Quality so low that it is not useful 	+ 14: L1B data faulty 	+ 15: Not useful for any other reason/not processed * Bits 6\-7: Aerosol Quantity 	+ 0: Climatology 	+ 1: Low 	+ 2: Intermediate 	+ 3: High * Bit 8: Adjacent cloud detected 	+ 0: No 	+ 1: Yes * Bit 9: Atmosphere BRDF correction 	+ 0: No 	+ 1: Yes * Bit 10: Mixed Clouds 	+ 0: No 	+ 1: Yes * Bits 11\-13: Land/water mask 	+ 0: Shallow ocean 	+ 1: Land (nothing else but land) 	+ 2: Ocean coastlines and lake shorelines 	+ 3: Shallow inland water 	+ 4: Ephemeral water 	+ 5: Deep inland water 	+ 6: Moderate or continental ocean 	+ 7: Deep ocean * Bit 14: Possible snow/ice 	+ 0: No 	+ 1: Yes * Bit 15: Possible shadow 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `sur_refl_b01` | None | 0 | 10000 | 0\.0001 | 620\-670nm | Surface reflectance band 1 (red) |
| `sur_refl_b02` | None | 0 | 10000 | 0\.0001 | 841\-876nm | Surface reflectance band 2 (near\-infrared) |
| `sur_refl_b03` | None | 0 | 10000 | 0\.0001 | 459\-479nm | Surface reflectance band 3 (blue) |
| `sur_refl_b07` | None | 0 | 10000 | 0\.0001 | 2105\-2155nm | Surface reflectance band 7 (mid\-infrared) |
| `ViewZenith` | deg | 0 | 18000 | 0\.01 | None | View zenith angle of VI Pixel |
| `SolarZenith` | deg | 0 | 18000 | 0\.01 | None | Sun zenith angle of VI pixel |
| `RelativeAzimuth` | deg | \-18000 | 18000 | 0\.01 | None | Relative azimuth angle of VI pixel |
| `SummaryQA` | None |  | None | Quality reliability of VI pixel |


**SummaryQA Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | Good Data: use with confidence |
| 1 | None | Marginal Data: useful, but look at other QA information |
| 2 | None | Snow/Ice: target covered with snow/ice |
| 3 | None | Cloudy: target not visible, covered with cloud |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MYD13A3\.061](https://doi.org/10.5067/MODIS/MYD13A3.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MYD13A3')
.filter(ee.Filter.date('2020-01-01','2023-05-01'));
varndvi=dataset.select('NDVI');
varndviVis={
min:0,
max:9000,
palette:[
'ffffff','ce7e45','df923d','f1b555','fcd163','99b718','74a901',
'66a000','529400','3e8601','207401','056201','004c00','023b01',
'012e01','011d01','011301'
],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(ndvi,ndviVis,'NDVI');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD13A3)


[MYD13A3\.061 Aqua Vegetation Indices Monthly L3 Global 1 km SIN Grid](/earth-engine/datasets/catalog/MODIS_061_MYD13A3)

The Aqua Moderate Resolution Imaging Spectroradiometer (MODIS) Vegetation Indices (MYD13A3\) Version 6\.1 data are provided monthly at 1 kilometer (km) spatial resolution as a gridded Level 3 product in the sinusoidal projection. In generating this monthly product, the algorithm ingests all the MYD13A2 products that overlap the month and employs …

 MODIS/061/MYD13A3,
 aqua,evi,global,modis,monthly,nasa,ndvi,usgs,vegetation,vegetation\-indices

2002\-07\-01T00:00:00Z/2025\-06\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MYD13A3\.061](https://doi.org/https://doi.org/10.5067/MODIS/MYD13A3.061)
* [https://doi.org/10\.5067/MODIS/MYD13A3\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MYD13A3)









