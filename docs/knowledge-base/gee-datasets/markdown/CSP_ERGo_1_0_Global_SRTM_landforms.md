



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global SRTM Landforms


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================








Dataset Availability
2006\-01\-24T00:00:00Z–2011\-05\-13T00:00:00Z
Dataset Provider


[Conservation Science Partners](https://www.csp-inc.org/)



Earth Engine Snippet


`ee.Image("CSP/ERGo/1_0/Global/SRTM_landforms")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSP/CSP_ERGo_1_0_Global_SRTM_landforms)





Tags


[aspect](/earth-engine/datasets/tags/aspect)
[csp](/earth-engine/datasets/tags/csp)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[ergo](/earth-engine/datasets/tags/ergo)
[geophysical](/earth-engine/datasets/tags/geophysical)
[global](/earth-engine/datasets/tags/global)
[landforms](/earth-engine/datasets/tags/landforms)
[slope](/earth-engine/datasets/tags/slope)
[topography](/earth-engine/datasets/tags/topography)








#### Description



The SRTM Landform dataset provides landform classes created by combining
the Continuous Heat\-Insolation Load Index (SRTM CHILI) and the
multi\-scale Topographic Position Index (SRTM mTPI) datasets. It is
based on the 30m SRTM DEM (available in EE as USGS/SRTMGL1\_003\).


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
| `constant` | SRTM\-derived landform classes |


**constant Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 11 | \#141414 | Peak/ridge (warm) |
| 12 | \#383838 | Peak/ridge |
| 13 | \#808080 | Peak/ridge (cool) |
| 14 | \#ebeb8f | Mountain/divide |
| 15 | \#f7d311 | Cliff |
| 21 | \#aa0000 | Upper slope (warm) |
| 22 | \#d89382 | Upper slope |
| 23 | \#ddc9c9 | Upper slope (cool) |
| 24 | \#dccdce | Upper slope (flat) |
| 31 | \#1c6330 | Lower slope (warm) |
| 32 | \#68aa63 | Lower slope |
| 33 | \#b5c98e | Lower slope (cool) |
| 34 | \#e1f0e5 | Lower slope (flat) |
| 41 | \#a975ba | Valley |
| 42 | \#6f198c | Valley (narrow) |




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
vardataset=ee.Image('CSP/ERGo/1_0/Global/SRTM_landforms');
varlandforms=dataset.select('constant');
varlandformsVis={
min:11.0,
max:42.0,
palette:[
'141414','383838','808080','ebeb8f','f7d311','aa0000','d89382',
'ddc9c9','dccdce','1c6330','68aa63','b5c98e','e1f0e5','a975ba',
'6f198c'
],
};
Map.setCenter(-105.58,40.5498,11);
Map.addLayer(landforms,landformsVis,'Landforms');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSP/CSP_ERGo_1_0_Global_SRTM_landforms)


[Global SRTM Landforms](/earth-engine/datasets/catalog/CSP_ERGo_1_0_Global_SRTM_landforms)

The SRTM Landform dataset provides landform classes created by combining the Continuous Heat\-Insolation Load Index (SRTM CHILI) and the multi\-scale Topographic Position Index (SRTM mTPI) datasets. It is based on the 30m SRTM DEM (available in EE as USGS/SRTMGL1\_003\). The Conservation Science Partners (CSP) Ecologically Relevant Geomorphology (ERGo) Datasets, Landforms …

 CSP/ERGo/1\_0/Global/SRTM\_landforms,
 aspect,csp,elevation,elevation\-topography,ergo,geophysical,global,landforms,slope,topography

2006\-01\-24T00:00:00Z/2011\-05\-13T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








