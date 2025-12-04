



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil USDA Texture Class


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/texture_class")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_texture_class)





Tags


[africa](/earth-engine/datasets/tags/africa)
[aluminium](/earth-engine/datasets/tags/aluminium)
[isda](/earth-engine/datasets/tags/isda)
[soil](/earth-engine/datasets/tags/soil)








#### Description



USDA Texture Class at soil depths of 0\-20 cm and 20\-50 cm.
In areas of dense jungle (generally over central Africa), model accuracy is
low and therefore artifacts such as banding (striping) might be seen.


Soil property predictions were made by
[Innovative Solutions for Decision Agriculture Ltd. (iSDA)](https://isda-africa.com/)
at 30 m pixel size using machine learning coupled with remote sensing data
and a training set of over 100,000 analyzed soil samples.


Further information can be found in the
[FAQ](https://www.isda-africa.com/isdasoil/faq/) and
[technical information documentation](https://www.isda-africa.com/isdasoil/technical-information/). To submit an issue or request support, please visit
[the iSDAsoil site](https://isda-africa.com/isdasoil).





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `texture_0_20` | USDA Texture Class at 0\-20 cm depth |
| `texture_20_50` | USDA Texture Class at 20\-50 cm depth |


**texture\_0\_20 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d5c36b | Clay |
| 2 | \#b96947 | Silty Clay |
| 3 | \#9d3706 | Sandy Clay |
| 4 | \#ae868f | Clay Loam |
| 5 | \#f86714 | Silty Clay Loam |
| 6 | \#46d143 | Sandy Clay Loam |
| 7 | \#368f20 | Loam |
| 8 | \#3e5a14 | Silt Loam |
| 9 | \#ffd557 | Sandy Loam |
| 10 | \#fff72e | Silt |
| 11 | \#ff5a9d | Loamy Sand |
| 12 | \#ff005b | Sand |


**texture\_20\_50 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d5c36b | Clay |
| 2 | \#b96947 | Silty Clay |
| 3 | \#9d3706 | Sandy Clay |
| 4 | \#ae868f | Clay Loam |
| 5 | \#f86714 | Silty Clay Loam |
| 6 | \#46d143 | Sandy Clay Loam |
| 7 | \#368f20 | Loam |
| 8 | \#3e5a14 | Silt Loam |
| 9 | \#ffd557 | Sandy Loam |
| 10 | \#fff72e | Silt |
| 11 | \#ff5a9d | Loamy Sand |
| 12 | \#ff005b | Sand |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Hengl, T., Miller, M.A.E., Križan, J., et al. African soil properties and nutrients
mapped at 30 m spatial resolution using two\-scale ensemble machine learning.
Sci Rep 11, 6130 (2021\).
[doi:10\.1038/s41598\-021\-85639\-y](https://doi.org/10.1038/s41598-021-85639-y)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varraw=ee.Image("ISDASOIL/Africa/v1/texture_class");
Map.addLayer(
raw.select(0),{},"Texture class, 0-20 cm");
Map.addLayer(
raw.select(1),{},"Texture class, 20-50 cm");

Map.setCenter(25,-3,2);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_texture_class)


[iSDAsoil USDA Texture Class](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_texture_class)

USDA Texture Class at soil depths of 0\-20 cm and 20\-50 cm. In areas of dense jungle (generally over central Africa), model accuracy is low and therefore artifacts such as banding (striping) might be seen. Soil property predictions were made by Innovative Solutions for Decision Agriculture Ltd. (iSDA) at 30 …

 ISDASOIL/Africa/v1/texture\_class,
 africa,aluminium,isda,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








