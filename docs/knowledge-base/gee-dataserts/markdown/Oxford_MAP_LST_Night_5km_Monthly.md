



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Oxford MAP LST: Malaria Atlas Project Gap\-Filled Nighttime Land Surface Temperature


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================================================








Dataset Availability
2001\-03\-01T00:00:00Z–2015\-06\-01T00:00:00Z
Dataset Provider


[Oxford Malaria Atlas Project](https://www.bdi.ox.ac.uk/research/malaria-atlas-project)



Earth Engine Snippet


`ee.ImageCollection("Oxford/MAP/LST_Night_5km_Monthly")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Oxford/Oxford_MAP_LST_Night_5km_Monthly)





Cadence
1 Month
Tags


[climate](/earth-engine/datasets/tags/climate)
[lst](/earth-engine/datasets/tags/lst)
[map](/earth-engine/datasets/tags/map)
[oxford](/earth-engine/datasets/tags/oxford)
[surface\-temperature](/earth-engine/datasets/tags/surface-temperature)








#### Description



The underlying dataset for this nighttime product is MODIS land surface
temperature data (MOD11A2\), which was gap\-filled using the approach outlined
in Weiss et al. (2014\) to eliminate missing data caused by factors such as
cloud cover. Gap\-free outputs were then aggregated temporally and spatially
to produce the monthly ≈5km product.


This dataset was produced by Harry Gibson and Daniel Weiss of the
Malaria Atlas Project (Big Data Institute, University of Oxford,
United Kingdom, <https://malariaatlas.org/>).





### Bands



**Pixel Size**
  
5000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `Mean` | °C | \-73\.39\* | 37\.64\* | The mean value of nighttime land surface temperature for each aggregated pixel. |
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





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('Oxford/MAP/LST_Night_5km_Monthly')
.filter(ee.Filter.date('2015-01-01','2015-12-31'));
varnighttimeLandSurfaceTemp=dataset.select('Mean');
varvisParams={
min:-30.0,
max:30.0,
palette:[
'800080','0000ab','0000ff','008000','19ff2b','a8f7ff','ffff00',
'd6d600','ffa500','ff6b01','ff0000'
],
};
Map.setCenter(-88.6,26.4,1);
Map.addLayer(
nighttimeLandSurfaceTemp,visParams,'Nighttime Land Surface Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Oxford/Oxford_MAP_LST_Night_5km_Monthly)


[Oxford MAP LST: Malaria Atlas Project Gap\-Filled Nighttime Land Surface Temperature](/earth-engine/datasets/catalog/Oxford_MAP_LST_Night_5km_Monthly)

The underlying dataset for this nighttime product is MODIS land surface temperature data (MOD11A2\), which was gap\-filled using the approach outlined in Weiss et al. (2014\) to eliminate missing data caused by factors such as cloud cover. Gap\-free outputs were then aggregated temporally and spatially to produce the monthly ≈5km …

 Oxford/MAP/LST\_Night\_5km\_Monthly,
 climate,lst,map,oxford,surface\-temperature

2001\-03\-01T00:00:00Z/2015\-06\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








