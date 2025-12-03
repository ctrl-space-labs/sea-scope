



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD44B.061 Terra Vegetation Continuous Fields Yearly Global 250m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================================








Dataset Availability
2000\-03\-05T00:00:00Z–2024\-03\-05T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MOD44B.006)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MOD44B")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD44B)





Cadence
1 Year
Tags


[annual](/earth-engine/datasets/tags/annual)
[geophysical](/earth-engine/datasets/tags/geophysical)
[global](/earth-engine/datasets/tags/global)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[terra](/earth-engine/datasets/tags/terra)
[tree\-cover](/earth-engine/datasets/tags/tree-cover)
[vegetation](/earth-engine/datasets/tags/vegetation)
mod44b








#### Description



The Terra MODIS Vegetation Continuous Fields (VCF)
product is a sub\-pixel\-level representation of surface vegetation
cover estimates globally. Designed to continuously represent
Earth's terrestrial surface as a proportion of basic vegetation
traits, it provides a gradation of three surface cover components:
percent tree cover, percent non\-tree cover, and percent bare.
VCF products provide a continuous, quantitative portrayal of
land surface cover with improved spatial detail, and hence, are
widely used in environmental modeling and monitoring applications.


Generated yearly, the VCF product is produced using monthly
composites of Terra MODIS 250 and 500 meters Land Surface Reflectance
data, including all seven bands, and Land Surface Temperature.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/1494/MOD44B_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/113/MOD44B_ATBD.pdf)
* [General Documentation](https://lpdaac.usgs.gov/products/mod44bv061/)





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `Percent_Tree_Cover` | % | 0 | 100 |  | Percent of a pixel which is covered by tree canopy |
| `Percent_NonTree_Vegetation` | % | 0 | 100 |  | Percent of a pixel which is covered by non\-tree vegetation |
| `Percent_NonVegetated` | % | 0 | 100 |  | Percent of a pixel which is not vegetated |
| `Quality` | None |  | Describes those inputs that had poor quality (cloudy, high aerosol, cloud shadow, or view zenith \>45°). Each bit in the field represents 1 out of 8 input surface reflectance files to the model. |
| Bitmask for Quality * Bit 0: State of input layers DOY 065\-097 	+ 0: Clear 	+ 1: Bad * Bit 1: State of input layers DOY 113\-145 	+ 0: Clear 	+ 1: Bad * Bit 2: State of input layers DOY 161\-193 	+ 0: Clear 	+ 1: Bad * Bit 3: State of input layers DOY 209\-241 	+ 0: Clear 	+ 1: Bad * Bit 4: State of input layers DOY 257\-289 	+ 0: Clear 	+ 1: Bad * Bit 5: State of input layers DOY 305\-337 	+ 0: Clear 	+ 1: Bad * Bit 6: State of input layers DOY 353\-017 	+ 0: Clear 	+ 1: Bad * Bit 7: State of input layers DOY 033\-045 	+ 0: Clear 	+ 1: Bad | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `Percent_Tree_Cover_SD` | % | 0 | 32767 | 0\.01 | Standard deviation (SD) of the 30 models that were used to generate the pixel value in the percent tree cover data layer |
| `Percent_NonVegetated_SD` | % | 0 | 32767 | 0\.01 | Standard deviation (SD) of the 30 models that were used to generate the pixel value in the percent non\-vegetated data layer |
| `Cloud` | None |  | Clarifies the 'Quality' layer to give the user an indication that the 'bad' data refers to cloudy input data. Each bit in the field represents 1 out of 8 input surface reflectance files to the model. |
| Bitmask for Cloud * Bit 0: State of input layers DOY 065\-097 	+ 0: Clear 	+ 1: Cloudy * Bit 1: State of input layers DOY 113\-145 	+ 0: Clear 	+ 1: Cloudy * Bit 2: State of input layers DOY 161\-193 	+ 0: Clear 	+ 1: Cloudy * Bit 3: State of input layers DOY 209\-241 	+ 0: Clear 	+ 1: Cloudy * Bit 4: State of input layers DOY 257\-289 	+ 0: Clear 	+ 1: Cloudy * Bit 5: State of input layers DOY 305\-337 	+ 0: Clear 	+ 1: Cloudy * Bit 6: State of input layers DOY 353\-017 	+ 0: Clear 	+ 1: Cloudy * Bit 7: State of input layers DOY 033\-045 	+ 0: Clear 	+ 1: Cloudy | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MOD44B')
.filter(ee.Filter.date('2000-01-01','2001-01-01'));

varvisualization={
bands:['Percent_Tree_Cover'],
min:0,
max:100,
palette:['bbe029','0a9501','074b03']
};

Map.setCenter(6.746,46.529,3);

Map.addLayer(dataset,visualization,'Percent Tree Cover');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD44B)


[MOD44B.061 Terra Vegetation Continuous Fields Yearly Global 250m](/earth-engine/datasets/catalog/MODIS_061_MOD44B)

The Terra MODIS Vegetation Continuous Fields (VCF) product is a sub\-pixel\-level representation of surface vegetation cover estimates globally. Designed to continuously represent Earth's terrestrial surface as a proportion of basic vegetation traits, it provides a gradation of three surface cover components: percent tree cover, percent non\-tree cover, and percent bare. …

 MODIS/061/MOD44B,
 annual,geophysical,global,landuse\-landcover,modis,nasa,terra,tree\-cover,vegetation

2000\-03\-05T00:00:00Z/2024\-03\-05T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








