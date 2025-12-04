



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

JRC Monthly Water Recurrence, v1\.4


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================








Dataset Availability
1984\-03\-16T00:00:00Z–2022\-01\-01T00:00:00Z
Dataset Provider


[EC JRC / Google](https://global-surface-water.appspot.com)



Earth Engine Snippet


`ee.ImageCollection("JRC/GSW1_4/MonthlyRecurrence")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GSW1_4_MonthlyRecurrence)





Climatological Interval
1 Month
Tags


[geophysical](/earth-engine/datasets/tags/geophysical)
[google](/earth-engine/datasets/tags/google)
[history](/earth-engine/datasets/tags/history)
[jrc](/earth-engine/datasets/tags/jrc)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[monthly](/earth-engine/datasets/tags/monthly)
[surface](/earth-engine/datasets/tags/surface)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[water](/earth-engine/datasets/tags/water)
recurrence








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


The Monthly Recurrence collection contains 12 images: monthly measures of
the seasonality of water based on the occurrence values detected in that
month over all years.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `monthly_recurrence` | % | 0 | 100 | The recurrence value expressed as a percentage for this month. |
| `has_observations` | None | A flag to indicate if the month has observations. |
| Bitmask for has\_observations * Bit 0: Observations for the month. 	+ 0: No valid observations 	+ 1: At least 1 valid observation was available | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| month | DOUBLE | Month |




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
vardataset=ee.ImageCollection('JRC/GSW1_4/MonthlyRecurrence');

varvisualization={
bands:['monthly_recurrence'],
min:0.0,
max:100.0,
palette:['ffffff','ffbbbb','0000ff']
};

Map.setCenter(-51.482,-0.835,6);

Map.addLayer(dataset,visualization,'Monthly Recurrence');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GSW1_4_MonthlyRecurrence)


[JRC Monthly Water Recurrence, v1\.4](/earth-engine/datasets/catalog/JRC_GSW1_4_MonthlyRecurrence)

This dataset contains maps of the location and temporal distribution of surface water from 1984 to 2021 and provides statistics on the extent and change of those water surfaces. For more information see the associated journal article: High\-resolution mapping of global surface water and its long\-term changes (Nature, 2016\) and …

 JRC/GSW1\_4/MonthlyRecurrence,
 geophysical,google,history,jrc,landsat\-derived,monthly,surface,surface\-ground\-water,water

1984\-03\-16T00:00:00Z/2022\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








