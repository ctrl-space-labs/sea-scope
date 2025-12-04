



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NOAA CDR AVHRR: Surface Reflectance, Version 5


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================








Dataset Availability
1981\-06\-24T00:00:00Z–2013\-12\-31T00:00:00Z
Dataset Provider


[NOAA](https://www.ncei.noaa.gov/products/climate-data-records/surface-reflectance)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CDR/AVHRR/SR/V5")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_AVHRR_SR_V5)





Cadence
1 Day
Tags


[avhrr](/earth-engine/datasets/tags/avhrr)
[cdr](/earth-engine/datasets/tags/cdr)
[daily](/earth-engine/datasets/tags/daily)
[land](/earth-engine/datasets/tags/land)
[noaa](/earth-engine/datasets/tags/noaa)
[reflectance](/earth-engine/datasets/tags/reflectance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sr](/earth-engine/datasets/tags/sr)








#### Description



The NOAA Climate Data Record (CDR) of AVHRR Surface Reflectance contains
gridded daily surface reflectance and brightness temperatures derived from
the Advanced Very High Resolution Radiometer (AVHRR) sensors onboard seven
NOAA polar orbiting satellites. The data are gridded at a
resolution of 0\.05° and computed globally over land surfaces.


Known issues with this dataset include:


* TIMEOFDAY variable contains values that are too large by 1 day
* Latitude values are not correctly associated with the center of
the grid cell, error is \< 0\.002 degrees
* Longitude values are not correctly associated with the center of
the grid cell, error is \< 0\.02 degrees


See [technical note from the data provider](https://www.ncei.noaa.gov/pub/data/sds/cdr/CDRs/Surface_Reflectance/AVHRR/AlgorithmDescriptionAVHRR_01B-20a.pdf).


Provider's note: the orbital drift of N\-19 (the last NOAA satellite
carrying the AVHRR sensor) began to severely degrade the retrieved
product quality. Therefore, VIIRS is now the primary sensor being used for
these products from 2014\-present.





### Bands



**Pixel Size**
  
5566 meters



**Bands**




| Name | Units | Min | Max | Scale | Wavelength | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `SREFL_CH1` | None | 1\* | 10000\* | 0\.0001 | 640nm | Bidirectional surface reflectance |
| `SREFL_CH2` | None | 1\* | 10000\* | 0\.0001 | 860nm | Bidirectional surface reflectance |
| `SREFL_CH3` | None | \-32768\* | 32767\* | 0\.0001 | 3\.75µm | Bidirectional surface reflectance |
| `BT_CH3` | K | \-32519\* | 30136\* | 0\.1 | 3\.75µm | Brightness temperature |
| `BT_CH4` | K | \-32519\* | 31450\* | 0\.1 | 11\.0µm | Brightness temperature |
| `BT_CH5` | K | \-7623\* | 18788\* | 0\.1 | 12\.0µm | Brightness temperature |
| `TIMEOFDAY` | h | 0\* | 2399\* | 0\.01 | None | Hours since start of day |
| `RELAZ` | deg | \-32768\* | 32767\* | 0\.01 | None | Relative sensor azimuth angle |
| `SZEN` | deg | 219\* | 8546\* | 0\.01 | None | Solar zenith angle |
| `VZEN` | deg | 0\* | 6936\* | 0\.01 | None | View zenith angle, scale 0\.01 |
| `QA` | None |  | None | Quality control bit flags |
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
* Eric Vermote, Chris Justice, Ivan Csiszar, Jeff Eidenshink, Ranga Myneni,
Frederic Baret, Ed Masuoka, Robert Wolfe, Martin Claverie and NOAA CDR
Program (2014\): NOAA Climate Data Record (CDR) of AVHRR Surface Reflectance,
Version 4\. \[indicate subset used]. NOAA National Climatic Data Center.





### DOIs


* [https://doi.org/10\.7289/V53776Z4](https://doi.org/10.7289/V53776Z4)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CDR/AVHRR/SR/V5')
.filter(ee.Filter.date('2018-05-01','2018-06-01'));
varsurfaceReflectance=dataset.select('SREFL_CH1');
varsurfaceReflectanceVis={
min:-1000.0,
max:9000.0,
palette:['003b02','006a03','008d05','01be07','01ff09','ffffff'],
};
Map.setCenter(52.48,71.72,1);
Map.addLayer(surfaceReflectance,surfaceReflectanceVis,'Surface Reflectance');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_AVHRR_SR_V5)


[NOAA CDR AVHRR: Surface Reflectance, Version 5](/earth-engine/datasets/catalog/NOAA_CDR_AVHRR_SR_V5)

The NOAA Climate Data Record (CDR) of AVHRR Surface Reflectance contains gridded daily surface reflectance and brightness temperatures derived from the Advanced Very High Resolution Radiometer (AVHRR) sensors onboard seven NOAA polar orbiting satellites. The data are gridded at a resolution of 0\.05° and computed globally over land surfaces. Known …

 NOAA/CDR/AVHRR/SR/V5,
 avhrr,cdr,daily,land,noaa,reflectance,satellite\-imagery,sr

1981\-06\-24T00:00:00Z/2013\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7289/V53776Z4](https://doi.org/https://www.ncei.noaa.gov/products/climate-data-records/surface-reflectance)
* [https://doi.org/10\.7289/V53776Z4](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_AVHRR_SR_V5)









