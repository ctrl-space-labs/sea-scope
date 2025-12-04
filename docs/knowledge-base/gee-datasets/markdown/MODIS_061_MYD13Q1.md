



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MYD13Q1\.061 Aqua Vegetation Indices 16\-Day Global 250m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================================








Dataset Availability
2002\-07\-04T00:00:00Z–2025\-06\-18T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MYD13Q1.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MYD13Q1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD13Q1)





Cadence
16 Days
Tags


[16\-day](/earth-engine/datasets/tags/16-day)
[aqua](/earth-engine/datasets/tags/aqua)
[evi](/earth-engine/datasets/tags/evi)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[ndvi](/earth-engine/datasets/tags/ndvi)
[usgs](/earth-engine/datasets/tags/usgs)
[vegetation](/earth-engine/datasets/tags/vegetation)
[vegetation\-indices](/earth-engine/datasets/tags/vegetation-indices)
myd13q1








#### Description



The MYD13Q1 V6\.1 product provides a Vegetation Index (VI)
value at a per pixel basis. There are two primary vegetation layers.
The first is the Normalized Difference Vegetation Index (NDVI)
which is referred to as the continuity index to the existing National
Oceanic and Atmospheric Administration\-Advanced Very High Resolution
Radiometer (NOAA\-AVHRR) derived NDVI. The second vegetation layer
is the Enhanced Vegetation Index (EVI) that minimizes canopy background
variations and maintains sensitivity over dense vegetation conditions.
The EVI also uses the blue band to remove residual atmosphere contamination
caused by smoke and sub\-pixel thin cloud clouds. The MODIS NDVI
and EVI products are computed from atmospherically corrected bi\-directional
surface reflectances that have been masked for water, clouds, heavy
aerosols, and cloud shadows.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/103/MOD13_User_Guide_V6.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/104/MOD13_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MOD13A2)





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Units | Min | Max | Scale | Wavelength | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `NDVI` | None | \-2000 | 10000 | 0\.0001 | None | Normalized Difference Vegetation Index |
| `EVI` | None | \-2000 | 10000 | 0\.0001 | None | Enhanced Vegetation Index |
| `DetailedQA` | None |  | None | VI quality indicators |
| Bitmask for DetailedQA * Bits 0\-1: VI quality (MODLAND QA Bits) 	+ 0: VI produced with good quality 	+ 1: VI produced, but check other QA 	+ 2: Pixel produced, but most probably cloudy 	+ 3: Pixel not produced due to other reasons than clouds * Bits 2\-5: VI usefulness 	+ 0: Highest quality 	+ 1: Lower quality 	+ 2: Decreasing quality 	+ 4: Decreasing quality 	+ 8: Decreasing quality 	+ 9: Decreasing quality 	+ 10: Decreasing quality 	+ 12: Lowest quality 	+ 13: Quality so low that it is not useful 	+ 14: L1B data faulty 	+ 15: Not useful for any other reason/not processed * Bits 6\-7: Aerosol Quantity 	+ 0: Climatology 	+ 1: Low 	+ 2: Intermediate 	+ 3: High * Bit 8: Adjacent cloud detected 	+ 0: No 	+ 1: Yes * Bit 9: Atmosphere BRDF correction 	+ 0: No 	+ 1: Yes * Bit 10: Mixed Clouds 	+ 0: No 	+ 1: Yes * Bits 11\-13: Land/water mask 	+ 0: Shallow ocean 	+ 1: Land (nothing else but land) 	+ 2: Ocean coastlines and lake shorelines 	+ 3: Shallow inland water 	+ 4: Ephemeral water 	+ 5: Deep inland water 	+ 6: Moderate or continental ocean 	+ 7: Deep ocean * Bit 14: Possible snow/ice 	+ 0: No 	+ 1: Yes * Bit 15: Possible shadow 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `sur_refl_b01` | None | 0 | 10000 | 0\.0001 | 645nm | Red surface reflectance |
| `sur_refl_b02` | None | 0 | 10000 | 0\.0001 | 858nm | NIR surface reflectance |
| `sur_refl_b03` | None | 0 | 10000 | 0\.0001 | 469nm | Blue surface reflectance |
| `sur_refl_b07` | None | 0 | 10000 | 0\.0001 | 2130nm/2105 \- 2155nm | MIR surface reflectance |
| `ViewZenith` | deg | 0 | 18000 | 0\.01 | None | View zenith angle |
| `SolarZenith` | deg | 0 | 18000 | 0\.01 | None | Solar zenith angle |
| `RelativeAzimuth` | deg | \-18000 | 18000 | 0\.01 | None | Relative azimuth angle |
| `DayOfYear` | None | 1 | 366 |  | None | Julian day of year |
| `SummaryQA` | None |  | None | Quality reliability of VI pixel |
| Bitmask for SummaryQA * Bits 0\-1: VI quality (MODLAND QA Bits) 	+ 0: Good data, use with confidence 	+ 1: Marginal data, useful but look at detailed QA for more information 	+ 2: Pixel covered with snow/ice 	+ 3: Pixel is cloudy | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MYD13Q1\.061](https://doi.org/10.5067/MODIS/MYD13Q1.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MYD13Q1')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varndvi=dataset.select('NDVI');
varndviVis={
min:0,
max:8000,
palette:[
'ffffff','ce7e45','df923d','f1b555','fcd163','99b718','74a901',
'66a000','529400','3e8601','207401','056201','004c00','023b01',
'012e01','011d01','011301'
],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(ndvi,ndviVis,'NDVI');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD13Q1)


[MYD13Q1\.061 Aqua Vegetation Indices 16\-Day Global 250m](/earth-engine/datasets/catalog/MODIS_061_MYD13Q1)

The MYD13Q1 V6\.1 product provides a Vegetation Index (VI) value at a per pixel basis. There are two primary vegetation layers. The first is the Normalized Difference Vegetation Index (NDVI) which is referred to as the continuity index to the existing National Oceanic and Atmospheric Administration\-Advanced Very High Resolution Radiometer …

 MODIS/061/MYD13Q1,
 16\-day,aqua,evi,global,modis,nasa,ndvi,usgs,vegetation,vegetation\-indices

2002\-07\-04T00:00:00Z/2025\-06\-18T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MYD13Q1\.061](https://doi.org/https://doi.org/10.5067/MODIS/MYD13Q1.061)
* [https://doi.org/10\.5067/MODIS/MYD13Q1\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MYD13Q1)









