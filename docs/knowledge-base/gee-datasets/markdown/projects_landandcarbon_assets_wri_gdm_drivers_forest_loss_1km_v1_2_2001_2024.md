



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WRI/Google DeepMind Global Drivers of Forest Loss 2001\-2024 v1\.2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================================









info


 This dataset is part of a Publisher Catalog, and not managed by Google Earth Engine.
 
 Contact [Land \& Carbon Lab](https://landcarbonlab.org/contact/)
 
 for bugs or [view more datasets](https://developers.google.com/earth-engine/datasets/publisher/landandcarbon)
 from the Land \& Carbon Lab Catalog. [Learn more about Publisher datasets](/earth-engine/datasets/publisher).
 






Catalog Owner
Land \& Carbon Lab
Dataset Availability
2001\-01\-01T00:00:00Z–2025\-01\-01T00:00:00Z
Dataset Provider


[World Resources Institute](https://zenodo.org/records/15366671)


[Google DeepMind](https://deepmind.google/)


Contact
[Land \& Carbon Lab](https://landcarbonlab.org/contact/)

Earth Engine Snippet


`ee.Image("projects/landandcarbon/assets/wri_gdm_drivers_forest_loss_1km/v1_2_2001_2024")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/landandcarbon/projects_landandcarbon_assets_wri_gdm_drivers_forest_loss_1km_v1_2_2001_2024)





Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[deforestation](/earth-engine/datasets/tags/deforestation)
[forest](/earth-engine/datasets/tags/forest)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[google](/earth-engine/datasets/tags/google)
[landandcarbon](/earth-engine/datasets/tags/landandcarbon)
[landuse](/earth-engine/datasets/tags/landuse)
[publisher\-dataset](/earth-engine/datasets/tags/publisher-dataset)
[wri](/earth-engine/datasets/tags/wri)








#### Description



This dataset maps the dominant driver of tree cover loss from 2001\-2024 globally at 1 km resolution. 
Produced by the World Resources Institute (WRI) and Google DeepMind, the data were developed using 
a global neural network model (ResNet) trained on a set of samples collected through visual 
interpretation of very high\-resolution satellite imagery. The model used satellite imagery 
(Landsat 7 \& 8, Sentinel\-2\) and ancillary data to classify seven driver categories: 
permanent agriculture, hard commodities, shifting cultivation, logging, wildfires, 
settlements and infrastructure, and other natural disturbances. An independent stratified random 
sample collected through interpretation of very high resolution satellite imagery was used to 
estimate the accuracy of the map. 


A *driver* is defined as the direct cause of tree cover loss, and can include both temporary 
disturbances (natural or anthropogenic) or permanent loss of tree cover due to a change to 
a non\-forest land use (e.g., deforestation). The *dominant* driver is defined as the 
direct driver that caused the majority of tree cover loss within each 1 km cell over the time 
period. Classes are defined as follows:


* Permanent agriculture: Long\-term, permanent tree cover loss for small\- to large\-scale agriculture. 
This includes perennial tree crops, as well as pasture and seasonal crops and cropping systems, 
which may include a fallow period. Agricultural activities are considered "permanent" if there 
is visible evidence that they persist following the tree cover loss event and are not a part of 
a temporary cultivation cycle.
* Hard commodities: Loss due to the establishment or expansion of mining or energy infrastructure.
* Shifting cultivation: Tree cover loss due to small\- to medium\-scale clearing for temporary 
cultivation that is later abandoned and followed by subsequent regrowth of secondary forest or 
vegetation.
* Logging: Forest management and logging activities occurring within managed, natural or semi\-natural 
forests and plantations, often with evidence of forest regrowth or planting in subsequent years. 
Includes clear\-cut and selective logging, establishment of logging roads, forest thinning, and 
salvage or sanitation logging.
* Wildfire: Tree cover loss due to fire with no visible human conversion or agricultural activity 
afterward. Fires may be started by natural causes (e.g. lightning) or may be related to human 
activities (accidental or deliberate).
* Settlements and infrastructure: Tree cover loss due to expansion and intensification of roads, 
settlements, urban areas, or built infrastructure (not associated with other classes).
* Other natural disturbances: Tree cover loss due to other non\-fire natural disturbances 
(e.g., landslides, insect outbreaks, river meandering). If loss due to natural causes is followed 
by salvage or sanitation logging, it is classified as forest management.


**Limitations**: This product does not distinguish between the loss of *natural forest* and *planted 
trees* (e.g., plantations, tree crops, or agroforestry systems). While tree cover loss associated 
with the *permanent agriculture*, *hard commodities*, and *settlements and infrastructure* classes represent 
a close approximation of deforestation (permanent conversion of forest to another land use), these 
classes may sometimes include the clearing of planted trees. For example, clearing and replanting an 
orchard would be included in the *permanent agriculture* class, but is not deforestation of a natural forest. 
Similarly, replacement of natural forest with wood fiber plantations is not distinguished from routine 
harvesting within existing plantations established before 2000, as these are both included in the logging 
class. 


This product shows the dominant driver in each 1km cell over the entire period. It does not show 
multiple drivers if they occur in the same cell at smaller scales, nor does it detail the sequence of 
drivers if multiple occurred at different times within the period. Additionally, these data are limited 
in scope to attributing drivers to tree cover loss as mapped by the 
[Global Forest Change v1\.12](https://www.science.org/doi/10.1126/science.1244693) tree cover loss product, 
and therefore the detection of loss is subject to the accuracy of that product. 


**For a full description of the methods, technical specifications, definitions, accuracy, and 
limitations, please see the publication**: 
[https://doi.org/10\.1088/1748\-9326/add606](https://doi.org/10.1088/1748-9326/add606). 
The data is also available for download on [Zenodo](https://zenodo.org/records/15366671) and 
the [WRI Data Explorer](https://datasets.wri.org/datasets/dominant-drivers-of-tree-cover-loss-at-1km). 





### Bands



**Pixel Size**
  
1111\.95 meters



**Bands**




| Name | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- |
| `classification` | 1 | 7 |  | Most likely class based on raw probabilities. |
| `probability_1` | 0 | 250 | 0\.004 | Probability of "Permanent agriculture" class (scaled to \[0\-250]). |
| `probability_2` | 0 | 250 | 0\.004 | Probability of "Hard commodities" class (scaled to \[0\-250]). |
| `probability_3` | 0 | 250 | 0\.004 | Probability of "Shifting cultivation" class (scaled to \[0\-250]). |
| `probability_4` | 0 | 250 | 0\.004 | Probability of "Logging" class (scaled to \[0\-250]). |
| `probability_5` | 0 | 250 | 0\.004 | Probability of "Wildfire" class (scaled to \[0\-250]). |
| `probability_6` | 0 | 250 | 0\.004 | Probability of "Settlements and infrastructure" class (scaled to \[0\-250]). |
| `probability_7` | 0 | 250 | 0\.004 | Probability of "Other natural disturbances" class (scaled to \[0\-250]). |


**classification Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#E39D29 | Permanent agriculture |
| 2 | \#E58074 | Hard commodities |
| 3 | \#E9D700 | Shifting cultivation |
| 4 | \#51A44E | Logging |
| 5 | \#895128 | Wildfire |
| 6 | \#A354A0 | Settlements and infrastructure |
| 7 | \#3A209A | Other natural disturbances |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Sims, M., Stanimirova, R., Raichuk, A., Neumann, M., Richter, J., Follett, F., 
MacCarthy, J., Lister, K., Randle, C., Sloat, L., Esipova, E., Jupiter, J., Stanton, 
C., Morris, D., Slay, C. M., Purves, D., and Harris, N. (2025\). 
Global drivers of forest loss at 1 km resolution. 
Environmental Research Letters. 
[doi:10\.1088/1748\-9326/add606](https://doi.org/10.1088/1748-9326/add606)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
Map.setCenter(-9.22,20.65,3)

vardrivers=ee.Image('projects/landandcarbon/assets/wri_gdm_drivers_forest_loss_1km/v1_2_2001_2024');

vardrivers_class=drivers.select(['classification']);

varvis={
"min":1,
"max":7,
"palette":['E39D29','E58074','e9d700','51a44e','895128','a354a0','3a209a']
};

Map.addLayer(drivers_class,vis,'Drivers of Forest Loss, 2001-2024');

varpermAg_prob=drivers.select(['probability_1']);//Select a probability band

varprobVis={
min:0,
max:250,
palette:['#440154','#481567','#482677','#453781','#3b528b','#2c728e','#21908d','#27ad81','#5ec962','#aadc32','#fde725']
};

Map.addLayer(permAg_prob,probVis,'Probability band for permanent agriculture',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/landandcarbon/projects_landandcarbon_assets_wri_gdm_drivers_forest_loss_1km_v1_2_2001_2024)


[WRI/Google DeepMind Global Drivers of Forest Loss 2001\-2024 v1\.2](/earth-engine/datasets/catalog/projects_landandcarbon_assets_wri_gdm_drivers_forest_loss_1km_v1_2_2001_2024)

This dataset maps the dominant driver of tree cover loss from 2001\-2024 globally at 1 km resolution. Produced by the World Resources Institute (WRI) and Google DeepMind, the data were developed using a global neural network model (ResNet) trained on a set of samples collected through visual interpretation of very …

 projects/landandcarbon/assets/wri\_gdm\_drivers\_forest\_loss\_1km/v1\_2\_2001\_2024,
 agriculture,deforestation,forest,forest\-biomass,google,landandcarbon,landuse,publisher\-dataset,wri

2001\-01\-01T00:00:00Z/2025\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








