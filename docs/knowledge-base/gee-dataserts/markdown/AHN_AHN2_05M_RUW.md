



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

AHN Netherlands 0\.5m DEM, Raw Samples


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================








Dataset Availability
2012\-01\-01T00:00:00Z–2012\-01\-01T00:00:00Z
Dataset Provider


[AHN](https://www.ahn.nl)



Earth Engine Snippet


`ee.Image("AHN/AHN2_05M_RUW")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/AHN/AHN_AHN2_05M_RUW)





Tags


[ahn](/earth-engine/datasets/tags/ahn)
[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[geophysical](/earth-engine/datasets/tags/geophysical)
[lidar](/earth-engine/datasets/tags/lidar)
[netherlands](/earth-engine/datasets/tags/netherlands)








#### Description



The AHN DEM is a 0\.5m DEM covering the Netherlands. It was generated from
LIDAR data taken in the spring between 2007 and 2012\.


This version contains both ground level samples and items above ground level
(such as buildings, bridges, trees etc). The point cloud was converted to a
0\.5m grid using a squared inverse distance weighting method.





### Bands



**Pixel Size**
  
0\.5 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `elevation` | m | Elevation |




### Terms of Use


**Terms of Use**


The datasets of the AHN are available as Open Data.
This means that the data can be used by anyone for free and without
restrictions. For more information visit the
[Open Data](https://www.ahn.nl/open-data/) page. Downloads are available
under the terms of the
[CC\-0 license](https://data.overheid.nl/licenties-voor-hergebruik).




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('AHN/AHN2_05M_RUW');
varelevation=dataset.select('elevation');
varelevationVis={
min:-5.0,
max:30.0,
};
Map.setCenter(5.76583,51.855276,16);
Map.addLayer(elevation,elevationVis,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/AHN/AHN_AHN2_05M_RUW)


[AHN Netherlands 0\.5m DEM, Raw Samples](/earth-engine/datasets/catalog/AHN_AHN2_05M_RUW)

The AHN DEM is a 0\.5m DEM covering the Netherlands. It was generated from LIDAR data taken in the spring between 2007 and 2012\. This version contains both ground level samples and items above ground level (such as buildings, bridges, trees etc). The point cloud was converted to a 0\.5m …

 AHN/AHN2\_05M\_RUW,
 ahn,dem,elevation,elevation\-topography,geophysical,lidar,netherlands

2012\-01\-01T00:00:00Z/2012\-01\-01T00:00:00Z



 50\.74 3\.35 53\.55 7\.24
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








