



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD21A1D.061 Terra Land Surface Temperature and 3\-Band Emissivity Daily Global 1km


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-16T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MOD21A1D.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MOD21A1D")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD21A1D)





Cadence
1 Day
Tags


[climate](/earth-engine/datasets/tags/climate)
[daily](/earth-engine/datasets/tags/daily)
[emissivity](/earth-engine/datasets/tags/emissivity)
[global](/earth-engine/datasets/tags/global)
[lst](/earth-engine/datasets/tags/lst)
[nasa](/earth-engine/datasets/tags/nasa)
[surface\-temperature](/earth-engine/datasets/tags/surface-temperature)
[terra](/earth-engine/datasets/tags/terra)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The MOD21A1D dataset is produced daily from daytime Level 2 Gridded (L2G)
intermediate LST products at a spatial resolution of 1,000 meters. The L2G
process maps the daily MOD21 swath granules onto a sinusoidal MODIS grid and
stores all observations falling over a gridded cell for a given day. The
MOD21A1 algorithm sorts through these observations for each cell and
estimates the final LST value as an average from all observations that are
cloud free and have good LST\&E accuracies. The daytime average is weighted
by the observation coverage for that cell. Only observations having an
observation coverage greater than a 15% threshold are considered. The
MOD21A1D product contains the calculated LST as well as quality control, the
three emissivity bands, view zenith angle, and time of observation.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/1398/MOD21_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/1399/MOD21_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MOD21A1D)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `LST_1KM` | K | 7500 | 65535 | Land Surface Temperature |
| `QC` | None | Quality Control |
| Bitmask for QC * Bits 0\-1: Mandatory QA flags 	+ 0: Pixel produced, good quality, no further QA info necessary 	+ 1: Pixel produced, nominal quality. 	+ 2: Pixel not produced due to cloud 	+ 3: Pixel not produced due to reasons other than cloud * Bits 2\-3: Data quality flag 	+ 0: Good data quality of L1B bands 29, 31, 32 	+ 1: Missing pixel 	+ 2: Fairly calibrated 	+ 3: Poorly calibrated, TES processing skipped * Bits 4\-5: Cloud Flag 	+ 0: Cloud free 	+ 1: Thin cirrus 	+ 2: Pixel within 2 pixels of nearest cloud 	+ 3: Cloudy pixel * Bits 6\-7: TES Iterations 	+ 0:  	\=7 (Slow convergence) 	+ 1: 6 (Nominal) 	+ 2: 5 (Nominal) 	+ 3: \<5 (Fast) * Bits 8\-9: Atmospheric Opacity 	+ 0:  	\=3 (Warm, humid air; or cold land) 	+ 1: 0\.2 \- 0\.3 (Nominal value) 	+ 2: 0\.1 \- 0\.2 (Nominal value) 	+ 3: \<0\.1 (Dry, or high altitude pixel) * Bits 10\-11: Min\-Max Difference(MMD). Difference between minimum and maximum emissivity for bands 29, 31, 32 	+ 0: 0\.15 (Most silicate rocks) 	+ 1: 0\.1 \- 0\.15 (Rocks, sand, some soils) 	+ 2: 0\.03 \- 0\.1 (Mostly soils, mixed pixel) 	+ 3: \<0\.03 (Vegetation, snow, water, ice) * Bits 12\-13: Emissivity accuracy 	+ 0:  	0\.02 (Poor performance) 	+ 1: 0\.015 \- 0\.02 (Marginal performance) 	+ 2: 0\.01 \- 0\.015 (Good performance) 	+ 3: \<0\.01 (Excellent performance) * Bits 14\-15: LST accuracy 	+ 0:  	2 K (Poor performance) 	+ 1: 1\.5 \- 2 K (Marginal performance) 	+ 2: 1 \- 1\.5 K (Good performance) 	+ 3: \<1 K (Excellent performance) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `Emis_29` | None | 0 | 255 | Band 29 emissivity |
| `Emis_31` | None | 1 | 255 | Band 31 emissivity |
| `Emis_32` | None | 1 | 255 | Band 32 emissivity |
| `View_Angle` | deg | 0 | 130 | MODIS view zenith angle |
| `View_Time` | h | 0 | 240 | Time of MODIS observation |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MOD21A1D.061](https://doi.org/10.5067/MODIS/MOD21A1D.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MOD21A1D')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varlandSurfaceTemperature=dataset.select('LST_1KM');
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
'Land Surface Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD21A1D)


[MOD21A1D.061 Terra Land Surface Temperature and 3\-Band Emissivity Daily Global 1km](/earth-engine/datasets/catalog/MODIS_061_MOD21A1D)

The MOD21A1D dataset is produced daily from daytime Level 2 Gridded (L2G) intermediate LST products at a spatial resolution of 1,000 meters. The L2G process maps the daily MOD21 swath granules onto a sinusoidal MODIS grid and stores all observations falling over a gridded cell for a given day. The …

 MODIS/061/MOD21A1D,
 climate,daily,emissivity,global,lst,nasa,surface\-temperature,terra,usgs

2000\-02\-24T00:00:00Z/2025\-07\-16T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MOD21A1D.061](https://doi.org/https://doi.org/10.5067/MODIS/MOD21A1D.061)
* [https://doi.org/10\.5067/MODIS/MOD21A1D.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD21A1D)









