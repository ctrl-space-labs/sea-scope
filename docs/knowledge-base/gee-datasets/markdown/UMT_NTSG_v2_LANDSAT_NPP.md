



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Landsat Net Primary Production CONUS


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================








Dataset Availability
1986\-01\-01T00:00:00Z–2020\-01\-01T00:00:00Z
Dataset Provider


[University of Montana Numerical Terradynamic Simulation Group (NTSG)](https://www.ntsg.umt.edu/project/landsat/landsat-productivity.php)



Earth Engine Snippet


`ee.ImageCollection("UMT/NTSG/v2/LANDSAT/NPP")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMT/UMT_NTSG_v2_LANDSAT_NPP)





Cadence
1 Year
Tags


[conus](/earth-engine/datasets/tags/conus)
[gridmet\-derived](/earth-engine/datasets/tags/gridmet-derived)
[landsat](/earth-engine/datasets/tags/landsat)
[mod17](/earth-engine/datasets/tags/mod17)
[nlcd\-derived](/earth-engine/datasets/tags/nlcd-derived)
[npp](/earth-engine/datasets/tags/npp)
[photosynthesis](/earth-engine/datasets/tags/photosynthesis)
[plant\-productivity](/earth-engine/datasets/tags/plant-productivity)
[production](/earth-engine/datasets/tags/production)
[productivity](/earth-engine/datasets/tags/productivity)
[yearly](/earth-engine/datasets/tags/yearly)








#### Description



The Landsat Net Primary Production (NPP) CONUS dataset estimates NPP using
Landsat Surface Reflectance for CONUS. NPP is the amount of
carbon captured by plants in an ecosystem, after accounting for losses due to
respiration. NPP is calculated using the MOD17 algorithm (see [MOD17 User
Guide](https://www.ntsg.umt.edu/files/modis/MOD17UsersGuide2015_v3.pdf)) with
Landsat Surface Reflectance, gridMET, and the National Land Cover Database.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `annualNPP` | kg\*C/m^2 | 0 | 65535 | 0\.0001 | Annual net primary production |
| `QC` | % | 0 | 255 |  | Percentage of gap\-filled Landsat 16\-day composites. Gaps are caused by missing data, high cloud contamination, and/or erroneous pixels. A value of 255 indicates incomplete data due to failure of the gap\-filling method. |




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
vardataset=ee.ImageCollection('UMT/NTSG/v2/LANDSAT/NPP')
.filter(ee.Filter.date('2016-01-01','2016-12-31'));
varnpp=dataset.select('annualNPP');
varnppVis={
min:0.0,
max:20000.0,
palette:['bbe029','0a9501','074b03'],
};
Map.setCenter(-98.26,39.32,5);
Map.addLayer(npp,nppVis,'NPP');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMT/UMT_NTSG_v2_LANDSAT_NPP)


[Landsat Net Primary Production CONUS](/earth-engine/datasets/catalog/UMT_NTSG_v2_LANDSAT_NPP)

The Landsat Net Primary Production (NPP) CONUS dataset estimates NPP using Landsat Surface Reflectance for CONUS. NPP is the amount of carbon captured by plants in an ecosystem, after accounting for losses due to respiration. NPP is calculated using the MOD17 algorithm (see MOD17 User Guide) with Landsat Surface Reflectance, …

 UMT/NTSG/v2/LANDSAT/NPP,
 conus,gridmet\-derived,landsat,mod17,nlcd\-derived,npp,photosynthesis,plant\-productivity,production,productivity,yearly

1986\-01\-01T00:00:00Z/2020\-01\-01T00:00:00Z



 24\.42 \-124\.84 49\.72 \-64\.82
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








