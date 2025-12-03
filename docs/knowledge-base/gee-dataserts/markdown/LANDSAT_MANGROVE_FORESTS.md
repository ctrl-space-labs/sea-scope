



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global Mangrove Forests Distribution, v1 (2000\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2001\-01\-01T00:00:00Z
Dataset Provider


[NASA SEDAC at the Center for International Earth Science Information Network](https://doi.org/10.7927/H4J67DW8)



Earth Engine Snippet


`ee.ImageCollection("LANDSAT/MANGROVE_FORESTS")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_MANGROVE_FORESTS)





Tags


[annual](/earth-engine/datasets/tags/annual)
[ciesin](/earth-engine/datasets/tags/ciesin)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[global](/earth-engine/datasets/tags/global)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[mangrove](/earth-engine/datasets/tags/mangrove)
[nasa](/earth-engine/datasets/tags/nasa)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The database was prepared using Landsat satellite data from the year 2000\.
More than 1,000 Landsat scenes obtained from the USGS Earth Resources
Observation and Science Center (EROS) were classified using hybrid
supervised and unsupervised digital image classification techniques. This
database is the first, most comprehensive mangrove assessment of the world
([Giri et al., 2011](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1466-8238.2010.00584.x)).
Partial funding of this research was provided by NASA.


The mangrove database is being used for identifying priority areas
for mangrove conservation, studying the role of mangrove forests in
saving lives and properties from natural disasters (e.g. tsunami),
carbon accounting, and biodiversity conservation. The USGS EROS has
been using the data to study the impact of sea level rise on mangrove
ecosystems. The database serves as a baseline for mangrove
monitoring.


[General Documentation](https://sedac.ciesin.columbia.edu/data/set/lulc-global-mangrove-forests-distribution-2000/docs)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `1` | Mangroves |


**1 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d40115 | Mangroves |




### Terms of Use


**Terms of Use**


Landsat datasets are federally created data
and therefore reside in the public domain and may be used, transferred, or reproduced without copyright restriction.


Acknowledgement or credit of the USGS as data source should be provided
by including a line of text citation such as the example shown below.


(Product, Image, Photograph, or Dataset Name) courtesy of
the U.S. Geological Survey


Example: Landsat\-7 image courtesy of the U.S. Geological Survey


See the
[USGS Visual Identity System Guidance](https://www.usgs.gov/information-policies-and-instructions/usgs-visual-identity-system)
for further details on proper citation and acknowledgement of USGS products.




### Citations



Citations:
* Giri, C., E. Ochieng, L.L.Tieszen, Z. Zhu, A. Singh, T. Loveland, J. Masek, and N. Duke. 2013\. Global Mangrove Forests Distribution, 2000\. Palisades, NY: NASA Socioeconomic Data and Applications Center (SEDAC). [https://doi.org/10\.7927/H4J67DW8](https://doi.org/10.7927/H4J67DW8). Accessed DAY MONTH YEAR
* Giri, C., E. Ochieng, L. L. Tieszen, Z. Zhu, A. Singh, T. Loveland, J. Masek, and N. Duke. 2010\. Status and Distribution of Mangrove Forests of the World Using Earth Observation Satellite Data. Global Ecology and Biogeography: A Journal of Macroecology 20(1\): 154\-159\. [https://doi.org/10\.1111/j.1466\-8238\.2010\.00584\.x](https://doi.org/10.1111/j.1466-8238.2010.00584.x).





### DOIs


* [https://doi.org/10\.1111/j.1466\-8238\.2010\.00584\.x](https://doi.org/10.1111/j.1466-8238.2010.00584.x)
* [https://doi.org/10\.7927/H4J67DW8](https://doi.org/10.7927/H4J67DW8)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('LANDSAT/MANGROVE_FORESTS');
varmangrovesVis={
min:0,
max:1.0,
palette:['d40115'],
};
Map.setCenter(-44.5626,-2.0164,9);
Map.addLayer(dataset,mangrovesVis,'Mangroves');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_MANGROVE_FORESTS)


[Global Mangrove Forests Distribution, v1 (2000\)](/earth-engine/datasets/catalog/LANDSAT_MANGROVE_FORESTS)

The database was prepared using Landsat satellite data from the year 2000\. More than 1,000 Landsat scenes obtained from the USGS Earth Resources Observation and Science Center (EROS) were classified using hybrid supervised and unsupervised digital image classification techniques. This database is the first, most comprehensive mangrove assessment of the …

 LANDSAT/MANGROVE\_FORESTS,
 annual,ciesin,forest\-biomass,global,landsat\-derived,mangrove,nasa,usgs

2000\-01\-01T00:00:00Z/2001\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7927/H4J67DW8](https://doi.org/https://doi.org/10.7927/H4J67DW8)
* [https://doi.org/10\.7927/H4J67DW8](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_MANGROVE_FORESTS)









