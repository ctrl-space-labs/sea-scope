



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD43A2\.061 MODIS BRDF\-Albedo Quality Daily 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================








Dataset Availability
2000\-02\-24T00:00:00Z–2025\-07\-05T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD43A2.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD43A2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43A2)





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
quality








#### Description



The MCD43A2 V6\.1 Bidirectional Reflectance Distribution
Function and Albedo (BRDF/Albedo) Quality dataset is a 500 meter
daily 16\-day product. It contains all the quality information
for the corresponding 16\-day MCD43A3 Albedo and the MCD43A4 Nadir\-BRDF
(NBAR) products.


The MCD43A2 contains individual band quality
and observation information for the MODIS land bands
1\-7, along with the overall BRDF/Albedo quality information.


See
[dataset user guide](https://www.umb.edu/spectralmass/terra_aqua_modis/v006/mcd43a2_albedo_product)
for more information.


Documentation:


* [User's Guide](https://www.umb.edu/spectralmass/terra_aqua_modis/v006)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/97/MCD43_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MCD43A2)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `Snow_BRDF_Albedo` | None |  | Snow\-free or snow BRDF/albedo retrieved |
| Bitmask for Snow\_BRDF\_Albedo * Bit 0: Mandatory QA 	+ 0: Snow\-free albedo retrieved 	+ 1: Snow albedo retrieved | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Platform` | None |  | BRDF albedo platform information |
| Bitmask for BRDF\_Albedo\_Platform * Bits 0\-1: Platform 	+ 0: Terra 	+ 1: Terra/Aqua 	+ 2: Aqua | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_LandWaterType` | None |  | Land/water type |
| Bitmask for BRDF\_Albedo\_LandWaterType * Bits 0\-2: Land/water type 	+ 0: Shallow ocean 	+ 1: Land (nothing else but land) 	+ 2: Ocean coastlines and lake shorelines 	+ 3: Shallow inland water 	+ 4: Ephemeral water 	+ 5: Deep inland water 	+ 6: Moderate or continental ocean 	+ 7: Deep ocean | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_LocalSolarNoon` | deg | 0 | 254 |  | Solar zenith angle of local solar noon |
| `BRDF_Albedo_ValidObs_Band1` | None |  | Valid observation for band 1 |
| Bitmask for BRDF\_Albedo\_ValidObs\_Band1 * Bit 0: Day 1 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 1: Day 2 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 2: Day 3 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 3: Day 4 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 4: Day 5 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 5: Day 6 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 6: Day 7 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 7: Day 8 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 8: Day 9 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 9: Day 10 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 10: Day 11 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 11: Day 12 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 12: Day 13 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 13: Day 14 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 14: Day 15 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation * Bit 15: Day 16 reflectance quality 	+ 0: Observation not used 	+ 1: Valid clear observation | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_ValidObs_Band2` | None |  | Valid observation for band 2 (same bit meaning as in band 1\) |
| `BRDF_Albedo_ValidObs_Band3` | None |  | Valid observation for band 3 (same bit meaning as in band 1\) |
| `BRDF_Albedo_ValidObs_Band4` | None |  | Valid observation for band 4 (same bit meaning as in band 1\) |
| `BRDF_Albedo_ValidObs_Band5` | None |  | Valid observation for band 5 (same bit meaning as in band 1\) |
| `BRDF_Albedo_ValidObs_Band6` | None |  | Valid observation for band 6 (same bit meaning as in band 1\) |
| `BRDF_Albedo_ValidObs_Band7` | None |  | Valid observation for band 7 (same bit meaning as in band 1\) |
| `BRDF_Albedo_Band_Quality_Band1` | None |  | BRDF inversion information for band 1 |
| Bitmask for BRDF\_Albedo\_Band\_Quality\_Band1 * Bits 0\-2: BRDF inversion information for band 1 	+ 0: Best quality, full inversion (WoDs and RMSE are good) 	+ 1: Good quality, full inversion (also including 	the cases with no clear sky observations over the day of 	interest and those with a Solar Zenith Angle that is \> 	70 degrees even though WoDs and RMSE majority are good) 	+ 2: Magnitude inversion (numobs \>\= 7\) 	+ 3: Magnitude inversion (numobs \>\= 2 \& \< 7\) 	+ 4: Fill value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Quality_Band2` | None |  | BRDF inversion information for band 2 |
| Bitmask for BRDF\_Albedo\_Band\_Quality\_Band2 * Bits 0\-2: BRDF inversion information for band 2 	+ 0: Best quality, full inversion (WoDs and RMSE are good) 	+ 1: Good quality, full inversion (also including 	the cases with no clear sky observations over the day of 	interest and those with a Solar Zenith Angle that is \> 	70 degrees even though WoDs and RMSE majority are good) 	+ 2: Magnitude inversion (numobs \>\= 7\) 	+ 3: Magnitude inversion (numobs \>\= 2 \& \< 7\) 	+ 4: Fill value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Quality_Band3` | None |  | BRDF inversion information for band 3 |
| Bitmask for BRDF\_Albedo\_Band\_Quality\_Band3 * Bits 0\-2: BRDF inversion information for band 3 	+ 0: Best quality, full inversion (WoDs and RMSE are good) 	+ 1: Good quality, full inversion (also including 	the cases with no clear sky observations over the day of 	interest and those with a Solar Zenith Angle that is \> 	70 degrees even though WoDs and RMSE majority are good) 	+ 2: Magnitude inversion (numobs \>\= 7\) 	+ 3: Magnitude inversion (numobs \>\= 2 \& \< 7\) 	+ 4: Fill value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Quality_Band4` | None |  | BRDF inversion information for band 4 |
| Bitmask for BRDF\_Albedo\_Band\_Quality\_Band4 * Bits 0\-2: BRDF inversion information for band 4 	+ 0: Best quality, full inversion (WoDs and RMSE are good) 	+ 1: Good quality, full inversion (also including 	the cases with no clear sky observations over the day of 	interest and those with a Solar Zenith Angle that is \> 	70 degrees even though WoDs and RMSE majority are good) 	+ 2: Magnitude inversion (numobs \>\= 7\) 	+ 3: Magnitude inversion (numobs \>\= 2 \& \< 7\) 	+ 4: Fill value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Quality_Band5` | None |  | BRDF inversion information for band 5 |
| Bitmask for BRDF\_Albedo\_Band\_Quality\_Band5 * Bits 0\-2: BRDF inversion information for band 5 	+ 0: Best quality, full inversion (WoDs and RMSE are good) 	+ 1: Good quality, full inversion (also including 	the cases with no clear sky observations over the day of 	interest and those with a Solar Zenith Angle that is \> 	70 degrees even though WoDs and RMSE majority are good) 	+ 2: Magnitude inversion (numobs \>\= 7\) 	+ 3: Magnitude inversion (numobs \>\= 2 \& \< 7\) 	+ 4: Fill value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Quality_Band6` | None |  | BRDF inversion information for band 6 |
| Bitmask for BRDF\_Albedo\_Band\_Quality\_Band6 * Bits 0\-2: BRDF inversion information for band 6 	+ 0: Best quality, full inversion (WoDs and RMSE are good) 	+ 1: Good quality, full inversion (also including 	the cases with no clear sky observations over the day of 	interest and those with a Solar Zenith Angle that is \> 	70 degrees even though WoDs and RMSE majority are good) 	+ 2: Magnitude inversion (numobs \>\= 7\) 	+ 3: Magnitude inversion (numobs \>\= 2 \& \< 7\) 	+ 4: Fill value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Band_Quality_Band7` | None |  | BRDF inversion information for band 7 |
| Bitmask for BRDF\_Albedo\_Band\_Quality\_Band7 * Bits 0\-2: BRDF inversion information for band 7 	+ 0: Best quality, full inversion (WoDs and RMSE are good) 	+ 1: Good quality, full inversion (also including 	the cases with no clear sky observations over the day of 	interest and those with a Solar Zenith Angle that is \> 	70 degrees even though WoDs and RMSE majority are good) 	+ 2: Magnitude inversion (numobs \>\= 7\) 	+ 3: Magnitude inversion (numobs \>\= 2 and \< 7\) 	+ 4: Fill value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `BRDF_Albedo_Uncertainty` | None | 0 | 32766 | 0\.001 | BRDF inversion information |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD43A2\.061](https://doi.org/10.5067/MODIS/MCD43A2.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MCD43A2')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
vardefaultVisualization=dataset.select('Snow_BRDF_Albedo');
vardefaultVisualizationVis={
min:0.0,
max:1.0,
};
Map.setCenter(6.746,46.529,6);
Map.addLayer(
defaultVisualization,defaultVisualizationVis,'Default visualization');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD43A2)


[MCD43A2\.061 MODIS BRDF\-Albedo Quality Daily 500m](/earth-engine/datasets/catalog/MODIS_061_MCD43A2)

The MCD43A2 V6\.1 Bidirectional Reflectance Distribution Function and Albedo (BRDF/Albedo) Quality dataset is a 500 meter daily 16\-day product. It contains all the quality information for the corresponding 16\-day MCD43A3 Albedo and the MCD43A4 Nadir\-BRDF (NBAR) products. The MCD43A2 contains individual band quality and observation information for the MODIS land …

 MODIS/061/MCD43A2,
 albedo,brdf,daily,global,modis,nasa,reflectance,satellite\-imagery,usgs

2000\-02\-24T00:00:00Z/2025\-07\-05T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD43A2\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD43A2.061)
* [https://doi.org/10\.5067/MODIS/MCD43A2\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD43A2)









