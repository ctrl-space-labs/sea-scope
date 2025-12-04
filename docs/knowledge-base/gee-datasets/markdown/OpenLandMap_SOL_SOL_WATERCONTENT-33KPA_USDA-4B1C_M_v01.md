



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap Soil Water Content at 33kPa (Field Capacity)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.2629589)



Earth Engine Snippet


`ee.Image("OpenLandMap/SOL/SOL_WATERCONTENT-33KPA_USDA-4B1C_M/v01")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_WATERCONTENT-33KPA_USDA-4B1C_M_v01)





Tags


[envirometrix](/earth-engine/datasets/tags/envirometrix)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[soil](/earth-engine/datasets/tags/soil)
watercontent








#### Description



Soil water content (volumetric %) for 33kPa and 1500kPa suctions
predicted at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution


Training points are based on a global compilation of soil profiles:


* [USDA NCSS](https://ncsslabdatamart.sc.egov.usda.gov/)
* [AfSPDB](https://www.isric.org/projects/africa-soil-profiles-database-afsp)
* [ISRIC WISE](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/a351682c-330a-4995-a5a1-57ad160e621c)
* [EGRPR](http://egrpr.esoil.ru/)
* [SPADE](https://esdac.jrc.ec.europa.eu/content/soil-profile-analytical-database-2)
* [CanNPDB](https://open.canada.ca/data/en/dataset/6457fad6-b6f5-47a3-9bd1-ad14aea4b9e0)
* [UNSODA](https://data.nal.usda.gov/dataset/unsoda-20-unsaturated-soil-hydraulic-database-database-and-program-indirect-methods-estimating-unsaturated-hydraulic-properties)
* [SWIG](https://doi.pangaea.de/10.1594/PANGAEA.885492)
* [HYBRAS](https://www.cprm.gov.br/en/Hydrology/Research-and-Innovation/HYBRAS-4208.html)
* [HydroS](https://doi.org/10.4228/ZALF.2003.273)


Data import steps are available [here](https://gitlab.com/openlandmap/compiled-ess-point-data-sets).
Spatial prediction steps are described in detail [here](https://gitlab.com/openlandmap/global-layers/tree/master/soil/soil_water).
Note: these are actually measured and mapped soil content values; no Pedo\-Transfer\-Functions
have been used (except to fill in the missing NCSS bulk densities). Available
water capacity in mm (derived as a difference between field capacity and wilting
point multiplied by layer thickness) per layer is available [here](https://doi.org/10.5281/zenodo.2629148).
Antarctica is not included.


To access and visualize maps outside of Earth Engine, use [this page](https://opengeohub.org/about-openlandmap).


If you discover a bug, artifact or inconsistency in the LandGIS maps
or if you have a question please use the following channels:


* [Technical issues and questions about the code](https://gitlab.com/openlandmap/global-layers/issues)
* [General questions and comments](https://disqus.com/home/forums/landgis/)





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `b0` | % | 0\* | 52\.974\* | Soil water content at 33kPa (field capacity) at 0 cm depth |
| `b10` | % | 0\* | 52\.974\* | Soil water content at 33kPa (field capacity) at 10 cm depth |
| `b30` | % | 0\* | 52\.974\* | Soil water content at 33kPa (field capacity) at 30 cm depth |
| `b60` | % | 0\* | 52\.974\* | Soil water content at 33kPa (field capacity) at 60 cm depth |
| `b100` | % | 0\* | 52\.974\* | Soil water content at 33kPa (field capacity) at 100 cm depth |
| `b200` | % | 0\* | 52\.974\* | Soil water content at 33kPa (field capacity) at 200 cm depth |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Tomislav Hengl, \& Surya Gupta. (2019\). Soil water content (volumetric %) for 33kPa and 1500kPa suctions predicted at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution (Version v01\) \[Data set]. Zenodo.
[10\.5281/zenodo.2629589](https://doi.org/10.5281/zenodo.2629589)





### DOIs


* [https://doi.org/10\.5281/zenodo.2629589](https://doi.org/10.5281/zenodo.2629589)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/SOL/SOL_WATERCONTENT-33KPA_USDA-4B1C_M/v01');

varvisualization={
bands:['b0'],
min:0.0,
max:52.9740182135385,
palette:[
'd29642','eec764','b4ee87','32eeeb','0c78ee','2601b7',
'083371',
]
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'Soil water content at 33kPa (field capacity)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_WATERCONTENT-33KPA_USDA-4B1C_M_v01)


[OpenLandMap Soil Water Content at 33kPa (Field Capacity)](/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_WATERCONTENT-33KPA_USDA-4B1C_M_v01)

Soil water content (volumetric %) for 33kPa and 1500kPa suctions predicted at 6 standard depths (0, 10, 30, 60, 100 and 200 cm) at 250 m resolution Training points are based on a global compilation of soil profiles: USDA NCSS AfSPDB ISRIC WISE EGRPR SPADE CanNPDB UNSODA SWIG HYBRAS HydroS …

 OpenLandMap/SOL/SOL\_WATERCONTENT\-33KPA\_USDA\-4B1C\_M/v01,
 envirometrix,opengeohub,openlandmap,soil

1950\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.2629589](https://doi.org/https://doi.org/10.5281/zenodo.2629589)
* [https://doi.org/10\.5281/zenodo.2629589](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_WATERCONTENT-33KPA_USDA-4B1C_M_v01)









