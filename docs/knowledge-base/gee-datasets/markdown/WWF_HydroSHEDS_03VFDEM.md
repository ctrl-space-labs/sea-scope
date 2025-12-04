



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WWF HydroSHEDS Void\-Filled DEM, 3 Arc\-Seconds


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================








Dataset Availability
2000\-02\-11T00:00:00Z–2000\-02\-22T00:00:00Z
Dataset Provider


[WWF](https://www.hydrosheds.org/)



Earth Engine Snippet


`ee.Image("WWF/HydroSHEDS/03VFDEM")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_03VFDEM)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[geophysical](/earth-engine/datasets/tags/geophysical)
[hydrography](/earth-engine/datasets/tags/hydrography)
[hydrology](/earth-engine/datasets/tags/hydrology)
[hydrosheds](/earth-engine/datasets/tags/hydrosheds)
[srtm](/earth-engine/datasets/tags/srtm)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[topography](/earth-engine/datasets/tags/topography)
[water](/earth-engine/datasets/tags/water)
[wwf](/earth-engine/datasets/tags/wwf)
void\-filled








#### Description



HydroSHEDS is a mapping product that provides hydrographic
information for regional and global\-scale applications in a consistent
format. It offers a suite of geo\-referenced datasets (vector and
raster) at various scales, including river networks, watershed
boundaries, drainage directions, and flow accumulations. HydroSHEDS
is based on elevation data obtained in 2000 by NASA's Shuttle Radar
Topography Mission (SRTM).


This void\-filled elevation dataset is the first step
towards producing the conditioned DEM datasets. Spikes and wells
in the SRTM data were detected and voided out. Small voids were
filled by interpolation of surrounding elevations. The ocean
was set to an elevation of 0 meters, and lakes, islands, and
rivers were filled using other techniques. Full details of the
underlying digital elevation model are available in the HydroSHEDS
website and documentation.


This dataset is at 3 arc\-second
resolution. The datasets available at 3 arc\-seconds are the Void\-Filled
DEM, Hydrologically Conditioned DEM, and Drainage (Flow) Direction.


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
  
92\.77 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `b1` | m | \-424\* | 8642\* | Elevation |


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
vardataset=ee.Image('WWF/HydroSHEDS/03VFDEM');
varelevation=dataset.select('b1');
varelevationVis={
min:-50.0,
max:3000.0,
gamma:2.0,
};
Map.setCenter(-121.652,38.022,8);
Map.addLayer(elevation,elevationVis,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_03VFDEM)


[WWF HydroSHEDS Void\-Filled DEM, 3 Arc\-Seconds](/earth-engine/datasets/catalog/WWF_HydroSHEDS_03VFDEM)

HydroSHEDS is a mapping product that provides hydrographic information for regional and global\-scale applications in a consistent format. It offers a suite of geo\-referenced datasets (vector and raster) at various scales, including river networks, watershed boundaries, drainage directions, and flow accumulations. HydroSHEDS is based on elevation data obtained in 2000 …

 WWF/HydroSHEDS/03VFDEM,
 dem,elevation,geophysical,hydrography,hydrology,hydrosheds,srtm,surface\-ground\-water,topography,water,wwf

2000\-02\-11T00:00:00Z/2000\-02\-22T00:00:00Z



 \-67\.3 \-180 60 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








