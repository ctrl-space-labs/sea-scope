



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

geoBoundaries: Political administrative boundaries at Municipality level (ADM2\), v6\.0\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================================================================








Dataset Availability
2023\-09\-14T00:00:00Z–2023\-09\-14T00:00:00Z
Dataset Provider


[William and Mary geoLab](https://www.geoboundaries.org/index.html)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("WM/geoLab/geoBoundaries/600/ADM2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WM/WM_geoLab_geoBoundaries_600_ADM2)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("WM/geoLab/geoBoundaries/600/ADM2_FeatureView")` 





Tags


[borders](/earth-engine/datasets/tags/borders)
[countries](/earth-engine/datasets/tags/countries)
[infrastructure\-boundaries](/earth-engine/datasets/tags/infrastructure-boundaries)
[table](/earth-engine/datasets/tags/table)








#### Description



The geoBoundaries Global Database of Political Administrative Boundaries
Database is an online, open license resource of boundaries (i.e., state,
county) for every country in the world. Currently 199 total entities are
tracked, including all 195 UN member states, Greenland, Taiwan, Niue, and
Kosovo.


Comprehensive Global Administrative Zones (CGAZ) is a set of global
composites for administrative boundaries. Disputed areas are removed and
replaced with polygons following US Department of State definitions. It has
three boundary levels ADM0, ADM1, and ADM2, clipped to international
boundaries (US Department of State), with gaps filled between borders.


This dataset is part of CGAZ. It was ingested from
[version 6\.0\.0](https://github.com/wmgeolab/geoBoundaries/tree/1289e40e366c7b320550be1ee0614a9472d572d4)
of Global Composite Files with DBF\_DATE\_LAST\_UPDATE\=2023\-09\-13\.
It shows boundaries at level 
ADM2 (municipality\-level boundaries).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| shapeGroup | STRING | Unique country code |
| shapeName | STRING | Administrative region name |
| shapeType | STRING | Boundary type:* ADM0: Country level * ADM1: District level * ADM2: Municipality level |
| shapeID | DOUBLE | Unique ID assigned to the shape |




### Terms of Use


**Terms of Use**


geoBoundaries datasets are provided under the CC BY 4\.0 license, which
allows for most commmercial, noncommercial, and academic uses. See 
[provider terms of use](https://www.geoboundaries.org/index.html#usage).




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('WM/geoLab/geoBoundaries/600/ADM2');

Map.setCenter(-100.0,38.5,4);

varstyleParams={
fillColor:'b5ffb4',
color:'00909F',
width:1.0,
};

dataset=dataset.style(styleParams);

Map.addLayer(dataset,{},'ADM2 Boundaries');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WM/WM_geoLab_geoBoundaries_600_ADM2)


[geoBoundaries: Political administrative boundaries at Municipality level (ADM2\), v6\.0\.0](/earth-engine/datasets/catalog/WM_geoLab_geoBoundaries_600_ADM2)

The geoBoundaries Global Database of Political Administrative Boundaries Database is an online, open license resource of boundaries (i.e., state, county) for every country in the world. Currently 199 total entities are tracked, including all 195 UN member states, Greenland, Taiwan, Niue, and Kosovo. Comprehensive Global Administrative Zones (CGAZ) is a …

 WM/geoLab/geoBoundaries/600/ADM2,
 borders,countries,infrastructure\-boundaries,table

2023\-09\-14T00:00:00Z/2023\-09\-14T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








