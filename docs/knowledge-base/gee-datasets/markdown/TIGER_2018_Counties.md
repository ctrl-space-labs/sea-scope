



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TIGER: US Census Counties 2018


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================








Dataset Availability
2018\-01\-01T00:00:00Z–2019\-01\-01T00:00:00Z
Dataset Provider


[United States Census Bureau](https://www.census.gov/programs-surveys/geography/guidance/tiger-data-products-guide.html)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("TIGER/2018/Counties")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2018_Counties)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("TIGER/2018/Counties_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2018_Counties_FeatureView)





Tags


[census](/earth-engine/datasets/tags/census)
[county](/earth-engine/datasets/tags/county)
[infrastructure\-boundaries](/earth-engine/datasets/tags/infrastructure-boundaries)
[table](/earth-engine/datasets/tags/table)
[tiger](/earth-engine/datasets/tags/tiger)
[us](/earth-engine/datasets/tags/us)








#### Description



The United States Census Bureau TIGER dataset contains the 2018 boundaries
for primary legal divisions of US states. In most states, these entities
are termed "counties". In Louisiana, these divisions are known as
"parishes".


Alaska has governmental entities called "boroughs" which fill a similar
governmental role to counties, but in some areas those governmental
responsibilities are handled directly by the state and sometimes by a city.
For Alaska, county equivalent entities thus include


1. organized boroughs,
2. combined city and borough entities (e.g. Juneau),
3. municipalities, and
4. census areas.


The census areas are delineated cooperatively for statistical purposes by
the State of Alaska and the Census Bureau.


In four states (Maryland, Missouri, Nevada, and Virginia), there are one
or more incorporated places that are independent of any county
organization and thus constitute primary divisions of their states. These
incorporated places are known as independent cities and are treated as
county\-equivalent entities for purposes of data presentation.


The District of Columbia and Guam have no primary divisions and each area is
considered a county\-equivalent entity for purposes of data presentation.
The Census Bureau treats the following entities as equivalents of counties
for purposes of data presentation: municipios in Puerto Rico, districts
and islands in America Samoa, municipalities in the Commonwealth of the
Northern Mariana Islands, and islands in the U.S. Virgin Islands.


For full technical details on all TIGER 2018 products, see the [TIGER
technical documentation](https://www2.census.gov/geo/pdfs/maps-data/data/tiger/tgrshp2018/TGRSHP2018_TechDoc.pdf).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| ALAND | DOUBLE | Land area |
| AWATER | DOUBLE | Water area |
| CBSAFP | STRING | Metropolitan statistical area/micropolitan statistical area code |
| CLASSFP | STRING | FIPS class code |
| COUNTYFP | STRING | County FIPS code |
| COUNTYNS | STRING | County GNIS code |
| CSAFP | STRING | Combined statistical area code |
| FUNCSTAT | STRING | Functional Status |
| GEOID | STRING | County identifier; a concatenation of state FIPS code and county FIPS code |
| INTPTLAT | STRING | Internal point latitude |
| INTPTLON | STRING | Internal point longitude |
| LSAD | STRING | Legal/statistical area description for the county |
| METDIVFP | STRING | Metropolitan division code |
| MTFCC | STRING | MAF/TIGER feature class code (\=G4020\) |
| NAME | STRING | County name |
| NAMELSAD | STRING | Name and the translated legal/statistical area description for the county |
| STATEFP | STRING | State FIPS code |




### Terms of Use


**Terms of Use**


The U.S. Census Bureau offers some of its public data
in machine\-readable format via an Application Programming Interface
(API). All of the content, documentation, code and related materials
made available through the API are subject to [these terms and
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
vardataset=ee.FeatureCollection('TIGER/2018/Counties');
varvisParams={
palette:['purple','blue','green','yellow','orange','red'],
min:0,
max:50,
opacity:0.8,
};

// Turn the strings into numbers
dataset=dataset.map(function(f){
returnf.set('STATEFP',ee.Number.parse(f.get('STATEFP')));
});

varimage=ee.Image().float().paint(dataset,'STATEFP');
varcountyOutlines=ee.Image().float().paint({
featureCollection:dataset,
color:'black',
width:1
});

Map.setCenter(-99.844,37.649,5);
Map.addLayer(image,visParams,'TIGER/2018/Counties');
Map.addLayer(countyOutlines,{},'county outlines');
Map.addLayer(dataset,null,'for Inspector',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2018_Counties)
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
varfvLayer=ui.Map.FeatureViewLayer('TIGER/2018/Counties_FeatureView');

varvisParams={
opacity:1,
polygonStrokeColor:'black',
polygonFillColor:{
property:'STATEFP',
categories:[
['08','purple'],// Colorado counties
['32','blue']// Nevada counties
],
defaultValue:'white'
}
};

fvLayer.setVisParams(visParams);
fvLayer.setName('US census counties (FV)');

Map.setCenter(-99.844,37.649,5);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2018_Counties_FeatureView)


[TIGER: US Census Counties 2018](/earth-engine/datasets/catalog/TIGER_2018_Counties)

The United States Census Bureau TIGER dataset contains the 2018 boundaries for primary legal divisions of US states. In most states, these entities are termed "counties". In Louisiana, these divisions are known as "parishes". Alaska has governmental entities called "boroughs" which fill a similar governmental role to counties, but in …

 TIGER/2018/Counties,
 census,county,infrastructure\-boundaries,table,tiger,us

2018\-01\-01T00:00:00Z/2019\-01\-01T00:00:00Z



 \-14\.69 \-180 71\.567 \-64\.435
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








