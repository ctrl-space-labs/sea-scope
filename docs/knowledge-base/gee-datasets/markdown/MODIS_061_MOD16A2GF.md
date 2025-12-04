



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD16A2GF.061: Terra Net Evapotranspiration Gap\-Filled 8\-Day Global 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2024\-12\-26T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MOD16A2GF.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MOD16A2GF")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD16A2GF)





Cadence
8 Days
Tags


[8\-day](/earth-engine/datasets/tags/8-day)
[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)








#### Description



The Terra Moderate Resolution Imaging Spectroradiometer (MODIS) MOD16A2GF
Version 6\.1 Evapotranspiration/Latent Heat Flux (ET/LE) product is a
year\-end gap\-filled 8\-day composite dataset produced at 500 meter (m) pixel
resolution. The algorithm used for the MOD16 data product collection is
based on the logic of the Penman\-Monteith equation, which includes inputs of
daily meteorological reanalysis data along with MODIS remotely sensed data
products such as vegetation property dynamics, albedo, and land cover.


The pixel values for the two Evapotranspiration layers (ET and PET) are the
sum of all eight days within the composite period, and the pixel values for
the two Latent Heat layers (LE and PLE) are the average of all eight days
within the composite period. The last acquisition period of each year is a
5 or 6\-day composite period, depending on the year.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/931/MOD16_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/93/MOD16_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/6/MOD16A2GF)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `ET` | kg/m^2/8day | \-32767 | 32700 | 0\.1 | Total evapotranspiration |
| `LE` | J/m^2/day | \-32767 | 32700 | 10000 | Average latent heat flux |
| `PET` | kg/m^2/8day | \-32767 | 32700 | 0\.1 | Total potential evapotranspiration |
| `PLE` | J/m^2/day | \-32767 | 32700 | 10000 | Average potential latent heat flux |
| `ET_QC` | None |  | Evapotranspiration quality control flags |
| Bitmask for ET\_QC * Bit 0: MODLAND\_QC bits 	+ 0: Good quality (main algorithm with or without saturation) 	+ 1: Other quality (back\-up algorithm or fill values) * Bit 1: Sensor 	+ 0: Terra 	+ 1: Aqua * Bit 2: Dead detector 	+ 0: Detectors apparently fine for up to 50% of channels 1, 2 	+ 1: Dead detectors caused \>50% adjacent detector retrieval * Bits 3\-4: Cloud state 	+ 0: Significant clouds NOT present (clear) 	+ 1: Significant clouds WERE present 	+ 2: Mixed cloud present on pixel 	+ 3: Cloud state not defined, assumed clear * Bits 5\-7: SCF\_QC 5\-level confidence quality score 	+ 0: Main (RT) method used, best result possible (no saturation) 	+ 1: Main (RT) method used with saturation. Good, very usable 	+ 2: Main (RT) method failed due to bad geometry, empirical algorithm used 	+ 3: Main (RT) method failed due to problems other than geometry, empirical algorithm used 	+ 4: Pixel not produced at all, value couldn't be 	retrieved (possible reasons: bad L1B data, unusable MOD09GA data) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit
[LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MOD16A2GF.061](https://doi.org/10.5067/MODIS/MOD16A2GF.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MOD16A2GF')
.filter(ee.Filter.date('2022-01-01','2022-05-01'));
varevapotranspiration=dataset.select('ET');
varevapotranspirationVis={
min:0,
max:300,
palette:[
'ffffff','fcd163','99b718','66a000','3e8601','207401','056201',
'004c00','011301'
],
};
Map.setCenter(0,0,2);
Map.addLayer(evapotranspiration,evapotranspirationVis,'Evapotranspiration');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD16A2GF)


[MOD16A2GF.061: Terra Net Evapotranspiration Gap\-Filled 8\-Day Global 500m](/earth-engine/datasets/catalog/MODIS_061_MOD16A2GF)

The Terra Moderate Resolution Imaging Spectroradiometer (MODIS) MOD16A2GF Version 6\.1 Evapotranspiration/Latent Heat Flux (ET/LE) product is a year\-end gap\-filled 8\-day composite dataset produced at 500 meter (m) pixel resolution. The algorithm used for the MOD16 data product collection is based on the logic of the Penman\-Monteith equation, which includes inputs …

 MODIS/061/MOD16A2GF,
 8\-day,evapotranspiration,global,modis,nasa,water\-vapor

2000\-01\-01T00:00:00Z/2024\-12\-26T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MOD16A2GF.061](https://doi.org/https://doi.org/10.5067/MODIS/MOD16A2GF.061)
* [https://doi.org/10\.5067/MODIS/MOD16A2GF.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD16A2GF)









