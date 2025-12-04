



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Soil Organic Carbon Content


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.1475457)



Earth Engine Snippet


`ee.Image("OpenLandMap/SOL/SOL_ORGANIC-CARBON_USDA-6A1C_M/v02")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_ORGANIC-CARBON_USDA-6A1C_M_v02)





Tags


[carbon](/earth-engine/datasets/tags/carbon)
[envirometrix](/earth-engine/datasets/tags/envirometrix)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[soil](/earth-engine/datasets/tags/soil)
organic








#### Description



Soil organic carbon content in x 5 g / kg at 6 standard depths
(0, 10, 30, 60, 100 and 200 cm) at 250 m resolution


Predicted from a global compilation of soil points. Processing steps are described
in detail [here](https://gitlab.com/openlandmap/global-layers/tree/master/soil).
Antarctica is not included.


To access and visualize maps outside of Earth Engine, use [this page](https://opengeohub.org/about-openlandmap).


If you discover a bug, artifact or inconsistency in the LandGIS maps
or if you have a question please use the following channels:


* [Technical issues and questions about the code](https://gitlab.com/openlandmap/global-layers/issues)
* [General questions and comments](https://disqus.com/home/forums/landgis/)





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `b0` | g/kg | 0\* | 120\* | 5 | Soil organic carbon content at 0 cm depth |
| `b10` | g/kg | 0\* | 120\* | 5 | Soil organic carbon content at 10 cm depth |
| `b30` | g/kg | 0\* | 120\* | 5 | Soil organic carbon content at 30 cm depth |
| `b60` | g/kg | 0\* | 120\* | 5 | Soil organic carbon content at 60 cm depth |
| `b100` | g/kg | 0\* | 120\* | 5 | Soil organic carbon content at 100 cm depth |
| `b200` | g/kg | 0\* | 120\* | 5 | Soil organic carbon content at 200 cm depth |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Tomislav Hengl, \& Ichsani Wheeler. (2018\). Soil organic carbon content in x 5 g / kg at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution (Version v02\) \[Data set]. Zenodo.
[10\.5281/zenodo.1475457](https://doi.org/10.5281/zenodo.1475457)





### DOIs


* [https://doi.org/10\.5281/zenodo.1475457](https://doi.org/10.5281/zenodo.1475457)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/SOL/SOL_ORGANIC-CARBON_USDA-6A1C_M/v02');

varvisualization={
bands:['b0'],
min:0.0,
max:120.0,
palette:[
'ffffa0','f7fcb9','d9f0a3','addd8e','78c679','41ab5d',
'238443','005b29','004b29','012b13','00120b',
]
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Soil organic carbon content in x 5 g / kg');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_ORGANIC-CARBON_USDA-6A1C_M_v02)


[OpenLandMap Soil Organic Carbon Content](/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_ORGANIC-CARBON_USDA-6A1C_M_v02)

Soil organic carbon content in x 5 g / kg at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution Predicted from a global compilation of soil points. Processing steps are described in detail here. Antarctica is not included. To access and visualize maps …

 OpenLandMap/SOL/SOL\_ORGANIC\-CARBON\_USDA\-6A1C\_M/v02,
 carbon,envirometrix,opengeohub,openlandmap,soil

1950\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.1475457](https://doi.org/https://doi.org/10.5281/zenodo.1475457)
* [https://doi.org/10\.5281/zenodo.1475457](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_ORGANIC-CARBON_USDA-6A1C_M_v02)









