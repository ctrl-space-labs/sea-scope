



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Latvia Color InfraRed (CIR) orthophotos


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================








Dataset Availability
2007\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[Latvia orthophotos](https://www.lgia.gov.lv/lv/ortofotokartes-1)



Earth Engine Snippet


`ee.ImageCollection("Latvia/Maamet/orthos/cir")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Latvia/Latvia_Maamet_orthos_cir)





Tags


[latvia](/earth-engine/datasets/tags/latvia)
[nrg](/earth-engine/datasets/tags/nrg)
[orthophotos](/earth-engine/datasets/tags/orthophotos)








#### Description



In Latvia, orthophoto maps are prepared in the Latvian coordinate system
LKS\-92 TM according to the TKS\-93 map sheet division (scale 1:10000 map
sheet corresponds to 5 x 5 kilometers in nature). Orthophoto maps are
prepared for the whole territory of Latvia at the scale of 1:10000, but for
separate territories \- for cities and densely populated areas \- at the scale
of 1:2000 or 1:1000\.


The CIR dataset has three bands: Near\-Infrared, Red, and Green.


For more information, please see the
[Latvia orthophotos documentation](https://www.lgia.gov.lv/lv/ortofotokartes-1)





### Bands



**Pixel Size**
  
0\.2 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `N` | dn | 0 | 255 | Near\-Infrared |
| `R` | dn | 0 | 255 | Red |
| `G` | dn | 0 | 255 | Green |




### Terms of Use


**Terms of Use**


For more details please see the
[Terms of use](https://www.lgia.gov.lv/sites/lgia/files/document/Atverto%20datu%20licence%20CC%20BY_0.pdf)




### Citations



Citations:
* Latvijas Geospatial Information Agency





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('Latvia/Maamet/orthos/cir');

Map.setCenter(24.737,56.861,15);
Map.addLayer(dataset,null,'Latvia Maamet Color InfraRed (CIR)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Latvia/Latvia_Maamet_orthos_cir)


[Latvia Color InfraRed (CIR) orthophotos](/earth-engine/datasets/catalog/Latvia_Maamet_orthos_cir)

In Latvia, orthophoto maps are prepared in the Latvian coordinate system LKS\-92 TM according to the TKS\-93 map sheet division (scale 1:10000 map sheet corresponds to 5 x 5 kilometers in nature). Orthophoto maps are prepared for the whole territory of Latvia at the scale of 1:10000, but for separate …

 Latvia/Maamet/orthos/cir,
 latvia,nrg,orthophotos

2007\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 55\.5 20\.5 58\.5 28\.6
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








