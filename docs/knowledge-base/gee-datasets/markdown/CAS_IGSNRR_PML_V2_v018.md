



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

PML\_V2 0\.1\.8: Coupled Evapotranspiration and Gross Primary Product (GPP)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================================================








Dataset Availability
2000\-02\-26T00:00:00Z–2023\-12\-27T00:00:00Z
Dataset Provider


[PML\_V2](https://github.com/kongdd/PML)



Earth Engine Snippet


`ee.ImageCollection("CAS/IGSNRR/PML/V2_v018")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CAS/CAS_IGSNRR_PML_V2_v018)





Cadence
8 Days
Tags


[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[gpp](/earth-engine/datasets/tags/gpp)
[plant\-productivity](/earth-engine/datasets/tags/plant-productivity)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)








#### Description



Penman\-Monteith\-Leuning Evapotranspiration V2 (PML\_V2\) products include
evapotranspiration (ET), its three components, and
gross primary production (GPP) at 500m and 8\-day resolution during 2000\-2023
and with spatial range from \-60°S to 90°N. The major advantages of the
PML\_V2 products are:


1. Coupled estimates of transpiration and GPP via canopy
conductance (Gan et al., 2018; Zhang et al., 2019\)
2. Partitioning ET into three components: transpiration from vegetation,
direct evaporation from the soil, and vaporization of intercepted
rainfall from vegetation (Zhang et al., 2016\).


The PML\_V2 products perform well against observations
at 95 flux sites across the globe, and are similar to or noticeably better than
major state\-of\-the\-art ET and GPP products widely used by water and ecology
research communities (Zhang et al., 2019\).


Key changes in v0\.1\.8 compared with the original v0\.1\.4:


1. Temporal coverage is lengthened to the latest (may update annually) with the MODIS C6\.1 data.
2. MODIS Terra LAI (MOD15A2H) is used rather than the composite LAI (MCD15A3H).
3. Parameters are recalibrated with the change in LAI, while other forcings remain the same.





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `GPP` | gC m\-2 d\-1 | 0\* | 39\.01\* | Gross primary production |
| `Ec` | mm/d | 0\* | 15\.33\* | Vegetation transpiration |
| `Es` | mm/d | 0\* | 8\.2\* | Soil evaporation |
| `Ei` | mm/d | 0\* | 12\.56\* | Interception from vegetation canopy |
| `ET_water` | mm/d | 0\* | 20\.11\* | Evaporation from water bodies, snow, and ice. Calculated using the Penman equation, which is considered a good estimate of actual evaporation for these surfaces. |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


Acknowledgements


Whenever PML datasets are used in a scientific publication, the given
references should be cited.


License


The dataset is licensed under the
[CC\-BY 4\.0 license](https://creativecommons.org/licenses/by/4.0/).




### Citations



Citations:
* Zhang, Y., Kong, D., Gan, R., Chiew, F.H.S., McVicar, T.R., Zhang, Q.,
and Yang, Y., 2019\. Coupled estimation of 500m and 8\-day resolution global
evapotranspiration and gross primary production in 2002\-2017\.
Remote Sens. Environ. 222, 165\-182,
[doi:10\.1016/j.rse.2018\.12\.031](https://doi.org/10.1016/j.rse.2018.12.031)
* Gan, R., Zhang, Y.Q., Shi, H., Yang, Y.T., Eamus, D., Cheng, L.,
Chiew, F.H.S., Yu, Q., 2018\. Use of satellite leaf area index estimating
evapotranspiration and gross assimilation for Australian ecosystems.
Ecohydrology, [doi:10\.1002/eco.1974](https://doi.org/10.1002/eco.1974)
* Zhang, Y., Peña\-Arancibia, J.L., McVicar, T.R., Chiew, F.H.S., Vaze, J.,
Liu, C., Lu, X., Zheng, H., Wang, Y., Liu, Y.Y., Miralles, D.G., Pan,
M., 2016\. Multi\-decadal trends in global terrestrial evapotranspiration
and its components. Sci. Rep. 6, 19124\.
[doi:10\.1038/srep19124](https://doi.org/10.1038/srep19124)





### DOIs


* [https://doi.org/10\.1002/eco.1974](https://doi.org/10.1002/eco.1974)
* [https://doi.org/10\.1038/srep19124](https://doi.org/10.1038/srep19124)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('CAS/IGSNRR/PML/V2_v018');

varvisualization={
bands:['GPP'],
min:0.0,
max:9.0,
palette:[
'a50026','d73027','f46d43','fdae61','fee08b','ffffbf',
'd9ef8b','a6d96a','66bd63','1a9850','006837',
]
};

Map.setCenter(0.0,15.0,2);

Map.addLayer(
dataset.first(),visualization,'PML_V2 0.1.8 Gross Primary Product (GPP)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CAS/CAS_IGSNRR_PML_V2_v018)


[PML\_V2 0\.1\.8: Coupled Evapotranspiration and Gross Primary Product (GPP)](/earth-engine/datasets/catalog/CAS_IGSNRR_PML_V2_v018)

Penman\-Monteith\-Leuning Evapotranspiration V2 (PML\_V2\) products include evapotranspiration (ET), its three components, and gross primary production (GPP) at 500m and 8\-day resolution during 2000\-2023 and with spatial range from \-60°S to 90°N. The major advantages of the PML\_V2 products are: Coupled estimates of transpiration and GPP via canopy conductance (Gan et …

 CAS/IGSNRR/PML/V2\_v018,
 evapotranspiration,gpp,plant\-productivity,water\-vapor

2000\-02\-26T00:00:00Z/2023\-12\-27T00:00:00Z



 \-60 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1038/srep19124](https://doi.org/https://github.com/kongdd/PML)
* [https://doi.org/10\.1038/srep19124](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/CAS_IGSNRR_PML_V2_v018)









