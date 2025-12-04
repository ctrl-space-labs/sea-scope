



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GLDAS\-2\.1: Global Land Data Assimilation System


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================








Dataset Availability
2000\-01\-01T03:00:00Z–2025\-06\-15T21:00:00Z
Dataset Provider


[NASA GES DISC at NASA Goddard Space Flight Center](https://doi.org/10.5067/E7TYRXPJKWOQ)



Earth Engine Snippet


`ee.ImageCollection("NASA/GLDAS/V021/NOAH/G025/T3H")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GLDAS_V021_NOAH_G025_T3H)





Cadence
3 Hours
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
products.GLDAS\-2\.1 is one of two components of the GLDAS Version 2 (GLDAS\-2\) dataset,
the second being GLDAS\-2\.0\. GLDAS\-2\.1 is analogous to GLDAS\-1 product stream,
with upgraded models forced by a combination of [GDAS, disaggregated GPCP,
and AGRMET radiation data sets](https://ldas.gsfc.nasa.gov/gldas/GLDASforcing.php).


The GLDAS\-2\.1 simulation started on January 1, 2000 using the
conditions from the GLDAS\-2\.0 simulation. This simulation was
forced with National Oceanic and Atmospheric Administration
(NOAA)/Global Data Assimilation System (GDAS) atmospheric analysis
fields (Derber et al., 1991\), the disaggregated Global Precipitation
Climatology Project (GPCP) precipitation fields (Adler et al., 2003\),
and the Air Force Weather Agency's AGRicultural METeorological
modeling system (AGRMET) radiation fields which became available
for March 1, 2001 onwards.


Documentation:


* [Readme](https://hydro1.gesdisc.eosdis.nasa.gov/data/GLDAS/GLDAS_NOAH025_3H.2.1/doc/README_GLDAS2.pdf)
* [How\-to](https://disc.gsfc.nasa.gov/information/howto?tags=hydrology)
* [GES DISC Hydrology Documentation](https://disc.gsfc.nasa.gov/information/documents?title=Hydrology%20Documentation)
* [GES DISC Data Rods Documentation](https://disc.gsfc.nasa.gov/information/tools?title=Hydrology%20Data%20Rods)


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
| `Albedo_inst` | % | 4\.99\* | 82\.25\* | Albedo |
| `AvgSurfT_inst` | K | 187\.48\* | 1323\.35\* | Average surface skin temperature |
| `CanopInt_inst` | kg/m^2 | 0\* | 0\.5\* | Plant canopy surface water |
| `ECanop_tavg` | W/m^2 | 0\* | 1273\.66\* | Canopy water evaporation |
| `ESoil_tavg` | W/m^2 | 0\* | 2275\.63\* | Direct evaporation from bare soil |
| `Evap_tavg` | kg/m^2/s | 0\* | 0\.002\* | Evapotranspiration |
| `LWdown_f_tavg` | W/m^2 | 26\.85\* | 600\.9\* | Downward long\-wave radiation flux |
| `Lwnet_tavg` | W/m^2 | \-13792\.7\* | 196\.97\* | Net long\-wave radiation flux |
| `PotEvap_tavg` | W/m^2 | \-227\.75\* | 18977\.9\* | Potential evaporation rate |
| `Psurf_f_inst` | Pa | 44063\.1\* | 108344\* | Pressure |
| `Qair_f_inst` | Mass fraction | \-0\.02\* | 0\.07\* | Specific humidity |
| `Qg_tavg` | W/m^2 | \-552\.64\* | 1538\.41\* | Heat flux |
| `Qh_tavg` | W/m^2 | \-1005\.15\* | 18190\.6\* | Sensible heat net flux |
| `Qle_tavg` | W/m^2 | \-227\.75\* | 5072\.25\* | Latent heat net flux |
| `Qs_acc` | kg/m^2 | 0\* | 170\.93\* | Storm surface runoff |
| `Qsb_acc` | kg/m^2 | 0\* | 50\.6\* | Baseflow\-groundwater runoff |
| `Qsm_acc` | kg/m^2 | 0\* | 42\.87\* | Snow melt |
| `Rainf_f_tavg` | kg/m^2/s | 0\* | 0\.01\* | Total precipitation rate |
| `Rainf_tavg` | kg/m^2/s | 0\* | 0\.01\* | Rain precipitation rate |
| `RootMoist_inst` | kg/m^2 | 2\* | 949\.6\* | Root zone soil moisture |
| `SWE_inst` | kg/m^2 | 0\* | 120787\* | Snow depth water equivalent |
| `SWdown_f_tavg` | W/m^2 | \-56\.93\* | 30462\.8\* | Downward short\-wave radiation flux |
| `SnowDepth_inst` | m | 0\* | 301\.96\* | Snow depth |
| `Snowf_tavg` | kg/m^2/s | 0\* | 0\.009\* | Snow precipitation rate |
| `SoilMoi0_10cm_inst` | kg/m^2 | 1\.99\* | 47\.59\* | Soil moisture |
| `SoilMoi10_40cm_inst` | kg/m^2 | 5\.99\* | 142\.8\* | Soil moisture |
| `SoilMoi40_100cm_inst` | kg/m^2 | 11\.99\* | 285\.6\* | Soil moisture |
| `SoilMoi100_200cm_inst` | kg/m^2 | 20\* | 476\* | Soil moisture |
| `SoilTMP0_10cm_inst` | K | 221\.98\* | 377\.5\* | Soil temperature |
| `SoilTMP10_40cm_inst` | K | 227\.43\* | 319\.44\* | Soil temperature |
| `SoilTMP40_100cm_inst` | K | 232\.97\* | 316\.2\* | Soil temperature |
| `SoilTMP100_200cm_inst` | K | 238\.52\* | 314\.11\* | Soil temperature |
| `Swnet_tavg` | W/m^2 | \-48\.96\* | 23741\.3\* | Net short wave radiation flux |
| `Tair_f_inst` | K | 206\.8\* | 327\.66\* | Air temperature |
| `Tveg_tavg` | W/m^2 | 0\* | 3455\.14\* | Transpiration |
| `Wind_f_inst` | m/s | 0\* | 57\.7\* | Wind speed |


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
* Rodell, M., P.R. Houser, U. Jambor, J. Gottschalck, K. Mitchell,
C.\-J. Meng, K. Arsenault, B. Cosgrove, J. Radakovich, M. Bosilovich,
J.K. Entin, J.P. Walker, D. Lohmann, and D. Toll, The Global Land Data
Assimilation System, Bull. Amer. Meteor. Soc., 85(3\), 381\-394, 2004\.
* [Additional references](https://ldas.gsfc.nasa.gov/gldas/GLDASpublications.php)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/GLDAS/V021/NOAH/G025/T3H')
.filter(ee.Filter.date('2010-06-01','2010-06-02'));
varaverageSurfaceSkinTemperatureK=dataset.select('AvgSurfT_inst');
varaverageSurfaceSkinTemperatureKVis={
min:250.0,
max:300.0,
palette:['1303ff','42fff6','f3ff40','ff5d0f'],
};
Map.setCenter(71.72,52.48,3.0);
Map.addLayer(
averageSurfaceSkinTemperatureK,averageSurfaceSkinTemperatureKVis,
'Average Surface Skin Temperature [K]');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GLDAS_V021_NOAH_G025_T3H)


[GLDAS\-2\.1: Global Land Data Assimilation System](/earth-engine/datasets/catalog/NASA_GLDAS_V021_NOAH_G025_T3H)

NASA Global Land Data Assimilation System Version 2 (GLDAS\-2\) has three components: GLDAS\-2\.0, GLDAS\-2\.1, and GLDAS\-2\.2\. GLDAS\-2\.0 is forced entirely with the Princeton meteorological forcing input data and provides a temporally consistent series from 1948 through 2014\. GLDAS\-2\.1 is forced with a combination of model and observation data from 2000 …

 NASA/GLDAS/V021/NOAH/G025/T3H,
 3\-hourly,climate,cryosphere,evaporation,forcing,geophysical,gldas,humidity,ldas,nasa,precipitation,pressure,radiation,soil,soil\-moisture,surface,temperature,water\-vapor,wind

2000\-01\-01T03:00:00Z/2025\-06\-15T21:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








