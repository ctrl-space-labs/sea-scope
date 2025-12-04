



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TUBerlin/BigEarthNet/v1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================








Dataset Availability
2017\-06\-01T00:00:00Z–2018\-05\-31T00:00:00Z
Dataset Provider


[BigEarthNet](http://bigearth.net/)



Earth Engine Snippet


`ee.ImageCollection("TUBerlin/BigEarthNet/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TUBerlin/TUBerlin_BigEarthNet_v1)





Tags


[copernicus](/earth-engine/datasets/tags/copernicus)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[sentinel](/earth-engine/datasets/tags/sentinel)
chip
corine\-derived
label
ml
tile








#### Description



BigEarthNet is a new large\-scale Sentinel\-2 benchmark archive, consisting of
590,326 Sentinel\-2 image patches. To construct BigEarthNet, 125 Sentinel\-2
tiles were acquired between June 2017 and May 2018 over the 10 countries
(Austria, Belgium, Finland, Ireland, Kosovo, Lithuania, Luxembourg,
Portugal, Serbia, Switzerland) of Europe. All the tiles were atmospherically
corrected by the Sentinel\-2 Level 2A product generation and formatting tool
(sen2cor). Then, they were divided into 590,326 non\-overlapping image
patches. Each image patch was annotated by the multiple land\-cover classes
(i.e., multi\-labels) that were provided from the CORINE Land Cover database
of the year 2018 (CLC 2018\).





### Bands


**Bands**




| Name | Scale | Pixel Size | Wavelength | Description |
| --- | --- | --- | --- | --- |
| `B1` | 0\.0001 | 443\.9nm (S2A) / 442\.3nm (S2B) | Aerosols |
| `B2` | 0\.0001 | 496\.6nm (S2A) / 492\.1nm (S2B) | Blue |
| `B3` | 0\.0001 | 560nm (S2A) / 559nm (S2B) | Green |
| `B4` | 0\.0001 | 664\.5nm (S2A) / 665nm (S2B) | Red |
| `B5` | 0\.0001 | 703\.9nm (S2A) / 703\.8nm (S2B) | Red Edge 1 |
| `B6` | 0\.0001 | 740\.2nm (S2A) / 739\.1nm (S2B) | Red Edge 2 |
| `B7` | 0\.0001 | 782\.5nm (S2A) / 779\.7nm (S2B) | Red Edge 3 |
| `B8` | 0\.0001 | 835\.1nm (S2A) / 833nm (S2B) | NIR |
| `B9` | 0\.0001 | 945nm (S2A) / 943\.2nm (S2B) | Water vapor |
| `B10` | 0\.0001 | 1373\.5nm (S2A) / 1376\.9nm (S2B) | Cirrus |
| `B11` | 0\.0001 | 1613\.7nm (S2A) / 1610\.4nm (S2B) | SWIR 1 |
| `B12` | 0\.0001 | 2202\.4nm (S2A) / 2185\.7nm (S2B) | SWIR 2 |
| `B8A` | 0\.0001 | 864\.8nm (S2A) / 864nm (S2B) | Red Edge 4 |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| labels | STRING\_LIST | List of landcover types found in this image |
| source | STRING | Product ID of the corresponding Sentinel\-2 1C image |
| tile\_x | DOUBLE | X coordinate of tile in source image |
| tile\_y | DOUBLE | Y coordinate of tile in source image |




### Terms of Use


**Terms of Use**


The BigEarthNet Archive is licensed under the Community Data License
Agreement \- Permissive, Version 1\.0\. For more information,
please refer to
[https://cdla.dev/permissive\-1\-0](https://cdla.dev/permissive-1-0/).




### Citations



Citations:
* G. Sumbul, M. Charfuelan, B. Demir, V. Markl, BigEarthNet: A Large\-Scale
Benchmark Archive for Remote Sensing Image Understanding, IEEE International
Conference on Geoscience and Remote Sensing Symposium, pp. 5901\-5904,
Yokohama, Japan, 2019\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vargeometry=ee.Geometry.Polygon(
[[
[16.656886757418057,48.27086673747943],
[16.656886757418057,48.21359065567954],
[16.733276070162198,48.21359065567954],
[16.733276070162198,48.27086673747943]]]);

varic=ee.ImageCollection('TUBerlin/BigEarthNet/v1');

varfiltered=ic.filterBounds(geometry);

vartiles=filtered.map(function(image){
varlabels=ee.List(image.get('labels'));

varurban=labels.indexOf('Discontinuous urban fabric').gte(0);
varhighlight_urban=ee.Image(urban).toInt().multiply(1000);

returnimage.addBands(
{srcImg:image.select(['B4']).add(highlight_urban),overwrite:true});
});

varimage=tiles.mosaic().clip(geometry);

varvisParams={bands:['B4','B3','B2'],min:0,max:3000};

Map.addLayer(image,visParams);
Map.centerObject(image,13);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TUBerlin/TUBerlin_BigEarthNet_v1)


[TUBerlin/BigEarthNet/v1](/earth-engine/datasets/catalog/TUBerlin_BigEarthNet_v1)

BigEarthNet is a new large\-scale Sentinel\-2 benchmark archive, consisting of 590,326 Sentinel\-2 image patches. To construct BigEarthNet, 125 Sentinel\-2 tiles were acquired between June 2017 and May 2018 over the 10 countries (Austria, Belgium, Finland, Ireland, Kosovo, Lithuania, Luxembourg, Portugal, Serbia, Switzerland) of Europe. All the tiles were atmospherically corrected …

 TUBerlin/BigEarthNet/v1,
 copernicus,landuse\-landcover,sentinel

2017\-06\-01T00:00:00Z/2018\-05\-31T00:00:00Z



 36\.9 \-9 68\.1 31\.6
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








