



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TIGER: 2020 Tabulation (Census) Block


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================








Dataset Availability
2020\-01\-01T00:00:00Z–2020\-01\-02T00:00:00Z
Dataset Provider


[United States Census Bureau](https://www.census.gov/programs-surveys/geography/guidance/tiger-data-products-guide.html)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("TIGER/2020/TABBLOCK20")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2020_TABBLOCK20)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("TIGER/2020/TABBLOCK20_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2020_TABBLOCK20_FeatureView)





Tags


[census](/earth-engine/datasets/tags/census)
[city](/earth-engine/datasets/tags/city)
[infrastructure\-boundaries](/earth-engine/datasets/tags/infrastructure-boundaries)
[neighborhood](/earth-engine/datasets/tags/neighborhood)
[table](/earth-engine/datasets/tags/table)
[tiger](/earth-engine/datasets/tags/tiger)
[urban](/earth-engine/datasets/tags/urban)
[us](/earth-engine/datasets/tags/us)








#### Description



The United States Census Bureau regularly releases
a geodatabase named TIGER. This dataset contains the 2020 census
blocks, roughly equivalent to a city block. There are just over
eight million polygon features covering the United States, the District
of Columbia, Puerto Rico, and the
[Island areas](https://www.census.gov/programs-surveys/decennial-census/decade/2020/planning-management/release/2020-island-areas-data-products.html).


For full technical details on all TIGER 2020 products, see the
[TIGER technical documentation](https://www2.census.gov/geo/pdfs/maps-data/data/tiger/tgrshp2020/TGRSHP2020_TechDoc.pdf).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| ALAND20 | DOUBLE | 2020 Census land area |
| AWATER20 | DOUBLE | 2020 Census water area |
| BLOCKCE20 | STRING | 2020 Census tabulation block number |
| COUNTYFP20 | STRING | 2020 Census county FIPS code |
| FUNCSTAT20 | STRING | 2020 Census functional status |
| GEOID20 | STRING | Census block identifier: a concatenation of 2020 Census state FIPS code, 2020 Census county FIPS code, 2020 Census tract code, and 2020 Census block number |
| INTPTLAT20 | STRING | 2020 Census latitude of the internal point |
| INTPTLON20 | STRING | 2020 Census longitude of the internal point |
| MTFCC20 | STRING | MAF/TIGER feature class code |
| NAME20 | STRING | 2020 Census tabulation block name: a concatenation of Block and the tabulation block number |
| STATEFP20 | STRING | 2020 Census state FIPS code |
| TRACTCE20 | STRING | 2020 Census tract code |
| UACE20 | STRING | 2020 Census urban area code |
| UATYPE20 | STRING | 2020 Census urban area type |
| UR20 | STRING | 2020 Census urban/rural indicator |




### Terms of Use


**Terms of Use**


The U.S. Census Bureau offers some of its public data
in machine\-readable format via an Application Programming Interface
(API). All of the content, documentation, code and related materials
made available to you through the API are subject to [these terms and
conditions](https://www.census.gov/data/developers/about/terms-of-service.html).




### Citations



Citations:
* For the creation of any reports, publications, new data sets, derived
products, or services resulting from the data set, users should
[cite the US Census Bureau](https://www.census.gov/about/policies/citation.html).





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('TIGER/2020/TABBLOCK20');

varvisParams={
min:0.0,
max:1e7,
palette:['d8d9d9','aaaaaa','b6dfe9','2ea3f2','0c71c3']
};

// plotting the water area per polygon
dataset=dataset.map(function(f){
returnf.set('AWATER20',ee.Number.parse(f.get('AWATER20')));
});

varimage=ee.Image().float().paint(dataset,'AWATER20');

Map.setCenter(-73.15,40.9,9);
Map.addLayer(ee.Image(1),{min:0,max:1},'background');
Map.addLayer(image,visParams,'TIGER/2020/TABBLOCK20');
Map.addLayer(dataset,null,'for Inspector',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2020_TABBLOCK20)
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
varfvLayer=ui.Map.FeatureViewLayer('TIGER/2020/TABBLOCK20_FeatureView');

varvisParams={
opacity:1,
color:{
property:'AWATER20',
mode:'linear',
palette:['d8d9d9','aaaaaa','b6dfe9','2ea3f2','0c71c3'],
min:0,
max:1e7
}
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Water area by US census block');

Map.setCenter(-73.15,40.9,9);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2020_TABBLOCK20_FeatureView)


[TIGER: 2020 Tabulation (Census) Block](/earth-engine/datasets/catalog/TIGER_2020_TABBLOCK20)

The United States Census Bureau regularly releases a geodatabase named TIGER. This dataset contains the 2020 census blocks, roughly equivalent to a city block. There are just over eight million polygon features covering the United States, the District of Columbia, Puerto Rico, and the Island areas. For full technical details …

 TIGER/2020/TABBLOCK20,
 census,city,infrastructure\-boundaries,neighborhood,table,tiger,urban,us

2020\-01\-01T00:00:00Z/2020\-01\-02T00:00:00Z



 \-14\.69 \-180 71\.567 \-64\.435
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








