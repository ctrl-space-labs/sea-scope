



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

LANDFIRE EVH (Existing Vegetation Height) v1\.4\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================








Dataset Availability
2014\-09\-01T00:00:00Z–2014\-09\-01T00:00:00Z
Dataset Provider


[U.S. Department of Agriculture's (USDA), U.S. Forest Service (USFS), U.S.
Department of the Interior's Geological Survey (USGS), and The Nature Conservancy.](https://landfire.gov/)



Earth Engine Snippet


`ee.ImageCollection("LANDFIRE/Vegetation/EVH/v1_4_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Vegetation_EVH_v1_4_0)





Tags


[doi](/earth-engine/datasets/tags/doi)
[fire](/earth-engine/datasets/tags/fire)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[landfire](/earth-engine/datasets/tags/landfire)
[nature\-conservancy](/earth-engine/datasets/tags/nature-conservancy)
[usda](/earth-engine/datasets/tags/usda)
[usgs](/earth-engine/datasets/tags/usgs)
[vegetation](/earth-engine/datasets/tags/vegetation)
[wildfire](/earth-engine/datasets/tags/wildfire)








#### Description



LANDFIRE (LF), Landscape Fire and Resource Management Planning Tools, is a
shared program between the wildland fire management programs of the U.S.
Department of Agriculture's Forest Service, U.S. Department of the Interior's
Geological Survey, and The Nature Conservancy.


LANDFIRE (LF) layers are created using predictive landscape models based on
extensive field\-referenced data, satellite imagery and biophysical gradient
layers using classification and regression trees.


Existing Vegetation Height (EVH) represents the average height of the dominant vegetation for a 30\-m cell.
Canopy height is generated separately for tree, shrub, and herbaceous lifeforms using training data and other geospatial layers. EVH is determined by the average height weighted by species cover and based on the Existing Vegetation Type (EVT) lifeform.


* Decision tree models using field reference data, lidar, Landsat, and ancillary data are developed separately for each lifeform. Decision tree relationships are used to generate lifeform specific height class layers, which are merged into a single composite EVH layer.
* Disturbance data were used to develop LF Remap products for LFRDB plot filtering and to ensure 2015 and 2016 disturbances were included that were not visible in the source imagery.
* The EVC product is then reconciled through QA/QC measures to ensure life\-form is synchronized with both Existing Vegetation Cover and EVT products.


LF uses EVH in several subsequent layers, including the development of the fuel products.


The LANDIFRE Vegetation datasets include:


* Biophysical Settings (BPS)
* Environmental Site Potential (ESP)
* Existing Vegetation Canopy Cover (EVC)
* Existing Vegetation Height (EVH).
* Existing Vegetation Type (EVT)
These layers are created using predictive landscape models based on extensive
field\-referenced data, satellite imagery and biophysical gradient layers using
classification and regression trees.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `EVH` | Existing Vegetation Height |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| EVH\_classes | DOUBLE | Class values of the Existing Vegetation Height. |
| EVH\_names | STRING | Descriptive names of the Existing Vegetation Height. |




### Terms of Use


**Terms of Use**


LANDFIRE data are public domain data with no use restrictions, though if modifications
or derivatives of the product(s) are created, then please add some descriptive modifier
to the data set to avoid confusion.




### Citations



Citations:
* The suggested way to cite LANDFIRE products is specific to each product,
so the model for citation is provided, with an example for a particular product.
Producer. Year released. Product xxxxx:



	+ Individual model name.
	+ BpS Models and Descriptions, Online. LANDFIRE. Washington, DC. U.S. Department of
	Agriculture, Forest Service
	+ U.S. Department of the Interior; U.S. Geological Survey; Arlington, VA
	+ The Nature Conservancy (Producers). Available\- URL. Access date.
Example Citation: LANDFIRE Biophysical Settings. 2018\. Biophysical setting 14420:
South Texas sand sheet grassland. In: LANDFIRE Biophysical Setting Model: Map zone 36,
\[Online]. In: BpS Models and Descriptions. In: LANDFIRE. Washington, DC:
U.S. Department of Agriculture, Forest Service; U.S. Department of the Interior;
U.S. Geological Survey; Arlington, VA: The Nature Conservancy (Producers).
Available: [https://www.landfire.gov/bps\-models.php](https://www.landfire.gov/bps-models.php) \[2018, June 27].
Additional guidance on citation of LANDFIRE products can be found
[here](https://landfire.gov/data/citation)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('LANDFIRE/Vegetation/EVH/v1_4_0');

varvisualization={
bands:['EVH'],
};

Map.setCenter(-121.671,40.699,5);

Map.addLayer(dataset,visualization,'EVH');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Vegetation_EVH_v1_4_0)


[LANDFIRE EVH (Existing Vegetation Height) v1\.4\.0](/earth-engine/datasets/catalog/LANDFIRE_Vegetation_EVH_v1_4_0)

LANDFIRE (LF), Landscape Fire and Resource Management Planning Tools, is a shared program between the wildland fire management programs of the U.S. Department of Agriculture's Forest Service, U.S. Department of the Interior's Geological Survey, and The Nature Conservancy. LANDFIRE (LF) layers are created using predictive landscape models based on extensive …

 LANDFIRE/Vegetation/EVH/v1\_4\_0,
 doi,fire,forest\-biomass,landfire,nature\-conservancy,usda,usgs,vegetation,wildfire

2014\-09\-01T00:00:00Z/2014\-09\-01T00:00:00Z



 17\.52 \-175\.1 71\.48 \-63\.66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








