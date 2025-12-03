



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Open Buildings V3 Polygons


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================








Dataset Availability
2023\-05\-30T00:00:00Z–2023\-05\-30T00:00:00Z
Dataset Provider


[Google Research \- Open Buildings](https://sites.research.google/open-buildings/)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("GOOGLE/Research/open-buildings/v3/polygons")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_Research_open-buildings_v3_polygons)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("GOOGLE/Research/open-buildings/v3/polygons_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_Research_open-buildings_v3_polygons_FeatureView)





Tags


[africa](/earth-engine/datasets/tags/africa)
[asia](/earth-engine/datasets/tags/asia)
[building](/earth-engine/datasets/tags/building)
[built\-up](/earth-engine/datasets/tags/built-up)
[open\-buildings](/earth-engine/datasets/tags/open-buildings)
[population](/earth-engine/datasets/tags/population)
[south\-asia](/earth-engine/datasets/tags/south-asia)
[southeast\-asia](/earth-engine/datasets/tags/southeast-asia)
[table](/earth-engine/datasets/tags/table)
structure








#### Description



This large\-scale open dataset consists of outlines of buildings derived
from high\-resolution 50 cm satellite imagery. It contains 1\.8B building
detections in Africa, Latin America, Caribbean, South Asia and Southeast
Asia. The inference spanned an area of 58M km².


For each building in this dataset we include the polygon describing its
footprint on the ground, a confidence score indicating how sure we are that
this is a building, and a [Plus Code](https://plus.codes/) corresponding to
the center of the building. There is no information about the type of
building, its street address, or any details other than its geometry.


Building footprints are useful for a range of important applications: from
population estimation, urban planning and humanitarian response to
environmental and climate science. The project is based in Ghana, with an
initial focus on the continent of Africa and new updates on South Asia,
South\-East Asia, Latin America and the Caribbean.


Inference was carried out during May 2023\.


For more details see the official
[website](https://sites.research.google/open-buildings/) of the Open
Buildings dataset.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| area\_in\_meters | DOUBLE | Area in square meters of the polygon. |
| confidence | DOUBLE | Confidence score \[0\.65;1\.0] assigned by the model. |
| full\_plus\_code | STRING | The full [Plus Code](https://plus.codes/) at the building polygon centroid. |
| longitude\_latitude | GEOMETRY | Centroid of the polygon. |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* W. Sirko, S. Kashubin, M. Ritter, A. Annkah, Y.S.E. Bouchareb, Y. Dauphin,
D. Keysers, M. Neumann, M. Cisse, J.A. Quinn. Continental\-scale building
detection from high resolution satellite imagery.
[arXiv:2107\.12283](https://arxiv.org/abs/2107.12283), 2021\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Visualization of GOOGLE/Research/open-buildings/v3/polygons.

vart=ee.FeatureCollection('GOOGLE/Research/open-buildings/v3/polygons');

vart_065_070=t.filter('confidence >= 0.65 && confidence < 0.7');
vart_070_075=t.filter('confidence >= 0.7 && confidence < 0.75');
vart_gte_075=t.filter('confidence >= 0.75');

Map.addLayer(t_065_070,{color:'FF0000'},'Buildings confidence [0.65; 0.7)');
Map.addLayer(t_070_075,{color:'FFFF00'},'Buildings confidence [0.7; 0.75)');
Map.addLayer(t_gte_075,{color:'00FF00'},'Buildings confidence >= 0.75');
Map.setCenter(3.389,6.492,17);// Lagos, Nigeria
Map.setOptions('SATELLITE');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_Research_open-buildings_v3_polygons)
### Visualize as a FeatureView



 A `FeatureView` is a view\-only, accelerated representation of a
 `FeatureCollection`. For more details, visit the
 [`FeatureView` documentation.](/earth-engine/guides/featureview_overview) 



**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varfvLayer=ui.Map.FeatureViewLayer(
'GOOGLE/Research/open-buildings/v3/polygons_FeatureView');

varvisParams={
rules:[
{
filter:ee.Filter.expression('confidence >= 0.65 && confidence < 0.7'),
color:'FF0000'
},
{
filter:ee.Filter.expression('confidence >= 0.7 && confidence < 0.75'),
color:'FFFF00'
},
{
filter:ee.Filter.expression('confidence >= 0.75'),
color:'00FF00'
},
]
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Buildings');

Map.setCenter(3.389,6.492,17);// Lagos, Nigeria
Map.add(fvLayer);
Map.setOptions('SATELLITE');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_Research_open-buildings_v3_polygons_FeatureView)


[Open Buildings V3 Polygons](/earth-engine/datasets/catalog/GOOGLE_Research_open-buildings_v3_polygons)

This large\-scale open dataset consists of outlines of buildings derived from high\-resolution 50 cm satellite imagery. It contains 1\.8B building detections in Africa, Latin America, Caribbean, South Asia and Southeast Asia. The inference spanned an area of 58M km². For each building in this dataset we include the polygon describing …

 GOOGLE/Research/open\-buildings/v3/polygons,
 africa,asia,building,built\-up,open\-buildings,population,south\-asia,southeast\-asia,table

2023\-05\-30T00:00:00Z/2023\-05\-30T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








