



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

IrrMapper Irrigated Lands, Version 1\.2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================








Dataset Availability
1986\-01\-01T00:00:00Z–2024\-01\-01T00:00:00Z
Dataset Provider


[University of Montana / Montana Climate Office](https://climate.umt.edu/research/irrmapper/)



Earth Engine Snippet


`ee.ImageCollection("UMT/Climate/IrrMapper_RF/v1_2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMT/UMT_Climate_IrrMapper_RF_v1_2)





Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)








#### Description



IrrMapper is an annual classification of irrigation status in the 11
Western United States made at Landsat scale (i.e., 30 m) using the
Random Forest algorithm, covering years 1986 \- present.


While the [IrrMapper paper](https://www.mdpi.com/2072-4292/12/14/2328)
describes classification of four classes (i.e., irrigated, dryland,
uncultivated, wetland), the dataset is converted to a binary
classification of irrigated and non\-irrigated.


'Irrigated' refers to the detection of any irrigation during the year.
The IrrMapper random forest model was trained using an extensive
geospatial database of land cover from each of four irrigated\- and
non\-irrigated classes, including over 50,000 human\-verified irrigated
fields, 38,000 dryland fields, and over 500,000 square kilometers of
uncultivated lands.


For version 1\.2, the original training data was greatly expanded,
a RF model built for each state, and a more thorough validation and uncertainty
analysis undertaken. See the [supplement](https://static-content.springer.com/esm/art%3A10.1038%2Fs43247-023-01152-2/MediaObjects/43247_2023_1152_MOESM3_ESM.docx)
to our [paper](https://www.nature.com/articles/s43247-023-01152-2) on the impacts of irrigation on streamflow.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `classification` | Irrigated pixels have the value of 1, the other pixels are masked out. |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Ketchum, D.; Jencso, K.; Maneta, M.P.; Melton, F.; Jones, M.O.; Huntington, J.
IrrMapper: A Machine Learning Approach for High Resolution Mapping of
Irrigated Agriculture Across the Western U.S.,
Remote Sens. 2020, 12, 2328\. [doi:10\.3390/rs12142328](https://doi.org/10.3390/rs12142328)


Ketchum, D., Hoylman, Z.H., Huntington, J. et al. Irrigation intensification impacts sustainability
of streamflow in the Western United States. Commun Earth Environ 4, 479 (2023\). [doi:10\.1038/s43247\-023\-01152\-2](https://doi.org/10.1038/s43247-023-01152-2)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('UMT/Climate/IrrMapper_RF/v1_2');
varirr=dataset.filterDate('2023-01-01','2023-12-31').mosaic();

varvisualization={
min:0.0,
max:1.0,
palette:['blue']
};
Map.addLayer(irr,visualization,'IrrMapper 2023');
Map.setCenter(-112.516,45.262,10);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UMT/UMT_Climate_IrrMapper_RF_v1_2)


[IrrMapper Irrigated Lands, Version 1\.2](/earth-engine/datasets/catalog/UMT_Climate_IrrMapper_RF_v1_2)

IrrMapper is an annual classification of irrigation status in the 11 Western United States made at Landsat scale (i.e., 30 m) using the Random Forest algorithm, covering years 1986 \- present. While the IrrMapper paper describes classification of four classes (i.e., irrigated, dryland, uncultivated, wetland), the dataset is converted to …

 UMT/Climate/IrrMapper\_RF/v1\_2,
 agriculture,landsat\-derived

1986\-01\-01T00:00:00Z/2024\-01\-01T00:00:00Z



 31\.3 \-124\.5 49 \-99
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








