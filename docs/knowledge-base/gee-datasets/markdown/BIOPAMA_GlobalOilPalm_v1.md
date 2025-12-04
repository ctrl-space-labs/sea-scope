



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global Map of Oil Palm Plantations


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================








Dataset Availability
2019\-01\-01T00:00:00Z–2019\-12\-31T00:00:00Z
Dataset Provider


[Biopama programme](https://doi.org/10.5281/zenodo.4473715)



Earth Engine Snippet


`ee.ImageCollection("BIOPAMA/GlobalOilPalm/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/BIOPAMA/BIOPAMA_GlobalOilPalm_v1)





Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[biodiversity](/earth-engine/datasets/tags/biodiversity)
[conservation](/earth-engine/datasets/tags/conservation)
[crop](/earth-engine/datasets/tags/crop)
[global](/earth-engine/datasets/tags/global)
[landuse](/earth-engine/datasets/tags/landuse)
[palm](/earth-engine/datasets/tags/palm)
[plantation](/earth-engine/datasets/tags/plantation)
biopama








#### Description



The dataset is a 10m global industrial and smallholder oil palm map for 2019\.
It covers areas where oil palm plantations were detected. The classified images are the output
of a convolutional neural network based on Sentinel\-1 and Sentinel\-2 half\-year composites.


See [article](https://essd.copernicus.org/articles/13/1211/2021/) for additional information.





### Bands


**Bands**




| Name | Pixel Size | Description |
| --- | --- | --- |
| `classification` | Oil Palm class description |


**classification Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#ff0000 | Industrial closed\-canopy oil palm plantations |
| 2 | \#ef00ff | Smallholder closed\-canopy oil palm plantations |
| 3 | \#696969 | Other land covers and/or uses that are not closed\-canopy oil palm. |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Adrià, D., Serge, W., Erik, M., David, G., Stephen, P., \& Zoltan, S. (2021\). High resolution global industrial and smallholder oil palm map for 2019 (Version v1\) \[Data set]. Zenodo.
[doi:10\.5281/zenodo.4473715](https://doi.org/10.5281/zenodo.4473715)





### DOIs


* [https://doi.org/10\.5281/zenodo.4473715](https://doi.org/10.5281/zenodo.4473715)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Import the dataset; a collection of composite granules from 2019.
vardataset=ee.ImageCollection('BIOPAMA/GlobalOilPalm/v1');

// Select the classification band.
varopClass=dataset.select('classification');

// Mosaic all of the granules into a single image.
varmosaic=opClass.mosaic();

// Define visualization parameters.
varclassificationVis={
min:1,
max:3,
palette:['ff0000','ef00ff','696969']
};

// Create a mask to add transparency to non-oil palm plantation class pixels.
varmask=mosaic.neq(3);
mask=mask.where(mask.eq(0),0.6);

// Display the data on the map.
Map.addLayer(mosaic.updateMask(mask),
classificationVis,'Oil palm plantation type',true);
Map.setCenter(-3.0175,5.2745,12);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/BIOPAMA/BIOPAMA_GlobalOilPalm_v1)


[Global Map of Oil Palm Plantations](/earth-engine/datasets/catalog/BIOPAMA_GlobalOilPalm_v1)

The dataset is a 10m global industrial and smallholder oil palm map for 2019\. It covers areas where oil palm plantations were detected. The classified images are the output of a convolutional neural network based on Sentinel\-1 and Sentinel\-2 half\-year composites. See article for additional information.

 BIOPAMA/GlobalOilPalm/v1,
 agriculture,biodiversity,conservation,crop,global,landuse,palm,plantation

2019\-01\-01T00:00:00Z/2019\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.4473715](https://doi.org/https://doi.org/10.5281/zenodo.4473715)
* [https://doi.org/10\.5281/zenodo.4473715](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/BIOPAMA_GlobalOilPalm_v1)









