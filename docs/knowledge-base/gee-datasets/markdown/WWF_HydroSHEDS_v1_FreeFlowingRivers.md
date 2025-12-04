



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WWF HydroSHEDS Free Flowing Rivers Network v1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================================








Dataset Availability
2000\-02\-11T00:00:00Z–2000\-02\-22T00:00:00Z
Dataset Provider


[WWF](https://www.hydrosheds.org/)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("WWF/HydroSHEDS/v1/FreeFlowingRivers")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_v1_FreeFlowingRivers)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("WWF/HydroSHEDS/v1/FreeFlowingRivers_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_v1_FreeFlowingRivers_FeatureView)





Tags


[geophysical](/earth-engine/datasets/tags/geophysical)
[hydrography](/earth-engine/datasets/tags/hydrography)
[hydrology](/earth-engine/datasets/tags/hydrology)
[hydrosheds](/earth-engine/datasets/tags/hydrosheds)
[srtm](/earth-engine/datasets/tags/srtm)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[table](/earth-engine/datasets/tags/table)
[water](/earth-engine/datasets/tags/water)
[wwf](/earth-engine/datasets/tags/wwf)
flow\-regulation
river\-networks








#### Description



HydroSHEDS is a mapping product that provides hydrographic
information for regional and global\-scale applications in a consistent
format. It offers a suite of geo\-referenced datasets (vector and
raster) at various scales, including river networks, watershed
boundaries, drainage directions, and flow accumulations. HydroSHEDS
is based on elevation data obtained in 2000 by NASA's Shuttle Radar
Topography Mission (SRTM).


This dataset provides polylines that represent river networks, derived from and consistent
with other HydroSHEDS datasets. These data are based on 15 arc\-seconds
(approx. 500 m at the equator) resolution raster data.


[Mapping the world's free\-flowing rivers: data set and technical documentation](https://figshare.com/articles/Mapping_the_world_s_free-flowing_rivers_data_set_and_technical_documentation/7688801)


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
| BAS\_ID | INT | Basin Identifier. Identifies the hydrological river basin according to the HydroSHEDS framework |
| BAS\_NAME | STRING | Basin Name (if available). Based on HydroSHEDS original basins and other sources. |
| BB\_DIS\_ORD | INT | Backbone river discharge order. River Order (RIV\_ORD) of the most downstream reach of the backbone river (BB\_ID). |
| BB\_ID | INT | Backbone River Identifier. Represents the contiguous river unit (defined as flow path from source/headwater to sink/terminus). |
| BB\_LEN\_KM | DOUBLE | Backbone river length. Sum of length (LENGTH\_KM) of the river reaches of the backbone river (BB\_ID). |
| BB\_OCEAN | DOUBLE | Ocean connectivity. Determines if river reach is part of a backbone river (BB\_ID) that is directly connected to the ocean (value\=1\) or not (value\=0\). Used to summarize statistics based on connectivity to ocean. |
| BB\_VOL\_TCM | DOUBLE | Backbone river volume. Sum of volume (VOLUME\_TCM) of the river reaches of the backbone river (BB\_ID). |
| CONTINENT | STRING | Name of the continent. See CON\_ID. |
| CON\_ID | DOUBLE | Identifier for the continent to which the reach belongs. Continent boundaries are delineated based on HydroBASINS.  \* 1 \= North America  \* 2 \= South America  \* 3 \= Europe  \* 4 \= Africa  \* 5 \= Asia  \* 6 \= Australia |
| COUNTRY | STRING | Country name |
| CSI | DOUBLE | Connectivity Status. Index from 0 to 100%; 100% \= full connectivity; 0% \= no connectivity. |
| CSI\_D | STRING | Dominant pressure factor (DOM). Possible field values are: DOF; DOR; SED; USE; RDD; URB. |
| CSI\_FF | INT | CSI above or below free\-flowing threshold. Indicates if the CSI value of a river reach is below (value \= 0\) or above (value \= 1\) the threshold of 95%. The attribute is used to calculate the free\-flowing status of the river (see CSI\_FF1 and CSI\_FF2\). |
| CSI\_FF1 | INT | Free\-flowing status (two categories). Indicates river reaches that belong to a river with "freeflowing" status (value \= 1\) or "non\-free\-flowing" status (value \= 3\). Note that the value 2 is reserved for river stretches with "good connectivity" status (see CSI\_FF2\). |
| CSI\_FF2 | INT | Free\-flowing status (three categories). Indicates river reaches that belong to a river with "free flowing" status (value \= 1\), or a river stretch with "good connectivity" status (value \= 2\) or a river or river stretch with "impacted" status(value \= 3\). |
| CSI\_FFID | INT | River stretch identifier. Additional identifier to distinguish contiguous river stretches. |
| DIS\_AV\_CMS | DOUBLE | Average long\-term (1971\-2000\) naturalized discharge in cubic meters per second (CMS). |
| DOF | DOUBLE | Degree of Fragmentation. Index from 0 to 100% (see extended Data figure 5a of manuscript). |
| DOR | DOUBLE | Degree of Regulation. Index from 0 to 100% (see extended Data figure 5b of manuscript). |
| ERO\_YLD\_TO | DOUBLE | Sum of erosion in tons per year per river reach. Calculated as the sum of sediment erosion within the river reach catchment (i.e., sediment erosion is not accumulated along the river network). |
| FLD | DOUBLE | Inundation (floodplain) extent in river reach catchment (%). |
| GOID | INT | The feature ID. |
| HYFALL | DOUBLE | Indicates the presence (1\) or absence (0\) of one or more waterfalls along the river reach. |
| INC | DOUBLE | Filter field. In Grill et al. (2019\), we considered all river reaches for routing purposes, but only analyzed and produced results for a subset of river reaches (INC \= 1\). |
| LENGTH\_KM | DOUBLE | Length of the river reach in kilometers. |
| NDOID | INT | Identifies the NOID of the next downstream river reach. If value\=0, the river reach represents a terminal reach (ocean, inland sink). |
| NOID | INT | Network Object Identifier. Same purpose as GOID' |
| NUOID | STRING | Identifies the NOIDs of the next upstream river reach. If there is "NoData" given, the reach is a headwater reach. Otherwise, the field holds 2 or more NOIDs. In the case of multiple NOIDs, the NOIDs are separated by an underscore. |
| OBJECTID | INT | Object Identifier |
| RDD | DOUBLE | Road construction. Index from 0 to 100% (see extended Data figure 5e of manuscript). |
| REACH\_ID | INT | Reach Identifier. The reach identifier can be used to link this dataset to the HydroATLAS database. |
| RIV\_ORD | INT | River order. River order is here defined and calculated based on the long\-term average discharge (DIS\_AV\_CMS) using logarithmic progression:  \* 1 \= \> 100000  \* 2 \= 10000 \- 100000  \* 3 \= 1000 \- 10000  \* 4 \= 100 \- 1000  \* 5 \= 10 \- 100  \* 6 \= 1 \- 10  \* 7 \= 0\.1 \- 1  \* 8 \= 0\.01 \- 0\.1  \* 9 \= 0\.001 \- 0\.01  \* 10 \= \< 0\.001 |
| SED | DOUBLE | Sediment trapping. Index from 0 to 100% (see extended Data figure 5c of manuscript). |
| Shape\_Leng | DOUBLE | Use field LENGTH\_KM instead. |
| UPLAND\_SKM | DOUBLE | Upstream watershed area of river reach in square kilometers (SKM). |
| URB | DOUBLE | Urbanization. Index from 0 to 100% (see extended Data figure 5f of manuscript). |
| USE | DOUBLE | Water consumption. Index from 0 to 100% (see extended Data figure 5d of manuscript). |
| VOLUME\_TCM | DOUBLE | Volume of the reach channel in thousand cubic meters (TCM). Calculated using width, length and depth of river channel. |




### Terms of Use


**Terms of Use**


HydroSHEDS data are free for non\-commercial and commercial
use. For more information, please refer to the [License Agreement](https://www.hydrosheds.org/page/license).




### Citations



Citations:
* Lehner, B., Verdin, K., Jarvis, A. (2008\): New global hydrography
derived from spaceborne elevation data. Eos, Transactions, AGU,
89(10\): 93\-94\.
* Grill, G., Lehner, B., Thieme, M., Geenen, B., Tickner, D., Antonelli, F., Babu, S., Borrelli,
P., Cheng, L., Crochetiere, H. and Macedo, H.E., 2019\. Mapping the world's free\-flowing rivers.
Nature, 569(7755\), p.215\. Data is available at www.hydrosheds.org





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('WWF/HydroSHEDS/v1/FreeFlowingRivers');

// Paint 'RIV_ORD' (river order) value to an image for visualization.
vardatasetVis=ee.Image().byte().paint(dataset,'RIV_ORD',2);

varvisParams={
min:1,
max:10,
palette:['08519c','3182bd','6baed6','bdd7e7','eff3ff']
};

Map.setCenter(-122.348,45.738,9);
Map.addLayer(datasetVis,visParams,'Free flowing rivers');
Map.addLayer(dataset,null,'FeatureCollection',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_v1_FreeFlowingRivers)
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
'WWF/HydroSHEDS/v1/FreeFlowingRivers_FeatureView');

varvisParams={
lineWidth:2,
color:{
property:'RIV_ORD',
mode:'linear',
palette:['08519c','3182bd','6baed6','bdd7e7','eff3ff'],
min:1,
max:10
}
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Free flowing rivers');

Map.setCenter(-122.348,45.738,9);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WWF/WWF_HydroSHEDS_v1_FreeFlowingRivers_FeatureView)


[WWF HydroSHEDS Free Flowing Rivers Network v1](/earth-engine/datasets/catalog/WWF_HydroSHEDS_v1_FreeFlowingRivers)

HydroSHEDS is a mapping product that provides hydrographic information for regional and global\-scale applications in a consistent format. It offers a suite of geo\-referenced datasets (vector and raster) at various scales, including river networks, watershed boundaries, drainage directions, and flow accumulations. HydroSHEDS is based on elevation data obtained in 2000 …

 WWF/HydroSHEDS/v1/FreeFlowingRivers,
 geophysical,hydrography,hydrology,hydrosheds,srtm,surface\-ground\-water,table,water,wwf

2000\-02\-11T00:00:00Z/2000\-02\-22T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








