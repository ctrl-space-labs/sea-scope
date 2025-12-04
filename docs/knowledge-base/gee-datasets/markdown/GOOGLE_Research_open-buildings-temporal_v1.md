



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Open Buildings Temporal V1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================








Dataset Availability
2016\-06\-30T07:00:00Z–2023\-06\-30T07:00:00Z
Dataset Provider


[Google Research \- Open Buildings](https://sites.research.google/gr/open-buildings/temporal/)



Earth Engine Snippet


`ee.ImageCollection("GOOGLE/Research/open-buildings-temporal/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_Research_open-buildings-temporal_v1)





Tags


[africa](/earth-engine/datasets/tags/africa)
[annual](/earth-engine/datasets/tags/annual)
[asia](/earth-engine/datasets/tags/asia)
[built\-up](/earth-engine/datasets/tags/built-up)
[height](/earth-engine/datasets/tags/height)
[open\-buildings](/earth-engine/datasets/tags/open-buildings)
[population](/earth-engine/datasets/tags/population)
[south\-asia](/earth-engine/datasets/tags/south-asia)
[southeast\-asia](/earth-engine/datasets/tags/southeast-asia)
building\-height
high\-resolution








#### Description



The Open Buildings 2\.5D Temporal Dataset contains data about building
presence, fractional building counts, and building heights at an effective1
spatial resolution of 4m (rasters are provided at 0\.5m resolution) at an
annual cadence from 2016\-2023\. It is produced from open\-source,
low\-resolution imagery from the [Sentinel\-2](https://www.esa.int/Applications/Observing_the_Earth/Copernicus/Sentinel-2)
collection.


The dataset is available across Africa, South Asia, South\-East Asia, Latin
America and the Caribbean. The goal of this data is to support organizations
(e.g., governmental, non\-profits, commercial) focusing on a range of
applications for social good.


Explore the data interactively with the demo Earth Engine [app](https://goo.gle/open-buildings-temporal-demo-app). (In case you encounter performance issues with the Earth Engine app please try [this](https://goo.gle/open-buildings-temporal-demo) Earth Engine script instead.)


Alternatively, if you are not an Earth Engine user, you can download the
data directly from Google Cloud Storage using [this notebook](https://colab.research.google.com/github/google-research/google-research/blob/master/building_detection/open_buildings_temporal_download_region_geotiffs.ipynb).


For more details on the project and FAQs about the data checkout the project
[website](https://sites.research.google/gr/open-buildings/temporal/).


Example scripts:


* `[How to compute building count for a given AOI](https://code.earthengine.google.com/31ca8ccee65887ed2a152c8ea920bbd2)`
* `[How to compute built-up area for a given AOI](https://code.earthengine.google.com/46468628f66eb57c79753ae4c1c09f54)`
* `[How to see two years side-by-side and compare](https://code.earthengine.google.com/e9e5a84d279d4b5669872a560e8329a2?hideCode=true)`


1equivalent to what could be achieved by a high\-resolution model
using a single frame of 4 m resolution imagery.





### Bands



**Pixel Size**
  
4 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `building_fractional_count` | None | 0 | 0\.0216 | Source data for deriving building counts for a given AOI. Please see accompanying example scripts. |
| `building_height` | m | 0 | 100 | Building height relative to the terrain in range \[0m, 100m]. |
| `building_presence` | None | 0 | 1 | Model confidence values (i.e. how confident a model is that the pixel is part of a building) in range \[0\.0, 1\.0]. Note that model confidence values are uncalibrated, meaning, if model confidence for a certain pixel is 0\.8, it doesn't mean the actual likelihood of building presence is 80%. As such, confidence values can only be used for relative ranking (eg. thresholding) of pixels. Also, the model confidence can vary across location and time based on a number of factors such as cloud cover, imagery misalignment, etc. |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| imagery\_start\_time\_epoch\_s | DOUBLE | Oldest possible date for source Sentinel\-2 imagery used to produce these rasters. |
| imagery\_end\_time\_epoch\_s | DOUBLE | Newest possible date for source Sentinel\-2 imagery used to produce these rasters. |
| inference\_time\_epoch\_s | DOUBLE | Time the rasters are supposed to predict the state of the world for, in seconds since epoch. |
| s2cell\_token | STRING | Token of the S2 cell this tile belongs to. Due to UTM zone boundaries, a single S2 cell that spans multiple zones may have multiple corresponding tiles in different projection zones. See <http://s2geometry.io/>. |




### Terms of Use


**Terms of Use**


The data is shared under the Creative Commons Attribution
([CC\-BY 4\.0](https://creativecommons.org/licenses/by/4.0/)) license and the
Open Data Commons Open Database License (ODbL) v1\.0 license. As the user,
you can pick which of the two licenses you prefer and use the data under the
terms of that license.


Leverages the Copernicus Sentinel\-2 data (2015\-present). See the [Sentinel Data
Legal Notice](https://sentinels.copernicus.eu/documents/247904/690755/Sentinel_Data_Legal_Notice)




### Citations



Citations:
* Wojciech Sirko, Emmanuel Asiedu Brempong, Juliana T. C. Marcos, Abigail
Annkah, Abel Korme, Mohammed Alewi Hassen, Krishna Sapkota, Tomer Shekel,
Abdoulaye Diack, Sella Nevo, Jason Hickey, John Quinn. [High\-Resolution
Building and Road Detection from Sentinel\-2](https://arxiv.org/abs/2310.11622), 2023\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vargeometry=ee.Geometry.Point(
[31.549876545106667,30.011531513347673]);// New Cairo, Egypt

varcol=ee.ImageCollection('GOOGLE/Research/open-buildings-temporal/v1');

/**
 * Adds building presence and height layers for a given timestamp.
 * @param {number} millis Timestamp in milliseconds.
 */
functionaddLayers(millis){
// Create a mosaic of tiles with the same timestamp.
varmosaic=col.filter(ee.Filter.eq('system:time_start',millis)).mosaic();
varyear=newDate(millis).getFullYear();
Map.addLayer(
mosaic.select('building_presence'),{max:1},
'building_presence_conf_'+year);
Map.addLayer(
mosaic.select('building_height'),{max:100},'building_height_m_'+year,
/*shown=*/false);
};

// Get latest 2 years
varts=col.filterBounds(geometry)
.aggregate_array('system:time_start')
.distinct()
.sort()
.getInfo()
.slice(-2);


ts.forEach(addLayers);


Map.centerObject(geometry,14);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_Research_open-buildings-temporal_v1)


[Open Buildings Temporal V1](/earth-engine/datasets/catalog/GOOGLE_Research_open-buildings-temporal_v1)

The Open Buildings 2\.5D Temporal Dataset contains data about building presence, fractional building counts, and building heights at an effective1 spatial resolution of 4m (rasters are provided at 0\.5m resolution) at an annual cadence from 2016\-2023\. It is produced from open\-source, low\-resolution imagery from the Sentinel\-2 collection. The dataset is …

 GOOGLE/Research/open\-buildings\-temporal/v1,
 africa,annual,asia,built\-up,height,open\-buildings,population,south\-asia,southeast\-asia

2016\-06\-30T07:00:00Z/2023\-06\-30T07:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








