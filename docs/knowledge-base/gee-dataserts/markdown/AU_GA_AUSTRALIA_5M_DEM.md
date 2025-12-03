



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Australian 5M DEM


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================








Dataset Availability
2015\-12\-01T00:00:00Z–2015\-12\-01T00:00:00Z
Dataset Provider


[Geoscience Australia](https://ecat.ga.gov.au/geonetwork/srv/eng/catalog.search#/metadata/89644)



Earth Engine Snippet


`ee.ImageCollection("AU/GA/AUSTRALIA_5M_DEM")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/AU/AU_GA_AUSTRALIA_5M_DEM)





Tags


[australia](/earth-engine/datasets/tags/australia)
[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[ga](/earth-engine/datasets/tags/ga)
[geophysical](/earth-engine/datasets/tags/geophysical)
[geoscience\-australia](/earth-engine/datasets/tags/geoscience-australia)
[lidar](/earth-engine/datasets/tags/lidar)








#### Description



The Digital Elevation Model (DEM) 5 meter Grid of Australia
derived from LiDAR model represents a National 5 meter (bare
earth) DEM which has been derived from some 236 individual LiDAR
surveys between 2001 and 2015 covering an area in excess of 245,000
square kilometers. These surveys cover Australia's populated
coastal zone; floodplain surveys within the Murray Darling Basin,
and individual surveys of major and minor population centers.
All available 1 meter resolution LiDAR\-derived DEMs have been
compiled and resampled using a neighborhood\-mean method to 5
meter resolution datasets for each survey area, and then merged
into a single dataset for each State. Each state's dataset is
provided as a separate image within the image collection.


The acquisition of the individual LiDAR surveys and derivation
of the 5m product has been part of a long\-term collaboration
between Geoscience Australia, the Cooperative Research Centre
for Spatial Information (CRCSI), the Departments of Climate Change
and Environment, State and Territory jurisdictions, Local Government
and the Murray Darling Basin Authority under the auspices of
the National Elevation Data Framework and Coastal and Urban DEM
Program. The source datasets have been captured to standards
that are generally consistent with the Australian ICSM LiDAR
Acquisition Specifications with require a fundamental vertical
accuracy of at least 0\.30m (95% confidence) and horizontal accuracy
of at least 0\.80m (95% confidence).


There are several areas close to Perth with null (NaN) values around
(115\.85, \-31\.99\), (115\.72, \-33\.75\), and (115\.10, \-33\.43\).





### Bands



**Pixel Size**
  
5 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `elevation` | m | Elevation |




### Terms of Use


**Terms of Use**


This dataset is made available by Geoscience Australia
under the Creative Commons Attribution 4\.0 International License.
The data must be referenced with the provided citation and DOI.




### Citations



Citations:
* Geoscience Australia, 2015\. Digital Elevation Model (DEM) of Australia
derived from LiDAR 5 Metre Grid. Geoscience Australia, Canberra.





### DOIs


* [https://doi.org/10\.4225/25/5652419862E23](https://doi.org/10.4225/25/5652419862E23)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('AU/GA/AUSTRALIA_5M_DEM');
varelevation=dataset.select('elevation');
varelevationVis={
min:0.0,
max:150.0,
palette:['0000ff','00ffff','ffff00','ff0000','ffffff'],
};
Map.setCenter(140.1883,-35.9113,8);
Map.addLayer(elevation,elevationVis,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/AU/AU_GA_AUSTRALIA_5M_DEM)


[Australian 5M DEM](/earth-engine/datasets/catalog/AU_GA_AUSTRALIA_5M_DEM)

The Digital Elevation Model (DEM) 5 meter Grid of Australia derived from LiDAR model represents a National 5 meter (bare earth) DEM which has been derived from some 236 individual LiDAR surveys between 2001 and 2015 covering an area in excess of 245,000 square kilometers. These surveys cover Australia's populated …

 AU/GA/AUSTRALIA\_5M\_DEM,
 australia,dem,elevation,elevation\-topography,ga,geophysical,geoscience\-australia,lidar

2015\-12\-01T00:00:00Z/2015\-12\-01T00:00:00Z



 \-43\.45 114\.09 \-9\.88 153\.64
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.4225/25/5652419862E23](https://doi.org/https://ecat.ga.gov.au/geonetwork/srv/eng/catalog.search#/metadata/89644)
* [https://doi.org/10\.4225/25/5652419862E23](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/AU_GA_AUSTRALIA_5M_DEM)









