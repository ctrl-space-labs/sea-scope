



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP64A1: Burned Area Monthly L4 Global 500m SIN Grid


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================








Dataset Availability
2014\-01\-01T00:00:00Z–2019\-01\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/VIIRS/VNP64A1.001)



Earth Engine Snippet


`ee.ImageCollection("NOAA/VIIRS/001/VNP64A1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_VIIRS_001_VNP64A1)





Cadence
30 Days
Tags


[burn](/earth-engine/datasets/tags/burn)
[change\-detection](/earth-engine/datasets/tags/change-detection)
[fire](/earth-engine/datasets/tags/fire)
[land](/earth-engine/datasets/tags/land)
[nasa](/earth-engine/datasets/tags/nasa)
[noaa](/earth-engine/datasets/tags/noaa)
[surface](/earth-engine/datasets/tags/surface)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The daily Suomi National Polar\-Orbiting Partnership (Suomi NPP) NASA Visible
Infrared Imaging Radiometer Suite (VIIRS) Burned Area (VNP64A1\) Version 1
data product is a monthly, global gridded 500m product containing per\-pixel
burned area and quality information. The VNP64 burned area mapping approach
employs 750m VIIRS imagery coupled with 750m VIIRS active fire
observations.


VIIRS bands that are both sensitive and insensitive to biomass burning are
used to detect changes caused by fire and to differentiate them from other
types of change.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/1330/VNP64A1_User_Guide_V1.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/572/VNP64A1_ATBD_V1.pdf)
* [General Documentation](https://lpdaac.usgs.gov/products/vnp64a1v001/)
* [Land Product Quality Assessment website](https://landweb.modaps.eosdis.nasa.gov/browse?sensor=VIIRS&sat=SNPP)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `Burn_Date` | None | Ordinal day of burn (1\-366\) for each 500\-m grid cell. |
| `Burn_Date_Uncertainty` | % | Estimated uncertainty in date of burn, in days. Unburned, unmapped, and water grid cells are masked out. |
| `QA` | None | Quality Assurance Indicators |
| Bitmask for QA * Bit 0: land/water state 	+ 0: water grid cell 	+ 1: land grid cell * Bit 1: Valid data flag (0 \= false, 1 \= true). A value of 1 indicates that there was sufficient valid data in the reflectance time series for the grid cell to be processed. 	+ 0: false 	+ 1: true * Bit 2: Shortened mapping period (0 \= false, 1 \= true). This flag indicates that the period of reliable mapping does not encompass the full one\-month product period. 	+ 0: false 	+ 1: true * Bit 3: Grid cell was relabeled during the contextual relabeling phase of the algorithm (0 \= false, 1 \= true). 	+ 0: false 	+ 1: true * Bit 4: Spare bit set to 0 	+ 0: Spare bit * Bits 5\-7: Special condition code reserved for unburned grid cells. This code provides an explanation for any grid cells that were summarily classified as unburned by the detection algorithm due to special circumstances. 	+ 0: burned, unmapped, or water grid cells 	+ 1: Valid observations spaced too sparsely in time 	+ 2: Too few training observations or insufficient spectral 	separability between burned and unburned classes. 	+ 3: Apparent burn date at limits of time series 	+ 4: Apparent water contamination 	+ 5: Persistent hot spot 	+ 6: Reserved for future use 	+ 7: Reserved for future use | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `First_Day` | None | First day of the year of reliable change detection |
| `Last_Day` | None | Last day of the year of reliable change detection |




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


* [https://doi.org/10\.5067/VIIRS/VNP64A1\.001](https://doi.org/10.5067/VIIRS/VNP64A1.001)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varimage=ee.Image('NOAA/VIIRS/001/VNP64A1/2018_12_01');
varvisualization={
bands:['Last_Day'],
min:250.0,
max:320.0,
palette:[
'000080','0000d9','4000ff','8000ff','0080ff','00ffff',
'00ff80','80ff00','daff00','ffff00','fff500','ffda00',
'ffb000','ffa400','ff4f00','ff2500','ff0a00','ff00ff',
]
};

Map.setCenter(-119.13,38.32,8);
Map.addLayer(image,visualization,'Last day');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_VIIRS_001_VNP64A1)


[VNP64A1: Burned Area Monthly L4 Global 500m SIN Grid](/earth-engine/datasets/catalog/NOAA_VIIRS_001_VNP64A1)

The daily Suomi National Polar\-Orbiting Partnership (Suomi NPP) NASA Visible Infrared Imaging Radiometer Suite (VIIRS) Burned Area (VNP64A1\) Version 1 data product is a monthly, global gridded 500m product containing per\-pixel burned area and quality information. The VNP64 burned area mapping approach employs 750m VIIRS imagery coupled with 750m VIIRS …

 NOAA/VIIRS/001/VNP64A1,
 burn,change\-detection,fire,land,nasa,noaa,surface,viirs

2014\-01\-01T00:00:00Z/2019\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP64A1\.001](https://doi.org/https://doi.org/10.5067/VIIRS/VNP64A1.001)
* [https://doi.org/10\.5067/VIIRS/VNP64A1\.001](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_VIIRS_001_VNP64A1)









