



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Potential FAPAR Monthly


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2002\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.7910/DVN/QQHCIK)



Earth Engine Snippet


`ee.Image("OpenLandMap/PNV/PNV_FAPAR_PROBA-V_D/v01")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_PNV_PNV_FAPAR_PROBA-V_D_v01)





Tags


[envirometrix](/earth-engine/datasets/tags/envirometrix)
[fapar](/earth-engine/datasets/tags/fapar)
[monthly](/earth-engine/datasets/tags/monthly)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[plant\-productivity](/earth-engine/datasets/tags/plant-productivity)
[potential](/earth-engine/datasets/tags/potential)








#### Description



Potential Natural Vegetation FAPAR predicted monthly median (based on PROB\-V FAPAR 2014\-2017\).
[Description](https://gitlab.com/openlandmap/global-layers/#potential-natural-vegetation).


To access and visualize maps outside of Earth Engine, use [this page](https://opengeohub.org/about-openlandmap).


If you discover a bug, artifact or inconsistency in the LandGIS maps
or if you have a question please use the following channels:


* [Technical issues and questions about the code](https://gitlab.com/openlandmap/global-layers/issues)
* [General questions and comments](https://disqus.com/home/forums/landgis/)





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `jan` | Fraction | 0\* | 220\* | Jan Potential FAPAR monthly |
| `feb` | Fraction | 0\* | 220\* | Feb Potential FAPAR monthly |
| `mar` | Fraction | 0\* | 220\* | Mar Potential FAPAR monthly |
| `apr` | Fraction | 0\* | 220\* | Apr Potential FAPAR monthly |
| `may` | Fraction | 0\* | 220\* | May Potential FAPAR monthly |
| `jun` | Fraction | 0\* | 220\* | Jun Potential FAPAR monthly |
| `jul` | Fraction | 0\* | 220\* | Jul Potential FAPAR monthly |
| `aug` | Fraction | 0\* | 220\* | Aug Potential FAPAR monthly |
| `sep` | Fraction | 0\* | 220\* | Sep Potential FAPAR monthly |
| `oct` | Fraction | 0\* | 220\* | Oct Potential FAPAR monthly |
| `nov` | Fraction | 0\* | 220\* | Nov Potential FAPAR monthly |
| `dec` | Fraction | 0\* | 220\* | Dec Potential FAPAR monthly |
| `annual` | Fraction | 0\* | 220\* | Anuual Potential FAPAR monthly |
| `annualdiff` | Fraction | 0\* | 220\* | Annual Difference Potential FAPAR monthly |


 \* estimated min or max value


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
[10\.7287/peerj.preprints.26811v5](https://doi.org/10.7910/DVN/QQHCIK)





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
vardataset=ee.Image('OpenLandMap/PNV/PNV_FAPAR_PROBA-V_D/v01');

varvisualization={
bands:['jan'],
min:0.0,
max:220.0,
palette:['0000ff','00ffff','ffff00','ff0000']
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Potential FAPAR monthly');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_PNV_PNV_FAPAR_PROBA-V_D_v01)


[OpenLandMap Potential FAPAR Monthly](/earth-engine/datasets/catalog/OpenLandMap_PNV_PNV_FAPAR_PROBA-V_D_v01)

Potential Natural Vegetation FAPAR predicted monthly median (based on PROB\-V FAPAR 2014\-2017\). Description. To access and visualize maps outside of Earth Engine, use this page. If you discover a bug, artifact or inconsistency in the LandGIS maps or if you have a question please use the following channels: Technical issues …

 OpenLandMap/PNV/PNV\_FAPAR\_PROBA\-V\_D/v01,
 envirometrix,fapar,monthly,opengeohub,openlandmap,plant\-productivity,potential

2001\-01\-01T00:00:00Z/2002\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7910/DVN/QQHCIK](https://doi.org/https://doi.org/10.7910/DVN/QQHCIK)
* [https://doi.org/10\.7910/DVN/QQHCIK](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_PNV_PNV_FAPAR_PROBA-V_D_v01)









