



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

RTMA: Real\-Time Mesoscale Analysis


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================








Dataset Availability
2011\-01\-01T00:00:00Z–2025\-07\-16T18:00:00Z
Dataset Provider


[NOAA/NWS](https://www.nco.ncep.noaa.gov/pmb/products/rtma/)



Earth Engine Snippet


`ee.ImageCollection("NOAA/NWS/RTMA")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_NWS_RTMA)





Cadence
1 Hour
Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[cloud](/earth-engine/datasets/tags/cloud)
[geophysical](/earth-engine/datasets/tags/geophysical)
[humidity](/earth-engine/datasets/tags/humidity)
[noaa](/earth-engine/datasets/tags/noaa)
[nws](/earth-engine/datasets/tags/nws)
[precipitation](/earth-engine/datasets/tags/precipitation)
[pressure](/earth-engine/datasets/tags/pressure)
[surface](/earth-engine/datasets/tags/surface)
[temperature](/earth-engine/datasets/tags/temperature)
[weather](/earth-engine/datasets/tags/weather)
[wind](/earth-engine/datasets/tags/wind)
rtma
visibility








#### Description



The Real\-Time Mesoscale Analysis (RTMA) is a high\-spatial and temporal
resolution analysis for near\-surface weather conditions. This dataset
includes hourly analyses at 2\.5 km for CONUS.





### Bands



**Pixel Size**
  
2500 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `HGT` | m | \-81\* | 4226\* | Model terrain elevation |
| `PRES` | Pa | 60848\* | 105183\* | Pressure |
| `TMP` | °C | \-43\.2\* | 43\.73\* | Temperature |
| `DPT` | °C | \-81\.41\* | 30\.92\* | Dew point temperature |
| `UGRD` | m/s | \-32\.93\* | 34\.04\* | U\-component of wind |
| `VGRD` | m/s | \-28\.44\* | 39\.21\* | V\-component of wind |
| `SPFH` | Mass fraction | 0\* | 0\.02\* | Specific humidity |
| `WDIR` | deg | 0\* | 360\* | Wind direction (from which blowing) |
| `WIND` | m/s | 0\* | 42\.46\* | Wind speed |
| `GUST` | m/s | 0\* | 58\.02\* | Wind speed (gust) |
| `VIS` | m | 0\* | 20000\* | Visibility |
| `TCDC` | % | 0\* | 100\* | Total cloud cover |
| `ACPC01` | kg/m^2 | 0\* | 1\* | Total precipitation |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


NOAA data, information, and products, regardless of the method of delivery,
are not subject to copyright and carry no restrictions on their subsequent
use by the public. Once obtained, they may be put to any lawful use. The
forgoing data is in the public domain and is being provided without
restriction on use and distribution. For more information visit the
[NWS disclaimer site](https://www.weather.gov/disclaimer/).




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/NWS/RTMA')
.filter(ee.Filter.date('2018-03-01','2018-03-02'));
varwindSpeed=dataset.select('WIND');
varwindSpeedVis={
min:0.0,
max:12.0,
palette:['001137','01abab','e7eb05','620500'],
};
Map.setCenter(-95.62,39.91,4);
Map.addLayer(windSpeed,windSpeedVis,'Wind Speed');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_NWS_RTMA)


[RTMA: Real\-Time Mesoscale Analysis](/earth-engine/datasets/catalog/NOAA_NWS_RTMA)

The Real\-Time Mesoscale Analysis (RTMA) is a high\-spatial and temporal resolution analysis for near\-surface weather conditions. This dataset includes hourly analyses at 2\.5 km for CONUS.

 NOAA/NWS/RTMA,
 atmosphere,climate,cloud,geophysical,humidity,noaa,nws,precipitation,pressure,surface,temperature,weather,wind

2011\-01\-01T00:00:00Z/2025\-07\-16T18:00:00Z



 20\.15 \-130\.17 52\.91 \-60\.81
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








