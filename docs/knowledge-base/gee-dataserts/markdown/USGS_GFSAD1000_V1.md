



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GFSAD1000: Cropland Extent 1km Multi\-Study Crop Mask, Global Food\-Support Analysis Data


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2010\-01\-01T00:00:00Z
Dataset Provider


[Global Food Security\-support Analysis Data at 30m Project (GFSAD30\)](https://geography.wr.usgs.gov/science/croplands/)



Earth Engine Snippet


`ee.Image("USGS/GFSAD1000_V1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GFSAD1000_V1)





Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[crop](/earth-engine/datasets/tags/crop)
[landcover](/earth-engine/datasets/tags/landcover)
[usgs](/earth-engine/datasets/tags/usgs)
gfsad








#### Description



The GFSAD is a NASA\-funded project to provide high\-resolution global
cropland data and their water use that contributes towards global food
security in the twenty\-first century. The GFSAD products are derived
through multi\-sensor remote sensing data (e.g., Landsat, MODIS, AVHRR),
secondary data, and field\-plot data and aims at documenting cropland
dynamics.


At a nominal 1km scale, V0\.1 provides the spatial distribution of a
disaggregated five\-class global cropland extent map derived from four
major studies: Thenkabail et al. (2009a, 2011\), Pittman et al. (2010\),
Yu et al. (2013\), and Friedl et al. (2010\). V1\.0 is a 5\-class product that
provides information on global cropland extent and irrigated versus rainfed
cropping. There is no crop type or crop type dominance information. Cropping
intensity (single, double, triple, and continuous crops) can be obtained for
every pixel using time\-series remote sensing data. The GFSAD1000 nominal
2010 product was created with data from 2007 to 2012\.





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `landcover` | 0 | 9 | Crop mask class descriptions |


**landcover Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | black | Non\-croplands |
| 1 | orange | Croplands: irrigation major |
| 2 | brown | Croplands: irrigation minor |
| 3 | darkseagreen | Croplands: rainfed |
| 4 | green | Croplands: rainfed, minor fragments |
| 5 | yellow | Croplands: rainfed, very minor fragments |




### Terms of Use


**Terms of Use**


Most U.S. Geological Survey (USGS) information resides
in the public domain and may be used without restriction. Additional
information on [Acknowledging or Crediting USGS as Information
Source](https://www.usgs.gov/information-policies-and-instructions/acknowledging-or-crediting-usgs)
is available.




### Citations



Citations:
* [Teluguntla, P., Thenkabail, P.S., Xiong, J., Gumma, M.K., Giri, C., Milesi,
C., Ozdogan, M., Congalton, R., Tilton, J., Sankey, T.R., Massey, R.,
Phalke, A., and Yadav, K. 2014\. Global Cropland Area Database (GCAD)
derived from Remote Sensing in Support of Food Security in the Twenty\-first
Century: Current Achievements and Future Possibilities. Chapter 7, Vol. II.
Land Resources: Monitoring, Modelling, and Mapping, Remote Sensing Handbook
edited by Prasad S. Thenkabail. In Press.](https://lpdaac.usgs.gov/documents/173/GFSAD1K_ATBD.pdf)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('USGS/GFSAD1000_V1');
varcropMask=dataset.select('landcover');
varcropMaskVis={
min:0.0,
max:5.0,
palette:['black','orange','brown','02a50f','green','yellow'],
};
Map.setCenter(-17.22,13.72,2);
Map.addLayer(cropMask,cropMaskVis,'Crop Mask');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GFSAD1000_V1)


[GFSAD1000: Cropland Extent 1km Multi\-Study Crop Mask, Global Food\-Support Analysis Data](/earth-engine/datasets/catalog/USGS_GFSAD1000_V1)

The GFSAD is a NASA\-funded project to provide high\-resolution global cropland data and their water use that contributes towards global food security in the twenty\-first century. The GFSAD products are derived through multi\-sensor remote sensing data (e.g., Landsat, MODIS, AVHRR), secondary data, and field\-plot data and aims at documenting cropland …

 USGS/GFSAD1000\_V1,
 agriculture,crop,landcover,usgs

2010\-01\-01T00:00:00Z/2010\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








