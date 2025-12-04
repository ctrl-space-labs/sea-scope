



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MERIT DEM: Multi\-Error\-Removed Improved\-Terrain DEM


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================








Dataset Availability
1987\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[Dai Yamazaki (University of Tokyo)](http://hydro.iis.u-tokyo.ac.jp/~yamadai/MERIT_DEM/index.html)



Earth Engine Snippet


`ee.Image("MERIT/DEM/v1_0_3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MERIT/MERIT_DEM_v1_0_3)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[merit](/earth-engine/datasets/tags/merit)
[topography](/earth-engine/datasets/tags/topography)








#### Description



MERIT DEM a high accuracy global DEM at 3 arc second resolution (\~90 m at
the equator) produced by eliminating major error components from existing DEMs
(NASA SRTM3 DEM, JAXA AW3D DEM, Viewfinder Panoramas DEM).


MERIT DEM separates absolute bias, stripe noise, speckle
noise and tree height bias using multiple satellite datasets and filtering techniques.
After the error removal, land areas mapped with 2 m or better vertical accuracy
were increased from 39% to 58%. Significant improvements were found in flat regions
where height errors larger than topography variability, and landscapes such as
river networks and hill\-valley structures became clearly represented.


'MERIT DEM was developed by processing the following products as baseline data:


* [NASA SRTM3 DEM v2\.1](https://dds.cr.usgs.gov/srtm/version2_1/SRTM3)
* [JAXA AW3D \- 30 m DEM v1](https://www.eorc.jaxa.jp/ALOS/en/aw3d30/index.htm)
* [Viewfinder Panoramas DEM](http://www.viewfinderpanoramas.org/dem3.html)


In addition to the above baseline dems, these products were used as supplementary data:


* [NASA\-NSIDC ICESat/GLAS GLA14 data](https://nsidc.org/data/gla14)
* [U\-Maryland Landsat forest cover data](https://glad.earthengine.app/view/global-forest-change)
* [NASA Global Forest height data](https://www.nasa.gov/topics/earth/features/forest-height-map.html)
* [JAMSTEC/U\-Tokyo G3WBM water body data](http://hydro.iis.u-tokyo.ac.jp/%7Eyamadai/G3WBM/index.html)





### Bands


**Bands**




| Name | Pixel Size | Description |
| --- | --- | --- |
| `dem` | Elevation in meters, referenced to EGM96 geoid model. |




### Terms of Use


**Terms of Use**


Citation to the paper is adequate if you simply use MERIT DEM. If you
asked for help for additional handling/editing of the dataset, or if your research
outcome highly depends on the product, the developer would request co\-authorship.


MERIT DEM is licensed under a Creative Commons "CC\-BY\-NC 4\.0" or
Open Data Commons "Open Database License (ODbL 1\.0\)". With a dual license, you
can choose an appropriate license for you.


To view a copy of these license, please visit:


* [CC\-BY\-NC 4\.0 license](https://creativecommons.org/licenses/by-nc/4.0/): Non\-Commercial Use with less restriction.
* [ODbL 1\.0 license](https://opendatacommons.org/licenses/odbl/summary/): Commercial Use is OK, but the derived data based on MERIT
DEM should be made publicly available under the same ODbL license. For
example, if you create a flood hazard map using MERIT DEM and you would like to
provide a COMMERCIAL service based on that, you have to make the hazard map
PUBLICLY AVAILABLE under OdBL license.


Note that the above license terms are applied to the "derived data" based
on MERIT DEM, while they are not applied to "produced work / artwork" created
with MERIT DEM (such as figures in a journal paper). The users may have a
copyright of the artwork and may assign any license, when the produced work
is not considered as "derived data".


By downloading and using the data the user agrees to the terms and
conditions of one of these licenses. Notwithstanding this free license, we ask
users to refrain from redistributing the data in whole in its original format
on other websites without the explicit written permission from the authors.


The copyright of MERIT DEM is held by the developers, 2018, all rights reserved.




### Citations



Citations:
* Yamazaki D., D. Ikeshima, R. Tawatari, T. Yamaguchi, F. O'Loughlin, J.C. Neal,
C.C. Sampson, S. Kanae \& P.D. Bates. A high accuracy map of global
terrain elevations. Geophysical Research Letters, vol.44, pp.5844\-5853, 2017\.


[doi:10\.1002/2017GL072874](https://doi.org/10.1002/2017GL072874)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('MERIT/DEM/v1_0_3');

varvisualization={
bands:['dem'],
min:-3,
max:18,
palette:[
'000000','478fcd','86c58e','afc35e',
'8f7131','b78d4f','e2b8a6','ffffff']
};

Map.setCenter(90.301,23.052,10);

Map.addLayer(dataset,visualization,'Elevation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MERIT/MERIT_DEM_v1_0_3)


[MERIT DEM: Multi\-Error\-Removed Improved\-Terrain DEM](/earth-engine/datasets/catalog/MERIT_DEM_v1_0_3)

MERIT DEM a high accuracy global DEM at 3 arc second resolution (\~90 m at the equator) produced by eliminating major error components from existing DEMs (NASA SRTM3 DEM, JAXA AW3D DEM, Viewfinder Panoramas DEM). MERIT DEM separates absolute bias, stripe noise, speckle noise and tree height bias using multiple …

 MERIT/DEM/v1\_0\_3,
 dem,elevation,elevation\-topography,merit,topography

1987\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-60 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








