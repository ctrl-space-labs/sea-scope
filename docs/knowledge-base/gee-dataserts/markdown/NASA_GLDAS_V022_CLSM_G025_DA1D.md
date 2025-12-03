



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GLDAS\-2\.2: Global Land Data Assimilation System


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================








Dataset Availability
2003\-01\-01T03:00:00Z–2025\-03\-31T00:00:00Z
Dataset Provider


[NASA GES DISC at NASA Goddard Earth Sciences Data and Information Services Center](https://doi.org/10.5067/TXBMLX370XX8)



Earth Engine Snippet


`ee.ImageCollection("NASA/GLDAS/V022/CLSM/G025/DA1D")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GLDAS_V022_CLSM_G025_DA1D)





Cadence
1 Day
Tags


[3\-hourly](/earth-engine/datasets/tags/3-hourly)
[climate](/earth-engine/datasets/tags/climate)
[cryosphere](/earth-engine/datasets/tags/cryosphere)
[evaporation](/earth-engine/datasets/tags/evaporation)
[forcing](/earth-engine/datasets/tags/forcing)
[geophysical](/earth-engine/datasets/tags/geophysical)
[gldas](/earth-engine/datasets/tags/gldas)
[humidity](/earth-engine/datasets/tags/humidity)
[ldas](/earth-engine/datasets/tags/ldas)
[nasa](/earth-engine/datasets/tags/nasa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[pressure](/earth-engine/datasets/tags/pressure)
[radiation](/earth-engine/datasets/tags/radiation)
[soil](/earth-engine/datasets/tags/soil)
[soil\-moisture](/earth-engine/datasets/tags/soil-moisture)
[surface](/earth-engine/datasets/tags/surface)
[temperature](/earth-engine/datasets/tags/temperature)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)
[wind](/earth-engine/datasets/tags/wind)








#### Description



NASA Global Land Data Assimilation System Version 2 (GLDAS\-2\) has three
components: GLDAS\-2\.0, GLDAS\-2\.1, and GLDAS\-2\.2\. GLDAS\-2\.0 is forced entirely
with the Princeton meteorological forcing input data and provides a temporally
consistent series from 1948 through 2014\. GLDAS\-2\.1 is forced with a combination
of model and observation data from 2000 to present. GLDAS\-2\.2 product suites use
data assimilation (DA), whereas the GLDAS\-2\.0 and GLDAS\-2\.1 products are
"open\-loop" (i.e., no data assimilation). The choice of forcing data, as well as
DA observation source, variable, and scheme, vary for different GLDAS\-2\.2
products.GLDAS\-2\.2 is new to the GES DISC archive and currently includes a main
product from CLSM\-F2\.5 with Data Assimilation for the Gravity Recovery and
Climate Experiment (GRACE\-DA) from February 2003 to present. The GLDAS\-2\.2
data are available in two production streams: main and Early, only main one
is ingested.


The GLDAS\-2\.2 GRACE\-DA product was simulated with Catchment\-F2\.5 in Land
Information System (LIS) Version 7\. The data product contains 24 land
surface fields from February 1, 2003 to present.


The simulation started on February 1, 2003 using the conditions from the
GLDAS\-2\.0 Daily Catchment model simulation, forced with the meteorological
analysis fields from the operational European Centre for Medium\-Range
Weather Forecasts (ECMWF) Integrated Forecasting System. The total
terrestrial water anomaly observation from GRACE satellite was assimilated
(Li et al, 2019\). Due to the data agreement with ECMWF, this GLDAS\-2\.2 daily
product does not include the meteorological forcing fields.


Documentation:


* [Readme](https://hydro1.gesdisc.eosdis.nasa.gov/data/GLDAS/GLDAS_CLSM025_DA1_D.2.2/doc/README_GLDAS2.pdf)
* [How\-to](https://disc.gsfc.nasa.gov/information/howto?tags=hydrology)
* [GES DISC Hydrology Documentation](https://disc.gsfc.nasa.gov/information/documents?title=Hydrology%20Documentation)


Provider's Note: the names with extension \_tavg are variables
averaged over the past 3\-hours, the names with extension '\_acc' are
variables accumulated over the past 3\-hours, the names with extension
'\_inst' are instantaneous variables, and the names with '\_f' are
forcing variables.





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `ACond_tavg` | m/s | 0\.000379\* | 5\.99291\* | Aerodynamic conductance |
| `AvgSurfT_tavg` | K | 179\.818\* | 324\.265\* | Average surface skin temperature |
| `CanopInt_tavg` | kg/m^2 | 0\* | 1\.57295\* | Plant canopy surface water |
| `ECanop_tavg` | kg/m^2/s | \-0\.021881\* | 5\.3e\-05\* | Canopy water evaporation |
| `ESoil_tavg` | kg/m^2/s | \-0\.003637\* | 0\.001172\* | Direct evaporation from bare soil |
| `EvapSnow_tavg` | kg/m^2/s | \-0\.021057\* | 0\.000728\* | Snow Evaporation |
| `Evap_tavg` | kg/m^2/s | \-0\.02737\* | 0\.00121\* | Evapotranspiration |
| `GWS_tavg` | mm | 77\.0153\* | 3599\.01\* | Ground water storage |
| `Lwnet_tavg` | W/m^2 | \-221\.308\* | 490\.842\* | Net long\-wave radiation flux |
| `Qg_tavg` | W/m^2 | \-344\.072\* | 174\.036\* | Heat flux |
| `Qh_tavg` | W/m^2 | \-2851\.75\* | 54076\.7\* | Sensible heat net flux |
| `Qle_tavg` | W/m^2 | \-53856\.6\* | 2983\.65\* | Latent heat net flux |
| `Qsb_tavg` | kg/m^2/s | 0\* | 0\.000416\* | Baseflow\-groundwater runoff |
| `Qsm_tavg` | kg/m^2/s | 0\* | 0\.018311\* | Snow melt |
| `Qs_tavg` | kg/m^2/s | 0\* | 0\.020244\* | Storm surface runoff |
| `SnowDepth_tavg` | m | 0\* | 8\.57951\* | Snow depth |
| `SnowT_tavg` | K | 179\.818\* | 324\.265\* | Snow Surface temperature |
| `SoilMoist_P_tavg` | kg/m^2 | 109\.394\* | 4049\.02\* | Profile Soil moisture |
| `SoilMoist_RZ_tavg` | kg/m^2 | 32\.3665\* | 478\.397\* | Root Zone Soil moisture |
| `SoilMoist_S_tavg` | kg/m^2 | 0\.001389\* | 9\.56\* | Surface Soil moisture |
| `SWE_tavg` | kg/m^2 | 0\* | 3688\.07\* | Snow depth water equivalent |
| `Swnet_tavg` | W/m^2 | 0\* | 421\.784\* | Net short wave radiation flux |
| `TVeg_tavg` | kg/m^2/s | \-0\.000371\* | 0\.001654\* | Transpiration |
| `TWS_tavg` | mm | 109\.394\* | 5084\.16\* | Terrestrial water storage |


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
* Li, B., M. Rodell, S. Kumar, H. Beaudoing, A. Getirana, B. F. Zaitchik, et
al. (2019\) Global GRACE data assimilation for groundwater and drought
monitoring: Advances and challenges. Water Resources Research, 55,
7564\-7586\.
* [Additional references](https://ldas.gsfc.nasa.gov/gldas/GLDASpublications.php)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/GLDAS/V022/CLSM/G025/DA1D')
.filter(ee.Filter.date('2010-06-01','2010-06-02'));
varaverageSurfaceSkinTemperatureK=dataset.select('AvgSurfT_tavg');
varaverageSurfaceSkinTemperatureKVis={
min:258,
max:316,
palette:['1303ff','42fff6','f3ff40','ff5d0f'],
};
Map.setCenter(71.72,52.48,3.0);
Map.addLayer(
averageSurfaceSkinTemperatureK,averageSurfaceSkinTemperatureKVis,
'Average Surface Skin Temperature [K]');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GLDAS_V022_CLSM_G025_DA1D)


[GLDAS\-2\.2: Global Land Data Assimilation System](/earth-engine/datasets/catalog/NASA_GLDAS_V022_CLSM_G025_DA1D)

NASA Global Land Data Assimilation System Version 2 (GLDAS\-2\) has three components: GLDAS\-2\.0, GLDAS\-2\.1, and GLDAS\-2\.2\. GLDAS\-2\.0 is forced entirely with the Princeton meteorological forcing input data and provides a temporally consistent series from 1948 through 2014\. GLDAS\-2\.1 is forced with a combination of model and observation data from 2000 …

 NASA/GLDAS/V022/CLSM/G025/DA1D,
 3\-hourly,climate,cryosphere,evaporation,forcing,geophysical,gldas,humidity,ldas,nasa,precipitation,pressure,radiation,soil,soil\-moisture,surface,temperature,water\-vapor,wind

2003\-01\-01T03:00:00Z/2025\-03\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








