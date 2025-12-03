



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WorldClim Climatology V1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================








Dataset Availability
1960\-01\-01T00:00:00Z–1991\-01\-01T00:00:00Z
Dataset Provider


[University of California, Berkeley](https://www.worldclim.org/)



Earth Engine Snippet


`ee.ImageCollection("WORLDCLIM/V1/MONTHLY")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WORLDCLIM/WORLDCLIM_V1_MONTHLY)





Climatological Interval
1 Month
Tags


[berkeley](/earth-engine/datasets/tags/berkeley)
[climate](/earth-engine/datasets/tags/climate)
[monthly](/earth-engine/datasets/tags/monthly)
[precipitation](/earth-engine/datasets/tags/precipitation)
[temperature](/earth-engine/datasets/tags/temperature)
[weather](/earth-engine/datasets/tags/weather)
[worldclim](/earth-engine/datasets/tags/worldclim)








#### Description



WorldClim version 1 has average monthly global climate data for minimum,
mean, and maximum temperature and for precipitation.


WorldClim version 1 was developed by Robert J. Hijmans, Susan Cameron,
and Juan Parra, at the Museum of Vertebrate Zoology, University
of California, Berkeley, in collaboration with Peter Jones and
Andrew Jarvis (CIAT), and with Karen Richardson (Rainforest CRC).





### Bands



**Pixel Size**
  
927\.67 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `tavg` | °C | \-53\.6\* | 39\.4\* | 0\.1 | Mean temperature |
| `tmin` | °C | \-57\.3\* | 32\.5\* | 0\.1 | Minimum temperature |
| `tmax` | °C | \-50\* | 49\* | 0\.1 | Maximum temperature |
| `prec` | mm | 0\* | 2949\* |  | Precipitation |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| month | DOUBLE | Month |




### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Hijmans, R.J., S.E. Cameron, J.L. Parra, P.G. Jones and A. Jarvis,
2005\. Very High Resolution Interpolated Climate Surfaces for Global Land
Areas. International Journal of Climatology 25: 1965\-1978\.
[doi:10\.1002/joc.1276](https://doi.org/10.1002/joc.1276).





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('WORLDCLIM/V1/MONTHLY');
varmeanTemperature=dataset.select('tavg').first().multiply(0.1);
varmeanTemperatureVis={
min:-40,
max:30,
palette:['blue','purple','cyan','green','yellow','red'],
};
Map.setCenter(71.7,52.4,3);
Map.addLayer(meanTemperature,meanTemperatureVis,'Mean Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WORLDCLIM/WORLDCLIM_V1_MONTHLY)


[WorldClim Climatology V1](/earth-engine/datasets/catalog/WORLDCLIM_V1_MONTHLY)

WorldClim version 1 has average monthly global climate data for minimum, mean, and maximum temperature and for precipitation. WorldClim version 1 was developed by Robert J. Hijmans, Susan Cameron, and Juan Parra, at the Museum of Vertebrate Zoology, University of California, Berkeley, in collaboration with Peter Jones and Andrew Jarvis …

 WORLDCLIM/V1/MONTHLY,
 berkeley,climate,monthly,precipitation,temperature,weather,worldclim

1960\-01\-01T00:00:00Z/1991\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








