



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Soil Texture Class (USDA System)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.1475451)



Earth Engine Snippet


`ee.Image("OpenLandMap/SOL/SOL_TEXTURE-CLASS_USDA-TT_M/v02")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_TEXTURE-CLASS_USDA-TT_M_v02)





Tags


[envirometrix](/earth-engine/datasets/tags/envirometrix)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[soil](/earth-engine/datasets/tags/soil)
[usda](/earth-engine/datasets/tags/usda)
texture








#### Description



Soil texture classes (USDA system) for 6 soil depths (0, 10, 30, 60, 100 and 200 cm) at 250 m


Derived from predicted soil texture fractions using the soiltexture package in R.
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




| Name | Description |
| --- | --- |
| `b0` | Soil texture class (USDA system) at 0 cm depth |
| `b10` | Soil texture class (USDA system) at 10 cm depth |
| `b30` | Soil texture class (USDA system) at 30 cm depth |
| `b60` | Soil texture class (USDA system) at 60 cm depth |
| `b100` | Soil texture class (USDA system) at 100 cm depth |
| `b200` | Soil texture class (USDA system) at 200 cm depth |


**b0 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d5c36b | Cl |
| 2 | \#b96947 | SiCl |
| 3 | \#9d3706 | SaCl |
| 4 | \#ae868f | ClLo |
| 5 | \#f86714 | SiClLo |
| 6 | \#46d143 | SaClLo |
| 7 | \#368f20 | Lo |
| 8 | \#3e5a14 | SiLo |
| 9 | \#ffd557 | SaLo |
| 10 | \#fff72e | Si |
| 11 | \#ff5a9d | LoSa |
| 12 | \#ff005b | Sa |


**b10 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d5c36b | Cl |
| 2 | \#b96947 | SiCl |
| 3 | \#9d3706 | SaCl |
| 4 | \#ae868f | ClLo |
| 5 | \#f86714 | SiClLo |
| 6 | \#46d143 | SaClLo |
| 7 | \#368f20 | Lo |
| 8 | \#3e5a14 | SiLo |
| 9 | \#ffd557 | SaLo |
| 10 | \#fff72e | Si |
| 11 | \#ff5a9d | LoSa |
| 12 | \#ff005b | Sa |


**b30 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d5c36b | Cl |
| 2 | \#b96947 | SiCl |
| 3 | \#9d3706 | SaCl |
| 4 | \#ae868f | ClLo |
| 5 | \#f86714 | SiClLo |
| 6 | \#46d143 | SaClLo |
| 7 | \#368f20 | Lo |
| 8 | \#3e5a14 | SiLo |
| 9 | \#ffd557 | SaLo |
| 10 | \#fff72e | Si |
| 11 | \#ff5a9d | LoSa |
| 12 | \#ff005b | Sa |


**b60 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d5c36b | Cl |
| 2 | \#b96947 | SiCl |
| 3 | \#9d3706 | SaCl |
| 4 | \#ae868f | ClLo |
| 5 | \#f86714 | SiClLo |
| 6 | \#46d143 | SaClLo |
| 7 | \#368f20 | Lo |
| 8 | \#3e5a14 | SiLo |
| 9 | \#ffd557 | SaLo |
| 10 | \#fff72e | Si |
| 11 | \#ff5a9d | LoSa |
| 12 | \#ff005b | Sa |


**b100 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d5c36b | Cl |
| 2 | \#b96947 | SiCl |
| 3 | \#9d3706 | SaCl |
| 4 | \#ae868f | ClLo |
| 5 | \#f86714 | SiClLo |
| 6 | \#46d143 | SaClLo |
| 7 | \#368f20 | Lo |
| 8 | \#3e5a14 | SiLo |
| 9 | \#ffd557 | SaLo |
| 10 | \#fff72e | Si |
| 11 | \#ff5a9d | LoSa |
| 12 | \#ff005b | Sa |


**b200 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d5c36b | Cl |
| 2 | \#b96947 | SiCl |
| 3 | \#9d3706 | SaCl |
| 4 | \#ae868f | ClLo |
| 5 | \#f86714 | SiClLo |
| 6 | \#46d143 | SaClLo |
| 7 | \#368f20 | Lo |
| 8 | \#3e5a14 | SiLo |
| 9 | \#ffd557 | SaLo |
| 10 | \#fff72e | Si |
| 11 | \#ff5a9d | LoSa |
| 12 | \#ff005b | Sa |




### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Tomislav Hengl. (2018\). Soil texture classes (USDA system) for 6 soil depths (0, 10, 30, 60, 100 and 200 cm) at 250 m (Version v02\) \[Data set]. Zenodo.
[10\.5281/zenodo.1475451](https://doi.org/10.5281/zenodo.1475451)





### DOIs


* [https://doi.org/10\.5281/zenodo.1475451](https://doi.org/10.5281/zenodo.1475451)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/SOL/SOL_TEXTURE-CLASS_USDA-TT_M/v02');

varvisualization={
bands:['b0'],
min:1.0,
max:12.0,
palette:[
'd5c36b','b96947','9d3706','ae868f','f86714','46d143',
'368f20','3e5a14','ffd557','fff72e','ff5a9d','ff005b',
]
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Soil texture class (USDA system)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_TEXTURE-CLASS_USDA-TT_M_v02)


[OpenLandMap Soil Texture Class (USDA System)](/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_TEXTURE-CLASS_USDA-TT_M_v02)

Soil texture classes (USDA system) for 6 soil depths (0, 10, 30, 60, 100 and 200 cm) at 250 m Derived from predicted soil texture fractions using the soiltexture package in R. Processing steps are described in detail here. Antarctica is not included. To access and visualize maps outside of …

 OpenLandMap/SOL/SOL\_TEXTURE\-CLASS\_USDA\-TT\_M/v02,
 envirometrix,opengeohub,openlandmap,soil,usda

1950\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.1475451](https://doi.org/https://doi.org/10.5281/zenodo.1475451)
* [https://doi.org/10\.5281/zenodo.1475451](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_TEXTURE-CLASS_USDA-TT_M_v02)









