



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GPWv411: Water Mask (Gridded Population of the World Version 4\.11\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2020\-01\-01T00:00:00Z
Dataset Provider


[NASA SEDAC at the Center for International Earth Science Information Network](https://doi.org/10.7927/H42Z13KG)



Earth Engine Snippet


`ee.ImageCollection("CIESIN/GPWv411/GPW_Water_Mask")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CIESIN/CIESIN_GPWv411_GPW_Water_Mask)





Tags


[ciesin](/earth-engine/datasets/tags/ciesin)
[gpw](/earth-engine/datasets/tags/gpw)
[nasa](/earth-engine/datasets/tags/nasa)
[population](/earth-engine/datasets/tags/population)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)








#### Description



This dataset identifies water pixels; non\-water pixels are masked.
The water mask was used to exclude areas of water and permanent ice
from the population allocation.


[General Documentation](https://sedac.ciesin.columbia.edu/data/set/gpw-v4-basic-demographic-characteristics-rev11/docs)


The Gridded Population of World Version 4 (GPWv4\), Revision 11 models the distribution
of global human population for the years 2000, 2005, 2010, 2015, and 2020
on 30 arc\-second (approximately 1 km) grid cells. Population is distributed
to cells using proportional allocation of population from census and
administrative units. Population input data are collected at the most
detailed spatial resolution available from the results of the 2010 round of
censuses, which occurred between 2005 and 2014\. The input data are
extrapolated to produce population estimates for each modeled year.





### Bands



**Pixel Size**
  
927\.67 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `water_mask` | Water mask |
| Bitmask for water\_mask * Bits 0\-1: Identifies water pixels; non\-water pixels are masked 	+ 0: Total water pixels that are completely water and/or permanent ice. 	+ 1: Partial water pixels that also contain land. 	+ 2: Total land pixels. 	+ 3: Ocean pixels. | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Center for International Earth Science Information Network \- CIESIN \-
Columbia University. 2018\. Gridded Population of the World, Version 4
(GPWv4\): Water Mask, Revision 11\. Palisades, NY: NASA Socioeconomic Data
and Applications Center (SEDAC). [https://doi.org/10\.7927/H42Z13KG](https://doi.org/10.7927/H42Z13KG).
Accessed DAY MONTH YEAR.





### DOIs


* [https://doi.org/10\.7927/H42Z13KG](https://doi.org/10.7927/H42Z13KG)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('CIESIN/GPWv411/GPW_Water_Mask');
varraster=dataset.select('water_mask');
varraster_vis={
'min':0.0,
'palette':[
'005ce6',
'00ffc5',
'bed2ff',
'aed0f1'
],
'max':3.0
};
Map.setCenter(-88.6,26.4,1);
Map.addLayer(raster,raster_vis,'water_mask');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CIESIN/CIESIN_GPWv411_GPW_Water_Mask)


[GPWv411: Water Mask (Gridded Population of the World Version 4\.11\)](/earth-engine/datasets/catalog/CIESIN_GPWv411_GPW_Water_Mask)

This dataset identifies water pixels; non\-water pixels are masked. The water mask was used to exclude areas of water and permanent ice from the population allocation. General Documentation The Gridded Population of World Version 4 (GPWv4\), Revision 11 models the distribution of global human population for the years 2000, 2005, …

 CIESIN/GPWv411/GPW\_Water\_Mask,
 ciesin,gpw,nasa,population,surface\-ground\-water

2000\-01\-01T00:00:00Z/2020\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7927/H42Z13KG](https://doi.org/https://doi.org/10.7927/H42Z13KG)
* [https://doi.org/10\.7927/H42Z13KG](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/CIESIN_GPWv411_GPW_Water_Mask)









