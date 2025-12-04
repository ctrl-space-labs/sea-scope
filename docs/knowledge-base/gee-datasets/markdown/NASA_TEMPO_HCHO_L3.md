



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TEMPO gridded HCHO vertical columns V03


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================








Dataset Availability
2023\-08\-01T00:00:00Z–2025\-07\-16T12:33:53Z
Dataset Provider


[NASA ASDC](https://asdc.larc.nasa.gov/)



Earth Engine Snippet


`ee.ImageCollection("NASA/TEMPO/HCHO_L3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_TEMPO_HCHO_L3)





Tags


[air\-quality](/earth-engine/datasets/tags/air-quality)
[formaldehyde](/earth-engine/datasets/tags/formaldehyde)
[nasa](/earth-engine/datasets/tags/nasa)
[pollution](/earth-engine/datasets/tags/pollution)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[tropomi](/earth-engine/datasets/tags/tropomi)








#### Description



Formaldehyde Level 3 collection provides trace gas information on a
regular grid covering the TEMPO field of regard for nominal TEMPO
observations. Level 3 files are derived by combining information from
all Level 2 files constituting a TEMPO East\-West scan cycle. The
rasters contain information on formaldehyde vertical columns,
ancillary data used in air mass factor calculations and reference sector
or de\-striping corrections, and retrieval quality flags.
The re\-gridding algorithm uses an area\-weighted approach.


* A version of this dataset with QA filters applied is available as [NASA/TEMPO/HCHO\_L3\_QA](/earth-engine/datasets/catalog/NASA_TEMPO_HCHO_L3_QA)
* [General Documentation](https://asdc.larc.nasa.gov/documents/tempo/guide/TEMPO_Level-2-3_trace_gas_clouds_user_guide_V1.2.pdf)





### Bands



**Pixel Size**
  
2226 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `weight` | km^2 | Sum of Level 2 pixel overlap areas. Represents the weighting factor for each grid cell, indicating the fraction of the grid cell area with valid data. |
| `vertical_column` | molecules/cm^2 | HCHO vertical column |
| `vertical_column_uncertainty` | molecules/cm^2 | HCHO vertical column uncertainty |
| `main_data_quality_flag` | Dimensionless | Main data quality flag. Provides an overall assessment of the data quality |
| `num_vertical_column_samples` | Dimensionless | Number of vertical column samples |
| `min_vertical_column_sample` | molecules/cm^2 | Smallest vertical column sample |
| `max_vertical_column_sample` | molecules/cm^2 | Largest vertical column sample |
| `solar_zenith_angle` | deg | Solar zenith angle at pixel center |
| `viewing_zenith_angle` | deg | Viewing zenith angle at pixel center |
| `relative_azimuth_angle` | deg | Relative azimuth angle at pixel center |
| `surface_pressure` | hPa | Surface pressure |
| `terrain_height` | m | Terrain height |
| `snow_ice_fraction` | Dimensionless | Fraction of pixel area covered by snow and/or ice |
| `fitted_slant_column` | molecules/cm^2 | HCHO fitted slant column |
| `fitted_slant_column_uncertainty` | molecules/cm^2 | HCHO fitted slant column uncertainty |
| `albedo` | Dimensionless | Surface albedo |
| `amf` | Dimensionless | HCHO air mass factor |
| `eff_cloud_fraction` | Dimensionless | Effective cloud fraction |
| `amf_cloud_fraction` | Dimensionless | Cloud radiance fraction for AMF calculation |
| `amf_cloud_pressure` | hPa | Cloud pressure for AMF calculation |


**main\_data\_quality\_flag Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | good |
| 1 | None | suspect |
| 2 | None | bad |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* NASA/LARC/SD/ASDC. (n.d.). TEMPO gridded HCHO vertical columns V03
(PROVISIONAL) \[Data set]. NASA Langley
Atmospheric Science Data Center DAAC.
Retrieved from https://doi.org/10\.5067/IS\-40e/TEMPO/HCHO\_L3\.003





### DOIs


* [https://doi.org/10\.5067/IS\-40e/TEMPO/HCHO\_L3\.003](https://doi.org/10.5067/IS-40e/TEMPO/HCHO_L3.003)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcollection=ee.ImageCollection('NASA/TEMPO/HCHO_L3')
.filterDate('2024-04-01','2024-04-05')

varvisParams={
min:0,
max:1.5e16,
bands:['vertical_column'],
palette:[
'000080','0000D9','4000FF','8000FF','0080FF',
'00D9FF','80FFFF','FF8080','D90000','800000'
]
};
Map.setCenter(-95.06,42.02,3)
Map.addLayer(collection,visParams,'HCHO vertical column')
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_TEMPO_HCHO_L3)


[TEMPO gridded HCHO vertical columns V03](/earth-engine/datasets/catalog/NASA_TEMPO_HCHO_L3)

Formaldehyde Level 3 collection provides trace gas information on a regular grid covering the TEMPO field of regard for nominal TEMPO observations. Level 3 files are derived by combining information from all Level 2 files constituting a TEMPO East\-West scan cycle. The rasters contain information on formaldehyde vertical columns, ancillary …

 NASA/TEMPO/HCHO\_L3,
 air\-quality,formaldehyde,nasa,pollution,satellite\-imagery,tropomi

2023\-08\-01T00:00:00Z/2025\-07\-16T12:33:53Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/IS\-40e/TEMPO/HCHO\_L3\.003](https://doi.org/https://asdc.larc.nasa.gov/)
* [https://doi.org/10\.5067/IS\-40e/TEMPO/HCHO\_L3\.003](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_TEMPO_HCHO_L3)









