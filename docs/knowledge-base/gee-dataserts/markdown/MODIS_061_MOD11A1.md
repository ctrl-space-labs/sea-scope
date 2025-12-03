



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD11A1\.061 Terra Land Surface Temperature and Emissivity Daily Global 1km


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-12T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MOD11A1.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MOD11A1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD11A1)





Cadence
1 Day
Tags


[climate](/earth-engine/datasets/tags/climate)
[daily](/earth-engine/datasets/tags/daily)
[emissivity](/earth-engine/datasets/tags/emissivity)
[global](/earth-engine/datasets/tags/global)
[lst](/earth-engine/datasets/tags/lst)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[surface\-temperature](/earth-engine/datasets/tags/surface-temperature)
[terra](/earth-engine/datasets/tags/terra)
[usgs](/earth-engine/datasets/tags/usgs)
mod11a1








#### Description



The MOD11A1 V6\.1 product provides daily land surface temperature
(LST) and emissivity values in a 1200 x 1200 kilometer grid. The
temperature value is derived from the MOD11\_L2 swath product. Above
30 degrees latitude, some pixels may have multiple observations
where the criteria for clear\-sky are met. When this occurs, the
pixel value is the average of all qualifying observations. Provided
along with both the day\-time and night\-time surface temperature
bands and their quality indicator layers are MODIS bands 31 and
32 and six observation layers.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/118/MOD11_User_Guide_V6.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/119/MOD11_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MOD11A1)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Scale | Offset | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `LST_Day_1km` | K | 7500 | 65535 | 0\.02 |  | Daytime Land Surface Temperature |
| `QC_Day` | None |  |  | Daytime LST Quality Indicators |
| Bitmask for QC\_Day * Bits 0\-1: Mandatory QA flags 	+ 0: LST produced, good quality, not necessary to examine more detailed QA 	+ 1: LST produced, other quality, recommend examination of more detailed QA 	+ 2: LST not produced due to cloud effects 	+ 3: LST not produced primarily due to reasons other than cloud * Bits 2\-3: Data quality flag 	+ 0: Good data quality 	+ 1: Other quality data 	+ 2: TBD 	+ 3: TBD * Bits 4\-5: Emissivity error flag 	+ 0: Average emissivity error \<\= 0\.01 	+ 1: Average emissivity error \<\= 0\.02 	+ 2: Average emissivity error \<\= 0\.04 	+ 3: Average emissivity error \> 0\.04 * Bits 6\-7: LST error flag 	+ 0: Average LST error \<\= 1K 	+ 1: Average LST error \<\= 2K 	+ 2: Average LST error \<\= 3K 	+ 3: Average LST error \> 3K | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `Day_view_time` | h | 0 | 240 | 0\.1 |  | Local time of day observation |
| `Day_view_angle` | deg | 0 | 130 |  | \-65 | View zenith angle of day observation |
| `LST_Night_1km` | K | 7500 | 65535 | 0\.02 |  | Nighttime Land Surface Temperature |
| `QC_Night` | None |  |  | Nighttime LST Quality indicators |
| Bitmask for QC\_Night * Bits 0\-1: Mandatory QA flags 	+ 0: LST produced, good quality, not necessary to examine more detailed QA 	+ 1: LST produced, other quality, recommend examination of more detailed QA 	+ 2: LST not produced due to cloud effects 	+ 3: LST not produced primarily due to reasons other than cloud * Bits 2\-3: Data quality flag 	+ 0: Good data quality 	+ 1: Other quality data 	+ 2: TBD 	+ 3: TBD * Bits 4\-5: Emissivity error flag 	+ 0: Average emissivity error \<\= 0\.01 	+ 1: Average emissivity error \<\= 0\.02 	+ 2: Average emissivity error \<\= 0\.04 	+ 3: Average emissivity error \> 0\.04 * Bits 6\-7: LST error flag 	+ 0: Average LST error \<\= 1K 	+ 1: Average LST error \<\= 2K 	+ 2: Average LST error \<\= 3K 	+ 3: Average LST error \> 3K | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `Night_view_time` | h | 0 | 240 | 0\.1 |  | Local time of night observation |
| `Night_view_angle` | deg | 0 | 130 |  | \-65 | View zenith angle of night observation |
| `Emis_31` | None | 1 | 255 | 0\.002 | 0\.49 | Band 31 emissivity |
| `Emis_32` | None | 1 | 255 | 0\.002 | 0\.49 | Band 32 emissivity |
| `Clear_day_cov` | None | 1 | 65535 | 0\.0005 |  | Day clear\-sky coverage |
| `Clear_night_cov` | None | 1 | 65535 | 0\.0005 |  | Night clear\-sky coverage |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MOD11A1\.061](https://doi.org/10.5067/MODIS/MOD11A1.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MOD11A1')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varlandSurfaceTemperature=dataset.select('LST_Day_1km');
varlandSurfaceTemperatureVis={
min:13000.0,
max:16500.0,
palette:[
'040274','040281','0502a3','0502b8','0502ce','0502e6',
'0602ff','235cb1','307ef3','269db1','30c8e2','32d3ef',
'3be285','3ff38f','86e26f','3ae237','b5e22e','d6e21f',
'fff705','ffd611','ffb613','ff8b13','ff6e08','ff500d',
'ff0000','de0101','c21301','a71001','911003'
],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(
landSurfaceTemperature,landSurfaceTemperatureVis,
'Land Surface Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD11A1)


[MOD11A1\.061 Terra Land Surface Temperature and Emissivity Daily Global 1km](/earth-engine/datasets/catalog/MODIS_061_MOD11A1)

The MOD11A1 V6\.1 product provides daily land surface temperature (LST) and emissivity values in a 1200 x 1200 kilometer grid. The temperature value is derived from the MOD11\_L2 swath product. Above 30 degrees latitude, some pixels may have multiple observations where the criteria for clear\-sky are met. When this occurs, …

 MODIS/061/MOD11A1,
 climate,daily,emissivity,global,lst,modis,nasa,surface\-temperature,terra,usgs

2000\-02\-24T00:00:00Z/2025\-07\-12T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MOD11A1\.061](https://doi.org/https://doi.org/10.5067/MODIS/MOD11A1.061)
* [https://doi.org/10\.5067/MODIS/MOD11A1\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD11A1)









