



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GHSL: Global settlement characteristics (10 m) 2018 (P2023A)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================================








Dataset Availability
2018\-01\-01T00:00:00Z–2018\-12\-31T00:00:00Z
Dataset Provider


[EC JRC](https://ghsl.jrc.ec.europa.eu/ghs_buC2023.php)



Earth Engine Snippet


`ee.ImageCollection("JRC/GHSL/P2023A/GHS_BUILT_C")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_C)





Tags


[building](/earth-engine/datasets/tags/building)
[built](/earth-engine/datasets/tags/built)
[builtup](/earth-engine/datasets/tags/builtup)
[copernicus](/earth-engine/datasets/tags/copernicus)
[ghsl](/earth-engine/datasets/tags/ghsl)
[height](/earth-engine/datasets/tags/height)
[jrc](/earth-engine/datasets/tags/jrc)
[landcover](/earth-engine/datasets/tags/landcover)
[population](/earth-engine/datasets/tags/population)
[roads](/earth-engine/datasets/tags/roads)
[sdg](/earth-engine/datasets/tags/sdg)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)
[settlement](/earth-engine/datasets/tags/settlement)
[urban](/earth-engine/datasets/tags/urban)








#### Description



This spatial raster dataset delineates human settlements at 10 m resolution,
and describes their inner characteristics in terms of the functional and
height\-related components of the built environment.


More information about the GHSL data products can be found in the [GHSL Data
Package 2023 report](https://ghsl.jrc.ec.europa.eu/documents/GHSL_Data_Package_2023.pdf?t=1683540422)


The Global Human Settlement Layer (GHSL) project is supported by the European
Commission, Joint Research Centre, and Directorate\-General for Regional and
Urban Policy.





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Description |
| --- | --- |
| `built_characteristics` | Settlement characteristics |


**built\_characteristics Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#718c6c | open spaces, low vegetation surfaces |
| 2 | \#8ad86b | open spaces, medium vegetation surfaces |
| 3 | \#c1ffa1 | open spaces, high vegetation surfaces |
| 4 | \#01b7ff | open spaces, water surfaces |
| 5 | \#ffd501 | open spaces, road surfaces |
| 11 | \#d28200 | built spaces, residential, building height \<\= 3m |
| 12 | \#fe5900 | built spaces, residential, 3m \< building height \<\= 6m |
| 13 | \#ff0101 | built spaces, residential, 6m \< building height \<\= 15m |
| 14 | \#ce001b | built spaces, residential, 15m \< building height \<\= 30m |
| 15 | \#7a000a | built spaces, residential, building height \> 30m |
| 21 | \#ff9ff4 | built spaces, non\-residential, building height \<\= 3m |
| 22 | \#ff67e4 | built spaces, non\-residential, 3m \< building height \<\= 6m |
| 23 | \#f701ff | built spaces, non\-residential, 6m \< building height \<\= 15m |
| 24 | \#a601ff | built spaces, non\-residential, 15m \< building height \<\= 30m |
| 25 | \#6e00fe | built spaces, non\-residential, building height \> 30m |




### Terms of Use


**Terms of Use**


The GHSL has been produced by the European Commission Joint Research Centre
as open and free data. Reuse is authorised, provided the source is
acknowledged. For more information, please read the use conditions ([European
Commission Reuse and Copyright Notice](https://ec.europa.eu/info/legal-notice_en)).




### Citations



Citations:
* Dataset : Pesaresi, Martino; Politis, Panagiotis (2023\): GHS\-BUILT\-C
R2023A \- GHS Settlement Characteristics, derived from Sentinel2
composite (2018\) and other GHS R2023A data. European Commission,
Joint Research Centre (JRC)
[PID: http://data.europa.eu/89h/3c60ddf6\-0586\-4190\-854b\-f6aa0edc2a30](http://data.europa.eu/89h/3c60ddf6-0586-4190-854b-f6aa0edc2a30)
[doi:10\.2905/3c60ddf6\-0586\-4190\-854b\-f6aa0edc2a30](https://doi.org/10.2905/3c60ddf6-0586-4190-854b-f6aa0edc2a30)
* Methodology : Pesaresi, Martino, Marcello Schiavina, Panagiotis Politis,
Sergio Freire, Katarzyna Krasnodebska,
Johannes H. Uhl, Alessandra Carioli, et al. (2024\). Advances on the
Global Human Settlement Layer by Joint Assessment of Earth Observation
and Population Survey Data. International Journal of Digital Earth 17(1\).
[doi:10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454).





### DOIs


* [https://doi.org/10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454)
* [https://doi.org/10\.2905/3c60ddf6\-0586\-4190\-854b\-f6aa0edc2a30](https://doi.org/10.2905/3c60ddf6-0586-4190-854b-f6aa0edc2a30)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varimage=ee.Image("JRC/GHSL/P2023A/GHS_BUILT_C/2018");
varbuilt=image.select('built_characteristics');
Map.setCenter(77.58,12.97,13);
Map.addLayer(built,{},'Settlement_characteristics (2018)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_C)


[GHSL: Global settlement characteristics (10 m) 2018 (P2023A)](/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_C)

This spatial raster dataset delineates human settlements at 10 m resolution, and describes their inner characteristics in terms of the functional and height\-related components of the built environment. More information about the GHSL data products can be found in the GHSL Data Package 2023 report The Global Human Settlement Layer …

 JRC/GHSL/P2023A/GHS\_BUILT\_C,
 building,built,builtup,copernicus,ghsl,height,jrc,landcover,population,roads,sdg,sentinel2\-derived,settlement,urban

2018\-01\-01T00:00:00Z/2018\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.2905/3c60ddf6\-0586\-4190\-854b\-f6aa0edc2a30](https://doi.org/https://ghsl.jrc.ec.europa.eu/ghs_buC2023.php)
* [https://doi.org/10\.2905/3c60ddf6\-0586\-4190\-854b\-f6aa0edc2a30](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_C)









