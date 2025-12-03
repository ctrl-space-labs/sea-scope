



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD43C3\.061 BRDF/Albedo Daily L3 0\.05 Deg CMG


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-07T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD43C3.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD43C3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43C3)





Cadence
1 Day
Tags


[albedo](/earth-engine/datasets/tags/albedo)
[black\-sky](/earth-engine/datasets/tags/black-sky)
[brdf](/earth-engine/datasets/tags/brdf)
[daily](/earth-engine/datasets/tags/daily)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[usgs](/earth-engine/datasets/tags/usgs)
[white\-sky](/earth-engine/datasets/tags/white-sky)








#### Description



The MCD43C3 Version 6\.1
Bidirectional Reflectance Distribution Function and Albedo (BRDF/Albedo) Albedo
dataset is produced daily using 16 days of Terra and Aqua MODIS data in a 0\.05
degree (5,600 meters at the equator) Climate Modeling Grid (CMG). Data are
temporally weighted to the ninth day of the retrieval period which is reflected
in the Julian date in the file name. This CMG product covers the entire globe
for use in climate simulation models.


MCD43C3 provides black\-sky albedo (directional hemispherical reflectance)
and white\-sky albedo (bihemispherical reflectance) at local solar noon.
Black\-sky albedo and white\-sky albedo values are available as a separate layer
for MODIS spectral bands 1 through 7 as well as the visible, near infrared
(NIR), and shortwave bands. Along with the 20 albedo layers are ancillary
layers for quality, local solar noon, percent finer resolution inputs, snow
cover, and uncertainty.


See
[dataset user guide](https://www.umb.edu/spectralmass/terra_aqua_modis/v006/mcd43c3)
for more information.





### Bands



**Pixel Size**
  
5600 meters



**Bands**




| Name | Units | Min | Max | Scale | Wavelength | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `Albedo_BSA_Band1` | None | 0 | 32766 | 0\.001 | 620\-670nm | Black\-sky albedo for band 1 |
| `Albedo_BSA_Band2` | None | 0 | 32766 | 0\.001 | 841\-876nm | Black\-sky albedo for band 2 |
| `Albedo_BSA_Band3` | None | 0 | 32766 | 0\.001 | 459\-479nm | Black\-sky albedo for band 3 |
| `Albedo_BSA_Band4` | None | 0 | 32766 | 0\.001 | 545\-565nm | Black\-sky albedo for band 4 |
| `Albedo_BSA_Band5` | None | 0 | 32766 | 0\.001 | 1230\-1250nm | Black\-sky albedo for band 5 |
| `Albedo_BSA_Band6` | None | 0 | 32766 | 0\.001 | 1628\-1652nm | Black\-sky albedo for band 6 |
| `Albedo_BSA_Band7` | None | 0 | 32766 | 0\.001 | 2105\-2155nm | Black\-sky albedo for band 7 |
| `Albedo_BSA_vis` | None | 0 | 32766 | 0\.001 | None | Black\-sky albedo for visible brodband |
| `Albedo_BSA_nir` | None | 0 | 32766 | 0\.001 | 858nm | Black\-sky albedo for NIR broadband |
| `Albedo_BSA_shortwave` | None | 0 | 32766 | 0\.001 | None | Black\-sky albedo for shortwave broadband |
| `Albedo_WSA_Band1` | None | 0 | 32766 | 0\.001 | 620\-670nm | White\-sky albedo for band 1 |
| `Albedo_WSA_Band2` | None | 0 | 32766 | 0\.001 | 841\-876nm | White\-sky albedo for band 2 |
| `Albedo_WSA_Band3` | None | 0 | 32766 | 0\.001 | 459\-479nm | White\-sky albedo for band 3 |
| `Albedo_WSA_Band4` | None | 0 | 32766 | 0\.001 | 545\-565nm | White\-sky albedo for band 4 |
| `Albedo_WSA_Band5` | None | 0 | 32766 | 0\.001 | 1230\-1250nm | White\-sky albedo for band 5 |
| `Albedo_WSA_Band6` | None | 0 | 32766 | 0\.001 | 1628\-1652nm | White\-sky albedo for band 6 |
| `Albedo_WSA_Band7` | None | 0 | 32766 | 0\.001 | 2105\-2155nm | White\-sky albedo for band 7 |
| `Albedo_WSA_vis` | None | 0 | 32766 | 0\.001 | None | White\-sky albedo for visible broadband |
| `Albedo_WSA_nir` | None | 0 | 32766 | 0\.001 | 858nm | White\-sky albedo for NIR broadband |
| `Albedo_WSA_shortwave` | None | 0 | 32766 | 0\.001 | None | White\-sky albedo for shortwave broadband |
| `BRDF_Quality` | None |  | None | Global albedo quality |
| Bitmask for BRDF\_Quality * Bits 0\-2: BRDF and albedo quality information 	+ 0: best quality, 100% with full inversions 	+ 1: good quality, 75% or more with best full inversions and 90% or more 	with full inversions 	+ 2: relative good quality, 75% or more with full inversions 	+ 3: mixed, 75% or less full inversions and 25% or less fill values 	+ 4: all magnitude inversions or 50% or less fill values 	+ 5: all magnitude inversions or 50% or less fill values | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `Local_Solar_Noon` | deg | 0 | 90 |  | None | Local solar noon zenith angle |
| `Percent_Inputs` | % | 0 | 100 |  | None | Percent of the processed finer resolution data which contributed to this CMG pixel |
| `Percent_Snow` | % | 0 | 100 |  | None | Percent of underlying data flagged as snow |
| `BRDF_Albedo_Uncertainty` | None | 0 | 32766 | 0\.001 | None | BRDF inversion information. Weights of determination (WoD) of the white sky albedo (see Lucht, W., \& Lewis, P. (2000\). Theoretical noise sensitivity of BRDF and albedo retrieval from the EOS\-MODIS and MISR sensors with respect to angular sampling. International Journal of Remote Sensing, 21(1\), 81\-98\). WoDs give a measure of the uncertainty due to the angular sampling of the inputs available for each retrieval. |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD43C3\.061](https://doi.org/10.5067/MODIS/MCD43C3.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MCD43C3')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varblackSkyAlbedo=dataset.select('Albedo_BSA_Band1');
varblackSkyAlbedoVis={
min:0.0,
max:400.0,
};
Map.setCenter(6.746,46.529,6);
Map.addLayer(blackSkyAlbedo,blackSkyAlbedoVis,'Black-Sky Albedo');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43C3)


[MCD43C3\.061 BRDF/Albedo Daily L3 0\.05 Deg CMG](/earth-engine/datasets/catalog/MODIS_061_MCD43C3)

The MCD43C3 Version 6\.1 Bidirectional Reflectance Distribution Function and Albedo (BRDF/Albedo) Albedo dataset is produced daily using 16 days of Terra and Aqua MODIS data in a 0\.05 degree (5,600 meters at the equator) Climate Modeling Grid (CMG). Data are temporally weighted to the ninth day of the retrieval period …

 MODIS/061/MCD43C3,
 albedo,black\-sky,brdf,daily,global,modis,nasa,satellite\-imagery,usgs,white\-sky

2000\-02\-24T00:00:00Z/2025\-07\-07T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD43C3\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD43C3.061)
* [https://doi.org/10\.5067/MODIS/MCD43C3\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD43C3)









