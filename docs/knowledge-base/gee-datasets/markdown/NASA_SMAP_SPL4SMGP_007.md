



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

SPL4SMGP.007 SMAP L4 Global 3\-hourly 9\-km Surface and Root Zone Soil Moisture


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================================================








Dataset Availability
2015\-03\-31T12:00:00Z–2025\-06\-27T22:30:00Z
Dataset Provider


[Google and NSIDC](https://nsidc.org/data/spl4smgp/versions/7)



Earth Engine Snippet


`ee.ImageCollection("NASA/SMAP/SPL4SMGP/007")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_SMAP_SPL4SMGP_007)





Cadence
3 Hours
Tags


[drought](/earth-engine/datasets/tags/drought)
[nasa](/earth-engine/datasets/tags/nasa)
[smap](/earth-engine/datasets/tags/smap)
[soil](/earth-engine/datasets/tags/soil)
[soil\-moisture](/earth-engine/datasets/tags/soil-moisture)
[surface](/earth-engine/datasets/tags/surface)
[weather](/earth-engine/datasets/tags/weather)








#### Description



The SMAP Level\-4 (L4\) Soil Moisture product includes surface soil moisture
(0\-5 cm vertical average), root\-zone soil moisture (0\-100 cm vertical
average), and additional research products (not validated), including
surface meteorological forcing variables, soil temperature,
evapotranspiration, and net radiation.


SMAP L4 provides uninterrupted soil moisture data. During outages of the
SMAP instrument, SMAP L4 soil moisture is based on land model simulations
alone, without the concomitant assimilation of SMAP brightness temperature
observations. Significant SMAP instrument outages occurred between 19 June
and 23 July 2019 and between 6 August and 20 September 2022\.


SMAP L\-band brightness temperature data from descending and ascending
half\-orbit satellite passes (approximately 6:00 a.m. and 6:00 p.m. local
solar time, respectively) are assimilated into a land surface model that is
gridded using an Earth\-fixed, global cylindrical 9 km Equal\-Area Scalable
Earth Grid, Version 2\.0 (EASE\-Grid 2\.0\) projection.


The SPL4SMGP product includes a series of 3\-hourly time\-averaged geophysical
data fields from the assimilation system. SPL4SMGP data are transformed to
[geographic coordinates using GDAL libraries](https://github.com/google/earthengine-catalog/blob/main/pipelines/smap_convert_l4.py)
before the data are ingested into Google Earth Engine.


See the [SMAP L4 Soil Moisture User Guide](https://nsidc.org/sites/default/files/documents/user-guide/multi_spl4smau-v007-userguide.pdf)
and references therein for additional documentation and algorithm details.


See
[basic](https://developers.google.com/earth-engine/tutorials/community/smap-soil-moisture)
and
[advanced](https://developers.google.com/earth-engine/tutorials/community/anomalies-analysis-smo-and-pre)
tutorials to learn how to use SMAP data in Earth Engine.





### Bands



**Pixel Size**
  
11000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `sm_surface` | Volume fraction | 0 | 0\.9 | Top layer soil moisture (0\-5 cm) |
| `sm_rootzone` | Volume fraction | 0 | 0\.9 | Root zone soil moisture (0\-100 cm) |
| `sm_profile` | Volume fraction | 0 | 0\.9 | Total profile soil moisture (0 cm to model bedrock depth). |
| `sm_surface_wetness` | None | 0 | 1 | Top layer soil wetness (0\-5 cm;wetness units). Soil wetness units (dimensionless) vary between 0 and 1,  indicating relative saturation between completely dry conditions and  completely saturated conditions, respectively. |
| `sm_rootzone_wetness` | None | 0 | 1 | Root zone soil wetness (0\-100 cm;wetness units). Soil wetness units (dimensionless) vary between 0 and 1,  indicating relative saturation between completely dry conditions and  completely saturated conditions, respectively. |
| `sm_profile_wetness` | None | 0 | 1 | Total profile soil wetness (0 cm to model bedrock depth; wetness units). Soil wetness units (dimensionless) vary between 0 and 1,  indicating relative saturation between completely dry conditions and  completely saturated conditions, respectively. |
| `surface_temp` | K | 180 | 350 | Mean land surface temperature (including snow\-covered land area). Excluding areas of open water and permanent ice |
| `soil_temp_layer1` | K | 210 | 350 | Soil temperature in layer 1 of soil heat diffusion model |
| `soil_temp_layer2` | K | 210 | 330 | Soil temperature in layer 2 of soil heat diffusion model |
| `soil_temp_layer3` | K | 215 | 325 | Soil temperature in layer 3 of soil heat diffusion model |
| `soil_temp_layer4` | K | 220 | 325 | Soil temperature in layer 4 of soil heat diffusion model |
| `soil_temp_layer5` | K | 225 | 325 | Soil temperature in layer 5 of soil heat diffusion model |
| `soil_temp_layer6` | K | 230 | 320 | Soil temperature in layer 6 of soil heat diffusion model |
| `snow_mass` | kg/m^2 | 0 | 10000 | Average snow mass (or snow water equivalent) over land  fraction of grid cell |
| `snow_depth` | m | 0 | 50 | Snow depth within snow\-covered land fraction of grid cell |
| `land_evapotranspiration_flux` | kg/m^2/s | \-0\.001 | 0\.001 | Evapotranspiration from land |
| `overland_runoff_flux` | kg/m^2/s | 0 | 0\.05 | Overland (surface) runoff (including throughflow) |
| `baseflow_flux` | kg/m^2/s | 0 | 0\.01 | Baseflow |
| `snow_melt_flux` | kg/m^2/s | 0 | 0\.05 | Snowmelt |
| `soil_water_infiltration_flux` | kg/m^2/s | 0 | 0\.05 | Soil water infiltration rate |
| `land_fraction_saturated` | None | 0 | 1 | Fractional land area that is saturated and snow\-free |
| `land_fraction_unsaturated` | None | 0 | 1 | Fractional land area that is unsaturated (but non\-wilting) and snow\-free |
| `land_fraction_wilting` | None | 0 | 1 | Fractional land area that is wilting and snow\-free |
| `land_fraction_snow_covered` | None | 0 | 1 | Fractional land area that is snowcovered |
| `heat_flux_sensible` | W/m^2 | \-2500 | 3000 | Sensible heat flux from land |
| `heat_flux_latent` | W/m^2 | \-2500 | 3000 | Latent heat flux from land |
| `heat_flux_ground` | W/m^2 | \-1000 | 1000 | Downward ground heat flux into layer 1 of soil heat diffusion model |
| `net_downward_shortwave_flux` | W/m^2 | 0 | 1365 | Net downward shortwave flux over land |
| `net_downward_longwave_flux` | W/m^2 | \-1000 | 200 | Net downward longwave flux over land |
| `radiation_shortwave_downward_flux` | W/m^2 | 0 | 1500 | Downward shortwave flux incident on the surface |
| `radiation_longwave_absorbed_flux` | W/m^2 | 35 | 800 | Absorbed (downward) longwave radiation at the surface |
| `precipitation_total_surface_flux` | kg m^\-2 s^\-2 | 0 | 0\.05 | Total surface precipitation (incl. snow fall) |
| `snowfall_surface_flux` | kg m^\-2 s^\-2 | 0 | 0\.05 | Surface snow fall |
| `surface_pressure` | K | 40000 | 110000 | Mean land surface temperature (incl. snow\-covered land area) |
| `height_lowatmmodlay` | m | 40 | 80 | Center height of lowest atmospheric model layer |
| `temp_lowatmmodlay` | K | 180 | 350 | Air temperature at center height of lowest atmospheric  model layer |
| `specific_humidity_lowatmmodlay` | Mass fraction | 0 | 0\.4 | Air specific humidity at center height of lowest atmospheric model layer |
| `windspeed_lowatmmodlay` | m/s | \-60 | 60 | Surface wind speed at center height of lowest atmospheric model layer |
| `vegetation_greenness_fraction` | None | 0 | 1 | Vegetation "greenness" or fraction of transpiring leaves averaged over the land area\* of the grid cell. |
| `leaf_area_index` | Area fraction | 0 | 10 | Vegetation leaf area index |
| `sm_rootzone_pctl` | % | 0 | 100 | Root zone soil moisture (0\-100 cm; percentile units) |
| `sm_profile_pctl` | % | 0 | 100 | Total profile soil moisture (0 cm to model bedrock depth; percentile units) |
| `depth_to_water_table_from_surface_in_peat` | m | \-5 | 0\.15 | Depth to water table from mean surface elevation in peatlands (positive above ground) |
| `free_surface_water_on_peat_flux` | kg/m^2/s | \-0\.001 | 0\.001 | Change in free surface water storage on peatlands |
| `mwrtm_vegopacity` | None | 0 | 2\.5 | Microwave radiative transfer model: Vegetation opacity. |
| `sm_surface_anomaly` | None | Experimental. Difference of the 30\-day average of 'sm\_surface', centered on asset date, relative to the same 30\-day period averaged across years from 2015 to present, excluding asset year. See [this script](https://github.com/google/earthengine-community/blob/master/datasets/smap_anomaly_l4.py) for anomaly computations. |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* **Reichle, R.H., G. De Lannoy, R.D. Koster, W.T. Crow, J.S. Kimball,
Q. Liu, and M. Bechtold. 2022\.**
SMAP L4 Global 3\-hourly 9 km EASE\-Grid Surface and Root Zone Soil
Moisture Analysis Update, Version 7\. \[Indicate subset used]. Boulder,
Colorado USA. NASA National Snow and Ice Data Center Distributed Active
Archive Center.
[doi:10\.5067/LWJ6TF5SZRG3](https://doi.org/10.5067/LWJ6TF5SZRG3)


**Reichle, R.H., G. De Lannoy, R.D. Koster, W.T. Crow, J.S. Kimball,
Q. Liu, and M. Bechtold. 2022\.**
SMAP L4 Global 3\-hourly 9 km EASE\-Grid Surface and Root Zone Soil
Moisture Analysis Update, Version 7\. \[Indicate subset used]. Boulder,
Colorado USA. NASA National Snow and Ice Data Center Distributed Active
Archive Center.
[doi:10\.5067/EVKPQZ4AFC4D](https://doi.org/10.5067/EVKPQZ4AFC4D)


**Reichle, R.H., G. De Lannoy, R.D. Koster, W.T. Crow, J.S. Kimball,
Q. Liu, and M. Bechtold. 2022\.**
SMAP L4 Global 3\-hourly 9 km EASE\-Grid Surface and Root Zone Soil
Moisture Analysis Update, Version 7\. \[Indicate subset used]. Boulder,
Colorado USA. NASA National Snow and Ice Data Center Distributed Active
Archive Center.
[doi:10\.5067/EVKPQZ4AFC4D](https://doi.org/10.5067/EVKPQZ4AFC4D)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/SMAP/SPL4SMGP/007')
.filter(ee.Filter.date('2017-04-01','2017-04-30'));

varsmSurface=dataset.select('sm_surface');
varsmSurfaceVis={
min:0.0,
max:0.9,
palette:['0300ff','418504','efff07','efff07','ff0303'],
};
Map.setCenter(-6.746,46.529,2);
Map.addLayer(smSurface,smSurfaceVis,'SM Surface');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_SMAP_SPL4SMGP_007)


[SPL4SMGP.007 SMAP L4 Global 3\-hourly 9\-km Surface and Root Zone Soil Moisture](/earth-engine/datasets/catalog/NASA_SMAP_SPL4SMGP_007)

The SMAP Level\-4 (L4\) Soil Moisture product includes surface soil moisture (0\-5 cm vertical average), root\-zone soil moisture (0\-100 cm vertical average), and additional research products (not validated), including surface meteorological forcing variables, soil temperature, evapotranspiration, and net radiation. SMAP L4 provides uninterrupted soil moisture data. During outages of the …

 NASA/SMAP/SPL4SMGP/007,
 drought,nasa,smap,soil,soil\-moisture,surface,weather

2015\-03\-31T12:00:00Z/2025\-06\-27T22:30:00Z



 \-84 \-180 84 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








