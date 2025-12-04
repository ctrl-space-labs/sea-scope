



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Forest proximate people (FPP) 1\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================








Dataset Availability
2019\-01\-01T00:00:00Z–2019\-01\-01T00:00:00Z
Dataset Provider


[FAO Forestry Division (FPP 1km)](https://data.apps.fao.org/catalog/iso/8ed893bd-842a-4866-a655-a0a0c02b79b4)


[FAO Forestry Division (FPP 5km)](https://data.apps.fao.org/catalog/iso/8ed893bd-842a-4866-a655-a0a0c02b79b5)



Earth Engine Snippet


`ee.ImageCollection("FAO/SOFO/1/FPP")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/FAO/FAO_SOFO_1_FPP)





Cadence
1 Year
Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[fao](/earth-engine/datasets/tags/fao)
[forest](/earth-engine/datasets/tags/forest)
[global](/earth-engine/datasets/tags/global)
[plant\-productivity](/earth-engine/datasets/tags/plant-productivity)
[population](/earth-engine/datasets/tags/population)
[rural\-area](/earth-engine/datasets/tags/rural-area)








#### Description



The "Forest Proximate People" (FPP) dataset is one of the data layers
contributing to the development of indicator \#13, "number of
forest\-dependent people in extreme poverty," of the Collaborative
Partnership on Forests (CPF) Global Core Set of forest\-related
indicators (GCS). The FPP dataset provides an estimate of the number of
people living in or within 1 kilometer of forests
(forest\-proximate people) for the year 2019 with a pixel size of 100 meters
at a global level.
[Find out more about the dataset.](https://data.apps.fao.org/catalog/dcat/forest-proximate-people)





### Bands



**Pixel Size**
  
0\.0009 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `FPP_1km` | Number of people/ha | Number of people living in or within 1 kilometer of forests. |
| `FPP_5km` | Number of people/ha | Number of people living in or within 5 kilometer of forests. |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* FAO 2022\. The State of the World's Forests (SOFO) \- Forest pathways for
green recovery and building inclusive, resilient and sustainable
economies. FAO, Rome.
<https://www.fao.org/documents/card/en/c/cb9360en>
* Newton, P., Castle, S.E., Kinzer, A.T., Miller, D.C., Oldekop, J.A.,
Linhares\-Juvenal, T., Pina, L., Madrid, M., \& de Lamo, J. 2022\. The
number of forest\- and tree\-proximate people: a new methodology and
global estimates, One Earth, 2020
[doi:10\.1016/j.oneear.2020\.08\.016](https://doi.org/10.1016/j.oneear.2020.08.016),





### DOIs


* [https://doi.org/10\.1016/j.oneear.2020\.08\.016](https://doi.org/10.1016/j.oneear.2020.08.016)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcoll=ee.ImageCollection('FAO/SOFO/1/FPP');
varimage=coll.first().select('FPP_1km');
Map.setCenter(17.5,20,3);
Map.addLayer(
image,{min:0,max:12,palette:['blue','yellow','red']},
'Forest proximate people – 1km cutoff distance');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/FAO/FAO_SOFO_1_FPP)


[Forest proximate people (FPP) 1\.0](/earth-engine/datasets/catalog/FAO_SOFO_1_FPP)

The "Forest Proximate People" (FPP) dataset is one of the data layers contributing to the development of indicator \#13, "number of forest\-dependent people in extreme poverty," of the Collaborative Partnership on Forests (CPF) Global Core Set of forest\-related indicators (GCS). The FPP dataset provides an estimate of the number of …

 FAO/SOFO/1/FPP,
 agriculture,fao,forest,global,plant\-productivity,population,rural\-area

2019\-01\-01T00:00:00Z/2019\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1016/j.oneear.2020\.08\.016](https://doi.org/https://data.apps.fao.org/catalog/iso/8ed893bd-842a-4866-a655-a0a0c02b79b4)
* [https://doi.org/10\.1016/j.oneear.2020\.08\.016](https://doi.org/https://data.apps.fao.org/catalog/iso/8ed893bd-842a-4866-a655-a0a0c02b79b5)
* [https://doi.org/10\.1016/j.oneear.2020\.08\.016](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/FAO_SOFO_1_FPP)









