



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MYD09GQ.061 Aqua Surface Reflectance Daily Global 250m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================








Dataset Availability
2002\-07\-04T00:00:00Z–2025\-07\-13T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MYD09GQ.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MYD09GQ")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD09GQ)





Cadence
1 Day
Tags


[aqua](/earth-engine/datasets/tags/aqua)
[daily](/earth-engine/datasets/tags/daily)
[global](/earth-engine/datasets/tags/global)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sr](/earth-engine/datasets/tags/sr)
[surface\-reflectance](/earth-engine/datasets/tags/surface-reflectance)
[usgs](/earth-engine/datasets/tags/usgs)
myd09gq








#### Description



The MODIS Surface Reflectance products provide an estimate
of the surface spectral reflectance as it would be measured at
ground level in the absence of atmospheric scattering or absorption.
Low\-level data are corrected for atmospheric gases and aerosols.
MYD09GQ version 6\.1 provides bands 1 and 2 at a 250m resolution in
a daily gridded L2G product in the Sinusoidal projection, including
a QC and five observation layers. This product is meant to be used
in conjunction with the MYD09GA where important quality and viewing
geometry information is stored.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/306/MOD09_User_Guide_V6.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/305/MOD09_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MYD09GQ)





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Min | Max | Scale | Wavelength | Description |
| --- | --- | --- | --- | --- | --- |
| `num_observations` | 0 | 127 |  | None | Number of observations per 250m pixel |
| `sur_refl_b01` | \-100 | 16000 | 0\.0001 | 620\-670nm | Surface reflectance band 1 |
| `sur_refl_b02` | \-100 | 16000 | 0\.0001 | 841\-876nm | Surface reflectance for band 2 |
| `QC_250m` |  | None | Surface reflectance quality assurance |
| Bitmask for QC\_250m * Bits 0\-1: MODLAND QA bits 	+ 0: Corrected product produced at ideal quality \- all bands 	+ 1: Corrected product produced at less than ideal quality \- some or all bands 	+ 2: Corrected product not produced due to cloud effects \- all bands 	+ 3: Corrected product not produced for other reasons 	\- some or all bands, may be fill value (11\) \[Note that 	a value of (11\) overrides a value of (01\)] * Bits 2\-3: Spare (unused) 	+ 0: N/A * Bits 4\-7: Band 1 data quality 	+ 0: Highest quality 	+ 7: Noisy detector 	+ 8: Dead detector, data interpolated in L1B 	+ 9: Solar zenith \>\= 86 degrees 	+ 10: Solar zenith \>\= 85 and \< 86 degrees 	+ 11: Missing input 	+ 12: Internal constant used in place of climatological 	data for at least one atmospheric constant 	+ 13: Correction out of bounds, pixel constrained 	to extreme allowable value 	+ 14: L1B data faulty 	+ 15: Not processed due to deep ocean or clouds * Bits 8\-11: Band 2 data quality 	+ 0: Highest quality 	+ 7: Noisy detector 	+ 8: Dead detector, data interpolated in L1B 	+ 9: Solar zenith \>\= 86 degrees 	+ 10: Solar zenith \>\= 85 and \< 86 degrees 	+ 11: Missing input 	+ 12: Internal constant used in place of climatological 	data for at least one atmospheric constant 	+ 13: Correction out of bounds, pixel constrained to extreme allowable value 	+ 14: L1B data faulty 	+ 15: Not processed due to deep ocean or clouds * Bit 12: Atmospheric correction performed 	+ 0: No 	+ 1: Yes * Bit 13: Adjacency correction performed 	+ 0: No 	+ 1: Yes * Bits 14\-15: Spare (unused) 	+ 0: N/A | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `obscov` | 0 | 100 | 0\.01 | None | Observation coverage percent |
| `iobs_res` | 0 | 254 |  | None | Observation number |
| `orbit_pnt` | 0 | 15 |  | None | Orbit pointer |
| `granule_pnt` | 0 | 254 |  | None | Granule pointer |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MYD09GQ.061](https://doi.org/10.5067/MODIS/MYD09GQ.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MYD09GQ')
.filter(ee.Filter.date('2018-01-01','2018-05-01'));
varfalseColorVis={
min:-100.0,
max:8000.0,
bands:['sur_refl_b02','sur_refl_b02','sur_refl_b01'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(dataset,falseColorVis,'False Color');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD09GQ)


[MYD09GQ.061 Aqua Surface Reflectance Daily Global 250m](/earth-engine/datasets/catalog/MODIS_061_MYD09GQ)

The MODIS Surface Reflectance products provide an estimate of the surface spectral reflectance as it would be measured at ground level in the absence of atmospheric scattering or absorption. Low\-level data are corrected for atmospheric gases and aerosols. MYD09GQ version 6\.1 provides bands 1 and 2 at a 250m resolution …

 MODIS/061/MYD09GQ,
 aqua,daily,global,modis,nasa,satellite\-imagery,sr,surface\-reflectance,usgs

2002\-07\-04T00:00:00Z/2025\-07\-13T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MYD09GQ.061](https://doi.org/https://doi.org/10.5067/MODIS/MYD09GQ.061)
* [https://doi.org/10\.5067/MODIS/MYD09GQ.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MYD09GQ)









