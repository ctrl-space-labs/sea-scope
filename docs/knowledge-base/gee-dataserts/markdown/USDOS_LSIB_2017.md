



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

LSIB 2017: Large Scale International Boundary Polygons, Detailed


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================================








Dataset Availability
2017\-12\-29T00:00:00Z–2017\-12\-29T00:00:00Z
Dataset Provider


[United States Department of State, Office of the Geographer](https://geonode.state.gov/layers/catalog:geonode:LSIB)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("USDOS/LSIB/2017")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USDOS/USDOS_LSIB_2017)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("USDOS/LSIB/2017_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USDOS/USDOS_LSIB_2017_FeatureView)





Tags


[borders](/earth-engine/datasets/tags/borders)
[countries](/earth-engine/datasets/tags/countries)
[dos](/earth-engine/datasets/tags/dos)
[infrastructure\-boundaries](/earth-engine/datasets/tags/infrastructure-boundaries)
[political](/earth-engine/datasets/tags/political)
[table](/earth-engine/datasets/tags/table)
[usdos](/earth-engine/datasets/tags/usdos)








#### Description



The United States Office of the Geographer provides
the Large Scale International Boundary (LSIB) dataset. It is derived
from two other datasets: a LSIB line vector file and the World
Vector Shorelines (WVS) from the National Geospatial\-Intelligence
Agency (NGA). The interior boundaries reflect U.S. government policies
on boundaries, boundary disputes, and sovereignty. The exterior
boundaries are derived from the WVS; however, the WVS coastline
data is outdated and generally shifted from between several hundred
meters to over a kilometer. Each feature is the polygonal area
enclosed by interior boundaries and exterior coastlines where applicable,
and many countries consist of multiple features, one per disjoint
region. Each of the 180,741 features is a part of the geometry
of one of the 284 countries described in this dataset.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| OBJECTID | STRING | Object ID |
| COUNTRY\_NA | STRING | US\-recognized country name |




### Terms of Use


**Terms of Use**


There are no restrictions on use of this US public domain data.




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('USDOS/LSIB/2017');
varstyleParams={
fillColor:'b5ffb4',
color:'00909F',
width:3,
};
varcountries=dataset.style(styleParams);
Map.setCenter(16.35,48.83,4);
Map.addLayer(countries,{},'USDOS/LSIB/2017',true,0.8);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USDOS/USDOS_LSIB_2017)
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
varfvLayer=ui.Map.FeatureViewLayer('USDOS/LSIB/2017_FeatureView');

varvisParams={
color:'00909F',
fillColor:'b5ffb4',
width:3,
opacity:1
};

fvLayer.setVisParams(visParams);
fvLayer.setName('USDOS/LSIB/2017');

Map.setCenter(16.35,48.83,4);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USDOS/USDOS_LSIB_2017_FeatureView)


[LSIB 2017: Large Scale International Boundary Polygons, Detailed](/earth-engine/datasets/catalog/USDOS_LSIB_2017)

The United States Office of the Geographer provides the Large Scale International Boundary (LSIB) dataset. It is derived from two other datasets: a LSIB line vector file and the World Vector Shorelines (WVS) from the National Geospatial\-Intelligence Agency (NGA). The interior boundaries reflect U.S. government policies on boundaries, boundary disputes, …

 USDOS/LSIB/2017,
 borders,countries,dos,infrastructure\-boundaries,political,table,usdos

2017\-12\-29T00:00:00Z/2017\-12\-29T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








