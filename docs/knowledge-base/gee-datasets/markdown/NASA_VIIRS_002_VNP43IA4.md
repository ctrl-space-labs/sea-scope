



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP43IA4: BRDF/Albedo Quality Daily L3 Global 500m SIN Grid


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================================








Dataset Availability
2012\-01\-17T00:00:00Z–2025\-06\-25T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/VIIRS/VNP43IA4.002)



Earth Engine Snippet


`ee.ImageCollection("NASA/VIIRS/002/VNP43IA4")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP43IA4)





Cadence
1 Day
Tags


[brdf](/earth-engine/datasets/tags/brdf)
[land](/earth-engine/datasets/tags/land)
[nasa](/earth-engine/datasets/tags/nasa)
[noaa](/earth-engine/datasets/tags/noaa)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[surface](/earth-engine/datasets/tags/surface)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The NASA/NOAA Suomi National Polar\-orbiting Partnership (Suomi NPP) Visible
Infrared Imaging Radiometer Suite (VIIRS) Nadir Bidirectional Reflectance
Distribution Function (BRDF) Adjusted Reflectance (NBAR) Version 2 product
provides NBAR estimates at 500 meter resolution. The VNP43IA4 product is
produced daily using 16 days of VIIRS data and is weighted temporally to the
ninth day, which is reflected in the file name. The view angle effects are
removed from the directional reflectances, resulting in a stable and
consistent NBAR product. The VNP43 data products are designed to promote the
continuity of NASA's Moderate Resolution Imaging Spectroradiometer (MODIS)
BRDF/Albedo data product suite.


The VNP43 algorithm uses the RossThick/Li\-Sparse\-Reciprocal (RTLSR)
semi\-empirical kernel\-driven BRDF model, with the three kernel weights from
VNP43IA1 to reconstruct surface anisotropic effects, correcting the
directional reflectance to a common view geometry (VNP43IA4\), while
also computing integrated black\-sky albedo (BSA) at local solar noon and
white\-sky albedo (WSA) (VNP43IA3\). Researchers can use the BRDF model
parameters with a simple polynomial, to obtain black\-sky albedo at any solar
illumination angle. Likewise, both the BSA and WSA Science Dataset (SDS)
layers can be used with a simple polynomial, to manually estimate
instantaneous actual albedo (blue\-sky albedo). Additional details regarding
the methodology are available in the Algorithm Theoretical Basis Document
(ATBD).


Documentation:


* [User's Guide](https://www.umb.edu/spectralmass/viirs-user-guides-c1-and-c2/vnp43ia4-and-vnpma4-nbar-products/)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/194/VNP43_ATBD_V1.pdf)
* [General Documentation](https://lpdaac.usgs.gov/products/vnp43ia4v002/)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Description |
| --- | --- |
| `BRDF_Albedo_Band_Mandatory_Quality_I1` | BRDF/Albedo mandatory quality for band I1 |
| `BRDF_Albedo_Band_Mandatory_Quality_I2` | BRDF/Albedo mandatory quality for band I2 |
| `BRDF_Albedo_Band_Mandatory_Quality_I3` | BRDF/Albedo mandatory quality for band I3 |
| `Nadir_Reflectance_I1` | Nadir BRDF/Albedo Reflectance at local solar noon for band I1 |
| `Nadir_Reflectance_I2` | Nadir BRDF/Albedo Reflectance at local solar noon for band I2 |
| `Nadir_Reflectance_I3` | Nadir BRDF/Albedo Reflectance at local solar noon for band I3 |




### Terms of Use


**Terms of Use**


LP DAAC NASA data are freely accessible; however, when an author
publishes these data or works based on the data, it is requested that the
author cite the datasets within the text of the publication and include a
reference to them in the reference list.




### Citations



Citations:
* Schaaf, C., Z. Wang, A. Erb, I. Paynter. VIIRS/NPP BRDF/Albedo Nadir
BRDF\-Adjusted Ref Daily L3 Global 500m SIN Grid V002\. 2024, distributed by
NASA EOSDIS Land Processes Distributed Active Archive Center,
[10\.5067/VIIRS/VNP43IA4\.002](https://doi.org/10.5067/VIIRS/VNP43IA4.002).





### DOIs


* [https://doi.org/10\.5067/VIIRS/VNP43IA4\.002](https://doi.org/10.5067/VIIRS/VNP43IA4.002)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/VIIRS/002/VNP43IA4')
.filter(ee.Filter.date('2021-06-01','2021-06-03'));

varnadir_reflectance_I1=dataset.select('Nadir_Reflectance_I1').first();
varpalette=[
'000080',
'0000d9',
'4000ff',
'8000ff',
'0080ff',
'00ffff',
'00ff80',
'80ff00',
'daff00',
'ffff00',
'fff500',
'ffda00',
'ffb000',
'ffa400',
'ff4f00',
'ff2500',
'ff0a00',
'ff00ff',
];
varvisParams={
min:0,
max:10000,
palette:palette,
};

// cadetblue
varbackground=ee.Image.rgb(95,158,160).visualize({min:0,max:255});
varimage=nadir_reflectance_I1.visualize(visParams);

varlon=-8;
varlat=60;

Map.addLayer(background,{},'background');
Map.addLayer(image,{},'Nadir BRDF/Albedo Reflectance I1');
Map.setCenter(lon,lat,3);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_VIIRS_002_VNP43IA4)


[VNP43IA4: BRDF/Albedo Quality Daily L3 Global 500m SIN Grid](/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP43IA4)

The NASA/NOAA Suomi National Polar\-orbiting Partnership (Suomi NPP) Visible Infrared Imaging Radiometer Suite (VIIRS) Nadir Bidirectional Reflectance Distribution Function (BRDF) Adjusted Reflectance (NBAR) Version 2 product provides NBAR estimates at 500 meter resolution. The VNP43IA4 product is produced daily using 16 days of VIIRS data and is weighted temporally to …

 NASA/VIIRS/002/VNP43IA4,
 brdf,land,nasa,noaa,satellite\-imagery,surface,viirs

2012\-01\-17T00:00:00Z/2025\-06\-25T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP43IA4\.002](https://doi.org/https://doi.org/10.5067/VIIRS/VNP43IA4.002)
* [https://doi.org/10\.5067/VIIRS/VNP43IA4\.002](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_VIIRS_002_VNP43IA4)









