



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

ArcticDEM Mosaic V4\.1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================








Dataset Availability
2012\-06\-03T00:00:00Z–2020\-09\-03T23:59:59Z
Dataset Provider


[University of Minnesota Polar Geospatial Center](https://www.pgc.umn.edu/data/arcticdem/)



Earth Engine Snippet


`ee.Image("UMN/PGC/ArcticDEM/V4/2m_mosaic")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMN/UMN_PGC_ArcticDEM_V4_2m_mosaic)





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


Mosaicked DEM files are compiled from the best quality strip DEM files
which have been blended and feathered to reduce void areas and edge\-matching
artifacts. Filtered IceSAT altimetry data has been applied to the raster
files to improve absolute accuracy.


These version (V4\.1\) mosaics include additional raster bands:
'count', 'mad','mindate', and 'maxdate' to provide
information on data provenance and uncertainty.





### Bands



**Pixel Size**
  
2 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `elevation` | m | \-416\.45\* | 5971\.24\* | Elevation |
| `count` | None | Number of source DEMs used to calculate the elevation value at that pixel. |
| `mad` | m | Median absolute deviation of the stack of source datasets from the median elevation value. |
| `mindate` | None | Earliest date of the source DEMs used to build the mosaic, as the number of days since January 1, 2000\. |
| `maxdate` | None | Latest date of the source DEMs used to build the mosaic, as the number of days since January 1, 2000\. |
| `datamask` | None | Data mask indicates whether the elevation was 0 or 1\. where 0 indicates , Filled/merged with another dataset or masked out as NoData in quality control steps. 1 indicates output by SETSM, the Ohio State University’s Surface Extraction with TIN\-based Search\-space Minimization software package. |


 \* estimated min or max value


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
vardataset=ee.Image('UMN/PGC/ArcticDEM/V4/2m_mosaic');

varelevationVis={
min:-50.0,
max:1000.0,
palette:['0d13d8','60e1ff','ffffff'],
bands:['elevation'],
};

varcountVis={
min:0,
max:10,
palette:[
'black',
'blue',
'purple',
'cyan',
'green',
'yellow',
'red',
],
bands:['count'],
};

varmadVis={
min:0,
max:50,
palette:[
'006633',
'E69800',
'D4E157',
'FFF59D',
],
bands:['mad'],
};

vardatamaskVis={
min:0,
max:1,
palette:[
'black',
'white',
],
bands:['datamask'],
};

Map.setCenter(-63.402,66.368,7);

Map.addLayer(dataset,elevationVis,'Elevation',true);
Map.addLayer(dataset,countVis,'Data Count',false);
Map.addLayer(dataset,madVis,'MAD',false);
Map.addLayer(dataset,datamaskVis,'Data Mask',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMN/UMN_PGC_ArcticDEM_V4_2m_mosaic)


[ArcticDEM Mosaic V4\.1](/earth-engine/datasets/catalog/UMN_PGC_ArcticDEM_V4_2m_mosaic)

ArcticDEM is a National Geospatial\-Intelligence Agency (NGA) and National Science Foundation (NSF) public\-private initiative to automatically produce a high\-resolution, high\-quality digital surface model (DSM) of the Arctic using optical stereo imagery, high\-performance computing, and open source photogrammetry software. It includes vegetation, tree canopy, buildings, and other man\-made surface features. The …

 UMN/PGC/ArcticDEM/V4/2m\_mosaic,
 arctic,dem,elevation\-topography,geophysical,pgc,umn

2012\-06\-03T00:00:00Z/2020\-09\-03T23:59:59Z



 50 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7910/DVN/OHHUKH](https://doi.org/https://www.pgc.umn.edu/data/arcticdem/)
* [https://doi.org/10\.7910/DVN/OHHUKH](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/UMN_PGC_ArcticDEM_V4_2m_mosaic)









