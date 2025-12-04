



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

ESA WorldCover 10m v200


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================








Dataset Availability
2021\-01\-01T00:00:00Z–2022\-01\-01T00:00:00Z
Dataset Provider


[ESA WorldCover Consortium](https://esa-worldcover.org/en)



Earth Engine Snippet


`ee.ImageCollection("ESA/WorldCover/v200")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ESA/ESA_WorldCover_v200)





Tags


[esa](/earth-engine/datasets/tags/esa)
[landcover](/earth-engine/datasets/tags/landcover)
[landuse](/earth-engine/datasets/tags/landuse)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[sentinel1\-derived](/earth-engine/datasets/tags/sentinel1-derived)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)








#### Description



The European Space Agency (ESA) WorldCover 10 m 2021 product provides a
global land cover map for 2021 at 10 m resolution based on Sentinel\-1 and
Sentinel\-2 data.
 The WorldCover product comes with 11 land cover classes and has been
generated in the framework of the ESA WorldCover project, part of the
5th Earth Observation Envelope Programme (EOEP\-5\) of the European Space
Agency.


See also:


* [ESA WorldCover website](https://esa-worldcover.org)
* [User Manual and Validation Report](https://esa-worldcover.org/en/data-access)





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Description |
| --- | --- |
| `Map` | Landcover class |


**Map Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 10 | \#006400 | Tree cover |
| 20 | \#ffbb22 | Shrubland |
| 30 | \#ffff4c | Grassland |
| 40 | \#f096ff | Cropland |
| 50 | \#fa0000 | Built\-up |
| 60 | \#b4b4b4 | Bare / sparse vegetation |
| 70 | \#f0f0f0 | Snow and ice |
| 80 | \#0064c8 | Permanent water bodies |
| 90 | \#0096a0 | Herbaceous wetland |
| 95 | \#00cf75 | Mangroves |
| 100 | \#fae6a0 | Moss and lichen |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Zanaga, D., Van De Kerchove, R., Daems, D., De Keersmaecker, W., Brockmann,
C., Kirches, G., Wevers, J., Cartus, O., Santoro, M., Fritz, S., Lesiv, M.,
Herold, M., Tsendbazar, N.E., Xu, P., Ramoino, F., Arino, O., 2022\. ESA
WorldCover 10 m 2021 v200\.
([doi:10\.5281/zenodo.7254221](https://doi.org/10.5281/zenodo.7254221))





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('ESA/WorldCover/v200').first();

varvisualization={
bands:['Map'],
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Landcover');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ESA/ESA_WorldCover_v200)


[ESA WorldCover 10m v200](/earth-engine/datasets/catalog/ESA_WorldCover_v200)

The European Space Agency (ESA) WorldCover 10 m 2021 product provides a global land cover map for 2021 at 10 m resolution based on Sentinel\-1 and Sentinel\-2 data. The WorldCover product comes with 11 land cover classes and has been generated in the framework of the ESA WorldCover project, part …

 ESA/WorldCover/v200,
 esa,landcover,landuse,landuse\-landcover,sentinel1\-derived,sentinel2\-derived

2021\-01\-01T00:00:00Z/2022\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








