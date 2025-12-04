



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP14A1\.002: Thermal Anomalies/Fire Daily L3 Global 1km SIN Grid


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================================








Dataset Availability
2012\-01\-19T00:00:00Z–2025\-07\-07T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/VIIRS/VNP14A1.002)



Earth Engine Snippet


`ee.ImageCollection("NASA/VIIRS/002/VNP14A1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP14A1)





Cadence
1 Day
Tags


[fire](/earth-engine/datasets/tags/fire)
[land](/earth-engine/datasets/tags/land)
[nasa](/earth-engine/datasets/tags/nasa)
[noaa](/earth-engine/datasets/tags/noaa)
[surface](/earth-engine/datasets/tags/surface)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The daily Suomi National Polar\-Orbiting Partnership NASA Visible Infrared
Imaging Radiometer Suite (VIIRS) Thermal Anomalies/Fire (VNP14A1\) Version 1
data product provides daily information about active fires and other thermal
anomalies. The VNP14A1 data product is a global, 1km gridded composite of
fire pixels detected from VIIRS 750m bands over a daily (24\-hour) period.
The VNP14 data products are designed after the Moderate Resolution Imaging
Spectroradiometer (MODIS) Thermal Anomalies/Fire product suite.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/427/VNP14_User_Guide_V1.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/427/VNP14_User_Guide_V1.pdf)
* [General Documentation](https://lpdaac.usgs.gov/products/vnp14a1v002/)
* [Land Product Quality Assessment website](https://landweb.modaps.eosdis.nasa.gov/browse?sensor=VIIRS&sat=SNPP)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `FireMask` | None | Confidence of fire. |
| `MaxFRP` | MW | Maximum Fire Radiative Power |
| `QA` | None | Global Land Surface Phenology Quality Control |
| Bitmask for QA * Bits 0\-1: land/water state 	+ 0: water 	+ 1: coast 	+ 2: land 	+ 3: unused * Bit 2: EDR ground trim zone 	+ 0: false 	+ 1: true * Bit 3: atmospheric correction performed 	+ 0: no 	+ 1: yes * Bit 4: day/night algorithm 	+ 0: night 	+ 1: day * Bit 5: potential fire pixel 	+ 0: false 	+ 1: true * Bit 6: Unused0 	+ 0: Unused value * Bits 7\-10: background window size parameter * Bits 11\-16: individual detection test flags 	+ 0: fail 	+ 1: pass * Bits 17\-19: Unused1 	+ 0: Unused value * Bit 20: adjacent cloud pixel 	+ 0: no 	+ 1: yes * Bit 21: adjacent water pixel 	+ 0: no 	+ 1: yes * Bits 22\-23: Sun glint level 	+ 0: Sun glint level \- 1 	+ 1: Sun glint level \- 2 	+ 2: Sun glint level \- 3 	+ 3: Sun glint level \- 4 * Bits 24\-28: individual rejection test flags 	+ 0: false 	+ 1: true * Bits 29\-31: Unused2 	+ 0: Unused value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `sample` | None | Sample number within a swath |


**FireMask Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | Not processed (no data or poor quality data) |
| 1 | None | Not processed (bowtie deletion) |
| 2 | None | Unused |
| 3 | None | Water |
| 4 | None | Cloud |
| 5 | None | Land |
| 6 | None | Unclassified |
| 7 | None | Low confidence fire pixel |
| 8 | None | Nominal confidence fire pixel |
| 9 | None | High confidence fire pixel |




### Terms of Use


**Terms of Use**


LP DAAC NASA data are freely accessible; however, when an author
publishes these data or works based on the data, it is requested that the
author cite the datasets within the text of the publication and include a
reference to them in the reference list.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/VIIRS/VNP14A1\.002](https://doi.org/10.5067/VIIRS/VNP14A1.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/VIIRS/002/VNP14A1')
.filter(ee.Filter.date('2017-05-01','2017-12-30'));
varvisualization={
bands:['MaxFRP'],
min:0.0,
max:1.0,
palette:['#00FF00','#00FFFF','#00FF00','#FFFFE0','#FFFFA0','#FFFF00'],
};
varlon=38.06;
varlat=-14.22;
Map.setCenter(lon,lat,6);
Map.addLayer(dataset,visualization,'MaxFRP');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP14A1)


[VNP14A1\.002: Thermal Anomalies/Fire Daily L3 Global 1km SIN Grid](/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP14A1)

The daily Suomi National Polar\-Orbiting Partnership NASA Visible Infrared Imaging Radiometer Suite (VIIRS) Thermal Anomalies/Fire (VNP14A1\) Version 1 data product provides daily information about active fires and other thermal anomalies. The VNP14A1 data product is a global, 1km gridded composite of fire pixels detected from VIIRS 750m bands over a …

 NASA/VIIRS/002/VNP14A1,
 fire,land,nasa,noaa,surface,viirs

2012\-01\-19T00:00:00Z/2025\-07\-07T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP14A1\.002](https://doi.org/https://doi.org/10.5067/VIIRS/VNP14A1.002)
* [https://doi.org/10\.5067/VIIRS/VNP14A1\.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP14A1)









