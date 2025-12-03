



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GEDI L4A Aboveground Biomass Density, Version 2\.1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================








Dataset Availability
2019\-04\-18T00:00:00Z–2024\-11\-28T00:00:00Z
Dataset Provider


[USFS Laboratory for Applications of Remote Sensing in Ecology (LARSE)](https://www.fs.usda.gov/)


[NASA GEDI mission, accessed through the USGS LP DAAC](https://daac.ornl.gov/GEDI/guides/GEDI_L4A_AGB_Density_V2_1.html)




Tags


[elevation](/earth-engine/datasets/tags/elevation)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[gedi](/earth-engine/datasets/tags/gedi)
[larse](/earth-engine/datasets/tags/larse)
[nasa](/earth-engine/datasets/tags/nasa)
[tree\-cover](/earth-engine/datasets/tags/tree-cover)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



This dataset contains Global Ecosystem Dynamics Investigation (GEDI)
Level 4A (L4A) Version 2 predictions of the aboveground biomass
density (AGBD; in Mg/ha) and estimates of the prediction standard
error within each sampled geolocated laser footprint. In this version,
the granules are in sub\-orbits.
Height metrics from simulated waveforms associated with field estimates
of AGBD from multiple regions and plant functional types (PFTs) were
compiled to generate a calibration dataset for models representing
the combinations of world regions and PFTs (i.e., deciduous broadleaf
trees, evergreen broadleaf trees, evergreen needleleaf trees, deciduous
needleleaf trees, and the combination of grasslands, shrubs, and
woodlands).The algorithm setting group selection
used for GEDI02\_A Version 2 has been modified for evergreen broadleaf
trees in South America to reduce false positive errors resulting from
the selection of waveform modes above ground elevation as the lowest mode.


Please see [User Guide](https://daac.ornl.gov/GEDI/guides/GEDI_L4A_AGB_Density_V2_1.html)
for more information.


The Global Ecosystem Dynamics Investigation [GEDI](https://gedi.umd.edu/)
mission aims to characterize ecosystem structure and dynamics to enable
radically improved quantification and understanding of the Earth's carbon cycle
and biodiversity. The GEDI instrument, attached to the International Space
Station (ISS), collects data globally between 51\.6° N and 51\.6° S
latitudes at the highest resolution and densest sampling of the
3\-dimensional structure of the Earth. The GEDI instrument consists of three
lasers producing a total of eight beam ground transects, which instantaneously
sample eight \~25 m footprints spaced approximately every 60 m along\-track.




| Product | Description |
| --- | --- |
| L2A Vector | [LARSE/GEDI/GEDI02\_A\_002](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_A_002) |
| L2A Monthly raster | [LARSE/GEDI/GEDI02\_A\_002\_MONTHLY](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_A_002_MONTHLY) |
| L2A table index | [LARSE/GEDI/GEDI02\_A\_002\_INDEX](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_A_002_INDEX) |
| L2B Vector | [LARSE/GEDI/GEDI02\_B\_002](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_B_002) |
| L2B Monthly raster | [LARSE/GEDI/GEDI02\_B\_002\_MONTHLY](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_B_002_MONTHLY) |
| L2B table index | [LARSE/GEDI/GEDI02\_B\_002\_INDEX](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_B_002_INDEX) |
| L4A Biomass Vector | [LARSE/GEDI/GEDI04\_A\_002](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002) |
| L4A Monthly raster | [LARSE/GEDI/GEDI04\_A\_002\_MONTHLY](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002_MONTHLY) |
| L4A table index | [LARSE/GEDI/GEDI04\_A\_002\_INDEX](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002_INDEX) |
| L4B Biomass | [LARSE/GEDI/GEDI04\_B\_002](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_B_002) |





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| agbd | INT | Predicted aboveground biomass density |
| agbd\_pi\_lower | INT | Lower prediction interval (see "alpha" attribute for the level) |
| agbd\_pi\_upper | INT | Upper prediction interval (see "alpha" attribute for the level) |
| agbd\_se | INT | Aboveground biomass density prediction standard error |
| agbd\_t | INT | Model prediction in fit units |
| agbd\_t\_se | INT | Model prediction standard error in fit units (needed for calculation of custom prediction intervals) |
| algorithm\_run\_flag | INT | The L4A algorithm is run if this flag is set to 1\. This flag selects data that have sufficient waveform fidelity for AGBD estimation. |
| beam | INT | Beam identifier |
| channel | INT | Channel identifier |
| degrade\_flag | INT | Flag indicating degraded state of pointing and/or positioning information |
| delta\_time | INT | Time since Jan 1 00:00 2018 |
| elev\_lowestmode | INT | Elevation of center of lowest mode relative to reference ellipsoid |
| l2\_quality\_flag | INT | Flag identifying the most useful L2 data for biomass predictions |
| l4\_quality\_flag | INT | Flag simplifying selection of most useful biomass predictions |
| lat\_lowestmode | INT | Latitude of center of lowest mode |
| lon\_lowestmode | INT | Longitude of center of lowest mode |
| master\_frac | INT | Master time, fractional part. master\_int\+master\_frac is equivalent to /BEAMXXXX/delta\_time |
| master\_int | INT | Master time, integer part. Seconds since master\_time\_epoch. master\_int\+master\_frac is equivalent to /BEAMXXXX/delta\_time', |
| predict\_stratum | STRING | Prediction stratum identifier. Character ID of the prediction stratum name for the 1 km cell |
| predictor\_limit\_flag | INT | Predictor value is outside the bounds of the training data (0\=in bounds; 1\=lower bound; 2\=upper bound) |
| response\_limit\_flag | INT | Prediction value is outside the bounds of the training data (0\=in bounds; 1\=lower bound; 2\=upper bound) |
| selected\_algorithm | INT | Selected algorithm setting group |
| selected\_mode | INT | ID of mode selected as lowest non\-noise mode |
| selected\_mode\_flag | INT | Flag indicating status of selected\_mode |
| sensitivity | INT | Beam sensitivity. Maximum canopy cover that can be penetrated considering the SNR of the waveform |
| solar\_elevation | INT | Solar elevation angle |
| surface\_flag | INT | Indicates elev\_lowestmode is within 300m of Digital Elevation Model (DEM) or Mean Sea Surface (MSS) elevation |
| shot\_number | STRING | Shot number, a unique identifier. This field has the format of OOOOOBBRRGNNNNNNNN, where:* OOOOO: Orbit number * BB: Beam number * RR: Reserved for future use * G: Sub\-orbit granule number * NNNNNNNN: Shot index |
| shot\_number\_within\_beam | INT | Shot number within beam |
| agbd\_aN | INT | Above ground biomass density; Geolocation latitude lowestmode |
| agbd\_pi\_lower\_aN | INT | Above ground biomass density lower prediction interval |
| agbd\_pi\_upper\_aN | INT | Above ground biomass density upper prediction interval |
| agbd\_se\_aN | INT | Aboveground biomass density prediction standard error |
| agbd\_t\_aN | INT | Aboveground biomass density model prediction in transform space |
| agbd\_t\_pi\_lower\_aN | INT | Lower prediction interval in transform space |
| agbd\_t\_pi\_upper\_aN | INT | Upper prediction interval in transform space |
| agbd\_t\_se\_aN | INT | Model prediction standard error in fit units |
| algorithm\_run\_flag\_aN | INT | Algorithm run flag\-this algorithm is run if this flag is set to 1\. This flag selects data that have sufficient waveform fidelity for AGBD estimation |
| l2\_quality\_flag\_aN | INT | Flag identifying the most useful L2 data for biomass predictions' |
| l4\_quality\_flag\_aN | INT | Flag simplifying selection of most useful biomass predictions |
| predictor\_limit\_flag\_aN | INT | Predictor value is outside the bounds of the training data |
| response\_limit\_flag\_aN | INT | Prediction value is outside the bounds of the training data |
| selected\_mode\_aN | INT | ID of mode selected as lowest non\-noise mode |
| selected\_mode\_flag\_aN | INT | Flag indicating status of selected mode |
| elev\_lowestmode\_aN | INT | Elevation of center of lowest mode relative to the reference ellipsoid |
| lat\_lowestmode\_aN | INT | Latitude of center of lowest mode |
| lon\_lowestmode\_aN | INT | Longitude of center of lowest mode |
| sensitivity\_aN | INT | Maximum canopy cover that can be penetrated considering the SNR of the waveform |
| stale\_return\_flag | INT | Flag from digitizer indicating the real\-time pulse detection algorithm did not detect a return signal above its detection threshold within the entire 10 km search window. The pulse location of the previous shot was used to select the telemetered waveform. |
| landsat\_treecover | INT | Tree cover in the year 2010, defined as canopy closure for all vegetation taller than 5 m in height (Hansen et al., 2013\) and encoded as a percentage per output grid cell. |
| landsat\_water\_persistence | INT | The percent UMD GLAD Landsat observations with classified surface water between 2018 and 2019\. Values \>80 usually represent permanent water while values \<10 represent permanent land. |
| leaf\_off\_doy | INT | GEDI 1 km EASE 2\.0 grid leaf\-off start day\-of\-year derived from the NPP VIIRS Global Land Surface Phenology Product. |
| leaf\_off\_flag | INT | GEDI 1 km EASE 2\.0 grid flag derived from leaf\_off\_doy, leaf\_on\_doy, and pft\_class, indicating if the observation was recorded during leaf\-off conditions in deciduous needleleaf or broadleaf forests and woodlands. 1\=leaf\-off, 0\=leaf\-on. |
| leaf\_on\_cycle | INT | Flag that indicates the vegetation growing cycle for leaf\-on observations. Values are 0\=leaf\-off conditions, 1\=cycle 1, 2\=cycle 2\. |
| leaf\_on\_doy | INT | GEDI 1 km EASE 2\.0 grid leaf\-on start day\- of\-year derived from the NPP VIIRS Global Land Surface Phenology product. |
| pft\_class | INT | GEDI 1 km EASE 2\.0 grid Plant Functional Type (PFT) derived from the MODIS MCD12Q1v006 product. Values follow the Land Cover Type 5 Classification scheme. |
| region\_class | INT | GEDI 1 km EASE 2\.0 grid world continental regions (0\=Water, 1\=Europe, 2\=North Asia, 3\=Australasia, 4\=Africa, 5\=South Asia, 6\=South America, 7\=North America). |
| urban\_focal\_window\_size | INT | The focal window size used to calculate urban\_proportion. Values are 3 (3x3 pixel window size) or 5 (5x5 pixel window size). |
| urban\_proportion | INT | The percentage proportion of land area within a focal area surrounding each shot that is urban land cover. Urban land cover was derived from the DLR 12 m resolution TanDEM\-X Global Urban Footprint Product. |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* GEDI L4A Footprint Level Aboveground Biomass Density, Version 2\.1\.
Dubayah, R.O., J. Armston, J.R. Kellner, L. Duncanson, S.P. Healey,
P.L. Patterson, S. Hancock, H. Tang, J. Bruening, M.A. Hofton, J.B. Blair,
and S.B. Luthcke. 2022\. ORNL DAAC, Oak Ridge, Tennessee, USA.
[doi:10\.3334/ORNLDAAC/2056](https://doi.org/10.3334/ORNLDAAC/2056)





### DOIs


* [https://doi.org/10\.5067/GEDI/GEDI04\_A.002](https://doi.org/10.5067/GEDI/GEDI04_A.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection(
'LARSE/GEDI/GEDI04_A_002/GEDI04_A_2022157233128_O19728_03_T11129_02_003_01_V002');
Map.setCenter(-94.77616,38.9587,14);
Map.addLayer(dataset);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI04_A_002)


[GEDI L4A Aboveground Biomass Density, Version 2\.1](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002)

This dataset contains Global Ecosystem Dynamics Investigation (GEDI) Level 4A (L4A) Version 2 predictions of the aboveground biomass density (AGBD; in Mg/ha) and estimates of the prediction standard error within each sampled geolocated laser footprint. In this version, the granules are in sub\-orbits. Height metrics from simulated waveforms associated with …

 LARSE/GEDI/GEDI04\_A\_002,
 elevation,forest\-biomass,gedi,larse,nasa,tree\-cover,usgs

2019\-04\-18T00:00:00Z/2024\-11\-28T00:00:00Z



 \-51\.6 \-180 51\.6 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/GEDI/GEDI04\_A.002](https://doi.org/https://www.fs.usda.gov/)
* [https://doi.org/10\.5067/GEDI/GEDI04\_A.002](https://doi.org/https://daac.ornl.gov/GEDI/guides/GEDI_L4A_AGB_Density_V2_1.html)
* [https://doi.org/10\.5067/GEDI/GEDI04\_A.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002)









