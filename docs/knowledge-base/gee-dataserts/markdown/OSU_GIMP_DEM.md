



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Greenland DEM \- Greenland Mapping Project (GIMP)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================








Dataset Availability
1999\-06\-30T00:00:00Z–2002\-09\-04T00:00:00Z
Dataset Provider


[NASA NSIDC DAAC at CIRES](https://doi.org/10.5067/NV34YUIXLP9W)



Earth Engine Snippet


`ee.Image("OSU/GIMP/DEM")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OSU/OSU_GIMP_DEM)





Tags


[arctic](/earth-engine/datasets/tags/arctic)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[gimp](/earth-engine/datasets/tags/gimp)
[greenland](/earth-engine/datasets/tags/greenland)
[nasa](/earth-engine/datasets/tags/nasa)
[polar](/earth-engine/datasets/tags/polar)








#### Description



This Digital Elevation Model (DEM) is constructed from a combination
of ASTER and SPOT\-5 DEM's for the ice sheet periphery and margin
(i.e. below the equilbrium line elevation) south of
approximately 82\.5°N and AVHRR photoclinometry in the ice sheet
interior and far north (Scambos and Haran, 2002\).


SPOT\-5 DEM's were produced and distributed as part of the Spot5
stereoscopic survey of Polar Ice: Reference Images \& Topographies
(SPIRIT) project (Korona et al., 2009\). Ocean surfaces were masked
using the GIMP Land Classification mask and replaced with the
CNES CLS11 mean sea surface height (Schaeffer et al., 2012\).


**Note**


* All land elevation data is horizontally and vertically registered
to average ICESat elevations for the 2003\-2009 time period, and
therefore the DEM has a nominal date of 2007, although care must
be taken when using the DEM in areas of rapid change, such as
major outlet glaciers south of 70°0N.
* The DEM has a resolution of 30 m, although the "true" resolution of the
DEM will vary from 40 m in areas of SPOT\-5 coverage
(see Korona et al. 2009\) to 500 m in areas of photoclinometry.
* The ice\-sheet\-wide root\-mean\-squared validation error
relative to ICESat is \+/\-10 m, rangining from close to \+/\- 1 m
over most ice surfaces to \+/\- 30 m in areas of high relief.


[General documentation](https://doi.org/10.5067/NV34YUIXLP9W)





### Bands


**Bands**




| Name | Units | Pixel Size | Description |
| --- | --- | --- | --- |
| `elevation` | m | Elevation |




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


* [https://doi.org/10\.5067/NV34YUIXLP9W](https://doi.org/10.5067/NV34YUIXLP9W)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OSU/GIMP/DEM');
varelevation=dataset.select('elevation');
varelevationVis={
min:0.0,
max:2000.0,
};
Map.setCenter(-41.0,76.0,4);
Map.addLayer(elevation,elevationVis,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OSU/OSU_GIMP_DEM)


[Greenland DEM \- Greenland Mapping Project (GIMP)](/earth-engine/datasets/catalog/OSU_GIMP_DEM)

This Digital Elevation Model (DEM) is constructed from a combination of ASTER and SPOT\-5 DEM's for the ice sheet periphery and margin (i.e. below the equilbrium line elevation) south of approximately 82\.5°N and AVHRR photoclinometry in the ice sheet interior and far north (Scambos and Haran, 2002\). SPOT\-5 DEM's were …

 OSU/GIMP/DEM,
 arctic,elevation\-topography,gimp,greenland,nasa,polar

1999\-06\-30T00:00:00Z/2002\-09\-04T00:00:00Z



 58\.795926930232035 \-89\.32179714240877 83\.95392768557056 7\.556480769227746
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/NV34YUIXLP9W](https://doi.org/https://doi.org/10.5067/NV34YUIXLP9W)
* [https://doi.org/10\.5067/NV34YUIXLP9W](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OSU_GIMP_DEM)









