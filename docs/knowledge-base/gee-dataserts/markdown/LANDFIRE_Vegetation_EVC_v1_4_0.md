



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

LANDFIRE EVC (Existing Vegetation Cover) v1\.4\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================








Dataset Availability
2014\-09\-01T00:00:00Z–2014\-09\-01T00:00:00Z
Dataset Provider


[U.S. Department of Agriculture's (USDA), U.S. Forest Service (USFS), U.S.
Department of the Interior's Geological Survey (USGS), and The Nature Conservancy.](https://landfire.gov/)



Earth Engine Snippet


`ee.ImageCollection("LANDFIRE/Vegetation/EVC/v1_4_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Vegetation_EVC_v1_4_0)





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


LANDFIRE's (LF) Existing Vegetation Cover (EVC) represents the vertically projected percent cover of the live canopy layer for a 30\-m cell.
EVC is generated separately for tree, shrub, and herbaceous cover lifeforms using training data and other geospatial layers. Percentage tree, shrub, and herbaceous canopy cover training data are generated using plot\-level ground\-based visual assessments and lidar observations.
\* Once the training data are developed, relationships are then established separately for each lifeform between the training data and combination of Landsat and ancillary data. Each of the derived data layers (tree, shrub, herbaceous) has a potential range from 0\-100 percent which are merged into a single composite EVC layer.
\* Disturbance data were used to develop LF Remap products for LFRDB plot filtering and to ensure 2015 and 2016 disturbances were included that were not visible in the source imagery.
\* The EVC product is then reconciled through QA/QC measures to ensure life\-form is synchronized with both Existing Vegetation Height and Existing Vegetation Type products.
LF uses EVC in several subsequent layers, including the development of the fuel layers.


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
| `EVC` | Existing Vegetation Cover |


**EVC Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 11 | \#0000ff | Open Water |
| 12 | \#9fa1f0 | Snow/Ice |
| 13 | \#403da8 | Developed\-Upland Deciduous Forest |
| 14 | \#444f89 | Developed\-Upland Evergreen Forest |
| 15 | \#6677cd | Developed\-Upland Mixed Forest |
| 16 | \#7a8ef5 | Developed\-Upland Herbaceous |
| 17 | \#9eaad7 | Developed\-Upland Shrubland |
| 18 | \#343434 | Developed\-Herbaceous Wetland Vegetation |
| 19 | \#343434 | Developed\-Woody Wetland Vegetation |
| 20 | \#ffebe0 | Developed \- General |
| 21 | \#fdccd3 | Developed \- Open Space |
| 22 | \#ff7a8f | Developed \- Low Intensity |
| 23 | \#fd2c4f | Developed \- Medium Intensity |
| 24 | \#ad001c | Developed \- High Intensity |
| 25 | \#010101 | Developed\-Roads |
| 31 | \#bfbfbf | Barren |
| 32 | \#e6e8fa | Quarries\-Strip Mines\-Gravel Pits |
| 60 | \#d21c5e | NASS\-Orchard |
| 61 | \#a80084 | NASS\-Vineyard |
| 62 | \#d21c77 | NASS\-Bush fruit and berries |
| 63 | \#fff58c | NASS\-Row Crop\-Close Grown Crop |
| 64 | \#faff77 | NASS\-Row Crop |
| 65 | \#ffed77 | NASS\-Close Grown Crop |
| 66 | \#ffff77 | NASS\-Fallow/Idle Cropland |
| 67 | \#e3d41c | NASS\-Pasture and Hayland |
| 68 | \#fae3a3 | NASS\-Wheat |
| 69 | \#d2ffed | NASS\-Aquaculture |
| 75 | \#7f38ff | Herbaceous Semi\-dry |
| 76 | \#7f38ff | Herbaceous Semi\-wet |
| 78 | \#7f382b | Recently Disturbed Forest |
| 80 | \#ffffbf | Agriculture \- General |
| 81 | \#ffff9c | Pasture/Hay |
| 82 | \#ffff78 | Cultivated Crops |
| 83 | \#ffff54 | Small Grains |
| 84 | \#ffff2b | Fallow |
| 85 | \#ffff00 | Urban\-Recreational Grasses |
| 95 | \#7f8fff | Herbaceous Wetlands |
| 100 | \#7a7f75 | Sparse Vegetation Canopy |
| 101 | \#ccff99 | Tree Cover \>\= 10 and \< 20% |
| 102 | \#aee082 | Tree Cover \>\= 20 and \< 30% |
| 103 | \#91c46c | Tree Cover \>\= 30 and \< 40% |
| 104 | \#77ab57 | Tree Cover \>\= 40 and \< 50% |
| 105 | \#5e9144 | Tree Cover \>\= 50 and \< 60% |
| 106 | \#467832 | Tree Cover \>\= 60 and \< 70% |
| 107 | \#336324 | Tree Cover \>\= 70 and \< 80% |
| 108 | \#204f16 | Tree Cover \>\= 80 and \< 90% |
| 109 | \#003300 | Tree Cover \>\= 90 and \<\= 100% |
| 111 | \#d4b27d | Shrub Cover \>\= 10 and \< 20% |
| 112 | \#d1a171 | Shrub Cover \>\= 20 and \< 30% |
| 113 | \#cc9166 | Shrub Cover \>\= 30 and \< 40% |
| 114 | \#c77e5a | Shrub Cover \>\= 40 and \< 50% |
| 115 | \#c26e4f | Shrub Cover \>\= 50 and \< 60% |
| 116 | \#bd5e46 | Shrub Cover \>\= 60 and \< 70% |
| 117 | \#b54c3c | Shrub Cover \>\= 70 and \< 80% |
| 118 | \#b03b33 | Shrub Cover \>\= 80 and \< 90% |
| 119 | \#9e0020 | Shrub Cover \>\= 90 and \<\= 100% |
| 121 | \#ffcc66 | Herb Cover \>\= 10 and \< 20% |
| 122 | \#ffba59 | Herb Cover \>\= 20 and \< 30% |
| 123 | \#ffa94d | Herb Cover \>\= 30 and \< 40% |
| 124 | \#ff9a42 | Herb Cover \>\= 40 and \< 50% |
| 125 | \#ff8636 | Herb Cover \>\= 50 and \< 60% |
| 126 | \#ff752b | Herb Cover \>\= 60 and \< 70% |
| 127 | \#ff6421 | Herb Cover \>\= 70 and \< 80% |
| 128 | \#ff5517 | Herb Cover \>\= 80 and \< 90% |
| 129 | \#ff3300 | Herb Cover \>\= 90 and \<\= 100% |
| 150 | \#7a7f75 | Sparse Vegetation Canopy |
| 151 | \#ccff99 | Tree Canopy \>\= 10 and \< 25% |
| 152 | \#467832 | Tree Canopy \>\= 25 and \< 60% |
| 153 | \#003300 | Tree Canopy \>\= 60 and \<\= 100% |
| 161 | \#d4b27d | Shrub Canopy \>\= 10 and \< 25% |
| 162 | \#c26e4f | Shrub Canopy \>\= 25 and \< 60% |
| 163 | \#9e0020 | Shrub Canopy \>\= 60 and \<\= 100% |
| 171 | \#ffa94d | Herb Canopy \>\= 10 and \< 60% |
| 172 | \#ff752b | Herb Canopy \>\= 60 and \<\= 100% |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| EVC\_classes | DOUBLE | Class values of the Existing Vegetation Cover. |
| EVC\_names | STRING | Descriptive names of the Existing Vegetation Cover. |




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
vardataset=ee.ImageCollection('LANDFIRE/Vegetation/EVC/v1_4_0');

varvisualization={
bands:['EVC'],
};

Map.setCenter(-121.671,40.699,5);

Map.addLayer(dataset,visualization,'EVC');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Vegetation_EVC_v1_4_0)


[LANDFIRE EVC (Existing Vegetation Cover) v1\.4\.0](/earth-engine/datasets/catalog/LANDFIRE_Vegetation_EVC_v1_4_0)

LANDFIRE (LF), Landscape Fire and Resource Management Planning Tools, is a shared program between the wildland fire management programs of the U.S. Department of Agriculture's Forest Service, U.S. Department of the Interior's Geological Survey, and The Nature Conservancy. LANDFIRE (LF) layers are created using predictive landscape models based on extensive …

 LANDFIRE/Vegetation/EVC/v1\_4\_0,
 doi,fire,forest\-biomass,landfire,nature\-conservancy,usda,usgs,vegetation,wildfire

2014\-09\-01T00:00:00Z/2014\-09\-01T00:00:00Z



 17\.52 \-175\.1 71\.48 \-63\.66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








