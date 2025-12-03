



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD15A2H.061: Terra Leaf Area Index/FPAR 8\-Day Global 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================================








Dataset Availability
2000\-02\-18T00:00:00Z–2025\-07\-04T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MOD15A2H.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MOD15A2H")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD15A2H)





Cadence
8 Days
Tags


[8\-day](/earth-engine/datasets/tags/8-day)
[fpar](/earth-engine/datasets/tags/fpar)
[global](/earth-engine/datasets/tags/global)
[lai](/earth-engine/datasets/tags/lai)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[plant\-productivity](/earth-engine/datasets/tags/plant-productivity)
[terra](/earth-engine/datasets/tags/terra)
[usgs](/earth-engine/datasets/tags/usgs)
mod15a2h








#### Description



The MOD15A2H V6\.1 MODIS combined Leaf Area Index (LAI) and
Fraction of Photosynthetically Active Radiation (FPAR) product is an 8\-day
composite dataset at 500m resolution. The algorithm chooses the "best" pixel
available from all the acquisitions of the Terra sensor from within the 8\-day period.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/624/MOD15_User_Guide_V6.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/90/MOD15_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/61/MOD15A2H)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `Fpar_500m` | % | 0 | 100 | 0\.01 | Fraction of Photosynthetically Active Radiation |
| `Lai_500m` | Area fraction | 0 | 100 | 0\.1 | Leaf Area Index |
| `FparLai_QC` | None | 0 | 254 |  | Quality for LAI and FPAR |
| `FparExtra_QC` | None | 0 | 254 |  | Extra detail Quality for LAI and FPAR |
| `FparStdDev_500m` | % | 0 | 100 | 0\.01 | Standard deviation of FPAR |
| `LaiStdDev_500m` | Area fraction | 0 | 100 | 0\.1 | Standard deviation of LAI |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MOD15A2H.061](https://doi.org/10.5067/MODIS/MOD15A2H.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcollection=ee.ImageCollection('MODIS/061/MOD15A2H')
.filterDate('2019-01-01','2019-10-01');

varcolorizedVis={
min:0,
max:100,
palette:[
'ffffff','ce7e45','df923d','f1b555','fcd163','99b718','74a901',
'66a000','529400','3e8601','207401','056201','004c00','023b01',
'012e01','011d01','011301'
],
};

Map.setCenter(-10.88,40.94,2);
Map.addLayer(collection.select('Lai_500m'),colorizedVis,'Lai');
Map.addLayer(collection.select('Fpar_500m'),colorizedVis,'Fpar');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MOD15A2H)


[MOD15A2H.061: Terra Leaf Area Index/FPAR 8\-Day Global 500m](/earth-engine/datasets/catalog/MODIS_061_MOD15A2H)

The MOD15A2H V6\.1 MODIS combined Leaf Area Index (LAI) and Fraction of Photosynthetically Active Radiation (FPAR) product is an 8\-day composite dataset at 500m resolution. The algorithm chooses the "best" pixel available from all the acquisitions of the Terra sensor from within the 8\-day period. Documentation: User's Guide Algorithm Theoretical …

 MODIS/061/MOD15A2H,
 8\-day,fpar,global,lai,modis,nasa,plant\-productivity,terra,usgs

2000\-02\-18T00:00:00Z/2025\-07\-04T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MOD15A2H.061](https://doi.org/https://doi.org/10.5067/MODIS/MOD15A2H.061)
* [https://doi.org/10\.5067/MODIS/MOD15A2H.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD15A2H)









