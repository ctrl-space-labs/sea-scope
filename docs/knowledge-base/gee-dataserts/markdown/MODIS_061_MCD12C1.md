



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD12C1\.061 MODIS Land Cover Type Yearly Global 0\.05 Deg CMG


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2023\-01\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD12C1.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD12C1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD12C1)





Cadence
1 Year
Tags


[landcover](/earth-engine/datasets/tags/landcover)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[usgs](/earth-engine/datasets/tags/usgs)
[yearly](/earth-engine/datasets/tags/yearly)








#### Description



The Terra and Aqua combined Moderate Resolution Imaging Spectroradiometer
(MODIS) Land Cover Climate Modeling Grid (CMG) (MCD12C1\) Version 6\.1 data
product provides a spatially aggregated and reprojected version of the tiled
MCD12Q1 Version 6\.1 data product. Maps of the International
Geosphere\-Biosphere Programme (IGBP), University of Maryland (UMD), and Leaf
Area Index (LAI) classification schemes are provided at yearly intervals at
0\.05 degree (5,600 meter) spatial resolution for the entire globe from 2001
to 2022\. Additionally, sub\-pixel proportions of each land cover class in
each 0\.05 degree pixel is provided along with the aggregated quality
assessment information for each of the three land classification schemes.


Provided in each MCD12C1 Version 6\.1 Hierarchical Data Format 4 (HDF4\) file
are layers for Majority Land Cover Type 1\-3, Majority Land Cover Type 1\-3
Assessment, and Land Cover Type 1\-3 Percent for each class.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/1409/MCD12_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/86/MCD12_ATBD.pdf)





### Bands



**Pixel Size**
  
5600 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `Majority_Land_Cover_Type_1` | None | 0 | 16 | Majority Land Cover Type 1: Most likely IGBP class for each 0\.05 degree pixel |
| `Majority_Land_Cover_Type_1_Assessment` | % | 0 | 100 | Majority Land Cover Type 1 Assessment: Majority IGBP class confidence |
| `Land_Cover_Type_1_Percent_Class_0` | % | 0 | 100 | Percent cover of IGBP class 0 (Water Bodies) at each pixel |
| `Land_Cover_Type_1_Percent_Class_1` | % | 0 | 100 | Percent cover of IGBP class 1 (Evergreen Needleleaf Forests) at each pixel |
| `Land_Cover_Type_1_Percent_Class_2` | % | 0 | 100 | Percent cover of IGBP class 2 (Evergreen Broadleaf Forests) at each pixel |
| `Land_Cover_Type_1_Percent_Class_3` | % | 0 | 100 | Percent cover of IGBP class 3 (Deciduous Needleleaf Forests) at each pixel |
| `Land_Cover_Type_1_Percent_Class_4` | % | 0 | 100 | Percent cover of IGBP class 4 (Deciduous Broadleaf Forests) at each pixel |
| `Land_Cover_Type_1_Percent_Class_5` | % | 0 | 100 | Percent cover of IGBP class 5 (Mixed Forests) at each pixel |
| `Land_Cover_Type_1_Percent_Class_6` | % | 0 | 100 | Percent cover of IGBP class 6 (Closed Shrublands) at each pixel |
| `Land_Cover_Type_1_Percent_Class_7` | % | 0 | 100 | Percent cover of IGBP class 7 (Open Shrublands) at each pixel |
| `Land_Cover_Type_1_Percent_Class_8` | % | 0 | 100 | Percent cover of IGBP class 8 (Woody Savannas) at each pixel |
| `Land_Cover_Type_1_Percent_Class_9` | % | 0 | 100 | Percent cover of IGBP class 9 (Savannas) at each pixel |
| `Land_Cover_Type_1_Percent_Class_10` | % | 0 | 100 | Percent cover of IGBP class 10 (Grasslands) at each pixel |
| `Land_Cover_Type_1_Percent_Class_11` | % | 0 | 100 | Percent cover of IGBP class 11 (Permanent Wetlands) at each pixel |
| `Land_Cover_Type_1_Percent_Class_12` | % | 0 | 100 | Percent cover of IGBP class 12 (Croplands) at each pixel |
| `Land_Cover_Type_1_Percent_Class_13` | % | 0 | 100 | Percent cover of IGBP class 13 (Urban and Built\-up Lands) at each pixel |
| `Land_Cover_Type_1_Percent_Class_14` | % | 0 | 100 | Percent cover of IGBP class 14 (Cropland/Natural Vegetation Mosaics) at each pixel |
| `Land_Cover_Type_1_Percent_Class_15` | % | 0 | 100 | Percent cover of IGBP class 15 (Permanent Snow and Ice) at each pixel |
| `Land_Cover_Type_1_Percent_Class_16` | % | 0 | 100 | Percent cover of IGBP class 16 (Barren) at each pixel |
| `Majority_Land_Cover_Type_2` | None | 0 | 15 | Majority Land Cover Type 2: Most likely UMD class for each 0\.05 degree pixel |
| `Majority_Land_Cover_Type_2_Assessment` | % | 0 | 100 | Majority Land Cover Type 2 Assessment: Majority UMD class confidence |
| `Land_Cover_Type_2_Percent_Class_0` | % | 0 | 100 | Percent cover of UMD class 0 (Water Bodies) at each pixel |
| `Land_Cover_Type_2_Percent_Class_1` | % | 0 | 100 | Percent cover of UMD class 1 (Evergreen Needleleaf Forests) at each pixel |
| `Land_Cover_Type_2_Percent_Class_2` | % | 0 | 100 | Percent cover of UMD class 2 (Evergreen Broadleaf Forests) at each pixel |
| `Land_Cover_Type_2_Percent_Class_3` | % | 0 | 100 | Percent cover of UMD class 3 (Deciduous Needleleaf Forests) at each pixel |
| `Land_Cover_Type_2_Percent_Class_4` | % | 0 | 100 | Percent cover of UMD class 4 (Deciduous Broadleaf Forests) at each pixel |
| `Land_Cover_Type_2_Percent_Class_5` | % | 0 | 100 | Percent cover of UMD class 5 (Mixed Forests) at each pixel |
| `Land_Cover_Type_2_Percent_Class_6` | % | 0 | 100 | Percent cover of UMD class 6 (Closed Shrublands) at each pixel |
| `Land_Cover_Type_2_Percent_Class_7` | % | 0 | 100 | Percent cover of UMD class 7 (Open Shrublands) at each pixel |
| `Land_Cover_Type_2_Percent_Class_8` | % | 0 | 100 | Percent cover of UMD class 8 (Woody Savannas) at each pixel |
| `Land_Cover_Type_2_Percent_Class_9` | % | 0 | 100 | Percent cover of UMD class 9 (Savannas) at each pixel |
| `Land_Cover_Type_2_Percent_Class_10` | % | 0 | 100 | Percent cover of UMD class 10 (Grasslands) at each pixel |
| `Land_Cover_Type_2_Percent_Class_11` | % | 0 | 100 | Percent cover of UMD class 11 (Croplands) at each pixel. (Note that "Croplands" has value 12 in Majority\_Land\_Cover\_Type\_2 to match IGBP.) |
| `Land_Cover_Type_2_Percent_Class_12` | % | 0 | 100 | Percent cover of UMD class 12 (Urban and Built\-up Lands) at each pixel. (Note that "Urban and Built\-up Lands" has value 13 in Majority\_Land\_Cover\_Type\_2 to match IGBP.) |
| `Land_Cover_Type_2_Percent_Class_13` | % | 0 | 100 | Percent cover of UMD class 13 (Barren) at each pixel. (Note that "Barren" has value 15 in Majority\_Land\_Cover\_Type\_2\.) |
| `Majority_Land_Cover_Type_3` | None | 0 | 10 | Majority Land Cover Type 3: Most likely LAI class for each 0\.05 degree pixel |
| `Majority_Land_Cover_Type_3_Assessment` | % | 0 | 100 | Majority Land Cover Type 3 Assessment: Majority LAI class confidence |
| `Land_Cover_Type_3_Percent_Class_0` | % | 0 | 100 | Percent cover of LAI class 0 (Water Bodies) at each pixel |
| `Land_Cover_Type_3_Percent_Class_1` | % | 0 | 100 | Percent cover of LAI class 1 (Grasslands) at each pixel |
| `Land_Cover_Type_3_Percent_Class_2` | % | 0 | 100 | Percent cover of LAI class 2 (Shrublands) at each pixel |
| `Land_Cover_Type_3_Percent_Class_3` | % | 0 | 100 | Percent cover of LAI class 3 (Broadleaf Croplands) at each pixel |
| `Land_Cover_Type_3_Percent_Class_4` | % | 0 | 100 | Percent cover of LAI class 4 (Savannas) at each pixel |
| `Land_Cover_Type_3_Percent_Class_5` | % | 0 | 100 | Percent cover of LAI class 5 (Evergreen Broadleaf Forests) at each pixel |
| `Land_Cover_Type_3_Percent_Class_6` | % | 0 | 100 | Percent cover of LAI class 6 (Deciduous Broadleaf Forests) at each pixel |
| `Land_Cover_Type_3_Percent_Class_7` | % | 0 | 100 | Percent cover of LAI class 7 (Evergreen Needleleaf Forests) at each pixel |
| `Land_Cover_Type_3_Percent_Class_8` | % | 0 | 100 | Percent cover of LAI class 8 (Deciduous Needleleaf Forests) at each pixel |
| `Land_Cover_Type_3_Percent_Class_9` | % | 0 | 100 | Percent cover of LAI class 9 (Unvegetated) at each pixel |
| `Land_Cover_Type_3_Percent_Class_10` | % | 0 | 100 | Percent cover of LAI class 10 (Urban and Built\-up Lands) at each pixel |


**Majority\_Land\_Cover\_Type\_1 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#1c0dff | Water Bodies: at least 60% of area is covered by permanent water bodies. |
| 1 | \#05450a | Evergreen Needleleaf Forests: dominated by evergreen conifer trees (canopy \>2m). Tree cover \>60%. |
| 2 | \#086a10 | Evergreen Broadleaf Forests: dominated by evergreen broadleaf and palmate trees (canopy \>2m). Tree cover \>60%. |
| 3 | \#54a708 | Deciduous Needleleaf Forests: dominated by deciduous needleleaf (larch) trees (canopy \>2m). Tree cover \>60%. |
| 4 | \#78d203 | Deciduous Broadleaf Forests: dominated by deciduous broadleaf trees (canopy \>2m). Tree cover \>60%. |
| 5 | \#009900 | Mixed Forests: dominated by neither deciduous nor evergreen (40\-60% of each) tree type (canopy \>2m). Tree cover \>60%. |
| 6 | \#c6b044 | Closed Shrublands: dominated by woody perennials (1\-2m height) \>60% cover. |
| 7 | \#dcd159 | Open Shrublands: dominated by woody perennials (1\-2m height) 10\-60% cover. |
| 8 | \#dade48 | Woody Savannas: tree cover 30\-60% (canopy \>2m). |
| 9 | \#fbff13 | Savannas: tree cover 10\-30% (canopy \>2m). |
| 10 | \#b6ff05 | Grasslands: dominated by herbaceous annuals (\<2m). |
| 11 | \#27ff87 | Permanent Wetlands: permanently inundated lands with 30\-60% water cover and \>10% vegetated cover. |
| 12 | \#c24f44 | cropland. |
| 13 | \#a5a5a5 | Urban and Built\-up Lands: at least 30% impervious surface area including building materials, asphalt and vehicles. |
| 14 | \#ff6d4c | Cropland/Natural Vegetation Mosaics: mosaics of small\-scale cultivation 40\-60% with natural tree, shrub, or herbaceous vegetation. |
| 15 | \#69fff8 | Permanent Snow and Ice: at least 60% of area is covered by snow and ice for at least 10 months of the year. |
| 16 | \#f9ffa4 | (sand, rock, soil) areas with less than 10% vegetation. |


**Majority\_Land\_Cover\_Type\_2 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#1c0dff | Water Bodies: at least 60% of area is covered by permanent water bodies. |
| 1 | \#05450a | Evergreen Needleleaf Forests: dominated by evergreen conifer trees (canopy \>2m). Tree cover \>60%. |
| 2 | \#086a10 | Evergreen Broadleaf Forests: dominated by evergreen broadleaf and palmate trees (canopy \>2m). Tree cover \>60%. |
| 3 | \#54a708 | Deciduous Needleleaf Forests: dominated by deciduous needleleaf (larch) trees (canopy \>2m). Tree cover \>60%. |
| 4 | \#78d203 | Deciduous Broadleaf Forests: dominated by deciduous broadleaf trees (canopy \>2m). Tree cover \>60%. |
| 5 | \#009900 | Mixed Forests: dominated by neither deciduous nor evergreen (40\-60% of each) tree type (canopy \>2m). Tree cover \>60%. |
| 6 | \#c6b044 | Closed Shrublands: dominated by woody perennials (1\-2m height) \>60% cover. |
| 7 | \#dcd159 | Open Shrublands: dominated by woody perennials (1\-2m height) 10\-60% cover. |
| 8 | \#dade48 | Woody Savannas: tree cover 30\-60% (canopy \>2m). |
| 9 | \#fbff13 | Savannas: tree cover 10\-30% (canopy \>2m). |
| 10 | \#b6ff05 | Grasslands: dominated by herbaceous annuals (\<2m). |
| 12 | \#c24f44 | cropland. |
| 13 | \#a5a5a5 | Urban and Built\-up Lands: at least 30% impervious surface area including building materials, asphalt and vehicles. |
| 15 | \#f9ffa4 | non\-vegetated barren (sand, rock, soil) or permanent snow and ice with less than 10% vegetation. |


**Majority\_Land\_Cover\_Type\_3 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#1c0dff | Water Bodies: at least 60% of area is covered by permanent water bodies. |
| 1 | \#b6ff05 | Grasslands: dominated by herbaceous annuals (\<2m) including cereal croplands. |
| 2 | \#dcd159 | Shrublands: shrub (1\-2m) cover \>10%. |
| 3 | \#c24f44 | Broadleaf Croplands: bominated by herbaceous annuals (\<2m) that are cultivated with broadleaf crops. |
| 4 | \#fbff13 | Savannas: between 10\-60% tree cover (\>2m). |
| 5 | \#086a10 | Evergreen Broadleaf Forests: dominated by evergreen broadleaf and palmate trees (canopy \>2m). Tree cover \>60%. |
| 6 | \#78d203 | Deciduous Broadleaf Forests: dominated by deciduous broadleaf trees (canopy \>2m). Tree cover \>60%. |
| 7 | \#05450a | Evergreen Needleleaf Forests: dominated by evergreen conifer trees (canopy \>2m). Tree cover \>60%. |
| 8 | \#54a708 | Deciduous Needleleaf Forests: dominated by deciduous needleleaf (larch) trees (canopy \>2m). Tree cover \>60%. |
| 9 | \#f9ffa4 | non\-vegetated barren (sand, rock, soil) or permanent snow and ice with less than 10% vegetation. |
| 10 | \#a5a5a5 | Urban and Built\-up Lands: at least 30% impervious surface area including building materials, asphalt and vehicles. |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD12C1\.061](https://doi.org/10.5067/MODIS/MCD12C1.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MCD12C1');
varigbpLandCover=dataset.select('Majority_Land_Cover_Type_1');
varigbpLandCoverVis={
min:0,
max:16.0,
palette:[
'1c0dff','05450a','086a10','54a708','78d203','009900','c6b044','dcd159',
'dade48','fbff13','b6ff05','27ff87','c24f44','a5a5a5','ff6d4c',
'69fff8','f9ffa4'
],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(igbpLandCover,igbpLandCoverVis,'IGBP Land Cover');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD12C1)


[MCD12C1\.061 MODIS Land Cover Type Yearly Global 0\.05 Deg CMG](/earth-engine/datasets/catalog/MODIS_061_MCD12C1)

The Terra and Aqua combined Moderate Resolution Imaging Spectroradiometer (MODIS) Land Cover Climate Modeling Grid (CMG) (MCD12C1\) Version 6\.1 data product provides a spatially aggregated and reprojected version of the tiled MCD12Q1 Version 6\.1 data product. Maps of the International Geosphere\-Biosphere Programme (IGBP), University of Maryland (UMD), and Leaf Area …

 MODIS/061/MCD12C1,
 landcover,landuse\-landcover,modis,nasa,usgs,yearly

2001\-01\-01T00:00:00Z/2023\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD12C1\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD12C1.061)
* [https://doi.org/10\.5067/MODIS/MCD12C1\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD12C1)









