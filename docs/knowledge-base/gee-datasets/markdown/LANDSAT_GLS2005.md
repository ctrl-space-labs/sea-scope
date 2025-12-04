



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Landsat Global Land Survey 2005, Landsat 5\+7 scenes


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================








Dataset Availability
2003\-07\-29T00:00:00Z–2008\-07\-29T00:00:00Z
Dataset Provider


[USGS](https://www.usgs.gov/landsat-missions/global-land-survey-gls)



Earth Engine Snippet


`ee.ImageCollection("LANDSAT/GLS2005")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_GLS2005)





Tags


[gls](/earth-engine/datasets/tags/gls)
[landsat](/earth-engine/datasets/tags/landsat)
[radiance](/earth-engine/datasets/tags/radiance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The GLS2005 data set is a collection of 9500
orthorectified leaf\-on medium\-resolution satellite images collected between
2004 and 2007 and covering the Earth's land masses. GLS2005 uses mainly Landsat
5 and gap\-filled Landsat 7 data with EO\-1 ALI and Terra ASTER data filling in
any data holes.


This dataset contains images from just the L5 TM and L7 ETM\+ sensors, and only the 6 bands that those two sensors have in common: 10, 20, 30, 40, 50, and 70\.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Wavelength | Description |
| --- | --- | --- |
| `10` | 0\.45 \- 0\.52 μm | Blue |
| `20` | 0\.52 \- 0\.60 μm | Green |
| `30` | 0\.63 \- 0\.69 μm | Red |
| `40` | 0\.76 \- 0\.90 μm | Near infrared |
| `50` | 1\.55 \- 1\.75 μm | Shortwave infrared 1 |
| `70` | 2\.08 \- 2\.35 μm | Shortwave infrared 2 |




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




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('LANDSAT/GLS2005');
vartrueColor321=dataset.select(['30','20','10']);
Map.setCenter(6.746,46.529,6);
Map.addLayer(trueColor321,{},'True Color (321)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_GLS2005)


[Landsat Global Land Survey 2005, Landsat 5\+7 scenes](/earth-engine/datasets/catalog/LANDSAT_GLS2005)

The GLS2005 data set is a collection of 9500 orthorectified leaf\-on medium\-resolution satellite images collected between 2004 and 2007 and covering the Earth's land masses. GLS2005 uses mainly Landsat 5 and gap\-filled Landsat 7 data with EO\-1 ALI and Terra ASTER data filling in any data holes. This dataset contains …

 LANDSAT/GLS2005,
 gls,landsat,radiance,satellite\-imagery,usgs

2003\-07\-29T00:00:00Z/2008\-07\-29T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








