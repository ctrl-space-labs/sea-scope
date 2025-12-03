



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MERRA\-2 M2T1NXSLV: Single\-Level Diagnostics V5\.12\.4


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================================








Dataset Availability
1980\-01\-01T00:00:00Z–2025\-06\-01T23:00:00Z
Dataset Provider


[NASA/MERRA](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GSFC/MERRA/slv/2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_slv_2)





Cadence
1 Hour
Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[humidity](/earth-engine/datasets/tags/humidity)
[merra](/earth-engine/datasets/tags/merra)
[nasa](/earth-engine/datasets/tags/nasa)
[pressure](/earth-engine/datasets/tags/pressure)
[temperature](/earth-engine/datasets/tags/temperature)
[vapor](/earth-engine/datasets/tags/vapor)
[water](/earth-engine/datasets/tags/water)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)
[wind](/earth-engine/datasets/tags/wind)
condensation
omega
slv








#### Description



M2T1NXSLV (or tavg1\_2d\_slv\_Nx) is an hourly time\-averaged 2\-dimensional data
collection in Modern\-Era Retrospective analysis for Research and
Applications version 2 (MERRA\-2\). This collection consists of meteorology
diagnostics at popularly used vertical levels, such as air temperature at
2\-meter (or at 10\-meter, 850hPa, 500 hPa, 250hPa), wind components at
50\-meter (or at 2\-meter, 10\-meter, 850 hPa, 500hPa, 250 hPa), sea level
pressure, surface pressure, and total precipitable water vapor (or ice
water, liquid water). The data field is time\-stamped with the central time
of an hour starting from 00:30 UTC, e.g.: 00:30, 01:30, ... , 23:30 UTC.


MERRA\-2 is the latest version of global atmospheric reanalysis for
the satellite era produced by NASA Global Modeling and Assimilation
Office (GMAO) using the Goddard Earth Observing System Model (GEOS)
version 5\.12\.4\. The dataset covers the period of 1980\-present with the
latency of \~3 weeks after the end of a month.





### Bands



**Pixel Size**
  
69375 meters




**Y Pixel Size**
  
55000 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `CLDPRS` | Pa | Cloud top pressure |
| `CLDTMP` | K | Cloud top temperature |
| `DISPH` | m | Zero plane displacement height |
| `H1000` | m | Height at 1000 mb |
| `H250` | m | Height at 250 hPa |
| `H500` | m | Height at 500 hPa |
| `H850` | m | Height at 850 hPa |
| `OMEGA500` | Pa/s | Omega at 500 hPa |
| `PBLTOP` | Pa | Pbltop pressure |
| `PS` | Pa | Surface pressure |
| `Q250` | Mass fraction | Specific humidity at 250 hPa |
| `Q500` | Mass fraction | Specific humidity at 500 hPa |
| `Q850` | Mass fraction | Specific humidity at 850 hPa |
| `QV10M` | Mass fraction | 10\-meter specific humidity |
| `QV2M` | Mass fraction | 2\-meter specific humidity |
| `SLP` | Pa | Sea level pressure |
| `T10M` | K | 10\-meter air temperature |
| `T250` | K | Air temperature at 250 hPa |
| `T2MDEW` | K | Dew point temperature at 2 m |
| `T2MWET` | K | Wet bulb temperature at 2 m |
| `T2M` | K | 2\-meter air temperature |
| `T500` | K | Air temperature at 500 hPa |
| `T850` | K | Air temperature at 850 hPa |
| `TO3` | Dobson | Total column ozone |
| `TOX` | kg/m^2 | Total column odd oxygen |
| `TQI` | kg/m^2 | Total precipitable ice water |
| `TQL` | kg/m^2 | Total precipitable liquid water |
| `TQV` | kg/m^2 | Total precipitable water vapor |
| `TROPPB` | Pa | Tropopause pressure (TROPP) based on blended estimate |
| `TROPPT` | Pa | Tropopause pressure based on thermal estimate |
| `TROPPV` | Pa | Tropopause pressure based on epv estimate |
| `TROPQ` | Mass fraction | Tropopause specific humidity using blended tropp (TROPPB) estimate |
| `TROPT` | K | Tropopause temperature using blended tropp estimate |
| `TS` | K | Surface skin temperature |
| `U10M` | m/s | 10\-meter eastward wind |
| `U250` | m/s | Eastward wind at 250 hPa |
| `U2M` | m/s | 2\-meter eastward wind |
| `U500` | m/s | Eastward wind at 500 hPa |
| `U50M` | m/s | Eastward wind at 50 meters |
| `U850` | m/s | Eastward wind at 850 hPa |
| `V10M` | m/s | 10\-meter northward wind |
| `V250` | m/s | Northward wind at 250 hPa |
| `V2M` | m/s | 2\-meter northward wind |
| `V500` | m/s | Northward wind at 500 hPa |
| `V50M` | m/s | Northward wind at 50 meters |
| `V850` | m/s | Northward wind at 850 hPa |
| `ZLCL` | m | Lifting condensation level |




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
vardataset=ee.ImageCollection('NASA/GSFC/MERRA/slv/2')
.filter(ee.Filter.date('2022-02-01','2022-02-02'));
varsurface_pressure=dataset.select('PS');
varsurface_pressure_vis={
min:81100,
max:117000,
palette:['001137','01abab','e7eb05','620500']
};
Map.setCenter(-95.62,39.91,2);
Map.addLayer(surface_pressure,surface_pressure_vis);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_slv_2)


[MERRA\-2 M2T1NXSLV: Single\-Level Diagnostics V5\.12\.4](/earth-engine/datasets/catalog/NASA_GSFC_MERRA_slv_2)

M2T1NXSLV (or tavg1\_2d\_slv\_Nx) is an hourly time\-averaged 2\-dimensional data collection in Modern\-Era Retrospective analysis for Research and Applications version 2 (MERRA\-2\). This collection consists of meteorology diagnostics at popularly used vertical levels, such as air temperature at 2\-meter (or at 10\-meter, 850hPa, 500 hPa, 250hPa), wind components at 50\-meter (or …

 NASA/GSFC/MERRA/slv/2,
 atmosphere,climate,humidity,merra,nasa,pressure,temperature,vapor,water,water\-vapor,wind

1980\-01\-01T00:00:00Z/2025\-06\-01T23:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








