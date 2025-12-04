



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

CSP gHM: Global Human Modification


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================








Dataset Availability
2016\-01\-01T00:00:00Z–2016\-12\-31T00:00:00Z
Dataset Provider


[Conservation Science Partners](https://www.csp-inc.org/)



Earth Engine Snippet


`ee.ImageCollection("CSP/HM/GlobalHumanModification")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSP/CSP_HM_GlobalHumanModification)





Cadence
1 Year
Tags


[csp](/earth-engine/datasets/tags/csp)
[fragmentation](/earth-engine/datasets/tags/fragmentation)
[human\-modification](/earth-engine/datasets/tags/human-modification)
[landcover](/earth-engine/datasets/tags/landcover)
[landscape\-gradient](/earth-engine/datasets/tags/landscape-gradient)
[population](/earth-engine/datasets/tags/population)
[stressors](/earth-engine/datasets/tags/stressors)
tnc








#### Description



The global Human Modification dataset (gHM) provides a cumulative measure of human modification
of terrestrial lands globally at 1 square\-kilometer resolution. The gHM
values range from 0\.0\-1\.0 and are calculated by estimating the proportion of a given location
(pixel) that is modified, the estimated intensity of modification
associated with a given type of human modification or "stressor".
5 major anthropogenic stressors circa 2016 were mapped using 13
individual datasets:


* human settlement (population density, built\-up areas)
* agriculture (cropland, livestock)
* transportation (major, minor, and two\-track roads; railroads)
* mining and energy production
* electrical infrastructure (power lines, nighttime lights)


Please see the paper for additional methodological details.
This asset was re\-projected to WGS84 for use in Earth Engine.





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `gHM` | km^2 | 0 | 1 | global Human Modification |




### Terms of Use


**Terms of Use**


[CC\-BY\-NC\-SA\-4\.0](https://spdx.org/licenses/CC-BY-NC-SA-4.0.html)




### Citations



Citations:
* Kennedy, C.M., J.R. Oakleaf, D.M. Theobald, S. Baruch\-Murdo, and J. Kiesecker. 2019\. Managing
the middle: A shift in conservation priorities based on the global human modification gradient.
Global Change Biology 00:1\-16\. [doi:10\.1111/gcb.14549](https://doi.org/10.1111/gcb.14549)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('CSP/HM/GlobalHumanModification');

varvisualization={
bands:['gHM'],
min:0.0,
max:1.0,
palette:['0c0c0c','071aff','ff0000','ffbd03','fbff05','fffdfd']
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Human modification');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSP/CSP_HM_GlobalHumanModification)


[CSP gHM: Global Human Modification](/earth-engine/datasets/catalog/CSP_HM_GlobalHumanModification)

The global Human Modification dataset (gHM) provides a cumulative measure of human modification of terrestrial lands globally at 1 square\-kilometer resolution. The gHM values range from 0\.0\-1\.0 and are calculated by estimating the proportion of a given location (pixel) that is modified, the estimated intensity of modification associated with a …

 CSP/HM/GlobalHumanModification,
 csp,fragmentation,human\-modification,landcover,landscape\-gradient,population,stressors

2016\-01\-01T00:00:00Z/2016\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








