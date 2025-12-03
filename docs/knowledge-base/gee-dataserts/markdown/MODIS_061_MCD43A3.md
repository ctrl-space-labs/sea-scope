



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD43A3\.061 MODIS Albedo Daily 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-05T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD43A3.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD43A3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43A3)





Cadence
1 Day
Tags


[albedo](/earth-engine/datasets/tags/albedo)
[black\-sky](/earth-engine/datasets/tags/black-sky)
[daily](/earth-engine/datasets/tags/daily)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[usgs](/earth-engine/datasets/tags/usgs)
[white\-sky](/earth-engine/datasets/tags/white-sky)








#### Description



The MCD43A3 V6\.1 Albedo Model dataset is a daily 16\-day
product. It provides both directional hemispherical reflectance
(black sky albedo) and bihemispherical reflectance (white sky albedo)
for each of the MODIS surface reflectance bands (band 1 through
band 7\) as well as 3 broad spectrum bands (visible, near infrared,
and shortwave). Each 500m/pixel daily image is generated using
16 days of data, centered on the given day. A quality band is
also provided for each of the 10 albedo bands.


Documentation:


* [User's Guide](https://www.umb.edu/spectralmass/terra_aqua_modis/v006)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/97/MCD43_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MCD43A3)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Min | Max | Scale | Wavelength | Description |
| --- | --- | --- | --- | --- | --- |
| `Albedo_BSA_Band1` | 0 | 32766 | 0\.001 | 620\-670nm | Black\-sky albedo for band 1 |
| `Albedo_BSA_Band2` | 0 | 32766 | 0\.001 | 841\-876nm | Black\-sky albedo for band 2 |
| `Albedo_BSA_Band3` | 0 | 32766 | 0\.001 | 459\-479nm | Black\-sky albedo for band 3 |
| `Albedo_BSA_Band4` | 0 | 32766 | 0\.001 | 545\-565nm | Black\-sky albedo for band 4 |
| `Albedo_BSA_Band5` | 0 | 32766 | 0\.001 | 1230\-1250nm | Black\-sky albedo for band 5 |
| `Albedo_BSA_Band6` | 0 | 32766 | 0\.001 | 1628\-1652nm | Black\-sky albedo for band 6 |
| `Albedo_BSA_Band7` | 0 | 32766 | 0\.001 | 2105\-2155nm | Black\-sky albedo for band 7 |
| `Albedo_BSA_vis` | 0 | 32766 | 0\.001 | None | Black\-sky albedo for visible brodband |
| `Albedo_BSA_nir` | 0 | 32766 | 0\.001 | 858nm | Black\-sky albedo for NIR broadband |
| `Albedo_BSA_shortwave` | 0 | 32766 | 0\.001 | None | Black\-sky albedo for shortwave broadband |
| `Albedo_WSA_Band1` | 0 | 32766 | 0\.001 | 620\-670nm | White\-sky albedo for band 1 |
| `Albedo_WSA_Band2` | 0 | 32766 | 0\.001 | 841\-876nm | White\-sky albedo for band 2 |
| `Albedo_WSA_Band3` | 0 | 32766 | 0\.001 | 459\-479nm | White\-sky albedo for band 3 |
| `Albedo_WSA_Band4` | 0 | 32766 | 0\.001 | 545\-565nm | White\-sky albedo for band 4 |
| `Albedo_WSA_Band5` | 0 | 32766 | 0\.001 | 1230\-1250nm | White\-sky albedo for band 5 |
| `Albedo_WSA_Band6` | 0 | 32766 | 0\.001 | 1628\-1652nm | White\-sky albedo for band 6 |
| `Albedo_WSA_Band7` | 0 | 32766 | 0\.001 | 2105\-2155nm | White\-sky albedo for band 7 |
| `Albedo_WSA_vis` | 0 | 32766 | 0\.001 | None | White\-sky albedo for visible broadband |
| `Albedo_WSA_nir` | 0 | 32766 | 0\.001 | 858nm | White\-sky albedo for NIR broadband |
| `Albedo_WSA_shortwave` | 0 | 32766 | 0\.001 | None | White\-sky albedo for shortwave broadband |
| `BRDF_Albedo_Band_Mandatory_Quality_Band1` |  | None | BRDF albedo mandatory quality for band 1 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band1 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band2` |  | None | BRDF albedo mandatory quality for band 2 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band2 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band3` |  | None | BRDF albedo mandatory quality for band 3 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band3 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band4` |  | None | BRDF albedo mandatory quality for band 4 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band4 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band5` |  | None | BRDF albedo mandatory quality for band 5 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band5 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band6` |  | None | BRDF albedo mandatory quality for band 6 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band6 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band7` |  | None | BRDF albedo mandatory quality for band 7 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band7 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_vis` |  | None | BRDF albedo mandatory quality for visible broadband |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_vis * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_nir` |  | None | BRDF albedo mandatory quality for NIR broadband |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_nir * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_shortwave` |  | None | BRDF albedo mandatory quality for shortwave broadband |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_shortwave * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD43A3\.061](https://doi.org/10.5067/MODIS/MCD43A3.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MCD43A3')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varblackSkyAlbedo=dataset.select('Albedo_BSA_Band1');
varblackSkyAlbedoVis={
min:0.0,
max:400.0,
};
Map.setCenter(6.746,46.529,6);
Map.addLayer(blackSkyAlbedo,blackSkyAlbedoVis,'Black-Sky Albedo');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43A3)


[MCD43A3\.061 MODIS Albedo Daily 500m](/earth-engine/datasets/catalog/MODIS_061_MCD43A3)

The MCD43A3 V6\.1 Albedo Model dataset is a daily 16\-day product. It provides both directional hemispherical reflectance (black sky albedo) and bihemispherical reflectance (white sky albedo) for each of the MODIS surface reflectance bands (band 1 through band 7\) as well as 3 broad spectrum bands (visible, near infrared, and …

 MODIS/061/MCD43A3,
 albedo,black\-sky,daily,global,modis,nasa,satellite\-imagery,usgs,white\-sky

2000\-02\-24T00:00:00Z/2025\-07\-05T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD43A3\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD43A3.061)
* [https://doi.org/10\.5067/MODIS/MCD43A3\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD43A3)









