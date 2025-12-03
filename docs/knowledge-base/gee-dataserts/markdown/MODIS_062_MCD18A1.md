



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD18A1\.062 Surface Radiation Daily/3\-Hour


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================








Dataset Availability
2000\-03\-03T00:00:00Z–2025\-06\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://lpdaac.usgs.gov/products/mcd18a1v062/)



Earth Engine Snippet


`ee.ImageCollection("MODIS/062/MCD18A1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_062_MCD18A1)





Cadence
1 Day
Tags


[climate](/earth-engine/datasets/tags/climate)
[par](/earth-engine/datasets/tags/par)
[radiation](/earth-engine/datasets/tags/radiation)








#### Description



The MCD18A1 Version 6\.2
is a Moderate Resolution Imaging Spectroradiometer
(MODIS) Terra and Aqua combined Downward Shortwave Radiation (DSR) gridded
Level 3 product produced daily at 1 kilometer pixel resolution with
estimates of DSR every 3 hours. DSR is incident solar radiation over land
surfaces in the shortwave spectrum (300\-4,000 nanometers) and is an
important variable in land\-surface models that address a variety of
scientific and application issues. The MCD18 products are based on a
prototyping algorithm that uses multi\-temporal signatures of MODIS data to
derive surface reflectance and then calculate incident DSR using the look\-up
table (LUT) approach. The LUTs consider different types of loadings of
aerosols and clouds at a variety of illumination/viewing geometry. Global
DSR products are generated from MODIS and geostationary satellite data.
Additional details regarding the methodology used to create the data are
available in the
[Algorithm Theoretical Basis Document](https://lpdaac.usgs.gov/documents/106/MCD18_ATBD.pdf).





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `DSR` | W/m^2 | 0 | 1400 | Instantaneous total DSR at MODIS overpass |
| `Direct` | W/m^2 | 0 | 1400 | Instantaneous direct DSR at MODIS overpass |
| `Diffuse` | W/m^2 | 0 | 1400 | Instantaneous diffuse DSR at MODIS overpass |
| `GMT_0000_DSR` | W/m^2 | 0 | 1400 | Total DSR at GMT 00:00 |
| `GMT_0300_DSR` | W/m^2 | 0 | 1400 | Total DSR at GMT 03:00 |
| `GMT_0600_DSR` | W/m^2 | 0 | 1400 | Total DSR at GMT 06:00 |
| `GMT_0900_DSR` | W/m^2 | 0 | 1400 | Total DSR at GMT 09:00 |
| `GMT_1200_DSR` | W/m^2 | 0 | 1400 | Total DSR at GMT 12:00 |
| `GMT_1500_DSR` | W/m^2 | 0 | 1400 | Total DSR at GMT 15:00 |
| `GMT_1800_DSR` | W/m^2 | 0 | 1400 | Total DSR at GMT 18:00 |
| `GMT_2100_DSR` | W/m^2 | 0 | 1400 | Total DSR at GMT 21:00 |
| `DSR_Quality` | None | Quality flag |
| Bitmask for DSR\_Quality * Bits 0\-1: Input source of surface reflectance data 	+ 0: no valid surface reflectance data 	+ 1: from the MCD43 product 	+ 2: from the climatology data | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD18A1\.062](https://doi.org/10.5067/MODIS/MCD18A1.062)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/062/MCD18A1')
.filter(ee.Filter.date('2000-01-01','2001-01-01'));
vargmt_1200_dsr=dataset.select('GMT_1200_DSR');
vargmt_1200_dsr_vis={
min:0,
max:350,
palette:['0f17ff','b11406','f1ff23'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(
gmt_1200_dsr,gmt_1200_dsr_vis,
'Total dsr at GMT 12:00');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_062_MCD18A1)


[MCD18A1\.062 Surface Radiation Daily/3\-Hour](/earth-engine/datasets/catalog/MODIS_062_MCD18A1)

The MCD18A1 Version 6\.2 is a Moderate Resolution Imaging Spectroradiometer (MODIS) Terra and Aqua combined Downward Shortwave Radiation (DSR) gridded Level 3 product produced daily at 1 kilometer pixel resolution with estimates of DSR every 3 hours. DSR is incident solar radiation over land surfaces in the shortwave spectrum (300\-4,000 …

 MODIS/062/MCD18A1,
 climate,par,radiation

2000\-03\-03T00:00:00Z/2025\-06\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD18A1\.062](https://doi.org/https://lpdaac.usgs.gov/products/mcd18a1v062/)
* [https://doi.org/10\.5067/MODIS/MCD18A1\.062](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_062_MCD18A1)









