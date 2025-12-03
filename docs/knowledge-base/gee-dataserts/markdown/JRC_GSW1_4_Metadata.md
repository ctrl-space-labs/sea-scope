



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

JRC Global Surface Water Metadata, v1\.4


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================








Dataset Availability
1984\-03\-16T00:00:00Z–2022\-01\-01T00:00:00Z
Dataset Provider


[EC JRC / Google](https://global-surface-water.appspot.com)



Earth Engine Snippet


`ee.Image("JRC/GSW1_4/Metadata")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GSW1_4_Metadata)





Tags


[geophysical](/earth-engine/datasets/tags/geophysical)
[google](/earth-engine/datasets/tags/google)
[jrc](/earth-engine/datasets/tags/jrc)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[surface](/earth-engine/datasets/tags/surface)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[water](/earth-engine/datasets/tags/water)








#### Description



This dataset contains maps of the location and temporal
distribution of surface water from 1984 to 2021 and provides
statistics on the extent and change of those water surfaces.
For more information see the associated journal article: [High\-resolution
mapping of global surface water and its long\-term changes](https://www.nature.com/nature/journal/v540/n7633/full/nature20584.html)
(Nature, 2016\) and the online
[Data Users Guide](https://storage.googleapis.com/global-surface-water/downloads_ancillary/DataUsersGuidev2021.pdf).


These data were generated using 4,716,475 scenes from Landsat
5, 7, and 8 acquired between 16 March 1984 and 31 December 2021\.
Each pixel was individually classified into water / non\-water
using an expert system and the results were collated into a monthly
history for the entire time period and two epochs (1984\-1999,
2000\-2021\) for change detection.


This product contains metadata about the observations that went into
computing The Global Surface Water dataset. Areas where water has never
been detected are masked.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `detections` | 0\* | 2007\* | The number of water detections in the study period. |
| `valid_obs` | 0\* | 2076\* | The number of valid observations in the study period. |
| `total_obs` | 0\* | 2417\* | The total number of available observations (i.e. scenes) in the study period. |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


All data here is produced under the Copernicus Programme and is provided
free of charge, without restriction of use. For the full license
information see the Copernicus Regulation.


Publications, models, and data products that make use of these datasets
must include proper acknowledgement, including citing datasets and the
journal article as in the following citation.


If you are using the data as a layer in a published map, please include the
following attribution text: 'Source: EC JRC/Google'




### Citations



Citations:
* Jean\-Francois Pekel, Andrew Cottam, Noel Gorelick, Alan S. Belward,
High\-resolution mapping of global surface water and its long\-term changes.
Nature 540, 418\-422 (2016\). ([doi:10\.1038/nature20584](https://doi.org/10.1038/nature20584))





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('JRC/GSW1_4/Metadata');

varvisualization={
bands:['detections','valid_obs','total_obs'],
min:100.0,
max:900.0,
};

Map.setCenter(71.72,52.48,0);

Map.addLayer(dataset,visualization,'Detections/Observations');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GSW1_4_Metadata)


[JRC Global Surface Water Metadata, v1\.4](/earth-engine/datasets/catalog/JRC_GSW1_4_Metadata)

This dataset contains maps of the location and temporal distribution of surface water from 1984 to 2021 and provides statistics on the extent and change of those water surfaces. For more information see the associated journal article: High\-resolution mapping of global surface water and its long\-term changes (Nature, 2016\) and …

 JRC/GSW1\_4/Metadata,
 geophysical,google,jrc,landsat\-derived,surface,surface\-ground\-water,water

1984\-03\-16T00:00:00Z/2022\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








