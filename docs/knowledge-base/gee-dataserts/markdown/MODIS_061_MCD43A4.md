



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD43A4\.061 MODIS Nadir BRDF\-Adjusted Reflectance Daily 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-05T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD43A4.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD43A4")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43A4)





Cadence
1 Day
Tags


[albedo](/earth-engine/datasets/tags/albedo)
[brdf](/earth-engine/datasets/tags/brdf)
[daily](/earth-engine/datasets/tags/daily)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[reflectance](/earth-engine/datasets/tags/reflectance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The MCD43A4 V6\.1 Nadir Bidirectional Reflectance Distribution
Function Adjusted Reflectance (NBAR) product provides 500 meter
reflectance data of the MODIS "land" bands 1\-7\. These are adjusted
using a bidirectional reflectance distribution function to model
the values as if they were collected from a nadir view. The data
are produced daily based on a 16\-day retrieval period, with the
image's date occurring on the 9th day. This product combines data
from both the Terra and Aqua spacecrafts, choosing the best representative
pixel from the 16\-day period.


Documentation:


* [User's Guide](https://www.umb.edu/spectralmass/terra_aqua_modis/v006)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/97/MCD43_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MCD43A4)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Min | Max | Scale | Wavelength | Description |
| --- | --- | --- | --- | --- | --- |
| `Nadir_Reflectance_Band1` | 0 | 32766 | 0\.0001 | 620\-670nm | NBAR at local solar noon for band 1 |
| `Nadir_Reflectance_Band2` | 0 | 32766 | 0\.0001 | 841\-876nm | NBAR at local solar noon for band 2 |
| `Nadir_Reflectance_Band3` | 0 | 32766 | 0\.0001 | 459\-479nm | NBAR at local solar noon for band 3 |
| `Nadir_Reflectance_Band4` | 0 | 32766 | 0\.0001 | 545\-565nm | NBAR at local solar noon for band 4 |
| `Nadir_Reflectance_Band5` | 0 | 32766 | 0\.0001 | 1230\-1250nm | NBAR at local solar noon for band 5 |
| `Nadir_Reflectance_Band6` | 0 | 32766 | 0\.0001 | 1628\-1652nm | NBAR at local solar noon for band 6 |
| `Nadir_Reflectance_Band7` | 0 | 32766 | 0\.0001 | 2105\-2155nm | NBAR at local solar noon for band 7 |
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




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD43A4\.061](https://doi.org/10.5067/MODIS/MCD43A4.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MCD43A4')
.filter(ee.Filter.date('2018-04-01','2018-06-01'));
vartrueColor=dataset.select([
'Nadir_Reflectance_Band1','Nadir_Reflectance_Band4',
'Nadir_Reflectance_Band3'
]);
vartrueColorVis={
min:0.0,
max:4000.0,
gamma:1.4,
};
Map.setCenter(-7.03125,31.0529339857,2);
Map.addLayer(trueColor,trueColorVis,'True Color');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43A4)


[MCD43A4\.061 MODIS Nadir BRDF\-Adjusted Reflectance Daily 500m](/earth-engine/datasets/catalog/MODIS_061_MCD43A4)

The MCD43A4 V6\.1 Nadir Bidirectional Reflectance Distribution Function Adjusted Reflectance (NBAR) product provides 500 meter reflectance data of the MODIS "land" bands 1\-7\. These are adjusted using a bidirectional reflectance distribution function to model the values as if they were collected from a nadir view. The data are produced daily …

 MODIS/061/MCD43A4,
 albedo,brdf,daily,global,modis,nasa,reflectance,satellite\-imagery,usgs

2000\-02\-24T00:00:00Z/2025\-07\-05T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD43A4\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD43A4.061)
* [https://doi.org/10\.5067/MODIS/MCD43A4\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD43A4)









