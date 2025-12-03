



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TIGER: US Census Blocks


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2010\-01\-02T00:00:00Z
Dataset Provider


[United States Census Bureau](https://www.census.gov/programs-surveys/geography/guidance/tiger-data-products-guide.html)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("TIGER/2010/Blocks")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_Blocks)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("TIGER/2010/Blocks_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_Blocks_FeatureView)





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
a geodatabase named TIGER. This dataset contains the 2010 census
blocks, roughly equivalent to a city block. There are just over
11 million polygon features covering the United States, the District
of Columbia, Puerto Rico, and the
[Island areas](https://www.census.gov/data/tables/2010/dec/2010-island-areas.html).


For full technical details on all TIGER 2010 products, see the
[TIGER technical documentation](https://www2.census.gov/geo/pdfs/maps-data/data/tiger/tgrshp2010/TGRSHP10SF1.pdf).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| blockce | STRING | 2010 Census tabulation block number |
| blockid10 | STRING | Block identifier: a concatenation of 2010 Census state Federal Information Processing Standards (FIPS) code, county FIPS code, census tract code, and tabulation block number |
| countyfp10 | STRING | County FIPS code |
| housing10 | DOUBLE | 2010 Census number of housing units |
| partflg | STRING | Partial block flag |
| pop10 | DOUBLE | Population total as of 2010 census |
| statefp10 | STRING | 2010 Census state FIPS code |
| tractce10 | STRING | 2010 Census tract code |




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
vardataset=ee.FeatureCollection('TIGER/2010/Blocks');
varvisParams={
min:0,
max:700,
palette:['black','brown','yellow','orange','red']
};

// Turn the strings into numbers
dataset=dataset.map(function(f){
returnf.set('pop10',ee.Number.parse(f.get('pop10')));
});

varimage=ee.Image().float().paint(dataset,'pop10');

Map.setCenter(-73.99172,40.74101,13);
Map.addLayer(image,visParams,'TIGER/2010/Blocks');
Map.addLayer(dataset,null,'for Inspector',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_Blocks)
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
varfvLayer=ui.Map.FeatureViewLayer('TIGER/2010/Blocks_FeatureView');

varvisParams={
opacity:1,
color:{
property:'pop10',
mode:'linear',
palette:['black','brown','yellow','orange','red'],
min:0,
max:700
}
};

fvLayer.setVisParams(visParams);
fvLayer.setName('US census blocks');

Map.setCenter(-73.99172,40.74101,13);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_Blocks_FeatureView)


[TIGER: US Census Blocks](/earth-engine/datasets/catalog/TIGER_2010_Blocks)

The United States Census Bureau regularly releases a geodatabase named TIGER. This dataset contains the 2010 census blocks, roughly equivalent to a city block. There are just over 11 million polygon features covering the United States, the District of Columbia, Puerto Rico, and the Island areas. For full technical details …

 TIGER/2010/Blocks,
 census,city,infrastructure\-boundaries,neighborhood,table,tiger,urban,us

2010\-01\-01T00:00:00Z/2010\-01\-02T00:00:00Z



 \-14\.69 \-180 71\.567 \-64\.435
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








