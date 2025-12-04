



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Precipitation Monthly


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================








Dataset Availability
2007\-01\-01T00:00:00Z–2019\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.1435912)



Earth Engine Snippet


`ee.Image("OpenLandMap/CLM/CLM_PRECIPITATION_SM2RAIN_M/v01")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_CLM_CLM_PRECIPITATION_SM2RAIN_M_v01)





Tags


[envirometrix](/earth-engine/datasets/tags/envirometrix)
[imerg](/earth-engine/datasets/tags/imerg)
[monthly](/earth-engine/datasets/tags/monthly)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[precipitation](/earth-engine/datasets/tags/precipitation)








#### Description



Monthly precipitation in mm at 1 km resolution based on [SM2RAIN\-ASCAT
2007\-2018](https://doi.org/10.5281/zenodo.2615278),
IMERG, CHELSA Climate, and WorldClim.


[Downscaled to 1 km resolution using gdalwarp](https://gitlab.com/openlandmap/global-layers/tree/master/input_layers/clim1km)
(cubic splines) and an average between [WorldClim](https://www.worldclim.org/data/worldclim21.html),
[CHELSA Climate](https://chelsa-climate.org/),
and [IMERG monthly product](https://gpm.nasa.gov/data/imerg) (see, e.g, "3B\-MO\-L.GIS.IMERG.20180601\.V05B.tif").
3x higher weight is given to the SM2RAIN\-ASCAT data since it assumed to be more accurate. Processing steps are available
[here](https://gitlab.com/openlandmap/global-layers/tree/master/input_layers/clim1km).
Antarctica is not included.


To access and visualize maps outside of Earth Engine, use [this page](https://opengeohub.org/about-openlandmap).


If you discover a bug, artifact or inconsistency in the LandGIS maps
or if you have a question please use the following channels:


* [Technical issues and questions about the code](https://gitlab.com/openlandmap/global-layers/issues)
* [General questions and comments](https://disqus.com/home/forums/landgis/)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `jan` | mm | 0\* | 380\* | Jan Precipitation monthly |
| `feb` | mm | 0\* | 380\* | Feb Precipitation monthly |
| `mar` | mm | 0\* | 380\* | Mar Precipitation monthly |
| `apr` | mm | 0\* | 380\* | Apr Precipitation monthly |
| `may` | mm | 0\* | 380\* | May Precipitation monthly |
| `jun` | mm | 0\* | 380\* | Jun Precipitation monthly |
| `jul` | mm | 0\* | 380\* | Jul Precipitation monthly |
| `aug` | mm | 0\* | 380\* | Aug Precipitation monthly |
| `sep` | mm | 0\* | 380\* | Sep Precipitation monthly |
| `oct` | mm | 0\* | 380\* | Oct Precipitation monthly |
| `nov` | mm | 0\* | 380\* | Nov Precipitation monthly |
| `dec` | mm | 0\* | 380\* | Dec Precipitation monthly |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


This is a human\-readable summary of (and not a substitute for) the [license](https://creativecommons.org/licenses/by-sa/4.0/).


You are free to \-
 Share \- copy and redistribute the material in any medium or format
 Adapt \- remix, transform, and build upon the material for any purpose, even commercially.


This license is acceptable for Free Cultural Works.
The licensor cannot revoke these freedoms as long as you follow the license terms.


Under the following terms \-
 Attribution \- You must give appropriate credit, provide a link to the license, and indicate if
 changes were made. You may do so in any reasonable manner, but not in any way that suggests the
 licensor endorses you or your use.


ShareAlike \- If you remix, transform, or build upon the material, you must distribute your
 contributions under the same license as the original.


No additional restrictions \- You may not apply legal terms or technological measures that
 legally restrict others from doing anything the license permits.




### Citations



Citations:
* Monthly precipitation in mm at 1 km resolution based on SM2RAIN\-ASCAT 2007\-2018 and IMERG 2014\-2018
[10\.5281/zenodo.1435912](https://doi.org/10.5281/zenodo.1435912)





### DOIs


* [https://doi.org/10\.5281/zenodo.1435912](https://doi.org/10.5281/zenodo.1435912)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/CLM/CLM_PRECIPITATION_SM2RAIN_M/v01');

varvisualization={
bands:['jan'],
min:0.0,
max:380.0,
palette:['ecffbd','ffff00','3af6ff','467aff','313eff','0008ff']
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Precipitation monthly in mm');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_CLM_CLM_PRECIPITATION_SM2RAIN_M_v01)


[OpenLandMap Precipitation Monthly](/earth-engine/datasets/catalog/OpenLandMap_CLM_CLM_PRECIPITATION_SM2RAIN_M_v01)

Monthly precipitation in mm at 1 km resolution based on SM2RAIN\-ASCAT 2007\-2018, IMERG, CHELSA Climate, and WorldClim. Downscaled to 1 km resolution using gdalwarp (cubic splines) and an average between WorldClim, CHELSA Climate, and IMERG monthly product (see, e.g, "3B\-MO\-L.GIS.IMERG.20180601\.V05B.tif"). 3x higher weight is given to the SM2RAIN\-ASCAT data since …

 OpenLandMap/CLM/CLM\_PRECIPITATION\_SM2RAIN\_M/v01,
 envirometrix,imerg,monthly,opengeohub,openlandmap,precipitation

2007\-01\-01T00:00:00Z/2019\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.1435912](https://doi.org/https://doi.org/10.5281/zenodo.1435912)
* [https://doi.org/10\.5281/zenodo.1435912](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_CLM_CLM_PRECIPITATION_SM2RAIN_M_v01)









