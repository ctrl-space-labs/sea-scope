



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GEOS\-CF fcst tavg1hr v1: Goddard Earth Observing System Composition Forecast


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================================================================








Dataset Availability
2022\-10\-01T00:00:00Z–2025\-07\-15T12:00:00Z
Dataset Provider


[NASA / GMAO](https://gmao.gsfc.nasa.gov/weather_prediction/GEOS-CF/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GEOS-CF/v1/fcst/tavg1hr")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GEOS-CF_v1_fcst_tavg1hr)





Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[composition](/earth-engine/datasets/tags/composition)
[forecast](/earth-engine/datasets/tags/forecast)
[geos](/earth-engine/datasets/tags/geos)
[gmao](/earth-engine/datasets/tags/gmao)
[nasa](/earth-engine/datasets/tags/nasa)








#### Description



This dataset contains meteorological forecast (fcst) of time\-averaged
frequency data (tavg1hr). Use the 'creation\_time' and 'forecast\_time' properties
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
| `ACET` | Mol fraction | Acetone (CH3C(O)CH3, MW \= 58\.08 g mol\-1\) volume mixing ratio dry air |
| `ALD2` | Mol fraction | Acetaldehyde (CH3CHO, MW \= 44\.05 g mol\-1\) volume mixing ratio dry air |
| `ALK4` | Mol fraction | Lumped \>\= C4 Alkanes (MW \= 58\.12 g mol\-1\) volume mixing ratio dry air |
| `AOD550_BC` | None | Black carbon optical depth at 550nm |
| `AOD550_CLOUD` | None | Cloud optical depth |
| `AOD550_DST1` | None | Dust bin1 optical depth at 550nm |
| `AOD550_DST2` | None | Dust bin2 optical depth at 550nm |
| `AOD550_DST3` | None | Dust bin3 optical depth at 550nm |
| `AOD550_DST4` | None | Dust bin4 optical depth at 550nm |
| `AOD550_DST5` | None | Dust bin5 optical depth at 550nm |
| `AOD550_DST6` | None | Dust bin6 optical depth at 550nm |
| `AOD550_DST7` | None | Dust bin7 optical depth at 550nm |
| `AOD550_DUST` | None | Dust optical depth at 550nm |
| `AOD550_OC` | None | Organic carbon optical depth at 550nm |
| `AOD550_SALA` | None | Accumulation mode sea salt optical depth at 550nm |
| `AOD550_SALC` | None | Coarse mode sea salt optical depth at 550nm |
| `AOD550_SULFATE` | None | Sulfate optical depth at 550nm |
| `BCPI` | Mol fraction | Hydrophilic black carbon aerosol (MW \= 12\.01 g mol\-1\) volume mixing ratio dry air |
| `BCPO` | Mol fraction | Hydrophobic black carbon aerosol (MW \= 12\.01 g mol\-1\) volume mixing ratio dry air |
| `BENZ` | Mol fraction | Benzene (C6H6, MW \= 78\.11 g mol\-1\) volume mixing ratio dry air |
| `C2H6` | Mol fraction | Ethane (C2H6, MW \= 30\.07 g mol\-1\) volume mixing ratio dry air |
| `C3H8` | Mol fraction | Propane (C3H8, MW \= 44\.10 g mol\-1\) volume mixing ratio dry air |
| `CH4` | Mol fraction | Methane (CH4, MW \= 16\.00 g mol\-1\) volume mixing ratio dry air |
| `CLDTT` | None | Total cloud area fraction |
| `CO` | Mol fraction | Carbon monoxide (CO, MW \= 28\.00 g mol\-1\) volume mixing ratio dry air |
| `DRYDEPFLX_BCPI` | molec cm\-2 s\-1 | Hydrophilic black carbon aerosol (MW \= 12\.01 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_BCPO` | molec cm\-2 s\-1 | Hydrophobic black carbon aerosol (MW \= 12\.01 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_DST1` | molec cm\-2 s\-1 | Dust aerosol, Reff \= 0\.7 microns (MW \= 29\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_DST2` | molec cm\-2 s\-1 | Dust aerosol, Reff \= 1\.4 microns (MW \= 29\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_DST3` | molec cm\-2 s\-1 | Dust aerosol, Reff \= 2\.4 microns (MW \= 29\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_DST4` | molec cm\-2 s\-1 | Dust aerosol, Reff \= 4\.5 microns (MW \= 29\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_HCHO` | molec cm\-2 s\-1 | Formaldehyde (CH2O, MW \= 30\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_HNO3` | molec cm\-2 s\-1 | Nitric acid (HNO3, MW \= 63\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_NH3` | molec cm\-2 s\-1 | Ammonia (NH3, MW \= 17\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_NH4` | molec cm\-2 s\-1 | Ammonium (NH4, MW \= 18\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_NIT` | molec cm\-2 s\-1 | Inorganic nitrates (MW \= 62\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_NO2` | molec cm\-2 s\-1 | Nitrogen dioxide (NO2, MW \= 46\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_O3` | molec cm\-2 s\-1 | Ozone (O3, MW \= 48\.00 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_OCPI` | molec cm\-2 s\-1 | Hydrophilic organic carbon aerosol (MW \= 12\.01 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_OCPO` | molec cm\-2 s\-1 | Hydrophobic organic carbon aerosol (MW \= 12\.01 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_SALA` | molec cm\-2 s\-1 | Fine (0\.01\-0\.05 microns) sea salt aerosol (MW \= 31\.40 g mol\-1\) dry deposition flux |
| `DRYDEPFLX_SALC` | molec cm\-2 s\-1 | Coarse (0\.5\-8 microns) sea salt aerosol (MW \= 31\.40 g mol\-1\) dry deposition flux |
| `DST1` | Mol fraction | Dust aerosol, Reff \= 0\.7 microns (MW \= 29\.00 g mol\-1\) volume mixing ratio dry air |
| `DST2` | Mol fraction | Dust aerosol, Reff \= 1\.4 microns (MW \= 29\.00 g mol\-1\) volume mixing ratio dry air |
| `DST3` | Mol fraction | Dust aerosol, Reff \= 2\.4 microns (MW \= 29\.00 g mol\-1\) volume mixing ratio dry air |
| `DST4` | Mol fraction | Dust aerosol, Reff \= 4\.5 microns (MW \= 29\.00 g mol\-1\) volume mixing ratio dry air |
| `EOH` | Mol fraction | Ethanol (C2H5OH, MW \= 46\.07 g mol\-1\) volume mixing ratio dry air |
| `H2O2` | Mol fraction | Hydrogen peroxide (H2O2, MW \= 34\.00 g mol\-1\) volume mixing ratio dry air |
| `HCHO` | Mol fraction | Formaldehyde (CH2O, MW \= 30\.00 g mol\-1\) volume mixing ratio dry air |
| `HNO3` | Mol fraction | Nitric acid (HNO3, MW \= 63\.00 g mol\-1\) volume mixing ratio dry air |
| `HNO4` | Mol fraction | Peroxynitric acid (HNO4, MW \= 79\.00 g mol\-1\) volume mixing ratio dry air |
| `ISOP` | Mol fraction | Isoprene (CH2\=C(CH3\)CH\=CH2, MW \= 68\.12 g mol\-1\) volume mixing ratio dry air |
| `MACR` | Mol fraction | Methacrolein (CH2\=C(CH3\)CHO, MW \= 70\.00 g mol\-1\) volume mixing ratio dry air |
| `MEK` | Mol fraction | Methyl Ethyl Ketone (RC(O)R, MW \= 72\.11 g mol\-1\) volume mixing ratio dry air |
| `MVK` | Mol fraction | Methyl vinyl ketone (CH2\=CHC(\=O)CH3, MW \= 70\.00 g mol\-1\) volume mixing ratio dry air |
| `N2O5` | Mol fraction | Dinitrogen pentoxide (N2O5, MW \= 108\.00 g mol\-1\) volume mixing ratio dry air |
| `NH3` | Mol fraction | Ammonia (NH3, MW \= 17\.00 g mol\-1\) volume mixing ratio dry air |
| `NH4` | Mol fraction | Ammonium (NH4, MW \= 18\.00 g mol\-1\) volume mixing ratio dry air |
| `NIT` | Mol fraction | Inorganic nitrates (MW \= 62\.00 g mol\-1\) volume mixing ratio dry air |
| `NO` | Mol fraction | Nitrogen oxide (NO, MW \= 30\.00 g mol\-1\) volume mixing ratio dry air |
| `NO2` | Mol fraction | Nitrogen dioxide (NO2, MW \= 46\.00 g mol\-1\) volume mixing ratio dry air |
| `NOy` | Mol fraction | Reactive nitrogen \= NO NO2 HNO3 HNO4 HONO 2xN2O5 PAN OrganicNitrates AerosolNitrates |
| `O3` | Mol fraction | Ozone (O3, MW \= 48\.00 g mol\-1\) volume mixing ratio dry air |
| `OCPI` | Mol fraction | Hydrophilic organic carbon aerosol (MW \= 12\.01 g mol\-1\) volume mixing ratio dry air |
| `OCPO` | Mol fraction | Hydrophobic organic carbon aerosol (MW \= 12\.01 g mol\-1\) volume mixing ratio dry air |
| `PAN` | Mol fraction | Peroxyacetyl nitrate (CH3C(O)OONO2, MW \= 121\.00 g mol\-1\) volume mixing ratio dry air |
| `PHIS` | m^2 s\-2 | Surface geopotential height |
| `PM25_RH35_GCC` | ug m\-3 | Particulate matter with diameter below 2\.5 um RH 35 |
| `PM25_RH35_GOCART` | kg/m^3 | Total reconstructed PM2\.5 RH 35 |
| `PM25bc_RH35_GCC` | ug m\-3 | Black carbon particulate matter with diameter below 2\.5 um RH 35 |
| `PM25du_RH35_GCC` | ug m\-3 | Dust particulate matter with diameter below 2\.5 um RH 35 |
| `PM25ni_RH35_GCC` | ug m\-3 | Nitrate particulate matter with diameter below 2\.5 um RH 35 |
| `PM25oc_RH35_GCC` | ug m\-3 | Organic carbon particulate matter with diameter below 2\.5 um RH 35 |
| `PM25soa_RH35_GCC` | ug m\-3 | Secondary organic aerosol particulate matter with diameter below 2\.5 um RH 35 |
| `PM25ss_RH35_GCC` | ug m\-3 | Seasalt particulate matter with diameter below 2\.5 um RH 35 |
| `PM25su_RH35_GCC` | ug m\-3 | Sulfate particulate matter with diameter below 2\.5 um RH 35 |
| `PRPE` | Mol fraction | Lumped \>\= C3 alkenes (C3H6, MW \= 42\.08 g mol\-1\) volume mixing ratio dry air |
| `PS` | Pa | Surface pressure |
| `Q` | Mass fraction | Specific humidity |
| `Q10M` | Mass fraction | 10\-meter specific humidity |
| `Q2M` | Mass fraction | 2\-meter specific humidity |
| `RCHO` | Mol fraction | Lumped aldehyde \>\= C3 (CH3CH2CHO, MW \= 58\.00 g mol\-1\) volume mixing ratio dry air |
| `RH` | None | Relative humidity after moist |
| `SALA` | Mol fraction | Fine (0\.01\-0\.05 microns) sea salt aerosol (MW \= 31\.40 g mol\-1\) volume mixing ratio dry air |
| `SALC` | Mol fraction | Coarse (0\.5\-8 microns) sea salt aerosol (MW \= 31\.40 g mol\-1\) volume mixing ratio dry air |
| `SLP` | Pa | Sea level pressure |
| `SO2` | Mol fraction | Sulfur dioxide (SO2, MW \= 64\.00 g mol\-1\) volume mixing ratio dry air |
| `SOAP` | Mol fraction | SOA Precursor \- lumped species for simplified SOA parameterization (MW \= 150\.00 g mol\-1\) volume mixing ratio dry air |
| `SOAS` | Mol fraction | SOA Simple \- simplified non\-volatile SOA parameterization (MW \= 150\.00 g mol\-1\) volume mixing ratio dry air |
| `T` | K | Air temperature |
| `T10M` | K | 10\-meter air temperature |
| `T2M` | K | 2\-meter air temperature |
| `TOLU` | Mol fraction | Toluene (C7H8, MW \= 92\.14 g mol\-1\) volume mixing ratio dry air |
| `TOTCOL_BrO` | 1\.0e15 molec cm\-2 | Bromine monoxide (BrO, MW \= 96\.00 g mol\-1\) total column density |
| `TOTCOL_CO` | 1\.0e15 molec cm\-2 | Carbon monoxide (CO, MW \= 28\.00 g mol\-1\) total column density |
| `TOTCOL_HCHO` | 1\.0e15 molec cm\-2 | Formaldehyde (CH2O, MW \= 30\.00 g mol\-1\) total column density |
| `TOTCOL_IO` | 1\.0e15 molec cm\-2 | Iodine monoxide (IO, MW \= 143\.00 g mol\-1\) total column density |
| `TOTCOL_NO2` | 1\.0e15 molec cm\-2 | Nitrogen dioxide (NO2, MW \= 46\.00 g mol\-1\) total column density |
| `TOTCOL_O3` | Dobson | Ozone (O3, MW \= 48\.00 g mol\-1\) total column density |
| `TOTCOL_SO2` | 1\.0e15 molec cm\-2 | Sulfur dioxide (SO2, MW \= 64\.00 g mol\-1\) total column density |
| `TPREC` | kg/m^2/s | Total precipitation |
| `TROPCOL_BrO` | 1\.0e15 molec cm\-2 | Bromine monoxide (BrO, MW \= 96\.00 g mol\-1\) tropospheric column density |
| `TROPCOL_CO` | 1\.0e15 molec cm\-2 | Carbon monoxide (CO, MW \= 28\.00 g mol\-1\) tropospheric column density |
| `TROPCOL_HCHO` | 1\.0e15 molec cm\-2 | Formaldehyde (CH2O, MW \= 30\.00 g mol\-1\) tropospheric column density |
| `TROPCOL_IO` | 1\.0e15 molec cm\-2 | Iodine monoxide (IO, MW \= 143\.00 g mol\-1\) tropospheric column density |
| `TROPCOL_NO2` | 1\.0e15 molec cm\-2 | Nitrogen dioxide (NO2, MW \= 46\.00 g mol\-1\) tropospheric column density |
| `TROPCOL_O3` | Dobson | Ozone (O3, MW \= 48\.00 g mol\-1\) tropospheric column density |
| `TROPCOL_SO2` | 1\.0e15 molec cm\-2 | Sulfur dioxide (SO2, MW \= 64\.00 g mol\-1\) tropospheric column density |
| `TROPPB` | Pa | Tropopause pressure based on blended estimate |
| `TS` | K | Surface skin temperature |
| `U` | m/s | Eastward wind |
| `U10M` | m/s | 10\-meter eastward wind |
| `U2M` | m/s | 2\-meter eastward wind |
| `V` | m/s | Northward wind |
| `V10M` | m/s | 10\-meter northward wind |
| `V2M` | m/s | 2\-meter northward wind |
| `WETDEPFLX_BCPI` | kg/m^2/s | Hydrophilic black carbon aerosol (MW \= 12\.01 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_BCPO` | kg/m^2/s | Hydrophobic black carbon aerosol (MW \= 12\.01 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_DST1` | kg/m^2/s | Dust aerosol, Reff \= 0\.7 microns (MW \= 29\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_DST2` | kg/m^2/s | Dust aerosol, Reff \= 1\.4 microns (MW \= 29\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_DST3` | kg/m^2/s | Dust aerosol, Reff \= 2\.4 microns (MW \= 29\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_DST4` | kg/m^2/s | Dust aerosol, Reff \= 4\.5 microns (MW \= 29\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_HCHO` | kg/m^2/s | Formaldehyde (CH2O, MW \= 30\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_HNO3` | kg/m^2/s | Nitric acid (HNO3, MW \= 63\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_NH3` | kg/m^2/s | Ammonia (NH3, MW \= 17\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_NH4` | kg/m^2/s | Ammonium (NH4, MW \= 18\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_NIT` | kg/m^2/s | Inorganic nitrates (MW \= 62\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_OCPI` | kg/m^2/s | Hydrophilic organic carbon aerosol (MW \= 12\.01 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_OCPO` | kg/m^2/s | Hydrophobic organic carbon aerosol (MW \= 12\.01 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_SALA` | kg/m^2/s | Fine (0\.01\-0\.05 microns) sea salt aerosol (MW \= 31\.40 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_SALC` | kg/m^2/s | Coarse (0\.5\-8 microns) sea salt aerosol (MW \= 31\.40 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_SO2` | kg/m^2/s | Sulfur dioxide (SO2, MW \= 64\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `WETDEPFLX_SO4` | kg/m^2/s | Sulfate (SO4, MW \= 96\.00 g mol\-1\) vertical integrated loss due to wet scavenging |
| `XYLE` | Mol fraction | Xylene (C8H10, MW \= 106\.16 g mol\-1\) volume mixing ratio dry air |
| `ZL` | m | Mid layer heights |
| `ZPBL` | m | Planetary boundary layer height |




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

vargeosCf=ee.ImageCollection('NASA/GEOS-CF/v1/fcst/tavg1hr');

Map.setCenter(100,20,3);

varweeklyT=
geosCf.select('T').filterDate('2022-11-01','2022-11-08').median();
Map.addLayer(weeklyT,imageVisParamT,'Weekly T',false,1);

varNO2=ee.Image('NASA/GEOS-CF/v1/fcst/tavg1hr/20220921_12z-20220921_1230z');
Map.addLayer(NO2,imageVisParamNO2,'NO2',true,1);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GEOS-CF_v1_fcst_tavg1hr)


[GEOS\-CF fcst tavg1hr v1: Goddard Earth Observing System Composition Forecast](/earth-engine/datasets/catalog/NASA_GEOS-CF_v1_fcst_tavg1hr)

This dataset contains meteorological forecast (fcst) of time\-averaged frequency data (tavg1hr). Use the 'creation\_time' and 'forecast\_time' properties to select data of interest. The Goddard Earth Observing System Composition Forecast (GEOS\-CF) system is a high\-resolution (0\.25°) global constituent prediction system from NASA's Global Modeling and Assimilation Office(GMAO). GEOS\-CF offers a new …

 NASA/GEOS\-CF/v1/fcst/tavg1hr,
 atmosphere,composition,forecast,geos,gmao,nasa

2022\-10\-01T00:00:00Z/2025\-07\-15T12:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1029/2020MS002413](https://doi.org/https://gmao.gsfc.nasa.gov/weather_prediction/GEOS-CF/)
* [https://doi.org/10\.1029/2020MS002413](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_GEOS-CF_v1_fcst_tavg1hr)









