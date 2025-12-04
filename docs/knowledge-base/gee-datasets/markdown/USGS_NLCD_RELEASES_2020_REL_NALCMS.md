



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Land Cover of North America at 30 meters, 2020


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================








Dataset Availability
2019\-01\-01T00:00:00Z–2021\-12\-31T00:00:00Z
Dataset Provider


[The Commission for Environmental Cooperation (CEC)](http://www.cec.org/)



Earth Engine Snippet


`ee.Image("USGS/NLCD_RELEASES/2020_REL/NALCMS")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_NLCD_RELEASES_2020_REL_NALCMS)





Tags


[landcover](/earth-engine/datasets/tags/landcover)
[landsat](/earth-engine/datasets/tags/landsat)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[nlcd](/earth-engine/datasets/tags/nlcd)
[reflectance](/earth-engine/datasets/tags/reflectance)








#### Description



The 2020 North American Land Cover 30\-meter dataset was produced as part of
the North American Land Change Monitoring System (NALCMS), a trilateral
effort between Natural Resources Canada, the United States Geological
Survey, and three Mexican organizations including the National Institute of
Statistics and Geography (Instituto Nacional de Estadística y
Geografía), National Commission for the Knowledge and Use of the
Biodiversity (Comisión Nacional Para el Conocimiento y Uso de la
Biodiversidad), and the National Forestry Commission of Mexico
(Comisión Nacional Forestal). The collaboration is facilitated by
the Commission for Environmental Cooperation, an international organization
created by the Canada, Mexico, and United States governments under the North
American Agreement on Environmental Cooperation to promote environmental
collaboration between the three countries.


The general objective of NALCMS is to devise, through collective effort, a
harmonized multi\-scale land cover monitoring approach which ensures high
accuracy and consistency in monitoring land cover changes at the North
American scale and which meets each country's specific requirements.


This 30\-meter dataset of North American Land Cover reflects land cover
information for 2020 from Mexico and Canada, 2019 over the conterminous
United States and 2021 over Alaska. Each country developed its own
classification method to identify Land Cover classes and then provided an
input layer to produce a continental Land Cover map across North America.
Canada, Mexico, and the United States developed their own 30\-meter land
cover products; see specific sections on data generation below.


The main inputs for image classification were 30\-meter Landsat 8 Collection
2 Level 1 data in the three countries (Canada, the United States and
Mexico). Image selection processes and reduction to specific spectral bands
varied among the countries due to study\-site\-specific requirements. While
Canada selected most images from the year 2020 with a few from 2019 and
2021, the Conterminous United States employed mainly images from 2019, while
Alaska land cover maps are mainly based on the use of images from 2021\. The
land cover map for Mexico was based on land cover change detection between
2015 and 2020 Mexico Landsat 8 mosaics.


In order to generate a seamless and consistent land cover map of North
America, national maps were generated for Canada by the CCRS; for Mexico by
CONABIO, INEGI, and CONAFOR; and for the United States by the USGS. Each
country chose their own approaches, ancillary data, and land cover mapping
methodologies to create national datasets. This North America dataset was
produced by combining the national land cover datasets. The integration of
the three national products merged four Land Cover map sections, Alaska,
Canada, the conterminous United States and Mexico.


See also:


* Natural Resources Canada has North American Land Cover information
available online at
[https://open.canada.ca/data/en/dataset/ee1580ab\-a23d\-4f86\-a09b\-79763677eb47](https://open.canada.ca/data/en/dataset/ee1580ab-a23d-4f86-a09b-79763677eb47)
* The National Commission for the Knowledge and Use of Biodiversity has
North American Land Cover information available online at
[https://www.biodiversidad.gob.mx/monitoreo/cobertura\-suelo](https://www.biodiversidad.gob.mx/monitoreo/cobertura-suelo)
* The U.S. Geological Survey has North American Land Cover information
available online at [www.mrlc.gov](https://www.mrlc.gov)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `landcover` | 1 | 19 | Land cover classification grid cell value. Values are categorized into the following. [Product Legend](https://www.mrlc.gov/sites/default/files/inline-images/2005_nalcms_large_0.jpg). The classes in the 2020 product legend are given below. |


**landcover Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#033e00 | Temperate or sub\-polar needleleaf forest. Forests generally taller than three meters and more than 20 percent of total vegetation cover. This type occurs across the northern United States, Canada, and mountainous zones of Mexico. The tree crown cover contains at least 75 percent of needleleaved species. |
| 2 | \#939b71 | Sub\-polar taiga needleleaf forest. Forest and woodlands with trees generally taller than three meters and more than 5 percent of total vegetation cover with shrubs and lichens commonly present in the understory. The tree crown cover contains at least 75 percent of needleleaved species. This type occurs across Alaska and northern Canada and may consist of treed muskeg or wetlands. Forest canopies are variable and often sparse, with generally greater tree cover in the southern latitude parts of the zone than the north. |
| 3 | \#196d12 | Tropical or sub\-tropical broadleaf evergreen forest. Forests generally taller than five meters and more than 20 percent of total vegetation cover. These occur in the southern United States and Mexico. These forests have greater than 75 percent of tree crown cover represented by evergreen species. |
| 4 | \#1fab01 | Tropical or sub\-tropical broadleaf deciduous forest. Forests generally taller than five meters and more than 20 percent of total vegetation cover. These occur in the southern United States and Mexico. These forests have greater than 75 percent of tree crown cover represented by deciduous species. |
| 5 | \#5b725c | Temperate or sub\-polar broadleaf deciduous forest. Forests generally taller than three meters and more than 20 percent of total vegetation cover. These occur in the northern United States, Canada and mountainous zones of Mexico. These forests have greater than 75 percent of tree crown cover represented by deciduous species. |
| 6 | \#6b7d2c | Mixed forest. Forests generally taller than three meters and more than 20 percent of total vegetation cover. Neither needleleaf nor broadleaf tree species occupy more than 75 percent of total tree cover but are co\-dominant. |
| 7 | \#b29d29 | Tropical or sub\-tropical shrubland. Areas dominated by woody perennial plants with persistent woody stems less than five meters tall and typically greater than 20 percent of total vegetation. This class occurs across the southern United States and Mexico. |
| 8 | \#b48833 | Temperate or sub\-polar shrubland. Areas dominated by woody perennial plants with persistent woody stems less than three meters tall and typically greater than 20 percent of total vegetation. This class occurs across the northern United States, Canada and highlands of Mexico. |
| 9 | \#e9da5d | Tropical or sub\-tropical grassland. Areas dominated by graminoid or herbaceous vegetation generally accounting for greater than 80 percent of total vegetation cover. These areas are not subject to intensive management such as tilling but can be utilized for grazing. This class occurs across the southern United States and Mexico. |
| 10 | \#e0cd88 | Temperate or sub\-polar grassland. Areas dominated by graminoid or herbaceous vegetation, generally accounting for greater than 80 percent of total vegetation cover. These areas are not subject to intensive management such as tilling but can be utilized for grazing. This class occurs across Canada, United States and highlands of Mexico. |
| 11 | \#a07451 | Sub\-polar or polar shrubland\-lichen\-moss. Areas dominated by dwarf shrubs with lichen and moss typically accounting for at least 20 percent of total vegetation cover. This class occurs across northern Canada and Alaska. |
| 12 | \#bad292 | Sub\-polar or polar grassland\-lichen\-moss. Areas dominated by grassland with lichen and moss typically accounting for at least 20 percent of total vegetation cover. This class occurs across northern Canada and Alaska. |
| 13 | \#3f8970 | Sub\-polar or polar barren\-lichen\-moss. Areas dominated by a mixture of bare areas with lichen and moss that typically account for at least 20 percent of total vegetation cover. This class occurs across northern Canada. |
| 14 | \#6ca289 | Wetland. Areas dominated by perennial herbaceous and woody wetland vegetation which is influenced by the water table at or near surface over extensive periods of time. This includes marshes, swamps, bogs, mangroves, etc., either coastal or inland where water is present for a substantial period annually. |
| 15 | \#e6ad6a | Cropland. Areas dominated by intensively managed crops. These areas typically require human activities for their maintenance. This includes areas used for the production of annual crops, such as corn, soybeans, wheat, maize, vegetables, tobacco, cotton, etc.; perennial grasses for grazing; and woody crops such as orchards and vineyards. Crop vegetation accounts for greater than 20 percent of total vegetation. This class does not represent natural grasslands used for light to moderate grazing. |
| 16 | \#a9abae | Barren lands. Areas characterized by bare rock, gravel, sand, silt, clay, or other earthen material, with little or no "green" vegetation present regardless of its inherent ability to support life. Generally, vegetation accounts for less than 10 percent of total cover. |
| 17 | \#db2126 | Urban and built\-up. Areas that contain at least 30 percent or greater urban constructed materials for human activities (cities, towns, transportation etc.) |
| 18 | \#4c73a1 | Water. Areas of open water, generally with less than 25 percent cover of non\-water cover types. This class refers to areas that are consistently covered by water. |
| 19 | \#fff7fe | Snow and ice. Areas characterized by a perennial cover of ice and/or snow, generally greater than 25 percent of total cover. |




### Terms of Use


**Terms of Use**


This work was authored as part of the Contributor's official duties as an
Employee of the United States Government and is therefore a work of the
United States Government. In accordance with 17 U.S.C. 105, no copyright
protection is available for such works under U.S. Law. This is an Open
Access article that has been identified as being free of known restrictions
under copyright law, including all related and neighboring rights
[https://creativecommons.org/publicdomain/mark/1\.0/](https://creativecommons.org/publicdomain/mark/1.0/).
You can copy, modify, distribute and perform the work, even for commercial
purposes, all without asking permission.




### Citations



Citations:
* North American Land Change Monitoring System download webpage.
[www.cec.org/north\-american\-land\-change\-monitoring\-system](http://www.cec.org/north-american-land-change-monitoring-system/)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Import the NALCMS image.
varimage=ee.Image('USGS/NLCD_RELEASES/2020_REL/NALCMS');

Map.addLayer(
image,
{
palette:[
'033e00',// 1  Temperate or sub-polar needleleaf forest
'939b71',// 2  Sub-polar taiga needleleaf forest
'196d12',// 3  Tropical or sub-tropical broadleaf evergreen forest
'1fab01',// 4  Tropical or sub-tropical broadleaf deciduous forest
'5b725c',// 5  Temperate or sub-polar broadleaf deciduous forest
'6b7d2c',// 6  Mixed forest
'b29d29',// 7  Tropical or sub-tropical shrubland
'b48833',// 8  Temperate or sub-polar shrubland
'e9da5d',// 9  Tropical or sub-tropical grassland
'e0cd88',// 10  Temperate or sub-polar grassland
'a07451',// 11  Sub-polar or polar shrubland-lichen-moss
'bad292',// 12  Sub-polar or polar grassland-lichen-moss
'3f8970',// 13  Sub-polar or polar barren-lichen-moss
'6ca289',// 14  Wetland
'e6ad6a',// 15  Cropland
'a9abae',// 16  Barren land
'db2126',// 17  Urban and built-up
'4c73a1',// 18  Water
'fff7fe',// 19  Snow and ice
],
min:1,
max:19,
},
'NALCMS Land Cover');

Map.setCenter(-114,38,6);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_NLCD_RELEASES_2020_REL_NALCMS)


[Land Cover of North America at 30 meters, 2020](/earth-engine/datasets/catalog/USGS_NLCD_RELEASES_2020_REL_NALCMS)

The 2020 North American Land Cover 30\-meter dataset was produced as part of the North American Land Change Monitoring System (NALCMS), a trilateral effort between Natural Resources Canada, the United States Geological Survey, and three Mexican organizations including the National Institute of Statistics and Geography (Instituto Nacional de Estadística y …

 USGS/NLCD\_RELEASES/2020\_REL/NALCMS,
 landcover,landsat,landuse\-landcover,nlcd,reflectance

2019\-01\-01T00:00:00Z/2021\-12\-31T00:00:00Z



 14 \-175 84 \-50
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








