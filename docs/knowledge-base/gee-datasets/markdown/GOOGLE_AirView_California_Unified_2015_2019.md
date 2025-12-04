



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Google Street View Air Quality: High Resolution Air Pollution Mapping in California


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================================================








Dataset Availability
2015\-05\-28T00:00:00Z–2019\-06\-07T00:00:00Z
Dataset Provider


[Google / Aclima](https://medium.com/google-earth/powering-new-research-with-hyperlocal-air-pollution-data-c9947359e87e)



Earth Engine Snippet


`ee.FeatureCollection("GOOGLE/AirView/California_Unified_2015_2019")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_AirView_California_Unified_2015_2019)





Tags


[air\-quality](/earth-engine/datasets/tags/air-quality)
[atmosphere](/earth-engine/datasets/tags/atmosphere)
[nitrogen\-dioxide](/earth-engine/datasets/tags/nitrogen-dioxide)
[pollution](/earth-engine/datasets/tags/pollution)
[table](/earth-engine/datasets/tags/table)








#### Description



This large vector dataset contains high resolution air pollution mapping of
NO, NO2, O3, CH4, CO2, BC, PN2\.5, and UFP concentrations in California
between June 2015 and June 2019\.


The dataset consists of measurements collected using four Google Street View
vehicles equipped with the Aclima mobile measurement and data integration
platform from 2015\-05\-28 to 2019\-06\-07\. Not all four cars were actively
mapping over the entire time frame. Note that there may be gaps in the data
when an individual car was not mapping due to operational, mechanical, or
system difficulties.


Dates of operation for each of the four cars:


* Car A: 2016\-05\-03 \- 2019\-04\-30
* Car B: 2016\-05\-03 \- 2018\-06\-08
* Car C: 2015\-05\-28 \- 2019\-06\-07
* Car D: 2015\-06\-24 \- 2018\-11\-05


Data was collected in several geographic regions of California including the
San Francisco Bay Area, Los Angeles, and the northern San Joaquin Valley.
Mapping occurred in targeted neighborhoods or cities within these regions. 
The data set contains a table titled "California\_Unified\_2015\_2019" which
consists of the concentration of the pollutants Ozone (O3\), Nitrogen Dioxide
(NO2\), Nitrogen Monoxide (NO), Methane (CH4\), Carbon Dioxide (CO2\),
Black Carbon (BC), particle number less than 2\.5 micrometers in size
(PN2\.5\), and Ultrafine Particles (UFP) measured using four Google Street
View cars equipped with fast time\-response, laboratory\-grade instruments.
The data was collected at 1\-Hz time resolution from 20150528 to 20190607 for
roads in three regions of California \- the San Francisco Bay area,
Los Angeles, and the northern San Joaquin Valley. Specific areas mapped
varied by region based on desired spatial data coverage and science
questions. Each data point is geolocated with latitude and longitude as
well as the identity and speed of the car.


For details including methodologies, standards, data providers,
metadata field definitions and descriptions, refer to the
[metadata](https://docs.google.com/document/d/1If15JccoJcN01Jg3ljN3V-qUFS0HywKAd4OsQ-_JXJo/view).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| BC | DOUBLE | Black carbon concentration |
| CH4 | DOUBLE | Methane dry air mixing ratio |
| CO2 | DOUBLE | Carbon dioxide mixing ratio |
| Car\_Identifier | STRING | Unique identifier for the four vehicles (Car\_A/B/C/D) |
| Car\_Speed | DOUBLE | Car speed |
| Date\_Time | STRING | Time in UTC, format YYYY\-MM\-DD hh:mm:ss |
| Metadata\_Link | STRING | Link to the document |
| NO | DOUBLE | Nitrogen monoxide mixing ratio |
| NO2 | DOUBLE | Nitrogen dioxide mixing ratio |
| NO2\_Overrange | STRING | Boolean flag indicating the measured value was higher than the operating range of the instrument's specification. This field can be empty. |
| NO\_Overrange | STRING | Boolean flag indicating the measured value was higher than the operating range of the instrument's specification. This field can be empty. |
| O3 | DOUBLE | Ozone mixing ratio |
| PN1 | DOUBLE | Particle number concentration between 0\.3 and 0\.5 μm |
| PN2 | DOUBLE | Particle number concentration between 0\.5 and 0\.7 μm |
| PN3 | DOUBLE | Particle number concentration between 0\.7 and 1\.0 μm |
| PN4 | DOUBLE | Particle number concentration between 1\.0 and 1\.5 μm |
| PN5 | DOUBLE | Particle number concentration between 1\.5 and 2\.5 μm |
| PN\_Overrange | STRING | Boolean flag indicating the measured value was higher than the operating range of the instrument's specification. This field can be empty. |
| UFP | DOUBLE | Total particle number concentration greater than 3 nm |
| UFP\_Overrange | STRING | Boolean flag indicating the measured value was higher than the operating range of the instrument's specification. This field can be empty. |




### Terms of Use


**Terms of Use**


[CC\-BY\-NC\-4\.0](https://spdx.org/licenses/CC-BY-NC-4.0.html)




### Citations



Citations:
* with the text "Air Quality Data from Google and Aclima"


Citation for publications: Google and Aclima 2019: Project Air View California 2015\-2019





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varfc=ee.FeatureCollection('GOOGLE/AirView/California_Unified_2015_2019');

varnormal=fc.filter('NO2 >= 0 && NO2 < 1');
varmild=fc.filter('NO2 >= 1 && NO2 < 2');
varstrong=fc.filter('NO2 >= 2');

Map.addLayer(normal,{color:'green'},'NO2 [0; 1)');
Map.addLayer(mild,{color:'yellow'},'NO2 [1; 2)');
Map.addLayer(strong,{color:'red'},'NO2 >= 2');
Map.setCenter(-122.827746,38.4001353,20);
Map.setOptions('SATELLITE');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_AirView_California_Unified_2015_2019)


[Google Street View Air Quality: High Resolution Air Pollution Mapping in California](/earth-engine/datasets/catalog/GOOGLE_AirView_California_Unified_2015_2019)

This large vector dataset contains high resolution air pollution mapping of NO, NO2, O3, CH4, CO2, BC, PN2\.5, and UFP concentrations in California between June 2015 and June 2019\. The dataset consists of measurements collected using four Google Street View vehicles equipped with the Aclima mobile measurement and data integration …

 GOOGLE/AirView/California\_Unified\_2015\_2019,
 air\-quality,atmosphere,nitrogen\-dioxide,pollution,table

2015\-05\-28T00:00:00Z/2019\-06\-07T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








