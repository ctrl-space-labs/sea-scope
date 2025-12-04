



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Finland NRG NLS orthophotos 50 cm by Mavi


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================================








Dataset Availability
2015\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[NLS orthophotos](https://www.maanmittauslaitos.fi/en/maps-and-spatial-data/expert-users/product-descriptions/orthophotos)



Earth Engine Snippet


`ee.ImageCollection("Finland/MAVI/VV/50cm")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Finland/Finland_MAVI_VV_50cm)





Tags


[falsecolor](/earth-engine/datasets/tags/falsecolor)
[finland](/earth-engine/datasets/tags/finland)
[nrg](/earth-engine/datasets/tags/nrg)
[orthophotos](/earth-engine/datasets/tags/orthophotos)
mavi








#### Description



NLS Orthophotos are an aerial photo dataset covering the whole of Finland.
This data is provided by [Mavi(Agency for Rural Affairs)](https://maaseutuverkosto.fi/en/).
An orthophoto is a combination of several individual aerial photos. The
aerial photo dataset in orthophoto format is available as the most recent
dataset consisting of the most recent aerial photos available. The most
recent data is usually 1\-3 years old. NLS Orthophotos are updated every
3 years (in Northern Lapland 12 years).


In these images, the bands are near\-infrared, red, and green.


(In Dataset id, VV stands for "vääräväri", false color)
For more information, please see the
[NLS orthophotos documentation](https://www.maanmittauslaitos.fi/en/maps-and-spatial-data/expert-users/product-descriptions/orthophotos)





### Bands



**Pixel Size**
  
0\.5 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `N` | 0 | 255 | Near\-Infrared |
| `R` | 0 | 255 | Red |
| `G` | 0 | 255 | Green |




### Terms of Use


**Terms of Use**


Mention the name of the Licensor (the National Land Survey of Finland),
the name of the dataset(s) and the time when the National Land Survey has
delivered the dataset(s) (e.g.: contains data from the National Land Survey
of Finland Topographic Database 06/2014\).
please see the [Terms of use](https://creativecommons.org/licenses/by/4.0/)




### Citations



Citations:
* The National Land Survey of Finland





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('Finland/MAVI/VV/50cm');

Map.setCenter(25.7416,62.2446,16);
Map.addLayer(dataset,null,'Finland 50 cm(false color)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Finland/Finland_MAVI_VV_50cm)


[Finland NRG NLS orthophotos 50 cm by Mavi](/earth-engine/datasets/catalog/Finland_MAVI_VV_50cm)

NLS Orthophotos are an aerial photo dataset covering the whole of Finland. This data is provided by Mavi(Agency for Rural Affairs). An orthophoto is a combination of several individual aerial photos. The aerial photo dataset in orthophoto format is available as the most recent dataset consisting of the most recent …

 Finland/MAVI/VV/50cm,
 falsecolor,finland,nrg,orthophotos

2015\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 59 18 69\.4 29\.2
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








