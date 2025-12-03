



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

FORMA Alert Thresholds


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================








Dataset Availability
2012\-01\-01T00:00:00Z–2016\-01\-01T00:00:00Z
Dataset Provider


[World Resources Institute / Global Forest Watch](https://www.globalforestwatch.org/)



Earth Engine Snippet


`ee.Image("WRI/GFW/FORMA/thresholds")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_GFW_FORMA_thresholds)





Tags


[daily](/earth-engine/datasets/tags/daily)
[deforestation](/earth-engine/datasets/tags/deforestation)
[fire](/earth-engine/datasets/tags/fire)
[forest](/earth-engine/datasets/tags/forest)
[forma](/earth-engine/datasets/tags/forma)
[gfw](/earth-engine/datasets/tags/gfw)
[modis](/earth-engine/datasets/tags/modis)
[monitoring](/earth-engine/datasets/tags/monitoring)
[wri](/earth-engine/datasets/tags/wri)








#### Description



**NOTE from WRI**: WRI decided to stop updating FORMA alerts. The goal was
to simplify the [Global Forest Watch](https://www.globalforestwatch.org)
user experience and reduce redundancy.
We found that [Terra\-i](http://www.terra-i.org/terra-i.html) and
[GLAD](https://glad-forest-alert.appspot.com/) were more frequently used.
Moreover, using GLAD as a standard, found that Terra\-i outperformed
FORMA globally.


FORMA alerts are detected using a combination of two MODIS
products: NDVI (Normalized Difference Vegetation Index) and FIRMS
(Fires Information for Resource Management System). NDVI updates are
processed every 16 days, while fire updates are processed daily. Models
are developed individually for each ecogroup to relate the two inputs to
the area of clearing, using the Hansen annual tree cover loss data to train
the model. The minimum threshold to qualify as an alert is 25% of the pixel
cleared, though thresholds vary by ecogroup to minimize false positives.
Here is an [example script](https://code.earthengine.google.com/f29b1e4360f3fc36847bd789ceeb20f6)
for a quick introduction to the FORMA datasets.


This image contains the thresholds at which, when crossed, a FORMA alert is
produced. The values are equal to max(25,40%\*RegionalMax), where RegionalMax
is the historical maximum clearing for a pixel in this ecogroup.





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `delta_bound` | % | 25 | 40 | The thresholds at which, when crossed, a FORMA alert is produced |




### Terms of Use


**Terms of Use**


The FORMA datasets are available without restriction
on use or distribution. WRI does request that the
user give proper attribution and identify WRI and GFW, where applicable,
as the source of the data.




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('WRI/GFW/FORMA/thresholds');
varthresholds=dataset.select('delta_bound');
varvisParams={
min:0,
max:50,
};
Map.setCenter(26,-8,3);
Map.addLayer(thresholds,visParams,'Thresholds for FORMA alerts');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_GFW_FORMA_thresholds)


[FORMA Alert Thresholds](/earth-engine/datasets/catalog/WRI_GFW_FORMA_thresholds)

NOTE from WRI: WRI decided to stop updating FORMA alerts. The goal was to simplify the Global Forest Watch user experience and reduce redundancy. We found that Terra\-i and GLAD were more frequently used. Moreover, using GLAD as a standard, found that Terra\-i outperformed FORMA globally. FORMA alerts are detected …

 WRI/GFW/FORMA/thresholds,
 daily,deforestation,fire,forest,forma,gfw,modis,monitoring,wri

2012\-01\-01T00:00:00Z/2016\-01\-01T00:00:00Z



 \-50 \-120 40 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








