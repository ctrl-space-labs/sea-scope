



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

SWISSIMAGE 10 cm RGB imagery


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================








Dataset Availability
2017\-01\-01T00:00:00Z–2021\-01\-01T00:00:00Z
Dataset Provider


[Topography swisstopo](https://www.swisstopo.admin.ch/en/geodata/images/ortho/swissimage10.html)



Earth Engine Snippet


`ee.ImageCollection("Switzerland/SWISSIMAGE/orthos/10cm")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Switzerland/Switzerland_SWISSIMAGE_orthos_10cm)





Tags


[orthophotos](/earth-engine/datasets/tags/orthophotos)
[rgb](/earth-engine/datasets/tags/rgb)
swissimage
swisstopo








#### Description



The SWISSIMAGE 10 cm orthophoto mosaic is an assembly of new color digital
aerial images over the whole of Switzerland with a ground resolution of
10 cm in the plains and the main alpine valleys and 25 cm in the Alps. It
is updated annually.


For more information, please see the
[SWISSIMAGE10cm\_FR documentation](https://backend.swisstopo.admin.ch/fileservice/sdweb-docs-prod-swisstopoch-files/files/2023/11/14/a84642dc-5feb-48e5-af6b-55df4ae7a10b.pdf)


This RGB collection contains digital aerial images with three bands.
Standard deviation for the precision in position: \+/\- 0\.15 m for the ground
sample distance of 0\.1 m.





### Bands



**Pixel Size**
  
0\.1 meters



**Bands**




| Name | Min | Max | Wavelength | Description |
| --- | --- | --- | --- | --- |
| `R` | 0 | 255 | 619\-651nm | Red |
| `G` | 0 | 255 | 525\-585nm | Green |
| `B` | 0 | 255 | 435\-495nm | Blue |




### Terms of Use


**Terms of Use**


The free geodata and geoservices of swisstopo may be used, distributed and
made accessible. Furthermore, they may be enriched and processed and also
used commercially.


A reference to the source is mandatory.
please see the [Terms of use](https://www.swisstopo.admin.ch/en/terms-and-conditions)




### Citations



Citations:
* Copyright Federal Office of Topography swisstopo





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('Switzerland/SWISSIMAGE/orthos/10cm/2017');

Map.setCenter(7.75,46.02,18);
Map.addLayer(dataset,null,'Switzerland RGB (10 cm)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Switzerland/Switzerland_SWISSIMAGE_orthos_10cm)


[SWISSIMAGE 10 cm RGB imagery](/earth-engine/datasets/catalog/Switzerland_SWISSIMAGE_orthos_10cm)

The SWISSIMAGE 10 cm orthophoto mosaic is an assembly of new color digital aerial images over the whole of Switzerland with a ground resolution of 10 cm in the plains and the main alpine valleys and 25 cm in the Alps. It is updated annually. For more information, please see …

 Switzerland/SWISSIMAGE/orthos/10cm,
 orthophotos,rgb

2017\-01\-01T00:00:00Z/2021\-01\-01T00:00:00Z



 45\.8 5\.9 47\.8 10\.6
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








