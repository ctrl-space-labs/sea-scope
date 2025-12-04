



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Primary Humid Tropical Forests


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2002\-01\-01T00:00:00Z
Dataset Provider


[UMD/GLAD](https://glad.umd.edu/dataset/primary-forest-humid-tropics)



Earth Engine Snippet


`ee.ImageCollection("UMD/GLAD/PRIMARY_HUMID_TROPICAL_FORESTS/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMD/UMD_GLAD_PRIMARY_HUMID_TROPICAL_FORESTS_v1)





Tags


[forest](/earth-engine/datasets/tags/forest)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[global](/earth-engine/datasets/tags/global)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[umd](/earth-engine/datasets/tags/umd)
glad








#### Description



Primary humid tropical forests provide numerous global ecosystem services,
but are under continuing threat of clearing from economic drivers. To facilitate
national land use planning and balancing the goals of economic development and
maintenance of ecosystem services, a primary humid tropical forest map was
created by the UMD GLAD team. The primary forest extent was mapped
for the year 2001 at a spatial resolution of 30 meters using globally acquired,
free\-of\-charge, and consistently processed Landsat imagery.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `Primary_HT_forests` | Primary Humid Tropical Forests |


**Primary\_HT\_forests Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#008000 | Primary Humid Tropical Forests |




### Terms of Use


**Terms of Use**


The data may be used by anyone, anywhere, anytime without permission,
license or royalty payment.
Attribution using the recommended citation is requested.




### Citations



Citations:
* Turubanova S., Potapov P., Tyukavina, A., and Hansen M. (2018\) Ongoing primary forest
loss in Brazil, Democratic Republic of the Congo, and Indonesia. Environmental
Research Letters.
[https://doi.org/10\.1088/1748\-9326/aacd1c](https://doi.org/10.1088/1748-9326/aacd1c)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection(
'UMD/GLAD/PRIMARY_HUMID_TROPICAL_FORESTS/v1').mosaic().selfMask();

varvisualization={
bands:['Primary_HT_forests'],
min:1.0,
max:1.0,
palette:['008000']
};

Map.setCenter(0.0,0.0,2);

Map.addLayer(dataset,visualization,'Primary HT forests');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMD/UMD_GLAD_PRIMARY_HUMID_TROPICAL_FORESTS_v1)


[Primary Humid Tropical Forests](/earth-engine/datasets/catalog/UMD_GLAD_PRIMARY_HUMID_TROPICAL_FORESTS_v1)

Primary humid tropical forests provide numerous global ecosystem services, but are under continuing threat of clearing from economic drivers. To facilitate national land use planning and balancing the goals of economic development and maintenance of ecosystem services, a primary humid tropical forest map was created by the UMD GLAD team. …

 UMD/GLAD/PRIMARY\_HUMID\_TROPICAL\_FORESTS/v1,
 forest,forest\-biomass,global,landsat\-derived,umd

2001\-01\-01T00:00:00Z/2002\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








