



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP15A2H: LAI/FPAR 8\-Day L4 Global 500m SIN Grid


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================








Dataset Availability
2012\-01\-17T00:00:00Z–2025\-06\-18T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/VIIRS/VNP15A2H.002)



Earth Engine Snippet


`ee.ImageCollection("NASA/VIIRS/002/VNP15A2H")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP15A2H)





Cadence
8 Days
Tags


[land](/earth-engine/datasets/tags/land)
[nasa](/earth-engine/datasets/tags/nasa)
[noaa](/earth-engine/datasets/tags/noaa)
[surface](/earth-engine/datasets/tags/surface)
[vegetation\-indices](/earth-engine/datasets/tags/vegetation-indices)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The Visible Infrared Imaging Radiometer Suite (VIIRS) Leaf Area Index (LAI)
and Fraction of Photosynthetically Active Radiation (FPAR) Version 1 data
product provides information about the vegetative canopy layer at 500 meter
resolution (VNP15A2H). The VIIRS sensor is located onboard the NOAA/NASA
joint Suomi National Polar\-Orbiting Partnership (Suomi NPP) satellite. LAI
is an index that quantifies the one\-sided leaf area of a canopy, while FPAR
is the fraction of incoming solar energy absorbed through photosynthesis at
400 to 700 nanometers. This product is intentionally designed after the
Terra and Aqua Moderate Resolution Imaging Spectroradiometer (MODIS)
LAI/FPAR operational algorithm to promote the continuity of the Earth
Observation System (EOS) mission.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/126/VNP15_User_Guide.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/125/VNP15_ATBD.pdf)
* [General Documentation](https://lpdaac.usgs.gov/products/vnp15a2hv002/)
* [Land Product Quality Assessment website](https://landweb.modaps.eosdis.nasa.gov/browse?sensor=VIIRS&sat=SNPP)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `Fpar` | None | Fraction of Photosynthetically Active Radiation. |
| `FparExtra_QC` | None | Pass\-through Quality Control (QC) for FPAR |
| Bitmask for FparExtra\_QC * Bits 0\-1: Cloud detection and confidence 	+ 0: Confident clear 	+ 1: Probably clear 	+ 2: Probably cloudy 	+ 3: Confident cloudy * Bit 2: Cloud shadow 	+ 0: No cloud shadow 	+ 1: Shadow * Bit 3: Thin cirrus 	+ 0: No 	+ 1: Yes * Bits 4\-5: Aerosol quantity 	+ 0: Climatology 	+ 1: Low 	+ 2: Average 	+ 3: High * Bit 6: Snow/Ice 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `FparLai_QC` | None | Quality for LAI and FPAR |
| Bitmask for FparLai\_QC * Bits 0\-2: SCF\_QC 	+ 0: Main (RT) method used, best result possible (no saturation) 	+ 1: Main (RT) method used with saturation. Good, very usable. 	+ 2: Main (RT) method failed due to bad geometry, empirical 	algorithm used 	+ 3: Main (RT) method failed due to problems other than geometry, 	empirical algorithm used 	+ 4: Pixel not produced at all, value couldn't be retrieved * Bit 3: DeadDetector 	+ 0: Both red and NIR detectors are fine 	+ 1: At least one band has dead detector * Bits 4\-7: BiomeType 	+ 0: Water 	+ 1: Grasses/cereal crops 	+ 2: Shrubs 	+ 3: Broadleaf crops 	+ 4: Savanna 	+ 5: Evergreen broadleaf forest 	+ 6: Deciduous broadleaf forest 	+ 7: Evergreen needleleaf forest 	+ 8: Deciduous needleleaf forest 	+ 9: Non\-vegetated 	+ 10: Urban 	+ 11: Unclassified 	+ 12: Filled Value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `FparStdDev` | None | Standard deviation of FPAR |
| `Lai` | Area fraction | Leaf Area Index |
| `LaiStdDev` | Area fraction | Standard deviation for LAI |




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


* [https://doi.org/10\.5067/VIIRS/VNP15A2H.002](https://doi.org/10.5067/VIIRS/VNP15A2H.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/VIIRS/002/VNP15A2H')
.filter(ee.Filter.date('2022-11-01','2022-12-01'));

varvisualization={
bands:['Lai'],
min:[0],
max:[4],
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
Map.addLayer(dataset,visualization,'Leaf Area Index (LAI)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP15A2H)


[VNP15A2H: LAI/FPAR 8\-Day L4 Global 500m SIN Grid](/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP15A2H)

The Visible Infrared Imaging Radiometer Suite (VIIRS) Leaf Area Index (LAI) and Fraction of Photosynthetically Active Radiation (FPAR) Version 1 data product provides information about the vegetative canopy layer at 500 meter resolution (VNP15A2H). The VIIRS sensor is located onboard the NOAA/NASA joint Suomi National Polar\-Orbiting Partnership (Suomi NPP) satellite. …

 NASA/VIIRS/002/VNP15A2H,
 land,nasa,noaa,surface,vegetation\-indices,viirs

2012\-01\-17T00:00:00Z/2025\-06\-18T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP15A2H.002](https://doi.org/https://doi.org/10.5067/VIIRS/VNP15A2H.002)
* [https://doi.org/10\.5067/VIIRS/VNP15A2H.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP15A2H)









