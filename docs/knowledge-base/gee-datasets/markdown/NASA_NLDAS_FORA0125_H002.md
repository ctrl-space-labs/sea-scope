



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NLDAS\-2: North American Land Data Assimilation System Forcing Fields


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================================================








Dataset Availability
1979\-01\-01T13:00:00Z–2025\-07\-13T12:00:00Z
Dataset Provider


[NASA GES DISC at NASA Goddard Space Flight Center](https://doi.org/10.5067/6J5LHHOHZHN4)



Earth Engine Snippet


`ee.ImageCollection("NASA/NLDAS/FORA0125_H002")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_NLDAS_FORA0125_H002)





Cadence
1 Hour
Tags


[climate](/earth-engine/datasets/tags/climate)
[evaporation](/earth-engine/datasets/tags/evaporation)
[forcing](/earth-engine/datasets/tags/forcing)
[geophysical](/earth-engine/datasets/tags/geophysical)
[hourly](/earth-engine/datasets/tags/hourly)
[humidity](/earth-engine/datasets/tags/humidity)
[ldas](/earth-engine/datasets/tags/ldas)
[nasa](/earth-engine/datasets/tags/nasa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[pressure](/earth-engine/datasets/tags/pressure)
[radiation](/earth-engine/datasets/tags/radiation)
[soil](/earth-engine/datasets/tags/soil)
[temperature](/earth-engine/datasets/tags/temperature)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)
[wind](/earth-engine/datasets/tags/wind)
nldas








#### Description



Land Data Assimilation System (LDAS) combines multiple
sources of observations (such as precipitation gauge data, satellite
data, and radar precipitation measurements) to produce estimates
of climatological properties at or near the Earth''s surface.


This dataset is the primary (default) forcing file (File A) for
Phase 2 of the North American Land Data Assimilation System (NLDAS\-2\).
The data are in 1/8th\-degree grid spacing; the temporal resolution
is hourly.


NLDAS is a collaboration project among several groups: NOAA/NCEP''s
Environmental Modeling Center (EMC), NASA''s Goddard Space Flight
Center (GSFC), Princeton University, the University of Washington,
the NOAA/NWS Office of Hydrological Development (OHD), and the
NOAA/NCEP Climate Prediction Center (CPC). NLDAS is a core project
with support from NOAA''s Climate Prediction Program for the Americas
(CPPA).


Documentation:


* [Readme](https://hydro1.gesdisc.eosdis.nasa.gov/data/NLDAS/README.NLDAS2.pdf)
* [How\-To](https://disc.gsfc.nasa.gov/information/howto?tags=hydrology)
* [GES DISC Hydrology Documentation](https://disc.gsfc.nasa.gov/information/documents?title=Hydrology%20Documentation)
* [GES DISC Data Rods Documentation](https://disc.gsfc.nasa.gov/information/tools?title=Hydrology%20Data%20Rods)





### Bands



**Pixel Size**
  
13915 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `temperature` | °C | \-49\.79\* | 51\.2\* | Air temperature at 2 meters above the surface |
| `specific_humidity` | Mass fraction | 0\* | 0\.02\* | Specific humidity at 2 meters above the surface |
| `pressure` | Pa | 61847\.6\* | 105338\* | Surface pressure |
| `wind_u` | m/s | \-27\.93\* | 27\.54\* | U wind component at 10 meters above the surface |
| `wind_v` | m/s | \-27\.45\* | 35\.13\* | V wind component at 10 meters above the surface |
| `longwave_radiation` | W/m^2 | 72\.18\* | 545\.11\* | Surface downward longwave radiation |
| `convective_fraction` | None | 0\* | 1\* | Fraction of total precipitation that is convective: from NARR |
| `potential_energy` | J/kg | 0\* | 76666\.2\* | Convective available potential energy (J/kg): from NARR |
| `potential_evaporation` | kg/m^2 | 0\* | 2\.76\* | Potential evaporation: from NARR |
| `total_precipitation` | kg/m^2 | 0\* | 124\.19\* | Hourly total precipitation |
| `shortwave_radiation` | W/m^2 | 0\* | 1368\.54\* | Surface downward shortwave radiation \- bias corrected |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| end\_hour | DOUBLE | End hour |
| start\_hour | DOUBLE | Start hour |




### Terms of Use


**Terms of Use**


Distribution of data from the Goddard Earth Sciences
Data and Information Services Center (GES DISC) is funded by NASA's
Science Mission Directorate (SMD). Consistent with NASA [Earth
Science Data and Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy/),
data from the GES DISC archive are available free to the user community.
For more information visit the GES DISC [Data Policy](https://disc.sci.gsfc.nasa.gov/citing)
page.




### Citations



Citations:
* The data set source should be properly cited when the data are
used. A formal reference of the form: \\, 2012, last updated
2013: \\. NASA/GSFC, Greenbelt, MD, USA, NASA Goddard
Earth Sciences Data and Information Services Center (GES DISC).
Accessed \\ at \\ is suggested following
Parsons et al. (2010\), [doi:10\.1029/2010EO340001](https://doi.org/10.1029/2010EO340001).





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/NLDAS/FORA0125_H002')
.filter(ee.Filter.date('2018-07-01','2018-07-30'));
vartemperature=dataset.select('temperature');
vartemperatureVis={
min:-5.0,
max:40.0,
palette:['3d2bd8','4e86da','62c7d8','91ed90','e4f178','ed6a4c'],
};
Map.setCenter(-110.21,35.1,4);
Map.addLayer(temperature,temperatureVis,'Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_NLDAS_FORA0125_H002)


[NLDAS\-2: North American Land Data Assimilation System Forcing Fields](/earth-engine/datasets/catalog/NASA_NLDAS_FORA0125_H002)

Land Data Assimilation System (LDAS) combines multiple sources of observations (such as precipitation gauge data, satellite data, and radar precipitation measurements) to produce estimates of climatological properties at or near the Earth''s surface. This dataset is the primary (default) forcing file (File A) for Phase 2 of the North American …

 NASA/NLDAS/FORA0125\_H002,
 climate,evaporation,forcing,geophysical,hourly,humidity,ldas,nasa,precipitation,pressure,radiation,soil,temperature,water\-vapor,wind

1979\-01\-01T13:00:00Z/2025\-07\-13T12:00:00Z



 24\.85 \-125\.15 53\.28 \-66\.85
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








