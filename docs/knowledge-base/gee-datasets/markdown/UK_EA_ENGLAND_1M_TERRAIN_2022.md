



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

England 1m Composite DTM/DSM (Environment Agency)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================








Dataset Availability
2000\-06\-06T00:00:00Z–2022\-04\-02T00:00:00Z
Dataset Provider


[UK Environment Agency](https://www.data.gov.uk/dataset/f0db0249-f17b-4036-9e65-309148c97ce4/national-lidar-programme)



Earth Engine Snippet


`ee.Image("UK/EA/ENGLAND_1M_TERRAIN/2022")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UK/UK_EA_ENGLAND_1M_TERRAIN_2022)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[lidar](/earth-engine/datasets/tags/lidar)








#### Description



The LIDAR Composite DTM/DSM is a raster terrain model covering \~99% of
England at 1m spatial resolution, produced by the UK Environment Agency in
2022\. The model contains 3 bands of terrain data: a Digital Terrain Model
(DTM), a first return Digital Surface Model (DSM), and a last return DSM.


The DTM is produced from the last or only laser pulse returned to the
sensor. Surface objects are removed from the DSM, using bespoke algorithms
and manual editing of the data, to produce a terrain model of just the
surface. The DTM is derived from a combination of EA Time Stamped archive
and National LIDAR Program surveys, which have been merged and re\-sampled
to give the best possible coverage. Where repeat surveys have been
undertaken the newest, best resolution data is used. Where data was
resampled a bilinear interpolation was used before being merged. The 2022
LIDAR Composite contains surveys undertaken between 6th June 2000 and 2nd
April 2022\.


The first return DSM is produced from the first or only laser pulse returned
to the sensor and includes heights of objects, such as vehicles, buildings
and vegetation, as well as the terrain surface where the first or only
return was the ground. The first return DSM is derived from data captured as
part of the National LIDAR Program between 11 November 2016 and 5th May
2022\. This program divided England into \~300 blocks for survey over
continuous winters from 2016 onwards. These surveys are merged together to
create the first return LIDAR composite using a feathering technique along
the overlaps to remove any small differences in elevation between surveys.
Please refer to the data provider's metadata index catalogs which show for
any location which survey was used in the production of the LIDAR composite.
The first return DSM will not match in coverage or extent of the last return
DSM, as the last return DSM composite is produced from both the National
LIDAR Program and Timeseries surveys.


The last return DSM is produced from the last or only laser pulse returned
to the sensor and includes heights of objects, such as vehicles, buildings
and vegetation, as well as the terrain surface. The last return DTM is
derived from a combination of EA Time Stamped archive and National LIDAR
Program surveys, which have been merged and re\-sampled to give the best
possible coverage. Where repeat surveys have been undertaken the newest,
best resolution data is used. Where data was resampled a bilinear
interpolation was used before being merged. The 2022 LIDAR Composite
contains surveys undertaken between 6th June 2000 and 2nd April 2022\. Please
refer to the data provider's metadata index catalogs which show for any
location which survey was used in the production of the LIDAR composite.


The data is aligned to the OS National grid and presented in metres,
referenced to Ordinance Survey Newlyn and using the OSTN'15 transformation
method. All individual LIDAR surveys going into the production of the
composites had a vertical accuracy of \+/\-15cm root\-mean\-square error.





### Bands



**Pixel Size**
  
1 meter



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `dtm` | m | Digital Terrain Model |
| `dsm_first` | m | First Return Digital Surface Model |
| `dsm_last` | m | Last Return Digital Surface Model |




### Terms of Use


**Terms of Use**


You are free to: copy, publish, distribute and transmit the Information;
adapt the Information; exploit the Information commercially and
non\-commercially for example, by combining it with other Information, or
by including it in your own product or application.


You must acknowledge the source of the Information in your product or
application by including or linking to any attribution statement specified
by the Information Provider(s) and, where possible, provide a link to the
[license](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
Attribution statement: Environment Agency copyright and/or database right
2022\. All rights reserved.




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varimg=ee.Image('UK/EA/ENGLAND_1M_TERRAIN/2022').select('dtm');
varvisParam={
palette:['0000ff','00ffff','ffff00','ff0000','ffffff'],
max:630,
min:-5,
};

varlon=-2.5;
varlat=54;

Map.addLayer(img,visParam,'dtm');
Map.setCenter(lon,lat,5);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UK/UK_EA_ENGLAND_1M_TERRAIN_2022)


[England 1m Composite DTM/DSM (Environment Agency)](/earth-engine/datasets/catalog/UK_EA_ENGLAND_1M_TERRAIN_2022)

The LIDAR Composite DTM/DSM is a raster terrain model covering \~99% of England at 1m spatial resolution, produced by the UK Environment Agency in 2022\. The model contains 3 bands of terrain data: a Digital Terrain Model (DTM), a first return Digital Surface Model (DSM), and a last return DSM. …

 UK/EA/ENGLAND\_1M\_TERRAIN/2022,
 dem,elevation,elevation\-topography,lidar

2000\-06\-06T00:00:00Z/2022\-04\-02T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








