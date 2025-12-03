



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TIGER: US Census 5\-digit ZIP Code Tabulation Areas 2010


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2010\-01\-02T00:00:00Z
Dataset Provider


[United States Census Bureau](https://www.census.gov/programs-surveys/geography/guidance/tiger-data-products-guide.html)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("TIGER/2010/ZCTA5")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_ZCTA5)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("TIGER/2010/ZCTA5_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_ZCTA5_FeatureView)





Tags


[census](/earth-engine/datasets/tags/census)
[infrastructure\-boundaries](/earth-engine/datasets/tags/infrastructure-boundaries)
[table](/earth-engine/datasets/tags/table)
[tiger](/earth-engine/datasets/tags/tiger)
[us](/earth-engine/datasets/tags/us)
zcta
zip\-code








#### Description



ZIP Code tabulation areas (ZCTAs) are approximate area representations of
U.S. Postal Service (USPS) 5\-digit ZIP Codes.
The Census Bureau defines ZCTAs by allocating each
Census block that contains addresses to a single ZIP Code tabulation area, usually
to the ZCTA that reflects the most frequently occurring ZIP Code for the
addresses within that block. Blocks that do not contain addresses but that
are completely surrounded by a single ZIP Code tabulation area (enclaves)
are assigned to the surrounding ZCTA; those surrounded by multiple ZCTAs
will be added to a single ZCTA based on the longest shared border.


The Census Bureau identifies 5\-digit ZIP Code tabulation areas using a 5\-
character numeric code that represents the most frequently occurring USPS
ZIP Code within that ZCTA. This code may contain leading zeros.


Data users should not use ZCTAs to identify the official USPS ZIP Code for
mail delivery. The USPS makes periodic changes to ZIP Codes to support more
efficient mail delivery. ZIP Codes that cover primarily nonresidential or
post office box addresses may not have a corresponding ZCTA because the
delineation process uses primarily residential addresses, resulting in a
bias towards ZIP Codes used for city\-style mail delivery.


For full technical details on all TIGER 2010 products, see the [TIGER
technical documentation](https://www2.census.gov/geo/pdfs/maps-data/data/tiger/tgrshp2010/TGRSHP10SF1.pdf).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| ALAND10 | DOUBLE | 2010 Census Land area |
| AWATER10 | DOUBLE | 2010 Census Water area |
| CLASSFP10 | STRING | 2010 Census FIPS 55 class code |
| FUNCSTAT10 | STRING | 2010 Census functional status (Always "S", for "Statistical entity".) |
| GEOID10 | STRING | 2010 Census 5\-digit ZIP Code Tabulation Area identifier |
| INTPTLAT10 | STRING | 2010 Census latitude of the internal point |
| INTPTLON10 | STRING | 2010 Census longitude of the internal point |
| MTFCC10 | STRING | MAF/TIGER feature class code (Always "G6350".) |
| ZCTA5CE10 | STRING | 2010 Census 5\-digit ZIP Code Tabulation Area code |




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
vardataset=ee.FeatureCollection('TIGER/2010/ZCTA5');
varvisParams={
palette:['black','purple','blue','green','yellow','orange','red'],
min:500000,
max:1000000000,
};

varzctaOutlines=ee.Image().float().paint({
featureCollection:dataset,
color:'black',
width:1
});

varimage=ee.Image().float().paint(dataset,'ALAND10');
Map.setCenter(-93.8008,40.7177,6);
Map.addLayer(image,visParams,'TIGER/2010/ZCTA5');
Map.addLayer(zctaOutlines,{},'borders');
Map.addLayer(dataset,{},'for Inspector',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_ZCTA5)
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
varfvLayer=ui.Map.FeatureViewLayer('TIGER/2010/ZCTA5_FeatureView');

varvisParams={
opacity:1,
polygonStrokeColor:'black',
polygonFillColor:{
property:'ALAND10',
mode:'linear',
palette:['black','purple','blue','green','yellow','orange','red'],
min:5e5,
max:5e9
}
};

fvLayer.setVisParams(visParams);
fvLayer.setName('US census zip codes');

Map.setCenter(-93.8008,40.7177,6);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TIGER/TIGER_2010_ZCTA5_FeatureView)


[TIGER: US Census 5\-digit ZIP Code Tabulation Areas 2010](/earth-engine/datasets/catalog/TIGER_2010_ZCTA5)

ZIP Code tabulation areas (ZCTAs) are approximate area representations of U.S. Postal Service (USPS) 5\-digit ZIP Codes. The Census Bureau defines ZCTAs by allocating each Census block that contains addresses to a single ZIP Code tabulation area, usually to the ZCTA that reflects the most frequently occurring ZIP Code for …

 TIGER/2010/ZCTA5,
 census,infrastructure\-boundaries,table,tiger,us

2010\-01\-01T00:00:00Z/2010\-01\-02T00:00:00Z



 \-14\.69 \-180 71\.567 \-64\.435
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








