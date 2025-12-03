



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NOAA CDR PATMOSX: Cloud Properties, Reflectance, and Brightness Temperatures, Version 5\.3


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================================================================








Dataset Availability
1979\-01\-01T00:00:00Z–2022\-01\-01T00:00:00Z
Dataset Provider


[NOAA](https://www.ncei.noaa.gov/products/climate-data-records/avhrr-hirs-cloud-properties-patmos)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CDR/PATMOSX/V53")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_PATMOSX_V53)





Cadence
1 Day
Tags


[atmospheric](/earth-engine/datasets/tags/atmospheric)
[avhrr](/earth-engine/datasets/tags/avhrr)
[brightness](/earth-engine/datasets/tags/brightness)
[cdr](/earth-engine/datasets/tags/cdr)
[climate](/earth-engine/datasets/tags/climate)
[cloud](/earth-engine/datasets/tags/cloud)
[noaa](/earth-engine/datasets/tags/noaa)
[optical](/earth-engine/datasets/tags/optical)
[reflectance](/earth-engine/datasets/tags/reflectance)
[temperature](/earth-engine/datasets/tags/temperature)
metop
poes








#### Description



This dataset provides high quality Climate Data Record (CDR) of multiple
cloud properties along with Advanced Very High Resolution Radiometer (AVHRR)
Pathfinder Atmospheres Extended (PATMOS\-x) brightness temperatures and
reflectances. These data have been fitted to a 0\.1 x 0\.1 equal angle\-grid
with both ascending and descending assets generated daily from two to ten
NOAA and MetOp satellite passes per day.


This dataset includes 48 bands, 11 of which are deemed CDR quality
(marked with "CDR variable" in the band list).
The cloud products are derived using the ABI (Advanced Baseline Imager)
Cloud Height Algorithm (ACHA), and the Daytime Cloud Optical Properties
(DCOMP) algorithm. For more detail on the processing see the
[Climate Algorithm Theoretical Basis Document (C\-ATBD)](https://www.ncei.noaa.gov/pub/data/sds/cdr/CDRs/AVHRR-HIRS_Reflectance_PATMOS-x/AlgorithmDescription%20_01B-1c.pdf).





### Bands



**Pixel Size**
  
11132 meters



**Bands**




| Name | Units | Min | Max | Scale | Offset | Wavelength | Description |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `cld_emiss_acha` | None | \-127\* | 127\* | 0\.00393701 | 0\.5 | 11µm | Cloud emissivity at 11µm, determined from ACHA (CDR variable) |
| `cld_height_acha` | km | \-32767\* | 32767\* | 0\.000305185 | 10 | None | Cloud height computed using ACHA |
| `cld_height_uncer_acha` | km | \-127\* | 127\* | 0\.0393701 | 5 | None | Cloud height uncertainty computed using ACHA |
| `cld_opd_acha` | None | \-127\* | 127\* | 0\.0322835 | 3\.9 | 0\.65µm | Cloud optical depth at 0\.65µm, determined from ACHA |
| `cld_opd_dcomp` | None | \-32685\* | 32149\* | 0\.00244453 | 79\.9 | 0\.65µm | Cloud optical depth at 0\.65µm, determined from DCOMP (CDR variable) |
| `cld_opd_dcomp_unc` | None | \-32685\* | \-32276\* | 0\.00244453 | 79\.9 | None | Uncertainty in the cloud optical depth at 0\.65µm, determined from DCOMP |
| `cld_press_acha` | hPa | \-32767\* | 32767\* | 0\.0167852 | 550 | None | Cloud\-top pressure computed using ACHA |
| `cld_reff_acha` | µm | \-127\* | 127\* | 0\.629921 | 80 | None | Effective radius of cloud particles determined from ACHA |
| `cld_reff_dcomp` | µm | \-32767\* | 32767\* | 0\.00244148 | 80 | None | Effective radius of cloud particles determined from DCOMP (CDR variable) |
| `cld_reff_dcomp_unc` | µm | \-32767\* | \-32357\* | 0\.00244148 | 80 | None | Uncertainty in the effective radius of cloud particle determined from DCOMP |
| `cld_temp_acha` | K | \-32767\* | 32767\* | 0\.00244148 | 240 | None | Cloud\-top temperature computed using ACHA (CDR variable) |
| `cloud_fraction` | None | \-127\* | 127\* | 0\.00393701 | 0\.5 | None | Cloud fraction computed over a 3x3 pixel array at the native resolution centered on this pixel |
| `cloud_fraction_uncertainty` | None | \-127\* | 0\.00393701 | 0\.5 | None | Cloud fraction uncertainty computed over a 3x3 array |
| `cloud_probability` | None | \-127\* | 127\* | 0\.00393701 | 0\.5 | None | Probability of a pixel being cloudy from the Bayesian cloud mask |
| `cloud_transmission_0_65um` | None | \-127\* | 127\* | 0\.00393701 | 0\.5 | 0\.65µm | Cloud transmission at 0\.65µm from DCOMP |
| `cloud_type` | None |  |  | None | Integer classification of the cloud type including clear and aerosol type |
| `cloud_water_path` | g/m^2 | \-127\* | 127\* | 4\.72441 | 600 | None | Integrated total cloud water over whole column |
| `land_class` | None |  |  | None | Land classes |
| `refl_0_65um` | None | \-32767\* | 32767\* | 0\.00186163 | 59 | 0\.65µm | Top of atmosphere reflectance 0\.65µm (CDR variable) |
| `refl_0_65um_counts` | None | \-21\* | 1017\* |  |  | None | Instrument counts for the 0\.65µm channel |
| `refl_0_65um_stddev_3x3` | None | \-127\* | 127\* | 0\.0787402 | 10 | None | Standard deviation of the 0\.63µm reflectance computed over a 3x3 pixel array |
| `refl_0_86um` | None | \-32767\* | 32767\* | 0\.00186163 | 59 | 0\.86µm | Top of atmosphere reflectance at 0\.86µm (CDR variable) |
| `refl_0_86um_counts` | None | \-21\* | 1016\* |  |  | None | Instrument counts for the 0\.86µm channel |
| `refl_1_60um` | None | \-32767\* | 32767\* | 0\.00186163 | 59 | 1\.60µm | Top of atmosphere reflectance at 1\.60µm (CDR variable) |
| `refl_1_60um_counts` | None | \-12\* | 1629\* |  |  | None | Instrument counts for the 1\.60µm channel |
| `refl_3_75um` | None | \-32767\* | 32767\* | 0\.00152593 | 30 | 3\.75µm | Top of atmosphere reflectance at 3\.75µm (CDR variable) |
| `relative_azimuth_angle` | deg | \-127\* | 127\* | 0\.708661 | 90 | None | Sun\-sensor relative azimuth angle; 0 is the principal plane looking towards sun |
| `scan_element_number` | None | \-999\* | 409\* |  |  | None | Scan element index of the pixel chosen for inclusion in level\-2b |
| `scan_line_number` | None | \-999\* | 13835\* |  |  | None | Scan line number |
| `scan_line_time` | h | 0\* | 23\.99\* |  |  | None | Scan line time |
| `sensor_zenith_angle` | deg | \-127\* | 68\* | 0\.354331 | 45 | None | Sensor zenith for each pixel measured in degrees from nadir |
| `snow_class` | None |  |  | None | Snow classes and values |
| `solar_azimuth_angle` | deg | \-127\* | 127\* | 1\.41732 |  | None | Solar azimuth angle in degrees from north, pixel to sun, positive values are clockwise from north |
| `solar_zenith_angle` | deg | \-101\* | 101\* | 0\.708661 | 90 | None | Solar zenith for each pixel measured in degrees away from the sun (0\=looking at sun) |
| `surface_temperature_retrieved` | K | \-127\* | 127\* | 0\.472441 | 280 | None | Surface temperature retrieved using atmospherically corrected 11µm radiance |
| `surface_type` | None |  |  | None | UMD surface type |
| `temp_11_0um` | K | \-32767\* | 32767\* | 0\.00244148 | 260 | 11\.0µm | Top of atmosphere brightness temperature at 11\.0µm (CDR variable) |
| `temp_11_0um_clear_sky` | K | \-30853\* | 32767\* | 0\.00244148 | 260 | None | Top of atmosphere brightness temperature modeled assuming clear skies at 11\.0µm |
| `temp_11_0um_stddev_3x3` | K | \-127\* | 127\* | 0\.0787402 | 10\.9 | None | Standard deviation of the 11\.0µm brightness temperature computed over a 3x3 pixel array |
| `temp_12_0um` | K | \-32767\* | 32767\* | 0\.00244148 | 260 | 12\.0µm | Top of atmosphere brightness temperature 12\.0µm (CDR variable) |
| `temp_3_75um` | K | \-32767\* | 32767\* | 0\.00244148 | 260 | 3\.75µm | Top of atmosphere brightness temperature 3\.75µm (CDR variable) |
| `acha_info` | None |  |  | None | ACHA processing information bit flags |
| Bitmask for acha\_info * Bit 0: Cloud height attempted 	+ 0: No 	+ 1: Yes * Bit 1: Bias correction employed 	+ 0: No 	+ 1: Yes * Bit 2: Ice cloud retrieval 	+ 0: No 	+ 1: Yes * Bit 3: Local radiative center processing used 	+ 0: No 	+ 1: Yes * Bit 4: Multi\-layer retrieval 	+ 0: No 	+ 1: Yes * Bit 5: Lower cloud interpolation used 	+ 0: No 	+ 1: Yes * Bit 6: Boundary layer inversion assumed 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `acha_quality` | None |  |  | None | ACHA quality flags |
| Bitmask for acha\_quality * Bit 0: ACHA products processed 	+ 0: No 	+ 1: Yes * Bit 1: Valid Tc retrieval 	+ 0: No 	+ 1: Yes * Bit 2: Valid ec retrieval 	+ 0: No 	+ 1: Yes * Bit 3: Valid beta retrieval 	+ 0: No 	+ 1: Yes * Bit 4: Degraded Tc retrieval 	+ 0: No 	+ 1: Yes * Bit 5: Degraded ec retrieval 	+ 0: No 	+ 1: Yes * Bit 6: Degraded beta retrieval 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `bad_pixel_mask` | None |  |  | None | Mask that distinguishes good from bad pixels |
| Bitmask for bad\_pixel\_mask * Bit 0: Bad pixel mask 	+ 0: Good 	+ 1: Bad | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `cloud_mask` | None |  |  | None | Integer classification of the cloud mask |
| `dcomp_info` | None |  |  | None | Processing flags for DCOMP |
| Bitmask for dcomp\_info * Bit 0: Info flag set 	+ 0: No 	+ 1: Yes * Bit 1: Land/sea mask 	+ 0: Land 	+ 1: Sea * Bit 2: Day/night mask 	+ 0: Day 	+ 1: Night * Bit 3: Twilight (65\-82 solar zenith) 	+ 0: No 	+ 1: Yes * Bit 4: Snow 	+ 0: No 	+ 1: Snow * Bit 5: Sea\-ice 	+ 0: No 	+ 1: Sea\-ice * Bit 6: Phase 	+ 0: Liquid 	+ 1: Ice * Bit 7: Thick cloud 	+ 0: No 	+ 1: Yes * Bit 8: Thin cloud 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `dcomp_quality` | None |  |  | None | DCOMP processing information bit flags |
| Bitmask for dcomp\_quality * Bit 0: DCOMP products processed 	+ 0: No 	+ 1: Yes * Bit 1: Valid COD retrieval 	+ 0: No 	+ 1: Yes * Bit 2: Valid REF retrieval 	+ 0: No 	+ 1: Yes * Bit 3: Degraded COD retrieval 	+ 0: No 	+ 1: Yes * Bit 4: Degraded REF retrieval 	+ 0: No 	+ 1: Yes * Bit 5: Convergency 	+ 0: No 	+ 1: Yes * Bit 6: Glint 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `glint_mask` | None |  |  | None | Glint mask |
| Bitmask for glint\_mask * Bit 0: Glint mask 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value
**cloud\_type Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#73d8ff | Clear |
| 1 | \#73d8ff | Probably clear |
| 2 | \#b1d8dc | Fog |
| 3 | \#030bff | Water |
| 4 | \#0013a1 | Supercooled water |
| 5 | \#05ffa3 | Mixed |
| 6 | \#d5fff9 | Opaque ice |
| 7 | \#ffffff | Cirrus |
| 8 | \#b2b8ff | Overlapping |
| 9 | \#b2b8ff | Overshooting |
| 10 | \#f8c4ff | Unknown |
| 11 | \#d7e9a1 | Dust |
| 12 | \#adadad | Smoke |


**land\_class Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#46ffba | Shallow ocean |
| 1 | \#c09968 | Land |
| 2 | \#eddc66 | Coastline |
| 3 | \#32bc76 | Shallow inland water |
| 4 | \#00b5c8 | Ephemeral water |
| 5 | \#338c91 | Deep inland water |
| 6 | \#0109ff | Moderate ocean |
| 7 | \#010583 | Deep ocean |


**snow\_class Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#000000 | No snow/ice |
| 2 | \#17b0c0 | Sea\-ice |
| 3 | \#ffffff | Snow |


**surface\_type Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#0d00d4 | Water |
| 1 | \#096619 | Evergreen needle |
| 2 | \#096619 | Evergreen broad |
| 3 | \#2ac027 | Deciduous needle |
| 4 | \#2ac027 | Deciduous broad |
| 5 | \#a0c800 | Mixed forest |
| 6 | \#7c6e48 | Woodlands |
| 7 | \#dcca76 | Wooded grass |
| 8 | \#c7ff42 | Closed shrubs |
| 9 | \#c7ff42 | Open shrubs |
| 10 | \#00ff5a | Grasses |
| 11 | \#fff700 | Croplands |
| 12 | \#ffdb77 | Bare |
| 13 | \#9f9f9f | Urban |


**cloud\_mask Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#73d8ff | Clear |
| 1 | \#b1d8dc | Probably clear |
| 2 | \#d0d0d0 | Probably cloudy |
| 3 | \#9d9d9d | Cloudy |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| orbit\_node | STRING | 'ascending' or 'descending' |
| platform | STRING | Name of platform |
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
* For the TOA Reflectances and Brightness Temperatures users must cite:
Andrew K. Heidinger, Michael J. Foster, Andi Walther, Xuepeng Zhao, and
NOAA CDR Program (2014\): NOAA Climate Data Record (CDR) of Reflectance
and Brightness Temperatures from AVHRR Pathfinder Atmospheres \- Extended
(PATMOS\-x), Version 5\.3\. \[indicate subset used]. NOAA National Centers for
Environmental Information.
[doi:10\.7289/V56W982J](https://doi.org/10.7289/V56W982J)
\[access date].
* For the cloud properties users must cite: Andrew K. Heidinger, Michael J.
Foster, Andi Walther, Xuepeng Zhao, and NOAA CDR Program (2014\): NOAA
Climate Data Record (CDR) of Cloud Properties from AVHRR Pathfinder
Atmospheres \- Extended (PATMOS\-x), Version 5\.3\. \[indicate subset used].
NOAA National Centers for Environmental Information.
[doi:10\.7289/V5348HCK](https://doi.org/10.7289/V5348HCK)
\[access date].





### DOIs


* [https://doi.org/10\.7289/V5348HCK](https://doi.org/10.7289/V5348HCK)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CDR/PATMOSX/V53')
.filter(ee.Filter.date('2017-05-01','2017-05-14'));
varcloudEmissivityAndHeight=dataset.select(
['cld_emiss_acha','cld_height_acha','cld_height_uncer_acha']);
Map.setCenter(71.72,52.48,1);
Map.addLayer(cloudEmissivityAndHeight,{},'Cloud Emissivity and Height');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_PATMOSX_V53)


[NOAA CDR PATMOSX: Cloud Properties, Reflectance, and Brightness Temperatures, Version 5\.3](/earth-engine/datasets/catalog/NOAA_CDR_PATMOSX_V53)

This dataset provides high quality Climate Data Record (CDR) of multiple cloud properties along with Advanced Very High Resolution Radiometer (AVHRR) Pathfinder Atmospheres Extended (PATMOS\-x) brightness temperatures and reflectances. These data have been fitted to a 0\.1 x 0\.1 equal angle\-grid with both ascending and descending assets generated daily from …

 NOAA/CDR/PATMOSX/V53,
 atmospheric,avhrr,brightness,cdr,climate,cloud,noaa,optical,reflectance,temperature

1979\-01\-01T00:00:00Z/2022\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7289/V5348HCK](https://doi.org/https://www.ncei.noaa.gov/products/climate-data-records/avhrr-hirs-cloud-properties-patmos)
* [https://doi.org/10\.7289/V5348HCK](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_PATMOSX_V53)









