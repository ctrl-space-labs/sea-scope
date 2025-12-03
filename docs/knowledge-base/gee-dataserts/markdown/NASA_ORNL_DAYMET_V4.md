



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Daymet V4: Daily Surface Weather and Climatological Summaries


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================================================








Dataset Availability
1980\-01\-01T00:00:00Z–2023\-12\-31T00:00:00Z
Dataset Provider


[NASA ORNL DAAC at Oak Ridge National Laboratory](https://doi.org/10.3334/ORNLDAAC/1840)



Earth Engine Snippet


`ee.ImageCollection("NASA/ORNL/DAYMET_V4")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_ORNL_DAYMET_V4)





Cadence
1 Day
Tags


[climate](/earth-engine/datasets/tags/climate)
[daily](/earth-engine/datasets/tags/daily)
[daylight](/earth-engine/datasets/tags/daylight)
[flux](/earth-engine/datasets/tags/flux)
[geophysical](/earth-engine/datasets/tags/geophysical)
[nasa](/earth-engine/datasets/tags/nasa)
[ornl](/earth-engine/datasets/tags/ornl)
[precipitation](/earth-engine/datasets/tags/precipitation)
[radiation](/earth-engine/datasets/tags/radiation)
[snow](/earth-engine/datasets/tags/snow)
[temperature](/earth-engine/datasets/tags/temperature)
[vapor](/earth-engine/datasets/tags/vapor)
[water](/earth-engine/datasets/tags/water)
[weather](/earth-engine/datasets/tags/weather)
daymet








#### Description



Daymet V4 provides gridded estimates of daily weather parameters for
Continental North America, Hawaii, and Puerto Rico (Data for Puerto Rico is available starting
in 1950\). It is derived from selected meteorological station data and various supporting data
sources.


Compared to the previous version, Daymet V4 provides effective solutions to known issues and
further considers improvements to what were believed to be input weather station biases.
Improvements include:


* Reductions in the timing bias of input reporting weather station measurements.
* Improvement to the three\-dimensional regression model techniques in the core algorithm.
* A novel approach to handling high elevation temperature measurement biases.


2020 and 2021 data are ingested from V4 R1 sources


Documentation:


* [ORNL DAAC Dataset Documentation](https://daac.ornl.gov/DAYMET/guides/Daymet_Daily_V4.html)
* [Dataset Documentation](https://daac.ornl.gov/daacdata/daymet/Daymet_Daily_V4/comp/Daymet_Daily_V4.pdf)
* [The THREDDS location for this Collection](https://thredds.daac.ornl.gov/thredds/catalogs/ornldaac/Regional_and_Global_Data/DAYMET_COLLECTIONS/DAYMET_COLLECTIONS.html)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `dayl` | seconds | 0\* | 86400\* | Duration of the daylight period. Based on the period of the day during which the sun is above a hypothetical flat horizon. |
| `prcp` | mm | 0\* | 544\* | Daily total precipitation, sum of all forms converted to water\-equivalent. |
| `srad` | W/m^2 | 0\* | 1051\* | Incident shortwave radiation flux density, taken as an average over the daylight period of the day. |
| `swe` | kg/m^2 | 0\* | 13931\* | Snow water equivalent, the amount of water contained within the snowpack. |
| `tmax` | °C | \-60\* | 60\* | Daily maximum 2\-meter air temperature. |
| `tmin` | °C | \-60\* | 42\* | Daily minimum 2\-meter air temperature. |
| `vp` | Pa | 0\* | 8230\* | Daily average partial pressure of water vapor. |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* Thornton, M.M., R. Shrestha, Y. Wei, P.E. Thornton, S\-C. Kao, and B.E. Wilson. 2022\.
Daymet: Daily Surface Weather Data on a 1\-km Grid for North America, Version 4 R1\.
ORNL DAAC, Oak Ridge, Tennessee, USA. https://doi.org/10\.3334/ORNLDAAC/2129
* Other Citation Details \- Thornton, M.M., R. Shrestha, Y. Wei, P.E. Thornton, S. Kao, and B.E. Wilson. 2020\.
Daymet: Daily Surface Weather Data on a 1\-km Grid for North America, Version 4\. ORNL DAAC, Oak Ridge, Tennessee, USA.
[doi:10\.3334/ORNLDAAC/1840](https://doi.org/10.3334/ORNLDAAC/1840)





### DOIs


* [https://doi.org/10\.3334/ORNLDAAC/1840](https://doi.org/10.3334/ORNLDAAC/1840)
* [https://doi.org/10\.3334/ORNLDAAC/2129](https://doi.org/10.3334/ORNLDAAC/2129)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/ORNL/DAYMET_V4')
.filter(ee.Filter.date('2017-04-01','2017-04-30'));
varmaximumTemperature=dataset.select('tmax');
varmaximumTemperatureVis={
min:-40.0,
max:30.0,
palette:['1621A2','white','cyan','green','yellow','orange','red'],
};
Map.setCenter(-110.21,35.1,4);
Map.addLayer(maximumTemperature,maximumTemperatureVis,'Maximum Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_ORNL_DAYMET_V4)


[Daymet V4: Daily Surface Weather and Climatological Summaries](/earth-engine/datasets/catalog/NASA_ORNL_DAYMET_V4)

Daymet V4 provides gridded estimates of daily weather parameters for Continental North America, Hawaii, and Puerto Rico (Data for Puerto Rico is available starting in 1950\). It is derived from selected meteorological station data and various supporting data sources. Compared to the previous version, Daymet V4 provides effective solutions to …

 NASA/ORNL/DAYMET\_V4,
 climate,daily,daylight,flux,geophysical,nasa,ornl,precipitation,radiation,snow,temperature,vapor,water,weather

1980\-01\-01T00:00:00Z/2023\-12\-31T00:00:00Z



 1\.6 \-150\.8 84 \-1\.1
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.3334/ORNLDAAC/2129](https://doi.org/https://doi.org/10.3334/ORNLDAAC/1840)
* [https://doi.org/10\.3334/ORNLDAAC/2129](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_ORNL_DAYMET_V4)









