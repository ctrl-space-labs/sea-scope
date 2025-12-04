



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Potential Distribution of Biomes


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2002\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.7910/DVN/QQHCIK)



Earth Engine Snippet


`ee.Image("OpenLandMap/PNV/PNV_BIOME-TYPE_BIOME00K_C/v01")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_PNV_PNV_BIOME-TYPE_BIOME00K_C_v01)





Tags


[ecosystems](/earth-engine/datasets/tags/ecosystems)
[envirometrix](/earth-engine/datasets/tags/envirometrix)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[potential](/earth-engine/datasets/tags/potential)
biome








#### Description



Potential Natural Vegetation biomes global predictions of classes
(based on predictions using the BIOMES 6000 dataset's 'current biomes' category.)


Potential Natural Vegetation (PNV) is the vegetation cover in equilibrium with climate
that would exist at a given location non\-impacted by human activities. PNV is useful for raising
public awareness about land degradation and for estimating land potential.
This dataset contains results of predictions of
\- (1\) global distribution of biomes based on the BIOME 6000 data set (8057 modern pollen\-based site reconstructions),
\- (2\) distribution of forest tree species in Europe based on detailed occurrence records (1,546,435 ground observations), and
\- (3\) global monthly Fraction of Absorbed Photosynthetically Active Radiation (FAPAR) values (30,301 randomly\-sampled points).


To report an issue or artifact in data, please use [this link](https://github.com/envirometrix/PNVmaps/issues).


To access and visualize maps outside of Earth Engine, use [this page](https://opengeohub.org/about-openlandmap).


If you discover a bug, artifact or inconsistency in the LandGIS maps
or if you have a question please use the following channels:


* [Technical issues and questions about the code](https://gitlab.com/openlandmap/global-layers/issues)
* [General questions and comments](https://disqus.com/home/forums/landgis/)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Description |
| --- | --- |
| `biome_type` | Potential distribution of biomes |


**biome\_type Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#1c5510 | tropical evergreen broadleaf forest |
| 2 | \#659208 | tropical semi\-evergreen broadleaf forest |
| 3 | \#ae7d20 | tropical deciduous broadleaf forest and woodland |
| 4 | \#000065 | warm\-temperate evergreen broadleaf and mixed forest |
| 7 | \#bbcb35 | cool\-temperate rainforest |
| 8 | \#009a18 | cool evergreen needleleaf forest |
| 9 | \#caffca | cool mixed forest |
| 13 | \#55eb49 | temperate deciduous broadleaf forest |
| 14 | \#65b2ff | cold deciduous forest |
| 15 | \#0020ca | cold evergreen needleleaf forest |
| 16 | \#8ea228 | temperate sclerophyll woodland and shrubland |
| 17 | \#ff9adf | temperate evergreen needleleaf open woodland |
| 18 | \#baff35 | tropical savanna |
| 20 | \#ffba9a | xerophytic woods/scrub |
| 22 | \#ffba35 | steppe |
| 27 | \#f7ffca | desert |
| 28 | \#e7e718 | graminoid and forb tundra |
| 30 | \#798649 | erect dwarf shrub tundra |
| 31 | \#65ff9a | low and high shrub tundra |
| 32 | \#d29e96 | prostrate dwarf shrub tundra |




### Terms of Use


**Terms of Use**


This is a human\-readable summary of (and not a substitute for) the [license](https://creativecommons.org/licenses/by-sa/4.0/).


You are free to \-
 Share \- copy and redistribute the material in any medium or format
 Adapt \- remix, transform, and build upon the material for any purpose, even commercially.


This license is acceptable for Free Cultural Works.
The licensor cannot revoke these freedoms as long as you follow the license terms.


Under the following terms \-
 Attribution \- You must give appropriate credit, provide a link to the license, and indicate if
 changes were made. You may do so in any reasonable manner, but not in any way that suggests the
 licensor endorses you or your use.


ShareAlike \- If you remix, transform, or build upon the material, you must distribute your
 contributions under the same license as the original.


No additional restrictions \- You may not apply legal terms or technological measures that
 legally restrict others from doing anything the license permits.




### Citations



Citations:
* Hengl T, Walsh MG, Sanderman J, Wheeler I, Harrison SP, Prentice IC. (2018\) Global Mapping of Potential Natural Vegetation: An Assessment of Machine Learning Algorithms for Estimating Land Potential. PeerJ Preprints.
[10\.7287/peerj.preprints.26811v1](https://doi.org/10.7910/DVN/QQHCIK)





### DOIs


* [https://doi.org/10\.7910/DVN/QQHCIK](https://doi.org/10.7910/DVN/QQHCIK)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/PNV/PNV_BIOME-TYPE_BIOME00K_C/v01');

varvisualization={
bands:['biome_type'],
min:1.0,
max:32.0,
palette:[
'1c5510','659208','ae7d20','000065','bbcb35','009a18',
'caffca','55eb49','65b2ff','0020ca','8ea228','ff9adf',
'baff35','ffba9a','ffba35','f7ffca','e7e718','798649',
'65ff9a','d29e96',
]
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Potential distribution of biomes');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_PNV_PNV_BIOME-TYPE_BIOME00K_C_v01)


[OpenLandMap Potential Distribution of Biomes](/earth-engine/datasets/catalog/OpenLandMap_PNV_PNV_BIOME-TYPE_BIOME00K_C_v01)

Potential Natural Vegetation biomes global predictions of classes (based on predictions using the BIOMES 6000 dataset's 'current biomes' category.) Potential Natural Vegetation (PNV) is the vegetation cover in equilibrium with climate that would exist at a given location non\-impacted by human activities. PNV is useful for raising public awareness about …

 OpenLandMap/PNV/PNV\_BIOME\-TYPE\_BIOME00K\_C/v01,
 ecosystems,envirometrix,opengeohub,openlandmap,potential

2001\-01\-01T00:00:00Z/2002\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7910/DVN/QQHCIK](https://doi.org/https://doi.org/10.7910/DVN/QQHCIK)
* [https://doi.org/10\.7910/DVN/QQHCIK](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_PNV_PNV_BIOME-TYPE_BIOME00K_C_v01)









