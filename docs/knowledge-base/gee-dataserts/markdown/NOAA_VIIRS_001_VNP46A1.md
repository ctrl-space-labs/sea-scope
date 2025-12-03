



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP46A1: VIIRS Daily Gridded Day Night Band 500m Linear Lat Lon Grid Night


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================================================








Dataset Availability
2012\-01\-19T00:00:00Z–2025\-01\-02T00:00:00Z
Dataset Provider


[NASA LAADS DAAC](https://doi.org/10.5067/VIIRS/VNP46A1.001)



Earth Engine Snippet


`ee.ImageCollection("NOAA/VIIRS/001/VNP46A1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_VIIRS_001_VNP46A1)





Cadence
1 Day
Tags


[daily](/earth-engine/datasets/tags/daily)
[dnb](/earth-engine/datasets/tags/dnb)
[nasa](/earth-engine/datasets/tags/nasa)
[noaa](/earth-engine/datasets/tags/noaa)
[population](/earth-engine/datasets/tags/population)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The Suomi National Polar\-orbiting Partnership (SNPP) Visible Infrared
Imaging Radiometer Suite (VIIRS) supports a Day\-Night Band (DNB) sensor
that provides global daily measurements of nocturnal visible and
near\-infrared (NIR) light that are suitable for Earth system science and
applications. The VIIRS DNB's ultra\-sensitivity in lowlight conditions
enables us to generate a new set of science\-quality nighttime products that
manifest substantial improvements in sensor resolution and calibration when
compared to the previous era of Defense Meteorological Satellite
Program/Operational Linescan System's (DMSP/OLS) nighttime lights image
products.


VNP46A1 is a daily, top\-of\-atmosphere, at\-sensor nighttime radiance product
called VIIRS/NPP Daily Gridded Day Night Band 15 arc\-second Linear Lat Lon
Grid Night. The product contains 26 Science Data Sets (SDS) that include
sensor radiance, zenith and azimuth angles (at\-sensor, solar, and lunar),
cloud\-mask flags, time, shortwave IR radiance, brightness temperatures,
VIIRS quality flags, moon phase angle, and moon illumination fraction. It
also provides Quality Flag (QF) information specific to the cloud\-mask,
VIIRS moderate\-resolution bands M10, M11, M12, M13, M15, M16, and DNB.


Documentation:


* [User's Guide](https://ladsweb.modaps.eosdis.nasa.gov/api/v2/content/archives/Document%20Archive/Science%20Data%20Product%20Documentation/VIIRS_Black_Marble_UG_v1.3_Sep_2022.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://ladsweb.modaps.eosdis.nasa.gov/api/v2/content/archives/Document%20Archive/Science%20Data%20Product%20Documentation/Product%20Generation%20Algorithms/VIIRS_Black_Marble_ATBD_v1.1_July_2020.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/missions-and-measurements/products/VNP46A1/)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Min | Max | Offset | Description |
| --- | --- | --- | --- | --- | --- |
| `BrightnessTemperature_M12` | K | 0 | 163\.835 | 203 | Brightness temperature of band M12 |
| `BrightnessTemperature_M13` | K | 0 | 163\.835 | 203 | Brightness temperature of band M13 |
| `BrightnessTemperature_M15` | K | 0 | 163\.835 | 111 | Brightness temperature of band M15 |
| `BrightnessTemperature_M16` | K | 0 | 163\.835 | 103 | Brightness temperature of band M16 |
| `DNB_At_Sensor_Radiance_500m` | None | 0 | 6553\.4 |  | At\-sensor DNB radiance |
| `Glint_Angle` | deg | \-180 | 180 |  | Moon glint angle |
| `Granule` | None | 0 | 254 |  | Number of selected Granule |
| `Lunar_Zenith` | deg | 0 | 180 |  | Lunar zenith angle |
| `Lunar_Azimuth` | deg | \-180 | 180 |  | Lunar azimuth angle |
| `Moon_Illumination_Fraction` | % | 0 | 100 |  | Moon illumination fraction |
| `Moon_Phase_Angle` | deg | 0 | 180 |  | Moon phase angle |
| `QF_Cloud_Mask` | None |  | Quality flag for cloud mask |
| Bitmask for QF\_Cloud\_Mask * Bit 0: Day/Night 	+ 0: Night 	+ 1: Day * Bits 1\-3: Land/Water Background 	+ 0: Land \& Desert 	+ 1: Land no Desert 	+ 2: Inland Water 	+ 3: Sea Water 	+ 5: Coastal * Bits 4\-5: Cloud Mask Quality 	+ 0: Poor 	+ 1: Low 	+ 2: Medium 	+ 3: High * Bits 6\-7: Cloud Detection Results \& Confidence Indicator 	+ 0: Confident Clear 	+ 1: Probably Clear 	+ 2: Probably Cloudy 	+ 3: Confident Cloudy * Bit 8: Shadow Detected 	+ 0: No 	+ 1: Yes * Bit 9: Cirrus Detection (IR) (BTM15 \- BTM16\) 	+ 0: No cloud 	+ 1: Cloud * Bit 10: Snow/Ice Surface 	+ 0: No Snow/Ice 	+ 1: Snow/Ice | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `QF_DNB` | None | 0 | 65534 |  | DNB quality flag |
| `QF_VIIRS_M10` | None | 0 | 65534 |  | Quality flag of band M10 |
| `QF_VIIRS_M11` | None | 0 | 65534 |  | Quality flag of band M11 |
| `QF_VIIRS_M12` | None | 0 | 65534 |  | Quality flag of band M12 |
| `QF_VIIRS_M13` | None | 0 | 65534 |  | Quality flag of band M13 |
| `QF_VIIRS_M15` | None | 0 | 65534 |  | Quality flag of band M15 |
| `QF_VIIRS_M16` | None | 0 | 65534 |  | Quality flag of band M16 |
| `Radiance_M10` | None | 0 | 85\.1942 | \-0\.04 | Radiance in band M10 |
| `Radiance_M11` | None | 0 | 38\.0097 | \-0\.02 | Radiance in band M11 |
| `Sensor_Azimuth` | deg | \-180 | 180 |  | Sensor azimuth angle |
| `Sensor_Zenith` | deg | 0 | 90 |  | Sensor zenith angle |
| `Solar_Azimuth` | deg | \-180 | 180 |  | Solar azimuth angle |
| `Solar_Zenith` | deg | 0 | 180 |  | Solar zenith angle |
| `UTC_Time` | h | 0 | 24 |  | UTC time |


**QF\_DNB Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | None | Substitute\_Cal |
| 2 | None | Out\_of\_Range |
| 4 | None | Saturation |
| 8 | None | Temp\_not\_Nominal |
| 16 | None | Stray\_light |
| 256 | None | Bowtie\_Deleted |
| 512 | None | Missing\_EV |
| 1024 | None | Cal\_Fail |
| 2048 | None | Dead\_Detector |


**QF\_VIIRS\_M10 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | None | Substitute\_Cal |
| 2 | None | Out\_of\_Range |
| 4 | None | Saturation |
| 8 | None | Temp\_not\_Nominal |
| 256 | None | Bowtie\_Deleted |
| 512 | None | Missing\_EV |
| 1024 | None | Cal\_Fail |
| 2048 | None | Dead\_Detector |


**QF\_VIIRS\_M11 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | None | Substitute\_Cal |
| 2 | None | Out\_of\_Range |
| 4 | None | Saturation |
| 8 | None | Temp\_not\_Nominal |
| 256 | None | Bowtie\_Deleted |
| 512 | None | Missing\_EV |
| 1024 | None | Cal\_Fail |
| 2048 | None | Dead\_Detector |


**QF\_VIIRS\_M12 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | None | Substitute\_Cal |
| 2 | None | Out\_of\_Range |
| 4 | None | Saturation |
| 8 | None | Temp\_not\_Nominal |
| 256 | None | Bowtie\_Deleted |
| 512 | None | Missing\_EV |
| 1024 | None | Cal\_Fail |
| 2048 | None | Dead\_Detector |


**QF\_VIIRS\_M13 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | None | Substitute\_Cal |
| 2 | None | Out\_of\_Range |
| 4 | None | Saturation |
| 8 | None | Temp\_not\_Nominal |
| 256 | None | Bowtie\_Deleted |
| 512 | None | Missing\_EV |
| 1024 | None | Cal\_Fail |
| 2048 | None | Dead\_Detector |


**QF\_VIIRS\_M15 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | None | Substitute\_Cal |
| 2 | None | Out\_of\_Range |
| 4 | None | Saturation |
| 8 | None | Temp\_not\_Nominal |
| 256 | None | Bowtie\_Deleted |
| 512 | None | Missing\_EV |
| 1024 | None | Cal\_Fail |
| 2048 | None | Dead\_Detector |


**QF\_VIIRS\_M16 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | None | Substitute\_Cal |
| 2 | None | Out\_of\_Range |
| 4 | None | Saturation |
| 8 | None | Temp\_not\_Nominal |
| 256 | None | Bowtie\_Deleted |
| 512 | None | Missing\_EV |
| 1024 | None | Cal\_Fail |
| 2048 | None | Dead\_Detector |




### Terms of Use


**Terms of Use**


LP DAAC NASA data are freely accessible; however, when an author
publishes these data or works based on the data, it is requested that the
author cite the datasets within the text of the publication and include a
reference to them in the reference list.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)





### DOIs


* [https://doi.org/10\.5067/VIIRS/VNP46A1\.001](https://doi.org/10.5067/VIIRS/VNP46A1.001)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/VIIRS/001/VNP46A1').filter(
ee.Filter.date('2013-01-01','2013-07-01'));

// At-sensor Day/night Band radiance (DNB).
vardnb=dataset.select('DNB_At_Sensor_Radiance_500m');
vardnbVis={
min:0,
max:50,
palette:['black','purple','cyan','green','yellow','red','white'],
};

Map.setCenter(-79.4,43.1,8);

Map.addLayer(dnb,dnbVis,'Day-Night Band (DNB) at sensor radiance 500m');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_VIIRS_001_VNP46A1)


[VNP46A1: VIIRS Daily Gridded Day Night Band 500m Linear Lat Lon Grid Night](/earth-engine/datasets/catalog/NOAA_VIIRS_001_VNP46A1)

The Suomi National Polar\-orbiting Partnership (SNPP) Visible Infrared Imaging Radiometer Suite (VIIRS) supports a Day\-Night Band (DNB) sensor that provides global daily measurements of nocturnal visible and near\-infrared (NIR) light that are suitable for Earth system science and applications. The VIIRS DNB's ultra\-sensitivity in lowlight conditions enables us to generate …

 NOAA/VIIRS/001/VNP46A1,
 daily,dnb,nasa,noaa,population,viirs

2012\-01\-19T00:00:00Z/2025\-01\-02T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP46A1\.001](https://doi.org/https://doi.org/10.5067/VIIRS/VNP46A1.001)
* [https://doi.org/10\.5067/VIIRS/VNP46A1\.001](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_VIIRS_001_VNP46A1)









