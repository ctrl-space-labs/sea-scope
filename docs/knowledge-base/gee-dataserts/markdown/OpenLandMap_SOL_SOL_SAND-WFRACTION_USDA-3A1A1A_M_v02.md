



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Sand Content


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.1476851)



Earth Engine Snippet


`ee.Image("OpenLandMap/SOL/SOL_SAND-WFRACTION_USDA-3A1A1A_M/v02")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_SAND-WFRACTION_USDA-3A1A1A_M_v02)





Tags


[envirometrix](/earth-engine/datasets/tags/envirometrix)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[sand](/earth-engine/datasets/tags/sand)
[soil](/earth-engine/datasets/tags/soil)
[usda](/earth-engine/datasets/tags/usda)








#### Description



Sand content in % (kg / kg) at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution


Based on machine learning predictions from global compilation of soil profiles and samples.
Processing steps are described in detail [here](https://gitlab.com/openlandmap/global-layers/tree/master/soil).
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




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `b0` | % (kg / kg) | 1\* | 100\* | Sand content at 0 cm depth |
| `b10` | % (kg / kg) | 1\* | 100\* | Sand content at 10 cm depth |
| `b30` | % (kg / kg) | 1\* | 100\* | Sand content at 30 cm depth |
| `b60` | % (kg / kg) | 1\* | 100\* | Sand content at 60 cm depth |
| `b100` | % (kg / kg) | 1\* | 100\* | Sand content at 100 cm depth |
| `b200` | % (kg / kg) | 1\* | 100\* | Sand content at 200 cm depth |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Tomislav Hengl. (2018\). Sand content in % (kg / kg) at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution (Version v02\) \[Data set].
[10\.5281/zenodo.1476851](https://doi.org/10.5281/zenodo.1476851)





### DOIs


* [https://doi.org/10\.5281/zenodo.1476851](https://doi.org/10.5281/zenodo.1476851)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/SOL/SOL_SAND-WFRACTION_USDA-3A1A1A_M/v02');

varvisualization={
bands:['b0'],
min:1.0,
max:100.0,
palette:[
'ffff00','f8f806','f1f10c','ebeb13','e4e419','dddd20',
'd7d726','d0d02d','caca33','c3c33a','bcbc41','b6b647',
'b0b04e','a9a954','a3a35a','9c9c61','959568','8f8f6e',
'898975','82827b','7b7b82','757589','6e6e8f','686895',
'61619c','5a5aa3','5454a9','4d4db0','4747b6','4141bc',
'3a3ac3','3333ca','2d2dd0','2626d7','2020dd','1919e4',
'1212eb','0c0cf1','0606f8','0000ff',
]
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Sand content in % (kg / kg)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_SAND-WFRACTION_USDA-3A1A1A_M_v02)


[OpenLandMap Sand Content](/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_SAND-WFRACTION_USDA-3A1A1A_M_v02)

Sand content in % (kg / kg) at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution Based on machine learning predictions from global compilation of soil profiles and samples. Processing steps are described in detail here. Antarctica is not included. To access and …

 OpenLandMap/SOL/SOL\_SAND\-WFRACTION\_USDA\-3A1A1A\_M/v02,
 envirometrix,opengeohub,openlandmap,sand,soil,usda

1950\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.1476851](https://doi.org/https://doi.org/10.5281/zenodo.1476851)
* [https://doi.org/10\.5281/zenodo.1476851](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_SAND-WFRACTION_USDA-3A1A1A_M_v02)









