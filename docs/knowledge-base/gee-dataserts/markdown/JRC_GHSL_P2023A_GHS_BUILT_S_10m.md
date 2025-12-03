



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GHSL: Global built\-up surface 10m (P2023A)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================








Dataset Availability
2018\-01\-01T00:00:00Z–2019\-01\-01T00:00:00Z
Dataset Provider


[EC JRC](https://ghsl.jrc.ec.europa.eu/ghs_buS2023.php)



Earth Engine Snippet


`ee.ImageCollection("JRC/GHSL/P2023A/GHS_BUILT_S_10m")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_S_10m)





Tags


[built](/earth-engine/datasets/tags/built)
[built\-environment](/earth-engine/datasets/tags/built-environment)
[builtup](/earth-engine/datasets/tags/builtup)
[copernicus](/earth-engine/datasets/tags/copernicus)
[ghsl](/earth-engine/datasets/tags/ghsl)
[jrc](/earth-engine/datasets/tags/jrc)
[landcover](/earth-engine/datasets/tags/landcover)
[population](/earth-engine/datasets/tags/population)
[sdg](/earth-engine/datasets/tags/sdg)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)
[settlement](/earth-engine/datasets/tags/settlement)
[urban](/earth-engine/datasets/tags/urban)








#### Description



This raster dataset depicts the distribution of built\-up surfaces,
expressed in square metres per 10 m grid cell, for 2018
as observed from the S2 image data.


The datasets measure:
a) the total built\-up surface, and b) the built\-up surface allocated to grid
cells of predominant non\-residential (NRES) use.


The complete information about the GHSL main products can be
found in the [GHSL Data Package 2023 report](https://ghsl.jrc.ec.europa.eu/documents/GHSL_Data_Package_2023.pdf?t=1683540422)


The Global Human Settlement Layer (GHSL) project is supported by the
European Commission, Joint Research Centre, and Directorate\-General for
Regional and Urban Policy.





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `built_surface` | m^2 | Built\-up surface per grid cell |
| `built_surface_nres` | None | Non\-residential built\-up class (NRES) |


**built\_surface\_nres Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | black | non\-NRES |
| 1 | magenta | NRES |




### Terms of Use


**Terms of Use**


The GHSL has been produced by the European Commission Joint Research Centre
as open and free data. Reuse is authorised, provided the source is
acknowledged. For more information, please read the use conditions ([European
Commission Reuse and Copyright Notice](https://ec.europa.eu/info/legal-notice_en)).




### Citations



Citations:
* Dataset : Pesaresi, Martino; Politis, Panagiotis (2023\): GHS\-BUILT\-S
R2023A \- GHS built\-up surface grid, derived from Sentinel2 composite and
Landsat, multitemporal (1975\-2030\). European Commission, Joint Research
Centre (JRC).
[PID: http://data.europa.eu/89h/9f06f36f\-4b11\-47ec\-abb0\-4f8b7b1d72ea](http://data.europa.eu/89h/9f06f36f-4b11-47ec-abb0-4f8b7b1d72ea)
[doi:10\.2905/9F06F36F\-4B11\-47EC\-ABB0\-4F8B7B1D72EA](https://doi.org/10.2905/9F06F36F-4B11-47EC-ABB0-4F8B7B1D72EA)
* Methodology : Pesaresi, Martino, Marcello Schiavina, Panagiotis Politis,
Sergio Freire, Katarzyna Krasnodebska,
Johannes H. Uhl, Alessandra Carioli, et al. (2024\). Advances on the
Global Human Settlement Layer by Joint Assessment of Earth Observation
and Population Survey Data. International Journal of Digital Earth 17(1\).
[doi:10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454).





### DOIs


* [https://doi.org/10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454)
* [https://doi.org/10\.2905/9F06F36F\-4B11\-47EC\-ABB0\-4F8B7B1D72EA](https://doi.org/10.2905/9F06F36F-4B11-47EC-ABB0-4F8B7B1D72EA)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varimage=ee.Image('JRC/GHSL/P2023A/GHS_BUILT_S_10m/2018');
varbuilt_total=image.select('built_surface');
varbuilt_nres=image.select('built_surface_nres');
built_nres=built_nres.updateMask(built_nres.gt(0));

varvisParams={min:0.0,max:100.0,palette:['000000','FFFFFF']};

Map.setCenter(31.23,30.05,12);
Map.addLayer(built_total,visParams,'Built-up surface [m^2], 2018');
Map.addLayer(
built_nres,{palette:['magenta']},
'Non-residential built-up surface, 2018');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_S_10m)


[GHSL: Global built\-up surface 10m (P2023A)](/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_S_10m)

This raster dataset depicts the distribution of built\-up surfaces, expressed in square metres per 10 m grid cell, for 2018 as observed from the S2 image data. The datasets measure: a) the total built\-up surface, and b) the built\-up surface allocated to grid cells of predominant non\-residential (NRES) use. The …

 JRC/GHSL/P2023A/GHS\_BUILT\_S\_10m,
 built,built\-environment,builtup,copernicus,ghsl,jrc,landcover,population,sdg,sentinel2\-derived,settlement,urban

2018\-01\-01T00:00:00Z/2019\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.2905/9F06F36F\-4B11\-47EC\-ABB0\-4F8B7B1D72EA](https://doi.org/https://ghsl.jrc.ec.europa.eu/ghs_buS2023.php)
* [https://doi.org/10\.2905/9F06F36F\-4B11\-47EC\-ABB0\-4F8B7B1D72EA](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_S_10m)









