



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WWF HydroSHEDS Drainage Direction, 30 Arc\-Seconds


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================








Dataset Availability
2000\-02\-11T00:00:00Z–2000\-02\-22T00:00:00Z
Dataset Provider


[WWF](https://www.hydrosheds.org/)



Earth Engine Snippet


`ee.Image("WWF/HydroSHEDS/30DIR")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_30DIR)





Tags


[direction](/earth-engine/datasets/tags/direction)
[drainage](/earth-engine/datasets/tags/drainage)
[flow](/earth-engine/datasets/tags/flow)
[geophysical](/earth-engine/datasets/tags/geophysical)
[hydrography](/earth-engine/datasets/tags/hydrography)
[hydrology](/earth-engine/datasets/tags/hydrology)
[hydrosheds](/earth-engine/datasets/tags/hydrosheds)
[srtm](/earth-engine/datasets/tags/srtm)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[water](/earth-engine/datasets/tags/water)
[wwf](/earth-engine/datasets/tags/wwf)








#### Description



HydroSHEDS is a mapping product that provides hydrographic
information for regional and global\-scale applications in a consistent
format. It offers a suite of geo\-referenced datasets (vector and
raster) at various scales, including river networks, watershed
boundaries, drainage directions, and flow accumulations. HydroSHEDS
is based on elevation data obtained in 2000 by NASA's Shuttle Radar
Topography Mission (SRTM).


This drainage direction dataset defines the direction
of flow from each cell in the conditioned DEM to its steepest
down\-slope neighbor. Values of drainage direction vary from 1
to 128\. All final outlet cells to the ocean are flagged with
a value of 0\. All cells that mark the lowest point of an endorheic
basin (inland sink) are flagged with a value of \-1\. The drainage
direction values follow the convention adopted by ESRI's flow
direction implementation: 1\=E, 2\=SE, 4\=S, 8\=SW, 16\=W, 32\=NW,
64\=N, 128\=NE.   

  

 This dataset is at 30 arc\-second resolution.
The datasets available at 30 arc\-seconds are the Hydrologically
Conditioned DEM, Drainage (Flow) Direction, and Flow Accumulation.


Note that the quality of the HydroSHEDS data is significantly lower for regions above
60 degrees northern latitude as there is no underlying SRTM elevation data available
and thus a coarser\-resolution DEM was (HYDRO1k provided by USGS).


HydroSHEDS was developed by the World Wildlife Fund (WWF)
Conservation Science Program in partnership with the U.S. Geological
Survey, the International Centre for Tropical Agriculture, The
Nature Conservancy, and the Center for Environmental Systems Research
of the University of Kassel, Germany.





### Bands



**Pixel Size**
  
927\.67 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `b1` | 0\* | 255\* | Drainage direction possible values: 1\=E, 2\=SE, 4\=S, 8\=SW, 16\=W, 32\=NW, 64\=N, 128\=NE; final outlet cells to the ocean are flagged with a value of 0 and cells that mark the lowest point of an endorheic basin (inland sink) are flagged with a value of 255 (original value of \-1\) |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


HydroSHEDS data are free for non\-commercial and commercial
use. For more information, please refer to the [License Agreement](https://www.hydrosheds.org/page/license).




### Citations



Citations:
* Lehner, B., Verdin, K., Jarvis, A. (2008\): New global hydrography
derived from spaceborne elevation data. Eos, Transactions, AGU,
89(10\): 93\-94\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('WWF/HydroSHEDS/30DIR');
vardrainageDirection=dataset.select('b1');
vardrainageDirectionVis={
min:1.0,
max:128.0,
palette:[
'000000','023858','006837','1a9850','66bd63','a6d96a','d9ef8b',
'ffffbf','fee08b','fdae61','f46d43','d73027'
],
};
Map.setCenter(-121.652,38.022,8);
Map.addLayer(drainageDirection,drainageDirectionVis,'Drainage Direction');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_30DIR)


[WWF HydroSHEDS Drainage Direction, 30 Arc\-Seconds](/earth-engine/datasets/catalog/WWF_HydroSHEDS_30DIR)

HydroSHEDS is a mapping product that provides hydrographic information for regional and global\-scale applications in a consistent format. It offers a suite of geo\-referenced datasets (vector and raster) at various scales, including river networks, watershed boundaries, drainage directions, and flow accumulations. HydroSHEDS is based on elevation data obtained in 2000 …

 WWF/HydroSHEDS/30DIR,
 direction,drainage,flow,geophysical,hydrography,hydrology,hydrosheds,srtm,surface\-ground\-water,water,wwf

2000\-02\-11T00:00:00Z/2000\-02\-22T00:00:00Z



 \-67\.3 \-180 62 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








