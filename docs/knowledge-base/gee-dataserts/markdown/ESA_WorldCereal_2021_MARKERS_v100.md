



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

ESA WorldCereal Active Cropland 10 m v100


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================================








Dataset Availability
2020\-01\-01T00:00:00Z–2021\-12\-31T23:59:59Z
Dataset Provider


[ESA WorldCereal Consortium](https://esa-worldcereal.org/en)



Earth Engine Snippet


`ee.ImageCollection("ESA/WorldCereal/2021/MARKERS/v100")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ESA/ESA_WorldCereal_2021_MARKERS_v100)





Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[copernicus](/earth-engine/datasets/tags/copernicus)
[crop](/earth-engine/datasets/tags/crop)
[esa](/earth-engine/datasets/tags/esa)
[global](/earth-engine/datasets/tags/global)
[landcover](/earth-engine/datasets/tags/landcover)
[landsat](/earth-engine/datasets/tags/landsat)
[sentinel1\-derived](/earth-engine/datasets/tags/sentinel1-derived)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)








#### Description



The European Space Agency (ESA) WorldCereal Active Cropland 10 m 2021
product suite contains global\-scale seasonal active cropland markers. They
were generated as part of the
[ESA\-WorldCereal project](https://esa-worldcereal.org/). The active cropland
products indicate whether or not a pixel identified as temporary crops has
been actively cultivated during a specific growing season. In order for a
pixel to be labeled as “active” during a particular growing season, a full
crop growth cycle (sowing, growing, senescence and harvesting) needs to take
place within the designated time period. Note that this active marker is not
crop\-type specific. Any crop grown (slightly) outside the predefined growing
seasons will not be flagged as active cropland in any of the seasons covered
by the WorldCereal system. The active marker results from running a growing
season detection algorithm \[1] on the Sentinel\-2 derived enhanced vegetation
index (EVI). More information on the methodology used to generate these
products is described in \[2].


This collection contains up to 106 agro\-ecological zone (AEZ) images per
crop season, where each AEZ has its own seasonality. The seasons for which
the active cropland marker is available are described in the list below and
were developed in \[3] as part of the project.


WorldCereal seasons description:


* tc\-wintercereals: the main cereals season defined in an AEZ
* tc\-springcereals: optional springcereals season, only defined in certain
AEZ
* tc\-maize\-main: the main maize season defined in an AEZ
* tc\-maize\-second: optional second maize season, only defined in certain AEZ


Each product (image) has a binary classification band where value 0
corresponds to inactive cropland and value 100 corresponds to active
cropland.


The collection should be filtered using one or more of the following image
properties:


* aez\_id, holding the ID of the AEZ to which the image belongs
* season, describing the season for which the image is valid.


References:


* \[1] Bolton, D. K., Gray, J. M., Melaas, E. K., Moon, M., Eklundh, L., and
Friedl, M. A.: Continental\-scale land surface phenology from harmonized
Landsat 8 and Sentinel\-2 imagery, Remote Sens. Environ., 240, 111685,
https://doi.org/10\.1016/j.rse.2020\.111685, 2020\.
* \[2] [WorldCereal methodology and products paper](https://doi.org/10.5194/essd-2023-184)
* \[3] [WorldCereal global seasonality paper](https://doi.org/10.1080/15481603.2022.2079273)


WorldCereal datasets:


* Version 100 for year 2021
	+ [ESA/WorldCereal/AEZ/v100](/earth-engine/datasets/catalog/ESA_WorldCereal_AEZ_v100)
	+ [ESA/WorldCereal/2021/MODELS/v100](/earth-engine/datasets/catalog/ESA_WorldCereal_2021_MODELS_v100)
	+ [ESA/WorldCereal/2021/MARKERS/v100](/earth-engine/datasets/catalog/ESA_WorldCereal_2021_MARKERS_v100)





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `classification` | 0 | 100 | Classification: 0 or 100 |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| aez\_id | INT | ID of the agro\-ecological zone (AEZ) to which the product belongs. |
| product | STRING | WorldCereal product name. |
| season | STRING | Season for which the product is valid. |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Van Tricht, K., Degerickx, J., Gilliams, S., Zanaga, D., Battude, M., Grosu,
A., Brombacher, J., Lesiv, M., Bayas, J. C. L., Karanam, S., Fritz, S.,
Becker\-Reshef, I., Franch, B., Mollà\-Bononad, B., Boogaard, H., Pratihast,
A. K., and Szantoi, Z.: WorldCereal: a dynamic open\-source system for
global\-scale, seasonal, and reproducible crop and irrigation mapping, Earth
Syst. Sci. Data Discuss. \[preprint],
[doi:10\.5194/essd\-2023\-184](https://doi.org/10.5194/essd-2023-184), in
review, 2023\.,





### DOIs


* [https://doi.org/10\.5194/essd\-2023\-184](https://doi.org/10.5194/essd-2023-184)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('ESA/WorldCereal/2021/MARKERS/v100')

// Filter on AEZ
varaez_46173=dataset.filter('aez_id == 46173');

// Get the active cropland marker for the different seasons
varactivemarker_summerseason=aez_46173.filter('season == "tc-maize-main"');
varactivemarker_winterseason=aez_46173.filter('season == "tc-wintercereals"');

// Visualization specifics: red is inactive, green is active cropland
varvisualization={
bands:['classification'],
max:100,
palette:['eb0000','37e622']
};

// Show active cropland in two major growing seasons in US.
Map.addLayer(activemarker_summerseason,visualization,'Active cropland tc-maize-main');
Map.addLayer(activemarker_winterseason,visualization,'Active cropland tc-wintercereals');

Map.setCenter(-98.987,38.0454,11)
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ESA/ESA_WorldCereal_2021_MARKERS_v100)


[ESA WorldCereal Active Cropland 10 m v100](/earth-engine/datasets/catalog/ESA_WorldCereal_2021_MARKERS_v100)

The European Space Agency (ESA) WorldCereal Active Cropland 10 m 2021 product suite contains global\-scale seasonal active cropland markers. They were generated as part of the ESA\-WorldCereal project. The active cropland products indicate whether or not a pixel identified as temporary crops has been actively cultivated during a specific growing …

 ESA/WorldCereal/2021/MARKERS/v100,
 agriculture,copernicus,crop,esa,global,landcover,landsat,sentinel1\-derived,sentinel2\-derived

2020\-01\-01T00:00:00Z/2021\-12\-31T23:59:59Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5194/essd\-2023\-184](https://doi.org/https://esa-worldcereal.org/en)
* [https://doi.org/10\.5194/essd\-2023\-184](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/ESA_WorldCereal_2021_MARKERS_v100)









