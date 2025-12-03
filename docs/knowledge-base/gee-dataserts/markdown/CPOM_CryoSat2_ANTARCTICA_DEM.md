



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

CryoSat\-2 Antarctica 1km DEM


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================








Dataset Availability
2010\-07\-01T00:00:00Z–2016\-07\-01T00:00:00Z
Dataset Provider


[CPOM](http://www.cpom.ucl.ac.uk/csopr/icesheets2/dems.php?ais_subject=dem&user_type=normal)



Earth Engine Snippet


`ee.Image("CPOM/CryoSat2/ANTARCTICA_DEM")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CPOM/CPOM_CryoSat2_ANTARCTICA_DEM)





Tags


[antarctica](/earth-engine/datasets/tags/antarctica)
[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[polar](/earth-engine/datasets/tags/polar)
cpom
cryosat\-2








#### Description



This dataset is a digital elevation model (DEM) of the
Antarctic ice sheet and ice shelves based on
observations recorded by the CryoSat\-2 satellite
radar altimeter between July 2010 and July 2016\.


The DEM is formed from spatio\-temporal fits to elevation
measurements accumulated within 1, 2, and 5 km grid cells,
and is posted at the modal resolution of 1 km. The median
and root mean square difference between the DEM and 2\.3\*107;
airborne laser altimeter measurements acquired during
NASA Operation IceBridge campaigns are \-0\.30 and 13\.50 m,
respectively.


The DEM uncertainty rises in regions of high slope,
especially where elevation measurements were acquired in
low\-resolution mode; taking this into account, we estimate
the average accuracy to be 9\.5 m.





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `elevation` | m | Antarctic ice sheet and ice shelf elevation. |
| `data_composition` | None | Data processing method of elevation per grid cell. |
| `slope` | deg | Slope derived from elevation gradient. |
| `z_smoothed` | m | Smoothed version of elevation model using a median filter. |
| `z_uncertainty` | m | Certainty of elevation model derived from RMS of elevation residuals in observed grid cells and the kriging variance error in interpolated grid cells. |


**data\_composition Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#000000 | interpolated |
| 1 | \#cbcbcb | 1 km fit |
| 2 | \#377eb7 | resampled 2 km fit |
| 3 | \#e2191b | resampled 5 km fit |




### Terms of Use


**Terms of Use**


[proprietary](/earth-engine/datasets/catalog/Use%20a%20custom%20URL%20for%20the%20non-standard%20license)




### Citations



Citations:
* Slater, T., Shepherd, A., McMillan, M., Muir, A., Gilbert, L.,
Hogg, A. E., Konrad, H. and Parrinello, T.: A new Digital Elevation
Model of Antarctica derived from CryoSat\-2 altimetry, The Cryosphere,
[doi:10\.5194/tc\-2017\-223](https://doi.org/10.5194/tc-2017-223), 2018





### DOIs


* [https://doi.org/10\.5194/tc\-2017\-223](https://doi.org/10.5194/tc-2017-223)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('CPOM/CryoSat2/ANTARCTICA_DEM');

varvisualization={
bands:['elevation'],
min:0.0,
max:4000.0,
palette:['001fff','00ffff','fbff00','ff0000']
};

Map.setCenter(17.0,-76.0,3);

Map.addLayer(dataset,visualization,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CPOM/CPOM_CryoSat2_ANTARCTICA_DEM)


[CryoSat\-2 Antarctica 1km DEM](/earth-engine/datasets/catalog/CPOM_CryoSat2_ANTARCTICA_DEM)

This dataset is a digital elevation model (DEM) of the Antarctic ice sheet and ice shelves based on observations recorded by the CryoSat\-2 satellite radar altimeter between July 2010 and July 2016\. The DEM is formed from spatio\-temporal fits to elevation measurements accumulated within 1, 2, and 5 km grid …

 CPOM/CryoSat2/ANTARCTICA\_DEM,
 antarctica,dem,elevation,elevation\-topography,polar

2010\-07\-01T00:00:00Z/2016\-07\-01T00:00:00Z



 \-88 \-180 \-60 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5194/tc\-2017\-223](https://doi.org/http://www.cpom.ucl.ac.uk/csopr/icesheets2/dems.php?ais_subject=dem&user_type=normal)
* [https://doi.org/10\.5194/tc\-2017\-223](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/CPOM_CryoSat2_ANTARCTICA_DEM)









