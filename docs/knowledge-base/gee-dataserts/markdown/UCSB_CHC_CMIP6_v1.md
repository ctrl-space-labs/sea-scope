



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

The Climate Hazards Center (CHC) Coupled Model Intercomparison Project Phase 6 (CHC\-CMIP6\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================================================================








Dataset Availability
1983\-01\-01T00:00:00Z–2016\-12\-31T00:00:00Z
Dataset Provider


[UCSB](https://chc.ucsb.edu/data/chc-cmip6)



Earth Engine Snippet


`ee.ImageCollection("UCSB/CHC/CMIP6/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UCSB/UCSB_CHC_CMIP6_v1)





Cadence
1 Day
Tags


[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[precipitation](/earth-engine/datasets/tags/precipitation)
[ucsb](/earth-engine/datasets/tags/ucsb)
[weather](/earth-engine/datasets/tags/weather)








#### Description



CHC\-CMIP6 was explicitly developed to support the analysis of
climate\-related hazards over the recent past and in the near\-future.


This climate projection dataset contains global, daily gridded data for the
observational (1983\-2016\) and projection (2030 and 2050\) periods to be used
in the identification and monitoring of hydroclimatic extremes. The dataset
contains global daily high resolution (0\.05°) grids of the Climate
Hazards InfraRed Temperature with Stations (CHIRTS\-daily) temperature
product, the Climate Hazards InfraRed Precipitation with Stations (CHIRPS)
precipitation product, and ERA5\-derived relative humidity, from which Vapor
Pressure Deficits (VPD) and maximum Wet Bulb Globe Temperatures (WBGTmax)
were derived.


Large CMIP6 ensembles from the Shared Socioeconomic Pathway (SSP) 245 and
SSP 585 scenarios were used to develop high resolution (0\.05°) daily
2030 and 2050 delta fields.


For more information, see
[The Climate Hazards Center (CHC) Coupled Model Intercomparison Project
Phase 6 (CHC\-CMIP6\)](https://chc.ucsb.edu/data/chc-cmip6).





### Bands



**Pixel Size**
  
5566 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `CHIRPS` | mm/d | 0 | 751\.05 | Daily total precipitation. |
| `himax` | °C | \-49\.76 | 78\.56 | Daily maximum Heat Index. |
| `RH` | % | \-1\.33 | 100 | Relative Humidity. |
| `RHx` | % | \-3\.11 | 100 | Relative humidity at the hour of maximum temperature |
| `RHn` | % | \-2\.603 | 100 | Relative humidity at the hour of minimum temperature. |
| `wbgtmax` | °C | \-100\.54 | 33\.76 | Daily maximum wet bulb globe temperature. |
| `vpd` | kPa | 0 | 67\.98 | Daily vapor pressure deficit. |
| `svp` | kPa | 0\.011 | 71\.41 | Daily average saturation vapor pressure. |
| `Tmax` | °C | \-43\.04 | 90\.52 | Daily maximum near\-surface air temperature. |
| `Tmin` | °C | \-46\.72 | 89\.82 | Daily minimum near\-surface air temperature. |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| projection\_year | INT | Projection Year |
| scenario | STRING | Shared Socioeconomic Pathway (SSP) scenarios |




### Terms of Use


**Terms of Use**


The dataset is under a Creative Commons Attribution 4\.0 International
(CC BY 4\.0\) license. For more information, see
[The Climate Hazards Center (CHC) Coupled Model Intercomparison Project
Phase 6 (CHC\-CMIP6\)](https://chc.ucsb.edu/data/chc-cmip6).




### Citations



Citations:
* Williams, E., Funk, C., Peterson, P., \& Tuholske, C. (2024\). High resolution
climate change observations and projections for the evaluation of
heat\-related extremes. Scientific Data, 11(1\), 261\.
[https://www.nature.com/articles/s41597\-024\-03074\-w](https://www.nature.com/articles/s41597-024-03074-w)
2015\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('UCSB/CHC/CMIP6/v1')
.filter(ee.Filter.date('2016-08-01','2016-08-30'));
varchirps=dataset.select('CHIRPS');
varchirpsVis={
min:0,
max:100.0,
palette:['d7191c','fdae61','ffffbf','abd9e9','2c7bb6'],
};
Map.setCenter(93.17,10.14,4);
Map.addLayer(chirps,chirpsVis,'CHC CMIP6');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UCSB/UCSB_CHC_CMIP6_v1)


[The Climate Hazards Center (CHC) Coupled Model Intercomparison Project Phase 6 (CHC\-CMIP6\)](/earth-engine/datasets/catalog/UCSB_CHC_CMIP6_v1)

CHC\-CMIP6 was explicitly developed to support the analysis of climate\-related hazards over the recent past and in the near\-future. This climate projection dataset contains global, daily gridded data for the observational (1983\-2016\) and projection (2030 and 2050\) periods to be used in the identification and monitoring of hydroclimatic extremes. The …

 UCSB/CHC/CMIP6/v1,
 climate,geophysical,precipitation,ucsb,weather

1983\-01\-01T00:00:00Z/2016\-12\-31T00:00:00Z



 \-50 \-180 50 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








