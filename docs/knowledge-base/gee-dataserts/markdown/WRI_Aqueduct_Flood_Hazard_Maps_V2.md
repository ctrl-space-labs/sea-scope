



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WRI Aqueduct Floods Hazard Maps Version 2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2080\-12\-31T23:59:59Z
Dataset Provider


[World Resources Institute](https://www.wri.org/research/aqueduct-floods-methodology)



Earth Engine Snippet


`ee.ImageCollection("WRI/Aqueduct_Flood_Hazard_Maps/V2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_Aqueduct_Flood_Hazard_Maps_V2)





Tags


[flood](/earth-engine/datasets/tags/flood)
[monitoring](/earth-engine/datasets/tags/monitoring)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[wri](/earth-engine/datasets/tags/wri)








#### Description



Aqueduct Floods data measures riverine and coastal food risks under both
current baseline conditions and future projections in 2030, 2050, and 2080\.
In addition to providing hazard maps and assessing risks, Aqueduct Floods
helps to conduct comprehensive cost\-benefit analysis to evaluate the value
of dike flood protection strategies.


Aqueduct Floods aims to empower disaster risk analysts and managers with
quantitative information on food risks and adaptation strategy costs, and to
help inform policy and investment decision\-making.


[This](https://files.wri.org/d8/s3fs-public/aqueduct-floods-methodology.pdf)
technical note explains in detail the framework, methodology, and data used
in developing Aqueduct Floods.





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `inundation_depth` | m | 0\* | 32\.05\* | Flood inundation depth |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| climatescenario | STRING | Climate Scenario types:* historical: Baseline condition/ no climate scenario needed * rcp4p5: Representative Concentration Pathway 4\.5 (steady carbon emissions) * rcp8p5: Representative Concentration Pathway 8\.5 (rising carbon emissions) |
| floodtype | STRING | Type of Flood:* inuncoast: Coastal flood hazard * inunriver: Riverine flood hazard |
| projection | INT | Sea level rise scenario (in percentile)* 5: A low sea level rise scenario * 50: The median sea level rise projection * 95: A high sea level rise scenario |
| returnperiod | INT | Return period is the average time interval expected between hazard events of a given magnitude or greater (in years). The flood hazard maps are generated for return periods of 1, 2, 5, 10, 25, 50, 100, 250, 500, and 1000 years. |
| subsidence | STRING | Applies only for inuncoast flood type* nosub: Subsidence not included in projection * wtsub: Subsidence included in projection |
| model | STRING | Applies only for inunriver flood type, represents type of model used.* 000000000WATCH: Baseline condition * 00000NorESM1\-M: (GCM model) Bjerknes Centre for Climate Research, Norwegian Meteorological Institute * 0000GFDL\_ESM2M: (GCM model) Geophysical Fluid Dynamics Laboratory (NOAA) * 0000HadGEM2\-ES: (GCM model) Met Office Hadley Centre * 00IPSL\-CM5A\-LR: (GCM model) Institut Pierre Simon Laplace |
| year | INT | Flood occurence year |




### Terms of Use


**Terms of Use**


The WRI datasets are available without restriction
on use or distribution. WRI does request that the
user give proper attribution and identify WRI, where applicable,
as the source of the data. For more information check
[WRI's open data commitment](https://www.wri.org/data/open-data-commitment),




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('WRI/Aqueduct_Flood_Hazard_Maps/V2');
varinundationDepth=dataset.select('inundation_depth');
varinundationDepthVis={
min:0,
max:1,
palette:['ffffff','0000ff'],
};
Map.setCenter(-68.36,-6.73,4);
Map.addLayer(inundationDepth,inundationDepthVis,'Aqueduct Flood Hazard Maps');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_Aqueduct_Flood_Hazard_Maps_V2)


[WRI Aqueduct Floods Hazard Maps Version 2](/earth-engine/datasets/catalog/WRI_Aqueduct_Flood_Hazard_Maps_V2)

Aqueduct Floods data measures riverine and coastal food risks under both current baseline conditions and future projections in 2030, 2050, and 2080\. In addition to providing hazard maps and assessing risks, Aqueduct Floods helps to conduct comprehensive cost\-benefit analysis to evaluate the value of dike flood protection strategies. Aqueduct Floods …

 WRI/Aqueduct\_Flood\_Hazard\_Maps/V2,
 flood,monitoring,surface\-ground\-water,wri

2010\-01\-01T00:00:00Z/2080\-12\-31T23:59:59Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








