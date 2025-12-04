



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Landsat Global Land Survey 1975


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================








Dataset Availability
1972\-07\-25T00:00:00Z–1983\-02\-20T00:00:00Z
Dataset Provider


[USGS](https://www.usgs.gov/core-science-systems/nli/landsat/global-land-survey-gls)



Earth Engine Snippet


`ee.ImageCollection("LANDSAT/GLS1975")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_GLS1975)





Tags


[global](/earth-engine/datasets/tags/global)
[gls](/earth-engine/datasets/tags/gls)
[landsat](/earth-engine/datasets/tags/landsat)
[radiance](/earth-engine/datasets/tags/radiance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The Global Land Survey (GLS) 1975 is a
global collection of imagery from the Landsat Multispectral
Scanner (MSS). Most scenes were acquired by Landsat 1\-3
in 1972\-1983\. A few gaps in the Landsat 1\-3 data
have been filled with scenes acquired by Landsat 4\-5 during the
years 1982\-1987\. These data contain 4 spectral bands:
Green, Red, an NIR band, and a SWIR band. In the typical
False\-color presentation, the images appear red because
the NIR band, displayed as red, highlights vegetation.





### Bands



**Pixel Size**
  
60 meters



**Bands**




| Name | Wavelength | Description |
| --- | --- | --- |
| `10` | 500\-600 nm | Green |
| `20` | 600\-700 nm | Red |
| `30` | 700\-800 nm | Near infrared |
| `40` | 800\-1100 nm | Short\-wavelength infrared |




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
* GLS 1975 image courtesy of the U.S. Geological Survey





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('LANDSAT/GLS1975');
varfalseColor=dataset.select(['30','20','10']);
varfalseColorVis={
gamma:1.6,
};
Map.setCenter(44.517,25.998,5);
Map.addLayer(falseColor,falseColorVis,'False Color');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_GLS1975)


[Landsat Global Land Survey 1975](/earth-engine/datasets/catalog/LANDSAT_GLS1975)

The Global Land Survey (GLS) 1975 is a global collection of imagery from the Landsat Multispectral Scanner (MSS). Most scenes were acquired by Landsat 1\-3 in 1972\-1983\. A few gaps in the Landsat 1\-3 data have been filled with scenes acquired by Landsat 4\-5 during the years 1982\-1987\. These data …

 LANDSAT/GLS1975,
 global,gls,landsat,radiance,satellite\-imagery,usgs

1972\-07\-25T00:00:00Z/1983\-02\-20T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








