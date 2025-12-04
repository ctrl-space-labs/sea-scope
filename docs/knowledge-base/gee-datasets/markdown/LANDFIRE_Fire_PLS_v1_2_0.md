



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

LANDFIRE PLS (Percent Low\-severity Fire) v1\.2\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2010\-12\-31T00:00:00Z
Dataset Provider


[U.S. Department of Agriculture's (USDA), U.S. Forest Service (USFS), U.S.
Department of the Interior's Geological Survey (USGS), and The Nature Conservancy.](https://landfire.gov/)



Earth Engine Snippet


`ee.ImageCollection("LANDFIRE/Fire/PLS/v1_2_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Fire_PLS_v1_2_0)





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


The Percent of Low\-severity Fire (PLS) layer quantifies the amount of low\-severity fires relative to mixed\- and replacement\-severity fires under the presumed historical fire regime.
Low severity is defined as less than 25 percent average top\-kill within a typical fire perimeter for a given vegetation type.
PLS was derived from the vegetation and disturbance dynamics model VDDT (Vegetation Dynamics Development Tool) (LF 1\.0\.0 CONUS only used the vegetation and disturbance dynamics model LANDSUM).
This layer is intended to describe one component of historical fire regime characteristics in the context of the broader historical time period represented by the LANDFIRE (LF) Biophysical Settings (BPS) layer and BPS Model documentation.
This layer is created by linking the BPS Group attribute in the BPS layer with the Refresh Model Tracker (RMT) data and assigning the PLS attribute.
This geospatial product should display a reasonable approximation of PLS, as documented in the RMT.
PLS is used in landscape assessments.


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
| `PLS` | Percent Low\-severity Fire |


**PLS Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#008200 | 0\-5% |
| 2 | \#138f00 | 6\-10% |
| 3 | \#229c00 | 11\-15% |
| 4 | \#34a600 | 16\-20% |
| 5 | \#47b300 | 21\-25% |
| 6 | \#66bf00 | 26\-30% |
| 7 | \#7ecc00 | 31\-35% |
| 8 | \#9bd900 | 36\-40% |
| 9 | \#b8e600 | 41\-45% |
| 10 | \#e2f200 | 46\-50% |
| 11 | \#fffb00 | 51\-55% |
| 12 | \#fadd00 | 56\-60% |
| 13 | \#f7c600 | 61\-65% |
| 14 | \#f5a300 | 66\-70% |
| 15 | \#f08c00 | 71\-75% |
| 16 | \#eb7100 | 76\-80% |
| 17 | \#e85d00 | 81\-85% |
| 18 | \#e63d00 | 86\-90% |
| 19 | \#e32a00 | 91\-95% |
| 20 | \#de1200 | 96\-100% |
| 111 | \#0000ff | Water |
| 112 | \#c8ffff | Snow / Ice |
| 131 | \#4e4e4e | Barren |
| 132 | \#b2b2b2 | Sparsely Vegetated |
| 133 | \#e1e1e1 | Indeterminate Fire Regime |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| PLS\_classes | DOUBLE | Class values of the Percent Low\-severity Fire. |
| PLS\_names | STRING | Descriptive names of Percent Low\-severity Fire. |




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
vardataset=ee.ImageCollection('LANDFIRE/Fire/PLS/v1_2_0');

varvisualization={
bands:['PLS'],
};

Map.setCenter(-121.671,40.699,5);

Map.addLayer(dataset,visualization,'PLS');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Fire_PLS_v1_2_0)


[LANDFIRE PLS (Percent Low\-severity Fire) v1\.2\.0](/earth-engine/datasets/catalog/LANDFIRE_Fire_PLS_v1_2_0)

LANDFIRE (LF), Landscape Fire and Resource Management Planning Tools, is a shared program between the wildland fire management programs of the U.S. Department of Agriculture's Forest Service, U.S. Department of the Interior's Geological Survey, and The Nature Conservancy. Landfire (LF) Historical fire regimes, intervals, and vegetation conditions are mapped using …

 LANDFIRE/Fire/PLS/v1\_2\_0,
 doi,fire,landfire,nature\-conservancy,usda,usgs,vegetation,wildfire

2010\-01\-01T00:00:00Z/2010\-12\-31T00:00:00Z



 17\.52 \-175\.1 71\.48 \-63\.66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








