



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

FORMA Vegetation T\-Statistics


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================








Dataset Availability
2012\-01\-01T00:00:00Z–2019\-04\-23T00:00:00Z
Dataset Provider


[World Resources Institute / Global Forest Watch](https://www.globalforestwatch.org/)



Earth Engine Snippet


`ee.ImageCollection("WRI/GFW/FORMA/vegetation_tstats")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_GFW_FORMA_vegetation_tstats)





Tags


[daily](/earth-engine/datasets/tags/daily)
[deforestation](/earth-engine/datasets/tags/deforestation)
[forest](/earth-engine/datasets/tags/forest)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
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


The images in this ImageCollection contain the "reversed rectified
t\-statistics" used in calculating NTT, the vegetation color index derived
from MODIS NDVI that FORMA uses to measure browning. Using a sum reducer on
over various date ranges in this ImageCollection produces an "NTT" image.


The images are broken by "ecogroup".





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `tstat_r` | 0\* | 25\.41\* | Reversed rectified, ie (max(0,\-t\_stat)), t\-statistics. |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| year | INT | Year of the most recent data included in the dataset |
| biweekly | INT | The biweekly (every 16 days) period of the year |
| ecogroup\_id | STRING | ID of associated ecogroup |




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
vardataset=ee.ImageCollection('WRI/GFW/FORMA/vegetation_tstats')
.filter(ee.Filter.date('2018-07-01','2018-07-15'));
vartstat=dataset.select('tstat_r');
varvisParams={
min:0,
max:1,
};
Map.setCenter(26,-8,3);
Map.addLayer(tstat,visParams,'Reversed rectified t-statistics');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_GFW_FORMA_vegetation_tstats)


[FORMA Vegetation T\-Statistics](/earth-engine/datasets/catalog/WRI_GFW_FORMA_vegetation_tstats)

NOTE from WRI: WRI decided to stop updating FORMA alerts. The goal was to simplify the Global Forest Watch user experience and reduce redundancy. We found that Terra\-i and GLAD were more frequently used. Moreover, using GLAD as a standard, found that Terra\-i outperformed FORMA globally. FORMA alerts are detected …

 WRI/GFW/FORMA/vegetation\_tstats,
 daily,deforestation,forest,forest\-biomass,forma,gfw,modis,monitoring,wri

2012\-01\-01T00:00:00Z/2019\-04\-23T00:00:00Z



 \-50 \-120 40 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








