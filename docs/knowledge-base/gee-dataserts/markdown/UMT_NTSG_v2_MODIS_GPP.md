



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MODIS Gross Primary Production CONUS


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2021\-12\-19T00:00:00Z
Dataset Provider


[University of Montana Numerical Terradynamic Simulation Group (NTSG)](https://www.ntsg.umt.edu/project/landsat/landsat-productivity.php)



Earth Engine Snippet


`ee.ImageCollection("UMT/NTSG/v2/MODIS/GPP")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMT/UMT_NTSG_v2_MODIS_GPP)





Cadence
8 Days
Tags


[8\-day](/earth-engine/datasets/tags/8-day)
[conus](/earth-engine/datasets/tags/conus)
[gpp](/earth-engine/datasets/tags/gpp)
[gridmet\-derived](/earth-engine/datasets/tags/gridmet-derived)
[mod09q1](/earth-engine/datasets/tags/mod09q1)
[mod17](/earth-engine/datasets/tags/mod17)
[modis](/earth-engine/datasets/tags/modis)
[nlcd\-derived](/earth-engine/datasets/tags/nlcd-derived)
[photosynthesis](/earth-engine/datasets/tags/photosynthesis)
[plant\-productivity](/earth-engine/datasets/tags/plant-productivity)
[production](/earth-engine/datasets/tags/production)
[productivity](/earth-engine/datasets/tags/productivity)








#### Description



The MODIS Gross Primary Production (GPP) CONUS dataset estimates GPP using
MODIS Surface Reflectance for CONUS. GPP is the amount of
carbon captured by plants in an ecosystem and is an essential component in
the calculations of Net Primary Production (NPP). GPP is calculated using the
MOD17 algorithm (see [MOD17 User
Guide](https://www.ntsg.umt.edu/files/modis/MOD17UsersGuide2015_v3.pdf)) with
MODIS Surface Reflectance, gridMET, and the National Land Cover Database.





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `GPP` | kg\*C/m^2/8\-day | 0 | 65535 | 0\.0001 | 8\-day gross primary production |
| `QC` | None | 0 | 1 |  | Indicates if the original NDVI value was adjusted through the smoothing algorithm. 0 denotes the value was not adjusted. 1 indicates the value was adjusted. |




### Terms of Use


**Terms of Use**


This work is in the public domain and is free of known copyright
restrictions. Users should properly cite the source used in the creation of
any reports and publications resulting from the use of this dataset and note
the date when the data was acquired.




### Citations



Citations:
* Robinson, N.P., B.W. Allred, W.K. Smith, M.O. Jones, A. Moreno, T.A.
Erickson, D.E. Naugle, and S.W. Running. 2018\. Terrestrial primary
production for the conterminous United States derived from Landsat 30 m and
MODIS 250 m. Remote Sensing in Ecology and Conservation.
[doi:10\.1002/rse2\.74](https://doi.org/10.1002/rse2.74)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('UMT/NTSG/v2/MODIS/GPP')
.filter(ee.Filter.date('2017-05-01','2017-05-31'));
vargpp=dataset.select('GPP');
vargppVis={
min:0.0,
max:1000.0,
palette:['bbe029','0a9501','074b03'],
};
Map.setCenter(-98.26,39.32,5);
Map.addLayer(gpp,gppVis,'GPP');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMT/UMT_NTSG_v2_MODIS_GPP)


[MODIS Gross Primary Production CONUS](/earth-engine/datasets/catalog/UMT_NTSG_v2_MODIS_GPP)

The MODIS Gross Primary Production (GPP) CONUS dataset estimates GPP using MODIS Surface Reflectance for CONUS. GPP is the amount of carbon captured by plants in an ecosystem and is an essential component in the calculations of Net Primary Production (NPP). GPP is calculated using the MOD17 algorithm (see MOD17 …

 UMT/NTSG/v2/MODIS/GPP,
 8\-day,conus,gpp,gridmet\-derived,mod09q1,mod17,modis,nlcd\-derived,photosynthesis,plant\-productivity,production,productivity

2001\-01\-01T00:00:00Z/2021\-12\-19T00:00:00Z



 24\.42 \-124\.84 49\.72 \-64\.82
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








