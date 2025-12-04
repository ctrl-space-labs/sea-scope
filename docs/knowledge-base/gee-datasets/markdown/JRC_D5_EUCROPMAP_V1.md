



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

EUCROPMAP


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================








Dataset Availability
2018\-01\-01T00:00:00Z–2022\-01\-01T00:00:00Z
Dataset Provider


[Joint Research Center (JRC)](https://data.jrc.ec.europa.eu/dataset/15f86c84-eae1-4723-8e00-c1b35c8f56b9)



Earth Engine Snippet


`ee.ImageCollection("JRC/D5/EUCROPMAP/V1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_D5_EUCROPMAP_V1)





Cadence
1 Year
Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[crop](/earth-engine/datasets/tags/crop)
[eu](/earth-engine/datasets/tags/eu)
[jrc](/earth-engine/datasets/tags/jrc)
[lucas](/earth-engine/datasets/tags/lucas)
[sentinel1\-derived](/earth-engine/datasets/tags/sentinel1-derived)








#### Description



European crop type map based on Sentinel\-1 and LUCAS Copernicus 2018 in\-situ
observations for 2018; and one based on Sentinel\-2 and LUCAS Copernicus 2022 for 2022\.


Capitalizing on the unique
[LUCAS 2018 Copernicus in\-situ survey](/earth-engine/datasets/catalog/JRC_LUCAS_HARMO_THLOC_V1),
the 2018 dataset is the first continental crop type map with 10m
pixel size for the EU based on S1A and S1B Synthetic Aperture Radar
observations for the year 2018; the 2022 dataset is a continuation of
the work and is based on optical S2 observations for the year 2022\.





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Description |
| --- | --- |
| `classification` | Main crop\-specific land cover classification. |


**classification Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 100 | \#ff130f | Artificial |
| 211 | \#a57000 | Common wheat |
| 212 | \#896054 | Durum wheat |
| 213 | \#e2007c | Barley |
| 214 | \#aa007c | Rye |
| 215 | \#a05989 | Oats |
| 216 | \#ffd300 | Maize |
| 217 | \#00a8e2 | Rice |
| 218 | \#d69ebc | Triticale |
| 219 | \#d69ebc | Other cereals |
| 221 | \#dda50a | Potatoes |
| 222 | \#a800e2 | Sugar beet |
| 223 | \#00af49 | Other root crops |
| 230 | \#00af49 | Other non\-permanent industrial crops |
| 231 | \#ffff00 | Sunflower |
| 232 | \#d1ff00 | Rapeseed and turnip rapeseed |
| 233 | \#267000 | Soya |
| 240 | \#f2a377 | Dry pulses |
| 250 | \#e8bfff | Fodder crops (cereals and leguminous) |
| 290 | \#696969 | Bare arable land |
| 300 | \#93cc93 | Woodland and Shrubland (incl. permanent crops) |
| 500 | \#e8ffbf | Grasslands |
| 600 | \#a89e7f | Bare land/lichens moss |
| 700 | \#0793de | Water |
| 800 | \#7cafaf | Wetlands |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| classification\_class\_names | STRING\_LIST | Array of cropland classification names. |
| classification\_class\_palette | STRING\_LIST | Array of hex code color strings used for the classification palette. |
| classification\_class\_values | INT\_LIST | Value of the cropland classification. |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* d'Andrimont, R., Verhegghen, A., Lemoine, G., Kempeneers, P., Meroni, M.,
\& Van der Velde, M. (2021\). From parcel to continental scale\-A first
European crop type map based on Sentinel\-1 and LUCAS Copernicus in\-situ
observations. Remote sensing of environment, 266, 112708\.
* d'Andrimont, R., Verhegghen, A., Lemoine, G., Kempeneers, P., Meroni, M.,
\& Van der Velde, M. (2021\). From parcel to continental scale\-A first
European crop type map based on Sentinel\-1 and LUCAS Copernicus in\-situ
observations. Remote sensing of environment, 266, 112708\.
[doi:10\.1016/j.rse.2021\.112708](https://doi.org/10.1016/j.rse.2021.112708).
* Ghassemi, B., Dujakovic, A., Żółtak, M., Immitzer, M., Atzberger, C. and Vuolo, F., 2022\. Designing a European\-wide crop type mapping approach based on machine learning algorithms using LUCAS field survey and Sentinel\-2 data. Remote sensing, 14(3\), p.541\.
[10\.3390/rs14030541](https://doi.org/10.3390/rs14030541)





### DOIs


* [https://doi.org/10\.1016/j.rse.2021\.112708](https://doi.org/10.1016/j.rse.2021.112708)
* [https://doi.org/10\.3390/rs14030541](https://doi.org/10.3390/rs14030541)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varimage=ee.ImageCollection('JRC/D5/EUCROPMAP/V1').filterDate(
'2018-01-01','2019-01-01').first();
Map.addLayer(image,{},'EUCROPMAP 2018');
Map.setCenter(10,48,4);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_D5_EUCROPMAP_V1)


[EUCROPMAP](/earth-engine/datasets/catalog/JRC_D5_EUCROPMAP_V1)

European crop type map based on Sentinel\-1 and LUCAS Copernicus 2018 in\-situ observations for 2018; and one based on Sentinel\-2 and LUCAS Copernicus 2022 for 2022\. Capitalizing on the unique LUCAS 2018 Copernicus in\-situ survey, the 2018 dataset is the first continental crop type map with 10m pixel size for …

 JRC/D5/EUCROPMAP/V1,
 agriculture,crop,eu,jrc,lucas,sentinel1\-derived

2018\-01\-01T00:00:00Z/2022\-01\-01T00:00:00Z



 34\.313433 \-16\.171875 72\.182526 36\.386719
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.3390/rs14030541](https://doi.org/https://data.jrc.ec.europa.eu/dataset/15f86c84-eae1-4723-8e00-c1b35c8f56b9)
* [https://doi.org/10\.3390/rs14030541](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JRC_D5_EUCROPMAP_V1)









