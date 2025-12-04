



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

HUC08: USGS Watershed Boundary Dataset of Subbasins


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================








Dataset Availability
2017\-04\-22T00:00:00Z–2017\-04\-23T00:00:00Z
Dataset Provider


[United States Geological Survey](https://nhd.usgs.gov/wbd.html)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("USGS/WBD/2017/HUC08")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_WBD_2017_HUC08)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("USGS/WBD/2017/HUC08_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_WBD_2017_HUC08_FeatureView)





Tags


[hydrology](/earth-engine/datasets/tags/hydrology)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[table](/earth-engine/datasets/tags/table)
[usgs](/earth-engine/datasets/tags/usgs)
[water](/earth-engine/datasets/tags/water)
[watershed](/earth-engine/datasets/tags/watershed)
[wbd](/earth-engine/datasets/tags/wbd)








#### Description



The Watershed Boundary Dataset (WBD) is a comprehensive
aggregated collection of hydrologic unit (HU) data consistent
with the national criteria for delineation and resolution. It
defines the areal extent of surface water drainage to a point
except in coastal or lake front areas where there could be multiple
outlets as stated by the [Federal Standards and Procedures for
the National Watershed Boundary Dataset](https://pubs.usgs.gov/tm/11/a3).
Watershed boundaries are determined solely upon science\-based
hydrologic principles, not favoring any administrative boundaries
or special projects, nor particular program or agency. The intent
of defining HUs for the WBD is to establish a baseline drainage
boundary framework, accounting for all land and surface areas.


The HUs are delineated at 1:24,000\-scale in the conterminous
United States, 1:25,000\-scale in Hawaii and the Caribbean, and
1:63,360\-scale in Alaska, meeting the National Map Accuracy Standards
(NMAS). WBDs are represented as polygons that define the boundary
of the HUs. The HUs are given a Hydrologic Unit Code (HUC) that
ranges from 2 digits to 12 digits. These codes describe where
the unit is in the country and the level of the unit. The number
of digits in a HUC is related to 6 levels of detail for the WBD:
the lower level polygons cover larger areas than higher level
ones. The higher the level, the more digits to the HUC, since
previous levels are nested in it.


The WBD polygons attributes
include HUCs, size (in the form of acres and square kilometers),
name, downstream HUC, type of watershed, non\-contributing areas,
and flow modifications. WBD line attributes contain the highest
level of hydrologic unit for each boundary, line source information
and flow modifications.




| Name | Level | Digit | HU Code |
| --- | --- | --- | --- |
| Region | 1 | 2 | 2 |
| Subregion | 2 | 4 | 4 |
| Basin | 3 | 6 | 6 |
| Subbasin | 4 | 8 | 8 |
| Watershed | 5 | 10 | 10 |
| Subwatershed | 6 | 12 | 12 |


\*Calculated by the data provider.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| areaacres | STRING | Size of the feature in acres |
| areasqkm | STRING | Size of the feature in square kilometers |
| gnis\_id | STRING | A unique number to relate the name of the hydrologic unit to the GNIS names database (always empty) |
| loaddate | STRING | Date when the data were loaded into the official provider database |
| metasource | STRING | A unique identifier that links the element to the metadata tables |
| name | STRING | GNIS name for the geographic area in which the hydrologic unit is located |
| shape\_area | STRING | Area of feature in internal units squared |
| shape\_leng | STRING | Length of feature in internal units |
| sourcedata | STRING | A space provided for a brief description of the type of base data used to update or change the current WBD (always empty) |
| sourcefeat | STRING | Identifies the parent of the feature if the feature is the result of a split or merge (always empty) |
| sourceorig | STRING | Description of the agency that created the base data used to improve the WBD (always empty) |
| states | STRING | Identifies the State(s) or outlying areas that the hydrologic unit falls within or touches |
| tnmid | STRING | A unique 40\-character field that identifies each element in the database exclusively |
| huc8 | STRING | Unique hydrologic unit code |




### Terms of Use


**Terms of Use**


Most U.S. Geological Survey (USGS) information resides
in the public domain and may be used without restriction. Additional
information on [Acknowledging or Crediting USGS as Information
Source](https://www.usgs.gov/information-policies-and-instructions/crediting-usgs) is available.




### Citations



Citations:
* Coordinated effort between the United States Department of Agriculture\-Natural
Resources Conservation Service (USDA\-NRCS), the United States Geological
Survey (USGS), and the Environmental Protection Agency (EPA). The
Watershed Boundary Dataset (WBD) was created from a variety of
sources from each state and aggregated into a standard national
layer for use in strategic planning and accountability. Watershed
Boundary Dataset for HUC\# \[Online WWW]. Available URL: (https://datagateway.nrcs.usda.gov)
\[Accessed 22/04/2017].





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('USGS/WBD/2017/HUC08');

varvisualization={
color:'808080',
strokeWidth:1
};

dataset=dataset.draw(visualization);

Map.setCenter(-105.861,39.529,7);
Map.addLayer(dataset,null,'Basins');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_WBD_2017_HUC08)
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
varfvLayer=ui.Map.FeatureViewLayer('USGS/WBD/2017/HUC08_FeatureView');

varvisParams={
color:'808080',
lineWidth:1
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Basins');

Map.setCenter(-105.861,39.529,7);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_WBD_2017_HUC08_FeatureView)


[HUC08: USGS Watershed Boundary Dataset of Subbasins](/earth-engine/datasets/catalog/USGS_WBD_2017_HUC08)

The Watershed Boundary Dataset (WBD) is a comprehensive aggregated collection of hydrologic unit (HU) data consistent with the national criteria for delineation and resolution. It defines the areal extent of surface water drainage to a point except in coastal or lake front areas where there could be multiple outlets as …

 USGS/WBD/2017/HUC08,
 hydrology,surface\-ground\-water,table,usgs,water,watershed,wbd

2017\-04\-22T00:00:00Z/2017\-04\-23T00:00:00Z



 \-14\.69 \-180 71\.567 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








