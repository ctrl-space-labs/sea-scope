



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

2000 Greenland Mosaic \- Greenland Ice Mapping Project (GIMP)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================================================








Dataset Availability
1999\-06\-30T00:00:00Z–2002\-09\-04T00:00:00Z
Dataset Provider


[NASA NSIDC DAAC at CIRES](https://doi.org/10.5067/4RNTRRE4JCYD)



Earth Engine Snippet


`ee.Image("OSU/GIMP/2000_IMAGERY_MOSAIC")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OSU/OSU_GIMP_2000_IMAGERY_MOSAIC)





Tags


[arctic](/earth-engine/datasets/tags/arctic)
[gimp](/earth-engine/datasets/tags/gimp)
[greenland](/earth-engine/datasets/tags/greenland)
[imagery](/earth-engine/datasets/tags/imagery)
[nasa](/earth-engine/datasets/tags/nasa)
[polar](/earth-engine/datasets/tags/polar)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
radarsat\-1








#### Description



This dataset provides a complete 15 m resolution image mosaic
of the Greenland ice sheet derived from Landsat 7 ETM\+ and
RADARSAT\-1 SAR imagery from the years 1999 to 2002\. The methods
include a combination of image cloud masking, pan sharpening,
image sampling and resizing, and image coregistration.
Please see Howat, 2014 for more information regarding
processing methods.


**Note**


* Users of GIMP DEM or GIMP 2000 Image Mosaic images may find
it helpful to mask out areas outside of the Greenland coastline
using the corresponding 15 m ocean mask image
Greenland Ice Mapping Project (GIMP) Land Ice and Ocean
Classification Mask,
* The SAR data are distributed at 20 m resolution. Data were
up\-sampled through bilinear interpolation to 15 m to match
the resolution of Landsat band\-8\.


[General documentation](https://doi.org/10.5067/4RNTRRE4JCYD)





### Bands


**Bands**




| Name | Pixel Size | Wavelength | Description |
| --- | --- | --- | --- |
| `B1` | 0\.45 \- 0\.52 μm | Landsat 7 ETM\+ blue |
| `B2` | 0\.52 \- 0\.60 μm | Landsat 7 ETM\+ green |
| `B3` | 0\.63 \- 0\.69 μm | Landsat 7 ETM\+ red |
| `B4` | 0\.77 \- 0\.90 μm | Landsat 7 ETM\+ near infrared |
| `B5` | 1\.55 \- 1\.75 μm | Landsat 7 ETM\+ shortwave infrared 1 |
| `B6_low_gain` | 10\.40 \- 12\.50 μm | Landsat 7 ETM\+ low\-gain thermal Infrared 1\. This band has expanded dynamic range and lower radiometric resolution (sensitivity), with less saturation at high Digital Number (DN) values. Resampled from 60m to 30m. |
| `B6_high_gain` | 10\.40 \- 12\.50 μm | Landsat 7 ETM\+ high\-gain thermal Infrared 1\. This band has higher radiometric resolution (sensitivity), although it has a more restricted dynamic range. Resampled from 60m to 30m. |
| `B7` | 2\.08 \- 2\.35 μm | Landsat 7 ETM\+ shortwave infrared 2 |
| `B8` | 0\.52 \- 0\.90 μm | Landsat 7 ETM\+ panchromatic |
| `B8_radarsat` | None | RADARSAT\-1 synthetic aperture radar amplitude imagery |




### Terms of Use


**Terms of Use**


As a condition of using these data, you must cite the use of this
data set using the given citation.




### Citations



Citations:
* Howat, I.M., A. Negrete, B.E. Smith, 2014, The Greenland Ice
Mapping Project (GIMP) land classification and surface elevation
datasets, The Cryosphere, 8, 1509\-1518,
[doi:10\.5194/tc\-8\-1509\-2014](https://doi.org/10.5194/tc-8-1509-2014)
[article pdf](https://www.the-cryosphere.net/8/1509/2014/tc-8-1509-2014.pdf)





### DOIs


* [https://doi.org/10\.5067/4RNTRRE4JCYD](https://doi.org/10.5067/4RNTRRE4JCYD)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OSU/GIMP/2000_IMAGERY_MOSAIC');
vargreenlandImage=dataset.select(['B3','B2','B1']);
varvisParams={
min:0.0,
max:255.0,
};
Map.setCenter(-29.1605,70.4,9);
Map.addLayer(greenlandImage,visParams,'Greenland Pansharpened Image');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OSU/OSU_GIMP_2000_IMAGERY_MOSAIC)


[2000 Greenland Mosaic \- Greenland Ice Mapping Project (GIMP)](/earth-engine/datasets/catalog/OSU_GIMP_2000_IMAGERY_MOSAIC)

This dataset provides a complete 15 m resolution image mosaic of the Greenland ice sheet derived from Landsat 7 ETM\+ and RADARSAT\-1 SAR imagery from the years 1999 to 2002\. The methods include a combination of image cloud masking, pan sharpening, image sampling and resizing, and image coregistration. Please see …

 OSU/GIMP/2000\_IMAGERY\_MOSAIC,
 arctic,gimp,greenland,imagery,nasa,polar,satellite\-imagery

1999\-06\-30T00:00:00Z/2002\-09\-04T00:00:00Z



 58\.79601275381146 \-89\.3211593425295 83\.95386175580668 7\.555941634834938
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/4RNTRRE4JCYD](https://doi.org/https://doi.org/10.5067/4RNTRRE4JCYD)
* [https://doi.org/10\.5067/4RNTRRE4JCYD](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OSU_GIMP_2000_IMAGERY_MOSAIC)









