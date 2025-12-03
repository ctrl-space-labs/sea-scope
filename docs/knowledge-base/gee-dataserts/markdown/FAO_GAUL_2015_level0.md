



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

FAO GAUL: Global Administrative Unit Layers 2015, Country Boundaries


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================================








Dataset Availability
2014\-12\-19T16:45:00Z–2014\-12\-19T16:45:00Z
Dataset Provider


[FAO UN](https://www.fao.org/geonetwork/srv/en/metadata.show?id=12691)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("FAO/GAUL/2015/level0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/FAO/FAO_GAUL_2015_level0)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("FAO/GAUL/2015/level0_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/FAO/FAO_GAUL_2015_level0_FeatureView)





Tags


[borders](/earth-engine/datasets/tags/borders)
[countries](/earth-engine/datasets/tags/countries)
[fao](/earth-engine/datasets/tags/fao)
[gaul](/earth-engine/datasets/tags/gaul)
[infrastructure\-boundaries](/earth-engine/datasets/tags/infrastructure-boundaries)
[table](/earth-engine/datasets/tags/table)
[un](/earth-engine/datasets/tags/un)








#### Description



The Global Administrative Unit Layers (GAUL) compiles and disseminates the
best available information on administrative units for all the countries in
the world, providing a contribution to the standardization of the spatial
dataset representing administrative units. The GAUL always maintains global
layers with a unified coding system at country, first (e.g. departments),
and second administrative levels (e.g. districts). Where data is available,
it provides layers on a country by country basis down to third, fourth, and
lowers levels. The overall methodology consists in a) collecting the best
available data from most reliable sources, b) establishing validation
periods of the geographic features (when possible), c) adding selected data
to the global layer based on the last country boundaries map provided by
the UN Cartographic Unit (UNCS), d) generating codes using GAUL Coding
System, and e) distribute data to the users
(see [Technical Aspects of the GAUL Distribution Set](https://data.apps.fao.org:/map/catalog/srv/api/records/9c35ba10-5649-41c8-bdfc-eb78e9e65654/attachments/GAUL2015_Documentation.zip).
Note that some administrative units are multipolygon features.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| ADM0\_CODE | INT | GAUL country code |
| ADM0\_NAME | STRING | UN country name |
| DISP\_AREA | STRING | Unsettled territory: 'Yes' or 'No' |
| STATUS | STRING | Status of the country |
| Shape\_Area | DOUBLE | Shape area |
| Shape\_Leng | DOUBLE | Shape length |
| EXP0\_YEAR | INT | Expiry year of the administrative unit |
| STR0\_YEAR | INT | Creation year of the administrative unit |




### Terms of Use


**Terms of Use**


The GAUL dataset is distributed to the United Nations and other authorized
international and national institutions/agencies. FAO grants a license to
use, download and print the materials contained in the GAUL dataset solely
for non\-commercial purposes and in accordance with the conditions specified
in the data license. [The full GAUL Data License
document](https://developers.google.com/earth-engine/datasets/catalog/DataLicenseGAUL2015.pdf)
is available for downloading. See also [the
disclaimer](https://developers.google.com/earth-engine/datasets/catalog/DisclaimerGAUL2015.pdf).




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('FAO/GAUL/2015/level0');

Map.setCenter(7.82,49.1,4);

varstyleParams={
fillColor:'b5ffb4',
color:'00909F',
width:1.0,
};

dataset=dataset.style(styleParams);

Map.addLayer(dataset,{},'Country Boundaries');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/FAO/FAO_GAUL_2015_level0)
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
varfvLayer=ui.Map.FeatureViewLayer('FAO/GAUL/2015/level0_FeatureView');

varvisParams={
color:'00909F',
fillColor:'b5ffb4',
opacity:1,
width:1,
pointSize:1
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Country Boundaries');

Map.setCenter(7.82,49.1,4);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/FAO/FAO_GAUL_2015_level0_FeatureView)


[FAO GAUL: Global Administrative Unit Layers 2015, Country Boundaries](/earth-engine/datasets/catalog/FAO_GAUL_2015_level0)

The Global Administrative Unit Layers (GAUL) compiles and disseminates the best available information on administrative units for all the countries in the world, providing a contribution to the standardization of the spatial dataset representing administrative units. The GAUL always maintains global layers with a unified coding system at country, first …

 FAO/GAUL/2015/level0,
 borders,countries,fao,gaul,infrastructure\-boundaries,table,un

2014\-12\-19T16:45:00Z/2014\-12\-19T16:45:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








