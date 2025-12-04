



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

US Lithology


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================








Dataset Availability
2006\-01\-24T00:00:00Z–2011\-05\-13T00:00:00Z
Dataset Provider


[Conservation Science Partners](https://www.csp-inc.org/)



Earth Engine Snippet


`ee.Image("CSP/ERGo/1_0/US/lithology")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSP/CSP_ERGo_1_0_US_lithology)





Tags


[aspect](/earth-engine/datasets/tags/aspect)
[csp](/earth-engine/datasets/tags/csp)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[ergo](/earth-engine/datasets/tags/ergo)
[geophysical](/earth-engine/datasets/tags/geophysical)
[landforms](/earth-engine/datasets/tags/landforms)
[slope](/earth-engine/datasets/tags/slope)
[topography](/earth-engine/datasets/tags/topography)
[us](/earth-engine/datasets/tags/us)








#### Description



The Lithology dataset provides classes of the general types of parent
material of soil on the surface. It is not derived from any DEM.


The Conservation Science Partners (CSP) Ecologically Relevant Geomorphology
(ERGo) Datasets, Landforms and Physiography contain detailed, multi\-scale
data on landforms and physiographic (aka land facet) patterns. Although
there are many potential uses of these data, the original purpose for these
data was to develop an ecologically relevant classification and map of
landforms and physiographic classes that are suitable for climate adaptation
planning. Because there is large uncertainty associated with future climate
conditions and even more uncertainty around ecological responses, providing
information about what is unlikely to change offers a strong foundation for
managers to build robust climate adaptation plans. The quantification of
these features of the landscape is sensitive to the resolution, so we
provide the highest resolution possible given the extent and characteristics
of a given index.





### Bands



**Pixel Size**
  
90 meters



**Bands**




| Name | Description |
| --- | --- |
| `b1` | Lithology classes |


**b1 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#356eff | Water |
| 1 | \#acb6da | Carbonate |
| 3 | \#d6b879 | Non\-carbonate |
| 4 | \#313131 | Alkaline intrusive |
| 5 | \#eda800 | Silicic residual |
| 7 | \#616161 | Extrusive volcanic |
| 8 | \#d6d6d6 | Colluvial sediment |
| 9 | \#d0ddae | Glacial till clay |
| 10 | \#b8d279 | Glacial till loam |
| 11 | \#d5d378 | Glacial till coarse |
| 13 | \#141414 | Glacial lake sediment fine |
| 14 | \#6db155 | Glacial outwash coarse |
| 15 | \#9b6d55 | Hydric |
| 16 | \#feeec9 | Eolian sediment coarse |
| 17 | \#d6b879 | Eolian sediment fine |
| 18 | \#00b7ec | Saline lake sediment |
| 19 | \#ffda90 | Alluvium and coastal sediment fine |
| 20 | \#f8b28c | Coastal sediment coarse |




### Terms of Use


**Terms of Use**


[CC\-BY\-NC\-SA\-4\.0](https://spdx.org/licenses/CC-BY-NC-SA-4.0.html)




### Citations



Citations:
* Theobald, D. M., Harrison\-Atlas, D., Monahan, W. B., \& Albano, C. M.
(2015\). Ecologically\-relevant maps of landforms and physiographic diversity
for climate adaptation planning. PloS one, 10(12\),
[e0143619](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0143619)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('CSP/ERGo/1_0/US/lithology');
varlithology=dataset.select('b1');
varlithologyVis={
min:0.0,
max:20.0,
palette:[
'356eff','acb6da','d6b879','313131','eda800','616161','d6d6d6',
'd0ddae','b8d279','d5d378','141414','6db155','9b6d55','feeec9',
'd6b879','00b7ec','ffda90','f8b28c'
],
};
Map.setCenter(-105.8636,40.3439,11);
Map.addLayer(lithology,lithologyVis,'Lithology');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSP/CSP_ERGo_1_0_US_lithology)


[US Lithology](/earth-engine/datasets/catalog/CSP_ERGo_1_0_US_lithology)

The Lithology dataset provides classes of the general types of parent material of soil on the surface. It is not derived from any DEM. The Conservation Science Partners (CSP) Ecologically Relevant Geomorphology (ERGo) Datasets, Landforms and Physiography contain detailed, multi\-scale data on landforms and physiographic (aka land facet) patterns. Although …

 CSP/ERGo/1\_0/US/lithology,
 aspect,csp,elevation,elevation\-topography,ergo,geophysical,landforms,slope,topography,us

2006\-01\-24T00:00:00Z/2011\-05\-13T00:00:00Z



 12\.54 \-132\.09 56\.21 \-60\.35
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








