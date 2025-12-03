



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GMTED2010: Global Multi\-resolution Terrain Elevation Data 2010


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2010\-01\-01T00:00:00Z
Dataset Provider


[USGS](https://www.usgs.gov/core-science-systems/eros/coastal-changes-and-impacts/gmted2010)



Earth Engine Snippet


`ee.Image("USGS/GMTED2010_FULL")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GMTED2010_FULL)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[geophysical](/earth-engine/datasets/tags/geophysical)
[srtm](/earth-engine/datasets/tags/srtm)
[topography](/earth-engine/datasets/tags/topography)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The Global Multi\-resolution Terrain Elevation Data
2010 (GMTED2010\) dataset contains elevation data for the globe
collected from various sources at 7\.5 arc\-seconds resolution. More details
are available in the dataset [report](https://pubs.usgs.gov/of/2011/1073/pdf/of2011-1073.pdf).


The primary source dataset for GMTED2010 is NGA''s SRTM Digital
Terrain Elevation Data (DTED®, [https://www2\.jpl.nasa.gov/srtm/](https://science.jpl.nasa.gov/projects/srtm/))
(void\-filled) 1\-arc\-second data. For the geographic areas outside
the SRTM coverage area and to fill in remaining holes in the SRTM
data, the following sources were used: non\-SRTM DTED®, Canadian
Digital Elevation Data (CDED) at two resolutions, Satellite Pour
l''Observation de la Terre (SPOT 5\) Reference3D, National Elevation
Dataset (NED) for the continental United States and Alaska, GEODATA
9 second digital elevation model (DEM) for Australia, an Antarctica
satellite radar and laser altimeter DEM, and a Greenland satellite
radar altimeter DEM.


This dataset replaces the GTOPO30 Elevation Model.





### Bands



**Pixel Size**
  
231\.92 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `std` | m | Standard Deviation |
| `min` | m | Minimum |
| `med` | m | Median |
| `mea` | m | Mean |
| `max` | m | Maximum |
| `dsc` | m | Sample |
| `be75` | m | Breakline emphasis maintains the critical topographic features (streams or ridges) within the landscape by maintaining any minimum elevation or maximum elevation value on a breakline that passes within the specified analysis window. |




### Terms of Use


**Terms of Use**


Most U.S. Geological Survey (USGS) information resides
in the public domain and may be used without restriction. Additional
information on [Acknowledging or Crediting USGS as Information
Source](https://www.usgs.gov/information-policies-and-instructions/crediting-usgs) is available.




### Citations



Citations:
* Global Multi\-resolution Terrain Elevation Data 2010 courtesy of
the U.S. Geological Survey





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('USGS/GMTED2010_FULL');
varelevation=dataset.select('min');
varelevationVis={
min:-100.0,
max:6500.0,
gamma:3.5,
};
Map.setCenter(17.93,7.71,2);
Map.addLayer(elevation,elevationVis,'Minimum Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GMTED2010_FULL)


[GMTED2010: Global Multi\-resolution Terrain Elevation Data 2010](/earth-engine/datasets/catalog/USGS_GMTED2010_FULL)

The Global Multi\-resolution Terrain Elevation Data 2010 (GMTED2010\) dataset contains elevation data for the globe collected from various sources at 7\.5 arc\-seconds resolution. More details are available in the dataset report. The primary source dataset for GMTED2010 is NGA''s SRTM Digital Terrain Elevation Data (DTED®, https://www2\.jpl.nasa.gov/srtm/) (void\-filled) 1\-arc\-second data. For …

 USGS/GMTED2010\_FULL,
 dem,elevation,elevation\-topography,geophysical,srtm,topography,usgs

2010\-01\-01T00:00:00Z/2010\-01\-01T00:00:00Z



 \-56 \-180 84 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








