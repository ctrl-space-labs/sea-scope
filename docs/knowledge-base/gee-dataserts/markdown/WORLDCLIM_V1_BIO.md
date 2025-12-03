



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WorldClim BIO Variables V1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================








Dataset Availability
1960\-01\-01T00:00:00Z–1991\-01\-01T00:00:00Z
Dataset Provider


[University of California, Berkeley](https://www.worldclim.org/)



Earth Engine Snippet


`ee.Image("WORLDCLIM/V1/BIO")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WORLDCLIM/WORLDCLIM_V1_BIO)





Tags


[berkeley](/earth-engine/datasets/tags/berkeley)
[climate](/earth-engine/datasets/tags/climate)
[monthly](/earth-engine/datasets/tags/monthly)
[precipitation](/earth-engine/datasets/tags/precipitation)
[temperature](/earth-engine/datasets/tags/temperature)
[weather](/earth-engine/datasets/tags/weather)
[worldclim](/earth-engine/datasets/tags/worldclim)
bioclim
coldest
diurnal
driest
isothermality
seasonality
warmest
wettest








#### Description



WorldClim V1 Bioclim provides bioclimatic variables that are derived from
the monthly temperature and rainfall in order to generate more biologically
meaningful values.


The bioclimatic variables represent annual trends (e.g., mean annual
temperature, annual precipitation), seasonality (e.g., annual range in
temperature and precipitation), and extreme or limiting environmental
factors (e.g., temperature of the coldest and warmest month, and
precipitation of the wet and dry quarters).


The bands scheme follows that of ANUCLIM, except that for temperature
seasonality the standard deviation was used because a coefficient of
variation does not make sense with temperatures between \-1 and 1\.


WorldClim version 1 was developed by Robert J. Hijmans, Susan Cameron,
and Juan Parra, at the Museum of Vertebrate Zoology, University of
California, Berkeley, in collaboration with Peter Jones and Andrew Jarvis
(CIAT), and with Karen Richardson (Rainforest CRC).





### Bands



**Pixel Size**
  
927\.67 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `bio01` | °C | \-29\* | 32\* | 0\.1 | Annual mean temperature |
| `bio02` | °C | 0\.9\* | 21\.4\* | 0\.1 | Mean diurnal range (mean of monthly (max temp \- min temp)) |
| `bio03` | % | 7\* | 96\* |  | Isothermality (bio02/bio07 \* 100\) |
| `bio04` | °C | 0\.62\* | 227\.21\* | 0\.01 | Temperature seasonality (Standard deviation \* 100\) |
| `bio05` | °C | \-9\.6\* | 49\* | 0\.1 | Max temperature of warmest month |
| `bio06` | °C | \-57\.3\* | 25\.8\* | 0\.1 | Min temperature of coldest month |
| `bio07` | °C | 5\.3\* | 72\.5\* | 0\.1 | Temperature annual range (bio05\-bio06\) |
| `bio08` | °C | \-28\.5\* | 37\.8\* | 0\.1 | Mean temperature of wettest quarter |
| `bio09` | °C | \-52\.1\* | 36\.6\* | 0\.1 | Mean temperature of driest quarter |
| `bio10` | °C | \-14\.3\* | 38\.3\* | 0\.1 | Mean temperature of warmest quarter |
| `bio11` | °C | \-52\.1\* | 28\.9\* | 0\.1 | Mean temperature of coldest quarter |
| `bio12` | mm | 0\* | 11401\* |  | Annual precipitation |
| `bio13` | mm | 0\* | 2949\* |  | Precipitation of wettest month |
| `bio14` | mm | 0\* | 752\* |  | Precipitation of driest month |
| `bio15` | Coefficient of Variation | 0\* | 265\* |  | Precipitation seasonality |
| `bio16` | mm | 0\* | 8019\* |  | Precipitation of wettest quarter |
| `bio17` | mm | 0\* | 2495\* |  | Precipitation of driest quarter |
| `bio18` | mm | 0\* | 6090\* |  | Precipitation of warmest quarter |
| `bio19` | mm | 0\* | 5162\* |  | Precipitation of coldest quarter |


 \* estimated min or max value


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
vardataset=ee.Image('WORLDCLIM/V1/BIO');
varannualMeanTemperature=dataset.select('bio01').multiply(0.1);
varvisParams={
min:-23,
max:30,
palette:['blue','purple','cyan','green','yellow','red'],
};
Map.setCenter(71.7,52.4,3);
Map.addLayer(annualMeanTemperature,visParams,'Annual Mean Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WORLDCLIM/WORLDCLIM_V1_BIO)


[WorldClim BIO Variables V1](/earth-engine/datasets/catalog/WORLDCLIM_V1_BIO)

WorldClim V1 Bioclim provides bioclimatic variables that are derived from the monthly temperature and rainfall in order to generate more biologically meaningful values. The bioclimatic variables represent annual trends (e.g., mean annual temperature, annual precipitation), seasonality (e.g., annual range in temperature and precipitation), and extreme or limiting environmental factors (e.g., …

 WORLDCLIM/V1/BIO,
 berkeley,climate,monthly,precipitation,temperature,weather,worldclim

1960\-01\-01T00:00:00Z/1991\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








