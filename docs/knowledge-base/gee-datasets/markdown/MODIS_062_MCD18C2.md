



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD18C2\.062 Photosynthetically Active Radiation Daily 3\-Hour


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-06\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://lpdaac.usgs.gov/products/mcd18c2v062/)



Earth Engine Snippet


`ee.ImageCollection("MODIS/062/MCD18C2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_062_MCD18C2)





Cadence
1 Day
Tags


[climate](/earth-engine/datasets/tags/climate)
[par](/earth-engine/datasets/tags/par)
[radiation](/earth-engine/datasets/tags/radiation)








#### Description



The MCD18C2 Version 6\.2
is a Moderate Resolution Imaging Spectroradiometer
(MODIS) Terra and Aqua combined Photosynthetically Active Radiation (PAR)
gridded Level 3 product produced daily at 0\.05 degree (5,600 meters at the
equator) resolution with estimates of PAR every 3 hours. PAR is incident
solar radiation in the visible spectrum (400\-700 nanometers) and is an
important variable in land\-surface models that address a variety of
scientific and application issues. The MCD18 products are based on a
prototyping algorithm that uses multi\-temporal signatures of MODIS data to
derive surface reflectance and then calculate incident PAR using the look\-up
table (LUT) approach. The LUTs consider different types of loadings of
aerosols and clouds at a variety of illumination/viewing geometry. Global
PAR products are generated from MODIS and geostationary satellite data.
Additional details regarding the methodology used to create the data are
available in the
[Algorithm Theoretical Basis Document](https://lpdaac.usgs.gov/documents/106/MCD18_ATBD.pdf)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Description |
| --- | --- |
| `GMT_0000_PAR` | Total PAR at GMT 00:00 |
| `GMT_0300_PAR` | Total PAR at GMT 03:00 |
| `GMT_0600_PAR` | Total PAR at GMT 06:00 |
| `GMT_0900_PAR` | Total PAR at GMT 09:00 |
| `GMT_1200_PAR` | Total PAR at GMT 12:00 |
| `GMT_1500_PAR` | Total PAR at GMT 15:00 |
| `GMT_1800_PAR` | Total PAR at GMT 18:00 |
| `GMT_2100_PAR` | Total PAR at GMT 21:00 |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD18C2\.062](https://doi.org/10.5067/MODIS/MCD18C2.062)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/062/MCD18C2')
.filter(ee.Filter.date('2001-01-01','2001-02-01'));
vargmt_1200_par=dataset.select('GMT_1200_PAR');
vargmt_1200_par_vis={
min:-236,
max:316,
palette:['0f17ff','b11406','f1ff23'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(
gmt_1200_par,gmt_1200_par_vis,
'Total PAR at GMT 12:00');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_062_MCD18C2)


[MCD18C2\.062 Photosynthetically Active Radiation Daily 3\-Hour](/earth-engine/datasets/catalog/MODIS_062_MCD18C2)

The MCD18C2 Version 6\.2 is a Moderate Resolution Imaging Spectroradiometer (MODIS) Terra and Aqua combined Photosynthetically Active Radiation (PAR) gridded Level 3 product produced daily at 0\.05 degree (5,600 meters at the equator) resolution with estimates of PAR every 3 hours. PAR is incident solar radiation in the visible spectrum …

 MODIS/062/MCD18C2,
 climate,par,radiation

2000\-02\-24T00:00:00Z/2025\-06\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD18C2\.062](https://doi.org/https://lpdaac.usgs.gov/products/mcd18c2v062/)
* [https://doi.org/10\.5067/MODIS/MCD18C2\.062](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_062_MCD18C2)









