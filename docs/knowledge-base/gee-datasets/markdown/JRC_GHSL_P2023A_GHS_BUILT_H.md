



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GHSL: Global building height 2018 (P2023A)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================








Dataset Availability
2018\-01\-01T00:00:00Z–2018\-12\-31T00:00:00Z
Dataset Provider


[EC JRC](https://ghsl.jrc.ec.europa.eu/ghs_buH2023.php)



Earth Engine Snippet


`ee.ImageCollection("JRC/GHSL/P2023A/GHS_BUILT_H")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_H)





Tags


[alos](/earth-engine/datasets/tags/alos)
[building](/earth-engine/datasets/tags/building)
[built](/earth-engine/datasets/tags/built)
[built\-environment](/earth-engine/datasets/tags/built-environment)
[builtup](/earth-engine/datasets/tags/builtup)
[copernicus](/earth-engine/datasets/tags/copernicus)
[dem](/earth-engine/datasets/tags/dem)
[ghsl](/earth-engine/datasets/tags/ghsl)
[height](/earth-engine/datasets/tags/height)
[jrc](/earth-engine/datasets/tags/jrc)
[population](/earth-engine/datasets/tags/population)
[sdg](/earth-engine/datasets/tags/sdg)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)
[srtm](/earth-engine/datasets/tags/srtm)
[urban](/earth-engine/datasets/tags/urban)








#### Description



This spatial raster dataset depicts the global distribution of building
heights at a resolution of 100 m, referred to the year 2018\. The input data
used to predict building heights are the ALOS Global Digital Surface Model
(30 m), the NASA Shuttle Radar Topographic Mission data (30 m), and a global
Sentinel\-2 image composite from L1C data for the period 2017\-2018\.


More information about the GHSL data products can be found in the
[GHSL Data Package 2023 report](https://ghsl.jrc.ec.europa.eu/documents/GHSL_Data_Package_2023.pdf?t=1683540422),
where the building height layer is referred to as the Average Net Building
Height (ANBH).


The Global Human Settlement Layer (GHSL) project is supported by the
European Commission, Joint Research Centre, and Directorate\-General for
Regional and Urban Policy.





### Bands



**Pixel Size**
  
100 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `built_height` | m | Average building height per grid cell |




### Terms of Use


**Terms of Use**


The GHSL has been produced by the European Commission Joint Research Centre
as open and free data. Reuse is authorised, provided the source is
acknowledged. For more information, please read the use conditions ([European
Commission Reuse and Copyright Notice](https://ec.europa.eu/info/legal-notice_en)).




### Citations



Citations:
* Dataset : Pesaresi, Martino; Politis, Panagiotis (2023\): GHS\-BUILT\-H
R2023A \- GHS building height, derived from AW3D30, SRTM30, and Sentinel2
composite (2018\). European Commission, Joint Research Centre (JRC)
[PID: http://data.europa.eu/89h/85005901\-3a49\-48dd\-9d19\-6261354f56fe](http://data.europa.eu/89h/85005901-3a49-48dd-9d19-6261354f56fe)
[doi:10\.2905/85005901\-3A49\-48DD\-9D19\-6261354F56FE](https://doi.org/10.2905/85005901-3A49-48DD-9D19-6261354F56FE)
* Methodology : Pesaresi, Martino, Marcello Schiavina, Panagiotis Politis,
Sergio Freire, Katarzyna Krasnodebska,
Johannes H. Uhl, Alessandra Carioli, et al. (2024\). Advances on the
Global Human Settlement Layer by Joint Assessment of Earth Observation
and Population Survey Data. International Journal of Digital Earth 17(1\).
[doi:10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454).





### DOIs


* [https://doi.org/10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454)
* [https://doi.org/10\.2905/85005901\-3A49\-48DD\-9D19\-6261354F56FE](https://doi.org/10.2905/85005901-3A49-48DD-9D19-6261354F56FE)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varimage=ee.Image("JRC/GHSL/P2023A/GHS_BUILT_H/2018");
varbuilt=image.select('built_height');
varvisParams={
min:0.0,
max:12.0,
palette:['000000','0d0887','7e03a8','cc4778','f89540','f0f921'],
};

Map.setCenter(2.349014,48.864716,10);
Map.addLayer(built,visParams,'Average building height [m], 2018');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_H)


[GHSL: Global building height 2018 (P2023A)](/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_H)

This spatial raster dataset depicts the global distribution of building heights at a resolution of 100 m, referred to the year 2018\. The input data used to predict building heights are the ALOS Global Digital Surface Model (30 m), the NASA Shuttle Radar Topographic Mission data (30 m), and a …

 JRC/GHSL/P2023A/GHS\_BUILT\_H,
 alos,building,built,built\-environment,builtup,copernicus,dem,ghsl,height,jrc,population,sdg,sentinel2\-derived,srtm,urban

2018\-01\-01T00:00:00Z/2018\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.2905/85005901\-3A49\-48DD\-9D19\-6261354F56FE](https://doi.org/https://ghsl.jrc.ec.europa.eu/ghs_buH2023.php)
* [https://doi.org/10\.2905/85005901\-3A49\-48DD\-9D19\-6261354F56FE](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_H)









