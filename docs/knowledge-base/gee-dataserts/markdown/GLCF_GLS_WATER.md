



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GLCF: Landsat Global Inland Water


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2000\-12\-31T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MEASURES/GFCC/GFCC30WC.001)



Earth Engine Snippet


`ee.ImageCollection("GLCF/GLS_WATER")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GLCF/GLCF_GLS_WATER)





Tags


[glcf](/earth-engine/datasets/tags/glcf)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[nasa](/earth-engine/datasets/tags/nasa)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[umd](/earth-engine/datasets/tags/umd)
[water](/earth-engine/datasets/tags/water)








#### Description



The Global Inland Water dataset shows inland surface water bodies, including
fresh and saline lakes, rivers, and reservoirs.


From the GLS 2000 epoch, 3,650,723 km2 of inland water were identified,
around three quarters of which were in North America and Asia. Boreal
forests and tundra hold the largest portion of inland water, about 40% of
the global total. The data exhibits strong linear correlation with both the
MODIS dataset as well as 30\-m resolution datasets over the United States
and Canada. Residual errors were due primarily to the seasonality of water
cover, snow and ice, and residual clouds.


The dataset contains one or more image for each available Landsat WRS2
path/row.


Documentation:


* [User's guide](https://lpdaac.usgs.gov/documents/1371/GFCC_User_Guide_V1.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/1370/GFCC_ATBD.pdf)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `water` | Water classification |


**water Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#fafafa | Land |
| 2 | \#00c5ff | Water |
| 4 | \#df73ff | Snow/ice |
| 200 | \#828282 | Cloud shadow |
| 201 | \#cccccc | Cloud |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| path | DOUBLE | Path |
| pathrow | STRING | Path and row |
| row | DOUBLE | Row |
| water\_class\_names | DOUBLE | Water class names |
| water\_class\_palette | DOUBLE | Water class palette |
| water\_class\_values | INT\_LIST | Water class values |




### Terms of Use


**Terms of Use**


Intellectual property rights to this dataset belong to University of
Maryland, Department of Geographical Sciences and NASA. Usage is free if
acklowedgement is made.




### Citations



Citations:
* Data Citation: Global Inland Water, {Year, ...}, Global Land Cover
Facility.
* Paper/Methods Citation: Feng, Min, Joseph O. Sexton, Saurabh Channan,
and John R. Townshend. 2015\. [A Global, High\-Resolution (30\-M) Inland Water
Body Dataset for 2000: First Results of a Topographic\-Spectral
Classification Algorithm](https://www.tandfonline.com/doi/pdf/10.1080/17538947.2015.1026420).
International Journal of Digital Earth.
[doi:10\.1080/17538947\.2015\.1026420](https://doi.org/10.1080/17538947.2015.1026420).





### DOIs


* [https://doi.org/10\.1080/17538947\.2015\.1026420](https://doi.org/10.1080/17538947.2015.1026420)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('GLCF/GLS_WATER');
varwater=dataset.select('water');
varwaterVis={
min:1.0,
max:4.0,
palette:['fafafa','00c5ff','df73ff','828282','cccccc'],
};
Map.setCenter(-79.3094,44.5693,8);
Map.addLayer(water,waterVis,'Water');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GLCF/GLCF_GLS_WATER)


[GLCF: Landsat Global Inland Water](/earth-engine/datasets/catalog/GLCF_GLS_WATER)

The Global Inland Water dataset shows inland surface water bodies, including fresh and saline lakes, rivers, and reservoirs. From the GLS 2000 epoch, 3,650,723 km2 of inland water were identified, around three quarters of which were in North America and Asia. Boreal forests and tundra hold the largest portion of …

 GLCF/GLS\_WATER,
 glcf,landsat\-derived,nasa,surface\-ground\-water,umd,water

2000\-01\-01T00:00:00Z/2000\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1080/17538947\.2015\.1026420](https://doi.org/https://doi.org/10.5067/MEASURES/GFCC/GFCC30WC.001)
* [https://doi.org/10\.1080/17538947\.2015\.1026420](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/GLCF_GLS_WATER)









