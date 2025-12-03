



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TIGER: US Census Block Groups (BG) 2010


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2010\-01\-02T00:00:00Z
Dataset Provider


[United States Census Bureau](https://www.census.gov/programs-surveys/geography/guidance/tiger-data-products-guide.html)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("TIGER/2010/BG")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_BG)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("TIGER/2010/BG_FeatureView")` 





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
[block groups](https://www.census.gov/programs-surveys/geography/about/glossary.html#par_textimage_4),
which is a cluster of blocks within the same census tract that have the same
first digit of their four\-digit census block number. There are just over
300,000 polygon features covering the United States, the District
of Columbia, Puerto Rico, and the
Island areas.


For full technical details on all TIGER 2010 products, see the
[TIGER technical documentation](https://www2.census.gov/geo/pdfs/maps-data/data/tiger/tgrshp2010/TGRSHP10SF1.pdf).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| ALAND10 | DOUBLE | Land Area (square meters) |
| AWATER10 | DOUBLE | Water Area (square meters) |
| BLKGRPCE10 | STRING | Block Group Code |
| COUNTYFP10 | STRING | County FIPS Code |
| FUNCSTAT10 | STRING | Functional Status (S \= Statistical) |
| GEOID10 | STRING | Unique Identifier of Summary Level, Characteristic Iteration, US, State, County, Tract, Block Group Code |
| INTPTLAT10 | DOUBLE | Internal Point Latitude |
| INTPTLON10 | DOUBLE | Internal Point Longitude |
| MTFCC10 | STRING | MAF/TIGER Feature Classification Code |
| NAMELSAD10 | STRING | Full Name |
| STATEFP10 | STRING | State FIPS Code |
| TRACTCE10 | STRING | Census Tract Code |




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
vardataset=ee.FeatureCollection('TIGER/2010/BG');

varvisParams={
min:0,
max:1e7,
palette:['d8d9d9','aaaaaa','b6dfe9','2ea3f2','0c71c3']
};

// plotting the water area per polygon
dataset=dataset.map(function(f){
returnf.set('AWATER10',ee.Number.parse(f.get('AWATER10')));
});

varimage=ee.Image().float().paint(dataset,'AWATER10');

Map.setCenter(-81.99172,29.74101,9);
Map.addLayer(ee.Image(1),{min:0,max:1},'background');
Map.addLayer(image,visParams,'TIGER/2010/BG');
Map.addLayer(dataset,null,'for Inspector',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_BG)


[TIGER: US Census Block Groups (BG) 2010](/earth-engine/datasets/catalog/TIGER_2010_BG)

The United States Census Bureau regularly releases a geodatabase named TIGER. This dataset contains the 2010 census block groups, which is a cluster of blocks within the same census tract that have the same first digit of their four\-digit census block number. There are just over 300,000 polygon features covering …

 TIGER/2010/BG,
 census,city,infrastructure\-boundaries,neighborhood,table,tiger,urban,us

2010\-01\-01T00:00:00Z/2010\-01\-02T00:00:00Z



 \-14\.69 \-180 71\.567 \-64\.435
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








