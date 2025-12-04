



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

CPC Global Unified Gauge\-Based Analysis of Daily Precipitation


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================================








Dataset Availability
2006\-01\-01T00:00:00Z–2025\-07\-15T00:00:00Z
Dataset Provider


[NOAA Physical Sciences Laboratory](https://psl.noaa.gov/data/gridded/data.cpc.globalprecip.html)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CPC/Precipitation")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CPC_Precipitation)





Tags


[daily](/earth-engine/datasets/tags/daily)
[noaa](/earth-engine/datasets/tags/noaa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[weather](/earth-engine/datasets/tags/weather)








#### Description



The CPC Unified Gauge\-Based Analysis of Global Daily Precipitation dataset
offers daily precipitation estimates over land from 1979 to the present.
Developed by NOAA's Climate Prediction Center (CPC), it leverages an optimal
interpolation technique to combine data from a global network of rain
gauges, with over 30,000 gauges contributing to the retrospective version
(1979\-2005\) and around 17,000 to the real\-time version (2006\-present).
Data is provided at a 0\.5\-degree resolution and includes both precipitation
amounts (in 0\.1 mm) and the number of gauges used for each grid cell,
allowing users to assess data quality.


The dataset's quality is acknowledged to be poor over tropical Africa and
Antarctica, and generally varies with gauge density. Real\-time data is
subject to revision as more complete station data becomes available.


[This](https://ftp.cpc.ncep.noaa.gov/precip/CPC_UNI_PRCP/GAUGE_GLB/DOCU/)
folder has all the technical documentation.


NOTE: The historical data spanning from 1979 to 2005 is not available in the
current version of the dataset.





### Bands



**Pixel Size**
  
55500 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `precipitation` | mm | 0\* | 10671\.5\* | Daily total precipitation estimate in 0\.1 mm |
| `num_gauges` | None | 0\* | 121\* | Number of rain gauges contributing to the precipitation estimate within the 0\.5\-degree grid cell |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


The NOAA CPC datasets are available without restriction
on use or distribution. NOAA PSL does request that the
user give proper attribution and identify NOAA PSL, where applicable,
as the source of the data.




### Citations



Citations:
* (Interpolation algorithm) Xie\_et\_al\_2007\_JHM\_EAG.pdf Xie,
P., A. Yatagai, M. Chen, T. Hayasaka, Y. Fukushima, C. Liu, and
S. Yang (2007\), A gauge\-based analysis of daily precipitation over East
Asia, J. Hydrometeorol., 8, 607\. 626\.
* (Gauge Algorithm Evaluation) Chen\_et\_al\_2008\_JGR\_Gauge\_Algo.pdf
Chen, M., W. Shi, P. Xie, V. B. S. Silva, V E. Kousky, R. Wayne Higgins,
and J. E. Janowiak (2008\), Assessing objective techniques for
gauge\-based analyses of global daily precipitation,
J. Geophys. Res., 113, D04110,
[doi:10\.1029/2007JD009132](https://doi.org/10.1029/2007JD009132)





### DOIs


* [https://doi.org/10\.1029/2007JD009132](https://doi.org/10.1029/2007JD009132)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CPC/Precipitation')
.filter(ee.Filter.date('2018-01-01','2019-01-01'));
varprecipitation=dataset.select('precipitation');
varprecipitationVis={
min:0,
max:150,
palette:['#ADD8E6','#008000','#FFFF00','#FFA500','#FF0000','#800080'],
};
Map.setCenter(-68.36,-6.73,3);
Map.addLayer(precipitation,precipitationVis,'NOAA CPC Precipitation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CPC_Precipitation)


[CPC Global Unified Gauge\-Based Analysis of Daily Precipitation](/earth-engine/datasets/catalog/NOAA_CPC_Precipitation)

The CPC Unified Gauge\-Based Analysis of Global Daily Precipitation dataset offers daily precipitation estimates over land from 1979 to the present. Developed by NOAA's Climate Prediction Center (CPC), it leverages an optimal interpolation technique to combine data from a global network of rain gauges, with over 30,000 gauges contributing to …

 NOAA/CPC/Precipitation,
 daily,noaa,precipitation,weather

2006\-01\-01T00:00:00Z/2025\-07\-15T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1029/2007JD009132](https://doi.org/https://psl.noaa.gov/data/gridded/data.cpc.globalprecip.html)
* [https://doi.org/10\.1029/2007JD009132](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CPC_Precipitation)









