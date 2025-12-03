



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Copernicus CORINE Land Cover


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================








Dataset Availability
1986\-01\-01T00:00:00Z–2018\-12\-31T00:00:00Z
Dataset Provider


[EEA/Copernicus](https://land.copernicus.eu/pan-european/corine-land-cover/view)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/CORINE/V20/100m")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_CORINE_V20_100m)





Tags


[copernicus](/earth-engine/datasets/tags/copernicus)
[eea](/earth-engine/datasets/tags/eea)
[esa](/earth-engine/datasets/tags/esa)
[eu](/earth-engine/datasets/tags/eu)
[landcover](/earth-engine/datasets/tags/landcover)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
clc
corine








#### Description



The CORINE (coordination of information on the environment) Land Cover
(CLC) inventory was initiated in 1985 to standardize data collection on land
in Europe to support environmental policy development. The project is
coordinated by the European Environment Agency (EEA) in the frame of the EU
Copernicus programme and implemented by national teams. The number of
participating countries has increased over time currently including 33 (EEA)
member countries and six cooperating countries (EEA39\) with a total area of
over 5\.8M km2\.


CLC2018 is one of the datasets produced within the frame the Corine Land Cover
programme referring to land cover / land use status of year 2018\.
The reference year of the first CLC inventory was 1990 and the first update
created in 2000\. Later, the update cycle has become 6 years. Satellite
imagery provides the geometrical and thematic basis for mapping with in\-situ
data as essential ancillary information. The basic technical parameters of
CLC (i.e. 44 classes in nomenclature, 25 hectares minimum mapping unit
(MMU), and 100 meters minimum mapping width) have not changed since the
beginning, therefore the results of the different inventories are
comparable.


The time period covered by each asset is:


* 1990 asset: 1989 to 1998
* 2000 asset: 1999 to 2001
* 2006 asset: 2005 to 2007
* 2012 asset: 2011 to 2012
* 2018 asset: 2017 to 2018





### Bands



**Pixel Size**
  
100 meters



**Bands**




| Name | Description |
| --- | --- |
| `landcover` | Land cover |


**landcover Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 111 | \#e6004d | Artificial surfaces \> Urban fabric \> Continuous urban fabric |
| 112 | \#ff0000 | Artificial surfaces \> Urban fabric \> Discontinuous urban fabric |
| 121 | \#cc4df2 | Artificial surfaces \> Industrial, commercial, and transport units \> Industrial or commercial units |
| 122 | \#cc0000 | Artificial surfaces \> Industrial, commercial, and transport units \> Road and rail networks and associated land |
| 123 | \#e6cccc | Artificial surfaces \> Industrial, commercial, and transport units \> Port areas |
| 124 | \#e6cce6 | Artificial surfaces \> Industrial, commercial, and transport units \> Airports |
| 131 | \#a600cc | Artificial surfaces \> Mine, dump, and construction sites \> Mineral extraction sites |
| 132 | \#a64dcc | Artificial surfaces \> Mine, dump, and construction sites \> Dump sites |
| 133 | \#ff4dff | Artificial surfaces \> Mine, dump, and construction sites \> Construction sites |
| 141 | \#ffa6ff | Artificial surfaces \> Artificial, non\-agricultural vegetated areas \> Green urban areas |
| 142 | \#ffe6ff | Artificial surfaces \> Artificial, non\-agricultural vegetated areas \> Sport and leisure facilities |
| 211 | \#ffffa8 | Agricultural areas \> Arable land \> Non\-irrigated arable land |
| 212 | \#ffff00 | Agricultural areas \> Arable land \> Permanently irrigated land |
| 213 | \#e6e600 | Agricultural areas \> Arable land \> Rice fields |
| 221 | \#e68000 | Agricultural areas \> Permanent crops \> Vineyards |
| 222 | \#f2a64d | Agricultural areas \> Permanent crops \> Fruit trees and berry plantations |
| 223 | \#e6a600 | Agricultural areas \> Permanent crops \> Olive groves |
| 231 | \#e6e64d | Agricultural areas \> Pastures \> Pastures |
| 241 | \#ffe6a6 | Agricultural areas \> Heterogeneous agricultural areas \> Annual crops associated with permanent crops |
| 242 | \#ffe64d | Agricultural areas \> Heterogeneous agricultural areas \> Complex cultivation patterns |
| 243 | \#e6cc4d | Agricultural areas \> Heterogeneous agricultural areas \> Land principally occupied by agriculture, with significant areas of natural vegetation |
| 244 | \#f2cca6 | Agricultural areas \> Heterogeneous agricultural areas \> Agro\-forestry areas |
| 311 | \#80ff00 | Forest and semi natural areas \> Forests \> Broad\-leaved forest |
| 312 | \#00a600 | Forest and semi natural areas \> Forests \> Coniferous forest |
| 313 | \#4dff00 | Forest and semi natural areas \> Forests \> Mixed forest |
| 321 | \#ccf24d | Forest and semi natural areas \> Scrub and/or herbaceous vegetation associations \> Natural grasslands |
| 322 | \#a6ff80 | Forest and semi natural areas \> Scrub and/or herbaceous vegetation associations \> Moors and heathland |
| 323 | \#a6e64d | Forest and semi natural areas \> Scrub and/or herbaceous vegetation associations \> Sclerophyllous vegetation |
| 324 | \#a6f200 | Forest and semi natural areas \> Scrub and/or herbaceous vegetation associations \> Transitional woodland\-shrub |
| 331 | \#e6e6e6 | Forest and semi natural areas \> Open spaces with little or no vegetation \> Beaches, dunes, sands |
| 332 | \#cccccc | Forest and semi natural areas \> Open spaces with little or no vegetation \> Bare rocks |
| 333 | \#ccffcc | Forest and semi natural areas \> Open spaces with little or no vegetation \> Sparsely vegetated areas |
| 334 | \#000000 | Forest and semi natural areas \> Open spaces with little or no vegetation \> Burnt areas |
| 335 | \#a6e6cc | Forest and semi natural areas \> Open spaces with little or no vegetation \> Glaciers and perpetual snow |
| 411 | \#a6a6ff | Wetlands \> Inland wetlands \> Inland marshes |
| 412 | \#4d4dff | Wetlands \> Inland wetlands \> Peat bogs |
| 421 | \#ccccff | Wetlands \> Maritime wetlands \> Salt marshes |
| 422 | \#e6e6ff | Wetlands \> Maritime wetlands \> Salines |
| 423 | \#a6a6e6 | Wetlands \> Maritime wetlands \> Intertidal flats |
| 511 | \#00ccf2 | Water bodies \> Inland waters \> Water courses |
| 512 | \#80f2e6 | Water bodies \> Inland waters \> Water bodies |
| 521 | \#00ffa6 | Water bodies \> Marine waters \> Coastal lagoons |
| 522 | \#a6ffe6 | Water bodies \> Marine waters \> Estuaries |
| 523 | \#e6f2ff | Water bodies \> Marine waters \> Sea and ocean |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| landcover\_class\_names | STRING\_LIST | Land cover class names |
| landcover\_class\_palette | STRING\_LIST | Land cover class palette |
| landcover\_class\_values | INT\_LIST | Value of the land cover classification. |




### Terms of Use


**Terms of Use**


Access to data is based on a principle of full, open, and free access as
established by the Copernicus data and information policy Regulation (EU)
No 1159/2013 of 12 July 2013\. For more information visit:
[https://land.copernicus.eu/pan\-european/corine\-land\-cover/clc2018?tab\=metadata](https://land.copernicus.eu/pan-european/corine-land-cover/clc2018?tab=metadata).




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('COPERNICUS/CORINE/V20/100m/2012');
varlandCover=dataset.select('landcover');
Map.setCenter(16.436,39.825,6);
Map.addLayer(landCover,{},'Land Cover');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_CORINE_V20_100m)


[Copernicus CORINE Land Cover](/earth-engine/datasets/catalog/COPERNICUS_CORINE_V20_100m)

The CORINE (coordination of information on the environment) Land Cover (CLC) inventory was initiated in 1985 to standardize data collection on land in Europe to support environmental policy development. The project is coordinated by the European Environment Agency (EEA) in the frame of the EU Copernicus programme and implemented by …

 COPERNICUS/CORINE/V20/100m,
 copernicus,eea,esa,eu,landcover,landuse\-landcover

1986\-01\-01T00:00:00Z/2018\-12\-31T00:00:00Z



 \-29\.2 \-81\.77 73\.81 94\.13
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








