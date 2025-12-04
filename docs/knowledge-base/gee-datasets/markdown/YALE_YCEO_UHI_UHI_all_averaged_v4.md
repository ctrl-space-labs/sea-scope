



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

YCEO Surface Urban Heat Islands: Spatially\-Averaged Daytime and Nighttime Intensity for Annual, Summer, and Winter


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================================================================================








Dataset Availability
2003\-01\-01T00:00:00Z–2018\-12\-31T00:00:00Z
Dataset Provider


[Yale Center for Earth Observation (YCEO)](https://yceo.yale.edu/research/global-surface-uhi-explorer)



Earth Engine Snippet


`ee.Image("YALE/YCEO/UHI/UHI_all_averaged/v4")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/YALE/YALE_YCEO_UHI_UHI_all_averaged_v4)





Tags


[climate](/earth-engine/datasets/tags/climate)
[uhi](/earth-engine/datasets/tags/uhi)
[urban](/earth-engine/datasets/tags/urban)
[yale](/earth-engine/datasets/tags/yale)








#### Description



This dataset contains annual, summertime, and wintertime surface urban
heat island (SUHI) intensities for day and night for over 10,000 urban clusters
throughout the world. The dataset was created using the MODIS 8\-day TERRA and
AQUA land surface temperature (LST) products, the Landscan urban extent
database, the Global Multi\-resolution Terrain Elevation Data 2010, and the
European Space Agency (ESA) Climate Change Initiative (CCI) land cover data
using the Simplified Urban\-Extent Algorithm. The product is available both at
the pixel level (at 300 m resolution after downscaling) and as urban cluster
means from 2003 to 2018\. The monthly composites are only available as urban
cluster means.


A summary of older versions,
including changes from the dataset created and analyzed in the originally
published manuscript can be found on the
[Yale Center for Earth Observation website](https://yceo.yale.edu/research/global-surface-uhi-explorer).
The dataset can also be explored using the [Global Surface UHI
Explorer web application](https://yceo.users.earthengine.app/view/uhimap).


The dataset is split into the following six components:


1. **UHI\_all\_averaged:** Image containing cluster\-mean
composite daytime and nighttime SUHI intensity for annual, summer,
and winter.
2. **UHI\_monthly\_averaged:** Image containing cluster\-mean
monthly composites of daytime and nighttime SUHI intensity.
3. **UHI\_yearly\_averaged:** Image collection of cluster\-mean
yearly composites of daytime and nighttime SUHI intensity from 2003\.
to 2018\.
4. **UHI\_yearly\_pixel:** Image collection of spatially
disaggregated (nominal scale of 300 m) annual daytime and nighttime
SUHI intensity from 2003 to 2018\.
5. **Summer\_UHI\_yearly\_pixel:** Image collection of spatially
disaggregated (nominal scale of 300 m) summertime daytime and
nighttime SUHI intensity from 2003 to 2018\.
6. **Winter\_UHI\_yearly\_pixel:** Image collection of spatially
disaggregated (nominal scale of 300 m) wintertime daytime and
nighttime SUHI intensity from 2003 to 2018\.


This asset is the first component.





### Bands



**Pixel Size**
  
300 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `all_daytime_UHI` | °C | All Daytime UHI |
| `all_nighttime_UHI` | °C | All Nighttime UHI |
| `summer_daytime_UHI` | °C | summer Daytime UHI |
| `summer_nighttime_UHI` | °C | Summer Nighttime UHI |
| `winter_daytime_UHI` | °C | Winter Daytime UHI |
| `winter_nighttime_UHI` | °C | Winter Nighttime UHI |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Chakraborty, T., \& Lee, X. (2019\). A simplified urban\-extent algorithm
to characterize surface urban heat islands on a global scale and examine
vegetation control on their spatiotemporal variability. International
Journal of Applied Earth Observation and Geoinformation, 74, 269\-280\.
[doi:10\.1016/j.jag.2018\.09\.015](https://doi.org/10.1016/j.jag.2018.09.015)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('YALE/YCEO/UHI/UHI_all_averaged/v4');

varvisualization={
bands:['all_daytime_UHI'],
min:-1.5,
max:7.5,
palette:[
'313695','74add1','fed976','feb24c','fd8d3c','fc4e2a','e31a1c',
'b10026']
};

Map.setCenter(-74.7,40.6,7);

Map.addLayer(dataset,visualization,'All Daytime UHI');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/YALE/YALE_YCEO_UHI_UHI_all_averaged_v4)


[YCEO Surface Urban Heat Islands: Spatially\-Averaged Daytime and Nighttime Intensity for Annual, Summer, and Winter](/earth-engine/datasets/catalog/YALE_YCEO_UHI_UHI_all_averaged_v4)

This dataset contains annual, summertime, and wintertime surface urban heat island (SUHI) intensities for day and night for over 10,000 urban clusters throughout the world. The dataset was created using the MODIS 8\-day TERRA and AQUA land surface temperature (LST) products, the Landscan urban extent database, the Global Multi\-resolution Terrain …

 YALE/YCEO/UHI/UHI\_all\_averaged/v4,
 climate,uhi,urban,yale

2003\-01\-01T00:00:00Z/2018\-12\-31T00:00:00Z



 \-49\.98 \-180 69\.7 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








