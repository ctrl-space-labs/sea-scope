



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Soil Bulk Density


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.1475970)



Earth Engine Snippet


`ee.Image("OpenLandMap/SOL/SOL_BULKDENS-FINEEARTH_USDA-4A1H_M/v02")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_BULKDENS-FINEEARTH_USDA-4A1H_M_v02)





Tags


[density](/earth-engine/datasets/tags/density)
[envirometrix](/earth-engine/datasets/tags/envirometrix)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[soil](/earth-engine/datasets/tags/soil)
bulk








#### Description



Soil bulk density (fine earth) 10 x kg / m3 at 6 standard
depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution.


Processing steps are described in detail [here](https://gitlab.com/openlandmap/global-layers/LandGISmaps/tree/master/soil).
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
| `b0` | kg/m^3 | 5\* | 185\* | 10 | Soil bulk density at 0 cm depth |
| `b10` | kg/m^3 | 5\* | 185\* | 10 | Soil bulk density at 10 cm depth |
| `b30` | kg/m^3 | 5\* | 185\* | 10 | Soil bulk density at 30 cm depth |
| `b60` | kg/m^3 | 5\* | 185\* | 10 | Soil bulk density at 60 cm depth |
| `b100` | kg/m^3 | 5\* | 185\* | 10 | Soil bulk density at 100 cm depth |
| `b200` | kg/m^3 | 5\* | 185\* | 10 | Soil bulk density at 200 cm depth |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Tomislav Hengl. (2018\). Soil bulk density (fine earth) 10 x kg / m\-cubic at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution (Version v02\) \[Data set]. Zenodo.
[10\.5281/zenodo.1475970](https://doi.org/10.5281/zenodo.1475970)





### DOIs


* [https://doi.org/10\.5281/zenodo.1475970](https://doi.org/10.5281/zenodo.1475970)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/SOL/SOL_BULKDENS-FINEEARTH_USDA-4A1H_M/v02');

varvisualization={
bands:['b0'],
min:5.0,
max:185.0,
palette:['5e3c99','b2abd2','f7e0b2','fdb863','e63b01']
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Soil bulk density in x 10 kg / m3');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_BULKDENS-FINEEARTH_USDA-4A1H_M_v02)


[OpenLandMap Soil Bulk Density](/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_BULKDENS-FINEEARTH_USDA-4A1H_M_v02)

Soil bulk density (fine earth) 10 x kg / m3 at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution. Processing steps are described in detail here. Antarctica is not included. To access and visualize maps outside of Earth Engine, use this page. If …

 OpenLandMap/SOL/SOL\_BULKDENS\-FINEEARTH\_USDA\-4A1H\_M/v02,
 density,envirometrix,opengeohub,openlandmap,soil

1950\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.1475970](https://doi.org/https://doi.org/10.5281/zenodo.1475970)
* [https://doi.org/10\.5281/zenodo.1475970](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_BULKDENS-FINEEARTH_USDA-4A1H_M_v02)









