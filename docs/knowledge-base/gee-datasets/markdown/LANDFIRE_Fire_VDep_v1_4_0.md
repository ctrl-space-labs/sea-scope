



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

LANDFIRE VDep (Vegetation Departure) v1\.4\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================================








Dataset Availability
2014\-09\-01T00:00:00Z–2014\-09\-01T00:00:00Z
Dataset Provider


[U.S. Department of Agriculture's (USDA), U.S. Forest Service (USFS), U.S.
Department of the Interior's Geological Survey (USGS), and The Nature Conservancy.](https://landfire.gov/)



Earth Engine Snippet


`ee.ImageCollection("LANDFIRE/Fire/VDep/v1_4_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Fire_VDep_v1_4_0)





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


Vegetation Departure (VDep) indicates how different current vegetation on a landscape is from estimated historical conditions.
VDep is based on changes to species composition, structural stage, and canopy closure using methods originally described in the Interagency Fire Regime Condition Class Guidebook, but is not identical to those methods.
LANDFIRE (LF) VDep is based only on departure of current vegetation conditions from reference vegetation conditions, whereas the Guidebook approach includes departure of current fire regimes from those of the reference period.
VDep is a landscape metric and is scale dependent. Every pixel in a unique biophysical settings (BpS) in a summary unit has the same VDep value.
These large landscape values may not represent smaller areas within a summary unit.
The VDep metric ranges from 0 \- 100, and is based on four factors. These inputs are held constant within a single version of LF, but can be different across LF versions, which directly impacts VDep comparability across versions.
VDep can be compared across versions but caution is advised.


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
| `VDep` | Vegetation Departure |


**VDep Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#00f0ff | 0 |
| 1 | \#00e5ee | 1 |
| 2 | \#00dadd | 2 |
| 3 | \#00cfcc | 3 |
| 4 | \#00c4bb | 4 |
| 5 | \#00b9aa | 5 |
| 6 | \#00ae99 | 6 |
| 7 | \#00a388 | 7 |
| 8 | \#009877 | 8 |
| 9 | \#008d66 | 9 |
| 10 | \#008255 | 10 |
| 11 | \#007744 | 11 |
| 12 | \#006c33 | 12 |
| 13 | \#006122 | 13 |
| 14 | \#005611 | 14 |
| 15 | \#004b00 | 15 |
| 16 | \#0e5900 | 16 |
| 17 | \#1c6600 | 17 |
| 18 | \#2a7400 | 18 |
| 19 | \#388100 | 19 |
| 20 | \#468f00 | 20 |
| 21 | \#549c00 | 21 |
| 22 | \#62aa00 | 22 |
| 23 | \#70b700 | 23 |
| 24 | \#7ec500 | 24 |
| 25 | \#8cd200 | 25 |
| 26 | \#9ad815 | 26 |
| 27 | \#a9dd2b | 27 |
| 28 | \#b7e340 | 28 |
| 29 | \#c6e955 | 29 |
| 30 | \#d4ee6a | 30 |
| 31 | \#e2f480 | 31 |
| 32 | \#f1f995 | 32 |
| 33 | \#ffffaa | 33 |
| 34 | \#ffffa0 | 34 |
| 35 | \#ffff96 | 35 |
| 36 | \#ffff8c | 36 |
| 37 | \#ffff82 | 37 |
| 38 | \#ffff78 | 38 |
| 39 | \#ffff6e | 39 |
| 40 | \#ffff64 | 40 |
| 41 | \#ffff5a | 41 |
| 42 | \#ffff50 | 42 |
| 43 | \#ffff46 | 43 |
| 44 | \#ffff3c | 44 |
| 45 | \#ffff32 | 45 |
| 46 | \#ffff28 | 46 |
| 47 | \#ffff1e | 47 |
| 48 | \#ffff14 | 48 |
| 49 | \#ffff0a | 49 |
| 50 | \#ffff00 | 50 |
| 51 | \#fff500 | 51 |
| 52 | \#ffeb00 | 52 |
| 53 | \#ffe000 | 53 |
| 54 | \#ffd600 | 54 |
| 55 | \#ffcc00 | 55 |
| 56 | \#ffc200 | 56 |
| 57 | \#ffb800 | 57 |
| 58 | \#ffad00 | 58 |
| 59 | \#ffa300 | 59 |
| 60 | \#ff9900 | 60 |
| 61 | \#ff8f00 | 61 |
| 62 | \#ff8500 | 62 |
| 63 | \#ff7a00 | 63 |
| 64 | \#ff7000 | 64 |
| 65 | \#ff6600 | 65 |
| 66 | \#ff5c00 | 66 |
| 67 | \#ff5200 | 67 |
| 68 | \#ff4700 | 68 |
| 69 | \#ff3d00 | 69 |
| 70 | \#ff3300 | 70 |
| 71 | \#ff2900 | 71 |
| 72 | \#ff1f00 | 72 |
| 73 | \#ff1400 | 73 |
| 74 | \#ff0a00 | 74 |
| 75 | \#ff0000 | 75 |
| 76 | \#fb0000 | 76 |
| 77 | \#f70000 | 77 |
| 78 | \#f20000 | 78 |
| 79 | \#ee0000 | 79 |
| 80 | \#ea0000 | 80 |
| 81 | \#e60000 | 81 |
| 82 | \#e10000 | 82 |
| 83 | \#dd0000 | 83 |
| 84 | \#d90000 | 84 |
| 85 | \#d50000 | 85 |
| 86 | \#d00000 | 86 |
| 87 | \#cc0000 | 87 |
| 88 | \#c80000 | 88 |
| 89 | \#c40000 | 89 |
| 90 | \#c00000 | 90 |
| 91 | \#bb0000 | 91 |
| 92 | \#b70000 | 92 |
| 93 | \#b30000 | 93 |
| 94 | \#af0000 | 94 |
| 95 | \#aa0000 | 95 |
| 96 | \#a60000 | 96 |
| 97 | \#a20000 | 97 |
| 98 | \#9e0000 | 98 |
| 99 | \#990000 | 99 |
| 100 | \#950000 | 100 |
| 101 | \#000000 | Departure not calculated |
| 111 | \#0000ff | Water |
| 112 | \#c8ffff | Snow / Ice |
| 120 | \#8400a8 | Non\-burnable Urban |
| 121 | \#8418a8 | Burnable Urban |
| 131 | \#4e4e4e | Barren |
| 132 | \#b2b2b2 | Sparse Vegetation |
| 180 | \#df73ff | Non\-burnable Agriculture |
| 181 | \#df73f0 | Burnable Agriculture |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| VDep\_classes | DOUBLE | Class values of the Vegetation Departure. |
| VDep\_names | STRING | Descriptive names of Vegetation Departure. |




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
vardataset=ee.ImageCollection('LANDFIRE/Fire/VDep/v1_4_0');

varvisualization={
bands:['VDep'],
};

Map.setCenter(-121.671,40.699,5);

Map.addLayer(dataset,visualization,'VDep');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDFIRE/LANDFIRE_Fire_VDep_v1_4_0)


[LANDFIRE VDep (Vegetation Departure) v1\.4\.0](/earth-engine/datasets/catalog/LANDFIRE_Fire_VDep_v1_4_0)

LANDFIRE (LF), Landscape Fire and Resource Management Planning Tools, is a shared program between the wildland fire management programs of the U.S. Department of Agriculture's Forest Service, U.S. Department of the Interior's Geological Survey, and The Nature Conservancy. Landfire (LF) Historical fire regimes, intervals, and vegetation conditions are mapped using …

 LANDFIRE/Fire/VDep/v1\_4\_0,
 doi,fire,landfire,nature\-conservancy,usda,usgs,vegetation,wildfire

2014\-09\-01T00:00:00Z/2014\-09\-01T00:00:00Z



 17\.52 \-175\.1 71\.48 \-63\.66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








