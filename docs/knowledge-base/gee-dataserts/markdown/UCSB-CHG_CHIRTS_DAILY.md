



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

CHIRTS\-daily: Climate Hazards Center InfraRed Temperature with Stations daily temperature data product


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================================================================================








Dataset Availability
1983\-01\-01T00:00:00Z–2016\-12\-31T00:00:00Z
Dataset Provider


[UCSB/CHG](https://chc.ucsb.edu/data/chirtsdaily)



Earth Engine Snippet


`ee.ImageCollection("UCSB-CHG/CHIRTS/DAILY")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UCSB-CHG/UCSB-CHG_CHIRTS_DAILY)





Cadence
1 Day
Tags


[chg](/earth-engine/datasets/tags/chg)
[climate](/earth-engine/datasets/tags/climate)
[daily](/earth-engine/datasets/tags/daily)
[era5](/earth-engine/datasets/tags/era5)
[geophysical](/earth-engine/datasets/tags/geophysical)
[reanalysis](/earth-engine/datasets/tags/reanalysis)
[temperature](/earth-engine/datasets/tags/temperature)
[ucsb](/earth-engine/datasets/tags/ucsb)
[wind](/earth-engine/datasets/tags/wind)








#### Description



The Climate Hazards Center InfraRed Temperature with Stations daily
temperature data product (CHIRTS\-daily; Verdin et al. 2020\) is a quasi
global, high\-resolution gridded dataset
(0\.05° × 0\.05° resolution, 60°S \- 70°N)
that provides daily minimum (Tmin) and maximum 2\-meter temperatures (Tmax)
and four derived variables: saturation vapor pressure (SVP),
vapor pressure deficit (VPD), relative humidity (RH), and heat index (HI).
CHIRTS temperature products are designed to support analysis of temperature
extremes and variability, especially in regions with a low density of
station observations.


CHIRTS\-daily is created by merging a high\-quality, high\-resolution monthly
maximum temperature dataset, the Climate Hazards Center InfraRed
Temperature with Stations monthly maximum temperature climate record
(CHIRTSmax; Funk et al. 2019\), with daily temperatures from the European
Centre for Medium\-Range Weather Forecasts (ECMWF) Reanalysis v5 (ERA5\).
The result is a high\-resolution, daily temperature dataset that maintains
spatio\-temporal information from monthly CHIRTSmax and the daily and diurnal
temperature variability from ERA5\. Monthly CHIRTSmax are based on:


1. A Tmax climatology constructed using geostatistical regressions and
 long\-term averages of FAO station observations, ERA5 temperatures, and
 several other geographic predictors.
2. Estimates of Tmax variability using approximately 15,000 in situ
 observations and high\-resolution
 (0\.05° × 0\.05°) satellite observations.
 These data are from Berkeley Earth and Global Telecommunication
 System (GTS) station reports and cloud\-screened GridSat geostationary
 satellite thermal infrared brightness temperatures.


Daily Tmax values are produced using downscaled ERA5 Tmax anomalies and
high\-resolution CHIRTSmax. Daily Tmin values are created by removing the
downscaled ERA5 diurnal temperature range (Tmax \- Tmin).
Daily SVP, VPD, RH, and HI are computed using CHIRTS\-daily Tmin and Tmax,
alongside hourly ERA5 inputs for other meteorological variables
(see Williams et al., 2024, for details). CHIRTS\-daily, version 1, covers
the period from 1983 to 2016\.





### Bands



**Pixel Size**
  
5566 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `minimum_temperature` | °C | The lowest air temperature recorded at 2 meters above the ground surface over a 24\-hour period. |
| `maximum_temperature` | °C | 10\* | 40\* | The highest air temperature recorded at 2 meters above the ground surface over a 24\-hour period. |
| `saturation_vapor_pressure` | kPa | The maximum amount of water vapor that the air can hold at a given temperature and pressure at 2 meters above ground. |
| `vapor_pressure_deficit` | kPa | The difference between the saturation vapor pressure and the actual vapor pressure at 2 meters above ground. |
| `relative_humidity` | % | The ratio of the actual amount of water vapor in the air to the maximum amount it could hold at that temperature and pressure (saturation vapor pressure) at 2 meters above ground. |
| `heat_index` | °F | A measure of how hot it feels when temperature and humidity are combined. |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


This datasets are in the public domain. To the extent possible under law,
[Chris Funk](https://chc.ucsb.edu/people/chris-funk) has waived all
copyright and related or neighboring rights to Climate Hazards InfraRed
Temperature with Stations daily temperature data product (CHIRTS\-daily).




### Citations



Citations:
* Verdin, A., C. Funk, P. Peterson, M. Landsfeld, C. Tuholske, and Grace, K.,
2020: Development and validation of the CHIRTS\-daily quasi\-global
high\-resolution daily temperature data set. Scientific Data, 7(1\), 303\.
[doi: 10\.1038/s41597\-020\-00643\-7](https://doi.org/10.1038/s41597-020-00643-7)
* Funk, C., P. Peterson, S. Peterson, S. Shukla,
F. Davenport, J. Michaelsen, K.R. Knapp, M. Landsfeld, G. Husak,
L. Harrison, J. Rowland, M. Budde, A. Meiburg, T. Dinku, D. Pedreros,
and N. Mata, 2019: A High\-Resolution 1983\-2016 Tmax Climate Data Record
Based on Infrared Temperatures and Stations by the Climate Hazard
Center. J. Climate, 32, 5639\-5658\.
[doi:10\.1175/JCLI\-D\-18\-0698\.1](https://doi.org/10.1175/JCLI-D-18-0698.1)
* Williams, E., C. Funk, P. Peterson, and C. Tuholske (2024\). High
resolution climate change observations and projections for the
evaluation of heat\-related extremes. Scientific Data, 11(1\), 261\.
[doi: 10\.1038/s41597\-024\-03074\-w](https://doi.org/10.1038/s41597-024-03074-w)





### DOIs


* [https://doi.org/10\.1038/s41597\-024\-03074\-w](https://doi.org/10.1038/s41597-024-03074-w)
* [https://doi.org/10\.1175/JCLI\-D\-18\-0698\.1](https://doi.org/10.1175/JCLI-D-18-0698.1)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('UCSB-CHG/CHIRTS/DAILY')
.filter(ee.Filter.date('2016-05-01','2016-05-03'));
varmaximumTemperature=dataset.select('maximum_temperature');
varvisParams={
min:10,
max:30,
palette:['darkblue','blue','cyan','green','yellow','orange','red','darkred'],
};
Map.setCenter(-104.28,46.07,3);
Map.addLayer(maximumTemperature,visParams,'Maximum temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UCSB-CHG/UCSB-CHG_CHIRTS_DAILY)


[CHIRTS\-daily: Climate Hazards Center InfraRed Temperature with Stations daily temperature data product](/earth-engine/datasets/catalog/UCSB-CHG_CHIRTS_DAILY)

The Climate Hazards Center InfraRed Temperature with Stations daily temperature data product (CHIRTS\-daily; Verdin et al. 2020\) is a quasi global, high\-resolution gridded dataset (0\.05° × 0\.05° resolution, 60°S \- 70°N) that provides daily minimum (Tmin) and maximum 2\-meter temperatures (Tmax) and four derived variables: saturation vapor pressure (SVP), vapor pressure deficit …

 UCSB\-CHG/CHIRTS/DAILY,
 chg,climate,daily,era5,geophysical,reanalysis,temperature,ucsb,wind

1983\-01\-01T00:00:00Z/2016\-12\-31T00:00:00Z



 \-60 \-180 70 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1175/JCLI\-D\-18\-0698\.1](https://doi.org/https://chc.ucsb.edu/data/chirtsdaily)
* [https://doi.org/10\.1175/JCLI\-D\-18\-0698\.1](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/UCSB-CHG_CHIRTS_DAILY)









