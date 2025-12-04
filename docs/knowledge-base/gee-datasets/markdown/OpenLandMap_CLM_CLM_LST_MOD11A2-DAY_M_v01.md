



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Long\-term Land Surface Temperature Daytime Monthly Median


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.1420114)



Earth Engine Snippet


`ee.Image("OpenLandMap/CLM/CLM_LST_MOD11A2-DAY_M/v01")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_CLM_CLM_LST_MOD11A2-DAY_M_v01)





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



Land Surface Temperature daytime monthly mean value 2000\-2017\.


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
| `jan` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, January |
| `feb` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, February |
| `mar` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, March |
| `apr` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, April |
| `may` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, May |
| `jun` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, June |
| `jul` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, July |
| `aug` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, August |
| `sep` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, September |
| `oct` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, October |
| `nov` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, November |
| `dec` | K | 11989\* | 16700\* | 0\.02 | Long\-term Land Surface Temperature daytime monthly mean, December |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Long\-term MODIS LST day\-time and night\-time temperatures, sd and differences
at 1 km based on the 2000\-2017 time series
[10\.5281/zenodo.1420114](https://doi.org/10.5281/zenodo.1420114)





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
vardataset=ee.Image('OpenLandMap/CLM/CLM_LST_MOD11A2-DAY_M/v01');

varvisualization={
bands:['jan'],
min:11989.0,
max:16700.0,
palette:['0000ff','00ffff','ffff00','ff0000']
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Long-term Land Surface Temperature daytime monthly mean');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_CLM_CLM_LST_MOD11A2-DAY_M_v01)


[OpenLandMap Long\-term Land Surface Temperature Daytime Monthly Median](/earth-engine/datasets/catalog/OpenLandMap_CLM_CLM_LST_MOD11A2-DAY_M_v01)

Land Surface Temperature daytime monthly mean value 2000\-2017\. Derived using the data.table package and quantile function in R. For more info about the MODIS LST product see this page. Antarctica is not included. To access and visualize maps outside of Earth Engine, use this page. If you discover a bug, …

 OpenLandMap/CLM/CLM\_LST\_MOD11A2\-DAY\_M/v01,
 climate,envirometrix,lst,mod11a2,modis,monthly,opengeohub,openlandmap

2000\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.1420114](https://doi.org/https://doi.org/10.5281/zenodo.1420114)
* [https://doi.org/10\.5281/zenodo.1420114](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_CLM_CLM_LST_MOD11A2-DAY_M_v01)









