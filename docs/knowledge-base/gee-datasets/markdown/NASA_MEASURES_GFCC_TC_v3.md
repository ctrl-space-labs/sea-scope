



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global Forest Cover Change (GFCC) Tree Cover Multi\-Year Global 30m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2015\-01\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MEaSUREs/GFCC/GFCC30TC.003)



Earth Engine Snippet


`ee.ImageCollection("NASA/MEASURES/GFCC/TC/v3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_MEASURES_GFCC_TC_v3)





Cadence
5 Years
Tags


[forest](/earth-engine/datasets/tags/forest)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[glcf](/earth-engine/datasets/tags/glcf)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[nasa](/earth-engine/datasets/tags/nasa)
[umd](/earth-engine/datasets/tags/umd)








#### Description



The Landsat Vegetation Continuous Fields (VCF) tree cover layers contain
estimates of the percentage of horizontal ground in each 30\-m pixel covered
by woody vegetation greater than 5 meters in height. The dataset is available
for four epochs centered on the years 2000, 2005, 2010 and 2015\. The dataset
is derived from the GFCC Surface Reflectance product (GFCC30SR), which is
based on enhanced Global Land Survey (GLS) datasets. The GLS datasets are
composed of high\-resolution Landsat 5 Thematic Mapper (TM) and Landsat 7
Enhanced Thematic Mapper Plus (ETM\+) images at 30 meter resolution.


Tree cover, the proportional, vertically projected area of vegetation
(including leaves, stems, branches, etc.) of woody plants above a given
height, affects terrestrial energy and water exchanges, photosynthesis and
transpiration, net primary production, and carbon and nutrient fluxes. Tree
cover also affects habitat quality and movements of wildlife, residential
property value for humans, and other ecosystem services. The continuous
classification scheme of the VCF product enables better depiction of land
cover gradients than traditional discrete classification schemes.
Importantly for detection and monitoring of forest changes (e.g.,
deforestation and degradation), tree cover provides a measurable attribute
upon which to define forest cover and its changes. Changes in tree cover
over time can be used to monitor and retrieve site\-specific histories of
forest change.


The dataset has been produced for four year epochs: 2000, 2005, 2010, and
2015 with an image in the collection for each available WRS2 path/row.


Documentation:


* [User's guide](https://lpdaac.usgs.gov/documents/1371/GFCC_User_Guide_V1.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/1370/GFCC_ATBD.pdf)


Provider's Note: Due to the end of NASA MEaSUREs funding, free versions of this dataset are no
longer being produced. Interested parties can obtain updated and expanded versions at
www.terraPulse.com.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `tree_canopy_cover` | % | 0 | 100 | The percentage of pixel area covered by trees. |
| `uncertainty` | None | RMSE for tree\-canopy\_cover |
| `source_index` | None | Identity of source image used for the particular pixel. This is an index into the per image metadata array 'sources'. Only available for 2000, 2005, and 2010\. |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| path | DOUBLE | Path |
| pathrow | STRING | Path and row |
| row | DOUBLE | Row |
| sources | DOUBLE | Sources. Only available for 2000, 2005, and 2010\. |
| tree\_canopy\_cover\_class\_palette | DOUBLE | Tree canopy cover class palette |
| tree\_canopy\_cover\_class\_values | DOUBLE | Tree canopy cover class values |
| year | DOUBLE | Year |




### Terms of Use


**Terms of Use**


Intellectual property rights to this dataset belong to
University of Maryland, Department of Geographical Sciences and NASA. Usage
is free if acklowedgement is made.




### Citations



Citations:
* Paper/Methods Citation: Sexton, J. O., Song, X.\-P., Feng, M., Noojipady,
P., Anand, A., Huang, C., Kim, D.\-H., Collins, K.M., Channan, S.,
DiMiceli, C., Townshend, J.R.G. (2013\). Global, 30\-m resolution
continuous fields of tree cover: Landsat\-based rescaling of MODIS
Vegetation Continuous Fields with lidar\-based estimates of error.
International Journal of Digital Earth, 130321031236007\.
[doi:10\.1080/17538947\.2013\.786146](https://doi.org/10.1080/17538947.2013.786146).





### DOIs


* [https://doi.org/10\.5067/MEaSUREs/GFCC/GFCC30TC.003](https://doi.org/10.5067/MEaSUREs/GFCC/GFCC30TC.003)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/MEASURES/GFCC/TC/v3')
.filter(ee.Filter.date('2015-01-01','2015-12-31'));
vartreeCanopyCover=dataset.select('tree_canopy_cover');
vartreeCanopyCoverVis={
min:0.0,
max:100.0,
palette:['ffffff','afce56','5f9c00','0e6a00','003800'],
};
Map.setCenter(-88.6,26.4,3);
Map.addLayer(treeCanopyCover.mean(),treeCanopyCoverVis,'Tree Canopy Cover');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_MEASURES_GFCC_TC_v3)


[Global Forest Cover Change (GFCC) Tree Cover Multi\-Year Global 30m](/earth-engine/datasets/catalog/NASA_MEASURES_GFCC_TC_v3)

The Landsat Vegetation Continuous Fields (VCF) tree cover layers contain estimates of the percentage of horizontal ground in each 30\-m pixel covered by woody vegetation greater than 5 meters in height. The dataset is available for four epochs centered on the years 2000, 2005, 2010 and 2015\. The dataset is …

 NASA/MEASURES/GFCC/TC/v3,
 forest,forest\-biomass,glcf,landsat\-derived,nasa,umd

2000\-01\-01T00:00:00Z/2015\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MEaSUREs/GFCC/GFCC30TC.003](https://doi.org/https://doi.org/10.5067/MEaSUREs/GFCC/GFCC30TC.003)
* [https://doi.org/10\.5067/MEaSUREs/GFCC/GFCC30TC.003](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_MEASURES_GFCC_TC_v3)









