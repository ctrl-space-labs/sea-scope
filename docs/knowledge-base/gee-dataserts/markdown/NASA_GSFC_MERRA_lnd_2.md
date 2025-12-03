



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MERRA\-2 M2T1NXLND: Land Surface Diagnostics V5\.12\.4


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================








Dataset Availability
1980\-01\-01T00:00:00Z–2025\-06\-01T23:00:00Z
Dataset Provider


[NASA/MERRA](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GSFC/MERRA/lnd/2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_lnd_2)





Cadence
1 Hour
Tags


[climate](/earth-engine/datasets/tags/climate)
[cryosphere](/earth-engine/datasets/tags/cryosphere)
[evaporation](/earth-engine/datasets/tags/evaporation)
[ice](/earth-engine/datasets/tags/ice)
[merra](/earth-engine/datasets/tags/merra)
[precipitation](/earth-engine/datasets/tags/precipitation)
[soil](/earth-engine/datasets/tags/soil)
[temperature](/earth-engine/datasets/tags/temperature)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)








#### Description



M2T1NXLND (or tavg1\_2d\_lnd\_Nx) is an hourly time\-averaged data
collection in Modern\-Era Retrospective analysis for Research and
Applications version 2 (MERRA\-2\). This collection consists of land
surface diagnostics, such a baseflow flux, runoff, surface soil wetness,
root zone soil wetness, water at surface layer, water at root zone
layer, and soil temperature at six layers. The data field is
time\-stamped with the central time of an hour starting from 00:30 UTC,
e.g.: 00:30, 01:30, ... , 23:30 UTC.


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
| `BASEFLOW` | kg/m^2/s | 0\* | 0\.000129\* | Baseflow flux |
| `ECHANGE` | W/m^2 | \-2930\.42\* | 689\.084\* | Rate of change of total land energy |
| `EVLAND` | kg/m^2/s | \-0\.00011\* | 0\.000682\* | Evaporation land |
| `EVPINTR` | W/m^2 | \-55\.2571\* | 582\.82\* | Interception loss energy flux |
| `EVPSBLN` | W/m^2 | \-310\.134\* | 729\.17\* | Snow ice evaporation energy flux |
| `EVPSOIL` | W/m^2 | \-0\.588216\* | 1217\.36\* | Baresoil evaporation energy flux |
| `EVPTRNS` | W/m^2 | \-0\.882528\* | 1635\.84\* | Transpiration energy flux |
| `FRSAT` | None | 0\* | 0\.983076\* | Fractional area of saturated zone |
| `FRSNO` | None | 0\* | 1\* | Fractional area of land snowcover |
| `FRUNST` | None | 0\* | 0\.999996\* | Fractional area of unsaturated zone |
| `FRWLT` | None | 0\* | 1\* | Fractional area of wilting zone |
| `GHLAND` | W/m^2 | \-245\.165\* | 304\.675\* | Ground heating land |
| `GRN` | None | 0\* | 0\.990087\* | Greeness fraction |
| `GWETPROF` | None | 0\.086402\* | 0\.99997\* | Average prof soil moisture |
| `GWETROOT` | None | 0\.085486\* | 1\* | Root zone soil wetness |
| `GWETTOP` | None | 0\.010069\* | 1\* | Surface soil wetness |
| `LAI` | None | 0\* | 8\.07408\* | Leaf area index |
| `LHLAND` | W/m^2 | \-308\.962\* | 1682\.57\* | Latent heat flux land |
| `LWLAND` | W/m^2 | \-318\.505\* | 47\.5398\* | Net longwave land |
| `PARDFLAND` | W/m^2 | 0\* | 277\.006\* | Surface downwelling photosynthetic active radiation diffuse flux |
| `PARDRLAND` | W/m^2 | 0\* | 441\.662\* | Surface downwelling par beam flux |
| `PRECSNOLAND` | kg/m^2/s | 0\* | 0\.008119\* | Snowfall land |
| `PRECTOTLAND` | kg/m^2/s | 0\* | 0\.110576\* | Total precipitation land |
| `PRMC` | Volume fraction | 0\.032228\* | 0\.476084\* | Water profile |
| `QINFIL` | kg/m^2/s | 0\* | 0\.012518\* | Soil water infiltration rate |
| `RUNOFF` | kg/m^2/s | 0\* | 0\.104504\* | Overland runoff including throughflow |
| `RZMC` | Volume fraction | 0\.031886\* | 0\.478268\* | Water root zone |
| `SFMC` | Volume fraction | 0\.003945\* | 0\.478\* | Water surface layer |
| `SHLAND` | W/m^2 | \-1189\.34\* | 768\.706\* | Sensible heat flux land |
| `SMLAND` | kg/m^2/s | 0\* | 0\.007922\* | Snowmelt flux land |
| `SNODP` | m | 0\* | 9\.30012\* | Snow depth |
| `SNOMAS` | kg/m^2 | 0\* | 3964\.6\* | Total snow storage land |
| `SPLAND` | W/m^2 | \-71\.822\* | 754\.467\* | Rate of spurious land energy source |
| `SPSNOW` | W/m^2 | \-1287\.32\* | 127\.015\* | Rate of spurious snow energy |
| `SPWATR` | kg/m^2/s | \-0\.000305\* | 2e\-06\* | Rate of spurious land water source |
| `SWLAND` | W/m^2 | 0\* | 1076\.59\* | Net shortwave land |
| `TELAND` | J/m^2 | \-2\.06745e\+09\* | 1\.09445e\+09\* | Total energy storage land |
| `TPSNOW` | K | 207\.984\* | 273\.16\* | Surface temperature of snow |
| `TSAT` | K | 231\.971\* | 319\.16\* | Surface temperature of saturated zone |
| `TSOIL1` | K | 235\.694\* | 326\.169\* | Soil temperatures layer 1 |
| `TSOIL2` | K | 236\.821\* | 317\.313\* | Soil temperatures layer 2 |
| `TSOIL3` | K | 238\.6\* | 314\.921\* | Soil temperatures layer 3 |
| `TSOIL4` | K | 241\.158\* | 313\.186\* | Soil temperatures layer 4 |
| `TSOIL5` | K | 244\.4\* | 311\.295\* | Soil temperatures layer 5 |
| `TSOIL6` | K | 249\.436\* | 309\.734\* | Soil temperatures layer 6 |
| `TSURF` | K | 207\.984\* | 341\.939\* | Surface temperature of land incl snow |
| `TUNST` | K | 231\.303\* | 341\.938\* | Surface temperature of unsaturated zone |
| `TWLAND` | kg/m^2 | 42\.9657\* | 4430\.25\* | Available water storage land |
| `TWLT` | K | 231\.303\* | 341\.939\* | Surface temperature of wilted zone |
| `WCHANGE` | kg/m^2/s | \-0\.001769\* | 0\.012293\* | Rate of change of total land water |


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
vardataset=ee.ImageCollection('NASA/GSFC/MERRA/lnd/2')
.filter(ee.Filter.date('2022-02-01','2022-02-02'));
varbaseflow_flux=dataset.select('BASEFLOW');
varbfVis={
min:-0.00000913,
max:0.00001076,
palette:['001137','01abab','e7eb05','620500']
};
Map.setCenter(-95,39,2);
Map.addLayer(baseflow_flux,bfVis,'Baseflow flux');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GSFC_MERRA_lnd_2)


[MERRA\-2 M2T1NXLND: Land Surface Diagnostics V5\.12\.4](/earth-engine/datasets/catalog/NASA_GSFC_MERRA_lnd_2)

M2T1NXLND (or tavg1\_2d\_lnd\_Nx) is an hourly time\-averaged data collection in Modern\-Era Retrospective analysis for Research and Applications version 2 (MERRA\-2\). This collection consists of land surface diagnostics, such a baseflow flux, runoff, surface soil wetness, root zone soil wetness, water at surface layer, water at root zone layer, and soil …

 NASA/GSFC/MERRA/lnd/2,
 climate,cryosphere,evaporation,ice,merra,precipitation,soil,temperature,water\-vapor

1980\-01\-01T00:00:00Z/2025\-06\-01T23:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








