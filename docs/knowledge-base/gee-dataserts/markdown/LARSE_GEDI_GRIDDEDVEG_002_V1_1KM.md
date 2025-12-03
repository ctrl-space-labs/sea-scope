



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Gridded GEDI Vegetation Structure Metrics and Biomass Density, 1KM pixel size


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================================================================








Dataset Availability
2019\-04\-17T00:00:00Z–2023\-03\-16T00:00:00Z
Dataset Provider


[Rasterization: Google and USFS Laboratory for Applications of Remote Sensing in Ecology (LARSE)](https://www.fs.usda.gov/)


[Gridded GEDI Vegetation Structure Metrics and Biomass Density](https://daac.ornl.gov/VEGETATION/guides/GEDI_HighQuality_Shots_Rasters.html)



Earth Engine Snippet


`ee.ImageCollection("LARSE/GEDI/GRIDDEDVEG_002/V1/1KM")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GRIDDEDVEG_002_V1_1KM)





Tags


[biomass](/earth-engine/datasets/tags/biomass)
[canopy](/earth-engine/datasets/tags/canopy)
[forest](/earth-engine/datasets/tags/forest)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[gedi](/earth-engine/datasets/tags/gedi)
[larse](/earth-engine/datasets/tags/larse)
[lidar](/earth-engine/datasets/tags/lidar)
[nasa](/earth-engine/datasets/tags/nasa)
[vegetation](/earth-engine/datasets/tags/vegetation)








#### Description



This dataset consists of near\-global, analysis\-ready, multi\-resolution
gridded vegetation structure metrics derived from NASA Global Ecosystem
Dynamics Investigation (GEDI) Level 2 and 4A products associated with 25\-m
diameter lidar footprints. This dataset provides a comprehensive
representation of near\-global vegetation structure that is inclusive of
the entire vertical profile, based solely on GEDI lidar, and validated with
independent data.


The GEDI sensor, mounted on the International Space
Station (ISS), uses eight laser beams spaced by 60 m along\-track and 600 m
across\-track on the Earth surface to measure ground elevation and vegetation
structure between approximately 52 degrees North and South latitude.
Between April 17th 2019 and March 16th 2023, GEDI acquired 11 and 7\.7
billion quality waveforms suitable for measuring ground elevation and
vegetation structure, respectively.


In addition to many of the standard L2 and L4A shot metrics, several
additional metrics have been derived which may be particularly useful for
applications in carbon and water cycling processes in earth system models,
as well as forest management, biodiversity modeling, and habitat assessment.
Variables include canopy height, canopy cover, plant area index, foliage
height diversity, and plant area volume density at 5 m strata. Refer to the
[Gridded GEDI Vegetation Structure Metrics and Biomass Density](https://daac.ornl.gov/VEGETATION/guides/GEDI_HighQuality_Shots_Rasters.html)
for more information.


Eight statistics are included for each GEDI shot metric: mean, bootstrapped
standard error of the mean, median, standard deviation, interquartile range,
95th percentile, Shannon's diversity index, and shot count.
Quality shot filtering methodology that aligns with the GEDI L4B Gridded
Aboveground Biomass Density, Version 2\.1 was used. In comparison to the
corresponding GEDI L3 dataset, this dataset provides additional gridded metrics at
multiple spatial resolutions and over several temporal periods (annual and
the full mission duration).


This dataset provides GEDI shot metrics aggregated into raster grids at
three spatial resolutions: 1 km, 6 km, and 12 km.
This dataset uses the pixel size of 1KM.





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Description |
| --- | --- |
| `mean` | The mean of GEDI shot metric values within a pixel |
| `meanbse` | Standard error of the mean calculated using bootstrap resampling. 100 bootstrap samples were created; each sample included 70% of shots, randomly selected. Standard error was calculated using the means of bootstrapped samples. (Only calculated when there are at least 10 GEDI shots in the grid cell.) |
| `median` | The median value (50th percentile) of GEDI shot metric values within a pixel. |
| `sd` | The standard deviation of GEDI shot metric values within a pixel. |
| `iqr` | The interquartile range (75 percentile minus 25th percentile) of GEDI shot metric values within a pixel. |
| `p95` | The 95th percentile value of GEDI shot metric values within a pixel. |
| `shan` | Shannons diversity index (H) of GEDI shot metric values within a pixel. Calculated as:\-1*(sum(p*log(p))) where p is the proportion of GEDI shot values per bin. |
| `countf` | The count of GEDI shot metric values within a pixel. A 30\-m sub\-grid was used to select the (temporally) first GEDI shot acquired in each 30\-m sub\-grid cell. |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* Burns, P., Hakkenberg, C.R. \& Goetz, S.J. Multi\-resolution gridded maps of
vegetation structure from GEDI. Sci Data 11, 881 (2024\).
[doi:10\.1038/s41597\-024\-03668\-4](https://doi.org/10.1038/s41597-024-03668-4)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varpalettes=require('users/gena/packages:palettes');

// GEDI image collections at different spatial resolutions
varic_1k=ee.ImageCollection('LARSE/GEDI/GRIDDEDVEG_002/V1/1KM')
varic_6k=ee.ImageCollection('LARSE/GEDI/GRIDDEDVEG_002/V1/6KM')
varic_12k=ee.ImageCollection('LARSE/GEDI/GRIDDEDVEG_002/V1/12KM')

// slopeshade basemap
varelev=ee.Image('MERIT/DEM/v1_0_3').select('dem')
varslope=ee.Terrain.slope(elev)
Map.setCenter(92.319,27.129,8)
Map.addLayer(
slope,{min:0,max:40,palette:['ffffff','000000']},'Slopeshade')

varopac=0.7
// View various measurement count metrics from 2019 to 2023
// "va" in the asset name corresponds to the count of high-quality, leaf-on
// vegetation measurements by GEDI
vari_counts_1k_19to23=ee.Image(
'LARSE/GEDI/GRIDDEDVEG_002/COUNTS/V1/1KM/gediv002_counts_va_20190417_20230316')
// Number of GEDI laser shots (i.e. footprints) per 1km pixel
Map.addLayer(
i_counts_1k_19to23.select('shots_count'),
{min:0,max:200,palette:palettes.matplotlib.magma[7]},
'Shot count per 1km pixel, 2019 to 2023',0,opac)
// Number of ISS orbits (with valid GEDI shots) per 1km pixel
Map.addLayer(
i_counts_1k_19to23.select('orbits_uniq'),
{min:0,max:10,palette:palettes.matplotlib.plasma[7]},
'Unique orbits per 1km pixel, 2019 to 2023',0,opac)
// The Nearest Neighbor Index (Evans et al. 2023), a proxy for quantifying
// spatial clustering/dispersion of GEDI shots
Map.addLayer(
i_counts_1k_19to23.select('shots_nni'),
{min:0.5,max:1.5,palette:palettes.colorbrewer.RdBu[7]},
'Shot nearest neighbor index per 1km pixel, 2019 to 2023',0,opac)

// View several GEDI vegetation structure metrics at 1km spatial res.
// For GEDI metric descriptions see Table 1 at
// https://daac.ornl.gov/GEDI/guides/GEDI_HighQuality_Shots_Rasters.html
// Relative height of the 98th percentile of returned energy (RH98), a proxy for
// tree canopy height
vari_rh98_1k_19to23=ee.Image(
'LARSE/GEDI/GRIDDEDVEG_002/V1/1KM/gediv002_rh-98-a0_vf_20190417_20230316')
// display the median value of GEDI RH98 measurements per 1km pixel, masking out
// values less than 3 consider using a threshold of 10 shots per 1km pixel. More
// shots generally yield more accurate estimates of the aggregation statistics
// (different bands)
vari_rh98_1k_19to23_med=i_rh98_1k_19to23.select('median')
varrh98_pal=palettes.crameri.bamako[10].reverse()
Map.addLayer(
i_rh98_1k_19to23_med.updateMask(i_rh98_1k_19to23_med.gte(3).and(
i_rh98_1k_19to23.select('countf').gte(10))),
{min:3,max:40,palette:rh98_pal},
'Median RH98 per 1km pixel, 2019 to 2023',1,opac)
// Standard deviation of RH98 per 1km pixel. Captures variability of GEDI
// measurements and vegetation heterogeneity
Map.addLayer(
i_rh98_1k_19to23.select('sd').updateMask(i_rh98_1k_19to23_med.gte(3).and(
i_rh98_1k_19to23.select('countf').gte(10))),
{min:2,max:20,palette:palettes.cmocean.Curl[7]},
'SD of RH98 per 1km pixel, 2019 to 2023',0,opac)
// Foliage height diversity of the 1m vertical Plant Area Index (PAI) profile
vari_fhd_1k_19to23=ee.Image(
'LARSE/GEDI/GRIDDEDVEG_002/V1/1KM/gediv002_fhd-pai-1m-a0_vf_20190417_20230316')
Map.addLayer(
i_fhd_1k_19to23.select('median').updateMask(i_rh98_1k_19to23_med.gte(3).and(
i_rh98_1k_19to23.select('countf').gte(10))),
{min:1.2,max:3.2,palette:palettes.matplotlib.viridis[7].reverse()},
'Median FHD per 1km pixel, 2019 to 2023',0,opac)
// The height above ground associated with the peak of the vertical Plant Area
// Volume Density (PAVD) profile
vari_pavdmaxh_19to23=ee.Image(
'LARSE/GEDI/GRIDDEDVEG_002/V1/1KM/gediv002_pavd-max-h_vf_20190417_20230316')
Map.addLayer(
i_pavdmaxh_19to23.select('mean').updateMask(i_rh98_1k_19to23_med.gte(3).and(
i_pavdmaxh_19to23.select('countf').gte(10))),
{min:0,max:25,palette:palettes.cmocean.Haline[7].reverse()},
'Mean Height of Max. PAVD, 2019 to 2023',0,opac)

// 1km coverage is not great in the low latitudes, try 6 or 12km for a more
// continuous depiction
vari_rh98_6k_19to23=ee.Image(
'LARSE/GEDI/GRIDDEDVEG_002/V1/6KM/gediv002_rh-98-a0_vf_20190417_20230316')
// display the median value of GEDI RH98 measurements per 6km pixel, masking out
// values less than 3 consider using a threshold of 100 shots per 6km pixel.
// More shots generally yield more accurate estimates of the aggregation
// statistics (different bands)
vari_rh98_6k_19to23_med=i_rh98_6k_19to23.select('median')
Map.addLayer(
i_rh98_6k_19to23_med.updateMask(i_rh98_6k_19to23_med.gte(3).and(
i_rh98_6k_19to23.select('countf').gte(100))),
{min:3,max:40,palette:rh98_pal},
'Median RH98 per 6km pixel, 2019 to 2023',0,opac)
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GRIDDEDVEG_002_V1_1KM)


[Gridded GEDI Vegetation Structure Metrics and Biomass Density, 1KM pixel size](/earth-engine/datasets/catalog/LARSE_GEDI_GRIDDEDVEG_002_V1_1KM)

This dataset consists of near\-global, analysis\-ready, multi\-resolution gridded vegetation structure metrics derived from NASA Global Ecosystem Dynamics Investigation (GEDI) Level 2 and 4A products associated with 25\-m diameter lidar footprints. This dataset provides a comprehensive representation of near\-global vegetation structure that is inclusive of the entire vertical profile, based solely …

 LARSE/GEDI/GRIDDEDVEG\_002/V1/1KM,
 biomass,canopy,forest,forest\-biomass,gedi,larse,lidar,nasa,vegetation

2019\-04\-17T00:00:00Z/2023\-03\-16T00:00:00Z



 \-52 \-180 52 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








