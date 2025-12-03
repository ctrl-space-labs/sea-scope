



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD64A1\.061 MODIS Burned Area Monthly Global 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================








Dataset Availability
2000\-11\-01T00:00:00Z–2025\-05\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD64A1.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD64A1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD64A1)





Cadence
1 Month
Tags


[burn](/earth-engine/datasets/tags/burn)
[change\-detection](/earth-engine/datasets/tags/change-detection)
[fire](/earth-engine/datasets/tags/fire)
[geophysical](/earth-engine/datasets/tags/geophysical)
[global](/earth-engine/datasets/tags/global)
[mcd64a1](/earth-engine/datasets/tags/mcd64a1)
[modis](/earth-engine/datasets/tags/modis)
[monthly](/earth-engine/datasets/tags/monthly)
[nasa](/earth-engine/datasets/tags/nasa)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The Terra and Aqua combined MCD64A1 Version 6\.1 Burned Area data product is
a monthly, global gridded 500m product containing per\-pixel burned\-area
and quality information. The MCD64A1 burned\-area mapping approach employs
500m MODIS Surface Reflectance imagery coupled with 1km MODIS active
fire observations. The algorithm uses a burn sensitive vegetation index (VI)
to create dynamic thresholds that are applied to the composite data.
The VI is derived from MODIS shortwave infrared atmospherically corrected
surface reflectance bands 5 and 7 with a measure of temporal texture.
The algorithm identifies the date of burn for the 500m grid cells within
each individual MODIS tile. The date is encoded in a single data layer as
the ordinal day of the calendar year on which the burn occurred, with
values assigned to unburned land pixels and additional special values
reserved for missing data and water grid cells.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/1006/MCD64_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/115/MCD64_ATBD_V6.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MCD64A1)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `BurnDate` | 0 | 366 | Burn day of year. Possible values: 0 (unburned), 1\-366 (approximate Julian day of burning). |
| `Uncertainty` | 0 | 100 | Estimated uncertainty in burn day |
| `QA` | Quality assurance indicators |
| Bitmask for QA * Bit 0: Land/water 	+ 0: Water grid cell 	+ 1: Land grid cell * Bit 1: Valid data flag. A value of 1 indicates that there was sufficient valid data in the reflectance time series for the grid cell to be processed. (NB Water grid cells will always have this bit clear.) 	+ 0: Insufficient valid data 	+ 1: Sufficient valid data * Bit 2: Shortened mapping period. This flag indicates that the period of reliable mapping does not encompass the full one\-month product period, i.e., burns could not be reliably mapped over the full calendar month. 	+ 0: Mapping period not shortened 	+ 1: Mapping period shortened * Bit 3: Grid cell was relabeled during the contextual relabeling phase of the algorithm. 	+ 0: Grid cell was not relabeled 	+ 1: Grid cell was relabeled * Bit 4: Spare bit 	+ 0: N/A * Bits 5\-7: Special condition code reserved for unburned grid cells. This code provides an explanation for any grid cells that were summarily classified as *unburned* by the detection algorithm due to special circumstances. 	+ 0: None or not applicable (i.e., burned, unmapped, or water grid cell). 	+ 1: Valid observations spaced too sparsely in time. 	+ 2: Too few training observations or insufficient spectral 	separability between burned and unburned classes. 	+ 3: Apparent burn date at limits of time series. 	+ 4: Apparent water contamination. 	+ 5: Persistent hot spot. 	+ 6: Reserved for future use. 	+ 7: Reserved for future use. | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `FirstDay` | 0 | 366 | First day of the year of reliable change detection |
| `LastDay` | 0 | 366 | Last day of the year of reliable change detection |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD64A1\.061](https://doi.org/10.5067/MODIS/MCD64A1.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MCD64A1')
.filter(ee.Filter.date('2017-01-01','2018-05-01'));
varburnedArea=dataset.select('BurnDate');
varburnedAreaVis={
min:30.0,
max:341.0,
palette:['4e0400','951003','c61503','ff1901'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(burnedArea,burnedAreaVis,'Burned Area');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD64A1)


[MCD64A1\.061 MODIS Burned Area Monthly Global 500m](/earth-engine/datasets/catalog/MODIS_061_MCD64A1)

The Terra and Aqua combined MCD64A1 Version 6\.1 Burned Area data product is a monthly, global gridded 500m product containing per\-pixel burned\-area and quality information. The MCD64A1 burned\-area mapping approach employs 500m MODIS Surface Reflectance imagery coupled with 1km MODIS active fire observations. The algorithm uses a burn sensitive vegetation …

 MODIS/061/MCD64A1,
 burn,change\-detection,fire,geophysical,global,mcd64a1,modis,monthly,nasa,usgs

2000\-11\-01T00:00:00Z/2025\-05\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD64A1\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD64A1.061)
* [https://doi.org/10\.5067/MODIS/MCD64A1\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD64A1)









