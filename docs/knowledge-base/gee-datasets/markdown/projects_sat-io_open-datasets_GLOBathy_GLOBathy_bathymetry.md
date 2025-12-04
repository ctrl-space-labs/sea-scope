



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GLOBathy Global lakes bathymetry dataset


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================









info


 This dataset is part of a Community Catalog, and not managed by Google Earth Engine.
 
 Contact gee\-community\-catalog@googlegroups.com
 
 for bugs or [view more datasets](https://developers.google.com/earth-engine/datasets/community/sat-io)
 from the Awesome GEE Community Catalog Catalog. [Learn more about Community datasets](/earth-engine/datasets/community).
 






Catalog Owner
Awesome GEE Community Catalog
Dataset Availability
2022\-01\-26T00:00:00Z–2022\-01\-26T23:59:00Z
Dataset Provider


[Bahram Khazaei](https://springernature.figshare.com/articles/dataset/GLOBathy_Bathymetry_Rasters/13404635)



Earth Engine Snippet


`ee.Image("projects/sat-io/open-datasets/GLOBathy/GLOBathy_bathymetry")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/sat-io/projects_sat-io_open-datasets_GLOBathy_GLOBathy_bathymetry)





Tags


[community\-dataset](/earth-engine/datasets/tags/community-dataset)
[hydrology](/earth-engine/datasets/tags/hydrology)
[sat\-io](/earth-engine/datasets/tags/sat-io)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
bathymetry
lake








#### Description



The GLObal Bathymetric (GLOBathy) dataset, comprising data on over 1\.4 million waterbodies globally, has been meticulously developed to harmonize with the widely recognized HydroLAKES dataset. Utilizing a sophisticated Geographic Information System (GIS)\-based framework, GLOBathy constructs detailed bathymetric maps by integrating maximum depth estimates and geometric/geophysical attributes sourced from HydroLAKES. Ensuring data accuracy and reliability, GLOBathy undergoes stringent validation procedures involving 1,503 waterbodies and a diverse range of observed data sources. Consequently, GLOBathy stands as a robust and comprehensive dataset for hydrography and aquatic sciences, offering invaluable resources for researchers and professionals in these fields.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `b1` | m | 0\* | 1548\.53\* | Maximum depth |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


The dataset is released under an assumed CC0 1\.0 Universal (CC0 1\.0\) Public Domain Dedication. The organizations responsible for generating and funding this dataset make no representations of any kind including, but not limited to the warranties of merchantability or fitness for a particular use, nor are any such warranties to be implied with respect to the data.




### Citations



Citations:
* Khazaei, Bahram; Read, Laura K; Casali, Matthew; Sampson, Kevin M; Yates, David N (2022\): GLOBathy Bathymetry Rasters. figshare. Dataset. https://doi.org/10\.6084/m9\.figshare.c.5243309\.v1





### DOIs


* [https://doi.org/10\.6084/m9\.figshare.c.5243309\.v1](https://doi.org/10.6084/m9.figshare.c.5243309.v1)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varglobathy=ee.Image(
"projects/sat-io/open-datasets/GLOBathy/GLOBathy_bathymetry"
);

varpalettes=require("users/samapriya/utils:palettes");

// Use these visualization parameters, customized by location.
varvisParams={min:1,max:700,palette:palettes.extra.blkred};

// Note that the visualization image doesn't require visualization parameters.
Map.addLayer(globathy,visParams,"Globathy Bathymetry (m)");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/sat-io/projects_sat-io_open-datasets_GLOBathy_GLOBathy_bathymetry)


[GLOBathy Global lakes bathymetry dataset](/earth-engine/datasets/catalog/projects_sat-io_open-datasets_GLOBathy_GLOBathy_bathymetry)

The GLObal Bathymetric (GLOBathy) dataset, comprising data on over 1\.4 million waterbodies globally, has been meticulously developed to harmonize with the widely recognized HydroLAKES dataset. Utilizing a sophisticated Geographic Information System (GIS)\-based framework, GLOBathy constructs detailed bathymetric maps by integrating maximum depth estimates and geometric/geophysical attributes sourced from HydroLAKES. Ensuring …

 projects/sat\-io/open\-datasets/GLOBathy/GLOBathy\_bathymetry,
 community\-dataset,hydrology,sat\-io,surface\-ground\-water

2022\-01\-26T00:00:00Z/2022\-01\-26T23:59:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.6084/m9\.figshare.c.5243309\.v1](https://doi.org/https://springernature.figshare.com/articles/dataset/GLOBathy_Bathymetry_Rasters/13404635)
* [https://doi.org/10\.6084/m9\.figshare.c.5243309\.v1](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/projects_sat-io_open-datasets_GLOBathy_GLOBathy_bathymetry)









