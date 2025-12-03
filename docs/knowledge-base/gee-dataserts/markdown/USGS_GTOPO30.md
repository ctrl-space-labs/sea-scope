



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GTOPO30: Global 30 Arc\-Second Elevation


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================








Dataset Availability
1996\-01\-01T00:00:00Z–1996\-01\-01T00:00:00Z
Dataset Provider


[United States Geological Survey](https://www.usgs.gov/centers/eros/science/usgs-eros-archive-digital-elevation-global-30-arc-second-elevation-gtopo30)



Earth Engine Snippet


`ee.Image("USGS/GTOPO30")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GTOPO30)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[geophysical](/earth-engine/datasets/tags/geophysical)
[nasa](/earth-engine/datasets/tags/nasa)
[topography](/earth-engine/datasets/tags/topography)
[usgs](/earth-engine/datasets/tags/usgs)
gtopo30








#### Description



GTOPO30 is a global digital elevation model (DEM) with
a horizontal grid spacing of 30 arc seconds (approximately 1 kilometer).
The DEM was derived from several raster and vector sources of topographic
information. Completed in late 1996, GTOPO30 was developed over
a three\-year period through a collaborative effort led by the U.S.
Geological Survey''s Center for Earth Resources Observation and
Science (EROS). The following organizations participated by contributing
funding or source data: the National Aeronautics and Space Administration
(NASA), the United Nations Environment Programme/Global Resource
Information Database (UNEP/GRID), the U.S. Agency for International
Development (USAID), the Instituto Nacional de Estadistica Geografica
e Informatica (INEGI) of Mexico, the Geographical Survey Institute (GSI)
of Japan, Manaaki Whenua Landcare Research of New Zealand, and
the Scientific Committee on Antarctic Research (SCAR).





### Bands


**Bands**




| Name | Units | Min | Max | Pixel Size | Description |
| --- | --- | --- | --- | --- | --- |
| `elevation` | m | \-407\* | 8752\* | Elevation |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


There are no restrictions on the use of data received
from the U.S. Geological Survey's Earth Resources Observation and
Science (EROS) Center. For more information, visit the USGS' [Data
Use and Citation](https://www.usgs.gov/centers/eros/science/usgs-eros-archive-data-use-and-citation) page.




### Citations



Citations:
* GTOPO30 DEM courtesy of the U.S. Geological Survey





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('USGS/GTOPO30');
varelevation=dataset.select('elevation');
varelevationVis={
min:-10.0,
max:8000.0,
gamma:1.6,
};
Map.setCenter(11.69,43.9,4);
Map.addLayer(elevation,elevationVis,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GTOPO30)


[GTOPO30: Global 30 Arc\-Second Elevation](/earth-engine/datasets/catalog/USGS_GTOPO30)

GTOPO30 is a global digital elevation model (DEM) with a horizontal grid spacing of 30 arc seconds (approximately 1 kilometer). The DEM was derived from several raster and vector sources of topographic information. Completed in late 1996, GTOPO30 was developed over a three\-year period through a collaborative effort led by …

 USGS/GTOPO30,
 dem,elevation,elevation\-topography,geophysical,nasa,topography,usgs

1996\-01\-01T00:00:00Z/1996\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








