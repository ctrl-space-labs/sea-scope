



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD43A1\.061 MODIS BRDF\-Albedo Model Parameters Daily 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-05T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD43A1.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD43A1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43A1)





Cadence
1 Day
Tags


[albedo](/earth-engine/datasets/tags/albedo)
[brdf](/earth-engine/datasets/tags/brdf)
[daily](/earth-engine/datasets/tags/daily)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[reflectance](/earth-engine/datasets/tags/reflectance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[usgs](/earth-engine/datasets/tags/usgs)
mcd43a1








#### Description



The MCD43A1 V6\.1 Bidirectional Reflectance Distribution
Function and Albedo (BRDF/Albedo) Model Parameters dataset is
a 500 meter daily 16\-day product. The Julian date represents
the 9th day of the 16\-day retrieval period, and consequently
the observations are weighted to estimate the BRDF/Albedo for
that day. The MCD43A1 algorithm, as is with all combined products,
chooses the best representative pixel from a pool that includes
all the acquisitions from both the Terra and Aqua sensors from
the retrieval period.


The MCD43A1 provides the three model
weighting parameters (isotropic, volumetric, and geometric) for
each of the MODIS bands 1 through 7 and the visible (vis), near
infrared (nir), and shortwave bands used to derive the Albedo
and BRDF products (MCD43A3 and MCD43A4\). The Mandatory Quality
layers for each of the 10 bands are supplied as well.


Documentation:


* [User's Guide](https://www.umb.edu/spectralmass/modis-user-guide-v006-and-v0061/mcd43a1-brdfalbedo-model-parameters-product/)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/97/MCD43_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MCD43A1)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Min | Max | Scale | Wavelength | Description |
| --- | --- | --- | --- | --- | --- |
| `BRDF_Albedo_Parameters_Band1_iso` | 0 | 32766 | 0\.001 | 620\-670nm | BDRF/Albedo isotropic parameter for band 1 |
| `BRDF_Albedo_Parameters_Band1_vol` | 0 | 32766 | 0\.001 | 620\-670nm | BDRF/Albedo volumetric parameter for band 1 |
| `BRDF_Albedo_Parameters_Band1_geo` | 0 | 32766 | 0\.001 | 620\-670nm | BDRF/Albedo geometric parameter for band 1 |
| `BRDF_Albedo_Parameters_Band2_iso` | 0 | 32766 | 0\.001 | 841\-876nm | BDRF/Albedo isotropic parameter for band 2 |
| `BRDF_Albedo_Parameters_Band2_vol` | 0 | 32766 | 0\.001 | 841\-876nm | BDRF/Albedo volumetric parameter for band 2 |
| `BRDF_Albedo_Parameters_Band2_geo` | 0 | 32766 | 0\.001 | 841\-876nm | BDRF/Albedo geometric parameter for band 2 |
| `BRDF_Albedo_Parameters_Band3_iso` | 0 | 32766 | 0\.001 | 459\-479nm | BDRF/Albedo isotropic parameter for band 3 |
| `BRDF_Albedo_Parameters_Band3_vol` | 0 | 32766 | 0\.001 | 459\-479nm | BDRF/Albedo volumetric parameter for band 3 |
| `BRDF_Albedo_Parameters_Band3_geo` | 0 | 32766 | 0\.001 | 459\-479nm | BDRF/Albedo geometric parameter for band 3 |
| `BRDF_Albedo_Parameters_Band4_iso` | 0 | 32766 | 0\.001 | 545\-565nm | BDRF/Albedo isotropic parameter for band 4 |
| `BRDF_Albedo_Parameters_Band4_vol` | 0 | 32766 | 0\.001 | 545\-565nm | BDRF/Albedo volumetric parameter for band 4 |
| `BRDF_Albedo_Parameters_Band4_geo` | 0 | 32766 | 0\.001 | 545\-565nm | BDRF/Albedo geometric parameter for band 4 |
| `BRDF_Albedo_Parameters_Band5_iso` | 0 | 32766 | 0\.001 | 1230\-1250nm | BDRF/Albedo isotropic parameter for band 5 |
| `BRDF_Albedo_Parameters_Band5_vol` | 0 | 32766 | 0\.001 | 1230\-1250nm | BDRF/Albedo volumetric parameter for band 5 |
| `BRDF_Albedo_Parameters_Band5_geo` | 0 | 32766 | 0\.001 | 1230\-1250nm | BDRF/Albedo geometric parameter for band 5 |
| `BRDF_Albedo_Parameters_Band6_iso` | 0 | 32766 | 0\.001 | 1628\-1652nm | BDRF/Albedo isotropic parameter for band 6 |
| `BRDF_Albedo_Parameters_Band6_vol` | 0 | 32766 | 0\.001 | 1628\-1652nm | BDRF/Albedo volumetric parameter for band 6 |
| `BRDF_Albedo_Parameters_Band6_geo` | 0 | 32766 | 0\.001 | 1628\-1652nm | BDRF/Albedo geometric parameter for band 6 |
| `BRDF_Albedo_Parameters_Band7_iso` | 0 | 32766 | 0\.001 | 2105\-2155nm | BDRF/Albedo isotropic parameter for band 7 |
| `BRDF_Albedo_Parameters_Band7_vol` | 0 | 32766 | 0\.001 | 2105\-2155nm | BDRF/Albedo volumetric parameter for band 7 |
| `BRDF_Albedo_Parameters_Band7_geo` | 0 | 32766 | 0\.001 | 2105\-2155nm | BDRF/Albedo geometric parameter for band 7 |
| `BRDF_Albedo_Parameters_vis_iso` | 0 | 32766 | 0\.001 | None | BDRF/Albedo isotropic parameter for the visible band |
| `BRDF_Albedo_Parameters_vis_vol` | 0 | 32766 | 0\.001 | None | BDRF/Albedo volumetric parameter for the visible band |
| `BRDF_Albedo_Parameters_vis_geo` | 0 | 32766 | 0\.001 | None | BDRF/Albedo geometric parameter for the visible band |
| `BRDF_Albedo_Parameters_nir_iso` | 0 | 32766 | 0\.001 | 858nm | BDRF/Albedo isotropic parameter for the NIR band |
| `BRDF_Albedo_Parameters_nir_vol` | 0 | 32766 | 0\.001 | 858nm | BDRF/Albedo volumetric parameter for the NIR band |
| `BRDF_Albedo_Parameters_nir_geo` | 0 | 32766 | 0\.001 | 858nm | BDRF/Albedo geometric parameter for the NIR band |
| `BRDF_Albedo_Parameters_shortwave_iso` | 0 | 32766 | 0\.001 | None | BDRF/Albedo isotropic parameter for the shortwave band |
| `BRDF_Albedo_Parameters_shortwave_vol` | 0 | 32766 | 0\.001 | None | BDRF/Albedo volumetric parameter for the shortwave band |
| `BRDF_Albedo_Parameters_shortwave_geo` | 0 | 32766 | 0\.001 | None | BDRF/Albedo geometric parameter for the shortwave band |
| `BRDF_Albedo_Band_Mandatory_Quality_Band1` |  | None | BRDF albedo mandatory quality for band 1 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band1 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band2` |  | None | BRDF albedo mandatory quality for band 2 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band2 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band3` |  | None | BRDF albedo mandatory quality for band 3 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band3 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band4` |  | None | BRDF albedo mandatory quality for band 4 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band4 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band5` |  | None | BRDF albedo mandatory quality for band 5 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band5 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band6` |  | None | BRDF albedo mandatory quality for band 6 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band6 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_Band7` |  | None | BRDF albedo mandatory quality for band 7 |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_Band7 * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_vis` |  | None | BRDF albedo mandatory quality for visible broadband |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_vis * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_nir` |  | None | BRDF albedo mandatory quality for NIR broadband |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_nir * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Mandatory_Quality_shortwave` |  | None | BRDF albedo mandatory quality for shortwave broadband |
| Bitmask for BRDF\_Albedo\_Band\_Mandatory\_Quality\_shortwave * Bit 0: Mandatory QA bit index 	+ 0: Processed, good quality (full BRDF inversions) 	+ 1: Processed, see other QA (magnitude BRDF inversions) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD43A1\.061](https://doi.org/10.5067/MODIS/MCD43A1.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MCD43A1')
.filter(ee.Filter.date('2018-05-01','2018-07-01'));
vardefaultVisualization=dataset.select([
'BRDF_Albedo_Parameters_Band1_iso','BRDF_Albedo_Parameters_Band4_iso',
'BRDF_Albedo_Parameters_Band3_iso'
]);
vardefaultVisualizationVis={
min:0.0,
max:1400.0,
gamma:2.0,
};
Map.setCenter(6.746,46.529,6);
Map.addLayer(
defaultVisualization,defaultVisualizationVis,'Default visualization');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43A1)


[MCD43A1\.061 MODIS BRDF\-Albedo Model Parameters Daily 500m](/earth-engine/datasets/catalog/MODIS_061_MCD43A1)

The MCD43A1 V6\.1 Bidirectional Reflectance Distribution Function and Albedo (BRDF/Albedo) Model Parameters dataset is a 500 meter daily 16\-day product. The Julian date represents the 9th day of the 16\-day retrieval period, and consequently the observations are weighted to estimate the BRDF/Albedo for that day. The MCD43A1 algorithm, as is …

 MODIS/061/MCD43A1,
 albedo,brdf,daily,global,modis,nasa,reflectance,satellite\-imagery,usgs

2000\-02\-24T00:00:00Z/2025\-07\-05T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD43A1\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD43A1.061)
* [https://doi.org/10\.5067/MODIS/MCD43A1\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD43A1)









