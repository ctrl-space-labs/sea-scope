



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WorldPop Global Project Population Data: Estimated Residential Population per 100x100m Grid Square


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2021\-01\-01T00:00:00Z
Dataset Provider


[WorldPop](https://www.worldpop.org)



Earth Engine Snippet


`ee.ImageCollection("WorldPop/GP/100m/pop")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WorldPop/WorldPop_GP_100m_pop)





Tags


[demography](/earth-engine/datasets/tags/demography)
[population](/earth-engine/datasets/tags/population)
[worldpop](/earth-engine/datasets/tags/worldpop)








#### Description



Global high\-resolution, contemporary data on human population distributions are
a prerequisite for the accurate measurement of the impacts of population
growth, for monitoring changes, and for planning interventions. The WorldPop
project aims to meet these needs through the provision of detailed and open
access population distribution datasets built using transparent and
peer\-reviewed approaches.


Full details on the methods and datasets used in constructing the
data, along with open access publications, are provided on the
[WorldPop website](https://www.worldpop.org/). In brief, recent census\-based
population counts matched to their associated administrative units are
disaggregated to \~100x100m grid cells through machine learning approaches
that exploit the relationships between population densities and a range of
geospatial covariate layers. The mapping approach
is Random Forest\-based dasymetric redistribution.


This dataset depict estimated number of people
residing in each grid cell in 2010, 2015, and other years.


For 2020, the breakdown of population by age and sex is available in
the [WorldPop/GP/100m/pop\_age\_sex](/earth-engine/datasets/catalog/WorldPop_GP_100m_pop_age_sex)
and [WorldPop/GP/100m/pop\_age\_sex\_cons\_unadj](/earth-engine/datasets/catalog/WorldPop_GP_100m_pop_age_sex_cons_unadj)
collections.


Further WorldPop gridded datasets on population age structures,
poverty, urban growth, and population dynamics are freely available on
the WorldPop website. WorldPop represents a collaboration between
researchers at the University of Southampton, Universite Libre de
Bruxelles, and University of Louisville. The project is principally funded by
the Bill and Melinda Gates Foundation.





### Bands



**Pixel Size**
  
92\.77 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `population` | 0\* | 21171\* | Estimated number of people residing in each grid cell |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| country | STRING | Country |
| year | DOUBLE | Year |




### Terms of Use


**Terms of Use**


WorldPop datasets are licensed under the Creative Commons Attribution 4\.0
International License. Users are free to use, copy, distribute, transmit,
and adapt the work for commercial and non\-commercial purposes, without
restriction, as long as clear attribution of the source is provided.




### Citations



Citations:
* Please cite the WorldPop website as the source: [www.worldpop.org](https://www.worldpop.org).
* Americas population data: Alessandro Sorichetta, Graeme M. Hornby,
Forrest R. Stevens, Andrea E. Gaughan, Catherine Linard, Andrew J. Tatem,
2015, High\-resolution gridded population datasets for Latin America and the
Caribbean in 2010, 2015, and 2020, Scientific Data,
[doi:10\.1038/sdata.2015\.45](https://doi.org/10.1038/sdata.2015.45)
* Africa population count data: Linard, C., Gilbert, M., Snow, R.W., Noor,
A.M. and Tatem, A.J., 2012, Population distribution, settlement patterns
and accessibility across Africa in 2010, PLoS ONE, 7(2\): e31743\.
* Asia population count data: Gaughan AE, Stevens FR, Linard C, Jia P and
Tatem AJ, 2013, High resolution population distribution maps for Southeast
Asia in 2010 and 2015, PLoS ONE, 8(2\): e55882\.





### DOIs


* [https://doi.org/10\.1038/sdata.2015\.45](https://doi.org/10.1038/sdata.2015.45)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('WorldPop/GP/100m/pop');

varvisualization={
bands:['population'],
min:0.0,
max:50.0,
palette:['24126c','1fff4f','d4ff50']
};

Map.setCenter(113.643,34.769,7);

Map.addLayer(dataset,visualization,'Population');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WorldPop/WorldPop_GP_100m_pop)


[WorldPop Global Project Population Data: Estimated Residential Population per 100x100m Grid Square](/earth-engine/datasets/catalog/WorldPop_GP_100m_pop)

Global high\-resolution, contemporary data on human population distributions are a prerequisite for the accurate measurement of the impacts of population growth, for monitoring changes, and for planning interventions. The WorldPop project aims to meet these needs through the provision of detailed and open access population distribution datasets built using transparent …

 WorldPop/GP/100m/pop,
 demography,population,worldpop

2000\-01\-01T00:00:00Z/2021\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1038/sdata.2015\.45](https://doi.org/https://www.worldpop.org)
* [https://doi.org/10\.1038/sdata.2015\.45](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/WorldPop_GP_100m_pop)









