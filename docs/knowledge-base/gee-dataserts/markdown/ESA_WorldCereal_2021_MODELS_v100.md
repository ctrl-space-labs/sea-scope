



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

ESA WorldCereal 10 m v100


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================








Dataset Availability
2020\-01\-01T00:00:00Z–2021\-12\-31T23:59:59Z
Dataset Provider


[ESA WorldCereal Consortium](https://esa-worldcereal.org/en)



Earth Engine Snippet


`ee.ImageCollection("ESA/WorldCereal/2021/MODELS/v100")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ESA/ESA_WorldCereal_2021_MODELS_v100)





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



The European Space Agency (ESA) WorldCereal 10 m 2021 product suite consists
of global\-scale annual and seasonal crop maps and their related confidence.
They were generated as part of the
[ESA\-WorldCereal project](https://esa-worldcereal.org/). More information on
the content of these products and the methodology used to generate them is
described in \[1].


This collection contains up to 106 agro\-ecological zone (AEZ) images for
each product which were all processed with respect to their own regional
seasonality and should be considered as independent products. These seasons
are described in the list below and were developed in \[2] as part of the
project. Note that cereals as described by WorldCereal include wheat,
barley, and rye, which belong to the *Triticeae* tribe.


WorldCereal seasons description:


* tc\-annual: a one\-year cycle being defined in an AEZ by the end of the last
considered growing season
* tc\-wintercereals: the main cereals season defined in an AEZ
* tc\-springcereals: optional springcereals season, only defined in certain
AEZ
* tc\-maize\-main: the main maize season defined in an AEZ
* tc\-maize\-second: optional second maize season, only defined in certain AEZ


The available products in this collection are:


* temporarycrops
* maize
* wintercereals
* springcereals
* irrigation


Each product (image) has a binary classification (0 or 100\) and a confidence
(0\-100\) band. Note that AEZs for which no irrigation product is available
were not processed because of the unavailability of thermal Landsat data.


The collection should be filtered using one or more of the following image
properties:


* aez\_id, holding the ID of the AEZ to which the image belongs
* product, describing the WorldCereal product name of the image
* season, describing the season for which the image is valid.


References:


* \[1] [WorldCereal methodology and products paper](https://doi.org/10.5194/essd-2023-184)
* \[2] [WorldCereal global seasonality paper](https://doi.org/10.1080/15481603.2022.2079273)


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
| `confidence` | 0 | 100 | Confidence, 0 to 100 |




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
vardataset=ee.ImageCollection('ESA/WorldCereal/2021/MODELS/v100')

// Set satellite background
Map.setOptions('SATELLITE');

// Typically we'd want to mask the "other" class (value 0)
// in the images
functionmask_other(img){
returnimg.updateMask(img.neq(0))
}

// Apply the mask_other function to the collection
dataset=dataset.map(mask_other);

/*--------------------------------------------------
Basic example for a global mosaic of temporary crops
--------------------------------------------------*/

// Get a global mosaic for all agro-ecological zone (AEZ) of temporary crops
vartemporarycrops=dataset.filter('product == "temporarycrops"').mosaic();

// Visualization specifics
varvisualization_class={
bands:["classification"],
max:100,
palette:["ff0000"]
};

varvisualization_conf={
bands:['confidence'],
min:[0],
max:[100],
palette:['be0000','fff816','069711'],
};

// Show global classification mosaic
Map.centerObject(temporarycrops);
Map.addLayer(temporarycrops,visualization_class,'Temporary crops');

// By default don't show confidence layer
Map.addLayer(
temporarycrops,visualization_conf,'Temporary crops confidence',false);

/*--------------------------------------------------
Advanced example for tc-maize-main season products
in a specific AEZ
--------------------------------------------------*/

// Filter on AEZ and season
vartc_maize_main_46172=dataset.filter(
ee.Filter.eq('season','tc-maize-main')
).filter(ee.Filter.eq('aez_id',46172));

// Get the different products
varmaize=tc_maize_main_46172.filter('product == "maize"');
varirrigation=tc_maize_main_46172.filter('product == "irrigation"');

// Visualization specifics
varvisualization_maize={
bands:["classification"],
max:100,
palette:["#ebc334"]
};

varvisualization_irrigation={
bands:["classification"],
max:100,
palette:["#2d79eb"]
};

// Show maize and irrigation classification
Map.addLayer(maize,visualization_maize,'Maize');
Map.addLayer(irrigation,visualization_irrigation,'Active irrigation');

// Uncomment the line below to zoom to a region
// where maize, other crops and active irrigation are visible
// Map.setCenter(-0.9911, 43.5017, 12)
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ESA/ESA_WorldCereal_2021_MODELS_v100)


[ESA WorldCereal 10 m v100](/earth-engine/datasets/catalog/ESA_WorldCereal_2021_MODELS_v100)

The European Space Agency (ESA) WorldCereal 10 m 2021 product suite consists of global\-scale annual and seasonal crop maps and their related confidence. They were generated as part of the ESA\-WorldCereal project. More information on the content of these products and the methodology used to generate them is described in …

 ESA/WorldCereal/2021/MODELS/v100,
 agriculture,copernicus,crop,esa,global,landcover,landsat,sentinel1\-derived,sentinel2\-derived

2020\-01\-01T00:00:00Z/2021\-12\-31T23:59:59Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5194/essd\-2023\-184](https://doi.org/https://esa-worldcereal.org/en)
* [https://doi.org/10\.5194/essd\-2023\-184](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/ESA_WorldCereal_2021_MODELS_v100)









