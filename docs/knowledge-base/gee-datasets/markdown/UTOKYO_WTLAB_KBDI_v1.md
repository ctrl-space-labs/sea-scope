



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

KBDI: Keetch\-Byram Drought Index


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================








Dataset Availability
2007\-01\-01T00:00:00Z–2025\-07\-14T00:00:00Z
Dataset Provider


[Institute of Industrial Science, The University of Tokyo, Japan](http://wtlab.iis.u-tokyo.ac.jp/DMEWS/)



Earth Engine Snippet


`ee.ImageCollection("UTOKYO/WTLAB/KBDI/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UTOKYO/UTOKYO_WTLAB_KBDI_v1)





Cadence
1 Day
Tags


[drought](/earth-engine/datasets/tags/drought)
[fire](/earth-engine/datasets/tags/fire)
[rainfall](/earth-engine/datasets/tags/rainfall)
kbdi
lst\-derived
utokyo
wtlab








#### Description



Keetch\-Byram Drought Index (KBDI) is a continuous reference scale for estimating the dryness of
the soil and duff layers. The index increases for each day without rain (the amount of increase
depends on the daily high temperature) and decreases when it rains. This system is based
primarily on recent rainfall patterns. It is a measure of meteorological drought; it reflects
water gain or loss within the soil.


The scale ranges from 0 (no moisture deficit) to 800 (extreme drought). The range of the index
is determined by assuming that there is 20 cm of moisture in a saturated soil that is readily
available to the vegetation (Keetch and Byram, 1968\). KBDI is world widely used for drought
monitoring for national weather forecast, wildfire prevention and usefully especially in regions
with rain\-fed crops.





### Bands



**Pixel Size**
  
4000 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `KBDI` | 0 | 800 | Keetch\-Byram Drought Index |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Wataru Takeuchi, Soni Darmawan, Rizatus Shofiyati, Mai Van Khiem, Kyaw San Oo, Uday Pimple
and Suthy Heng, 2015\. Near\-real time meteorological drought monitoring and early warning
system for croplands in Asia.
36th Asian conference on remote sensing (ACRS): Manila, Philippines, Oct. 20, 2015\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcollection=ee.ImageCollection('UTOKYO/WTLAB/KBDI/v1')
.select('KBDI')
.filterDate('2019-01-01','2019-01-10');
varbandViz={
min:0,
max:800,
palette:[
'001a4d','003cb3','80aaff','336600','cccc00','cc9900','cc6600',
'660033'
]
};
Map.addLayer(collection.mean(),bandViz,'Keetch-Byram Drought Index');
Map.setCenter(120,3,3);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UTOKYO/UTOKYO_WTLAB_KBDI_v1)


[KBDI: Keetch\-Byram Drought Index](/earth-engine/datasets/catalog/UTOKYO_WTLAB_KBDI_v1)

Keetch\-Byram Drought Index (KBDI) is a continuous reference scale for estimating the dryness of the soil and duff layers. The index increases for each day without rain (the amount of increase depends on the daily high temperature) and decreases when it rains. This system is based primarily on recent rainfall …

 UTOKYO/WTLAB/KBDI/v1,
 drought,fire,rainfall

2007\-01\-01T00:00:00Z/2025\-07\-14T00:00:00Z



 \-60 60 60 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








