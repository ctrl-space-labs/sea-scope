



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Predicted Hapludalfs Probability


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.1476844)



Earth Engine Snippet


`ee.Image("OpenLandMap/SOL/SOL_GRTGROUP_USDA-SOILTAX-HAPLUDALFS_P/v01")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_GRTGROUP_USDA-SOILTAX-HAPLUDALFS_P_v01)





Tags


[envirometrix](/earth-engine/datasets/tags/envirometrix)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[soil](/earth-engine/datasets/tags/soil)
argillic
hapludalfs








#### Description



Predicted USDA soil great groups at 250 m (probabilities).


Distribution of the USDA soil great groups based on machine learning predictions
from global compilation of soil profiles. To learn more about soil great groups
please refer to the [Illustrated Guide to Soil Taxonomy \- NRCS \- USDA](https://www.nrcs.usda.gov/wps/PA_NRCSConsumption/download/?cid=stelprdb1247203.pdf).


* Processing steps are described in detail [here](https://gitlab.com/openlandmap/global-layers/tree/master/soil)
* Antarctica is not included.


To access and visualize maps outside of Earth Engine, use [this page](https://opengeohub.org/about-openlandmap).


If you discover a bug, artifact or inconsistency in the LandGIS maps
or if you have a question please use the following channels:


* [Technical issues and questions about the code](https://gitlab.com/openlandmap/global-layers/issues)
* [General questions and comments](https://disqus.com/home/forums/landgis/)





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `grtgroup` | % | 0\* | 35\* | Predicted Hapludalfs probability |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Tomislav Hengl, \& Travis Nauman. (2018\). Predicted USDA soil great groups at 250 m (probabilities) (Version v01\) \[Data set]. Zenodo.
[10\.5281/zenodo.1476844](https://doi.org/10.5281/zenodo.1476844)





### DOIs


* [https://doi.org/10\.5281/zenodo.1476844](https://doi.org/10.5281/zenodo.1476844)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/SOL/SOL_GRTGROUP_USDA-SOILTAX-HAPLUDALFS_P/v01');

varvisualization={
bands:['grtgroup'],
min:0.0,
max:35.0,
palette:['ffffb2','fecc5c','fd8d3c','f03b20','bd0026']
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Hapludalfs');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_GRTGROUP_USDA-SOILTAX-HAPLUDALFS_P_v01)


[OpenLandMap Predicted Hapludalfs Probability](/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_GRTGROUP_USDA-SOILTAX-HAPLUDALFS_P_v01)

Predicted USDA soil great groups at 250 m (probabilities). Distribution of the USDA soil great groups based on machine learning predictions from global compilation of soil profiles. To learn more about soil great groups please refer to the Illustrated Guide to Soil Taxonomy \- NRCS \- USDA. Processing steps are …

 OpenLandMap/SOL/SOL\_GRTGROUP\_USDA\-SOILTAX\-HAPLUDALFS\_P/v01,
 envirometrix,opengeohub,openlandmap,soil

1950\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.1476844](https://doi.org/https://doi.org/10.5281/zenodo.1476844)
* [https://doi.org/10\.5281/zenodo.1476844](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_GRTGROUP_USDA-SOILTAX-HAPLUDALFS_P_v01)









