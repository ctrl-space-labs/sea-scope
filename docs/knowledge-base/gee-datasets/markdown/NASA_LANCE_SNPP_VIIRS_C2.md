



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP14IMGTDL\_NRT Daily Raster: VIIRS (S\-NPP) Band 375m Active Fire


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================================








Dataset Availability
2023\-09\-03T00:00:00Z–2025\-07\-18T00:00:00Z
Dataset Provider


[NASA / LANCE / SNPP\_VIIRS](https://www.earthdata.nasa.gov/learn/find-data/near-real-time/firms/vnp14imgtdlnrt)



Earth Engine Snippet


`ee.ImageCollection("NASA/LANCE/SNPP_VIIRS/C2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_LANCE_SNPP_VIIRS_C2)





Cadence
1 Day
Tags


[eosdis](/earth-engine/datasets/tags/eosdis)
[fire](/earth-engine/datasets/tags/fire)
[firms](/earth-engine/datasets/tags/firms)
[geophysical](/earth-engine/datasets/tags/geophysical)
[hotspot](/earth-engine/datasets/tags/hotspot)
[lance](/earth-engine/datasets/tags/lance)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[thermal](/earth-engine/datasets/tags/thermal)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



Suomi NPP Visible Infrared Imaging Radiometer Suite (VIIRS) Active Fire detection
product is based on the instrument's 375m nominal resolution data. Compared
to other coarser resolution (≥ 1km) satellite fire detection products, 
the improved 375 m data provide greater response over fires of relatively
small areas, as well as improved mapping of large fire perimeters.
Consequently, the data are well suited for use in support of fire management
(e.g., near real\-time alert systems), as well as other science applications
requiring improved fire mapping fidelity.


The data in the near\-real\-time dataset are not considered to be of science
quality.


Additional information can be found [here](https://earthdata.nasa.gov/earth-observation-data/near-real-time/firms).





### Bands



**Pixel Size**
  
375 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `Bright_ti4` | K | 250\* | 400\* | VIIRS I\-4 channel brightness temperature of the fire pixel. |
| `Bright_ti5` | K | 250\* | 400\* | VIIRS I\-5 Channel brightness temperature of the fire pixel. |
| `confidence` | None | 0 | 2 | A detection confidence intended to help users gauge the quality of individual active fire pixels. The confidence estimate ranges between 'low': 0, 'nominal': 1 and 'high': 2 for all fire pixels within the fire mask. Low confidence daytime fire pixels are typically associated with areas of Sun glint and lower relative temperature anomaly (\<15 K) in the mid\-infrared channel I4\. Nominal confidence pixels are those free of potential Sun glint contamination during the day and marked by strong (\>15 K) temperature anomaly in either day or nighttime data. High confidence fire pixels are associated with day or nighttime saturated pixels. Please note: Low confidence nighttime pixels occur only over the geographic area extending from 11° E to 110° W and 7° N to 55° S. This area describes the region of influence of the South Atlantic Magnetic Anomaly which can cause spurious brightness temperatures in the mid\-infrared channel I4 leading to potential false positive alarms. These have been removed from the NRT data distributed by FIRMS. |
| `line_number` | None | 1\* | 110000\* | Line number in the FIRMS CSV file that the pixel came from. |
| `frp` | MW | FRP depicts the pixel\-integrated fire radiative power in megawatts (MW). Given the unique spatial and spectral resolution of the data, the VIIRS 375m fire detection algorithm was customized and tuned to optimize its response over small fires while balancing the occurrence of false alarms . Frequent saturation of the mid\-infrared I4 channel (3\.55\-3\.93 μm) driving the detection of active fires requires additional tests and procedures to avoid pixel classification errors. As a result, sub\-pixel fire characterization (e.g., fire radiative power \[FRP] retrieval) is only viable across small and/or low\-intensity fires. Systematic FRP retrievals are based on a hybrid approach combining 375 and 750m data. |
| `acq_epoch` | seconds | Acquisation timestamp in seconds |
| `acq_time` | seconds | The time of day in seconds since midnight |
| `DayNight` | None | 1\= Daytime fire, 0\= Nighttime fire |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


NASA promotes the full and open sharing of all data with the research and
applications communities, private industry, academia, and the general
public. Read the [NASA Data and Information Policy](https://www.earthdata.nasa.gov/learn/use-data/data-use-policy).


If you provide the
[Land, Atmosphere Near real\-time Capability for EOS (LANCE) / Fire Information for Resource Management System (FIRMS)](https://earthdata.nasa.gov/earth-observation-data/near-real-time)
data to a third party, follow the guidelines in the
[LANCE Citation, Acknowledgements, and Disclaimer](https://earthdata.nasa.gov/earth-observation-data/near-real-time/citation#ed-lance-disclaimer)
site and replicate or provide a link to the
[disclaimer](https://earthdata.nasa.gov/earth-observation-data/near-real-time/citation#ed-lance-disclaimer).




### Citations



Citations:
* NRT VIIRS 375 m Active Fire product VNP14IMGT distributed from NASA FIRMS.
Available on\-line https://earthdata.nasa.gov/firms.
[doi:10\.5067/FIRMS/VIIRS/VNP14IMGT\_NRT.002](https://doi.org/10.5067/FIRMS/VIIRS/VNP14IMGT_NRT.002)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varsuomi_viirs=ee.ImageCollection('NASA/LANCE/SNPP_VIIRS/C2')
.filter(ee.Filter.date('2023-10-08','2023-10-30'))
varband_vis={
min:[
280.0,
],
max:[
400.0,
],
palette:['yellow','orange','red','white','darkred'],
bands:[
'Bright_ti4',
],
}
Map.setCenter(-113.2487,59.3943,8);
Map.addLayer(suomi_viirs,band_vis,'Suomi nrt firms')
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_LANCE_SNPP_VIIRS_C2)


[VNP14IMGTDL\_NRT Daily Raster: VIIRS (S\-NPP) Band 375m Active Fire](/earth-engine/datasets/catalog/NASA_LANCE_SNPP_VIIRS_C2)

Suomi NPP Visible Infrared Imaging Radiometer Suite (VIIRS) Active Fire detection product is based on the instrument's 375m nominal resolution data. Compared to other coarser resolution (≥ 1km) satellite fire detection products, the improved 375 m data provide greater response over fires of relatively small areas, as well as improved …

 NASA/LANCE/SNPP\_VIIRS/C2,
 eosdis,fire,firms,geophysical,hotspot,lance,modis,nasa,thermal,viirs

2023\-09\-03T00:00:00Z/2025\-07\-18T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








