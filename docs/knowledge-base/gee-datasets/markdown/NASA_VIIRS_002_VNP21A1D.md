



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP21A1D.002: Day Land Surface Temperature and Emissivity Daily 1km


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================================








Dataset Availability
2012\-01\-19T00:00:00Z–2025\-07\-04T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/VIIRS/VNP21A1D.002)



Earth Engine Snippet


`ee.ImageCollection("NASA/VIIRS/002/VNP21A1D")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP21A1D)





Cadence
1 Day
Tags


[climate](/earth-engine/datasets/tags/climate)
[daily](/earth-engine/datasets/tags/daily)
[day](/earth-engine/datasets/tags/day)
[land](/earth-engine/datasets/tags/land)
[nasa](/earth-engine/datasets/tags/nasa)
[noaa](/earth-engine/datasets/tags/noaa)
[surface](/earth-engine/datasets/tags/surface)
[temperature](/earth-engine/datasets/tags/temperature)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The NASA Suomi National Polar\-Orbiting Partnership (Suomi NPP) Visible
Infrared Imaging Radiometer Suite (VIIRS) Land Surface Temperature and
Emissivity (LST\&E) Day Version 1 product (VNP21A1D) is compiled daily
from daytime Level 2 Gridded (L2G) intermediate products.


The L2G process maps the daily VNP21 swath granules onto a sinusoidal MODIS
grid and stores all observations overlapping a gridded cell for a given
day. The VNP21A1 algorithm sorts through all these observations for each
cell and estimates the final LST value as an average from all cloud\-free
observations that have good LST accuracies. Only observations having
observation coverage more than a certain threshold (15%) are considered for
this averaging.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/429/VNP21_User_Guide_V1.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/1332/VNP21_ATBD_V1.pdf)
* [General Documentation](https://lpdaac.usgs.gov/products/vnp21a1dv002/)
* [Land Product Quality Assessment website](https://landweb.modaps.eosdis.nasa.gov/browse?sensor=VIIRS&sat=SNPP)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `LST_1KM` | K | Daily 1 km Land Surface Temperature. |
| `QC` | None | Daily Quality control for LST and emissivity |
| Bitmask for QC * Bits 0\-1: Mandatory QA flags 	+ 0: Pixel produced, good quality, no further QA info necessary 	+ 1: Pixel produced but unreliable quality 	+ 2: Pixel not produced due to cloud 	+ 3: Pixel not produced due to reasons other than cloud * Bits 2\-3: Data quality flag 	+ 0: Good data quality of L1B bands 14, 15, 16 	+ 1: Missing pixel 	+ 2: Fairly calibrated 	+ 3: Poorly calibrated, TES processing skipped * Bits 4\-5: Cloud Flag 	+ 0: Cloud\-free 	+ 1: Thin cirrus 	+ 2: Pixel within 2 pixels of nearest cloud 	+ 3: Cloudy pixels * Bits 6\-7: Iterations 	+ 0: Slow convergence 	+ 1: Nominal 	+ 2: Nominal 	+ 3: Fast * Bits 8\-9: Atmospheric Opacity 	+ 0: ≥3 (Warm, humid air; or cold land) 	+ 1: 0\.2 \- 0\.3 (Nominal value) 	+ 2: 0\.1 \- 0\.2 (Nominal value) 	+ 3: \<0\.1 (Dry, or high altitude pixel) * Bits 10\-11: MMD 	+ 0: \>0\.15 (Most silicate rocks) 	+ 1: 0\.1 \- 0\.15 (Rocks, sand, some soils) 	+ 2: 0\.03 \- 0\.1 (Mostly soils, mixed pixel) 	+ 3: \<0\.03 (Vegetation, snow, water, ice, some soils) * Bits 12\-13: Emissivity accuracy 	+ 0: \>0\.02 (Poor performance) 	+ 1: 0\.015 \- 0\.02 (Marginal performance) 	+ 2: 0\.01 \- 0\.015 (Good performance) 	+ 3: \<0\.01 (Excellent performance) * Bits 14\-15: LST accuracy 	+ 0: \>2K (Poor performance) 	+ 1: 1\.5 \- 2K (Marginal performance) 	+ 2: 1 \- 1\.5K (Good performance) 	+ 3: \<1K (Excellent performance) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `Emis_14` | None | Daily M14 emissivity |
| `Emis_15` | None | Daily M15 emissivity |
| `Emis_16` | None | Daily M16 emissivity |
| `View_Angle` | deg | View zenith angle of LST |
| `View_Time` | h | Time of LST observation |




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


* [https://doi.org/10\.5067/VIIRS/VNP21A1D.002](https://doi.org/10.5067/VIIRS/VNP21A1D.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/VIIRS/002/VNP21A1D')
.filter(ee.Filter.date('2022-11-01','2022-12-01'));

varvisualization={
bands:['LST_1KM'],
min:[150],
max:[300],
palette:[
'a50026',
'd73027',
'f46d43',
'fdae61',
'fee08b',
'ffffbf',
'd9ef8b',
'a6d96a',
'66bd63',
'1a9850',
'006837',
]
};
Map.setCenter(41.2,38.84,3);
Map.addLayer(dataset,visualization,'LST');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP21A1D)


[VNP21A1D.002: Day Land Surface Temperature and Emissivity Daily 1km](/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP21A1D)

The NASA Suomi National Polar\-Orbiting Partnership (Suomi NPP) Visible Infrared Imaging Radiometer Suite (VIIRS) Land Surface Temperature and Emissivity (LST\&E) Day Version 1 product (VNP21A1D) is compiled daily from daytime Level 2 Gridded (L2G) intermediate products. The L2G process maps the daily VNP21 swath granules onto a sinusoidal MODIS grid …

 NASA/VIIRS/002/VNP21A1D,
 climate,daily,day,land,nasa,noaa,surface,temperature,viirs

2012\-01\-19T00:00:00Z/2025\-07\-04T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP21A1D.002](https://doi.org/https://doi.org/10.5067/VIIRS/VNP21A1D.002)
* [https://doi.org/10\.5067/VIIRS/VNP21A1D.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP21A1D)









