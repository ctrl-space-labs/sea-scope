



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WorldPop Global Project Population Data: Constrained Estimated Age and Sex Structures of Residential Population per 100x100m Grid Square


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================================================================================================================








Dataset Availability
2020\-01\-01T00:00:00Z–2021\-01\-01T00:00:00Z
Dataset Provider


[WorldPop](https://www.worldpop.org)



Earth Engine Snippet


`ee.ImageCollection("WorldPop/GP/100m/pop_age_sex_cons_unadj")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WorldPop/WorldPop_GP_100m_pop_age_sex_cons_unadj)





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


This dataset contains top\-down constrained breakdown of
estimated population by age and gender groups. Currently only 2020 data
are present.


Top\-down constrained age/sex structure estimate datasets for individual
countries for 2020 at 100m spatial resolution with country totals adjusted to
match the corresponding official United Nations population estimates that have
been prepared by the Population Division of the Department of Economic and
Social Affairs of the United Nations Secretariat
([2019 Revision of World Population Prospects](https://population.un.org/wpp/Download/Files/1_Indicators%20(Standard)/EXCEL_FILES/1_Population/WPP2019_POP_F01_1_TOTAL_POPULATION_BOTH_SEXES.xlsx)).


[See explanation of constrained vs unconstrained datasets](https://www.worldpop.org/methods/top_down_constrained_vs_unconstrained).


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
| `M_0` | Estimated number of men between 0 and 1 years old residing in each grid cell |
| `M_1` | Estimated number of men between 1 and 4 years old residing in each grid cell |
| `M_5` | Estimated number of men between 5 and 9 years old residing in each grid cell |
| `M_10` | Estimated number of men between 10 and 14 years old residing in each grid cell |
| `M_15` | Estimated number of men between 15 and 19 years old residing in each grid cell |
| `M_20` | Estimated number of men between 20 and 24 years old residing in each grid cell |
| `M_25` | Estimated number of men between 25 and 29 years old residing in each grid cell |
| `M_30` | Estimated number of men between 30 and 34 years old residing in each grid cell |
| `M_35` | Estimated number of men between 35 and 39 years old residing in each grid cell |
| `M_40` | Estimated number of men between 40 and 44 years old residing in each grid cell |
| `M_45` | Estimated number of men between 45 and 49 years old residing in each grid cell |
| `M_50` | Estimated number of men between 50 and 54 years old residing in each grid cell |
| `M_55` | Estimated number of men between 55 and 59 years old residing in each grid cell |
| `M_60` | Estimated number of men between 60 and 64 years old residing in each grid cell |
| `M_65` | Estimated number of men between 65 and 69 years old residing in each grid cell |
| `M_70` | Estimated number of men between 70 and 74 years old residing in each grid cell |
| `M_75` | Estimated number of men between 75 and 79 years old residing in each grid cell |
| `M_80` | Estimated number of men 80 years old or above residing in each grid cell |
| `F_0` | Estimated number of women between 0 and 1 years old residing in each grid cell |
| `F_1` | Estimated number of women between 1 and 4 years old residing in each grid cell |
| `F_5` | Estimated number of women between 5 and 9 years old residing in each grid cell |
| `F_10` | Estimated number of women between 10 and 14 years old residing in each grid cell |
| `F_15` | Estimated number of women between 15 and 19 years old residing in each grid cell |
| `F_20` | Estimated number of women between 20 and 24 years old residing in each grid cell |
| `F_25` | Estimated number of women between 25 and 29 years old residing in each grid cell |
| `F_30` | Estimated number of women between 30 and 34 years old residing in each grid cell |
| `F_35` | Estimated number of women between 35 and 39 years old residing in each grid cell |
| `F_40` | Estimated number of women between 40 and 44 years old residing in each grid cell |
| `F_45` | Estimated number of women between 45 and 49 years old residing in each grid cell |
| `F_50` | Estimated number of women between 50 and 54 years old residing in each grid cell |
| `F_55` | Estimated number of women between 55 and 59 years old residing in each grid cell |
| `F_60` | Estimated number of women between 60 and 64 years old residing in each grid cell |
| `F_65` | Estimated number of women between 65 and 69 years old residing in each grid cell |
| `F_70` | Estimated number of women between 70 and 74 years old residing in each grid cell |
| `F_75` | Estimated number of women between 75 and 79 years old residing in each grid cell |
| `F_80` | Estimated number of women 80 years old or above residing in each grid cell |


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
vardataset=ee.ImageCollection('WorldPop/GP/100m/pop_age_sex_cons_unadj');

varvisualization={
bands:['population'],
min:0.0,
max:50.0,
palette:['24126c','1fff4f','d4ff50']
};

Map.setCenter(113.643,34.769,7);

Map.addLayer(dataset,visualization,'Population');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WorldPop/WorldPop_GP_100m_pop_age_sex_cons_unadj)


[WorldPop Global Project Population Data: Constrained Estimated Age and Sex Structures of Residential Population per 100x100m Grid Square](/earth-engine/datasets/catalog/WorldPop_GP_100m_pop_age_sex_cons_unadj)

Global high\-resolution, contemporary data on human population distributions are a prerequisite for the accurate measurement of the impacts of population growth, for monitoring changes, and for planning interventions. The WorldPop project aims to meet these needs through the provision of detailed and open access population distribution datasets built using transparent …

 WorldPop/GP/100m/pop\_age\_sex\_cons\_unadj,
 demography,population,worldpop

2020\-01\-01T00:00:00Z/2021\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1038/sdata.2015\.45](https://doi.org/https://www.worldpop.org)
* [https://doi.org/10\.1038/sdata.2015\.45](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/WorldPop_GP_100m_pop_age_sex_cons_unadj)









