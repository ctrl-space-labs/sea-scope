



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MERRA\-2 M2T1NXAER: Aerosol Diagnostics V5\.12\.4


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================








Dataset Availability
1980\-01\-01T00:00:00Z–2025\-06\-01T23:00:00Z
Dataset Provider


[NASA/MERRA](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GSFC/MERRA/aer/2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_aer_2)





Cadence
1 Hour
Tags


[aerosol](/earth-engine/datasets/tags/aerosol)
[atmosphere](/earth-engine/datasets/tags/atmosphere)
[carbon](/earth-engine/datasets/tags/carbon)
[dust](/earth-engine/datasets/tags/dust)
[mass](/earth-engine/datasets/tags/mass)
[merra](/earth-engine/datasets/tags/merra)
[nasa](/earth-engine/datasets/tags/nasa)
[sea\-salt](/earth-engine/datasets/tags/sea-salt)
[so2](/earth-engine/datasets/tags/so2)
[so4](/earth-engine/datasets/tags/so4)








#### Description



M2T1NXAER (or tavg1\_2d\_aer\_Nx) is an hourly time\-averaged 2\-dimensional data
collection in Modern\-Era Retrospective analysis for Research and
Applications version 2 (MERRA\-2\). This collection consists of assimilated
aerosol diagnostics, such as column mass density of aerosol components
(black carbon, dust, sea\-salt, sulfate, and organic carbon), surface mass
concentration of aerosol components, and total extinction (and scattering)
aerosol optical thickness (AOT) at 550 nm. The total PM1\.0, PM2\.5, and PM10
may be derived with the formula described in the
[in the FAQ](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/FAQ/)


The data field is time\-stamped with the
central time of an hour starting from 00:30 UTC,
e.g.: 00:30, 01:30, ... , 23:30 UTC.


MERRA\-2 is the latest version of global atmospheric reanalysis for the
satellite era produced by NASA Global Modeling and Assimilation Office
(GMAO) using the Goddard Earth Observing System Model (GEOS) version 5\.12\.4\.
The dataset covers the period of 1980\-present with the latency of \~3 weeks
after the end of a month.





### Bands



**Pixel Size**
  
69375 meters




**Y Pixel Size**
  
55000 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `BCANGSTR` | None | Black carbon angstrom parameter \[470\-870 nm] |
| `BCCMASS` | kg/m^2 | Black carbon column mass density |
| `BCEXTTAU` | None | Black carbon extinction AOT \[550 nm] |
| `BCFLUXU` | kg/m/s | Black carbon column u\-wind mass flux |
| `BCFLUXV` | kg/m/s | Black carbon column v\-wind mass flux |
| `BCSCATAU` | None | Black carbon scattering AOT \[550 nm] |
| `BCSMASS` | kg/m^3 | Black carbon surface mass concentration |
| `DMSCMASS` | kg/m^2 | Dms column mass density |
| `DMSSMASS` | kg/m^3 | Dms surface mass concentration |
| `DUANGSTR` | None | Dust angstrom parameter \[470\-870 nm] |
| `DUCMASS25` | kg/m^2 | Dust column mass density \- PM2\.5 |
| `DUCMASS` | kg/m^2 | Dust column mass density |
| `DUEXTT25` | None | Dust extinction AOT \[550 nm] \- PM2\.5 |
| `DUEXTTAU` | None | Dust extinction AOT \[550 nm] |
| `DUFLUXU` | kg/m/s | Dust column u\-wind mass flux |
| `DUFLUXV` | kg/m/s | Dust column v\-wind mass flux |
| `DUSCAT25` | None | Dust scattering AOT \[550 nm] \- PM2\.5 |
| `DUSCATAU` | None | Dust scattering AOT \[550 nm] |
| `DUSMASS25` | kg/m^3 | Dust surface mass concentration \- PM2\.5 |
| `DUSMASS` | kg/m^3 | Dust surface mass concentration |
| `OCANGSTR` | None | Organic carbon angstrom parameter \[470\-870 nm] |
| `OCCMASS` | kg/m^2 | Organic carbon column mass density |
| `OCEXTTAU` | None | Organic carbon extinction AOT \[550 nm] |
| `OCFLUXU` | kg/m/s | Organic carbon column u\-wind mass flux |
| `OCFLUXV` | kg/m/s | Organic carbon column v\-wind mass flux |
| `OCSCATAU` | None | Organic carbon scattering AOT \[550 nm] |
| `OCSMASS` | kg/m^3 | Organic carbon surface mass concentration |
| `SO2CMASS` | kg/m^2 | So2 column mass density |
| `SO2SMASS` | kg/m^3 | So2 surface mass concentration |
| `SO4CMASS` | kg/m^2 | SO4 column mass density |
| `SO4SMASS` | kg/m^3 | SO4 surface mass concentration |
| `SSANGSTR` | None | Sea salt angstrom parameter \[470\-870 nm] |
| `SSCMASS25` | kg/m^2 | Sea salt column mass density \- PM2\.5 |
| `SSCMASS` | kg/m^2 | Sea salt column mass density |
| `SSEXTT25` | None | Sea salt extinction AOT \[550 nm] \- PM2\.5 |
| `SSEXTTAU` | None | Sea salt extinction AOT \[550 nm] |
| `SSFLUXU` | kg/m/s | Sea salt column u\-wind mass flux |
| `SSFLUXV` | kg/m/s | Sea salt column v\-wind mass flux |
| `SSSCAT25` | None | Sea salt scattering AOT \[550 nm] \- PM2\.5 |
| `SSSCATAU` | None | Sea salt scattering AOT \[550 nm] |
| `SSSMASS25` | kg/m^3 | Sea salt surface mass concentration \- PM2\.5 |
| `SSSMASS` | kg/m^3 | Sea salt surface mass concentration |
| `SUANGSTR` | None | SO4 angstrom parameter \[470\-870 nm] |
| `SUEXTTAU` | None | SO4 extinction AOT \[550 nm] |
| `SUFLUXU` | kg/m/s | SO4 column u\-wind mass flux |
| `SUFLUXV` | kg/m/s | SO4 column v\-wind mass flux |
| `SUSCATAU` | None | SO4 scattering AOT \[550 nm] |
| `TOTANGSTR` | None | Total aerosol angstrom parameter \[470\-870 nm] |
| `TOTEXTTAU` | None | Total aerosol extinction AOT \[550 nm] |
| `TOTSCATAU` | None | Total aerosol scattering AOT \[550 nm] |




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
vardataset=ee.ImageCollection('NASA/GSFC/MERRA/aer/2')
.filter(ee.Filter.date('2022-02-01','2022-02-02'));
varblack_carbon_column_u_wind_mass_flux=dataset.select('BCFLUXU');
varbccVis={
min:-0.0000116,
max:0.0000165,
palette:['001137','01abab','e7eb05','620500']
};
Map.setCenter(-95.62,39.91,2);
Map.addLayer(black_carbon_column_u_wind_mass_flux,bccVis);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_aer_2)


[MERRA\-2 M2T1NXAER: Aerosol Diagnostics V5\.12\.4](/earth-engine/datasets/catalog/NASA_GSFC_MERRA_aer_2)

M2T1NXAER (or tavg1\_2d\_aer\_Nx) is an hourly time\-averaged 2\-dimensional data collection in Modern\-Era Retrospective analysis for Research and Applications version 2 (MERRA\-2\). This collection consists of assimilated aerosol diagnostics, such as column mass density of aerosol components (black carbon, dust, sea\-salt, sulfate, and organic carbon), surface mass concentration of aerosol components, …

 NASA/GSFC/MERRA/aer/2,
 aerosol,atmosphere,carbon,dust,mass,merra,nasa,sea\-salt,so2,so4

1980\-01\-01T00:00:00Z/2025\-06\-01T23:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








