



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GEDI L2A Raster Canopy Top Height (Version 2\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================








Dataset Availability
2019\-03\-25T00:00:00Z–2024\-11\-01T08:00:00Z
Dataset Provider


[Rasterization: Google and USFS Laboratory for Applications of Remote Sensing in Ecology (LARSE)](https://www.fs.usda.gov/)


[NASA GEDI mission, accessed through the USGS LP DAAC](https://lpdaac.usgs.gov/products/gedi02_av002/)



Earth Engine Snippet


`ee.ImageCollection("LARSE/GEDI/GEDI02_A_002_MONTHLY")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI02_A_002_MONTHLY)





Tags


[elevation](/earth-engine/datasets/tags/elevation)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[gedi](/earth-engine/datasets/tags/gedi)
[larse](/earth-engine/datasets/tags/larse)
[nasa](/earth-engine/datasets/tags/nasa)
[tree\-cover](/earth-engine/datasets/tags/tree-cover)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



GEDI's Level 2A Geolocated Elevation and Height Metrics Product (GEDI02\_A)
is primarily composed of 100 Relative Height (RH) metrics, which
collectively describe the waveform collected by GEDI.


The original GEDI02\_A product is a table of point with a spatial resolution
(average footprint) of 25 meters.
The dataset LARSE/GEDI/GEDI02\_A\_002\_MONTHLY is a raster version
of the original GEDI02\_A product. The raster images are organized as monthly
composites of individual orbits in the corresponding month. Only root\-level
RH values and their associated quality flags and metadata are preserved
as raster bands. Each GEDI02\_A\_002 raster has 136 bands.


See [User Guide](https://lpdaac.usgs.gov/documents/986/GEDI02_UserGuide_V2.pdf)
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




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `beam` | None | 0 | 12 | Beam identifier |
| `degrade_flag` | None | 0 | 99 | Flag indicating degraded state of pointing and/or positioning information.* 3X \- ADF CHU solution unavailable (ST\-2\) * 4X \- Platform attitude * 5X \- Poor solution (filter covariance large) * 6X \- Data outage (platform attitude gap also) * 7X \- ST 1\+2 unavailable (similar boresight FOV) * 8X \- ST 1\+2\+3 unavailable * 9X \- ST 1\+2\+3 and ISS unavailable * X1 \- Maneuver * X2 \- GPS data gap * X3 \- ST blinding * X4 \- Other * X5 \- GPS receiver clock drift * X6 \- Maneuver \& GPS receiver clock drift * X7 \- GPS data gap \& GPS receiver clock drift * X8 \- ST blinding \& GPS receiver clock drift * X9 \- Other \& GPS receiver clock drift |
| `delta_time` | seconds | Time delta since Jan 1 00:00 2018 |
| `digital_elevation_model` | m | TanDEM\-X elevation at GEDI footprint location |
| `digital_elevation_model_srtm` | m | SRTM elevation at GEDI footprint location |
| `elev_highestreturn` | m | \-1000 | 25000 | Elevation of highest detected return relative to reference ellipsoid |
| `elev_lowestmode` | m | \-1000 | 25000 | Elevation of center of lowest mode relative to reference ellipsoid |
| `elevation_bias_flag` | None | 0 | 1 | Elevations potentially affected by 4bin (\~60 cm) ranging error |
| `energy_total` | None | \-5000 | 5e\+06 | Integrated counts in the return waveform relative to the mean noise level |
| `landsat_treecover` | % | Tree cover in the year 2010, defined as canopy closure for all vegetation taller than 5 m in height as a percentage per output grid cell |
| `landsat_water_persistence` | None | 0 | 100 | Percent UMD GLAD Landsat observations with classified surface water |
| `lat_highestreturn` | deg | \-55 | 55 | Latitude of highest detected return |
| `leaf_off_doy` | None | 1 | 365 | GEDI 1 km EASE 2\.0 grid leaf\-off start day\-of\-year |
| `leaf_off_flag` | None | 0 | 1 | GEDI 1 km EASE 2\.0 grid flag |
| `leaf_on_cycle` | None | 1 | 2 | Flag that indicates the vegetation growing cycle for leaf\-on observations |
| `leaf_on_doy` | None | 1 | 365 | GEDI 1 km EASE 2\.0 grid leaf\-on start day\-of\-year |
| `lon_highestreturn` | deg | \-180 | 180 | Longitude of highest detected return |
| `modis_nonvegetated` | % | Percent non\-vegetated from MODIS MOD44B V6 data |
| `modis_nonvegetated_sd` | % | Percent non\-vegetated standard deviation from MODIS MOD44B V6 data |
| `modis_treecover` | % | Percent tree cover from MODIS MOD44B V6 data |
| `modis_treecover_sd` | % | Percent tree cover standard deviation from MODIS MOD44B V6 data |
| `num_detectedmodes` | None | 0 | 20 | Number of detected modes in rxwaveform |
| `pft_class` | None | 0 | 11 | GEDI 1 km EASE 2\.0 grid Plant Functional Type (PFT) |
| `quality_flag` | None | 0 | 1 | Flag indicating likely invalid waveform (1\=valid, 0\=invalid) |
| `region_class` | None | 0 | 7 | GEDI 1 km EASE 2\.0 grid world continental regions |
| `selected_algorithm` | None | 1 | 6 | Identifier of algorithm selected as identifying the lowest non\-noise mode |
| `selected_mode` | None | 0 | 20 | Identifier of mode selected as lowest non\-noise mode |
| `selected_mode_flag` | None | 0 | 1 | Flag indicating status of selected\_mode |
| `sensitivity` | None | 0 | 1 | Maxmimum canopy cover that can be penetrated. Valid range is \[0, 1]. Values outside of this range may be present but must be ignored. They represent noise and non\-land surface waveforms. |
| `solar_azimuth` | None | The azimuth of the sun position vector from the laser bounce point position in the local ENU frame. The angle is measured from North and is positive towards East. |
| `solar_elevation` | None | The elevation of the sun position vector from the laser bounce point position in the local ENU frame. The angle is measured from the East\-North plane and is positive Up. |
| `surface_flag` | None | 0 | 1 | Indicates elev\_lowestmode is within 300m of Digital Elevation Model (DEM) or Mean Sea Surface (MSS) elevation |
| `urban_focal_window_size` | pixel | 3 | 5 | The focal window size used to calculate urban\_proportion. Values are 3 (3x3 pixel window size) or 5 (5x5 pixel window size). |
| `urban_proportion` | None | 0 | 100 | The percentage proportion of land area within a focal area surrounding each shot that is urban land cover. |
| `orbit_number` | None | Orbit number |
| `minor_frame_number` | None | Minor frame number 0\-241() |
| `shot_number_within_beam` | None | Shot number within beam |
| `local_beam_azimuth` | rad | Azimuth in radians of the unit pointing vector for the laser in the local ENU frame. The angle is measured from North and positive towards East. |
| `local_beam_elevation` | rad | Elevation in radians of the unit pointing vector for the laser in the local ENU frame. The angle is measured from North and positive towards East. |
| `rh0` | m | \-213 | 213 | Relative height metrics at 0% |
| `rh1` | m | \-213 | 213 | Relative height metrics at 1% |
| `rh2` | m | \-213 | 213 | Relative height metrics at 2% |
| `rh3` | m | \-213 | 213 | Relative height metrics at 3% |
| `rh4` | m | \-213 | 213 | Relative height metrics at 4% |
| `rh5` | m | \-213 | 213 | Relative height metrics at 5% |
| `rh6` | m | \-213 | 213 | Relative height metrics at 6% |
| `rh7` | m | \-213 | 213 | Relative height metrics at 7% |
| `rh8` | m | \-213 | 213 | Relative height metrics at 8% |
| `rh9` | m | \-213 | 213 | Relative height metrics at 9% |
| `rh10` | m | \-213 | 213 | Relative height metrics at 10% |
| `rh11` | m | \-213 | 213 | Relative height metrics at 11% |
| `rh12` | m | \-213 | 213 | Relative height metrics at 12% |
| `rh13` | m | \-213 | 213 | Relative height metrics at 13% |
| `rh14` | m | \-213 | 213 | Relative height metrics at 14% |
| `rh15` | m | \-213 | 213 | Relative height metrics at 15% |
| `rh16` | m | \-213 | 213 | Relative height metrics at 16% |
| `rh17` | m | \-213 | 213 | Relative height metrics at 17% |
| `rh18` | m | \-213 | 213 | Relative height metrics at 18% |
| `rh19` | m | \-213 | 213 | Relative height metrics at 19% |
| `rh20` | m | \-213 | 213 | Relative height metrics at 20% |
| `rh21` | m | \-213 | 213 | Relative height metrics at 21% |
| `rh22` | m | \-213 | 213 | Relative height metrics at 22% |
| `rh23` | m | \-213 | 213 | Relative height metrics at 23% |
| `rh24` | m | \-213 | 213 | Relative height metrics at 24% |
| `rh25` | m | \-213 | 213 | Relative height metrics at 25% |
| `rh26` | m | \-213 | 213 | Relative height metrics at 26% |
| `rh27` | m | \-213 | 213 | Relative height metrics at 27% |
| `rh28` | m | \-213 | 213 | Relative height metrics at 28% |
| `rh29` | m | \-213 | 213 | Relative height metrics at 29% |
| `rh30` | m | \-213 | 213 | Relative height metrics at 30% |
| `rh31` | m | \-213 | 213 | Relative height metrics at 31% |
| `rh32` | m | \-213 | 213 | Relative height metrics at 32% |
| `rh33` | m | \-213 | 213 | Relative height metrics at 33% |
| `rh34` | m | \-213 | 213 | Relative height metrics at 34% |
| `rh35` | m | \-213 | 213 | Relative height metrics at 35% |
| `rh36` | m | \-213 | 213 | Relative height metrics at 36% |
| `rh37` | m | \-213 | 213 | Relative height metrics at 37% |
| `rh38` | m | \-213 | 213 | Relative height metrics at 38% |
| `rh39` | m | \-213 | 213 | Relative height metrics at 39% |
| `rh40` | m | \-213 | 213 | Relative height metrics at 40% |
| `rh41` | m | \-213 | 213 | Relative height metrics at 41% |
| `rh42` | m | \-213 | 213 | Relative height metrics at 42% |
| `rh43` | m | \-213 | 213 | Relative height metrics at 43% |
| `rh44` | m | \-213 | 213 | Relative height metrics at 44% |
| `rh45` | m | \-213 | 213 | Relative height metrics at 45% |
| `rh46` | m | \-213 | 213 | Relative height metrics at 46% |
| `rh47` | m | \-213 | 213 | Relative height metrics at 47% |
| `rh48` | m | \-213 | 213 | Relative height metrics at 48% |
| `rh49` | m | \-213 | 213 | Relative height metrics at 49% |
| `rh50` | m | \-213 | 213 | Relative height metrics at 50% |
| `rh51` | m | \-213 | 213 | Relative height metrics at 51% |
| `rh52` | m | \-213 | 213 | Relative height metrics at 52% |
| `rh53` | m | \-213 | 213 | Relative height metrics at 53% |
| `rh54` | m | \-213 | 213 | Relative height metrics at 54% |
| `rh55` | m | \-213 | 213 | Relative height metrics at 55% |
| `rh56` | m | \-213 | 213 | Relative height metrics at 56% |
| `rh57` | m | \-213 | 213 | Relative height metrics at 57% |
| `rh58` | m | \-213 | 213 | Relative height metrics at 58% |
| `rh59` | m | \-213 | 213 | Relative height metrics at 59% |
| `rh60` | m | \-213 | 213 | Relative height metrics at 60% |
| `rh61` | m | \-213 | 213 | Relative height metrics at 61% |
| `rh62` | m | \-213 | 213 | Relative height metrics at 62% |
| `rh63` | m | \-213 | 213 | Relative height metrics at 63% |
| `rh64` | m | \-213 | 213 | Relative height metrics at 64% |
| `rh65` | m | \-213 | 213 | Relative height metrics at 65% |
| `rh66` | m | \-213 | 213 | Relative height metrics at 66% |
| `rh67` | m | \-213 | 213 | Relative height metrics at 67% |
| `rh68` | m | \-213 | 213 | Relative height metrics at 68% |
| `rh69` | m | \-213 | 213 | Relative height metrics at 69% |
| `rh70` | m | \-213 | 213 | Relative height metrics at 70% |
| `rh71` | m | \-213 | 213 | Relative height metrics at 71% |
| `rh72` | m | \-213 | 213 | Relative height metrics at 72% |
| `rh73` | m | \-213 | 213 | Relative height metrics at 73% |
| `rh74` | m | \-213 | 213 | Relative height metrics at 74% |
| `rh75` | m | \-213 | 213 | Relative height metrics at 75% |
| `rh76` | m | \-213 | 213 | Relative height metrics at 76% |
| `rh77` | m | \-213 | 213 | Relative height metrics at 77% |
| `rh78` | m | \-213 | 213 | Relative height metrics at 78% |
| `rh79` | m | \-213 | 213 | Relative height metrics at 79% |
| `rh80` | m | \-213 | 213 | Relative height metrics at 80% |
| `rh81` | m | \-213 | 213 | Relative height metrics at 81% |
| `rh82` | m | \-213 | 213 | Relative height metrics at 82% |
| `rh83` | m | \-213 | 213 | Relative height metrics at 83% |
| `rh84` | m | \-213 | 213 | Relative height metrics at 84% |
| `rh85` | m | \-213 | 213 | Relative height metrics at 85% |
| `rh86` | m | \-213 | 213 | Relative height metrics at 86% |
| `rh87` | m | \-213 | 213 | Relative height metrics at 87% |
| `rh88` | m | \-213 | 213 | Relative height metrics at 88% |
| `rh89` | m | \-213 | 213 | Relative height metrics at 89% |
| `rh90` | m | \-213 | 213 | Relative height metrics at 90% |
| `rh91` | m | \-213 | 213 | Relative height metrics at 91% |
| `rh92` | m | \-213 | 213 | Relative height metrics at 92% |
| `rh93` | m | \-213 | 213 | Relative height metrics at 93% |
| `rh94` | m | \-213 | 213 | Relative height metrics at 94% |
| `rh95` | m | \-213 | 213 | Relative height metrics at 95% |
| `rh96` | m | \-213 | 213 | Relative height metrics at 96% |
| `rh97` | m | \-213 | 213 | Relative height metrics at 97% |
| `rh98` | m | \-213 | 213 | Relative height metrics at 98% |
| `rh99` | m | \-213 | 213 | Relative height metrics at 99% |
| `rh100` | m | \-213 | 213 | Relative height metrics at 100% |




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
returnim.updateMask(im.select('quality_flag').eq(1))
.updateMask(im.select('degrade_flag').eq(0));
};
vardataset=ee.ImageCollection('LARSE/GEDI/GEDI02_A_002_MONTHLY')
.map(qualityMask)
.select('rh98');

vargediVis={
min:1,
max:60,
palette:'darkred,red,orange,green,darkgreen',
};
Map.setCenter(-74.803466,-9.342209,10);
Map.addLayer(dataset,gediVis,'rh98');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI02_A_002_MONTHLY)


[GEDI L2A Raster Canopy Top Height (Version 2\)](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_A_002_MONTHLY)

GEDI's Level 2A Geolocated Elevation and Height Metrics Product (GEDI02\_A) is primarily composed of 100 Relative Height (RH) metrics, which collectively describe the waveform collected by GEDI. The original GEDI02\_A product is a table of point with a spatial resolution (average footprint) of 25 meters. The dataset LARSE/GEDI/GEDI02\_A\_002\_MONTHLY is a …

 LARSE/GEDI/GEDI02\_A\_002\_MONTHLY,
 elevation,forest\-biomass,gedi,larse,nasa,tree\-cover,usgs

2019\-03\-25T00:00:00Z/2024\-11\-01T08:00:00Z



 \-51\.6 \-180 51\.6 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








