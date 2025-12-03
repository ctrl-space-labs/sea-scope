



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NOAA CDR VIIRS NDVI: Normalized Difference Vegetation Index, Version 1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================================








Dataset Availability
2014\-01\-01T00:00:00Z–2025\-07\-12T00:00:00Z
Dataset Provider


[NOAA](https://www.ncei.noaa.gov/products/climate-data-records/normalized-difference-vegetation-index)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CDR/VIIRS/NDVI/V1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_VIIRS_NDVI_V1)





Cadence
1 Day
Tags


[cdr](/earth-engine/datasets/tags/cdr)
[daily](/earth-engine/datasets/tags/daily)
[land](/earth-engine/datasets/tags/land)
[ndvi](/earth-engine/datasets/tags/ndvi)
[noaa](/earth-engine/datasets/tags/noaa)
[vegetation\-indices](/earth-engine/datasets/tags/vegetation-indices)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



This dataset contains gridded daily Normalized Difference Vegetation Index
(NDVI) derived from the NOAA Climate Data Record (CDR) of Visible Infrared
Imaging Radiometer Suite (VIIRS) Surface Reflectance. The data record spans
from 2014 onward using data from NOAA polar orbiting
satellites. The data are projected on a 0\.05 degree x 0\.05 degree global
grid. This dataset is one of the Land Surface CDR products produced by the
NASA Goddard Space Flight Center (GSFC) and the University of Maryland
(UMD).


Known issues with this dataset include:


* TIMEOFDAY variable contains values that are too large by 1 day
* Latitude values are not correctly associated with the center of
the grid cell, error is \< 0\.002 degrees
* Longitude values are not correctly associated with the center of
the grid cell, error is \< 0\.02 degrees


See [technical note from the data provider](https://www.ncei.noaa.gov/pub/data/sds/cdr/CDRs/Normalized_Difference_Vegetation_Index/VIIRS/AlgorithmDescriptionVIIRS_01B-20b.pdf).


Provider's note: the orbital drift of N\-19 (the last NOAA satellite
carrying the AVHRR sensor) began to severely degrade the retrieved
product quality. Therefore, VIIRS is now the primary sensor being used for
these products from 2014\-present.





### Bands



**Pixel Size**
  
5566 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `NDVI` | None | \-9998\* | 9998\* | 0\.0001 | Normalized difference vegetation index |
| `TIMEOFDAY` | h | 0\* | 2400\* | 0\.01 | Hours since start of day |
| `QA` | None |  | Quality control bit flags |
| Bitmask for QA * Bit 0: Unused 	+ 0: No 	+ 1: Yes * Bit 1: Pixel is cloudy 	+ 0: No 	+ 1: Yes * Bit 2: Pixel contains cloud shadow 	+ 0: No 	+ 1: Yes * Bit 3: Pixel is over water 	+ 0: No 	+ 1: Yes * Bit 4: Pixel is over sunglint 	+ 0: No 	+ 1: Yes * Bit 5: Pixel is over dense dark vegetation 	+ 0: No 	+ 1: Yes * Bit 6: Pixel is at night (high solar zenith) 	+ 0: No 	+ 1: Yes * Bit 7: Channels 1\-5 are valid 	+ 0: No 	+ 1: Yes * Bit 8: Channel 1 value is invalid 	+ 0: No 	+ 1: Yes * Bit 9: Channel 2 value is invalid 	+ 0: No 	+ 1: Yes * Bit 10: Channel 3 value is invalid 	+ 0: No 	+ 1: Yes * Bit 11: Channel 4 value is invalid 	+ 0: No 	+ 1: Yes * Bit 12: Channel 5 value is invalid 	+ 0: No 	+ 1: Yes * Bit 13: RHO3 value is invalid 	+ 0: No 	+ 1: Yes * Bit 14: BRDF correction is invalid 	+ 0: No 	+ 1: Yes * Bit 15: Polar flag, latitude over 60 degrees (land) or 50 degrees (ocean) 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| status | STRING | 'provisional' or 'permanent' |




### Terms of Use


**Terms of Use**


The NOAA CDR Program's official distribution point for CDRs is NOAA's
National Climatic Data Center which provides sustained, open access and
active data management of the CDR packages and related information in
keeping with the United States' open data policies and practices as
described in the President's Memorandum on "Open Data Policy" and pursuant
to the Executive Order of May 9, 2013, "Making Open and Machine Readable
the New Default for Government Information". In line with these policies,
the CDR data sets are nonproprietary, publicly available, and no
restrictions are placed upon their use. For more information, see the
[Fair Use of NOAA's CDR Data Sets, Algorithms and Documentation](https://www1.ncdc.noaa.gov/pub/data/sds/cdr/CDRs/Aerosol_Optical_Thickness/UseAgreement_01B-04.pdf)
pdf.




### Citations



Citations:
* Cite as: Vermote, Eric; NOAA CDR Program. (2022\): NOAA Climate Data Record
(CDR) of VIIRS Normalized Difference Vegetation Index (NDVI), Version 1\.
\[indicate subset used]. NOAA National Centers for Environmental Information.
[https://doi.org/10\.25921/gakh\-st76](https://www.ncei.noaa.gov/metadata/geoportal/rest/metadata/item/gov.noaa.ncdc:C01677/html)





### DOIs


* [https://doi.org/10\.25921/gakh\-st76](https://doi.org/10.25921/gakh-st76)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CDR/VIIRS/NDVI/V1')
.filter(ee.Filter.date('2018-05-01','2018-06-01'));
varndvi=dataset.select('NDVI');
varndviVis={
min:-1000.0,
max:5000.0,
palette:[
'ffffff','ce7e45','fcd163','c6ca02','22cc04','99b718','207401',
'012e01'
],
};
Map.setCenter(7.71,17.93,2);
Map.addLayer(ndvi,ndviVis,'NDVI');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_VIIRS_NDVI_V1)


[NOAA CDR VIIRS NDVI: Normalized Difference Vegetation Index, Version 1](/earth-engine/datasets/catalog/NOAA_CDR_VIIRS_NDVI_V1)

This dataset contains gridded daily Normalized Difference Vegetation Index (NDVI) derived from the NOAA Climate Data Record (CDR) of Visible Infrared Imaging Radiometer Suite (VIIRS) Surface Reflectance. The data record spans from 2014 onward using data from NOAA polar orbiting satellites. The data are projected on a 0\.05 degree x …

 NOAA/CDR/VIIRS/NDVI/V1,
 cdr,daily,land,ndvi,noaa,vegetation\-indices,viirs

2014\-01\-01T00:00:00Z/2025\-07\-12T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.25921/gakh\-st76](https://doi.org/https://www.ncei.noaa.gov/products/climate-data-records/normalized-difference-vegetation-index)
* [https://doi.org/10\.25921/gakh\-st76](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_VIIRS_NDVI_V1)









