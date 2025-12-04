



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GPW Annual Dominant Class of Grasslands v1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================









info


 This dataset is part of a Publisher Catalog, and not managed by Google Earth Engine.
 
 Contact [Land \& Carbon Lab](https://landcarbonlab.org/subscribe)
 
 for bugs or [view more datasets](https://developers.google.com/earth-engine/datasets/publisher/global-pasture-watch)
 from the Land \& Carbon Lab Global Pasture Watch Catalog. [Learn more about Publisher datasets](/earth-engine/datasets/publisher).
 






Catalog Owner
Land \& Carbon Lab Global Pasture Watch
Dataset Availability
2000\-01\-01T00:00:00Z–2023\-01\-01T00:00:00Z
Dataset Provider


[Land and Carbon Lab Global Pasture Watch](https://landcarbonlab.org/data/global-grassland-and-livestock-monitoring)


Contact
[Land \& Carbon Lab](https://landcarbonlab.org/subscribe)

Earth Engine Snippet


`ee.ImageCollection("projects/global-pasture-watch/assets/ggc-30m/v1/grassland_c")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/global-pasture-watch/projects_global-pasture-watch_assets_ggc-30m_v1_grassland_c)





Cadence
1 Year
Tags


[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[global](/earth-engine/datasets/tags/global)
[global\-pasture\-watch](/earth-engine/datasets/tags/global-pasture-watch)
[land](/earth-engine/datasets/tags/land)
[landcover](/earth-engine/datasets/tags/landcover)
[landuse](/earth-engine/datasets/tags/landuse)
[publisher\-dataset](/earth-engine/datasets/tags/publisher-dataset)
[vegetation](/earth-engine/datasets/tags/vegetation)








#### Description



This dataset provides global annual dominant class maps of grasslands 
(cultivated and natural/semi\-natural) from 2000 to 2022 at 30\-m spatial 
resolution. 
Produced by Land \&
Carbon Lab Global Pasture Watch initiative, the mapped grassland extent
includes any land cover type, which contains at least 30% of dry or wet
low vegetation, dominated by grasses and forbs (less than 3 meters) 
and a:


* maximum of 50% tree canopy cover (greater than 5 meters),
* maximum of 70% of other woody vegetation (scrubs and open shrubland), and
* maximum of 50% active cropland cover in mosaic landscapes of cropland
\& other vegetation.


The grassland extent is classified into two classes:
\- **Cultivated grassland**: Areas where grasses and other forage plants have
been intentionally planted and managed, as well as areas of native 
grassland\-type vegetation where they clearly exhibit active and
heavy management for specific human\-directed uses, such as directed
grazing of livestock.
\- **Natural/Semi\-natural grassland**: Relatively undisturbed native
grasslands/short\-height vegetation, such as steppes and tundra, 
as well as areas that have experienced varying degrees of human 
activity in the past, which may contain a mix of native and 
introduced species due to historical land use and natural processes. 
In general, they exhibit natural\-looking patterns of varied vegetation 
and clearly ordered hydrological relationships throughout the landscape.


The implemented methodology considered [GLAD Landsat ARD\-2 images](https://glad.umd.edu/ard) (processed into cloud\-free bi\-monthly 
aggregates, see [Consoli et al, 2024](https://doi.org/10.7717/peerj.18585)
), accompanied by climatic, landform and proximity covariates, 
spatiotemporal machine learning (per\-class Random Forest) and over 
2\.3 million reference samples (visually interpreted in Very High 
Resolution imagery). Custom probability thresholds (based on five\-fold 
spatial cross\-validation and balanced precision and recall values) 
were used to derive dominant class maps, 0\.32 and 0\.42 for 
cultivated and natural/semi\-natural grassland probability thresholds, respectively.


**Limitations:** Grassland extent is partly under\-predicted in southeastern
Africa (Zimbabwe and Mozambique) and in eastern Australia (shrublands and
woodlands of the Mulga ecoregion). Cropland is misclassified as grassland
in parts of northern Africa, the Arabian Peninsula, Western Australia, 
New Zealand, the center of Bolivia, and Mato Grosso state (Brazil). Due 
to the Landsat 7 SLC failure, regular stripes of grassland probabilities 
are visible at parcel\-level, particularly in the year 2012\. The usage of 
coarser resolution layers (accessibility maps and MODIS products) 
introduced curvilinear macroscopic errors (due to the downscaling 
strategy based on cubicspline) in Uruguay, Southwest Argentina, South 
of Angola and in the Sahel region in Africa. Users need to be aware 
of the limitations and known issues; whilst considering them 
carefully to ensure appropriate use of maps at this initial prediction 
stage. GPW is working actively to collect systematic feedback via the [Geo\-Wiki 
platform](https://www.geo-wiki.org), validate the current version 
and improve future versions of the dataset.


**For more information see [Parente et. al, 2024](http://doi.org/10.1038/s41597-024-04139-6),
[Zenodo](https://zenodo.org/records/13890401) and 
[https://github.com/wri/global\-pasture\-watch](https://github.com/wri/global-pasture-watch)**





### Bands


**Bands**




| Name | Min | Max | Pixel Size | Description |
| --- | --- | --- | --- | --- |
| `dominant_class` | 0 | 2 | Dominant class derived through Random Forest and probability maps. |


**dominant\_class Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#ffffff | Other |
| 1 | \#ff9916 | Cultivated grassland |
| 2 | \#ffcd73 | Natural/Semi\-natural grassland |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| version | INT | Product version |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Parente, L., Sloat, L., Mesquita, V., et al. (2024\) 
Global Pasture Watch \- Annual grassland class and extent 
maps at 30\-m spatial resolution (2000—2022\) (Version v1\) 
\[Data set]. Zenodo
[doi:https://doi.org/10\.5281/zenodo.13890401](https://doi.org/10.5281/zenodo.13890401)
* Parente, L., Sloat, L., Mesquita, V., et al. (2024\).
Annual 30\-m maps of global grassland class and extent (2000–2022\) 
based on spatiotemporal Machine Learning, Scientific Data.
[doi: http://doi.org/10\.1038/s41597\-024\-04139\-6](http://doi.org/10.1038/s41597-024-04139-6)





### DOIs


* [https://doi.org/10\.1038/s41597\-024\-04139\-6](https://doi.org/10.1038/s41597-024-04139-6)
* [https://doi.org/10\.5281/zenodo.13890401](https://doi.org/10.5281/zenodo.13890401)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
Map.setCenter(-49.265188,-16.602052,4);

vardomi_grassland=ee.ImageCollection(
"projects/global-pasture-watch/assets/ggc-30m/v1/grassland_c"
)
varvisParams={"opacity":1,"min":1,"max":2,"palette":["ff9916","ffcd73"]};

vardomi_grassland_2022=domi_grassland.filterDate('2022-01-01','2023-01-01').first();
Map.addLayer(
domi_grassland_2022.selfMask(),
visParams,'Dominant grassland class (2022)'
);

vardomi_grassland_2000=domi_grassland.filterDate('2000-01-01','2001-01-01').first();
Map.addLayer(
domi_grassland_2000.selfMask(),
visParams,'Dominant grassland class (2000)'
);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/global-pasture-watch/projects_global-pasture-watch_assets_ggc-30m_v1_grassland_c)


[GPW Annual Dominant Class of Grasslands v1](/earth-engine/datasets/catalog/projects_global-pasture-watch_assets_ggc-30m_v1_grassland_c)

This dataset provides global annual dominant class maps of grasslands (cultivated and natural/semi\-natural) from 2000 to 2022 at 30\-m spatial resolution. Produced by Land \& Carbon Lab Global Pasture Watch initiative, the mapped grassland extent includes any land cover type, which contains at least 30% of dry or wet low …

 projects/global\-pasture\-watch/assets/ggc\-30m/v1/grassland\_c,
 forest\-biomass,global,global\-pasture\-watch,land,landcover,landuse,publisher\-dataset,vegetation

2000\-01\-01T00:00:00Z/2023\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.13890401](https://doi.org/https://landcarbonlab.org/data/global-grassland-and-livestock-monitoring)
* [https://doi.org/10\.5281/zenodo.13890401](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/projects_global-pasture-watch_assets_ggc-30m_v1_grassland_c)









