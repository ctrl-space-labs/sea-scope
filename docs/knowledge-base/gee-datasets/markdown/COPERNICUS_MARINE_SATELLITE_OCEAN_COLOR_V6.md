



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Copernicus Satellite Ocean Color Daily Data


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================








Dataset Availability
1997\-01\-01T00:00:00Z–2024\-12\-31T00:00:00Z
Dataset Provider


[Copernicus](https://doi.org/10.24381/cds.f85b319d)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/MARINE/SATELLITE_OCEAN_COLOR/V6")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_MARINE_SATELLITE_OCEAN_COLOR_V6)





Cadence
1 Day
Tags


[chlorophyll\-a](/earth-engine/datasets/tags/chlorophyll-a)
[copernicus](/earth-engine/datasets/tags/copernicus)
[daily](/earth-engine/datasets/tags/daily)
[marine](/earth-engine/datasets/tags/marine)
[oceans](/earth-engine/datasets/tags/oceans)








#### Description



This dataset provides global daily estimates of ocean surface chlorophyll\-a
concentration and remote sensing reflectance derived from multiple satellite
sensors.


Remote\-sensing reflectance (or Rrs) is defined as the ratio of water\-leaving
radiance to downwelling irradiance and serves as the main input to
algorithms used to derive other ocean colour products. Chlorophyll\-a (Chl\-a)
is the main photosynthetic pigment found in phytoplankton, which form the
base of the marine food\-web and are responsible for approximately half of
the global photosynthesis. Chl\-a can be estimated from Rrs data using
different algorithms (see details in the Documentation). Here, we provide a
blended Chl\-a estimate from multiple algorithms, where blending is based on
the suitability of each candidate algorithm to the optical typology of a
given pixel. This approach provides the best estimates of global Chl\-a
across a range of water types.


The files from this dataset contain global daily composites of merged sensor
products: SeaWiFS, MERIS, MODIS Aqua, VIIRS, and (from version 5\.0 onward)
OLCI. Note that Rrs and Chl\-a data are only available over cloud\- and
ice\-free areas. As a result, more complete spatial coverage (as shown in the
map in the upper\-right corner) can be achieved by aggregating data over
longer time periods.


This dataset is produced using the processing chain software developed by
the Ocean Colour component of the European Space Agency Climate Change
Initiative project (ESA OC\-CCI). More details are available in the dataset
[documentation](https://dast.copernicus-climate.eu/documents/satellite-ocean-colour/v6.0/WP2-FDDP-2022-04_C3S2-Lot3_PUGS-of-v6.0-OceanColour-product_v1.1_FINAL.pdf).





### Bands



**Pixel Size**
  
4000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `MERIS_nobs` | None | 0\.11 | 135\.55 | Number of observations from MERIS sensor |
| `MODISA_nobs` | None | 0\.11 | 126\.33 | Number of observations from MODIS\-A sensor |
| `OLCI-A_nobs` | None | 0\.11 | 121 | Number of observations from OLCI\-A sensor |
| `OLCI-B_nobs` | None | 0\.11 | 121 | Number of observations from OLCI\-B sensor |
| `SeaWiFS_nobs` | None | 0\.11 | 61\.77 | Number of observations from SeaWiFS sensor |
| `VIIRS_nobs` | None | 0\.11 | 236\.44 | Number of observations from VIIRS sensor |
| `chlor_a` | mg/m^3 | 0 | 99\.9 | Chlorophyll\-a concentration |
| `total_nobs` | None | 0\.11 | 329\.77 | Total number of observations |
| `Rrs_412` | sr^\-1 | 0 | 0\.26 | Remote sensing reflectance at 412 nm |
| `Rrs_443` | sr^\-1 | 0 | 0\.28 | Remote sensing reflectance at 443 nm |
| `Rrs_490` | sr^\-1 | 0 | 0\.38 | Remote sensing reflectance at 490 nm |
| `Rrs_510` | sr^\-1 | 0 | 0\.39 | Remote sensing reflectance at 510 nm |
| `Rrs_560` | sr^\-1 | 0 | 0\.402 | Remote sensing reflectance at 560 nm |
| `Rrs_665` | sr^\-1 | 0 | 0\.21 | Remote sensing reflectance at 665 nm |
| `Rrs_MERIS_nobs` | None | 0\.11 | 135\.55 | Number of observations from MERIS sensor |
| `Rrs_MODISA_nobs` | None | 0\.11 | 126\.33 | Number of observations from MODIS\-A sensor |
| `Rrs_OLCI-A_nobs` | None | 0\.11 | 121 | Number of observations from OLCI\-A sensor |
| `Rrs_OLCI-B_nobs` | None | 0\.11 | 121 | Number of observations from OLCI\-B sensor |
| `Rrs_SeaWiFS_nobs` | None | 0\.11 | 61\.77 | Number of observations from SeaWiFS sensor |
| `Rrs_VIIRS_nobs` | None | 0\.11 | 236\.44 | Number of observations from VIIRS sensor |
| `Rrs_total_nobs` | None | 0\.11 | 329\.77 | Total number of observations from RRS sensors |




### Terms of Use


**Terms of Use**


This dataset is released for use under the CC\-BY licence. Highlights and
key features of the licence are provided in this document. [License](https://creativecommons.org/licenses/by/4.0/).




### Citations



Citations:
* Copernicus Climate Change Service (2019\): Ocean colour daily data from 1997
to present derived from satellite observations. Copernicus Climate Change
Service (C3S) Climate Data Store (CDS). 
[doi:10\.24381/cds.f85b319d](https://doi.org/10.24381/cds.f85b319d)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('COPERNICUS/MARINE/SATELLITE_OCEAN_COLOR/V6')
.filter(ee.Filter.date('2024-06-01','2024-07-01'));
varchlorA=dataset.select('chlor_a');
varchlorAVis={
min:0,
max:1,
palette:['blue','purple','cyan','green','yellow','red'],
};
Map.setCenter(71,52,2);
Map.addLayer(
chlorA,chlorAVis,
'Chlorophyll-a concentration');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_MARINE_SATELLITE_OCEAN_COLOR_V6)


[Copernicus Satellite Ocean Color Daily Data](/earth-engine/datasets/catalog/COPERNICUS_MARINE_SATELLITE_OCEAN_COLOR_V6)

This dataset provides global daily estimates of ocean surface chlorophyll\-a concentration and remote sensing reflectance derived from multiple satellite sensors. Remote\-sensing reflectance (or Rrs) is defined as the ratio of water\-leaving radiance to downwelling irradiance and serves as the main input to algorithms used to derive other ocean colour products. …

 COPERNICUS/MARINE/SATELLITE\_OCEAN\_COLOR/V6,
 chlorophyll\-a,copernicus,daily,marine,oceans

1997\-01\-01T00:00:00Z/2024\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








