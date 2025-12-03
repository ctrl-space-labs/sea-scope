



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WAPOR Actual Evapotranspiration and Interception 2\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================================








Dataset Availability
2009\-01\-01T00:00:00Z–2023\-03\-01T00:00:00Z
Dataset Provider


[FAO UN](https://wapor.apps.fao.org/catalog/WAPOR_2/1/L1_AETI_D)



Earth Engine Snippet


`ee.ImageCollection("FAO/WAPOR/2/L1_AETI_D")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/FAO/FAO_WAPOR_2_L1_AETI_D)





Cadence
10 Days
Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[fao](/earth-engine/datasets/tags/fao)
[wapor](/earth-engine/datasets/tags/wapor)
[water](/earth-engine/datasets/tags/water)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)








#### Description



The actual evapotranspiration and interception (ETIa) (dekadal, in mm/day)
is the sum of the soil evaporation (E), canopy transpiration (T), and
evaporation from rainfall intercepted by leaves (I). The value of each pixel
represents the average daily ETIa in a given dekad.





### Bands



**Pixel Size**
  
248\.2 meters



**Bands**




| Name | Units | Scale | Description |
| --- | --- | --- | --- |
| `L1_AETI_D` | mm | 0\.1 | Actual Evapotranspiration and Interception (Dekadal) \[mm] |




### Terms of Use


**Terms of Use**


The Food and Agriculture Organization of the United Nations (FAO) is
mandated to collect, analyze, interpret, and disseminate information related
to nutrition, food, and agriculture. In this regard, it publishes a number
of databases on topics related to FAO's mandate, and encourages the use of
them for scientific and research purposes. Consistent with the principles
of openness and sharing envisioned under the [Open Data Licensing For
Statistical Databases](http://www.fao.org/3/ca7570en/ca7570en.pdf), and
consistent with the mandate of FAO, data from the [Water Productivity Open
Access Portal (WaPOR)](https://wapor.apps.fao.org/home/WAPOR_2/1), as part
of [AQUASTAT](http://www.fao.org/aquastat/en/) \- FAO's Global Information
System on Water and Agriculture, is available free to the user community.




### Citations



Citations:
* FAO 2018\. WaPOR Database Methodology: Level 1\. Remote Sensing for Water
Productivity Technical Report: Methodology Series. Rome, FAO. 72 pages.
* FAO 2020\. WaPOR V2 Database Methodology. Remote Sensing for Water
Productivity Technical Report: Methodology Series. Rome, FAO.
<https://www.fao.org/3/ca9894en/CA9894EN.pdf>





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcoll=ee.ImageCollection('FAO/WAPOR/2/L1_AETI_D');
varimage=coll.first();
Map.setCenter(17.5,20,3);
Map.addLayer(image,{min:0,max:50});
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/FAO/FAO_WAPOR_2_L1_AETI_D)


[WAPOR Actual Evapotranspiration and Interception 2\.0](/earth-engine/datasets/catalog/FAO_WAPOR_2_L1_AETI_D)

The actual evapotranspiration and interception (ETIa) (dekadal, in mm/day) is the sum of the soil evaporation (E), canopy transpiration (T), and evaporation from rainfall intercepted by leaves (I). The value of each pixel represents the average daily ETIa in a given dekad.

 FAO/WAPOR/2/L1\_AETI\_D,
 agriculture,fao,wapor,water,water\-vapor

2009\-01\-01T00:00:00Z/2023\-03\-01T00:00:00Z



 \-40\.0044644 \-30\.0044643 40\.0044643 65\.0044644
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








