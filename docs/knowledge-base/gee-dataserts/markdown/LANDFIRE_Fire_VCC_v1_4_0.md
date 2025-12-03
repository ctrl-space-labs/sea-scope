



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

LANDFIRE VCC (Vegetation Condition Class) v1\.4\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================








Dataset Availability
2014\-09\-01T00:00:00Z–2014\-09\-01T00:00:00Z
Dataset Provider


[U.S. Department of Agriculture's (USDA), U.S. Forest Service (USFS), U.S.
Department of the Interior's Geological Survey (USGS), and The Nature Conservancy.](https://landfire.gov/)



Earth Engine Snippet


`ee.ImageCollection("LANDFIRE/Fire/VCC/v1_4_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Fire_VCC_v1_4_0)





Tags


[doi](/earth-engine/datasets/tags/doi)
[fire](/earth-engine/datasets/tags/fire)
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


Landfire (LF) Historical fire regimes, intervals, and vegetation conditions
are mapped using the Vegetation Dynamics Development Tool (VDDT).
These data support fire and landscape management planning goals in
the National Cohesive Wildland Fire Management Strategy, the Federal Wildland
Fire Management Policy, and the Healthy Forests Restoration Act.


Vegetation Condition Class (VCC) represents a simple categorization of the associated Vegetation Departure (VDEP) layer and indicates the general level to which current vegetation is different from the simulated historical vegetation reference conditions.
VDEP and VCC are based upon methods originally described in Interagency Fire Regime Condition Class Guidebook, but are not identical to those methods.
Full descriptions of the methods used can be found in the VDEP product description.
Users should review those methods before comparing VDEP or VCC values across LANDFIRE (LF) versions.
VCC is a derivative of the VDEP layer.
It is important to read and understand the characteristics of the VDEP spatial product, particularly if VCC values are compared across versions as the VDEP methods varied which directly impacts across\-version VDEP and VCC comparability.
In LF 2012, the original three VCC classes were divided in half to create six VCC classes to provide additional precision.


The LANDIFRE Fire datasets include:


* Fire Regime Groups (FRG) is intended to characterize presumed historical
fire regimes within landscapes based on interactions between vegetation
dynamics, fire spread, fire effects, and spatial context
* Mean Fire Return Interval (MFRI) quantifies the average period between
fires under the presumed historical fire regime
* Percent of Low\-severity Fire (PLS) image quantifies the amount of
low\-severity fires relative to mixed\- and replacement\-severity fires
under the presumed historical fire regime and is defined as less than 25
percent average top\-kill within a typical fire perimeter for a given
vegetation type
* Percent of Mixed\-severity Fire (PMS) layer quantifies the amount of
mixed\-severity fires relative to low\- and replacement\-severity fires under
the presumed historical fire regime, and is defined as between 25 and 75
percent average top\-kill within a typical fire perimeter for a given
vegetation type
* Percent of Replacement\-severity Fire (PRS) layer quantifies the amount of
replacement\-severity fires relative to low\- and mixed\-severity fires under
the presumed historical fire regime, and is defined as greater than 75
percent average top\-kill within a typical fire perimeter for a given
vegetation type
* Succession Classes (SClass) layer characterizes current vegetation conditions
with respect to the vegetation species composition, cover, and height ranges
of successional states that occur within each biophysical setting
* Vegetation Condition Class (VCC) represents a simple categorization of the
associated Vegetation Departure (VDEP) layer and indicates the general level
to which current vegetation is different from the simulated historical
vegetation reference conditions
* Vegetation Departure (VDep) indicates how different current vegetation on a
landscape is from estimated historical conditions. VDep is based on changes
to species composition, structural stage, and canopy closure.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `VCC` | Vegetation Condition Class |


**VCC Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#38a800 | Very Low, Vegetation Departure 0\-16% |
| 2 | \#4ce600 | Low to Moderate, Vegetation Departure 17\-33% |
| 3 | \#ffff00 | Moderate to Low, Vegetation Departure 34\-50% |
| 4 | \#ffaa00 | Moderate to High, Vegetation Departure 51\-66% |
| 5 | \#ff0000 | High, Vegetation Departure 67\-83% |
| 6 | \#a80000 | Very High, Vegetation Departure 84\-100% |
| 111 | \#0000ff | Water |
| 112 | \#c8ffff | Snow / Ice |
| 120 | \#8400a8 | Non burnable Urban |
| 121 | \#f516b6 | Burnable Urban |
| 131 | \#4e4e4e | Barren |
| 132 | \#b2b2b2 | Sparsely Vegetated |
| 180 | \#df73ff | Non burnable Agriculture |
| 181 | \#e8beff | Burnable Agriculture |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| VCC\_classes | DOUBLE | Class values of the Vegetation Condition Class. |
| VCC\_names | STRING | Descriptive names of Vegetation Condition Class. |




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
vardataset=ee.ImageCollection('LANDFIRE/Fire/VCC/v1_4_0');

varvisualization={
bands:['VCC'],
};

Map.setCenter(-121.671,40.699,5);

Map.addLayer(dataset,visualization,'VCC');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Fire_VCC_v1_4_0)


[LANDFIRE VCC (Vegetation Condition Class) v1\.4\.0](/earth-engine/datasets/catalog/LANDFIRE_Fire_VCC_v1_4_0)

LANDFIRE (LF), Landscape Fire and Resource Management Planning Tools, is a shared program between the wildland fire management programs of the U.S. Department of Agriculture's Forest Service, U.S. Department of the Interior's Geological Survey, and The Nature Conservancy. Landfire (LF) Historical fire regimes, intervals, and vegetation conditions are mapped using …

 LANDFIRE/Fire/VCC/v1\_4\_0,
 doi,fire,landfire,nature\-conservancy,usda,usgs,vegetation,wildfire

2014\-09\-01T00:00:00Z/2014\-09\-01T00:00:00Z



 17\.52 \-175\.1 71\.48 \-63\.66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








