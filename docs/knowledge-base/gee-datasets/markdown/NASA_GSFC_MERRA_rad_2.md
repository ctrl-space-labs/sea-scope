



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MERRA\-2 M2T1NXRAD: Radiation Diagnostics V5\.12\.4


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================








Dataset Availability
1980\-01\-01T00:00:00Z–2025\-06\-01T23:00:00Z
Dataset Provider


[NASA/MERRA](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GSFC/MERRA/rad/2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_rad_2)





Cadence
1 Hour
Tags


[albedo](/earth-engine/datasets/tags/albedo)
[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[emissivity](/earth-engine/datasets/tags/emissivity)
[merra](/earth-engine/datasets/tags/merra)
[shortwave](/earth-engine/datasets/tags/shortwave)
[temperature](/earth-engine/datasets/tags/temperature)








#### Description



M2T1NXRAD (or tavg1\_2d\_rad\_Nx) is an hourly time\-averaged data
collection in Modern\-Era Retrospective analysis for Research and
Applications version 2 (MERRA\-2\). This collection consists of radiation
diagnostics, such as surface albedo, cloud area fraction, in cloud
optical thickness, surface incoming shortwave flux (i.e. solar
radiation), surface net downward shortwave flux, and upwelling longwave
flux at TOA (top of atmosphere) (i.e. outgoing longwave radiation (OLR)
at TOA). The data field is time\-stamped with the central time of an hour
starting from 00:30 UTC, e.g.: 00:30, 01:30, ... , 23:30 UTC.


MERRA\-2 is the latest version of global atmospheric reanalysis for the
satellite era produced by NASA Global Modeling and Assimilation Office
(GMAO) using the Goddard Earth Observing System Model (GEOS) version
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
| `ALBEDO` | None | 0\.01\* | 0\.898471\* | Surface albedo |
| `ALBNIRDF` | None | 0\.017455\* | 0\.820016\* | Surface albedo for near infrared diffuse |
| `ALBNIRDR` | None | 0\.018709\* | 0\.82001\* | Surface albedo for near infrared beam |
| `ALBVISDF` | None | 0\.016788\* | 0\.959771\* | Surface albedo for visible diffuse |
| `ALBVISDR` | None | 0\.01853\* | 0\.959762\* | Surface albedo for visible beam |
| `CLDHGH` | None | 0\* | 0\.999236\* | Cloud area fraction for high clouds |
| `CLDLOW` | None | 0\* | 0\.999997\* | Cloud area fraction for low clouds |
| `CLDMID` | None | 0\* | 0\.998779\* | Cloud area fraction for middle clouds |
| `CLDTOT` | None | 0\* | 1\* | Total cloud area fraction |
| `EMIS` | None | 0\.943074\* | 0\.999993\* | Surface emissivity |
| `LWGABCLRCLN` | W/m^2 | 41\.1408\* | 458\.523\* | Surface absorbed longwave radiation assuming clear sky and no aerosol |
| `LWGABCLR` | W/m^2 | 41\.1414\* | 465\.929\* | Surface absorbed longwave radiation assuming clear sky |
| `LWGAB` | W/m^2 | 41\.1446\* | 482\.398\* | Surface absorbed longwave radiation |
| `LWGEM` | W/m^2 | 67\.5297\* | 630\.29\* | Longwave flux emitted from surface |
| `LWGNTCLRCLN` | W/m^2 | \-248\.748\* | 61\.0736\* | Surface net downward longwave flux assuming clear sky and no aerosol |
| `LWGNTCLR` | W/m^2 | \-248\.653\* | 62\.2794\* | Surface net downward longwave flux assuming clear sky |
| `LWGNT` | W/m^2 | \-268\.862\* | 77\.255\* | Surface net downward longwave flux |
| `LWTUPCLRCLN` | W/m^2 | 80\.6768\* | 372\.229\* | Upwelling longwave flux at TOA assuming clear sky and no aerosol |
| `LWTUPCLR` | W/m^2 | 80\.6768\* | 372\.229\* | Upwelling longwave flux at TOA assuming clear sky |
| `LWTUP` | W/m^2 | 80\.6506\* | 370\.868\* | Upwelling longwave flux at TOA |
| `SWGDNCLR` | W/m^2 | \-0\.008217\* | 1155\.5\* | Surface incoming shortwave flux assuming clear sky |
| `SWGDN` | W/m^2 | 0\* | 1127\.49\* | Surface incoming shortwave flux |
| `SWGNTCLN` | W/m^2 | 0\* | 1088\.42\* | Surface net downward shortwave flux assuming no aerosol |
| `SWGNTCLRCLN` | W/m^2 | \-3\.2e\-05\* | 1088\.42\* | Surface net downward shortwave flux assuming clear sky and no aerosol |
| `SWGNTCLR` | W/m^2 | \-0\.001333\* | 1083\.95\* | Surface net downward shortwave flux assuming clear sky |
| `SWGNT` | W/m^2 | 0\* | 1083\.95\* | Surface net downward shortwave flux |
| `SWTDN` | W/m^2 | 0\* | 1404\.28\* | TOA incoming shortwave flux |
| `SWTNTCLN` | W/m^2 | 0\* | 1315\.89\* | TOA net downward shortwave flux assuming no aerosol |
| `SWTNTCLRCLN` | W/m^2 | 0\* | 1317\.5\* | TOA net downward shortwave flux assuming clear sky and no aerosol |
| `SWTNTCLR` | W/m^2 | 0\* | 1316\.5\* | TOA net downward shortwave flux assuming clear sky |
| `SWTNT` | W/m^2 | 0\* | 1313\.33\* | TOA net downward shortwave flux |
| `TAUHGH` | None | 0\* | 142\.188\* | In cloud optical thickness of high clouds(export) |
| `TAULOW` | None | 0\* | 318\.218\* | In cloud optical thickness of low clouds |
| `TAUMID` | None | 0\* | 252\.995\* | In cloud optical thickness of middle clouds |
| `TAUTOT` | None | 0\* | 348\.125\* | In cloud optical thickness of all clouds |
| `TS` | K | 185\.73\* | 328\.864\* | Surface skin temperature |


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
vardataset=ee.ImageCollection('NASA/GSFC/MERRA/rad/2')
.filter(ee.Filter.date('2022-02-01','2022-02-02')).first();
varsurface_albedo=dataset.select('ALBEDO');
varsaVis={
min:-0.428147,
max:0.833350,
palette:['001137','01abab','e7eb05','620500']
};
Map.setCenter(-95,39,2);
Map.addLayer(surface_albedo,saVis,'Surface albedo');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_rad_2)


[MERRA\-2 M2T1NXRAD: Radiation Diagnostics V5\.12\.4](/earth-engine/datasets/catalog/NASA_GSFC_MERRA_rad_2)

M2T1NXRAD (or tavg1\_2d\_rad\_Nx) is an hourly time\-averaged data collection in Modern\-Era Retrospective analysis for Research and Applications version 2 (MERRA\-2\). This collection consists of radiation diagnostics, such as surface albedo, cloud area fraction, in cloud optical thickness, surface incoming shortwave flux (i.e. solar radiation), surface net downward shortwave flux, and …

 NASA/GSFC/MERRA/rad/2,
 albedo,atmosphere,climate,emissivity,merra,shortwave,temperature

1980\-01\-01T00:00:00Z/2025\-06\-01T23:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








