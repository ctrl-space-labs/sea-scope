



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WWF HydroSHEDS Basins Level 3


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================








Dataset Availability
2000\-02\-11T00:00:00Z–2000\-02\-22T00:00:00Z
Dataset Provider


[WWF](https://www.hydrosheds.org/)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("WWF/HydroSHEDS/v1/Basins/hybas_3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_v1_Basins_hybas_3)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("WWF/HydroSHEDS/v1/Basins/hybas_3_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_v1_Basins_hybas_3_FeatureView)





Tags


[geophysical](/earth-engine/datasets/tags/geophysical)
[hydrography](/earth-engine/datasets/tags/hydrography)
[hydrology](/earth-engine/datasets/tags/hydrology)
[hydrosheds](/earth-engine/datasets/tags/hydrosheds)
[srtm](/earth-engine/datasets/tags/srtm)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[table](/earth-engine/datasets/tags/table)
[water](/earth-engine/datasets/tags/water)
[watershed](/earth-engine/datasets/tags/watershed)
[wwf](/earth-engine/datasets/tags/wwf)








#### Description



HydroSHEDS is a mapping product that provides hydrographic
information for regional and global\-scale applications in a consistent
format. It offers a suite of geo\-referenced datasets (vector and
raster) at various scales, including river networks, watershed
boundaries, drainage directions, and flow accumulations. HydroSHEDS
is based on elevation data obtained in 2000 by NASA's Shuttle Radar
Topography Mission (SRTM).


This dataset provides polygons of nested, hierarchical watersheds, based on
15 arc\-seconds (approx. 500 m at the equator) resolution raster data.
The watersheds range from level 1 (coarse) to level 12 (detailed), using Pfastetter codes.


Technical documentation:


<https://hydrosheds.org/images/inpages/HydroBASINS_TechDoc_v1c.pdf>


Note that the quality of the HydroSHEDS data is significantly lower for regions above
60 degrees northern latitude as there is no underlying SRTM elevation data available
and thus a coarser\-resolution DEM was (HYDRO1k provided by USGS).


HydroSHEDS was developed by the World Wildlife Fund (WWF)
Conservation Science Program in partnership with the U.S. Geological
Survey, the International Centre for Tropical Agriculture, The
Nature Conservancy, and the Center for Environmental Systems Research
of the University of Kassel, Germany.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| HYBAS\_ID | INT | First 1 digit represents the region:  \* 1 \= Africa  \* 2 \= Europe  \* 3 \= Siberia  \* 4 \= Asia  \* 5 \= Australia  \* 6 \= South America  \* 7 \= North America  \* 8 \= Arctic (North America)  \* 9 \= Greenland. Next 2 digits define the Pfafstetter level (01\-12\). The value '00' is used for the 'Level 0' layer that contains all original sub\-basins and all Pfafstetter codes (at all levels); 'Level 0' only exists in the standard format of HydroBASINS (without lakes). Next 6 digits represent a unique identifier within the HydroSHEDS network; values larger than 900,000 represent lakes and only occur in the customized format (with lakes) Last 1 digit indicates the side of a sub\-basin in relation to the river network (0 \= noSide; 1 \= Left; 2 \= Right). Sides are only defined for the customized format (with lakes). |
| NEXT\_DOWN | INT | Hybas\_id of the next downstream polygon. |
| NEXT\_SINK | INT | Hybas\_id of the next downstream sink. |
| MAIN\_BAS | INT | Hybas\_id of the most downstream sink, i.e. the outlet of the main river basin. |
| DIST\_SINK | DOUBLE | Distance from polygon outlet to the next downstream sink, in km. |
| DIST\_MAIN | DOUBLE | Distance from polygon outlet to the most downstream sink, in km. |
| SUB\_AREA | DOUBLE | Area of basin, in square kilometers. |
| UP\_AREA | DOUBLE | Total upstream area, in square kilometers. |
| PFAF\_ID | INT | The Pfafstetter code. |
| ENDO | INT | Indicator for endorheic (inland) basins without surface flow connection to the ocean: 0 \= not part of an endorheic basin; 1 \= part of an endorheic basin; 2 \= sink (i.e. most downstream polygon) of an endorheic basin. |
| COAST | INT | Indicator for lumped coastal basins: 0 \= no; 1 \= yes. Coastal basins represent conglomerates of small coastal watersheds that drain into the ocean between larger river basins. |
| ORDER | INT | Indicator of river order (classical ordering system): \* Order 1 represents the main stem river from sink to source; \* Order 2 represents all tributaries that flow into a 1st order river; \* Order 3 represents all tributaries that flow into a 2nd order river; etc.; \* Order 0 is used for conglomerates of small coastal watersheds. |
| SORT | INT | Indicator showing the record number (sequence) in which the original polygons are stored in the shapefile (i.e. counting upwards from 1 in the original shapefile). The original polygons are sorted from downstream to upstream. This field can be used to sort the polygons back to their original sequence or to perform topological searches. |




### Terms of Use


**Terms of Use**


HydroSHEDS data are free for non\-commercial and commercial
use. For more information, please refer to the [License Agreement](https://www.hydrosheds.org/page/license).




### Citations



Citations:
* Lehner, B., Verdin, K., Jarvis, A. (2008\): New global hydrography
derived from spaceborne elevation data. Eos, Transactions, AGU,
89(10\): 93\-94\.
* Lehner, B., Grill G. (2013\): Global river hydrography and network routing: baseline data and
new approaches to study the world's large river systems. Hydrological Processes, 27(15\):
2171\-2186\. Data is available at www.hydrosheds.org





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('WWF/HydroSHEDS/v1/Basins/hybas_3');

varvisualization={
color:'808080',
strokeWidth:1
};

dataset=dataset.draw(visualization);

Map.setCenter(-117.731,53.033,7);
Map.addLayer(dataset,null,'Basins');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_v1_Basins_hybas_3)
### Visualize as a FeatureView



 A `FeatureView` is a view\-only, accelerated representation of a
 `FeatureCollection`. For more details, visit the
 [`FeatureView` documentation.](/earth-engine/guides/featureview_overview) 



**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varfvLayer=ui.Map.FeatureViewLayer(
'WWF/HydroSHEDS/v1/Basins/hybas_3_FeatureView');

varvisParams={
color:'808080',
lineWidth:1
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Basins');

Map.setCenter(-117.731,53.033,7);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_v1_Basins_hybas_3_FeatureView)


[WWF HydroSHEDS Basins Level 3](/earth-engine/datasets/catalog/WWF_HydroSHEDS_v1_Basins_hybas_3)

HydroSHEDS is a mapping product that provides hydrographic information for regional and global\-scale applications in a consistent format. It offers a suite of geo\-referenced datasets (vector and raster) at various scales, including river networks, watershed boundaries, drainage directions, and flow accumulations. HydroSHEDS is based on elevation data obtained in 2000 …

 WWF/HydroSHEDS/v1/Basins/hybas\_3,
 geophysical,hydrography,hydrology,hydrosheds,srtm,surface\-ground\-water,table,water,watershed,wwf

2000\-02\-11T00:00:00Z/2000\-02\-22T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








