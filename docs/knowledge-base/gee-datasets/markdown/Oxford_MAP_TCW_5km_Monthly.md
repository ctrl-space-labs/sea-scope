



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Oxford MAP TCW: Malaria Atlas Project Gap\-Filled Tasseled Cap Wetness


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================================








Dataset Availability
2001\-02\-01T00:00:00Z–2015\-01\-01T00:00:00Z
Dataset Provider


[Oxford Malaria Atlas Project](https://www.bdi.ox.ac.uk/research/malaria-atlas-project)



Earth Engine Snippet


`ee.ImageCollection("Oxford/MAP/TCW_5km_Monthly")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Oxford/Oxford_MAP_TCW_5km_Monthly)





Cadence
1 Month
Tags


[map](/earth-engine/datasets/tags/map)
[oxford](/earth-engine/datasets/tags/oxford)
[tasseled\-cap](/earth-engine/datasets/tags/tasseled-cap)
[tcb](/earth-engine/datasets/tags/tcb)
[vegetation\-indices](/earth-engine/datasets/tags/vegetation-indices)
wetness








#### Description



This gap\-filled Tasseled Cap Wetness (TCW) dataset was created by applying
the tasseled\-cap equations defined in Lobser and Cohen (2007\) to
MODIS BRDF\-corrected imagery (MCD43B4\). The resulting data were
gap\-filled using the approach outlined in Weiss et al. (2014\) to eliminate
missing data caused by factors such as cloud cover, and then the data were
aggregated temporally and spatially to produce the monthly ≈5km product.


This dataset was produced by Harry Gibson and Daniel Weiss of the
Malaria Atlas Project (Big Data Institute, University of Oxford,
United Kingdom, <https://malariaatlas.org/>).





### Bands



**Pixel Size**
  
5000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `Mean` | None | \-0\.84\* | 0\.96\* | The mean value of Tasseled Cap Wetness for each aggregated pixel. |
| `FilledProportion` | % | 0\* | 100\* | A quality control band that indicates the percentage of each resulting pixel that was comprised of raw data (as opposed to gap\-filled estimates). |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-NC\-SA\-4\.0](https://spdx.org/licenses/CC-BY-NC-SA-4.0.html)




### Citations



Citations:
* Weiss, D.J., P.M. Atkinson, S. Bhatt, B. Mappin, S.I. Hay \& P.W. Gething
(2014\) An effective approach for gap\-filling continental scale remotely
sensed time\-series. ISPRS Journal of Photogrammetry and Remote Sensing,
98, 106\-118\.
* Lobser, S.E. \& Cohen, W.B. (2007\) MODIS tasselled cap: land cover
characteristics expressed through transformed MODIS data. International
Journal of Remote Sensing, 28, 5079\-5101\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('Oxford/MAP/TCW_5km_Monthly')
.filter(ee.Filter.date('2013-01-01','2013-12-31'));
vartcw=dataset.select('Mean');
vartcwVis={
min:-0.6,
max:0.5,
palette:[
'ffffff','fcd163','99b718','66a000','3e8601','207401','056201',
'004c00','011301'
],
};
Map.setCenter(-44.65,22.59,2);
Map.addLayer(tcw,tcwVis,'TCW');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Oxford/Oxford_MAP_TCW_5km_Monthly)


[Oxford MAP TCW: Malaria Atlas Project Gap\-Filled Tasseled Cap Wetness](/earth-engine/datasets/catalog/Oxford_MAP_TCW_5km_Monthly)

This gap\-filled Tasseled Cap Wetness (TCW) dataset was created by applying the tasseled\-cap equations defined in Lobser and Cohen (2007\) to MODIS BRDF\-corrected imagery (MCD43B4\). The resulting data were gap\-filled using the approach outlined in Weiss et al. (2014\) to eliminate missing data caused by factors such as cloud cover, …

 Oxford/MAP/TCW\_5km\_Monthly,
 map,oxford,tasseled\-cap,tcb,vegetation\-indices

2001\-02\-01T00:00:00Z/2015\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








