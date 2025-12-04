



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GPWv411: Population Density (Gridded Population of the World Version 4\.11\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2020\-01\-01T00:00:00Z
Dataset Provider


[NASA SEDAC at the Center for International Earth Science Information Network](https://doi.org/10.7927/H49C6VHW)



Earth Engine Snippet


`ee.ImageCollection("CIESIN/GPWv411/GPW_Population_Density")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CIESIN/CIESIN_GPWv411_GPW_Population_Density)





Cadence
5 Years
Tags


[ciesin](/earth-engine/datasets/tags/ciesin)
[gpw](/earth-engine/datasets/tags/gpw)
[nasa](/earth-engine/datasets/tags/nasa)
[population](/earth-engine/datasets/tags/population)








#### Description



This dataset contains estimates of the number of persons
per square kilometer consistent with national censuses and population
registers. There is one image for each modeled year.


[General Documentation](https://sedac.ciesin.columbia.edu/data/set/gpw-v4-population-density-rev11/docs)


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
| `population_density` | 0\* | 810694\* | The estimated number of persons per square kilometer. |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Center for International Earth Science Information Network \- CIESIN \-
Columbia University. 2018\. Gridded Population of the World, Version 4
(GPWv4\): Population Density, Revision 11\. Palisades, NY: NASA Socioeconomic Data and
Applications Center (SEDAC). [https://doi.org/10\.7927/H49C6VHW](https://doi.org/10.7927/H49C6VHW).
Accessed DAY MONTH YEAR.





### DOIs


* [https://doi.org/10\.7927/H49C6VHW](https://doi.org/10.7927/H49C6VHW)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('CIESIN/GPWv411/GPW_Population_Density').first();
varraster=dataset.select('population_density');
varraster_vis={
'max':1000.0,
'palette':[
'ffffe7',
'FFc869',
'ffac1d',
'e17735',
'f2552c',
'9f0c21'
],
'min':200.0
};
Map.setCenter(79.1,19.81,3);
Map.addLayer(raster,raster_vis,'population_density');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CIESIN/CIESIN_GPWv411_GPW_Population_Density)


[GPWv411: Population Density (Gridded Population of the World Version 4\.11\)](/earth-engine/datasets/catalog/CIESIN_GPWv411_GPW_Population_Density)

This dataset contains estimates of the number of persons per square kilometer consistent with national censuses and population registers. There is one image for each modeled year. General Documentation The Gridded Population of World Version 4 (GPWv4\), Revision 11 models the distribution of global human population for the years 2000, …

 CIESIN/GPWv411/GPW\_Population\_Density,
 ciesin,gpw,nasa,population

2000\-01\-01T00:00:00Z/2020\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7927/H49C6VHW](https://doi.org/https://doi.org/10.7927/H49C6VHW)
* [https://doi.org/10\.7927/H49C6VHW](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/CIESIN_GPWv411_GPW_Population_Density)









