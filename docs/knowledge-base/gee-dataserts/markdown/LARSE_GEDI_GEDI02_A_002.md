



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GEDI L2A Vector Canopy Top Height (Version 2\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================








Dataset Availability
2019\-03\-25T00:00:00Z–2024\-11\-29T00:00:00Z
Dataset Provider


[USFS Laboratory for Applications of Remote Sensing in Ecology (LARSE)](https://www.fs.usda.gov/)


[NASA GEDI mission, accessed through the USGS LP DAAC](https://lpdaac.usgs.gov/products/gedi02_av002/)




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


Please see [User Guide](https://lpdaac.usgs.gov/documents/986/GEDI02_UserGuide_V2.pdf)
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
| beam | INT | Beam identifier |
| degrade\_flag | INT | Flag indicating degraded state of pointing and/or positioning information.* 3X \- ADF CHU solution unavailable (ST\-2\) * 4X \- Platform attitude * 5X \- Poor solution (filter covariance large) * 6X \- Data outage (platform attitude gap also) * 7X \- ST 1\+2 unavailable (similar boresight FOV) * 8X \- ST 1\+2\+3 unavailable * 9X \- ST 1\+2\+3 and ISS unavailable * X1 \- Maneuver * X2 \- GPS data gap * X3 \- ST blinding * X4 \- Other * X5 \- GPS receiver clock drift * X6 \- Maneuver \& GPS receiver clock drift * X7 \- GPS data gap \& GPS receiver clock drift * X8 \- ST blinding \& GPS receiver clock drift * X9 \- Other \& GPS receiver clock drift |
| delta\_time | DOUBLE | Time delta since Jan 1 00:00 2018 |
| digital\_elevation\_model | DOUBLE | TanDEM\-X elevation at GEDI footprint location |
| digital\_elevation\_model\_srtm | DOUBLE | SRTM elevation at GEDI footprint location |
| elev\_highestreturn | DOUBLE | Elevation of highest detected return relative to reference ellipsoid |
| elev\_lowestmode | DOUBLE | Elevation of center of lowest mode relative to reference ellipsoid |
| elevation\_bias\_flag | INT | Elevations potentially affected by 4bin (\~60 cm) ranging error |
| energy\_total | DOUBLE | Integrated counts in the return waveform relative to the mean noise level |
| landsat\_treecover | DOUBLE | Tree cover in the year 2010, defined as canopy closure for all vegetation taller than 5 m in height as a percentage per output grid cell |
| landsat\_water\_persistence | INT | Percent UMD GLAD Landsat observations with classified surface water |
| lat\_highestreturn | DOUBLE | Latitude of highest detected return |
| leaf\_off\_doy | INT | GEDI 1 km EASE 2\.0 grid leaf\-off start day\-of\-year |
| leaf\_off\_flag | INT | GEDI 1 km EASE 2\.0 grid flag |
| leaf\_on\_cycle | INT | Flag that indicates the vegetation growing cycle for leaf\-on observations |
| leaf\_on\_doy | INT | GEDI 1 km EASE 2\.0 grid leaf\-on start day\-of\-year |
| lon\_highestreturn | DOUBLE | Longitude of highest detected return |
| modis\_nonvegetated | DOUBLE | Percent non\-vegetated from MODIS MOD44B V6 data |
| modis\_nonvegetated\_sd | DOUBLE | Percent non\-vegetated standard deviation from MODIS MOD44B V6 data |
| modis\_treecover | DOUBLE | Percent tree cover from MODIS MOD44B V6 data |
| modis\_treecover\_sd | DOUBLE | Percent tree cover standard deviation from MODIS MOD44B V6 data |
| num\_detectedmodes | INT | Number of detected modes in rxwaveform |
| pft\_class | INT | GEDI 1 km EASE 2\.0 grid Plant Functional Type (PFT) |
| quality\_flag | INT | Flag indicating likely invalid waveform (1\=valid, 0\=invalid) |
| region\_class | INT | GEDI 1 km EASE 2\.0 grid world continental regions |
| selected\_algorithm | INT | Identifier of algorithm selected as identifying the lowest non\-noise mode |
| selected\_mode | INT | Identifier of mode selected as lowest non\-noise mode |
| selected\_mode\_flag | INT | Flag indicating status of selected\_mode |
| sensitivity | DOUBLE | Maxmimum canopy cover that can be penetrated. Valid range is \[0, 1]. Values outside of this range may be present but must be ignored. They represent noise and non\-land surface waveforms. |
| solar\_azimuth | DOUBLE | The azimuth of the sun position vector from the laser bounce point position in the local ENU frame. The angle is measured from North and is positive towards East. |
| solar\_elevation | DOUBLE | The elevation of the sun position vector from the laser bounce point position in the local ENU frame. The angle is measured from the East\-North plane and is positive Up. |
| surface\_flag | INT | Indicates elev\_lowestmode is within 300m of Digital Elevation Model (DEM) or Mean Sea Surface (MSS) elevation |
| urban\_focal\_window\_size | INT | The focal window size used to calculate urban\_proportion. Values are 3 (3x3 pixel window size) or 5 (5x5 pixel window size). |
| urban\_proportion | INT | The percentage proportion of land area within a focal area surrounding each shot that is urban land cover. |
| orbit\_number | INT | Orbit number |
| minor\_frame\_number | INT | Minor frame number 0\-241() |
| shot\_number\_within\_beam | INT | Shot number within beam |
| local\_beam\_azimuth | DOUBLE | Azimuth in radians of the unit pointing vector for the laser in the local ENU frame. The angle is measured from North and positive towards East. |
| local\_beam\_elevation | DOUBLE | Elevation in radians of the unit pointing vector for the laser in the local ENU frame. The angle is measured from North and positive towards East. |
| shot\_number | STRING | Shot number, a unique identifier. This field has the format of OOOOOBBRRGNNNNNNNN, where:* OOOOO: Orbit number * BB: Beam number * RR: Reserved for future use * G: Sub\-orbit granule number * NNNNNNNN: Shot index |
| rh0 | DOUBLE | Relative height metrics at 0% |
| rh1 | DOUBLE | Relative height metrics at 1% |
| rh2 | DOUBLE | Relative height metrics at 2% |
| rh3 | DOUBLE | Relative height metrics at 3% |
| rh4 | DOUBLE | Relative height metrics at 4% |
| rh5 | DOUBLE | Relative height metrics at 5% |
| rh6 | DOUBLE | Relative height metrics at 6% |
| rh7 | DOUBLE | Relative height metrics at 7% |
| rh8 | DOUBLE | Relative height metrics at 8% |
| rh9 | DOUBLE | Relative height metrics at 9% |
| rh10 | DOUBLE | Relative height metrics at 10% |
| rh11 | DOUBLE | Relative height metrics at 11% |
| rh12 | DOUBLE | Relative height metrics at 12% |
| rh13 | DOUBLE | Relative height metrics at 13% |
| rh14 | DOUBLE | Relative height metrics at 14% |
| rh15 | DOUBLE | Relative height metrics at 15% |
| rh16 | DOUBLE | Relative height metrics at 16% |
| rh17 | DOUBLE | Relative height metrics at 17% |
| rh18 | DOUBLE | Relative height metrics at 18% |
| rh19 | DOUBLE | Relative height metrics at 19% |
| rh20 | DOUBLE | Relative height metrics at 20% |
| rh21 | DOUBLE | Relative height metrics at 21% |
| rh22 | DOUBLE | Relative height metrics at 22% |
| rh23 | DOUBLE | Relative height metrics at 23% |
| rh24 | DOUBLE | Relative height metrics at 24% |
| rh25 | DOUBLE | Relative height metrics at 25% |
| rh26 | DOUBLE | Relative height metrics at 26% |
| rh27 | DOUBLE | Relative height metrics at 27% |
| rh28 | DOUBLE | Relative height metrics at 28% |
| rh29 | DOUBLE | Relative height metrics at 29% |
| rh30 | DOUBLE | Relative height metrics at 30% |
| rh31 | DOUBLE | Relative height metrics at 31% |
| rh32 | DOUBLE | Relative height metrics at 32% |
| rh33 | DOUBLE | Relative height metrics at 33% |
| rh34 | DOUBLE | Relative height metrics at 34% |
| rh35 | DOUBLE | Relative height metrics at 35% |
| rh36 | DOUBLE | Relative height metrics at 36% |
| rh37 | DOUBLE | Relative height metrics at 37% |
| rh38 | DOUBLE | Relative height metrics at 38% |
| rh39 | DOUBLE | Relative height metrics at 39% |
| rh40 | DOUBLE | Relative height metrics at 40% |
| rh41 | DOUBLE | Relative height metrics at 41% |
| rh42 | DOUBLE | Relative height metrics at 42% |
| rh43 | DOUBLE | Relative height metrics at 43% |
| rh44 | DOUBLE | Relative height metrics at 44% |
| rh45 | DOUBLE | Relative height metrics at 45% |
| rh46 | DOUBLE | Relative height metrics at 46% |
| rh47 | DOUBLE | Relative height metrics at 47% |
| rh48 | DOUBLE | Relative height metrics at 48% |
| rh49 | DOUBLE | Relative height metrics at 49% |
| rh50 | DOUBLE | Relative height metrics at 50% |
| rh51 | DOUBLE | Relative height metrics at 51% |
| rh52 | DOUBLE | Relative height metrics at 52% |
| rh53 | DOUBLE | Relative height metrics at 53% |
| rh54 | DOUBLE | Relative height metrics at 54% |
| rh55 | DOUBLE | Relative height metrics at 55% |
| rh56 | DOUBLE | Relative height metrics at 56% |
| rh57 | DOUBLE | Relative height metrics at 57% |
| rh58 | DOUBLE | Relative height metrics at 58% |
| rh59 | DOUBLE | Relative height metrics at 59% |
| rh60 | DOUBLE | Relative height metrics at 60% |
| rh61 | DOUBLE | Relative height metrics at 61% |
| rh62 | DOUBLE | Relative height metrics at 62% |
| rh63 | DOUBLE | Relative height metrics at 63% |
| rh64 | DOUBLE | Relative height metrics at 64% |
| rh65 | DOUBLE | Relative height metrics at 65% |
| rh66 | DOUBLE | Relative height metrics at 66% |
| rh67 | DOUBLE | Relative height metrics at 67% |
| rh68 | DOUBLE | Relative height metrics at 68% |
| rh69 | DOUBLE | Relative height metrics at 69% |
| rh70 | DOUBLE | Relative height metrics at 70% |
| rh71 | DOUBLE | Relative height metrics at 71% |
| rh72 | DOUBLE | Relative height metrics at 72% |
| rh73 | DOUBLE | Relative height metrics at 73% |
| rh74 | DOUBLE | Relative height metrics at 74% |
| rh75 | DOUBLE | Relative height metrics at 75% |
| rh76 | DOUBLE | Relative height metrics at 76% |
| rh77 | DOUBLE | Relative height metrics at 77% |
| rh78 | DOUBLE | Relative height metrics at 78% |
| rh79 | DOUBLE | Relative height metrics at 79% |
| rh80 | DOUBLE | Relative height metrics at 80% |
| rh81 | DOUBLE | Relative height metrics at 81% |
| rh82 | DOUBLE | Relative height metrics at 82% |
| rh83 | DOUBLE | Relative height metrics at 83% |
| rh84 | DOUBLE | Relative height metrics at 84% |
| rh85 | DOUBLE | Relative height metrics at 85% |
| rh86 | DOUBLE | Relative height metrics at 86% |
| rh87 | DOUBLE | Relative height metrics at 87% |
| rh88 | DOUBLE | Relative height metrics at 88% |
| rh89 | DOUBLE | Relative height metrics at 89% |
| rh90 | DOUBLE | Relative height metrics at 90% |
| rh91 | DOUBLE | Relative height metrics at 91% |
| rh92 | DOUBLE | Relative height metrics at 92% |
| rh93 | DOUBLE | Relative height metrics at 93% |
| rh94 | DOUBLE | Relative height metrics at 94% |
| rh95 | DOUBLE | Relative height metrics at 95% |
| rh96 | DOUBLE | Relative height metrics at 96% |
| rh97 | DOUBLE | Relative height metrics at 97% |
| rh98 | DOUBLE | Relative height metrics at 98% |
| rh99 | DOUBLE | Relative height metrics at 99% |
| rh100 | DOUBLE | Relative height metrics at 100% |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* GEDI L2A Elevation and Height Metrics Data Global Footprint Level \- GEDI02\_A
Dubayah, R., M. Hofton, J. Blair, J. Armston, H. Tang, S. Luthcke. GEDI L2A
Elevation and Height Metrics Data Global Footprint Level V002\. 2021,
distributed by NASA EOSDIS Land Processes DAAC. Accessed YYYY\-MM\-DD.





### DOIs


* [https://doi.org/10\.5067/GEDI/GEDI02\_A.002](https://doi.org/10.5067/GEDI/GEDI02_A.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('LARSE/GEDI/GEDI02_A_002/GEDI02_A_2021244154857_O15413_04_T05622_02_003_02_V002');
dataset=dataset.style({color:'black',pointSize:1});
Map.setCenter(-64.88,-31.77,15);
Map.addLayer(dataset);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI02_A_002)


[GEDI L2A Vector Canopy Top Height (Version 2\)](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_A_002)

GEDI's Level 2A Geolocated Elevation and Height Metrics Product (GEDI02\_A) is primarily composed of 100 Relative Height (RH) metrics, which collectively describe the waveform collected by GEDI. The original GEDI02\_A product is a table of point with a spatial resolution (average footprint) of 25 meters. Please see User Guide for …

 LARSE/GEDI/GEDI02\_A\_002,
 elevation,forest\-biomass,gedi,larse,nasa,tree\-cover,usgs

2019\-03\-25T00:00:00Z/2024\-11\-29T00:00:00Z



 \-51\.6 \-180 51\.6 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/GEDI/GEDI02\_A.002](https://doi.org/https://www.fs.usda.gov/)
* [https://doi.org/10\.5067/GEDI/GEDI02\_A.002](https://doi.org/https://lpdaac.usgs.gov/products/gedi02_av002/)
* [https://doi.org/10\.5067/GEDI/GEDI02\_A.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_A_002)









