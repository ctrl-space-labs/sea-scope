



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP13A1\.002: VIIRS Vegetation Indices 16\-Day 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================








Dataset Availability
2012\-01\-17T00:00:00Z–2025\-06\-10T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/VIIRS/VNP13A1.002)



Earth Engine Snippet


`ee.ImageCollection("NASA/VIIRS/002/VNP13A1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP13A1)





Cadence
8 Days
Tags


[16\-day](/earth-engine/datasets/tags/16-day)
[evi](/earth-engine/datasets/tags/evi)
[nasa](/earth-engine/datasets/tags/nasa)
[ndvi](/earth-engine/datasets/tags/ndvi)
[noaa](/earth-engine/datasets/tags/noaa)
[npp](/earth-engine/datasets/tags/npp)
[vegetation](/earth-engine/datasets/tags/vegetation)
[vegetation\-indices](/earth-engine/datasets/tags/vegetation-indices)
[viirs](/earth-engine/datasets/tags/viirs)
vnp13a1








#### Description



The Suomi National Polar\-Orbiting Partnership (S\-NPP) NASA Visible
Infrared Imaging Radiometer Suite (VIIRS) Vegetation Indices (VNP13A1\)
data product provides vegetation indices by a process of
selecting the best available pixel over a 16\-day acquisition period
at 500 meter resolution. The VNP13 data products are designed
after the Moderate Resolution Imaging Spectroradiometer (MODIS)
Terra and Aqua Vegetation Indices product suite to promote the
continuity of the Earth Observation System (EOS) mission.


The VNP13 algorithm process produces three vegetation indices: (1\)
Normalized Difference Vegetation Index (NDVI), (2\) the Enhanced
Vegetation Index (EVI), and (3\) Enhanced Vegetation Index\-2 (EVI2\).
(1\) NDVI is one of the longest continual remotely sensed time series
observations, using both the red and near\-infrared (NIR) bands.
(2\) EVI is a slightly different vegetation index that is more sensitive
to canopy cover, while NDVI is more sensitive to chlorophyll. (3\) EVI2
is a reformation of the standard 3\-band EVI, using the red band and
NIR band. This reformation addresses arising issues when comparing
VIIRS EVI to other EVI models that do not include a blue band. EVI2
will eventually become the standard EVI.


Along with the three Vegetation Indices layers, this product also
includes layers for near\-infrared (NIR) reflectance; three shortwave
infrared (SWIR) reflectance\-red, blue, and green reflectance; composite
day of year; pixel reliability; view and sun angles, and a quality layer.


For additional information, visit the VIIRS [Land Product Quality
Assessment website](https://landweb.modaps.eosdis.nasa.gov/browse?sensor=VIIRS&sat=SNPP) and see
the [User Guide](https://lpdaac.usgs.gov/documents/1372/VNP13_User_Guide_ATBD_V2.1.2.pdf).


Documentation:


* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/VIIRS/1/VNP13A1)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Wavelength | Description |
| --- | --- | --- | --- |
| `EVI` | None | None | 3 band Enhanced Vegetation Index |
| `EVI2` | None | None | 2 band Enhanced Vegetation Index |
| `NDVI` | None | None | Normalized Difference Vegetation Index |
| `NIR_reflectance` | None | 846\-885nm | Near\-infrared Radiation reflectance |
| `SWIR1_reflectance` | None | 1230\-1250nm | Shortwave Infrared Radiation reflectance |
| `SWIR2_reflectance` | None | 1580\-1640nm | Shortwave Infrared Radiation reflectance |
| `SWIR3_reflectance` | None | 2225\-2275nm | Shortwave Infrared Radiation reflectance |
| `VI_Quality` | None | None | Quality Assessment (QA) bit\-field. |
| Bitmask for VI\_Quality * Bits 0\-1: MODLAND\_QA 	+ 0: VI produced, good quality 	+ 1: VI produced, but check other QA 	+ 2: Pixel produced, but probably cloudy 	+ 3: Pixel not produced due to other reason than clouds * Bits 2\-5: VI Usefulness, higher values are worse. 	+ 0: Highest Quality 	+ 1: Lower quality 	+ 2: Decreasing quality 	+ 3: Decreasing quality 	+ 4: Decreasing quality 	+ 5: Decreasing quality 	+ 6: Decreasing quality 	+ 7: Decreasing quality 	+ 8: Decreasing quality 	+ 9: Decreasing quality 	+ 10: Decreasing quality 	+ 11: Decreasing quality 	+ 12: Worst quality 	+ 13: Quality so low that it is not useful 	+ 14: L1B data faulty 	+ 15: Not useful for any reason/not processed * Bits 6\-7: Aerosol quantity 	+ 0: Climatology 	+ 1: Low 	+ 2: Average 	+ 3: High * Bit 8: Adjacent cloud detected 	+ 0: No 	+ 1: Yes * Bit 9: Adjacent BRDF correction performed 	+ 0: No 	+ 1: Yes * Bit 10: Mixed clouds 	+ 0: No 	+ 1: Yes * Bits 11\-13: Land/Water Flag 	+ 0: land \& desert 	+ 1: land no desert 	+ 2: inland water 	+ 3: sea\_water 	+ 5: coastal * Bit 14: Possible snow/ice 	+ 0: No 	+ 1: Yes * Bit 15: Possible shadow 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `red_reflectance` | None | 600\-680nm | Red band reflectance |
| `green_reflectance` | None | 545\-656nm | Green band reflectance |
| `blue_reflectance` | None | 478\-498nm | Blue band reflectance |
| `composite_day_of_the_year` | d | None | Julian day of year |
| `pixel_reliability` | None | None | Pixel usefulness using a simple rank class |
| `relative_azimuth_angle` | deg | None | Relative azimuth angle for each pixel |
| `sun_zenith_angle` | deg | None | Sun zenith angle for each pixel |
| `view_zenith_angle` | deg | None | View zenith angle for each pixel |


**pixel\_reliability Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | Excellent |
| 1 | None | Good |
| 2 | None | Acceptable |
| 3 | None | Marginal |
| 4 | None | Pass |
| 5 | None | Questionable |
| 6 | None | Poor |
| 7 | None | Cloud Shadow |
| 8 | None | Snow/Ice |
| 9 | None | Cloud |
| 10 | None | Estimated |
| 11 | None | LTAVG (taken from database) |




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


* [https://doi.org/10\.5067/VIIRS/VNP13A1\.002](https://doi.org/10.5067/VIIRS/VNP13A1.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/VIIRS/002/VNP13A1')
.filter(ee.Filter.date('2017-05-01','2017-06-30'));
varrgb=dataset.select(['EVI']);
varrgbVis={
min:0.0,
max:1.0,
palette:['000000','004400','008800','00bb00','00ff00'],
};
Map.setCenter(17.93,7.71,6);
Map.addLayer(rgb,rgbVis,'RGB');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP13A1)


[VNP13A1\.002: VIIRS Vegetation Indices 16\-Day 500m](/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP13A1)

The Suomi National Polar\-Orbiting Partnership (S\-NPP) NASA Visible Infrared Imaging Radiometer Suite (VIIRS) Vegetation Indices (VNP13A1\) data product provides vegetation indices by a process of selecting the best available pixel over a 16\-day acquisition period at 500 meter resolution. The VNP13 data products are designed after the Moderate Resolution Imaging …

 NASA/VIIRS/002/VNP13A1,
 16\-day,evi,nasa,ndvi,noaa,npp,vegetation,vegetation\-indices,viirs

2012\-01\-17T00:00:00Z/2025\-06\-10T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP13A1\.002](https://doi.org/https://doi.org/10.5067/VIIRS/VNP13A1.002)
* [https://doi.org/10\.5067/VIIRS/VNP13A1\.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP13A1)









