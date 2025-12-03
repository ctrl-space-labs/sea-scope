



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MERIT Hydro: Supplementary Visualization Layers


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================








Dataset Availability
1987\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[Dai Yamazaki (University of Tokyo)](http://hydro.iis.u-tokyo.ac.jp/~yamadai/MERIT_Hydro/index.html)



Earth Engine Snippet


`ee.Image("MERIT/Hydro_reduced/v1_0_1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MERIT/MERIT_Hydro_reduced_v1_0_1)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[flow\-direction](/earth-engine/datasets/tags/flow-direction)
[hand](/earth-engine/datasets/tags/hand)
[hydrography](/earth-engine/datasets/tags/hydrography)
[hydrosheds](/earth-engine/datasets/tags/hydrosheds)
[merit](/earth-engine/datasets/tags/merit)
[river\-width](/earth-engine/datasets/tags/river-width)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[upstream\-drainage\-area](/earth-engine/datasets/tags/upstream-drainage-area)








#### Description



Supplementary visualization layers for [MERIT Hydro](/earth-engine/datasets/catalog/MERIT_Hydro_v1_0_1)





### Bands



**Pixel Size**
  
556\.6 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `wth` | None | River channel width at the channel centerlines. River channel width is calculated by the method described in \[Yamazaki et al. 2012, WRR], with some improvements/changes on the algorithm. This band was upscaled to 18 arc seconds from the original 3 arc seconds for better visualization at global scale. |
| `upa` | km^2 | Upstream drainage area (flow accumulation area). This band was upscaled to 18 arc seconds from the original 3 arc seconds for better visualization at global scale. |




### Terms of Use


**Terms of Use**


Citation to the paper is adequate if you simply use MERIT Hydro. If you
asked for help for additional handling/editing of the dataset, or if your research
outcome highly depends on the product, the developer would request co\-authorship.


MERIT Hydro is licensed under a Creative Commons "CC\-BY\-NC 4\.0" or Open
Data Commons "Open Database License (ODbL 1\.0\)". With a dual license, you can
choose an appropriate license for you.


To view a copy of these license, please visit:


* [CC\-BY\-NC 4\.0 license](http://creativecommons.org/licenses/by-nc/4.0/):
Non\-Commercial Use with less restriction.
* [ODbL 1\.0 license](https://opendatacommons.org/licenses/odbl/summary/):
Commectial Use is OK, but the derived data based on MERIT Hydro should be made
publicly available under the same ODbL license. For example, if you create a
flood hazard map using MERIT Hydro and you would like to provide a COMMERCIAL
service based on that, you have to make the hazard map PUBLICLY AVAILABLE under
OdBL license.


Note that the above license terms are applied to the "derived data" based
on MERIT Hydro, while they are not applied to "produced work / artwork" created
with MERIT Hydro (such as figures in a journal paper). The users may have a
copyright of the artwork and may assign any license, when the produced work
is not considered as "derived data".


By downloading and using the data the user agrees to the terms and
conditions of the license. Notwithstanding this free license, we ask users to
refrain from redistributing the data in whole in its original format on other
websites without the explicit written permission from the authors.


The copyright of MERIT Hydro is held by the developers, 2019, all rights reserved.




### Citations



Citations:
* Yamazaki D., D. Ikeshima, J. Sosa, P.D. Bates, G.H. Allen, T.M. Pavelsky.
MERIT Hydro: A high\-resolution global hydrography map based on latest
topography datasets
Water Resources Research, vol.55, pp.5053\-5073, 2019,
[doi:10\.1029/2019WR024873](https://doi.org/10.1029/2019WR024873)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('MERIT/Hydro_reduced/v1_0_1');

varvisualization={
bands:'wth',
min:0,
max:400
};

Map.setCenter(90.301,23.052,10);

Map.addLayer(dataset,visualization,'River width');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MERIT/MERIT_Hydro_reduced_v1_0_1)


[MERIT Hydro: Supplementary Visualization Layers](/earth-engine/datasets/catalog/MERIT_Hydro_reduced_v1_0_1)

Supplementary visualization layers for MERIT Hydro

 MERIT/Hydro\_reduced/v1\_0\_1,
 dem,elevation,flow\-direction,hand,hydrography,hydrosheds,merit,river\-width,surface\-ground\-water,upstream\-drainage\-area

1987\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








