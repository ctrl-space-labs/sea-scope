



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

JRC Global River Flood Hazard Maps Version 1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================








Dataset Availability
2024\-03\-16T00:00:00Z–2024\-03\-16T23:59:59Z
Dataset Provider


[Joint Research Centre](https://data.jrc.ec.europa.eu/dataset/jrc-floods-floodmapgl_rp50y-tif)



Earth Engine Snippet


`ee.ImageCollection("JRC/CEMS_GLOFAS/FloodHazard/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_CEMS_GLOFAS_FloodHazard_v1)





Tags


[flood](/earth-engine/datasets/tags/flood)
[monitoring](/earth-engine/datasets/tags/monitoring)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[wri](/earth-engine/datasets/tags/wri)








#### Description



The global river flood hazard maps are a gridded data set representing
inundation along the river network, for seven different flood return periods
(from 1\-in\-10\-years to 1\-in\-500\-years). The input river flow data for the
new maps are produced by means of the open\-source hydrological model
LISFLOOD, while inundation simulations are performed with the hydrodynamic
model LISFLOOD\-FP. The extent comprises the entire world with the exception
of Greenland and Antarctica and small islands with river basins smaller than
500 km^2\.


Cell values indicate water depth (in meters). The maps can be used to assess
the exposure of population and economic assets to river floods, and to
perform flood risk assessments. The dataset is created as part of the
Copernicus Emergency Management Service.


**Note:** This dataset may have missing tiles. This collection will be
eventually be replaced by v2\.1 once it's updated by the provider.



### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `depth` | m | 0\.1 | 9494\.89 | Flood inundation depth |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| return\_period | INT | Return period of flood in years. **Note:** This property is not present for images that just show the permanent water bodies. |
| id | INT | Unique identifier for the latitude/longitude grid cell. |




### Terms of Use


**Terms of Use**


The JRC datasets are available without restriction
on use or distribution. For more information check
[access rights](https://data.jrc.ec.europa.eu/access-rights/no-limitations),




### Citations



Citations:
* Baugh, Calum; Colonese, Juan; D'Angelo, Claudia; Dottori, Francesco;
Neal, Jeffrey; Prudhomme, Christel; Salamon, Peter (2024\): Global river
flood hazard maps. European Commission, Joint Research Centre (JRC)
\[Dataset] PID:
[http://data.europa.eu/89h/jrc\-floods\-floodmapgl\_rp50y\-tif](http://data.europa.eu/89h/jrc-floods-floodmapgl_rp50y-tif)





### DOIs


* [https://doi.org/10\.1016/j.advwatres.2016\.05\.002](https://doi.org/10.1016/j.advwatres.2016.05.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('JRC/CEMS_GLOFAS/FloodHazard/v1');
vardepth=dataset.select('depth');
vardepthVis={
min:0,
max:1,
palette:['ffffff','0000ff'],
};
Map.setCenter(-86.47,47.28,4);
Map.addLayer(depth,depthVis,'JRC Flood Hazard Maps');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_CEMS_GLOFAS_FloodHazard_v1)


[JRC Global River Flood Hazard Maps Version 1](/earth-engine/datasets/catalog/JRC_CEMS_GLOFAS_FloodHazard_v1)

The global river flood hazard maps are a gridded data set representing inundation along the river network, for seven different flood return periods (from 1\-in\-10\-years to 1\-in\-500\-years). The input river flow data for the new maps are produced by means of the open\-source hydrological model LISFLOOD, while inundation simulations are …

 JRC/CEMS\_GLOFAS/FloodHazard/v1,
 flood,monitoring,surface\-ground\-water,wri

2024\-03\-16T00:00:00Z/2024\-03\-16T23:59:59Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1016/j.advwatres.2016\.05\.002](https://doi.org/https://data.jrc.ec.europa.eu/dataset/jrc-floods-floodmapgl_rp50y-tif)
* [https://doi.org/10\.1016/j.advwatres.2016\.05\.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JRC_CEMS_GLOFAS_FloodHazard_v1)









