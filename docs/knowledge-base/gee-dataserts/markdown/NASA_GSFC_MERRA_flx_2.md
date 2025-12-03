



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MERRA\-2 M2T1NXFLX: Surface Flux Diagnostics V5\.12\.4


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================








Dataset Availability
1980\-01\-01T00:00:00Z–2025\-06\-01T23:00:00Z
Dataset Provider


[NASA/MERRA](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GSFC/MERRA/flx/2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_flx_2)





Cadence
1 Hour
Tags


[climate](/earth-engine/datasets/tags/climate)
[merra](/earth-engine/datasets/tags/merra)
[precipitation](/earth-engine/datasets/tags/precipitation)
[sea\-salt](/earth-engine/datasets/tags/sea-salt)
[so2](/earth-engine/datasets/tags/so2)
[so4](/earth-engine/datasets/tags/so4)
[soil\-moisture](/earth-engine/datasets/tags/soil-moisture)








#### Description



M2T1NXFLX (or tavg1\_2d\_flx\_Nx) is an hourly time\-averaged data
collection in Modern\-Era Retrospective analysis for Research and
Applications version 2 (MERRA\-2\). This collection consists of
assimilated surface flux diagnostics, such as total precipitation, bias
corrected total precipitation, surface air temperature, surface specific
humidity, surface wind speed, and evaporation from turbulence. The
"surface" in this data collection is the model surface layer. The
heights of the model surface layer (HLML) vary with time and location,
with the value of \~60 meters above ground. The data field is time\-stamped
with the central time of an hour starting from 00:30 UTC, e.g.: 00:30,
01:30, ... , 23:30 UTC.


MERRA\-2 is the latest version of global atmospheric reanalysis for the
satellite era produced by [NASA Global Modeling and Assimilation Office
(GMAO)](https://gmao.gsfc.nasa.gov/) using the [Goddard Earth Observing
System Model (GEOS)](https://gmao.gsfc.nasa.gov/GEOS_systems/) version
5\.12\.4\. The dataset covers the period of 1980\-present with the latency
of \~3 weeks after the end of a month.





### Bands



**Pixel Size**
  
69375 meters




**Y Pixel Size**
  
55000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `BSTAR` | m/s^2 | \-0\.021035\* | 0\.791739\* | Surface buoyancy scale |
| `CDH` | kg/m^2/s | 8e\-06\* | 0\.522482\* | Surface exchange coefficient for heat |
| `CDM` | kg/m^2/s | 5e\-06\* | 0\.518079\* | Surface exchange coefficient for momentum |
| `CDQ` | kg/m^2/s | 8e\-06\* | 0\.522482\* | Surface exchange coefficient for moisture |
| `CN` | None | 0\.000646\* | 0\.032227\* | Surface neutral drag coefficient |
| `DISPH` | m | 0\* | 23\.0781\* | Zero plane displacement height |
| `EFLUX` | W/m^2 | \-308\.949\* | 1655\.85\* | Total latent energy flux |
| `EVAP` | kg/m^2/s | \-0\.00011\* | 0\.000673\* | Evaporation from turbulence |
| `FRCAN` | None | 0\* | 1\* | Areal fraction of anvil showers |
| `FRCCN` | None | 0\* | 0\.423096\* | Areal fraction of convective showers |
| `FRCLS` | None | 0\* | 1\* | Areal fraction of nonanvil large scale showers |
| `FRSEAICE` | None | 0\* | 1\* | Ice covered fraction of tile |
| `GHTSKIN` | W/m^2 | \-245\.078\* | 1e\+15\* | Ground heating for skin temperature |
| `HFLUX` | W/m^2 | \-1181\.24\* | 686\.742\* | Sensible heat flux from turbulence |
| `HLML` | m | 42\.3642\* | 71\.0599\* | Surface layer height |
| `NIRDF` | W/m^2 | 0\* | 282\.495\* | Surface downwelling nearinfrared diffuse flux |
| `NIRDR` | W/m^2 | 0\* | 592\.217\* | Surface downwelling nearinfrared beam flux |
| `PBLH` | m | 42\.3621\* | 5780\.88\* | Planetary boundary layer height |
| `PGENTOT` | kg/m^2/s | 0\* | 0\.017593\* | Total column production of precipitation |
| `PRECANV` | kg/m^2/s | 0\* | 0\.000968\* | Anvil precipitation |
| `PRECCON` | kg/m^2/s | 0\* | 0\.002629\* | Convective precipitation |
| `PRECLSC` | kg/m^2/s | 0\* | 0\.014614\* | Nonanvil large scale precipitation |
| `PRECSNO` | kg/m^2/s | 0\* | 0\.006308\* | Snowfall |
| `PRECTOTCORR` | kg/m^2/s | 0\* | 0\.110565\* | Total precipitation |
| `PRECTOT` | kg/m^2/s | 0\* | 0\.017509\* | Total precipitation |
| `PREVTOT` | kg/m^2/s | 0\* | 0\.001474\* | Total column re\-evaporation/sublimation of precipitation |
| `QLML` | None | 0\* | 0\.034333\* | Surface specific humidity |
| `QSH` | Mass fraction | 0\* | 0\.044069\* | Effective surface specific humidity |
| `QSTAR` | Mass fraction | \-0\.000139\* | 0\.005463\* | Surface moisture scale |
| `RHOA` | kg/m^3 | 0\.658498\* | 1\.68283\* | Air density at surface |
| `RISFC` | None | \-318\.273\* | 578\.05\* | Surface bulk Richardson number |
| `SPEEDMAX` | m/s | 0\.074227\* | 49\.4767\* | Surface wind speed |
| `SPEED` | m/s | 0\.061141\* | 49\.3541\* | Surface wind speed |
| `TAUGWX` | N/m^2 | \-3\.06294\* | 5\.8716\* | Surface eastward gravity wave stress |
| `TAUGWY` | N/m^2 | \-5\.10649\* | 4\.99554\* | Surface northward gravity wave stress |
| `TAUX` | N/m^2 | \-5\.48865\* | 5\.09378\* | Eastward surface stress |
| `TAUY` | N/m^2 | \-6\.19036\* | 4\.19191\* | Northward surface stress |
| `TCZPBL` | m | 6\.55864\* | 2\.83712e\+06\* | Transcom planetary boundary layer height |
| `TLML` | K | 191\.833\* | 320\.174\* | Surface air temperature |
| `TSH` | K | 185\.73\* | 328\.859\* | Effective surface skin temperature |
| `TSTAR` | K | \-11\.0761\* | 5\.74402\* | Surface temperature scale |
| `ULML` | m/s | \-48\.8082\* | 42\.8239\* | Surface eastward wind |
| `USTAR` | m/s | 0\.000667\* | 2\.31844\* | Surface velocity scale |
| `VLML` | m/s | \-41\.9408\* | 44\.3777\* | Surface northward wind |
| `Z0H` | m | 1e\-05\* | 4\.54622\* | Surface roughness for heat |
| `Z0M` | m | 1e\-05\* | 4\.54622\* | Surface roughness |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


NASA promotes the full and open sharing of all data with research and
applications communities, private industry, academia, and the general
public.




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/GSFC/MERRA/flx/2')
.filter(ee.Filter.date('2022-02-01','2022-02-02'));
varsurface_buoyancy_scale=dataset.select('BSTAR');
varsbsVis={
min:-0.00998,
max:0.01174,
palette:['001137','01abab','e7eb05','620500']
};
Map.setCenter(-95,39,2);
Map.addLayer(surface_buoyancy_scale,sbsVis,'Surface buoyancy scale');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_flx_2)


[MERRA\-2 M2T1NXFLX: Surface Flux Diagnostics V5\.12\.4](/earth-engine/datasets/catalog/NASA_GSFC_MERRA_flx_2)

M2T1NXFLX (or tavg1\_2d\_flx\_Nx) is an hourly time\-averaged data collection in Modern\-Era Retrospective analysis for Research and Applications version 2 (MERRA\-2\). This collection consists of assimilated surface flux diagnostics, such as total precipitation, bias corrected total precipitation, surface air temperature, surface specific humidity, surface wind speed, and evaporation from turbulence. The …

 NASA/GSFC/MERRA/flx/2,
 climate,merra,precipitation,sea\-salt,so2,so4,soil\-moisture

1980\-01\-01T00:00:00Z/2025\-06\-01T23:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








