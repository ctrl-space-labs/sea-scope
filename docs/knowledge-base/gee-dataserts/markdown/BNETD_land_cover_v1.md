



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Cote d'Ivoire BNETD 2020 Land Cover Map


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================








Dataset Availability
2020\-01\-01T00:00:00Z–2021\-01\-01T00:00:00Z
Dataset Provider


[BNETD\-CIGN](https://africageoportal.maps.arcgis.com/home/user.html?user=bnetdcignCI)



Earth Engine Snippet


`ee.ImageCollection("BNETD/land_cover/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/BNETD/BNETD_land_cover_v1)





Cadence
1 Year
Tags


[classification](/earth-engine/datasets/tags/classification)
[deforestation](/earth-engine/datasets/tags/deforestation)
[forest](/earth-engine/datasets/tags/forest)
[landcover](/earth-engine/datasets/tags/landcover)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)








#### Description



The Cote d'Ivoire BNETD 2020 Land Cover Map was produced by the Ivorian
Government through a national institution, the Center for Geographic
Information and Digital from the National Study Office Techniques and
Development (BNETD\-CIGN), with technical and financial support from the
European Union. The methodology used to produce the map was transparent,
participatory and in line with international standards.


To develop this map, a mosaic of satellite images (Sentinel 2\) from 2020 was
processed via Google Earth Engine and supplemented with data collected in the
field, to train a supervised classification algorithm (Random Forest).
Two field campaigns were conducted, from 10 November to 9 December 2022 and
from 26 January to 13 February 2023, throughout the country. These missions
involved 33 people from multiple partner organizations because the data
collection methods and definitions of certain land use classes
adopted by stakeholders may sometimes differ.


As part of the EUDR due diligence process, geolocation data for plots of
land producing EUDR\-relevant products could be overlaid with 2020 forest
cover data in order to assess the risk that the plot is located in an area
that was forested before the 2020 cut\-off date. To do this, forest cover
data aligned with the FAO definition of forests and the 2020 cut\-off date
is required. The 2020 land cover map of Cote d'Ivoire meets these needs.
Indeed, the classes in the land cover map can be combined to create a
forest/non\-forest map that is aligned with the FAO definition of forests.


A platform for accessing 2020 land cover data, metadata and the methodology
has been developed using ESRI solutions, from Africa GeoPortal, for data
analysis and visualization:


The address is: [https://bit.ly/carte\-ci\-2020](https://bit.ly/carte-ci-2020)


Documentation:


* [Detailed documentation](https://africageoportal.maps.arcgis.com/sharing/rest/content/items/26a717d4c13f4f3db2c6056f7e5c0bab/data)
* [Methodology in French](https://africageoportal.maps.arcgis.com/sharing/rest/content/items/76dc18767b89472eb89e8aa54e08a6c9/data)





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `classification` | 1 | 23 | Land Cover class |


**classification Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#276300 | Dense forest (Forêt dense) |
| 2 | \#59D757 | Light forest (Forêt claire) |
| 3 | \#569D6E | Forest gallery (Forêt galerie) |
| 4 | \#79CFAD | Secondary forest/degraded forest (Forêt secondaire/forêt dégradée) |
| 5 | \#34734C | Mangrove |
| 6 | \#B4FFAD | Forest plantation/Reforestation (Plantation forestière/Reboisement) |
| 7 | \#6EFA9A | Swamp forest/Forest on hydromorphic soil (Forêt marécageuse/Forêt sur sol hydromorphe) |
| 8 | \#D68589 | Coffee Plantation (Plantation de Café) |
| 9 | \#EBD37F | Cocoa Plantation (Plantation de Cacao) |
| 10 | \#D0E09D | Rubber plantation (Plantation d'Hévéa) |
| 11 | \#E8BEFF | Oil palm plantation (Plantation de Palmier à huile) |
| 12 | \#E751FE | Coconut Plantation (Plantation de Coco) |
| 13 | \#F3BFF2 | Cashew plantation (Plantation d'Anacarde) |
| 14 | \#9DFD00 | Fruit plantation / Arboriculture (Plantation fruitière / Arboricultures) |
| 15 | \#F2F38D | Agricultural development/Other crops/Orchards/Fallow land (Aménagement agricole/Autres cultures/Vergers/Jachères) |
| 16 | \#B6D322 | Tree savannah (Savane arborée) |
| 17 | \#E2FE5F | Shrub formations/ Thickets (Formations arbustives/ Fourrés) |
| 18 | \#F9FDCC | Herbaceous formations (Formations herbacées) |
| 19 | \#4A70C0 | Body of water, Courses and waterways (Plan d'eau, Cours et voies deau) |
| 20 | \#BEFFE8 | Swampy area (Zone marécageuse) |
| 21 | \#D20A02 | Human habitat, Infrastructure (Habitat humain, Infrastructures) |
| 22 | \#DBECEF | Rocky outcrop (Affleurement rocheux) |
| 23 | \#DCDCDC | Bare ground (Sol nu) |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* BNETD Land Cover Map 2020\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('BNETD/land_cover/v1/2020').select('classification');

Map.setCenter(-5.4400,7.5500,7);

Map.addLayer(dataset,{},"Cote d'Ivoire Land Cover Map 2020");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/BNETD/BNETD_land_cover_v1)


[Cote d'Ivoire BNETD 2020 Land Cover Map](/earth-engine/datasets/catalog/BNETD_land_cover_v1)

The Cote d'Ivoire BNETD 2020 Land Cover Map was produced by the Ivorian Government through a national institution, the Center for Geographic Information and Digital from the National Study Office Techniques and Development (BNETD\-CIGN), with technical and financial support from the European Union. The methodology used to produce the map …

 BNETD/land\_cover/v1,
 classification,deforestation,forest,landcover,landuse\-landcover

2020\-01\-01T00:00:00Z/2021\-01\-01T00:00:00Z



 4\.3603 \-8\.602 10\.74 \-2\.493
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








