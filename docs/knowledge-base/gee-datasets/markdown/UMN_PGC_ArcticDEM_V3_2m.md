



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

ArcticDEM Strips


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================








Dataset Availability
2009\-08\-16T00:00:00Z–2017\-03\-12T00:00:00Z
Dataset Provider


[University of Minnesota Polar Geospatial Center](https://www.pgc.umn.edu/data/arcticdem/)



Earth Engine Snippet


`ee.ImageCollection("UMN/PGC/ArcticDEM/V3/2m")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMN/UMN_PGC_ArcticDEM_V3_2m)





Tags


[arctic](/earth-engine/datasets/tags/arctic)
[dem](/earth-engine/datasets/tags/dem)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[geophysical](/earth-engine/datasets/tags/geophysical)
[pgc](/earth-engine/datasets/tags/pgc)
[umn](/earth-engine/datasets/tags/umn)








#### Description



ArcticDEM is a National Geospatial\-Intelligence Agency (NGA) and National
Science Foundation (NSF) public\-private initiative to automatically produce
a high\-resolution, high\-quality digital surface model (DSM) of the Arctic
using optical stereo imagery, high\-performance computing, and open source
photogrammetry software. It includes vegetation, tree canopy, buildings, and
other man\-made surface features. The 2m asset is a collection of strips rather
than a single mosaic due to projection differences between strips.


Strip DEM files correspond to the overlapping area of the input stereopair
image swaths as they are collected by DigitalGlobe's constellation of
polar\-orbiting satellites. Strip DEM dimensions will vary according to the
satellite sensor that acquired the images and the off\-nadir angle of
collection. Most strips are between 16km and 18km in width, and 110km and
120km in length.





### Bands



**Pixel Size**
  
2 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `elevation` | m | Elevation |
| `matchtag` | None | Bitmask raster indicating DEM pixels processing |
| Bitmask for matchtag * Bit 0: Pixel processing 	+ 0: Pixels have been interpolated 	+ 1: Pixels are derived from a stereo match | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


National Science Foundation (PGC's primary funding source) policy requires
researchers to acknowledge NSF support in all publications, web pages, and
media interviews.


By using PGC data in Earth Engine, users agree to cite PGC
and its sponsorship by the NSF. The original source of any third\-party data
supplied by PGC must also be properly attributed.


For more information see the PGC's
[Acknowledgement Policy](https://www.pgc.umn.edu/guides/user-services/acknowledgement-policy/).




### Citations



Citations:
* DEM(s) created by the Polar Geospatial Center from DigitalGlobe, Inc. imagery.
Porter, Claire; Morin, Paul; Howat, Ian; Noh, Myoung\-Jon; Bates, Brian;
Peterman, Kenneth; Keesey, Scott; Schlenk, Matthew; Gardiner, Judith;
Tomko, Karen; Willis, Michael; Kelleher, Cole; Cloutier, Michael; Husby, Eric;
Foga, Steven; Nakamura, Hitomi; Platson, Melisa; Wethington, Michael, Jr.;
Williamson, Cathleen; Bauer, Gregory; Enos, Jeremy; Arnold, Galen; Kramer, William;
Becker, Peter; Doshi, Abhijit; D'Souza, Cristelle; Cummens, Pat; Laurier, Fabien;
Bojesen, Mikkel, 2018, ArcticDEM, Harvard Dataverse, V1, \[Date Accessed].





### DOIs


* [https://doi.org/10\.7910/DVN/OHHUKH](https://doi.org/10.7910/DVN/OHHUKH)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('UMN/PGC/ArcticDEM/V3/2m');
varelevation=dataset.select('elevation');
varelevationVis={
min:-50.0,
max:1000.0,
palette:['0d13d8','60e1ff','ffffff'],
};
Map.setCenter(-63.402,66.368,7);
Map.addLayer(elevation,elevationVis,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMN/UMN_PGC_ArcticDEM_V3_2m)


[ArcticDEM Strips](/earth-engine/datasets/catalog/UMN_PGC_ArcticDEM_V3_2m)

ArcticDEM is a National Geospatial\-Intelligence Agency (NGA) and National Science Foundation (NSF) public\-private initiative to automatically produce a high\-resolution, high\-quality digital surface model (DSM) of the Arctic using optical stereo imagery, high\-performance computing, and open source photogrammetry software. It includes vegetation, tree canopy, buildings, and other man\-made surface features. The …

 UMN/PGC/ArcticDEM/V3/2m,
 arctic,dem,elevation\-topography,geophysical,pgc,umn

2009\-08\-16T00:00:00Z/2017\-03\-12T00:00:00Z



 50 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7910/DVN/OHHUKH](https://doi.org/https://www.pgc.umn.edu/data/arcticdem/)
* [https://doi.org/10\.7910/DVN/OHHUKH](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/UMN_PGC_ArcticDEM_V3_2m)









