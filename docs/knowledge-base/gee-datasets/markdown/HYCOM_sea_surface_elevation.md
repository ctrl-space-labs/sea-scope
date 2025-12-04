



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

HYCOM: Hybrid Coordinate Ocean Model, Sea Surface Elevation


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================================








Dataset Availability
1992\-10\-02T00:00:00Z–2024\-09\-05T09:00:00Z
Dataset Provider


[NOPP](https://hycom.org/)



Earth Engine Snippet


`ee.ImageCollection("HYCOM/sea_surface_elevation")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/HYCOM/HYCOM_sea_surface_elevation)





Cadence
1 Day
Tags


[elevation](/earth-engine/datasets/tags/elevation)
[hycom](/earth-engine/datasets/tags/hycom)
[nopp](/earth-engine/datasets/tags/nopp)
[ocean](/earth-engine/datasets/tags/ocean)
[oceans](/earth-engine/datasets/tags/oceans)
[water](/earth-engine/datasets/tags/water)
ssh








#### Description



The Hybrid Coordinate Ocean Model (HYCOM) is a data\-assimilative hybrid
isopycnal\-sigma\-pressure (generalized) coordinate ocean model. The subset
of HYCOM data hosted in EE contains the variables salinity, temperature,
velocity, and elevation. They have been interpolated to a uniform
0\.08 degree lat/long grid between 80\.48°S and 80\.48°N. The salinity,
temperature, and velocity variables have been interpolated to 40
standard z\-levels.


The HYCOM Consortium, which includes the National Ocean Partnership
Program (NOPP), is part of the U.S. Global Ocean Data Assimilation
Experiment (GODAE).


Funded by the National Ocean Partnership Program, the Office of Naval
Research (ONR), and DoD High Performance Computing Modernization Program.


For more information, see:


* [hycom.org](https://www.hycom.org/)
* [GIS StackExchange hycom](https://gis.stackexchange.com/questions/tagged/hycom)
* Wikipedia [HyCOM](https://en.wikipedia.org/wiki/HyCOM)
* Wikipedia [List of ocean circulation models](https://en.wikipedia.org/wiki/List_of_ocean_circulation_models)
* Wikipedia [Ocean general circulation model (OGCM)](https://en.wikipedia.org/wiki/Ocean_general_circulation_model)





### Bands



**Pixel Size**
  
8905\.6 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `surface_elevation` | m | \-5681\* | 5965\* | 0\.001 | Sea surface elevation anomaly relative to the modeled elevation mean |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| experiment | STRING | Experiment number |




### Terms of Use


**Terms of Use**


This dataset is freely available with no restrictions.




### Citations



Citations:
* J. A. Cummings and O. M. Smedstad. 2013: Variational Data Assimilation for
the Global Ocean. Data Assimilation for Atmospheric, Oceanic and Hydrologic
Applications vol II, chapter 13, 303\-343\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('HYCOM/sea_surface_elevation')
.filter(ee.Filter.date('2018-08-01','2018-08-15'));
varsurfaceElevation=dataset.select('surface_elevation');
varsurfaceElevationVis={
min:-2000.0,
max:2000.0,
palette:['blue','cyan','yellow','red'],
};
Map.setCenter(-28.1,28.3,1);
Map.addLayer(surfaceElevation,surfaceElevationVis,'Surface Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/HYCOM/HYCOM_sea_surface_elevation)


[HYCOM: Hybrid Coordinate Ocean Model, Sea Surface Elevation](/earth-engine/datasets/catalog/HYCOM_sea_surface_elevation)

The Hybrid Coordinate Ocean Model (HYCOM) is a data\-assimilative hybrid isopycnal\-sigma\-pressure (generalized) coordinate ocean model. The subset of HYCOM data hosted in EE contains the variables salinity, temperature, velocity, and elevation. They have been interpolated to a uniform 0\.08 degree lat/long grid between 80\.48°S and 80\.48°N. The salinity, temperature, and …

 HYCOM/sea\_surface\_elevation,
 elevation,hycom,nopp,ocean,oceans,water

1992\-10\-02T00:00:00Z/2024\-09\-05T09:00:00Z



 \-80\.48 \-180 80\.48 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








