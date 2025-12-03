



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GHSL: Global built\-up surface 1975\-2030 (P2023A)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================








Dataset Availability
1975\-01\-01T00:00:00Z–2030\-12\-31T00:00:00Z
Dataset Provider


[EC JRC](https://ghsl.jrc.ec.europa.eu/ghs_buS2023.php)



Earth Engine Snippet


`ee.ImageCollection("JRC/GHSL/P2023A/GHS_BUILT_S")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_S)





Tags


[built](/earth-engine/datasets/tags/built)
[built\-environment](/earth-engine/datasets/tags/built-environment)
[builtup](/earth-engine/datasets/tags/builtup)
[copernicus](/earth-engine/datasets/tags/copernicus)
[ghsl](/earth-engine/datasets/tags/ghsl)
[jrc](/earth-engine/datasets/tags/jrc)
[landcover](/earth-engine/datasets/tags/landcover)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[population](/earth-engine/datasets/tags/population)
[sdg](/earth-engine/datasets/tags/sdg)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)
[settlement](/earth-engine/datasets/tags/settlement)
[urban](/earth-engine/datasets/tags/urban)








#### Description



This raster dataset depicts the distribution of built\-up surfaces,
expressed in square metres per 100 m grid cell.
The dataset measures:
a) the total built\-up surface, and b) the built\-up surface allocated to grid
cells of predominant non\-residential (NRES) use. Data are
spatially\-temporally interpolated or extrapolated from 1975 to 2030 in 5
year intervals.


The complete information about the GHSL main products can be
found in the [GHSL Data Package 2023 report](https://ghsl.jrc.ec.europa.eu/documents/GHSL_Data_Package_2023.pdf?t=1683540422)


The Global Human Settlement Layer (GHSL) project is supported by the
European Commission, Joint Research Centre, and Directorate\-General for
Regional and Urban Policy.





### Bands



**Pixel Size**
  
100 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `built_surface` | m^2 | Built\-up surface per grid cell |
| `built_surface_nres` | m^2 | Non\-residential built\-up surface per grid cell |




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
varimage_1975=ee.Image('JRC/GHSL/P2023A/GHS_BUILT_S/1975');
varbuilt_1975=image_1975.select('built_surface');
varimage_2020=ee.Image('JRC/GHSL/P2023A/GHS_BUILT_S/2020');
varbuilt_2020=image_2020.select('built_surface');
varvisParams={min:0.0,max:8000.0,palette:['000000','FFFFFF']};

Map.setCenter(77.156,28.6532,10);
Map.addLayer(built_1975,visParams,'Built-up surface [m2], 1975');
Map.addLayer(built_2020,visParams,'Built-up surface [m2], 2020');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_S)


[GHSL: Global built\-up surface 1975\-2030 (P2023A)](/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_S)

This raster dataset depicts the distribution of built\-up surfaces, expressed in square metres per 100 m grid cell. The dataset measures: a) the total built\-up surface, and b) the built\-up surface allocated to grid cells of predominant non\-residential (NRES) use. Data are spatially\-temporally interpolated or extrapolated from 1975 to 2030 …

 JRC/GHSL/P2023A/GHS\_BUILT\_S,
 built,built\-environment,builtup,copernicus,ghsl,jrc,landcover,landsat\-derived,population,sdg,sentinel2\-derived,settlement,urban

1975\-01\-01T00:00:00Z/2030\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.2905/9F06F36F\-4B11\-47EC\-ABB0\-4F8B7B1D72EA](https://doi.org/https://ghsl.jrc.ec.europa.eu/ghs_buS2023.php)
* [https://doi.org/10\.2905/9F06F36F\-4B11\-47EC\-ABB0\-4F8B7B1D72EA](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_S)









