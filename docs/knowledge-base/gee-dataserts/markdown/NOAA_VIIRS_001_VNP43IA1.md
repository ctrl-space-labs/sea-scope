



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP43IA1: BRDF/Albedo Model Parameters Daily L3 Global 500m SIN Grid


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================================








Dataset Availability
2012\-01\-17T00:00:00Z–2024\-06\-09T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/VIIRS/VNP43IA1.001)



Earth Engine Snippet


`ee.ImageCollection("NOAA/VIIRS/001/VNP43IA1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_VIIRS_001_VNP43IA1)





Cadence
1 Day
Tags


[land](/earth-engine/datasets/tags/land)
[nasa](/earth-engine/datasets/tags/nasa)
[noaa](/earth-engine/datasets/tags/noaa)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[surface](/earth-engine/datasets/tags/surface)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The Suomi National Polar\-Orbiting Partnership (Suomi NPP) NASA Visible
Infrared Imaging Radiometer Suite (VIIRS) Bidirectional Reflectance
Distribution Function (BRDF) and Albedo Model Parameters (VNP43IA1\) Version
1 product provides kernel weights (parameters) at 500 resolution. The
VNP43IA1 product is produced daily using 16 days of VIIRS data, temporally
weighted to the ninth day, which is reflected in the file name. The VNP43IA1
product provides three spectrally dependent kernel weights, also known as
model parameters: isotropic (fiso), volumetric (fvol), and geometric (fgeo),
which can be used to model anisotropic effects of the Earth's surface.
All VNP43 data products are designed to promote the continuity of
NASA's Moderate Resolution Imaging Spectroradiometer (MODIS)
BRDF/Albedo data product suite.


Documentation:


* [User's Guide](https://www.umb.edu/spectralmass/viirs-user-guide/vnp43ia1-and-vnp43ma1-brdf-albedo-model-parameters)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/194/VNP43_ATBD_V1.pdf)
* [General Documentation](https://lpdaac.usgs.gov/products/vnp43ia1v001/)
* [Land Product Quality Assessment website](https://landweb.modaps.eosdis.nasa.gov/browse?sensor=VIIRS&sat=SNPP)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Description |
| --- | --- |
| `BRDF_Albedo_Band_Mandatory_Quality_I1` | BRDF/Albedo mandatory quality for band I1 |
| `BRDF_Albedo_Band_Mandatory_Quality_I2` | BRDF/Albedo mandatory quality for band I2 |
| `BRDF_Albedo_Band_Mandatory_Quality_I3` | BRDF/Albedo mandatory quality for band I3 |
| `BRDF_Albedo_Parameters_fiso_I1` | Isotropic parameter for band I1 |
| `BRDF_Albedo_Parameters_fvol_I1` | Volumetric parameter for band I1 |
| `BRDF_Albedo_Parameters_fgeo_I1` | Geometric parameter for band I1 |
| `BRDF_Albedo_Parameters_fiso_I2` | Isotropic parameter for band I2 |
| `BRDF_Albedo_Parameters_fvol_I2` | Volumetric parameter for band I2 |
| `BRDF_Albedo_Parameters_fgeo_I2` | Geometric parameter for band I2 |
| `BRDF_Albedo_Parameters_fiso_I3` | Isotropic parameter for band I3 |
| `BRDF_Albedo_Parameters_fvol_I3` | Volumetric parameter for band I3 |
| `BRDF_Albedo_Parameters_fgeo_I3` | Geometric parameter for band I3 |


**BRDF\_Albedo\_Band\_Mandatory\_Quality\_I1 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | Full BRDF inversions |
| 1 | None | Magnitude BRDF inversions |


**BRDF\_Albedo\_Band\_Mandatory\_Quality\_I2 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | Full BRDF inversions |
| 1 | None | Magnitude BRDF inversions |


**BRDF\_Albedo\_Band\_Mandatory\_Quality\_I3 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | Full BRDF inversions |
| 1 | None | Magnitude BRDF inversions |




### Terms of Use


**Terms of Use**


LP DAAC NASA data are freely accessible; however, when an author
publishes these data or works based on the data, it is requested that the
author cite the datasets within the text of the publication and include a
reference to them in the reference list.




### Citations



Citations:
* Please visit
[LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/VIIRS/VNP43IA1\.001](https://doi.org/10.5067/VIIRS/VNP43IA1.001)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/VIIRS/001/VNP43IA1')
.filter(ee.Filter.date('2017-03-10','2017-03-11'));

varvisualization={
bands:['BRDF_Albedo_Parameters_fiso_I1'],
min:0,
max:1,
palette:[
'000080','0000d9','4000ff','8000ff','0080ff','00ffff',
'00ff80','80ff00','daff00','ffff00','fff500','FFda00',
'ffb000','ffa400','ff4f00','ff2500','ff0a00','ff00ff',
]
};

Map.setCenter(89,58,3);

Map.addLayer(dataset,visualization,'Isotropic parameter for band I1');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_VIIRS_001_VNP43IA1)


[VNP43IA1: BRDF/Albedo Model Parameters Daily L3 Global 500m SIN Grid](/earth-engine/datasets/catalog/NOAA_VIIRS_001_VNP43IA1)

The Suomi National Polar\-Orbiting Partnership (Suomi NPP) NASA Visible Infrared Imaging Radiometer Suite (VIIRS) Bidirectional Reflectance Distribution Function (BRDF) and Albedo Model Parameters (VNP43IA1\) Version 1 product provides kernel weights (parameters) at 500 resolution. The VNP43IA1 product is produced daily using 16 days of VIIRS data, temporally weighted to the …

 NOAA/VIIRS/001/VNP43IA1,
 land,nasa,noaa,satellite\-imagery,surface,viirs

2012\-01\-17T00:00:00Z/2024\-06\-09T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP43IA1\.001](https://doi.org/https://doi.org/10.5067/VIIRS/VNP43IA1.001)
* [https://doi.org/10\.5067/VIIRS/VNP43IA1\.001](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_VIIRS_001_VNP43IA1)









