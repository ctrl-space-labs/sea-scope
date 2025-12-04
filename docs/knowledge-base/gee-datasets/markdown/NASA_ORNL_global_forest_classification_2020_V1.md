



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global 2020 Forest Classification for IPCC Aboveground Biomass Tier 1 Estimates, V1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================================================








Dataset Availability
2020\-01\-01T00:00:00Z–2020\-12\-31T00:00:00Z
Dataset Provider


[NASA ORNL DAAC at Oak Ridge National Laboratory](https://doi.org/10.3334/ORNLDAAC/2345)



Earth Engine Snippet


`ee.ImageCollection("NASA/ORNL/global_forest_classification_2020/V1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_ORNL_global_forest_classification_2020_V1)





Tags


[aboveground](/earth-engine/datasets/tags/aboveground)
[biomass](/earth-engine/datasets/tags/biomass)
[carbon](/earth-engine/datasets/tags/carbon)
[classification](/earth-engine/datasets/tags/classification)
[forest](/earth-engine/datasets/tags/forest)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[ipcc](/earth-engine/datasets/tags/ipcc)
[nasa](/earth-engine/datasets/tags/nasa)
[primary\-forest](/earth-engine/datasets/tags/primary-forest)
secondary\-forest








#### Description



This dataset provides classes of global forests delineated by
status/condition in 2020 at approximately 30m resolution. The data support
generating Tier 1 estimates for Aboveground dry woody Biomass Density (AGBD)
in natural forests in the 2019 Refinement to the 2006 IPCC Guidelines for
National Greenhouse Gas Inventories. Forest classes include primary, young
secondary (\<\=20 years), and old secondary forests (\>20 years). Classification
was based on a Boolean combination of a suite of existing Earth Observation
(EO) products of forest tree cover, height, age, and land use classification
layers representing years 2000 to 2020\. This forest status/condition
classification prioritizes the reduction of potential errors of commission in
the delineations by minimizing the inclusion of ambiguous pixels. Hence, it
provides a conservative estimate of global forest area, identifying
approximately 3\.26 billion ha of forests worldwide.


### Quality Assessment


These data provide a comprehensive compilation of the latest published
datasets on forest conditions, but the nonexistence of any independent sample
of global data that would enable the validation of these delineations is a
constraint. Hence, the global forest status/condition classification has not
been validated.


### Data Acquisition, Materials, and Methods


The forest status/condition classification is created by conducting a
Boolean analysis of a suite of existing datasets (see Table 1,
[Hunka et al., 2024](https://doi.org/10.1038/s41597-024-03930-9)),
including satellite\-derived forest tree cover, height, age,
and land use classification layers. In this approach, layers that
identify a potential forest status/condition class (e.g. primary forests) are
merged, and layers that identify sources of disagreement (e.g. presence of
plantations or deforestation detected in the delineated primary forests) are
used to remove areas of potential commission errors.


The primary forest class is established using datasets identifying
intact/primary forests, with a high forest integrity index, the presence of
tree cover and forest heights ≥5 m and no known forest loss events, planted
forests or plantations.


The young secondary forest class captures pixels that had changes in
forest height or cover between 2000 and 2020, excluding planted forests and
plantations. These forests were identified by heights ≥5 m in 2020 and either
(a) heights \<5 m in 2000 or (b) heights ≥5 m in 2000 but having experienced
tree cover loss after 2000\.


The old secondary forest class captures the remainder of pixels with
forests after excluding the primary and young secondary forest classes. These
pixels had forest heights ≥5 m in both 2000 and 2020 with no tree cover loss
nor forest disturbances detected after 2000, nor any planted forests or
plantations.


[Schematic of analysis workflow](https://daac.ornl.gov/CMS/guides/CMS_Global_Forest_Age_Fig2.jpg)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `classification` | Forest Type |


**classification Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#00ff00 | Primary Forest |
| 2 | \#ff0000 | Young Secondary Forest |
| 3 | \#6666ff | Old Secondary Forest |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* Hunka, N., L. Duncanson, J. Armston, R.O. Dubayah, S.P. Healey, M.
Santoro, P. May, A. Araza, C. Bourgain, P.M. Montesano, C.S. Neigh, H.
Grantham, V. Potapov, S. Turubanova, A. Tyukavina, J. Richter, N. Harris, M.
Urbazaev, A. Pascual, D. Requena Suarez, M. Herold, B. Poulter, S.N. Wilson,
G. Grassi, S. Federici, M.J. Sanz Sanchez, and J. Melo. 2024\. Classification
of Global Forests for IPCC Aboveground Biomass Tier 1 Estimates, 2020\. ORNL
DAAC, Oak Ridge, Tennessee, USA.
[https://doi.org/10\.3334/ORNLDAAC/2345](https://doi.org/10.3334/ORNLDAAC/2345)
* Hunka, N., Duncanson, L., Armston, J. et al. Intergovernmental Panel on Climate Change (IPCC) Tier 1 forest biomass estimates from Earth Observation. Sci Data 11, 1127 (2024\). https://doi.org/10\.1038/s41597\-024\-03930\-9
[doi:10\.1038/s41597\-024\-03930\-9](https://doi.org/10.1038/s41597-024-03930-9)





### DOIs


* [https://doi.org/10\.1038/s41597\-024\-03930\-9](https://doi.org/10.1038/s41597-024-03930-9)
* [https://doi.org/10\.3334/ORNLDAAC/2345](https://doi.org/10.3334/ORNLDAAC/2345)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/ORNL/global_forest_classification_2020/V1');

varvisualization={
bands:['classification'],
min:1.0,
max:3.0,
palette:['00ff00','ff0000','6666ff'],
};

Map.setCenter(-53,-5,6);
Map.addLayer(dataset,visualization,'Forest Type');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_ORNL_global_forest_classification_2020_V1)


[Global 2020 Forest Classification for IPCC Aboveground Biomass Tier 1 Estimates, V1](/earth-engine/datasets/catalog/NASA_ORNL_global_forest_classification_2020_V1)

This dataset provides classes of global forests delineated by status/condition in 2020 at approximately 30m resolution. The data support generating Tier 1 estimates for Aboveground dry woody Biomass Density (AGBD) in natural forests in the 2019 Refinement to the 2006 IPCC Guidelines for National Greenhouse Gas Inventories. Forest classes include …

 NASA/ORNL/global\_forest\_classification\_2020/V1,
 aboveground,biomass,carbon,classification,forest,forest\-biomass,ipcc,nasa,primary\-forest

2020\-01\-01T00:00:00Z/2020\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.3334/ORNLDAAC/2345](https://doi.org/https://doi.org/10.3334/ORNLDAAC/2345)
* [https://doi.org/10\.3334/ORNLDAAC/2345](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_ORNL_global_forest_classification_2020_V1)









