



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TIGER: US Census Tracts Demographic \- Profile 1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2010\-01\-02T00:00:00Z
Dataset Provider


[United States Census Bureau](https://www.census.gov/programs-surveys/geography/guidance/tiger-data-products-guide.html)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("TIGER/2010/Tracts_DP1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_Tracts_DP1)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("TIGER/2010/Tracts_DP1_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_Tracts_DP1_FeatureView)





Tags


[census](/earth-engine/datasets/tags/census)
[infrastructure\-boundaries](/earth-engine/datasets/tags/infrastructure-boundaries)
[table](/earth-engine/datasets/tags/table)
[tiger](/earth-engine/datasets/tags/tiger)
[us](/earth-engine/datasets/tags/us)
demographic
human
social








#### Description



The United States Census Bureau regularly releases
a geodatabase named TIGER. This table contains the 2010 census
Demographic Profile 1 values aggregated by census tract. Tract
areas vary tremendously, but in urban areas are roughly equivalent
to a neighborhood. There are about 74,000 polygon features covering
the United States, the District of Columbia, Puerto Rico, and
the [Island areas](https://www.census.gov/data/tables/2010/dec/2010-island-areas.html).


For full technical details on all TIGER 2010 products, see
the [TIGER technical documentation](https://www2.census.gov/geo/pdfs/maps-data/data/tiger/tgrshp2010/TGRSHP10SF1.pdf).


Each tract also includes attributes with sums of the DP1
population measurements that intersect the boundary. The columns
have the same name as the shortname column in the [DP1 lookup
table](https://developers.google.com/earth-engine/tiger_2010_tract_dp1_metadata).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| aland10 | DOUBLE | Land area |
| awater10 | DOUBLE | Water area |
| geoid10 | STRING | Census tract identifier: a concatenation of state FIPS code, county FIPS code, and census tract code |
| intptlat10 | STRING | Latitude of the internal point |
| intptlon10 | STRING | Longitude of the internal point |
| namelsad10 | STRING | Legal/statistical area description and the census tract name |
| shape\_area | DOUBLE | Area in square degrees |
| shape\_leng | DOUBLE | Perimeter in degrees |




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
vardataset=ee.FeatureCollection('TIGER/2010/Tracts_DP1');
varvisParams={
min:0,
max:4000,
opacity:0.8,
};

// Turn the strings into numbers
dataset=dataset.map(function(f){
returnf.set('shape_area',ee.Number.parse(f.get('dp0010001')));
});

Map.setCenter(-103.882,43.036,8);
varimage=ee.Image().float().paint(dataset,'dp0010001');

Map.addLayer(image,visParams,'TIGER/2010/Tracts_DP1');
Map.addLayer(dataset,null,'for Inspector',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_Tracts_DP1)
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
varfvLayer=ui.Map.FeatureViewLayer('TIGER/2010/Tracts_DP1_FeatureView');

varvisParams={
opacity:0.8,
color:{
property:'dp0010001',
mode:'linear',
palette:['black','white'],
min:0,
max:4000
}
};

fvLayer.setVisParams(visParams);
fvLayer.setName('US census tracts demographics');

Map.setCenter(-103.882,43.036,8);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_Tracts_DP1_FeatureView)


[TIGER: US Census Tracts Demographic \- Profile 1](/earth-engine/datasets/catalog/TIGER_2010_Tracts_DP1)

The United States Census Bureau regularly releases a geodatabase named TIGER. This table contains the 2010 census Demographic Profile 1 values aggregated by census tract. Tract areas vary tremendously, but in urban areas are roughly equivalent to a neighborhood. There are about 74,000 polygon features covering the United States, the …

 TIGER/2010/Tracts\_DP1,
 census,infrastructure\-boundaries,table,tiger,us

2010\-01\-01T00:00:00Z/2010\-01\-02T00:00:00Z



 \-14\.69 \-180 71\.567 \-64\.435
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








