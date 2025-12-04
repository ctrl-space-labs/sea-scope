



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GEDI L4A Raster Aboveground Biomass Density, Version 2\.1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================================================








Dataset Availability
2019\-03\-25T00:00:00Z–2024\-11\-01T08:00:00Z
Dataset Provider


[Rasterization: Google and USFS Laboratory for Applications of Remote Sensing in Ecology (LARSE)](https://www.fs.usda.gov/)


[NASA GEDI mission, accessed through the USGS LP DAAC](https://daac.ornl.gov/GEDI/guides/GEDI_L4A_AGB_Density_V2_1.html)



Earth Engine Snippet


`ee.ImageCollection("LARSE/GEDI/GEDI04_A_002_MONTHLY")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI04_A_002_MONTHLY)





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
The dataset LARSE/GEDI/GEDI04\_A\_002\_MONTHLY is a raster version
of the original GEDI04\_A product. The raster images are organized as monthly
composites of individual orbits in the corresponding month.


See [User Guide](https://daac.ornl.gov/GEDI/guides/GEDI_L4A_AGB_Density_V2_1.html)
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





### Bands



**Pixel Size**
  
25 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `agbd` | Mg/ha | Predicted aboveground biomass density |
| `agbd_pi_lower` | Mg/ha | Lower prediction interval (see "alpha" attribute for the level) |
| `agbd_pi_upper` | Mg/ha | Upper prediction interval (see "alpha" attribute for the level) |
| `agbd_se` | Mg/ha | Aboveground biomass density prediction standard error |
| `agbd_t` | None | Model prediction in fit units |
| `agbd_t_se` | None | Model prediction standard error in fit units (needed for calculation of custom prediction intervals) |
| `algorithm_run_flag` | None | The L4A algorithm is run if this flag is set to 1\. This flag selects data that have sufficient waveform fidelity for AGBD estimation. |
| `beam` | None | Beam identifier |
| `channel` | None | Channel identifier |
| `degrade_flag` | None | Flag indicating degraded state of pointing and/or positioning information |
| `delta_time` | seconds | Time since Jan 1 00:00 2018 |
| `elev_lowestmode` | m | Elevation of center of lowest mode relative to reference ellipsoid |
| `l2_quality_flag` | None | Flag identifying the most useful L2 data for biomass predictions |
| `l4_quality_flag` | None | Flag simplifying selection of most useful biomass predictions |
| `lat_lowestmode` | deg | Latitude of center of lowest mode |
| `lon_lowestmode` | deg | Longitude of center of lowest mode |
| `master_frac` | seconds | Master time, fractional part. master\_int\+master\_frac is equivalent to /BEAMXXXX/delta\_time |
| `master_int` | seconds | Master time, integer part. Seconds since master\_time\_epoch. master\_int\+master\_frac is equivalent to /BEAMXXXX/delta\_time', |
| `predict_stratum` | None | Prediction stratum identifier. Character ID of the prediction stratum name for the 1 km cell |
| `predictor_limit_flag` | None | Predictor value is outside the bounds of the training data (0\=in bounds; 1\=lower bound; 2\=upper bound) |
| `response_limit_flag` | None | Prediction value is outside the bounds of the training data (0\=in bounds; 1\=lower bound; 2\=upper bound) |
| `selected_algorithm` | None | Selected algorithm setting group |
| `selected_mode` | None | ID of mode selected as lowest non\-noise mode |
| `selected_mode_flag` | None | Flag indicating status of selected\_mode |
| `sensitivity` | None | Beam sensitivity. Maximum canopy cover that can be penetrated considering the SNR of the waveform |
| `solar_elevation` | deg | Solar elevation angle |
| `surface_flag` | None | Indicates elev\_lowestmode is within 300m of Digital Elevation Model (DEM) or Mean Sea Surface (MSS) elevation |
| `shot_number` | None | Shot number, a unique identifier. This field has the format of OOOOOBBRRGNNNNNNNN, where:* OOOOO: Orbit number * BB: Beam number * RR: Reserved for future use * G: Sub\-orbit granule number * NNNNNNNN: Shot index |
| `shot_number_within_beam` | None | Shot number within beam |
| `agbd_aN` | Mg/ha | Above ground biomass density; Geolocation latitude lowestmode |
| `agbd_pi_lower_aN` | Mg/ha | Above ground biomass density lower prediction interval |
| `agbd_pi_upper_aN` | Mg/ha | Above ground biomass density upper prediction interval |
| `agbd_se_aN` | Mg/ha | Aboveground biomass density prediction standard error |
| `agbd_t_aN` | Mg/ha | Aboveground biomass density model prediction in transform space |
| `agbd_t_pi_lower_aN` | Mg/ha | Lower prediction interval in transform space |
| `agbd_t_pi_upper_aN` | Mg/ha | Upper prediction interval in transform space |
| `agbd_t_se_aN` | None | Model prediction standard error in fit units |
| `algorithm_run_flag_aN` | None | Algorithm run flag\-this algorithm is run if this flag is set to 1\. This flag selects data that have sufficient waveform fidelity for AGBD estimation |
| `l2_quality_flag_aN` | None | Flag identifying the most useful L2 data for biomass predictions' |
| `l4_quality_flag_aN` | None | Flag simplifying selection of most useful biomass predictions |
| `predictor_limit_flag_aN` | None | Predictor value is outside the bounds of the training data |
| `response_limit_flag_aN` | None | Prediction value is outside the bounds of the training data |
| `selected_mode_aN` | None | ID of mode selected as lowest non\-noise mode |
| `selected_mode_flag_aN` | None | Flag indicating status of selected mode |
| `elev_lowestmode_aN` | m | Elevation of center of lowest mode relative to the reference ellipsoid |
| `lat_lowestmode_aN` | deg | Latitude of center of lowest mode |
| `lon_lowestmode_aN` | deg | Longitude of center of lowest mode |
| `sensitivity_aN` | None | Maximum canopy cover that can be penetrated considering the SNR of the waveform |
| `stale_return_flag` | None | Flag from digitizer indicating the real\-time pulse detection algorithm did not detect a return signal above its detection threshold within the entire 10 km search window. The pulse location of the previous shot was used to select the telemetered waveform. |
| `landsat_treecover` | % | Tree cover in the year 2010, defined as canopy closure for all vegetation taller than 5 m in height (Hansen et al., 2013\) and encoded as a percentage per output grid cell. |
| `landsat_water_persistence` | % | The percent UMD GLAD Landsat observations with classified surface water between 2018 and 2019\. Values \>80 usually represent permanent water while values \<10 represent permanent land. |
| `leaf_off_doy` | None | GEDI 1 km EASE 2\.0 grid leaf\-off start day\-of\-year derived from the NPP VIIRS Global Land Surface Phenology Product. |
| `leaf_off_flag` | None | GEDI 1 km EASE 2\.0 grid flag derived from leaf\_off\_doy, leaf\_on\_doy, and pft\_class, indicating if the observation was recorded during leaf\-off conditions in deciduous needleleaf or broadleaf forests and woodlands. 1\=leaf\-off, 0\=leaf\-on. |
| `leaf_on_cycle` | None | Flag that indicates the vegetation growing cycle for leaf\-on observations. Values are 0\=leaf\-off conditions, 1\=cycle 1, 2\=cycle 2\. |
| `leaf_on_doy` | None | GEDI 1 km EASE 2\.0 grid leaf\-on start day\- of\-year derived from the NPP VIIRS Global Land Surface Phenology product. |
| `pft_class` | None | GEDI 1 km EASE 2\.0 grid Plant Functional Type (PFT) derived from the MODIS MCD12Q1v006 product. Values follow the Land Cover Type 5 Classification scheme. |
| `region_class` | None | GEDI 1 km EASE 2\.0 grid world continental regions (0\=Water, 1\=Europe, 2\=North Asia, 3\=Australasia, 4\=Africa, 5\=South Asia, 6\=South America, 7\=North America). |
| `urban_focal_window_size` | pixel | The focal window size used to calculate urban\_proportion. Values are 3 (3x3 pixel window size) or 5 (5x5 pixel window size). |
| `urban_proportion` | % | The percentage proportion of land area within a focal area surrounding each shot that is urban land cover. Urban land cover was derived from the DLR 12 m resolution TanDEM\-X Global Urban Footprint Product. |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varqualityMask=function(im){
returnim.updateMask(im.select('l4_quality_flag').eq(1))
.updateMask(im.select('degrade_flag').eq(0));
};
vardataset=ee.ImageCollection('LARSE/GEDI/GEDI04_A_002_MONTHLY')
.map(qualityMask)
.select('solar_elevation');

vargediVis={
min:1,
max:60,
palette:'red, green, blue',
};
Map.setCenter(5.0198,51.7564,12);
Map.addLayer(dataset,gediVis,'Solar Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI04_A_002_MONTHLY)


[GEDI L4A Raster Aboveground Biomass Density, Version 2\.1](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002_MONTHLY)

This dataset contains Global Ecosystem Dynamics Investigation (GEDI) Level 4A (L4A) Version 2 predictions of the aboveground biomass density (AGBD; in Mg/ha) and estimates of the prediction standard error within each sampled geolocated laser footprint. In this version, the granules are in sub\-orbits. Height metrics from simulated waveforms associated with …

 LARSE/GEDI/GEDI04\_A\_002\_MONTHLY,
 elevation,forest\-biomass,gedi,larse,nasa,tree\-cover,usgs

2019\-03\-25T00:00:00Z/2024\-11\-01T08:00:00Z



 \-51\.6 \-180 51\.6 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








