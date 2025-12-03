



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

USGS GAP Hawaii 2001


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2002\-01\-01T00:00:00Z
Dataset Provider


[USGS](https://gapanalysis.usgs.gov/gaplandcover/)



Earth Engine Snippet


`ee.Image("USGS/GAP/HI/2001")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GAP_HI_2001)





Tags


[ecosystems](/earth-engine/datasets/tags/ecosystems)
[gap](/earth-engine/datasets/tags/gap)
[landcover](/earth-engine/datasets/tags/landcover)
[landfire](/earth-engine/datasets/tags/landfire)
[usgs](/earth-engine/datasets/tags/usgs)
[vegetation](/earth-engine/datasets/tags/vegetation)








#### Description



The GAP/LANDFIRE National Terrestrial Ecosystems data represents a detailed
vegetation and land cover classification for the Conterminous U.S., Alaska,
Hawaii, and Puerto Rico.GAP/LF 2011 Ecosystems for the Conterminous U.S. is
an update of the National Gap Analysis Program Land Cover Data \- Version 2\.2\.
Alaska ecosystems have been updated by LANDFIRE to 2012 conditions (LANDFIRE 2012\).
Hawaii and Puerto Rico data represent the 2001 time\-frame (Gon et al. 2006, Gould et al. 2008\).
The classification scheme used for the Alaska and the lower 48 states is based
on NatureServe's Ecological System Classification (Comer et al. 2003\), while
Puerto Rico and Hawaii's map legend are based on island specific classification
systems (Gon et al. 2006, Gould et al. 2008\).





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `landcover` | 1 | 9 | Landcover class descriptions |


**landcover Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#7c009c | Mixed Native\-Alien Forest |
| 2 | \#c14f00 | Mixed Native\-Alien Shrubs and Grasses |
| 3 | \#c1e09e | Native Coastal Vegetation |
| 4 | \#ef0047 | Deschampsia Grassland |
| 5 | \#d67900 | Aalii Shrubland |
| 6 | \#00e3eb | Bog Vegetation |
| 7 | \#ccbf70 | Native Dry Cliff Vegetation |
| 8 | \#7c7047 | Native Shrubland / Sparse Ohia (native shrubs) |
| 9 | \#617000 | Native Wet Cliff Vegetation |
| 10 | \#66e805 | Open Mao Shrubland |
| 11 | \#bf6b00 | Uluhe Shrubland |
| 12 | \#9bcc9b | Closed Hala Forest |
| 13 | \#008f99 | Closed Koa\-Ohia Forest |
| 14 | \#009c61 | Closed Ohia Forest |
| 15 | \#2bcf56 | Closed Pouteria Forest (native trees) |
| 16 | \#3ff2bf | Koa Forest |
| 17 | \#9b9b4c | Mamane / Naio / Native Trees |
| 18 | \#8ebc00 | Native Mesic to Dry Forest and Shrubland |
| 19 | \#33c7a6 | Native Wet Forest and Shrubland |
| 20 | \#7fbf00 | Ohia Forest |
| 21 | \#007f7f | Olopua\-Lama Forest |
| 22 | \#b3ed7f | Open Koa\-Mamane Forest |
| 23 | \#21ab33 | Open Koa\-Ohia Forest |
| 24 | \#000000 | Open Ohia Forest |
| 25 | \#002dc2 | Open Water |
| 26 | \#afe200 | Wetland Vegetation |
| 27 | \#fefec1 | Agriculture |
| 28 | \#eb3642 | High Intensity Developed |
| 29 | \#c94d42 | Low Intensity Developed |
| 30 | \#ccb8bf | Alien Grassland |
| 31 | \#9f298c | Alien Shrubland |
| 32 | \#75009c | Alien Forest |
| 33 | \#460075 | Kiawe Forest and Shrubland |
| 34 | \#001493 | Uncharacterized Forest |
| 35 | \#ededed | Uncharacterized Open\-Sparse Vegetation |
| 36 | \#d99485 | Uncharacterized Shrubland |
| 37 | \#6b6b6b | Very Sparse Vegetation to Unvegetated |




### Terms of Use


**Terms of Use**


Most U.S. Geological Survey (USGS) information resides
in the public domain and may be used without restriction. Additional
information on [Acknowledging or Crediting USGS as Information
Source](https://www.usgs.gov/information-policies-and-instructions/crediting-usgs) is available.




### Citations



Citations:
* Gon, S.M., A. Allison, R. J. Cannarella, J. D. Jacobi, K. Y. Kaneshiro,
M. H. Kido, M. Lane\-Kamehele, S. E. Miller. 2006\. The Hawaii Gap Analysis
Project Final Report. 487 pp.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('USGS/GAP/HI/2001');

varvisualization={
bands:['landcover'],
min:1.0,
max:37.0,
};

Map.setCenter(-157.0,20.1,7);

Map.addLayer(dataset,visualization,'GAP Hawaii');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GAP_HI_2001)


[USGS GAP Hawaii 2001](/earth-engine/datasets/catalog/USGS_GAP_HI_2001)

The GAP/LANDFIRE National Terrestrial Ecosystems data represents a detailed vegetation and land cover classification for the Conterminous U.S., Alaska, Hawaii, and Puerto Rico.GAP/LF 2011 Ecosystems for the Conterminous U.S. is an update of the National Gap Analysis Program Land Cover Data \- Version 2\.2\. Alaska ecosystems have been updated by …

 USGS/GAP/HI/2001,
 ecosystems,gap,landcover,landfire,usgs,vegetation

2001\-01\-01T00:00:00Z/2002\-01\-01T00:00:00Z



 18\.851697692492277 \-160\.2665484663998 22\.295218441899475 \-154\.669588436752
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








