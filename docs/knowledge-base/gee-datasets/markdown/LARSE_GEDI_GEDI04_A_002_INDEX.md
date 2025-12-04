



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GEDI L4A table index


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================








Dataset Availability
2019\-04\-18T00:00:00Z–2024\-11\-28T00:00:00Z
Dataset Provider


[Indexing: Google and USFS Laboratory for Applications of Remote Sensing in Ecology (LARSE)](https://www.fs.usda.gov/)


[NASA GEDI mission, accessed through the USGS LP DAAC](https://daac.ornl.gov/GEDI/guides/GEDI_L4A_AGB_Density_V2_1.html)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("LARSE/GEDI/GEDI04_A_002_INDEX")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI04_A_002_INDEX)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("LARSE/GEDI/GEDI04_A_002_INDEX_FeatureView")` 





Tags


[elevation](/earth-engine/datasets/tags/elevation)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[gedi](/earth-engine/datasets/tags/gedi)
[larse](/earth-engine/datasets/tags/larse)
[nasa](/earth-engine/datasets/tags/nasa)
[table](/earth-engine/datasets/tags/table)
[tree\-cover](/earth-engine/datasets/tags/tree-cover)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



This is a feature collection created from the geometries of L4A tables in
[LARSE/GEDI/GEDI04\_A\_002](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002). Each feature is
a polygon footprint of a source table with its asset id and start/end
timestamps.


Please see [User Guide](https://daac.ornl.gov/GEDI/guides/GEDI_L4A_AGB_Density_V2_1.html)
for more information.


The Global Ecosystem Dynamics Investigation [GEDI](https://gedi.umd.edu/)
mission aims to characterize ecosystem structure and dynamics to enable
radically improved quantification and understanding of the Earth's carbon cycle
and biodiversity. The GEDI instrument, attached to the International Space
Station (ISS), collects data globally between 51\.6° N and 51\.6° S
latitudes at the highest resolution and densest sampling of the
3\-dimensional structure of the Earth. The GEDI instrument consists of three
lasers producing a total of eight beam ground transects, which instantaneously
sample eight \~25 m footprints spaced approximately every 60 m along\-track.




| Product | Description |
| --- | --- |
| L2A Vector | [LARSE/GEDI/GEDI02\_A\_002](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_A_002) |
| L2A Monthly raster | [LARSE/GEDI/GEDI02\_A\_002\_MONTHLY](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_A_002_MONTHLY) |
| L2A table index | [LARSE/GEDI/GEDI02\_A\_002\_INDEX](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_A_002_INDEX) |
| L2B Vector | [LARSE/GEDI/GEDI02\_B\_002](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_B_002) |
| L2B Monthly raster | [LARSE/GEDI/GEDI02\_B\_002\_MONTHLY](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_B_002_MONTHLY) |
| L2B table index | [LARSE/GEDI/GEDI02\_B\_002\_INDEX](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI02_B_002_INDEX) |
| L4A Biomass Vector | [LARSE/GEDI/GEDI04\_A\_002](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002) |
| L4A Monthly raster | [LARSE/GEDI/GEDI04\_A\_002\_MONTHLY](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002_MONTHLY) |
| L4A table index | [LARSE/GEDI/GEDI04\_A\_002\_INDEX](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002_INDEX) |
| L4B Biomass | [LARSE/GEDI/GEDI04\_B\_002](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_B_002) |





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| table\_id | STRING | GEDI L4A table collection Ids |
| time\_start | STRING | GEDI L4A table start time in the ISO 8601 format |
| time\_end | STRING | GEDI L4A table end time in the ISO 8601 format |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* GEDI L4A Footprint Level Aboveground Biomass Density, Version 2\.1\.
Dubayah, R.O., J. Armston, J.R. Kellner, L. Duncanson, S.P. Healey,
P.L. Patterson, S. Hancock, H. Tang, J. Bruening, M.A. Hofton, J.B. Blair,
and S.B. Luthcke. 2022\. ORNL DAAC, Oak Ridge, Tennessee, USA.
[doi:10\.3334/ORNLDAAC/2056](https://doi.org/10.3334/ORNLDAAC/2056)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varrectangle=ee.Geometry.Rectangle([
-111.22,24.06,-6.54,51.9
]);
// Filter index by date and location
varfilter_index=ee.FeatureCollection(
'LARSE/GEDI/GEDI04_A_002_INDEX').filter(
'time_start > "2020-10-10T15:57:18Z" && time_end < "2020-10-11T01:20:45Z"')
.filterBounds(rectangle);

Map.addLayer(filter_index);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LARSE/LARSE_GEDI_GEDI04_A_002_INDEX)


[GEDI L4A table index](/earth-engine/datasets/catalog/LARSE_GEDI_GEDI04_A_002_INDEX)

This is a feature collection created from the geometries of L4A tables in LARSE/GEDI/GEDI04\_A\_002\. Each feature is a polygon footprint of a source table with its asset id and start/end timestamps. Please see User Guide for more information. The Global Ecosystem Dynamics Investigation GEDI mission aims to characterize ecosystem structure …

 LARSE/GEDI/GEDI04\_A\_002\_INDEX,
 elevation,forest\-biomass,gedi,larse,nasa,table,tree\-cover,usgs

2019\-04\-18T00:00:00Z/2024\-11\-28T00:00:00Z



 \-51\.6 \-180 51\.6 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








