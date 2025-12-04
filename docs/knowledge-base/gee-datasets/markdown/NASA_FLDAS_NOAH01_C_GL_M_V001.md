



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

FLDAS: Famine Early Warning Systems Network (FEWS NET) Land Data Assimilation System


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================================================








Dataset Availability
1982\-01\-01T00:00:00Z–2025\-05\-01T00:00:00Z
Dataset Provider


[NASA GES DISC at NASA Goddard Space Flight Center](https://doi.org/10.5067/5NHC22T9375G)



Earth Engine Snippet


`ee.ImageCollection("NASA/FLDAS/NOAH01/C/GL/M/V001")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_FLDAS_NOAH01_C_GL_M_V001)





Cadence
1 Month
Tags


[climate](/earth-engine/datasets/tags/climate)
[cryosphere](/earth-engine/datasets/tags/cryosphere)
[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[humidity](/earth-engine/datasets/tags/humidity)
[ldas](/earth-engine/datasets/tags/ldas)
[monthly](/earth-engine/datasets/tags/monthly)
[nasa](/earth-engine/datasets/tags/nasa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[runoff](/earth-engine/datasets/tags/runoff)
[snow](/earth-engine/datasets/tags/snow)
[soil](/earth-engine/datasets/tags/soil)
[soil\-moisture](/earth-engine/datasets/tags/soil-moisture)
[soil\-temperature](/earth-engine/datasets/tags/soil-temperature)
[temperature](/earth-engine/datasets/tags/temperature)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)
[wind](/earth-engine/datasets/tags/wind)
famine
fldas








#### Description



The FLDAS dataset (McNally et al. 2017\), was designed to assist with food
security assessments in data\-sparse, developing country settings. It
includes information on many climate\-related variables including moisture
content, humidity, evapotranspiration, average soil temperature, total
precipitation rate, etc.


There are multiple different FLDAS datasets; this one uses Noah version
3\.6\.1 surface model with CHIRPS\-6 hourly rainfall that has been
downscaled using the [NASA Land Surface Data Toolkit](https://lis.gsfc.nasa.gov/software/ldt).
which is part of the [Land Information System
framework](/earth-engine/datasets/catalog/LIS;%20%5Bhttps:/lis.gsfc.nasa.gov/%5D(https:/lis.gsfc.nasa.gov/)). Temporal desegregation is required so that daily
rainfall inputs can be used in both energy and water balance calculations


For forcing data, this simulation uses a combination of the new version of Modern\-Era
Retrospective analysis for Research and Applications version 2 (MERRA\-2\) data and Climate
Hazards Group InfraRed Precipitation with Station data (CHIRPS), a quasi\-global rainfall
dataset designed for seasonal drought monitoring and trend analysis (Funk et al., 2015\).


Documentation:


* [Readme](https://hydro1.gesdisc.eosdis.nasa.gov/data/FLDAS/FLDAS_NOAH01_C_GL_M.001/doc/README_FLDAS.pdf)
* [How\-to](https://disc.gsfc.nasa.gov/information/howto?tags=hydrology)
* [GES DISC Hydrology Documentation](https://disc.gsfc.nasa.gov/information/documents?title=Hydrology%20Documentation)





### Bands



**Pixel Size**
  
11132 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `Evap_tavg` | kg/m^2/s | Evapotranspiration |
| `LWdown_f_tavg` | W/m^2 | Downward longwave radiation flux |
| `Lwnet_tavg` | W/m^2 | Net longwave radiation flux |
| `Psurf_f_tavg` | Pa | Surface pressure |
| `Qair_f_tavg` | Mass fraction | Specific humidity |
| `Qg_tavg` | W/m^2 | Soil heat flux |
| `Qh_tavg` | W/m^2 | Sensible heat net flux |
| `Qle_tavg` | W/m^2 | Latent heat net flux |
| `Qs_tavg` | kg/m^2/s | Storm surface runoff |
| `Qsb_tavg` | kg/m^2/s | Baseflow\-groundwater runoff |
| `RadT_tavg` | K | Surface radiative temperature |
| `Rainf_f_tavg` | kg/m^2/s | Total precipitation rate |
| `SnowCover_inst` | None | Snow cover fraction |
| `SnowDepth_inst` | m | Snow depth |
| `Snowf_tavg` | kg/m^2/s | Snowfall rate |
| `SoilMoi00_10cm_tavg` | Volume fraction | Soil moisture (0 \- 10 cm underground) |
| `SoilMoi10_40cm_tavg` | Volume fraction | Soil moisture (10 \- 40 cm underground) |
| `SoilMoi100_200cm_tavg` | Volume fraction | Soil moisture (100 \- 200 cm underground) |
| `SoilMoi40_100cm_tavg` | Volume fraction | Soil moisture (40 \- 100 cm underground) |
| `SoilTemp00_10cm_tavg` | K | Soil temperature (0 \- 10 cm underground) |
| `SoilTemp10_40cm_tavg` | K | Soil temperature (10 \- 40 cm underground) |
| `SoilTemp100_200cm_tavg` | K | Soil temperature (100 \- 200 cm underground) |
| `SoilTemp40_100cm_tavg` | K | Soil temperature (40 \- 100 cm underground) |
| `SWdown_f_tavg` | W/m^2 | Surface downward shortwave radiation |
| `SWE_inst` | kg/m^2 | Snow water equivalent |
| `Swnet_tavg` | W/m^2 | Net shortwave radiation flux |
| `Tair_f_tavg` | K | Near surface air temperature |
| `Wind_f_tavg` | m/s | Near surface wind speed |




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
* If you use these data in your research or applications, please include a
reference in your publication(s) similar to the following example:
Amy McNally NASA/GSFC/HSL (2018\), FLDAS Noah Land Surface Model L4 Global
Monthly 0\.1 x 0\.1 degree (MERRA\-2 and CHIRPS), Greenbelt, MD, USA, Goddard
Earth Sciences Data and Information Services Center (GES DISC), Accessed:
\[Data Access Date], [doi:10\.5067/5NHC22T9375G](https://doi.org/10.5067/5NHC22T9375G)
* McNally, A., Arsenault, K., Kumar, S., Shukla, S., Peterson, P., Wang, S., Funk, C.,
Peters\-Lidard, C.D., \& Verdin, J. P. (2017\). A land data assimilation system for
sub\-Saharan Africa food and water security applications. Scientific Data, 4, 170012\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/FLDAS/NOAH01/C/GL/M/V001')
.filter(ee.Filter.date('2018-11-01','2018-12-01'));
varlayer=dataset.select('Evap_tavg');

varband_viz={
min:0.0,
max:0.00005,
opacity:1.0,
palette:['black','blue','purple','cyan','green','yellow','red']
};

Map.setCenter(30.0,30.0,2);
Map.addLayer(layer,band_viz,'Average Evapotranspiration');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_FLDAS_NOAH01_C_GL_M_V001)


[FLDAS: Famine Early Warning Systems Network (FEWS NET) Land Data Assimilation System](/earth-engine/datasets/catalog/NASA_FLDAS_NOAH01_C_GL_M_V001)

The FLDAS dataset (McNally et al. 2017\), was designed to assist with food security assessments in data\-sparse, developing country settings. It includes information on many climate\-related variables including moisture content, humidity, evapotranspiration, average soil temperature, total precipitation rate, etc. There are multiple different FLDAS datasets; this one uses Noah version …

 NASA/FLDAS/NOAH01/C/GL/M/V001,
 climate,cryosphere,evapotranspiration,humidity,ldas,monthly,nasa,precipitation,runoff,snow,soil,soil\-moisture,soil\-temperature,temperature,water\-vapor,wind

1982\-01\-01T00:00:00Z/2025\-05\-01T00:00:00Z



 \-60 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








