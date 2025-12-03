



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Long\-term Land Surface Temperature Daytime Monthly Standard Deviation


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.1420114)



Earth Engine Snippet


`ee.Image("OpenLandMap/CLM/CLM_LST_MOD11A2-DAY_SD/v01")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_CLM_CLM_LST_MOD11A2-DAY_SD_v01)





Tags


[climate](/earth-engine/datasets/tags/climate)
[envirometrix](/earth-engine/datasets/tags/envirometrix)
[lst](/earth-engine/datasets/tags/lst)
[mod11a2](/earth-engine/datasets/tags/mod11a2)
[modis](/earth-engine/datasets/tags/modis)
[monthly](/earth-engine/datasets/tags/monthly)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)








#### Description



Long\-term MODIS LST day\-time and night\-time temperatures standard deviation
at 1 km based on the 2000\-2017 time series.


Derived using the [data.table package and quantile function in R](https://gitlab.com/openlandmap/global-layers/tree/master/input_layers/MOD11A2).
For more info about the MODIS LST product see [this page](https://lpdaac.usgs.gov/products/mod11a2v006/).
Antarctica is not included.


To access and visualize maps outside of Earth Engine, use [this page](https://opengeohub.org/about-openlandmap).


If you discover a bug, artifact or inconsistency in the LandGIS maps
or if you have a question please use the following channels:


* [Technical issues and questions about the code](https://gitlab.com/openlandmap/global-layers/issues)
* [General questions and comments](https://disqus.com/home/forums/landgis/)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `jan` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, January |
| `feb` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, February |
| `mar` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, March |
| `apr` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, April |
| `may` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, May |
| `jun` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, June |
| `jul` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, July |
| `aug` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, August |
| `sep` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, September |
| `oct` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, October |
| `nov` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, November |
| `dec` | K | 25\* | 390\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly stddev, December |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Long\-term MODIS LST day\-time and night\-time temperatures, sd and differences
at 1 km based on the 2000\-2017 time series
[10\.5281/zenodo.1420115](https://doi.org/10.5281/zenodo.1420114)





### DOIs


* [https://doi.org/10\.5281/zenodo.1420114](https://doi.org/10.5281/zenodo.1420114)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/CLM/CLM_LST_MOD11A2-DAY_SD/v01');

varvisualization={
bands:['jan'],
min:25.0,
max:390.0,
palette:[
'2828ff','2828ff','6666ff','8989ff','a1a1ff','b2b2ff',
'c0c0ff','cbcbff','d5d5ff','dedeff','e6e6ff','ededff',
'f5f5ff','ffffff','fcfcff','fffbfb','fff4f4','ffeded',
'ffe5e5','ffdddd','ffd4d4','ffcbcb','ffbfbf','ffb2b2',
'ffa1a1','ff8a8a','ff6767','ff2929',
]
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Long-term Land Surface Temperature daytime monthly sd');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_CLM_CLM_LST_MOD11A2-DAY_SD_v01)


[OpenLandMap Long\-term Land Surface Temperature Daytime Monthly Standard Deviation](/earth-engine/datasets/catalog/OpenLandMap_CLM_CLM_LST_MOD11A2-DAY_SD_v01)

Long\-term MODIS LST day\-time and night\-time temperatures standard deviation at 1 km based on the 2000\-2017 time series. Derived using the data.table package and quantile function in R. For more info about the MODIS LST product see this page. Antarctica is not included. To access and visualize maps outside of …

 OpenLandMap/CLM/CLM\_LST\_MOD11A2\-DAY\_SD/v01,
 climate,envirometrix,lst,mod11a2,modis,monthly,opengeohub,openlandmap

2000\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.1420114](https://doi.org/https://doi.org/10.5281/zenodo.1420114)
* [https://doi.org/10\.5281/zenodo.1420114](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_CLM_CLM_LST_MOD11A2-DAY_SD_v01)









