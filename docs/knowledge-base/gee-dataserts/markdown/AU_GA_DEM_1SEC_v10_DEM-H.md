



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

DEM\-H: Australian SRTM Hydrologically Enforced Digital Elevation Model


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================================================








Dataset Availability
2010\-02\-01T00:00:00Z–2010\-02\-01T00:00:00Z
Dataset Provider


[Geoscience Australia](https://www.ga.gov.au/metadata-gateway/metadata/record/72759/)



Earth Engine Snippet


`ee.Image("AU/GA/DEM_1SEC/v10/DEM-H")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/AU/AU_GA_DEM_1SEC_v10_DEM-H)





Tags


[australia](/earth-engine/datasets/tags/australia)
[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[ga](/earth-engine/datasets/tags/ga)
[geophysical](/earth-engine/datasets/tags/geophysical)
[geoscience\-australia](/earth-engine/datasets/tags/geoscience-australia)
[smoothed](/earth-engine/datasets/tags/smoothed)
[srtm](/earth-engine/datasets/tags/srtm)








#### Description



The Hydrologically Enforced Digital Elevation Model
(DEM\-H) was derived from the SRTM data acquired by NASA in February
2000\. The model has been hydrologically conditioned and drainage
enforced. The DEM\-H captures flow paths based on SRTM elevations
and mapped stream lines, and supports delineation of catchments
and related hydrological attributes. The dataset was derived from
the 1 second smoothed Digital Elevation Model (DEM\-S; ANZCW0703014016\)
by enforcing hydrological connectivity with the ANUDEM software,
using selected AusHydro V1\.6 (February 2010\) 1:250,000 scale watercourse
lines (ANZCW0503900101\) and lines derived from DEM\-S to define
the watercourses. The drainage enforcement has produced a consistent
representation of hydrological connectivity with some elevation
artifacts resulting from the drainage enforcement. A full description
of the methods is in preparation (Dowling et al., in prep).


This product provides a DEM suitable for use in hydrological analysis
such as catchment definition and flow routing.


There are several areas with unexpected negative values: close to
Canberra around (150\.443044, \-35\.355281\) with values of \-55 and in Western
Australia around (124\.84, \-16\.44\) with \-43\.





### Bands



**Pixel Size**
  
30\.92 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `elevation` | m | \-31\.37\* | 2223\.24\* | Elevation |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Geoscience Australia, 2015\. Digital Elevation Model (DEM) of Australia
derived from LiDAR 5 Metre Grid. Geoscience Australia, Canberra.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('AU/GA/DEM_1SEC/v10/DEM-H');
varelevation=dataset.select('elevation');
varelevationVis={
min:-10.0,
max:1300.0,
palette:[
'3ae237','b5e22e','d6e21f','fff705','ffd611','ffb613','ff8b13',
'ff6e08','ff500d','ff0000','de0101','c21301','0602ff','235cb1',
'307ef3','269db1','30c8e2','32d3ef','3be285','3ff38f','86e26f'
],
};
Map.setCenter(133.95,-24.69,5);
Map.addLayer(elevation,elevationVis,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/AU/AU_GA_DEM_1SEC_v10_DEM-H)


[DEM\-H: Australian SRTM Hydrologically Enforced Digital Elevation Model](/earth-engine/datasets/catalog/AU_GA_DEM_1SEC_v10_DEM-H)

The Hydrologically Enforced Digital Elevation Model (DEM\-H) was derived from the SRTM data acquired by NASA in February 2000\. The model has been hydrologically conditioned and drainage enforced. The DEM\-H captures flow paths based on SRTM elevations and mapped stream lines, and supports delineation of catchments and related hydrological attributes. …

 AU/GA/DEM\_1SEC/v10/DEM\-H,
 australia,dem,elevation,elevation\-topography,ga,geophysical,geoscience\-australia,smoothed,srtm

2010\-02\-01T00:00:00Z/2010\-02\-01T00:00:00Z



 \-44\.06 112\.99 \-9\.99 154
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








