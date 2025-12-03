



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MYD08\_M3\.061 Aqua Atmosphere Monthly Global Product


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================================








Dataset Availability
2002\-07\-01T00:00:00Z–2025\-06\-01T00:00:00Z
Dataset Provider


[NASA LAADS DAAC at NASA Goddard Space Flight Center](https://doi.org/10.5067/MODIS/MYD08_M3.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MYD08_M3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD08_M3)





Cadence
1 Month
Tags


[aqua](/earth-engine/datasets/tags/aqua)
[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[monthly](/earth-engine/datasets/tags/monthly)
[nasa](/earth-engine/datasets/tags/nasa)
[temperature](/earth-engine/datasets/tags/temperature)
[usgs](/earth-engine/datasets/tags/usgs)
myd08
myd08\-m3








#### Description



MYD08\_M3 V6\.1 is an atmosphere global product that contains
monthly 1 x 1 degree grid average values of atmospheric parameters.
These parameters are related to atmospheric aerosol particle properties,
total ozone burden, atmospheric water vapor, cloud optical and
physical properties, and atmospheric stability indices. The product
also provides means, standard deviations, QA weighted statistics,
log\-normal distributions, uncertainty estimates, and statistics
for fractions of pixels that satisfy some condition. Below is a
subset of the bands, for a complete list see the
[MOD08 Band List](https://developers.google.com/earth-engine/MOD08_bands.html).


Documentation:


* [User's Guide](https://modis-atmos.gsfc.nasa.gov/sites/default/files/ModAtmo/L3_ATBD_C6_C61_2019_02_20.pdf)
* [Science Data Product Software Documentation](https://modis-atmos.gsfc.nasa.gov/sites/default/files/ModAtmo/L3_C61_Changes_v2.pdf)
* [MYD08\_M3 product description](https://modis-atmos.gsfc.nasa.gov/products/monthly)
* [File specification document](https://modis-atmos.gsfc.nasa.gov/sites/default/files/ModAtmo/MOD08_M3_fs_3045.txt)





### Bands



**Pixel Size**
  
111320 meters



**Bands**




| Name | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- |
| `Aerosol_Optical_Depth_Land_Ocean_Mean_Mean` | \-100 | 5000 | 0\.001 | Aerosol optical thickness at 0\.55 microns for both ocean (best) and land (corrected): mean of daily mean |
| `Aerosol_Optical_Depth_Land_Ocean_Std_Deviation_Mean` | \-100 | 5000 | 0\.001 | Aerosol optical thickness at 0\.55 microns for both ocean (best) and land (corrected): mean of daily standard deviation |
| `Aerosol_Optical_Depth_Land_QA_Mean_Mean_470` | \-100 | 5000 | 0\.001 | Corrected aerosol optical depth (land) at 0\.47 microns: mean of level\-3 QA weighted mean |
| `Aerosol_Optical_Depth_Land_QA_Std_Deviation_Mean_470` | \-100 | 5000 | 0\.001 | Corrected aerosol optical depth (land) at 0\.47 microns: mean of level\-3 weighted QA standard deviation |
| `Cirrus_Fraction_SWIR_FMean` | 0 | 10000 | 0\.0001 | Cirrus area fraction: mean of daily fraction |
| `Cirrus_Fraction_SWIR_FStd` | 0 | 10000 | 0\.0001 | Cirrus area fraction: standard deviation of daily fraction |
| `Cloud_Optical_Thickness_Liquid_Log_Mean_Mean` | 0 | 4176 | 0\.001 | Liquid water cloud optical thickness: mean of daily log mean |
| `Cloud_Optical_Thickness_Liquid_Log_Std_Deviation_Mean` | 0 | 4176 | 0\.001 | Liquid water cloud optical thickness: mean of daily log standard deviation |
| `Cloud_Optical_Thickness_Liquid_Mean_Uncertainty` | 0 | 2000 | 0\.01 | Liquid water cloud optical thickness: multi\-day absolute uncertainty estimate derived from the daily absolute uncertainty estimate |
| `Cloud_Optical_Thickness_Liquid_Log_Mean_Uncertainty` | 0 | 4477 | 0\.001 | Liquid water cloud optical thickness: multi\-day absolute log uncertainty estimate derived from the daily absolute log uncertainty estimate |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA\\'s
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* Platnick, S., M. King, P. Hubanks, 2015\. MODIS Atmosphere L3 Monthly
Product. NASA MODIS Adaptive Processing System, Goddard Space Flight
Center, [doi:10\.5067/MODIS/MYD08\_M3\.061](https://doi.org/10.5067/MODIS/MYD08_M3.061)





### DOIs


* [https://doi.org/10\.5067/MODIS/MYD08\_M3\.061](https://doi.org/10.5067/MODIS/MYD08_M3.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/006/MYD08_M3')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varaerosolOpticalDepth=
dataset.select('Aerosol_Optical_Depth_Land_Ocean_Mean_Mean');
varaerosolOpticalDepthVis={
min:0,
max:3000,
palette:['ffffff','1303ff','01ff09','ff2f00'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(
aerosolOpticalDepth,aerosolOpticalDepthVis,'Aerosol Optical Depth');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD08_M3)


[MYD08\_M3\.061 Aqua Atmosphere Monthly Global Product](/earth-engine/datasets/catalog/MODIS_061_MYD08_M3)

MYD08\_M3 V6\.1 is an atmosphere global product that contains monthly 1 x 1 degree grid average values of atmospheric parameters. These parameters are related to atmospheric aerosol particle properties, total ozone burden, atmospheric water vapor, cloud optical and physical properties, and atmospheric stability indices. The product also provides means, standard …

 MODIS/061/MYD08\_M3,
 aqua,atmosphere,climate,geophysical,global,modis,monthly,nasa,temperature,usgs

2002\-07\-01T00:00:00Z/2025\-06\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MYD08\_M3\.061](https://doi.org/https://doi.org/10.5067/MODIS/MYD08_M3.061)
* [https://doi.org/10\.5067/MODIS/MYD08\_M3\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MYD08_M3)









