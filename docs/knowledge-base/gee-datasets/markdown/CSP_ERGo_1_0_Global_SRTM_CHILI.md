



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global SRTM CHILI (Continuous Heat\-Insolation Load Index)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================================








Dataset Availability
2006\-01\-24T00:00:00Z–2011\-05\-13T00:00:00Z
Dataset Provider


[Conservation Science Partners](https://www.csp-inc.org/)



Earth Engine Snippet


`ee.Image("CSP/ERGo/1_0/Global/SRTM_CHILI")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSP/CSP_ERGo_1_0_Global_SRTM_CHILI)





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



CHILI is a surrogate for effects of insolation and topographic shading on
evapotranspiration represented by calculating insolation at early afternoon,
sun altitude equivalent to equinox. It is based on the 30m SRTM DEM
(available in EE as USGS/SRTMGL1\_003\).


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




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `constant` | 0 | 255 | SRTM\-derived CHILI index ranging from 0 (very cool) to 255 (very warm). This was rescaled from the \[0,1] range in the publication. |




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
vardataset=ee.Image('CSP/ERGo/1_0/Global/SRTM_CHILI');
varsrtmChili=dataset.select('constant');
varsrtmChiliVis={
min:0.0,
max:255.0,
};
Map.setCenter(-105.8636,40.3439,11);
Map.addLayer(srtmChili,srtmChiliVis,'SRTM CHILI');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSP/CSP_ERGo_1_0_Global_SRTM_CHILI)


[Global SRTM CHILI (Continuous Heat\-Insolation Load Index)](/earth-engine/datasets/catalog/CSP_ERGo_1_0_Global_SRTM_CHILI)

CHILI is a surrogate for effects of insolation and topographic shading on evapotranspiration represented by calculating insolation at early afternoon, sun altitude equivalent to equinox. It is based on the 30m SRTM DEM (available in EE as USGS/SRTMGL1\_003\). The Conservation Science Partners (CSP) Ecologically Relevant Geomorphology (ERGo) Datasets, Landforms and …

 CSP/ERGo/1\_0/Global/SRTM\_CHILI,
 aspect,csp,elevation,elevation\-topography,ergo,geophysical,global,landforms,slope,topography

2006\-01\-24T00:00:00Z/2011\-05\-13T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








