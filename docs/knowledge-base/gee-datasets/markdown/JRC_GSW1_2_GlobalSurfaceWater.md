



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

JRC Global Surface Water Mapping Layers, v1\.2 \[deprecated]


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================================








Dataset Availability
1984\-03\-16T00:00:00Z–2020\-01\-01T00:00:00Z
Dataset Provider


[EC JRC / Google](https://global-surface-water.appspot.com)



Earth Engine Snippet


`ee.Image("JRC/GSW1_2/GlobalSurfaceWater")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GSW1_2_GlobalSurfaceWater)





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
distribution of surface water from 1984 to 2019 and provides
statistics on the extent and change of those water surfaces.
For more information see the associated journal article: [High\-resolution
mapping of global surface water and its long\-term changes](https://www.nature.com/nature/journal/v540/n7633/full/nature20584.html)
(Nature, 2016\) and the online [Data Users Guide](https://storage.googleapis.com/global-surface-water/downloads_ancillary/DataUsersGuidev2.pdf).


These data were generated using 4,185,439 scenes from Landsat
5, 7, and 8 acquired between 16 March 1984 and 31 December 2019\.
Each pixel was individually classified into water / non\-water
using an expert system and the results were collated into a monthly
history for the entire time period and two epochs (1984\-1999,
2000\-2019\) for change detection.


This mapping layers product consists of 1 image containing 7 bands.
It maps different facets of the spatial and temporal distribution of
surface water over the last 35 years. Areas where water has
never been detected are masked.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `occurrence` | % | 0 | 100 | The frequency with which water was present. |
| `change_abs` | % | \-100 | 100 | Absolute change in occurrence between two epochs: 1984\-1999 vs 2000\-2019\. |
| `change_norm` | % | \-100 | 100 | Normalized change in occurrence. (epoch1\-epoch2\)/(epoch1\+epoch2\) \* 100 |
| `seasonality` | None | 0 | 12 | Number of months water is present. |
| `recurrence` | % | 0 | 100 | The frequency with which water returns from year to year. |
| `transition` | None | Categorical classification of change between first and last year. |
| `max_extent` | None | Binary image containing 1 anywhere water has ever been detected. |
| Bitmask for max\_extent * Bit 0: Flag indicating if water was detected or not 	+ 0: Not water 	+ 1: Water | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


**transition Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#ffffff | No change |
| 1 | \#0000ff | Permanent |
| 2 | \#22b14c | New permanent |
| 3 | \#d1102d | Lost permanent |
| 4 | \#99d9ea | Seasonal |
| 5 | \#b5e61d | New seasonal |
| 6 | \#e6a1aa | Lost seasonal |
| 7 | \#ff7f27 | Seasonal to permanent |
| 8 | \#ffc90e | Permanent to seasonal |
| 9 | \#7f7f7f | Ephemeral permanent |
| 10 | \#c3c3c3 | Ephemeral seasonal |




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
vardataset=ee.Image('JRC/GSW1_2/GlobalSurfaceWater');

varvisualization={
bands:['occurrence'],
min:0.0,
max:100.0,
palette:['ffffff','ffbbbb','0000ff']
};

Map.setCenter(59.414,45.182,6);

Map.addLayer(dataset,visualization,'Occurrence');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GSW1_2_GlobalSurfaceWater)


[JRC Global Surface Water Mapping Layers, v1\.2 \[deprecated]](/earth-engine/datasets/catalog/JRC_GSW1_2_GlobalSurfaceWater)

This dataset contains maps of the location and temporal distribution of surface water from 1984 to 2019 and provides statistics on the extent and change of those water surfaces. For more information see the associated journal article: High\-resolution mapping of global surface water and its long\-term changes (Nature, 2016\) and …

 JRC/GSW1\_2/GlobalSurfaceWater,
 geophysical,google,jrc,landsat\-derived,surface,surface\-ground\-water,water

1984\-03\-16T00:00:00Z/2020\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








