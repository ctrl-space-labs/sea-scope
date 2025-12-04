



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GEDI L2B Raster Canopy Cover Vertical Profile Metrics (Version 2\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================================








Dataset Availability
2019\-03\-25T00:00:00Z–2024\-11\-01T08:00:00Z
Dataset Provider


[Rasterization: Google and USFS Laboratory for Applications of Remote Sensing in Ecology (LARSE)](https://www.fs.usda.gov/)


[NASA GEDI mission, accessed through the USGS LP DAAC](https://lpdaac.usgs.gov/products/gedi02_av002/)



Earth Engine Snippet


`ee.ImageCollection("LARSE/GEDI/GEDI02_B_002_MONTHLY")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI02_B_002_MONTHLY)





Tags


[elevation](/earth-engine/datasets/tags/elevation)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[gedi](/earth-engine/datasets/tags/gedi)
[larse](/earth-engine/datasets/tags/larse)
[nasa](/earth-engine/datasets/tags/nasa)
[tree\-cover](/earth-engine/datasets/tags/tree-cover)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



GEDI Level 2B Canopy Cover and Vertical Profile Metrics product (GEDI02\_B)
extracts biophysical metrics from each GEDI waveform. These metrics
are based on the directional gap probability profile derived from the L1B
waveform.


The vertical step between foliage profile measurements
(known as dZ in GEDI documentation) is always 5 meters.


The dataset LARSE/GEDI/GEDI02\_B\_002\_MONTHLY is a raster version
of the original GEDI02\_B product. The raster images are organized as monthly
composites of individual orbits in the corresponding month. Only root\-level
cover, pai and pavd values and their associated quality flags and metadata
are preserved as raster bands. Each GEDI02\_B\_002 raster has 109 bands.


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
| `algorithmrun_flag` | None | 0 | 1 | The L2B algorithm is run if this flag is set to 1 indicating data have sufficient waveform fidelity for L2B to run. |
| `beam` | None | 0 | 11 | Beam number |
| `cover` | % | 0 | 1 | Total canopy cover |
| `degrade_flag` | None | 0 | 99 | Flag indicating degraded state of pointing and/or positioning information.* 3X \- ADF CHU solution unavailable (ST\-2\) * 4X \- Platform attitude * 5X \- Poor solution (filter covariance large) * 6X \- Data outage (platform attitude gap also) * 7X \- ST 1\+2 unavailable (similar boresight FOV) * 8X \- ST 1\+2\+3 unavailable * 9X \- ST 1\+2\+3 and ISS unavailable * X1 \- Maneuver * X2 \- GPS data gap * X3 \- ST blinding * X4 \- Other * X5 \- GPS receiver clock drift * X6 \- Maneuver \& GPS receiver clock drift * X7 \- GPS data gap \& GPS receiver clock drift * X8 \- ST blinding \& GPS receiver clock drift * X9 \- Other \& GPS receiver clock drift |
| `delta_time` | seconds | Transmit time of the shot, measured in seconds from the master\_time\_epoch since 2018\-01\-01 |
| `fhd_normal` | None | Foliage Height Diversity |
| `l2b_quality_flag` | Quality Flag | 0 | 1 | L2B quality flag |
| `local_beam_azimuth` | rad | \-180 | 180 | Azimuth of the unit pointing vector for the laser in the local ENU frame measured from North and positive towards East. |
| `local_beam_elevation` | rad | 1\.39 | 1\.57 | Elevation of the unit pointing vector for the laser in the local ENU frame measured from East\-North plane and positive towards Up. |
| `pai` | Area fraction | Total Plant Area Index |
| `pgap_theta` | None | 0 | 1 | Total Gap Probability (theta) |
| `selected_l2a_algorithm` | None | 1 | 6 | Selected L2A algorithm setting |
| `selected_rg_algorithm` | None | 0 | 99 | Selected R (ground) algorithm |
| `sensitivity` | None | 0 | 1 | Maxmimum canopy cover that can be penetrated. Valid range is \[0, 1]. Values outside of this range may be present but must be ignored. They represent noise and non\-land surface waveforms. |
| `solar_azimuth` | deg | \-180 | 180 | The azimuth of the sun position vector from the laser bounce point position in the local ENU frame measured from North and is positive towards East. |
| `solar_elevation` | deg | \-90 | 90 | The elevation of the sun position vector from the laser bounce point position in the local ENU frame measured from the East\-North plane and is positive Up. |
| `shot_number` | None | Shot number, a unique identifier. This field has the format of OOOOOBBRRGNNNNNNNN, where:* OOOOO: Orbit number * BB: Beam number * RR: Reserved for future use * G: Sub\-orbit granule number * NNNNNNNN: Shot index |
| `shot_number_within_beam` | None | Shot number within beam |
| `cover_z0` | % | 0 | 1 | Cumulative canopy cover vertical profile at 0% |
| `cover_z1` | % | 0 | 1 | Cumulative canopy cover vertical profile at 1% |
| `cover_z2` | % | 0 | 1 | Cumulative canopy cover vertical profile at 2% |
| `cover_z3` | % | 0 | 1 | Cumulative canopy cover vertical profile at 3% |
| `cover_z4` | % | 0 | 1 | Cumulative canopy cover vertical profile at 4% |
| `cover_z5` | % | 0 | 1 | Cumulative canopy cover vertical profile at 5% |
| `cover_z6` | % | 0 | 1 | Cumulative canopy cover vertical profile at 6% |
| `cover_z7` | % | 0 | 1 | Cumulative canopy cover vertical profile at 7% |
| `cover_z8` | % | 0 | 1 | Cumulative canopy cover vertical profile at 8% |
| `cover_z9` | % | 0 | 1 | Cumulative canopy cover vertical profile at 9% |
| `cover_z10` | % | 0 | 1 | Cumulative canopy cover vertical profile at 10% |
| `cover_z11` | % | 0 | 1 | Cumulative canopy cover vertical profile at 11% |
| `cover_z12` | % | 0 | 1 | Cumulative canopy cover vertical profile at 12% |
| `cover_z13` | % | 0 | 1 | Cumulative canopy cover vertical profile at 13% |
| `cover_z14` | % | 0 | 1 | Cumulative canopy cover vertical profile at 14% |
| `cover_z15` | % | 0 | 1 | Cumulative canopy cover vertical profile at 15% |
| `cover_z16` | % | 0 | 1 | Cumulative canopy cover vertical profile at 16% |
| `cover_z17` | % | 0 | 1 | Cumulative canopy cover vertical profile at 17% |
| `cover_z18` | % | 0 | 1 | Cumulative canopy cover vertical profile at 18% |
| `cover_z19` | % | 0 | 1 | Cumulative canopy cover vertical profile at 19% |
| `cover_z20` | % | 0 | 1 | Cumulative canopy cover vertical profile at 20% |
| `cover_z21` | % | 0 | 1 | Cumulative canopy cover vertical profile at 21% |
| `cover_z22` | % | 0 | 1 | Cumulative canopy cover vertical profile at 22% |
| `cover_z23` | % | 0 | 1 | Cumulative canopy cover vertical profile at 23% |
| `cover_z24` | % | 0 | 1 | Cumulative canopy cover vertical profile at 24% |
| `cover_z25` | % | 0 | 1 | Cumulative canopy cover vertical profile at 25% |
| `cover_z26` | % | 0 | 1 | Cumulative canopy cover vertical profile at 26% |
| `cover_z27` | % | 0 | 1 | Cumulative canopy cover vertical profile at 27% |
| `cover_z28` | % | 0 | 1 | Cumulative canopy cover vertical profile at 28% |
| `cover_z29` | % | 0 | 1 | Cumulative canopy cover vertical profile at 29% |
| `cover_z30` | % | 0 | 1 | Cumulative canopy cover vertical profile at 30% |
| `pai_z0` | Area fraction | Plant Area Index profile in 0 m²/m² |
| `pai_z1` | Area fraction | Plant Area Index profile in 1 m²/m² |
| `pai_z2` | Area fraction | Plant Area Index profile in 2 m²/m² |
| `pai_z3` | Area fraction | Plant Area Index profile in 3 m²/m² |
| `pai_z4` | Area fraction | Plant Area Index profile in 4 m²/m² |
| `pai_z5` | Area fraction | Plant Area Index profile in 5 m²/m² |
| `pai_z6` | Area fraction | Plant Area Index profile in 6 m²/m² |
| `pai_z7` | Area fraction | Plant Area Index profile in 7 m²/m² |
| `pai_z8` | Area fraction | Plant Area Index profile in 8 m²/m² |
| `pai_z9` | Area fraction | Plant Area Index profile in 9 m²/m² |
| `pai_z10` | Area fraction | Plant Area Index profile in 10 m²/m² |
| `pai_z11` | Area fraction | Plant Area Index profile in 11 m²/m² |
| `pai_z12` | Area fraction | Plant Area Index profile in 12 m²/m² |
| `pai_z13` | Area fraction | Plant Area Index profile in 13 m²/m² |
| `pai_z14` | Area fraction | Plant Area Index profile in 14 m²/m² |
| `pai_z15` | Area fraction | Plant Area Index profile in 15 m²/m² |
| `pai_z16` | Area fraction | Plant Area Index profile in 16 m²/m² |
| `pai_z17` | Area fraction | Plant Area Index profile in 17 m²/m² |
| `pai_z18` | Area fraction | Plant Area Index profile in 18 m²/m² |
| `pai_z19` | Area fraction | Plant Area Index profile in 19 m²/m² |
| `pai_z20` | Area fraction | Plant Area Index profile in 20 m²/m² |
| `pai_z21` | Area fraction | Plant Area Index profile in 21 m²/m² |
| `pai_z22` | Area fraction | Plant Area Index profile in 22 m²/m² |
| `pai_z23` | Area fraction | Plant Area Index profile in 23 m²/m² |
| `pai_z24` | Area fraction | Plant Area Index profile in 24 m²/m² |
| `pai_z25` | Area fraction | Plant Area Index profile in 25 m²/m² |
| `pai_z26` | Area fraction | Plant Area Index profile in 26 m²/m² |
| `pai_z27` | Area fraction | Plant Area Index profile in 27 m²/m² |
| `pai_z28` | Area fraction | Plant Area Index profile in 28 m²/m² |
| `pai_z29` | Area fraction | Plant Area Index profile in 29 m²/m² |
| `pai_z30` | Area fraction | Plant Area Index profile in 30 m²/m² |
| `pavd_z0` | m^2/m^3 | Plant Area Volume Density profile in 0 m²/m³ |
| `pavd_z1` | m^2/m^3 | Plant Area Volume Density profile in 1 m²/m³ |
| `pavd_z2` | m^2/m^3 | Plant Area Volume Density profile in 2 m²/m³ |
| `pavd_z3` | m^2/m^3 | Plant Area Volume Density profile in 3 m²/m³ |
| `pavd_z4` | m^2/m^3 | Plant Area Volume Density profile in 4 m²/m³ |
| `pavd_z5` | m^2/m^3 | Plant Area Volume Density profile in 5 m²/m³ |
| `pavd_z6` | m^2/m^3 | Plant Area Volume Density profile in 6 m²/m³ |
| `pavd_z7` | m^2/m^3 | Plant Area Volume Density profile in 7 m²/m³ |
| `pavd_z8` | m^2/m^3 | Plant Area Volume Density profile in 8 m²/m³ |
| `pavd_z9` | m^2/m^3 | Plant Area Volume Density profile in 9 m²/m³ |
| `pavd_z10` | m^2/m^3 | Plant Area Volume Density profile in 10 m²/m³ |
| `pavd_z11` | m^2/m^3 | Plant Area Volume Density profile in 11 m²/m³ |
| `pavd_z12` | m^2/m^3 | Plant Area Volume Density profile in 12 m²/m³ |
| `pavd_z13` | m^2/m^3 | Plant Area Volume Density profile in 13 m²/m³ |
| `pavd_z14` | m^2/m^3 | Plant Area Volume Density profile in 14 m²/m³ |
| `pavd_z15` | m^2/m^3 | Plant Area Volume Density profile in 15 m²/m³ |
| `pavd_z16` | m^2/m^3 | Plant Area Volume Density profile in 16 m²/m³ |
| `pavd_z17` | m^2/m^3 | Plant Area Volume Density profile in 17 m²/m³ |
| `pavd_z18` | m^2/m^3 | Plant Area Volume Density profile in 18 m²/m³ |
| `pavd_z19` | m^2/m^3 | Plant Area Volume Density profile in 19 m²/m³ |
| `pavd_z20` | m^2/m^3 | Plant Area Volume Density profile in 20 m²/m³ |
| `pavd_z21` | m^2/m^3 | Plant Area Volume Density profile in 21 m²/m³ |
| `pavd_z22` | m^2/m^3 | Plant Area Volume Density profile in 22 m²/m³ |
| `pavd_z23` | m^2/m^3 | Plant Area Volume Density profile in 23 m²/m³ |
| `pavd_z24` | m^2/m^3 | Plant Area Volume Density profile in 24 m²/m³ |
| `pavd_z25` | m^2/m^3 | Plant Area Volume Density profile in 25 m²/m³ |
| `pavd_z26` | m^2/m^3 | Plant Area Volume Density profile in 26 m²/m³ |
| `pavd_z27` | m^2/m^3 | Plant Area Volume Density profile in 27 m²/m³ |
| `pavd_z28` | m^2/m^3 | Plant Area Volume Density profile in 28 m²/m³ |
| `pavd_z29` | m^2/m^3 | Plant Area Volume Density profile in 29 m²/m³ |
| `pavd_z30` | m^2/m^3 | Plant Area Volume Density profile in 30 m²/m³ |




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
returnim.updateMask(im.select('l2b_quality_flag').eq(1))
.updateMask(im.select('degrade_flag').eq(0));
};
vardataset=ee.ImageCollection('LARSE/GEDI/GEDI02_B_002_MONTHLY')
.map(qualityMask)
.select('solar_elevation');

vargediVis={
min:1,
max:60,
palette:'red, green, blue',
};
Map.setCenter(12.60033,51.01051,12);
Map.addLayer(dataset,gediVis,'Solar Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI02_B_002_MONTHLY)


[GEDI L2B Raster Canopy Cover Vertical Profile Metrics (Version 2\)](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_B_002_MONTHLY)

GEDI Level 2B Canopy Cover and Vertical Profile Metrics product (GEDI02\_B) extracts biophysical metrics from each GEDI waveform. These metrics are based on the directional gap probability profile derived from the L1B waveform. The vertical step between foliage profile measurements (known as dZ in GEDI documentation) is always 5 meters. …

 LARSE/GEDI/GEDI02\_B\_002\_MONTHLY,
 elevation,forest\-biomass,gedi,larse,nasa,tree\-cover,usgs

2019\-03\-25T00:00:00Z/2024\-11\-01T08:00:00Z



 \-51\.6 \-180 51\.6 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








