



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD12Q1\.061 MODIS Land Cover Type Yearly Global 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2023\-01\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MCD12Q1.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD12Q1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD12Q1)





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
(MODIS) Land Cover Type (MCD12Q1\) Version 6\.1 data product provides global
land cover types at yearly intervals. The MCD12Q1 Version 6\.1
data product is derived using supervised classifications of MODIS Terra and
Aqua reflectance data. Land cover types are derived from the International
Geosphere\-Biosphere Programme (IGBP), University of Maryland (UMD), Leaf
Area Index (LAI), BIOME\-Biogeochemical Cycles (BGC), and Plant Functional
Types (PFT) classification schemes. The supervised classifications then
underwent additional post\-processing that incorporate prior knowledge and
ancillary information to further refine specific classes. Additional land
cover property assessment layers are provided by the Food and Agriculture
Organization (FAO) Land Cover Classification System (LCCS) for land cover,
land use, and surface hydrology.


Layers for Land Cover Type 1\-5, Land Cover Property 1\-3, Land Cover Property
Assessment 1\-3, Land Cover Quality Control (QC), and a Land Water Mask are
also provided.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/1409/MCD12_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/86/MCD12_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MCD12Q1)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `LC_Type1` | None | Land Cover Type 1: Annual International Geosphere\-Biosphere Programme (IGBP) classification |
| `LC_Type2` | None | Land Cover Type 2: Annual University of Maryland (UMD) classification |
| `LC_Type3` | None | Land Cover Type 3: Annual Leaf Area Index (LAI) classification |
| `LC_Type4` | None | Land Cover Type 4: Annual BIOME\-Biogeochemical Cycles (BGC) classification |
| `LC_Type5` | None | Land Cover Type 5: Annual Plant Functional Types classification |
| `LC_Prop1_Assessment` | % | 0 | 100 | LCCS1 land cover layer confidence |
| `LC_Prop2_Assessment` | % | 0 | 100 | LCCS2 land use layer confidence |
| `LC_Prop3_Assessment` | % | 0 | 100 | LCCS3 surface hydrology layer confidence |
| `LC_Prop1` | None | FAO\-Land Cover Classification System 1 (LCCS1\) land cover layer |
| `LC_Prop2` | None | FAO\-LCCS2 land use layer |
| `LC_Prop3` | None | FAO\-LCCS3 surface hydrology layer |
| `QC` | None | Product quality flags |
| `LW` | None | Binary land (class 2\) / water (class 1\) mask derived from MOD44W |


**LC\_Type1 Class Table**




| Value | Color | Description |
| --- | --- | --- |
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
| 17 | \#1c0dff | Water Bodies: at least 60% of area is covered by permanent water bodies. |


**LC\_Type2 Class Table**




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
| 15 | \#f9ffa4 | Non\-Vegetated Lands: at least 60% of area is non\-vegetated barren (sand, rock, soil) or permanent snow and ice with less than 10% vegetation. |


**LC\_Type3 Class Table**




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
| 9 | \#f9ffa4 | Non\-Vegetated Lands: at least 60% of area is non\-vegetated barren (sand, rock, soil) or permanent snow and ice with less than 10% vegetation. |
| 10 | \#a5a5a5 | Urban and Built\-up Lands: at least 30% impervious surface area including building materials, asphalt and vehicles. |


**LC\_Type4 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#1c0dff | Water Bodies: at least 60% of area is covered by permanent water bodies. |
| 1 | \#05450a | Evergreen Needleleaf Vegetation: dominated by evergreen conifer trees and shrubs (\>1m). Woody vegetation cover \>10%. |
| 2 | \#086a10 | Evergreen Broadleaf Vegetation: dominated by evergreen broadleaf and palmate trees and shrubs (\>1m). Woody vegetation cover  10%. |
| 3 | \#54a708 | Deciduous Needleleaf Vegetation: dominated by deciduous needleleaf (larch) trees and shrubs (\>1m). Woody vegetation cover  10%. |
| 4 | \#78d203 | Deciduous Broadleaf Vegetation: dominated by deciduous broadleaf trees and shrubs (\>1m). Woody vegetation cover \>10%. |
| 5 | \#009900 | Annual Broadleaf Vegetation: dominated by herbaceous annuals (\<2m). At least 60% cultivated broadleaf crops. |
| 6 | \#b6ff05 | Annual Grass Vegetation: dominated by herbaceous annuals (\<2m) including cereal croplands. |
| 7 | \#f9ffa4 | Non\-Vegetated Lands: at least 60% of area is non\-vegetated barren (sand, rock, soil) or permanent snow/ice with less than 10% vegetation. |
| 8 | \#a5a5a5 | Urban and Built\-up Lands: at least 30% impervious surface area including building materials, asphalt, and vehicles. |


**LC\_Type5 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#1c0dff | Water Bodies: at least 60% of area is covered by permanent water bodies. |
| 1 | \#05450a | Evergreen Needleleaf Trees: dominated by evergreen conifer trees (\>2m). Tree cover \>10%. |
| 2 | \#086a10 | Evergreen Broadleaf Trees: dominated by evergreen broadleaf and palmate trees (\>2m). Tree cover \>10%. |
| 3 | \#54a708 | Deciduous Needleleaf Trees: dominated by deciduous needleleaf (larch) trees (\>2m). Tree cover \>10%. |
| 4 | \#78d203 | Deciduous Broadleaf Trees: dominated by deciduous broadleaf trees (\>2m). Tree cover \>10%. |
| 5 | \#dcd159 | Shrub: Shrub (1\-2m) cover \>10%. |
| 6 | \#b6ff05 | not cultivated. |
| 7 | \#dade48 | Cereal Croplands: dominated by herbaceous annuals (\<2m). At least 60% cultivated cereal crops. |
| 8 | \#c24f44 | Broadleaf Croplands: dominated by herbaceous annuals (\<2m). At least 60% cultivated broadleaf crops. |
| 9 | \#a5a5a5 | Urban and Built\-up Lands: at least 30% impervious surface area including building materials, asphalt, and vehicles. |
| 10 | \#69fff8 | Permanent Snow and Ice: at least 60% of area is covered by snow and ice for at least 10 months of the year. |
| 11 | \#f9ffa4 | Non\-Vegetated Lands: at least 60% of area is non\-vegetated barren (sand, rock, soil) with less than 10% vegetation. |


**LC\_Prop1 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#f9ffa4 | (sand, rock, soil) or permanent snow/ice with less than 10% vegetation. |
| 2 | \#69fff8 | Permanent Snow and Ice: at least 60% of area is covered by snow and ice for at least 10 months of the year. |
| 3 | \#1c0dff | Water Bodies: at least 60% of area is covered by permanent water bodies. |
| 11 | \#05450a | Evergreen Needleleaf Forests: dominated by evergreen conifer trees (\>2m). Tree cover \>60%. |
| 12 | \#086a10 | Evergreen Broadleaf Forests: dominated by evergreen broadleaf and palmate trees (\>2m). Tree cover \>60%. |
| 13 | \#54a708 | Deciduous Needleleaf Forests: dominated by deciduous needleleaf (larch) trees (\>2m). Tree cover \>60%. |
| 14 | \#78d203 | Deciduous Broadleaf Forests: dominated by deciduous broadleaf trees (\>2m). Tree cover \>60%. |
| 15 | \#005a00 | Mixed Broadleaf/Needleleaf Forests: co\-dominated (40\-60%) by broadleaf deciduous and evergreen needleleaf tree (\>2m) types. Tree cover \>60%. |
| 16 | \#009900 | Mixed Broadleaf Evergreen/Deciduous Forests: co\-dominated (40\-60%) by broadleaf evergreen and deciduous tree (\>2m) types. Tree cover \>60%. |
| 21 | \#006c00 | Open Forests: tree cover 30\-60% (canopy \>2m). |
| 22 | \#00d000 | Sparse Forests: tree cover 10\-30% (canopy \>2m). |
| 31 | \#b6ff05 | Dense Herbaceous: dominated by herbaceous annuals (\<2m) at least 60% cover. |
| 32 | \#98d604 | Sparse Herbaceous: dominated by herbaceous annuals (\<2m) 10\-60% cover. |
| 41 | \#dcd159 | Dense Shrublands: dominated by woody perennials (1\-2m)  60% cover. |
| 42 | \#f1fb58 | Shrubland/Grassland Mosaics: dominated by woody perennials (1\-2m) 10\-60% cover with dense herbaceous annual understory. |
| 43 | \#fbee65 | Sparse Shrublands: dominated by woody perennials (1\-2m) 10\-60% cover with minimal herbaceous understory. |


**LC\_Prop2 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#f9ffa4 | (sand, rock, soil) or permanent snow/ice with less than 10% vegetation. |
| 2 | \#69fff8 | Permanent Snow and Ice: at least 60% of area is covered by snow and ice for at least 10 months of the year. |
| 3 | \#1c0dff | Water Bodies: at least 60% of area is covered by permanent water bodies. |
| 9 | \#a5a5a5 | Urban and Built\-up Lands: at least 30% of area is made up ofimpervious surfaces including building materials, asphalt, and vehicles. |
| 10 | \#003f00 | Dense Forests: tree cover \>60% (canopy \>2m). |
| 20 | \#006c00 | Open Forests: tree cover 10\-60% (canopy \>2m). |
| 25 | \#e3ff77 | Forest/Cropland Mosaics: mosaics of small\-scale cultivation 40\-60% with \>10% natural tree cover. |
| 30 | \#b6ff05 | Natural Herbaceous: dominated by herbaceous annuals (\<2m). At least 10% cover. |
| 35 | \#93ce04 | Natural Herbaceous/Croplands Mosaics: mosaics of small\-scale cultivation 40\-60% with natural shrub or herbaceous vegetation. |
| 36 | \#77a703 | Herbaceous Croplands: dominated by herbaceous annuals (\<2m). At least 60% cover. Cultivated fraction \>60%. |
| 40 | \#dcd159 | Shrublands: shrub cover \>60% (1\-2m). |


**LC\_Prop3 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#f9ffa4 | (sand, rock, soil) or permanent snow/ice with less than 10% vegetation. |
| 2 | \#69fff8 | Permanent Snow and Ice: at least 60% of area is covered by snow and ice for at least 10 months of the year. |
| 3 | \#1c0dff | Water Bodies: at least 60% of area is covered by permanent water bodies. |
| 10 | \#003f00 | Dense Forests: tree cover \>60% (canopy \>2m). |
| 20 | \#006c00 | Open Forests: tree cover 10\-60% (canopy \>2m). |
| 27 | \#72834a | Woody Wetlands: shrub and tree cover \>10% (\>1m). Permanently or seasonally inundated. |
| 30 | \#b6ff05 | Grasslands: dominated by herbaceous annuals (\<2m) \>10% cover. |
| 40 | \#c6b044 | Shrublands: shrub cover \>60% (1\-2m). |
| 50 | \#3aba73 | Herbaceous Wetlands: dominated by herbaceous annuals (\<2m) \>10% cover. Permanently or seasonally inundated. |
| 51 | \#1e9db3 | months of the year. |


**QC Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | Classified land: has a classification label and is land according to the water mask. |
| 1 | None | Unclassified land: not classified because of missing data but land according to the water mask, labeled as barren. |
| 2 | None | Classified water: has a classification label and is water according to the water mask. |
| 3 | None | Unclassified water: not classified because of missing data but water according to the water mask. |
| 4 | None | Classified sea ice: classified as snow/ice but water mask says it is water and less than 100m elevation, switched to water. |
| 5 | None | Misclassified water: classified as water but water mask says it is land, switched to secondary label. |
| 6 | None | Omitted snow/ice: land according to the water mask that was classified as something other than snow but with a maximum annual temperature below 1°C, relabeled as snow/ice. |
| 7 | None | Misclassified snow/ice: land according to the water mask that was classified as snow but with a minimum annual temperature greater than 1°C, relabeled as barren. |
| 8 | None | Backfilled label: missing label from stabilization, filled with the pre\-stabilized result. |
| 9 | None | Forest type changed: climate\-based change to forest class. |


**LW Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#1c0dff | Water |
| 2 | \#f9ffa4 | Land, |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD12Q1\.061](https://doi.org/10.5067/MODIS/MCD12Q1.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MCD12Q1');
varigbpLandCover=dataset.select('LC_Type1');
varigbpLandCoverVis={
min:1.0,
max:17.0,
palette:[
'05450a','086a10','54a708','78d203','009900','c6b044','dcd159',
'dade48','fbff13','b6ff05','27ff87','c24f44','a5a5a5','ff6d4c',
'69fff8','f9ffa4','1c0dff'
],
};
Map.setCenter(6.746,46.529,6);
Map.addLayer(igbpLandCover,igbpLandCoverVis,'IGBP Land Cover');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD12Q1)


[MCD12Q1\.061 MODIS Land Cover Type Yearly Global 500m](/earth-engine/datasets/catalog/MODIS_061_MCD12Q1)

The Terra and Aqua combined Moderate Resolution Imaging Spectroradiometer (MODIS) Land Cover Type (MCD12Q1\) Version 6\.1 data product provides global land cover types at yearly intervals. The MCD12Q1 Version 6\.1 data product is derived using supervised classifications of MODIS Terra and Aqua reflectance data. Land cover types are derived from …

 MODIS/061/MCD12Q1,
 landcover,landuse\-landcover,modis,nasa,usgs,yearly

2001\-01\-01T00:00:00Z/2023\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD12Q1\.061](https://doi.org/https://doi.org/10.5067/MODIS/MCD12Q1.061)
* [https://doi.org/10\.5067/MODIS/MCD12Q1\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD12Q1)









