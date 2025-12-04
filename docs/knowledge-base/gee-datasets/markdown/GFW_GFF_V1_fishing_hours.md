



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GFW (Global Fishing Watch) Daily Fishing Hours


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================








Dataset Availability
2012\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[Global Fishing Watch](https://globalfishingwatch.org/)



Earth Engine Snippet


`ee.ImageCollection("GFW/GFF/V1/fishing_hours")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GFW/GFW_GFF_V1_fishing_hours)





Cadence
1 Day
Tags


[fishing](/earth-engine/datasets/tags/fishing)
[gfw](/earth-engine/datasets/tags/gfw)
[marine](/earth-engine/datasets/tags/marine)
[monthly](/earth-engine/datasets/tags/monthly)
[ocean](/earth-engine/datasets/tags/ocean)
[oceans](/earth-engine/datasets/tags/oceans)








#### Description



Fishing effort, measured in hours of inferred fishing activity. Each asset
is the effort for a given flag state and day, with one band for the
fishing activity of each gear type.


See [sample Earth Engine
scripts](https://globalfishingwatch.org/research/global-footprint-of-fisheries/).
Also see [the main GFW site](https://GlobalFishingWatch.org) for program
information, fully interactive visualization maps, and impacts.





### Bands



**Pixel Size**
  
1113\.2 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `drifting_longlines` | h/km^2 | Hours per sq. km of fishing with drifting longlines. |
| `fixed_gear` | h/km^2 | Hours per sq. km of fishing with fixed gear. |
| `other_fishing` | h/km^2 | Hours per sq. km of fishing with other gear types. |
| `purse_seines` | h/km^2 | Hours per sq. km of fishing with purse seines. |
| `squid_jigger` | h/km^2 | Hours per sq. km of fishing with squid jiggers. |
| `trawlers` | h/km^2 | Hours per sq. km of fishing with trawlers. |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| country | STRING | ISO3 country code of the vessel flag state. For all countries, use "WLD". |




### Terms of Use


**Terms of Use**


This work is licensed under a Creative Commons Attribution\-ShareAlike 4\.0
International license. (CC\-BY\-SA)




### Citations



Citations:
* Global Fishing Watch, "Tracking the Global Footprint of Fisheries." Science 361\.6378 (2018\).





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('GFW/GFF/V1/fishing_hours')
.filter(ee.Filter.date('2016-12-01','2017-01-01'));
vartrawlers=dataset.select('trawlers');
vartrawlersVis={
min:0.0,
max:5.0,
};
Map.setCenter(16.201,36.316,7);
Map.addLayer(trawlers.max(),trawlersVis,'Trawlers');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GFW/GFW_GFF_V1_fishing_hours)


[GFW (Global Fishing Watch) Daily Fishing Hours](/earth-engine/datasets/catalog/GFW_GFF_V1_fishing_hours)

Fishing effort, measured in hours of inferred fishing activity. Each asset is the effort for a given flag state and day, with one band for the fishing activity of each gear type. See sample Earth Engine scripts. Also see the main GFW site for program information, fully interactive visualization maps, …

 GFW/GFF/V1/fishing\_hours,
 fishing,gfw,marine,monthly,ocean,oceans

2012\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








