



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MYD13C1\.061: Aqua Vegetation Indices 16\-Day L3 Global 0\.05 Deg CMG


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================================================








Dataset Availability
2002\-07\-04T00:00:00Z–2025\-06\-18T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MYD13C1.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MYD13C1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD13C1)





Cadence
16 Days
Tags


[16\-day](/earth-engine/datasets/tags/16-day)
[aqua](/earth-engine/datasets/tags/aqua)
[global](/earth-engine/datasets/tags/global)
[nasa](/earth-engine/datasets/tags/nasa)
[usgs](/earth-engine/datasets/tags/usgs)
[vegetation](/earth-engine/datasets/tags/vegetation)
[vegetation\-indices](/earth-engine/datasets/tags/vegetation-indices)








#### Description



The Aqua Moderate Resolution Imaging Spectroradiometer (MODIS) Vegetation Indices 16\-Day (MYD13C1\) Version 6\.1 product provides a Vegetation Index (VI) value at a per pixel basis. There are two primary vegetation layers. The first is the Normalized Difference Vegetation Index (NDVI), which maintains continuity with the existing National Oceanic and Atmospheric Administration\-Advanced Very High Resolution Radiometer (NOAA\-AVHRR) derived NDVI. The second vegetation layer is the Enhanced Vegetation Index (EVI), which has improved sensitivity over high biomass regions.
The Climate Modeling Grid (CMG) consists of 3,600 rows and 7,200 columns of 5,600 meter (m) pixels. Global MYD13C1 data are cloud\-free spatial composites of the gridded 16\-day 1 kilometer MYD13A2 data, and are provided as a Level 3 product projected on a 0\.05 degree (5,600 m) geographic CMG. The MYD13C1 has data fields for NDVI, EVI, VI QA, reflectance data, angular information, and spatial statistics such as mean, standard deviation, and number of used input pixels at the 0\.05 degree CMG resolution. 





### Bands



**Pixel Size**
  
5600 meters



**Bands**




| Name | Units | Min | Max | Wavelength | Description |
| --- | --- | --- | --- | --- | --- |
| `NDVI` | None | \-0\.2 | 1 | None | 16\-day NDVI average |
| `EVI` | None | \-0\.2 | 1 | None | 16\-day EVI average |
| `DetailedQA` | None | None | VI Quality indicators |
| Bitmask for DetailedQA * Bits 0\-1: VI quality (MODLAND QA Bits) 	+ 0: VI produced with good quality 	+ 1: VI produced, but check other QA 	+ 2: Pixel produced, but most probably cloudy 	+ 3: Pixel not produced due to other reasons than clouds * Bits 2\-5: VI usefulness 	+ 0: Highest quality 	+ 1: Lower quality 	+ 2: Decreasing quality 	+ 4: Decreasing quality 	+ 8: Decreasing quality 	+ 9: Decreasing quality 	+ 10: Decreasing quality 	+ 12: Lowest quality 	+ 13: Quality so low that it is not useful 	+ 14: L1B data faulty 	+ 15: Not useful for any other reason/not processed * Bits 6\-7: Aerosol Quantity 	+ 0: Climatology 	+ 1: Low 	+ 2: Intermediate 	+ 3: High * Bit 8: Adjacent cloud detected 	+ 0: No 	+ 1: Yes * Bit 9: Atmosphere BRDF correction 	+ 0: No 	+ 1: Yes * Bit 10: Mixed Clouds 	+ 0: No 	+ 1: Yes * Bits 11\-13: Land/water mask 	+ 0: Shallow ocean 	+ 1: Land (nothing else but land) 	+ 2: Ocean coastlines and lake shorelines 	+ 3: Shallow inland water 	+ 4: Ephemeral water 	+ 5: Deep inland water 	+ 6: Moderate or continental ocean 	+ 7: Deep ocean * Bit 14: Possible snow/ice 	+ 0: No 	+ 1: Yes * Bit 15: Possible shadow 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `sur_refl_b01` | None | 0 | 1 | 620\-670nm | Surface reflectance band 1 (red) |
| `sur_refl_b02` | None | 0 | 1 | 841\-876nm | Surface reflectance band 2 (near\-infrared) |
| `sur_refl_b03` | None | 0 | 1 | 459\-479nm | Surface reflectance band 3 (blue) |
| `sur_refl_b07` | None | 0 | 1 | 2105\-2155nm | Surface reflectance band 7 (mid\-infrared) |
| `SolarZenith` | deg | 0 | 180 | None | View zenith angle of VI Pixel |
| `NDVIStdDev` | None | \-0\.2 | 1 | None | Standard deviation computed from input NDVI pixels |
| `EVIStdDev` | None | \-0\.2 | 1 | None | Standard deviation computed from input NDVI pixels |
| `Pixel_1km` | count | 0 | 36 | None | Number of 1 km input pixels used |
| `Pixel_30deg_1km` | count | 0 | 36 | None | Number of 1 km input pixels used with VZ angle less than \+ or \- 30 degs |
| `SummaryQA` | None | None | Quality reliability of VI pixel |


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


* [https://doi.org/10\.5067/MODIS/MYD13C1\.061](https://doi.org/10.5067/MODIS/MYD13C1.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MYD13C1')
.filter(ee.Filter.date('2023-01-01','2023-05-01'));
varndvi=dataset.select('NDVI');
varndviVis={
min:0,
max:.9,
palette:[
'ffffff','ce7e45','df923d','f1b555','fcd163','99b718','74a901',
'66a000','529400','3e8601','207401','056201','004c00','023b01',
'012e01','011d01','011301'
],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(ndvi,ndviVis,'NDVI');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD13C1)


[MYD13C1\.061: Aqua Vegetation Indices 16\-Day L3 Global 0\.05 Deg CMG](/earth-engine/datasets/catalog/MODIS_061_MYD13C1)

The Aqua Moderate Resolution Imaging Spectroradiometer (MODIS) Vegetation Indices 16\-Day (MYD13C1\) Version 6\.1 product provides a Vegetation Index (VI) value at a per pixel basis. There are two primary vegetation layers. The first is the Normalized Difference Vegetation Index (NDVI), which maintains continuity with the existing National Oceanic and Atmospheric …

 MODIS/061/MYD13C1,
 16\-day,aqua,global,nasa,usgs,vegetation,vegetation\-indices

2002\-07\-04T00:00:00Z/2025\-06\-18T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MYD13C1\.061](https://doi.org/https://doi.org/10.5067/MODIS/MYD13C1.061)
* [https://doi.org/10\.5067/MODIS/MYD13C1\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MYD13C1)









