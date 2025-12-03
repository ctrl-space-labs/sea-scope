



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD21C2\.061 Terra Land Surface Temperature and 3\-Band Emissivity 8\-Day L3 Global 0\.05 Deg CMG


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-04T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MOD21C2.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MOD21C2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD21C2)





Cadence
8 Days
Tags


[climate](/earth-engine/datasets/tags/climate)
[emissivity](/earth-engine/datasets/tags/emissivity)
[global](/earth-engine/datasets/tags/global)
[lst](/earth-engine/datasets/tags/lst)
[nasa](/earth-engine/datasets/tags/nasa)
[surface\-temperature](/earth-engine/datasets/tags/surface-temperature)
[terra](/earth-engine/datasets/tags/terra)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The MOD21C2 dataset is an 8\-day composite LST product that uses an algorithm
based on a simple averaging method. The algorithm calculates the average
from all the cloud free MOD21A1D and MOD21A1N daily acquisitions from the
8\-day period. Unlike the MOD21A1 data sets where the daytime and nighttime
acquisitions are separate products, the MOD21A2 contains both daytime and
nighttime acquisitions. The LST, Quality Control (QC), view zenith angle,
and viewing time have separate day and night bands, while the values for the
MODIS emissivity bands 29, 31, and 32 are the average of both the nighttime
and daytime acquisitions.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/1398/MOD21_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/1399/MOD21_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MOD21C2)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Scale | Offset | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `Count_Day` | None | 1 | 65535 |  |  | Count of Daytime Input Values |
| `Count_Night` | None | 1 | 65535 |  |  | Count of Nighttime Input Values |
| `QC_Day` | None |  |  | Quality Control for Daytime LST and Emissivity |
| Bitmask for QC\_Day * Bits 0\-1: Mandatory QA flags 	+ 0: Pixel produced, good quality, no further QA info necessary 	+ 1: Pixel produced, nominal quality. Recommend more detailed analysis of other QC information 	+ 2: Pixel not produced due to cloud 	+ 3: Pixel not produced due to reasons other than cloud * Bits 2\-3: Data quality flag 	+ 0: Good data quality of L1B bands 29, 31, 32 	+ 1: Missing pixel 	+ 2: Fairly calibrated 	+ 3: Poorly calibrated, TES processing skipped * Bits 4\-5: Emissivity accuracy 	+ 0:  	0\.02 (Poor performance) 	+ 1: 0\.015 \- 0\.02 (Marginal performance) 	+ 2: 0\.01 \- 0\.015 (Good performance) 	+ 3: \<0\.01 (Excellent performance) * Bits 6\-7: LST accuracy 	+ 0:  	2K (Poor performance) 	+ 1: 1\.5 \- 2K (Marginal performance) 	+ 2: 1 \- 1\.5K (Good performance) 	+ 3: \<1K (Excellent performance) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `QC_Night` | None |  |  | Quality Control for Nighttime LST and Emissivity |
| Bitmask for QC\_Night * Bits 0\-1: Mandatory QA flags 	+ 0: Pixel produced, good quality, no further QA info necessary 	+ 1: Pixel produced, nominal quality. Recommend more detailed analysis of other QC information 	+ 2: Pixel not produced due to cloud 	+ 3: Pixel not produced due to reasons other than cloud * Bits 2\-3: Data quality flag 	+ 0: Good data quality of L1B bands 29, 31, 32 	+ 1: Missing pixel 	+ 2: Fairly calibrated 	+ 3: Poorly calibrated, TES processing skipped * Bits 4\-5: Emissivity accuracy 	+ 0:  	0\.02 (Poor performance) 	+ 1: 0\.015 \- 0\.02 (Marginal performance) 	+ 2: 0\.01 \- 0\.015 (Good performance) 	+ 3: \<0\.01 (Excellent performance) * Bits 6\-7: LST accuracy 	+ 0:  	2K (Poor performance) 	+ 1: 1\.5 \- 2K (Marginal performance) 	+ 2: 1 \- 1\.5K (Good performance) 	+ 3: \<1K (Excellent performance) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `LST_Day` | K | 7500 | 65535 | 0\.02 |  | Average Daytime Land Surface Temperature |
| `LST_Night` | K | 7500 | 65535 | 0\.02 |  | Average Nighttime Land Surface Temperature |
| `LST_Day_err` | K | 1 | 255 | 0\.04 |  | Root\-mean\-square\-error Daytime Land Surface Temperature |
| `LST_Night_err` | K | 1 | 255 | 0\.04 |  | Average Nighttime Land Surface Temperature |
| `Day_view_angle` | deg | 0 | 130 |  | \-65 | Average Daytime View Zenith Angle |
| `Night_view_angle` | deg | 0 | 130 |  | \-65 | Average Nighttime View Zenith Angle |
| `Day_view_time` | h | 0 | 120 | 0\.2 |  | Average Daytime View Time (UTC) |
| `Night_view_time` | h | 0 | 120 | 0\.2 |  | Average Nighttime View Time (UTC) |
| `Emis_29_Day` | None | 1 | 255 | 0\.002 | 0\.49 | Average Daytime Band 29 Emissivity |
| `Emis_29_Night` | None | 1 | 255 | 0\.002 | 0\.49 | Average Nighttime Band 29 Emissivity |
| `Emis_29_Day_err` | None | 1 | 65535 | 0\.0001 |  | Root\-mean\-square\-error Daytime Band 29 Emissivity |
| `Emis_29_Night_err` | None | 1 | 65535 | 0\.0001 |  | Root\-mean\-square\-error Nighttime Band 29 Emissivity |
| `Emis_31_Day` | None | 1 | 255 | 0\.002 | 0\.49 | Average Daytime Band 31 Emissivity |
| `Emis_31_Night` | None | 1 | 255 | 0\.002 | 0\.49 | Average Nighttime Band 31 Emissivity |
| `Emis_31_Day_err` | None | 1 | 65535 | 0\.0001 |  | Root\-mean\-square\-error Daytime Band 31 Emissivity |
| `Emis_31_Night_err` | None | 1 | 65535 | 0\.0001 |  | Root\-mean\-square\-error Nighttime Band 31 Emissivity |
| `Emis_32_Day` | None | 1 | 255 | 0\.002 | 0\.49 | Average Daytime Band 32 Emissivity |
| `Emis_32_Night` | None | 1 | 255 | 0\.002 | 0\.49 | Average Nighttime Band 32 Emissivity |
| `Emis_32_Day_err` | None | 1 | 65535 | 0\.0001 |  | Root\-mean\-square\-error Daytime Band 32 Emissivity |
| `Emis_32_Night_err` | None | 1 | 65535 | 0\.0001 |  | Root\-mean\-square\-error Nighttime Band 32 Emissivity |
| `View_Angle` | deg |  | \-65 | MODIS view zenith angle |
| `Percent_land_in_grid` | % | 1 | 100 |  |  | Percent of Land Detections in Grid Cell |
| `Clear_sky_days` | None | 0 | 2\.14748e\+09 |  |  | Bitmap of Clear Sky Days (1 \= clear, LSB \= 1st day) |
| `Clear_sky_nights` | None | 0 | 2\.14748e\+09 |  |  | Bitmap of Clear Sky Nights (1 \= clear, LSB \= 1st day) |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MOD21C2\.061](https://doi.org/10.5067/MODIS/MOD21C2.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MOD21C2')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varlandSurfaceTemperature=dataset.select('LST_Day');
varlandSurfaceTemperatureVis={
min:216.0,
max:348.0,
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
'Average Daytime Land Surface Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD21C2)


[MOD21C2\.061 Terra Land Surface Temperature and 3\-Band Emissivity 8\-Day L3 Global 0\.05 Deg CMG](/earth-engine/datasets/catalog/MODIS_061_MOD21C2)

The MOD21C2 dataset is an 8\-day composite LST product that uses an algorithm based on a simple averaging method. The algorithm calculates the average from all the cloud free MOD21A1D and MOD21A1N daily acquisitions from the 8\-day period. Unlike the MOD21A1 data sets where the daytime and nighttime acquisitions are …

 MODIS/061/MOD21C2,
 climate,emissivity,global,lst,nasa,surface\-temperature,terra,usgs

2000\-02\-24T00:00:00Z/2025\-07\-04T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MOD21C2\.061](https://doi.org/https://doi.org/10.5067/MODIS/MOD21C2.061)
* [https://doi.org/10\.5067/MODIS/MOD21C2\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD21C2)









