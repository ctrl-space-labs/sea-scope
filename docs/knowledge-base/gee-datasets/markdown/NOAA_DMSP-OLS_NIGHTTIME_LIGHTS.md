



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

DMSP OLS: Nighttime Lights Time Series Version 4, Defense Meteorological Program Operational Linescan System


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================================================================================








Dataset Availability
1992\-01\-01T00:00:00Z–2014\-01\-01T00:00:00Z
Dataset Provider


[Earth Observation Group, Payne Institute for Public Policy, Colorado School of Mines](https://eogdata.mines.edu/dmsp/downloadV4composites.html)



Earth Engine Snippet


`ee.ImageCollection("NOAA/DMSP-OLS/NIGHTTIME_LIGHTS")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_DMSP-OLS_NIGHTTIME_LIGHTS)





Tags


[dmsp](/earth-engine/datasets/tags/dmsp)
[eog](/earth-engine/datasets/tags/eog)
[imagery](/earth-engine/datasets/tags/imagery)
[lights](/earth-engine/datasets/tags/lights)
[nighttime](/earth-engine/datasets/tags/nighttime)
[ols](/earth-engine/datasets/tags/ols)
[population](/earth-engine/datasets/tags/population)
[visible](/earth-engine/datasets/tags/visible)
[yearly](/earth-engine/datasets/tags/yearly)








#### Description



The Defense Meteorological Program (DMSP) Operational Line\-Scan System
(OLS) has a unique capability to detect visible and near\-infrared (VNIR)
emission sources at night.


Version 4 of the DMSP\-OLS Nighttime Lights Time Series consists of
cloud\-free composites made using all the available archived DMSP\-OLS smooth
resolution data for calendar years. In cases where two satellites were
collecting data, two composites were produced.


Image and data processing by NOAA's National Geophysical Data Center.
DMSP data collected by US Air Force Weather Agency.





### Bands



**Pixel Size**
  
927\.67 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `avg_vis` | 0\* | 63\* | The average of the visible band digital number values with no further filtering. |
| `stable_lights` | 0\* | 63\* | The cleaned up avg\_vis contains the lights from cities, towns, and other sites with persistent lighting, including gas flares. Ephemeral events, such as fires, have been discarded. The background noise was identified and replaced with values of zero. |
| `cf_cvg` | 0\* | 126\* | Cloud\-free coverages tally the total number of observations that went into each 30\-arc second grid cell. This band can be used to identify areas with low numbers of observations where the quality is reduced. |
| `avg_lights_x_pct` | 0\* | 63\* | The average visible band digital number (DN) of cloud\-free light detections multiplied by the percent frequency of light detection. The inclusion of the percent frequency of detection term normalizes the resulting digital values for variations in the persistence of lighting. For instance, the value for a light only detected half the time is discounted by 50%. Note that this product contains detections from fires and a variable amount of background noise. |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


NOAA data, information, and products, regardless of the method of delivery,
are not subject to copyright and carry no restrictions on their subsequent
use by the public. Once obtained, they may be put to any lawful use. The
forgoing data is in the public domain and is being provided without
restriction on use and distribution.




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/DMSP-OLS/NIGHTTIME_LIGHTS')
.filter(ee.Filter.date('2010-01-01','2010-12-31'));
varnighttimeLights=dataset.select('avg_vis');
varnighttimeLightsVis={
min:3.0,
max:60.0,
};
Map.setCenter(7.82,49.1,4);
Map.addLayer(nighttimeLights,nighttimeLightsVis,'Nighttime Lights');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_DMSP-OLS_NIGHTTIME_LIGHTS)


[DMSP OLS: Nighttime Lights Time Series Version 4, Defense Meteorological Program Operational Linescan System](/earth-engine/datasets/catalog/NOAA_DMSP-OLS_NIGHTTIME_LIGHTS)

The Defense Meteorological Program (DMSP) Operational Line\-Scan System (OLS) has a unique capability to detect visible and near\-infrared (VNIR) emission sources at night. Version 4 of the DMSP\-OLS Nighttime Lights Time Series consists of cloud\-free composites made using all the available archived DMSP\-OLS smooth resolution data for calendar years. In …

 NOAA/DMSP\-OLS/NIGHTTIME\_LIGHTS,
 dmsp,eog,imagery,lights,nighttime,ols,population,visible,yearly

1992\-01\-01T00:00:00Z/2014\-01\-01T00:00:00Z



 \-65 \-180 75 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








