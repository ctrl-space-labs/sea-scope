



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

DMSP OLS: Global Radiance\-Calibrated Nighttime Lights Version 4, Defense Meteorological Program Operational Linescan System


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================================================================================================








Dataset Availability
1996\-03\-16T00:00:00Z–2011\-07\-31T00:00:00Z
Dataset Provider


[Earth Observation Group, Payne Institute for Public Policy, Colorado School of Mines](https://eogdata.mines.edu/dmsp/download_radcal.html)



Earth Engine Snippet


`ee.ImageCollection("NOAA/DMSP-OLS/CALIBRATED_LIGHTS_V4")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_DMSP-OLS_CALIBRATED_LIGHTS_V4)





Tags


[dmsp](/earth-engine/datasets/tags/dmsp)
[eog](/earth-engine/datasets/tags/eog)
[imagery](/earth-engine/datasets/tags/imagery)
[lights](/earth-engine/datasets/tags/lights)
[nighttime](/earth-engine/datasets/tags/nighttime)
[ols](/earth-engine/datasets/tags/ols)
[population](/earth-engine/datasets/tags/population)
[radiance](/earth-engine/datasets/tags/radiance)
[visible](/earth-engine/datasets/tags/visible)
[yearly](/earth-engine/datasets/tags/yearly)
calibrated








#### Description



The Defense Meteorological Program (DMSP) Operational Line\-Scan System
(OLS) has a unique capability to detect visible and near\-infrared (VNIR)
emission sources at night.


This collection contains global nighttime lights images with no sensor
saturation. The sensor is typically operated at a high\-gain setting to
enable the detection of moonlit clouds. However, with six bit quantization
and limited dynamic range, the recorded data are saturated in the bright
cores of urban centers. A limited set of observations at low lunar
illumination were obtained where the gain of the detector was set
significantly lower than its typical operational setting (sometimes by a
factor of 100\). Sparse data acquired at low\-gain settings were combined
with the operational data acquired at high\-gain settings to produce the set
of global nighttime lights images with no sensor saturation. Data from
different satellites were merged and blended into the final product in order
to gain maximum coverage. For more information, see this
[readme](https://eogdata.mines.edu/dmsp/radcal_readme.txt)
file from the provider.


Image and data processing by NOAA's National Geophysical Data Center.
DMSP data collected by US Air Force Weather Agency.





### Bands



**Pixel Size**
  
927\.67 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `avg_vis` | 0\* | 6060\.6\* | Average digital band numbers from observations with cloud\-free light detection. |
| `cf_cvg` | 0\* | 175\* | Cloud\-free coverages, the total number of observations that went into each 30\-arc second grid cell. This image can be used to identify areas with low numbers of observations where the quality is reduced. |


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
vardataset=ee.ImageCollection('NOAA/DMSP-OLS/CALIBRATED_LIGHTS_V4')
.filter(ee.Filter.date('2010-01-01','2010-12-31'));
varnighttimeLights=dataset.select('avg_vis');
varnighttimeLightsVis={
min:3.0,
max:60.0,
};
Map.setCenter(7.82,49.1,4);
Map.addLayer(nighttimeLights,nighttimeLightsVis,'Nighttime Lights');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_DMSP-OLS_CALIBRATED_LIGHTS_V4)


[DMSP OLS: Global Radiance\-Calibrated Nighttime Lights Version 4, Defense Meteorological Program Operational Linescan System](/earth-engine/datasets/catalog/NOAA_DMSP-OLS_CALIBRATED_LIGHTS_V4)

The Defense Meteorological Program (DMSP) Operational Line\-Scan System (OLS) has a unique capability to detect visible and near\-infrared (VNIR) emission sources at night. This collection contains global nighttime lights images with no sensor saturation. The sensor is typically operated at a high\-gain setting to enable the detection of moonlit clouds. …

 NOAA/DMSP\-OLS/CALIBRATED\_LIGHTS\_V4,
 dmsp,eog,imagery,lights,nighttime,ols,population,radiance,visible,yearly

1996\-03\-16T00:00:00Z/2011\-07\-31T00:00:00Z



 \-65 \-180 75 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








