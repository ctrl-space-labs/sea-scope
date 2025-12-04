



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

ASTER L1T Radiance


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================








Dataset Availability
2000\-03\-04T00:00:00Z–2025\-07\-15T22:12:30Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/ASTER/AST_L1T.003)



Earth Engine Snippet


`ee.ImageCollection("ASTER/AST_L1T_003")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ASTER/ASTER_AST_L1T_003)





Revisit Interval
16 Days
Tags


[aster](/earth-engine/datasets/tags/aster)
[imagery](/earth-engine/datasets/tags/imagery)
[nasa](/earth-engine/datasets/tags/nasa)
[nir](/earth-engine/datasets/tags/nir)
[radiance](/earth-engine/datasets/tags/radiance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[swir](/earth-engine/datasets/tags/swir)
[terra](/earth-engine/datasets/tags/terra)
[thermal](/earth-engine/datasets/tags/thermal)
[toa](/earth-engine/datasets/tags/toa)
[usgs](/earth-engine/datasets/tags/usgs)
eos
tir
vnir








#### Description



**Note:**
There is a gap in data collection between November 28, 2024 and January 16,
2025 due to technical issues with the ASTER instrument. See the USGS
[announcement](https://lpdaac.usgs.gov/news/aster-resumes-limited-operations/)
for more information.


The Advanced Spaceborne Thermal Emission and Reflection Radiometer (ASTER)
is a multispectral imager that was launched on board NASA's Terra spacecraft
in December, 1999\. ASTER can collect data in 14 spectral bands from the
visible to the thermal infrared. Each scene covers an area of 60 x 60 km.
These scenes, produced by the USGS, contain calibrated at\-sensor radiance,
ortho\-rectified and terrain corrected.


Not all 14 bands were collected in each scene. An asset property named
ORIGINAL\_BANDS\_PRESENT contains the list of bands that are present in each
scene.


To convert from Digital Numbers (DN) to radiance at the sensor, the unit
conversion coefficients are available in the metadata. See
[ASTER L1T Product Users' Guide](https://lpdaac.usgs.gov/documents/647/AST__L1T_User_Guide_V3.pdf)
and [ASTER L1T Product Specification](https://lpdaac.usgs.gov/documents/300/ASTER_L1T_Product_Specification.pdf)
for more information.


Documentation:


* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/72/AST_L1T_ATBD.pdf)
* [User's Guide](https://lpdaac.usgs.gov/documents/647/AST__L1T_User_Guide_V3.pdf)
* [ASTER Level\-1T Product Specification](https://lpdaac.usgs.gov/documents/300/ASTER_L1T_Product_Specification.pdf)
* [ASTER L1T Quick Reference Guide](https://lpdaac.usgs.gov/documents/174/AST_L1T_Quick_Reference_Guide.pdf)





### Bands


**Bands**




| Name | Min | Max | Pixel Size | Wavelength | Description |
| --- | --- | --- | --- | --- | --- |
| `B01` | 1 | 255 | 0\.520\-0\.600μm | VNIR\_Band1 (visible green/yellow) |
| `B02` | 1 | 255 | 0\.630\-0\.690μm | VNIR\_Band2 (visible red) |
| `B3N` | 1 | 255 | 0\.780\-0\.860μm | VNIR\_Band3N (near infrared, nadir pointing) |
| `B04` | 1 | 255 | 1\.600\-1\.700μm | SWIR\_Band4 (short\-wave infrared) |
| `B05` | 1 | 255 | 2\.145\-2\.185μm | SWIR\_Band5 (short\-wave infrared) |
| `B06` | 1 | 255 | 2\.185\-2\.225μm | SWIR\_Band6 (short\-wave infrared) |
| `B07` | 1 | 255 | 2\.235\-2\.285μm | SWIR\_Band7 (short\-wave infrared) |
| `B08` | 1 | 255 | 2\.295\-2\.365μm | SWIR\_Band8 (short\-wave infrared) |
| `B09` | 1 | 255 | 2\.360\-2\.430μm | SWIR\_Band9 (short\-wave infrared) |
| `B10` | 1 | 4095 | 8\.125\-8\.475μm | TIR\_Band10 (thermal infrared) |
| `B11` | 1 | 4095 | 8\.475\-8\.825μm | TIR\_Band11 (thermal infrared) |
| `B12` | 1 | 4095 | 8\.925\-9\.275μm | TIR\_Band12 (thermal infrared) |
| `B13` | 1 | 4095 | 10\.250\-10\.950μm | TIR\_Band13 (thermal infrared) |
| `B14` | 1 | 4095 | 10\.950\-11\.650μm | TIR\_Band14 (thermal infrared) |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| BAD\_PIXELS\_B01 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B02 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B03 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B04 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B05 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B06 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B07 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B08 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B09 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B10 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B11 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B12 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B13 | DOUBLE | Number of bad pixels |
| BAD\_PIXELS\_B14 | DOUBLE | Number of bad pixels |
| CLOUDCOVER | DOUBLE | Cloud coverage |
| COARSE\_DEM\_DATE | STRING | Coarse DEM issuance date |
| COARSE\_DEM\_NOTE | STRING | Coarse DEM comments |
| COARSE\_DEM\_VERSION | STRING | Coarse DEM version number |
| FLYING\_DIRECTION | STRING | The satellite flight direction when observation is done: 'AS' \- ascending direction, 'DE' \- descending direction |
| GAIN\_COEFFICIENT\_B01 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B02 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B03 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B04 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B05 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B06 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B07 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B08 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B09 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B10 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B11 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B12 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B13 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_COEFFICIENT\_B14 | DOUBLE | Coefficient used for radiance conversion |
| GAIN\_SETTING\_B01 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B02 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B03 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B04 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B05 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B06 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B07 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B08 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B09 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B10 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B11 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B12 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B13 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GAIN\_SETTING\_B14 | STRING | Band gain setting: 'HGH' \- high, 'NOR' \- normal, 'LOW' \- low, 'LO1' \- low 1, or 'LO2' \- low 2 |
| GCP\_CHIPS\_CORRELATED | DOUBLE | How many chips correlated during correlation statistics creation |
| GEOMETRIC\_DB\_DATE | STRING | Geometric correction data issuance date |
| GEOMETRIC\_DB\_VERSION | STRING | Geometric correction data version number |
| GRANULE\_REPROCESSING | STRING | What reprocessing has been performed on the granule: 'not reprocessed', 'reprocessed once', 'reprocessed twice', or 'reprocessing n times' |
| ORBIT\_NUMBER | DOUBLE | The orbit number of the satellite when data is acquired |
| ORIGINAL\_BANDS\_PRESENT | STRING\_LIST | List of bands that are present in each scene |
| PGE\_VERSION | STRING | The version of PGE |
| PRODUCTION\_TIME | DOUBLE | Generation time of this product |
| QA\_PERCENT\_INTERPOLATED\_DATA | DOUBLE | The percentage of interpolated data in the scene |
| QA\_PERCENT\_MISSING\_DATA | DOUBLE | The percentage of missing data in the scene |
| QA\_PERCENT\_OUT\_OF\_BOUNDS\_DATA | DOUBLE | The percentage of out of bounds data in the scene |
| RADIOMETRIC\_DB\_DATE | STRING | Radiometric correction data issuance date |
| RADIOMETRIC\_DB\_VERSION | STRING | Radiometric correction data version number |
| RESAMPLING\_METHOD\_B01 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B02 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B03 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B04 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B05 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B06 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B07 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B08 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B09 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B10 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B11 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B12 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B13 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| RESAMPLING\_METHOD\_B14 | STRING | Resampling method: 'BL', 'NN', or 'CC' |
| SATELLITE\_RECURRENT\_CYCLENUMBER | DOUBLE | The satellite recurrent cycle number |
| SATELLITE\_REVOLUTION\_NUMBER | DOUBLE | The satellite revolution number in the cycle |
| SCENE\_PATH | DOUBLE | Scene path |
| SCENE\_ROW | DOUBLE | Scene row |
| SCENE\_VIEW | DOUBLE | Scene view |
| SOLAR\_AZIMUTH | DOUBLE | Sun direction as seen from the scene center; azimuth angle in degrees measured eastward from North (0\.0\<az\<360\) |
| SOLAR\_ELEVATION | DOUBLE | Sun direction as seen from the scene center; elevation angle in degrees (\-90\.0\<el\<90\.0\) |
| SOURCE\_DATA\_GRANULE | STRING | ID of input AST\_L1A data granule used for generating this product |
| SWIR\_POINTING\_ANGLE | DOUBLE | Pointing angle in degrees |
| TIR\_POINTING\_ANGLE | DOUBLE | Pointing angle in degrees |
| VNIR\_POINTING\_ANGLE | DOUBLE | Pointing angle in degrees |




### Terms of Use


**Terms of Use**


ASTER data and products distributed by the LP DAAC, with the exception of
the ASTER Global Digital Elevation Model (GDEM) dataset (ASTGTM) version 2
(v2\), have no restrictions on data use, sale, or subsequent redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/ASTER/AST\_L1T.003](https://doi.org/10.5067/ASTER/AST_L1T.003)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('ASTER/AST_L1T_003')
.filter(ee.Filter.date('2018-01-01','2018-08-15'));
varfalseColor=dataset.select(['B3N','B02','B01']);
varfalseColorVis={
min:0.0,
max:255.0,
};
Map.setCenter(-122.0272,39.6734,11);
Map.addLayer(falseColor.median(),falseColorVis,'False Color');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ASTER/ASTER_AST_L1T_003)


[ASTER L1T Radiance](/earth-engine/datasets/catalog/ASTER_AST_L1T_003)

Note: There is a gap in data collection between November 28, 2024 and January 16, 2025 due to technical issues with the ASTER instrument. See the USGS announcement for more information. The Advanced Spaceborne Thermal Emission and Reflection Radiometer (ASTER) is a multispectral imager that was launched on board NASA's …

 ASTER/AST\_L1T\_003,
 aster,imagery,nasa,nir,radiance,satellite\-imagery,swir,terra,thermal,toa,usgs

2000\-03\-04T00:00:00Z/2025\-07\-15T22:12:30Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/ASTER/AST\_L1T.003](https://doi.org/https://doi.org/10.5067/ASTER/AST_L1T.003)
* [https://doi.org/10\.5067/ASTER/AST\_L1T.003](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/ASTER_AST_L1T_003)









