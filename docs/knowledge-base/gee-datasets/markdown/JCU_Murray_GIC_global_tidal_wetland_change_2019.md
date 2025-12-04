



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Murray Global Tidal Wetland Change v1\.0 (1999\-2019\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================








Dataset Availability
1999\-01\-01T00:00:00Z–2019\-12\-31T00:00:00Z
Dataset Provider


[Murray/JCU](https://github.com/nick-murray/gee-global-intertidal-change-data-descriptor)



Earth Engine Snippet


`ee.Image("JCU/Murray/GIC/global_tidal_wetland_change/2019")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JCU/JCU_Murray_GIC_global_tidal_wetland_change_2019)





Tags


[coastal](/earth-engine/datasets/tags/coastal)
[ecosystem](/earth-engine/datasets/tags/ecosystem)
[intertidal](/earth-engine/datasets/tags/intertidal)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[mangrove](/earth-engine/datasets/tags/mangrove)
[murray](/earth-engine/datasets/tags/murray)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
saltmarsh
tidal\-flat
tidal\-marsh








#### Description



The Murray Global Tidal Wetland Change Dataset contains maps of the global
extent of tidal wetlands and their change. The maps were developed from a three
stage classification that sought to (i) estimate the global distribution of
tidal wetlands (defined as either tidal marsh, tidal flat or mangrove
ecosystems), (ii) detect their change over the study period, and (iii) estimate
the ecosystem type and timing of tidal wetland change events.


The dataset was produced by combining observations from 1,166,385 satellite
images acquired by Landsat 5 to 8 with environmental data of variables known
to influence the distributions of each ecosystem type, including temperature,
slope, and elevation. The image contains bands for a tidal wetland extent
product (random forest probability of tidal wetland occurrence) for the
start and end time\-steps of the study period and a tidal wetland change product
over the full study period (loss and gain of tidal wetlands).


Please see the [usage notes](https://www.globalintertidalchange.org/data-usage)
on the [project website](https://www.globalintertidalchange.org/). A full
description of the methods, validation, and limitations of the data produced by
this software is available in the associated scientific paper.


See also
[UQ/murray/Intertidal/v1\_1/global\_intertidal](/earth-engine/datasets/catalog/UQ_murray_Intertidal_v1_1_global_intertidal)
for global maps of the distribution of tidal flat ecosystems.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `loss` | Set to 1 for loss locations, masked out otherwise. |
| `lossYear` | Integer representing the end year of the time\-step of loss analysis (e.g., 19 \= 2017\-2019\). |
| `lossType` | Loss type* 2 \- Tidal Flat * 3 \- Mangrove * 5 \- Tidal Marsh |
| `gain` | Set to 1 for gain locations, masked out otherwise. |
| `gainYear` | Integer representing the end year of the time\-step of gain analysis (e.g., 19 \= 2017\-2019\). |
| `gainType` | Gain type:* 2 \- Tidal Flat * 3 \- Mangrove * 5 \- Tidal Marsh |
| `twprobabilityStart` | Random forest agreement of the overarching tidal wetland class for the first time step (1999\-2001\). Integer between 0 and 100\. |
| `twprobabilityEnd` | Random forest agreement of the overarching tidal wetland class for the last time step (2017\-2019\). Integer between 0 and 100\. |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Murray, N.J., Worthington, T.A., Bunting, P., Duce, S., Hagger, V.,
Lovelock, C.E., Lucas, R., Saunders, M.I., Sheaves, M., Spalding, M.,
Waltham, N.J., Lyons, M.B., 2022\. High\-resolution mapping of losses and
gains of Earth's tidal wetlands. *Science*.
[doi:10\.1126/science.abm9583](https://doi.org/10.1126/science.abm9583)





### DOIs


* [https://doi.org/10\.1126/science.abm9583](https://doi.org/10.1126/science.abm9583)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('JCU/Murray/GIC/global_tidal_wetland_change/2019');

Map.setCenter(103.7,1.3,12);
Map.setOptions('SATELLITE');

varplasma=[
'0d0887','3d049b','6903a5','8d0fa1','ae2891','cb4679','df6363',
'f0844c','faa638','fbcc27','f0f921'
];
Map.addLayer(
dataset.select('twprobabilityStart'),{palette:plasma,min:0,max:100},
'twprobabilityStart',false,1);
Map.addLayer(
dataset.select('twprobabilityEnd'),{palette:plasma,min:0,max:100},
'twprobabilityEnd',false,1);

varlossPalette=['fe4a49'];
vargainPalette=['2ab7ca'];
Map.addLayer(
dataset.select('loss'),{palette:lossPalette,min:1,max:1},
'Tidal wetland loss',true,1);
Map.addLayer(
dataset.select('gain'),{palette:gainPalette,min:1,max:1},
'Tidal wetland gain',true,1);

varviridis=['440154','414487','2a788e','22a884','7ad151','fde725'];
Map.addLayer(
dataset.select('lossYear'),{palette:viridis,min:4,max:19},
'Year of loss',false,0.9);
Map.addLayer(
dataset.select('gainYear'),{palette:viridis,min:4,max:19},
'Year of gain',false,0.9);

// Ecosystem type.
varclassPalette=['9e9d9d','ededed','ff9900','009966','960000','006699'];
varclassNames=
['null','null','Tidal flat','Mangrove','null','Tidal marsh'];
Map.addLayer(
dataset.select('lossType'),{palette:classPalette,min:0,max:5},
'Loss type',false,0.9);
Map.addLayer(
dataset.select('gainType'),{palette:classPalette,min:0,max:5},
'Gain type',false,0.9);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JCU/JCU_Murray_GIC_global_tidal_wetland_change_2019)


[Murray Global Tidal Wetland Change v1\.0 (1999\-2019\)](/earth-engine/datasets/catalog/JCU_Murray_GIC_global_tidal_wetland_change_2019)

The Murray Global Tidal Wetland Change Dataset contains maps of the global extent of tidal wetlands and their change. The maps were developed from a three stage classification that sought to (i) estimate the global distribution of tidal wetlands (defined as either tidal marsh, tidal flat or mangrove ecosystems), (ii) …

 JCU/Murray/GIC/global\_tidal\_wetland\_change/2019,
 coastal,ecosystem,intertidal,landsat\-derived,mangrove,murray,surface\-ground\-water

1999\-01\-01T00:00:00Z/2019\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1126/science.abm9583](https://doi.org/https://github.com/nick-murray/gee-global-intertidal-change-data-descriptor)
* [https://doi.org/10\.1126/science.abm9583](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JCU_Murray_GIC_global_tidal_wetland_change_2019)









