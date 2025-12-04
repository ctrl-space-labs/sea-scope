



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GEOS\-CF fcst htf v1: Goddard Earth Observing System Composition Forecast


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================================================================








Dataset Availability
2022\-10\-01T00:00:00Z–2025\-07\-15T12:00:00Z
Dataset Provider


[NASA / GMAO](https://gmao.gsfc.nasa.gov/weather_prediction/GEOS-CF/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GEOS-CF/v1/fcst/htf")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GEOS-CF_v1_fcst_htf)





Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[composition](/earth-engine/datasets/tags/composition)
[forecast](/earth-engine/datasets/tags/forecast)
[geos](/earth-engine/datasets/tags/geos)
[gmao](/earth-engine/datasets/tags/gmao)
[nasa](/earth-engine/datasets/tags/nasa)








#### Description



This dataset contains meteorological forecast (fcst) of high\-temporal
frequency data (htf). Use the 'creation\_time' and 'forecast\_time' properties
to select data of interest.
The Goddard Earth Observing System Composition Forecast (GEOS\-CF) system is
a high\-resolution (0\.25°) global constituent prediction system from
NASA's [Global Modeling and Assimilation Office(GMAO)](https://gmao.gsfc.nasa.gov/).


GEOS\-CF offers a new tool for atmospheric chemistry research, with the goal
to supplement NASA's broad range of space\-based and in\-situ observations.
GEOS\-CF expands on the GEOS weather and aerosol modeling system by
introducing the [GEOS\-Chem](http://wiki.seas.harvard.edu/geos-chem/)
chemistry module to provide hindcasts and 5\-days forecasts of atmospheric
constituents including ozone (O3\), carbon monoxide (CO), nitrogen dioxide
(NO2\), sulfur dioxide (SO2\), and fine particulate matter (PM2\.5\). The
chemistry module integrated in GEOS\-CF is identical to the offline GEOS\-Chem
model and readily benefits from the innovations provided by the GEOS\-Chem
community.


Evaluation of GEOS\-CF against satellite, ozonesonde, and surface
observations for years 2018–2019 shows realistic simulated
concentrations of O3, NO2, and CO, with normalized mean biases of −0\.1
to 0\.3, normalized root mean square errors between 0\.1–0\.4, and
correlations between 0\.3–0\.8\. Comparisons against surface observations
highlight the successful representation of air pollutants in many regions of
the world and during all seasons, yet also highlight current limitations,
such as a global high bias in SO2 and an overprediction of summertime O3
over the Southeast United States.


GEOS\-CF v1\.0 generally overestimates aerosols by 20%–50% due to known
issues in GEOS\-Chem v12\.0\.1 that have been addressed in later versions. The
5\-days forecasts have skill scores comparable to the 1\-day hindcast. Model
skills can be improved significantly by applying a bias\-correction to the
surface model output using a machine\-learning approach.





### Bands



**Pixel Size**
  
27750 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `CO` | Mol fraction | Carbon monoxide (CO, MW \= 28\.00 g mol\-1\) volume mixing ratio dry air |
| `NO2` | Mol fraction | Nitrogen dioxide (NO2, MW \= 46\.00 g mol\-1\) volume mixing ratio dry air |
| `O3` | Mol fraction | Ozone (O3, MW \= 48\.00 g mol\-1\) volume mixing ratio dry air |
| `PM25_RH35_GCC` | ug m\-3 | Particulate matter with diameter below 2\.5 um RH 35 |
| `PM25_RH35_GOCART` | kg/m^3 | Total reconstructed PM2\.5 RH 35 |
| `Q` | Mass fraction | Specific humidity |
| `RH` | None | Relative humidity after moist |
| `SLP` | Pa | Sea level pressure |
| `SO2` | Mol fraction | Sulfur dioxide (SO2, MW \= 64\.00 g mol\-1\) volume mixing ratio dry air |
| `T` | K | Air temperature |
| `U` | m/s | Eastward wind |
| `V` | m/s | Northward wind |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| creation\_time | DOUBLE | Time of creation |
| forecast\_time | DOUBLE | Forecast time |




### Terms of Use


**Terms of Use**


Unless otherwise noted, all NASA\-produced data may be used for any purpose
without prior permission. For more information and exceptions visit the
[NASA Data \& Information Policy page](https://earthdata.nasa.gov/collaborate/open-data-services-and-software/data-information-policy).




### Citations



Citations:
* Keller, C. A., Knowland, K. E., Duncan, B. N., Liu, J., Anderson, D. C.,
Das, S., ... \& Pawson, S. (2021\). Description of the NASA GEOS composition
forecast modeling system GEOS\-CF v1\. 0\. Journal of Advances in Modeling
Earth Systems, 13(4\), e2020MS002413\.
[doi:10\.1029/2020MS002413](https://doi.org/10.1029/2020MS002413)





### DOIs


* [https://doi.org/10\.1029/2020MS002413](https://doi.org/10.1029/2020MS002413)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varimageVisParamNO2={
'bands':['NO2'],
'min':6.96e-11,
'max':4.42e-8,
};

varimageVisParamT={
'bands':['T'],
'min':220,
'max':320,
'palette':['d7191c','fdae61','ffffbf','abd9e9','2c7bb6'],
};

vargeosCf=ee.ImageCollection('NASA/GEOS-CF/v1/fcst/htf');

Map.setCenter(100,20,3);

varweeklyT=
geosCf.select('T').filterDate('2022-11-01','2022-11-08').median();
Map.addLayer(weeklyT,imageVisParamT,'Weekly T',false,1);

varNO2=ee.Image('NASA/GEOS-CF/v1/fcst/htf/20221215_12z-20221216_1200z');
Map.addLayer(NO2,imageVisParamNO2,'NO2',true,1);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GEOS-CF_v1_fcst_htf)


[GEOS\-CF fcst htf v1: Goddard Earth Observing System Composition Forecast](/earth-engine/datasets/catalog/NASA_GEOS-CF_v1_fcst_htf)

This dataset contains meteorological forecast (fcst) of high\-temporal frequency data (htf). Use the 'creation\_time' and 'forecast\_time' properties to select data of interest. The Goddard Earth Observing System Composition Forecast (GEOS\-CF) system is a high\-resolution (0\.25°) global constituent prediction system from NASA's Global Modeling and Assimilation Office(GMAO). GEOS\-CF offers a new …

 NASA/GEOS\-CF/v1/fcst/htf,
 atmosphere,composition,forecast,geos,gmao,nasa

2022\-10\-01T00:00:00Z/2025\-07\-15T12:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1029/2020MS002413](https://doi.org/https://gmao.gsfc.nasa.gov/weather_prediction/GEOS-CF/)
* [https://doi.org/10\.1029/2020MS002413](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_GEOS-CF_v1_fcst_htf)









