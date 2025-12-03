



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NCEP/NCAR Reanalysis Data, Water Vapor


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================








Dataset Availability
1948\-01\-01T00:00:00Z–2025\-07\-13T18:00:00Z
Dataset Provider


[NCEP](https://www.esrl.noaa.gov/psd/data/gridded/data.ncep.reanalysis.html)



Earth Engine Snippet


`ee.ImageCollection("NCEP_RE/surface_wv")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NCEP_RE/NCEP_RE_surface_wv)





Cadence
6 Hours
Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[ncep](/earth-engine/datasets/tags/ncep)
[noaa](/earth-engine/datasets/tags/noaa)
[reanalysis](/earth-engine/datasets/tags/reanalysis)
[vapor](/earth-engine/datasets/tags/vapor)
precipitable








#### Description



The NCEP/NCAR Reanalysis Project is a joint project between the National
Centers for Environmental Prediction (NCEP, formerly "NMC") and the
National Center for Atmospheric Research (NCAR). The goal of this joint
effort is to produce new atmospheric analyses using historical data as
well as to produce analyses of the current atmospheric state (Climate Data
Assimilation System, CDAS). The NCEP/NCAR Reanalysis 1 project is using a
state\-of\-the\-art analysis/forecast system to perform data assimilation using
past data from 1948 to the present. The data have 6\-hour temporal
resolution (0000, 0600, 1200, and 1800 UTC) and 2\.5 degree spatial
resolution.





### Bands



**Pixel Size**
  
278300 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `pr_wtr` | kg/m^2 | \-8\.2\* | 89\.8\* | Total column water vapor |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


There are no restrictions on the use of these datasets.




### Citations



Citations:
* Kalnay et al., 1996, The NCEP/NCAR 40\-Year Reanalysis Project. Bull. Amer.
Meteor. Soc., 77, 437\-471\.
[doi:10\.1175/1520\-0477(1996\)077](https://doi.org/10.1175/1520-0477(1996)077%3C0437:TNYRP%3E2.0.CO;2)[0437:TNYRP\\](/earth-engine/datasets/catalog/0437:TNYRP%5C)2\.0\.CO;2\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NCEP_RE/surface_wv')
.filter(ee.Filter.date('2018-08-01','2018-08-15'));
vartotalColumnWaterVapor=dataset.select('pr_wtr');
vartotalColumnWaterVaporVis={
min:0.0,
max:60.0,
palette:['0000ff','00ffff','008000','ffff00','ff0000'],
};
Map.setCenter(-158.2,2.81,2);
Map.addLayer(
totalColumnWaterVapor,totalColumnWaterVaporVis,
'Total Column Water Vapor');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NCEP_RE/NCEP_RE_surface_wv)


[NCEP/NCAR Reanalysis Data, Water Vapor](/earth-engine/datasets/catalog/NCEP_RE_surface_wv)

The NCEP/NCAR Reanalysis Project is a joint project between the National Centers for Environmental Prediction (NCEP, formerly "NMC") and the National Center for Atmospheric Research (NCAR). The goal of this joint effort is to produce new atmospheric analyses using historical data as well as to produce analyses of the current …

 NCEP\_RE/surface\_wv,
 atmosphere,climate,geophysical,ncep,noaa,reanalysis,vapor

1948\-01\-01T00:00:00Z/2025\-07\-13T18:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








