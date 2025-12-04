



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

AG100: ASTER Global Emissivity Dataset 100\-meter V003


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2008\-12\-31T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/COMMUNITY/ASTER_GED/AG100.003)



Earth Engine Snippet


`ee.Image("NASA/ASTER_GED/AG100_003")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_ASTER_GED_AG100_003)





Tags


[aster](/earth-engine/datasets/tags/aster)
[elevation](/earth-engine/datasets/tags/elevation)
[emissivity](/earth-engine/datasets/tags/emissivity)
[geophysical](/earth-engine/datasets/tags/geophysical)
[infrared](/earth-engine/datasets/tags/infrared)
[jpl](/earth-engine/datasets/tags/jpl)
[lst](/earth-engine/datasets/tags/lst)
[nasa](/earth-engine/datasets/tags/nasa)
[ndvi](/earth-engine/datasets/tags/ndvi)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[temperature](/earth-engine/datasets/tags/temperature)
[thermal](/earth-engine/datasets/tags/thermal)
caltech
ged








#### Description



The Advanced Spaceborne Thermal Emission and Reflection Radiometer Global
Emissivity Database (ASTER\-GED) was developed by the National Aeronautics
and Space Administration's (NASA) Jet Propulsion Laboratory (JPL),
California Institute of Technology. This product includes the mean
emissivity and standard deviation for all 5 ASTER Thermal Infrared bands,
mean land surface temperature (LST) and standard deviation, a re\-sampled
ASTER GDEM, land\-water mask, mean Normalized Difference Vegetation Index
(NDVI) and standard deviation, and observation count.


ASTER\-GED land surface temperature and emissivity (LST\&E) are generated
using the ASTER Temperature Emissivity Separation (TES) algorithm in
combination with a Water Vapor Scaling (WVS) atmospheric correction method
using MODIS MOD07 atmospheric profiles and the MODTRAN 5\.2 radiative
transfer model.


This product was derived from clear\-sky pixels for all available ASTER data
(2000\-2008\).


[User's Guide](https://lpdaac.usgs.gov/documents/120/ASTERGED_User_Guide_V3.pdf)





### Bands



**Pixel Size**
  
100 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `emissivity_band10` | None | 0 | 1000 | 0\.001 | Mean band 10 |
| `emissivity_band11` | None | 0 | 1000 | 0\.001 | Mean band 11 |
| `emissivity_band12` | None | 0 | 1000 | 0\.001 | Mean band 12 |
| `emissivity_band13` | None | 0 | 1000 | 0\.001 | Mean band 13 |
| `emissivity_band14` | None | 0 | 1000 | 0\.001 | Mean band 14 |
| `emissivity_sdev_band10` | None | \-1000 | 1000 | 0\.0001 | Standard deviation band 10 |
| `emissivity_sdev_band11` | None | \-1000 | 1000 | 0\.0001 | Standard deviation band 11 |
| `emissivity_sdev_band12` | None | \-1000 | 1000 | 0\.0001 | Standard deviation band 12 |
| `emissivity_sdev_band13` | None | \-1000 | 1000 | 0\.0001 | Standard deviation band 13 |
| `emissivity_sdev_band14` | None | \-1000 | 1000 | 0\.0001 | Standard deviation band 14 |
| `temperature` | K | 0 | 65535 | 0\.01 | Temperature mean |
| `temperature_sdev` | K | 0 | 65535 | 0\.01 | Temperature standard deviation |
| `ndvi` | None | 0 | 100 | 0\.01 | NDVI mean |
| `ndvi_sdev` | None | 0 | 100 | 0\.01 | NDVI standard deviation |
| `elevation` | m | \-500 | 9000 |  | ASTER Global Digital Elevation Model V002 |
| `land_water_map` | None |  | Land water map |
| `num_obs` | Number per pixel | 0\* | 120\* |  | Number of observations |


 \* estimated min or max value
**land\_water\_map Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | brown | Land |
| 2 | blue | Water |




### Terms of Use


**Terms of Use**


ASTER data and products distributed by the LP DAAC, with the exception of
the ASTER Global Digital Elevation Model (GDEM) dataset (ASTGTM) version 2
(v2\), have no restrictions on data use, sale, or subsequent redistribution.
For more information visit the
[ASTER Policies](https://lpdaac.usgs.gov/data/data-citation-and-policies/) site.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/COMMUNITY/ASTER\_GED/AG100\.003](https://doi.org/10.5067/COMMUNITY/ASTER_GED/AG100.003)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('NASA/ASTER_GED/AG100_003');
varelevation=dataset.select('elevation');
varelevationVis={
min:-15.0,
max:5000.0,
palette:[
'0602ff','235cb1','307ef3','269db1','30c8e2','32d3ef','3ae237',
'b5e22e','d6e21f','fff705','ffd611','ffb613','ff8b13','ff6e08',
'ff500d','ff0000','de0101','c21301'
],
};
Map.setCenter(89.12,37.72,3);
Map.addLayer(elevation,elevationVis,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_ASTER_GED_AG100_003)


[AG100: ASTER Global Emissivity Dataset 100\-meter V003](/earth-engine/datasets/catalog/NASA_ASTER_GED_AG100_003)

The Advanced Spaceborne Thermal Emission and Reflection Radiometer Global Emissivity Database (ASTER\-GED) was developed by the National Aeronautics and Space Administration's (NASA) Jet Propulsion Laboratory (JPL), California Institute of Technology. This product includes the mean emissivity and standard deviation for all 5 ASTER Thermal Infrared bands, mean land surface temperature …

 NASA/ASTER\_GED/AG100\_003,
 aster,elevation,emissivity,geophysical,infrared,jpl,lst,nasa,ndvi,satellite\-imagery,temperature,thermal

2000\-01\-01T00:00:00Z/2008\-12\-31T00:00:00Z



 \-59 \-180 80 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/COMMUNITY/ASTER\_GED/AG100\.003](https://doi.org/https://doi.org/10.5067/COMMUNITY/ASTER_GED/AG100.003)
* [https://doi.org/10\.5067/COMMUNITY/ASTER\_GED/AG100\.003](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_ASTER_GED_AG100_003)









