



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

CPC Global Unified Temperature


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================








Dataset Availability
1979\-01\-01T00:00:00Z–2025\-07\-15T00:00:00Z
Dataset Provider


[NOAA Physical Sciences Laboratory](https://psl.noaa.gov/data/gridded/data.cpc.globaltemp.html)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CPC/Temperature")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CPC_Temperature)





Tags


[climate](/earth-engine/datasets/tags/climate)
[daily](/earth-engine/datasets/tags/daily)
[noaa](/earth-engine/datasets/tags/noaa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[weather](/earth-engine/datasets/tags/weather)








#### Description



This dataset provides a gridded analysis of daily surface air temperature
over global land areas, including daily maximum (Tmax), minimum (Tmin)
temperatures. Spanning from 1979 to the present, the data is presented on
0\.5\-degree latitude/longitude grids, aligning with the resolution of CPC's
gauge\-based global daily precipitation analysis. The construction of this
dataset considers orographic effects. Its primary purpose is to support
climate monitoring and forecast verification activities. Input data
originates from the CPC archive of GTS (Global Telecommunication System)
daily reports, incorporating Tmax and Tmin data from approximately 6,000 to
7,000 global stations.


Refer [this](https://ftp.cpc.ncep.noaa.gov/precip/PEOPLE/wd52ws/global_temp/CPC-GLOBAL-T.pdf)
for technical documentation.





### Bands



**Pixel Size**
  
55500 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `tmax` | °C | \-89\.84\* | 66\.03\* | daily maximum temperature |
| `tmin` | °C | \-97\.92\* | 54\.26\* | daily minimum temperature |
| `nmax` | None | 0\* | 7\* | number of reports for maximum temperature |
| `nmin` | None | 0\* | 7\* | number of reports for minimum temperature |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


The NOAA CPC datasets are available without restriction
on use or distribution. NOAA PSL does request that the
user give proper attribution and identify NOAA PSL, where applicable,
as the source of the data.




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CPC/Temperature').filter(ee.Filter.date('2018-01-01','2019-01-01'));
vartemperature=dataset.select('tmax');
vartemperatureVis={
min:-40,
max:50,
palette:['#ADD8E6','#008000','#FFFF00','#FFA500','#FF0000','#800080'],
};
Map.setCenter(-104.8,49.1,3);
Map.addLayer(temperature,temperatureVis,'NOAA CPC Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CPC_Temperature)


[CPC Global Unified Temperature](/earth-engine/datasets/catalog/NOAA_CPC_Temperature)

This dataset provides a gridded analysis of daily surface air temperature over global land areas, including daily maximum (Tmax), minimum (Tmin) temperatures. Spanning from 1979 to the present, the data is presented on 0\.5\-degree latitude/longitude grids, aligning with the resolution of CPC's gauge\-based global daily precipitation analysis. The construction of …

 NOAA/CPC/Temperature,
 climate,daily,noaa,precipitation,weather

1979\-01\-01T00:00:00Z/2025\-07\-15T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








