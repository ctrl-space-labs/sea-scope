



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GHSL: Global building volume 1975\-2030 (P2023A)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================








Dataset Availability
1975\-01\-01T00:00:00Z–2030\-12\-31T00:00:00Z
Dataset Provider


[EC JRC](https://ghsl.jrc.ec.europa.eu/ghs_buV2023.php)



Earth Engine Snippet


`ee.ImageCollection("JRC/GHSL/P2023A/GHS_BUILT_V")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_V)





Tags


[alos](/earth-engine/datasets/tags/alos)
[building](/earth-engine/datasets/tags/building)
[built\-environment](/earth-engine/datasets/tags/built-environment)
[copernicus](/earth-engine/datasets/tags/copernicus)
[dem](/earth-engine/datasets/tags/dem)
[ghsl](/earth-engine/datasets/tags/ghsl)
[jrc](/earth-engine/datasets/tags/jrc)
[population](/earth-engine/datasets/tags/population)
[sdg](/earth-engine/datasets/tags/sdg)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)
[srtm](/earth-engine/datasets/tags/srtm)
[urban](/earth-engine/datasets/tags/urban)








#### Description



This raster dataset depicts the global distribution of building volume,
expressed in cubic metres per 100 m grid cell. The dataset measures the
total building volume and the building volume allocated to grid cells of
predominant non\-residential (NRES) use. Estimates are based on the [built\-up
surface](https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_S)
and [building height](https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_H)
products.


More information about the GHSL data products can be found in the [GHSL Data
Package 2023 report](https://ghsl.jrc.ec.europa.eu/documents/GHSL_Data_Package_2023.pdf?t=1683540422)


The Global Human Settlement Layer (GHSL) project is supported by the
European Commission, Joint Research Centre, and Directorate\-General for
Regional and Urban Policy.





### Bands



**Pixel Size**
  
100 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `built_volume_total` | m^3 | Total building volume per grid cell |
| `built_volume_nres` | m^3 | Non\-residential building volume per grid cell |




### Terms of Use


**Terms of Use**


The GHSL has been produced by the European Commission Joint Research Centre
as open and free data. Reuse is authorised, provided the source is
acknowledged. For more information, please read the use conditions ([European
Commission Reuse and Copyright Notice](https://ec.europa.eu/info/legal-notice_en)).




### Citations



Citations:
* Dataset : Pesaresi, Martino; Politis, Panagiotis (2023\):GHS\-BUILT\-V
R2023A \- GHS built\-up volume grids derived from joint assessment of
Sentinel2, Landsat, and global DEM data, multitemporal (1975\-2030\).
European Commission, Joint Research Centre (JRC)
[PID: http://data.europa.eu/89h/ab2f107a\-03cd\-47a3\-85e5\-139d8ec63283](http://data.europa.eu/89h/ab2f107a-03cd-47a3-85e5-139d8ec63283)
[doi:10\.2905/AB2F107A\-03CD\-47A3\-85E5\-139D8EC63283](https://doi.org/10.2905/AB2F107A-03CD-47A3-85E5-139D8EC63283)
* Methodology : Pesaresi, Martino, Marcello Schiavina, Panagiotis Politis,
Sergio Freire, Katarzyna Krasnodebska,
Johannes H. Uhl, Alessandra Carioli, et al. (2024\). Advances on the
Global Human Settlement Layer by Joint Assessment of Earth Observation
and Population Survey Data. International Journal of Digital Earth 17(1\).
[doi:10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454).





### DOIs


* [https://doi.org/10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454)
* [https://doi.org/10\.2905/AB2F107A\-03CD\-47A3\-85E5\-139D8EC63283](https://doi.org/10.2905/AB2F107A-03CD-47A3-85E5-139D8EC63283)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varimage_1975=ee.Image('JRC/GHSL/P2023A/GHS_BUILT_V/1975');
varimage_2020=ee.Image('JRC/GHSL/P2023A/GHS_BUILT_V/2020');
varvolume_total_1975=image_1975.select('built_volume_total');
varvolume_total_2020=image_2020.select('built_volume_total');


varvisParams={
min:0,
max:80000,
palette:['000004','51127c','b73779','fc8961','fcfdbf'],
};

Map.setCenter(77.156,28.6532,10);
Map.addLayer(volume_total_1975,visParams,'Total building volume [m3], 1975');
Map.addLayer(volume_total_2020,visParams,'Total building volume [m3], 2020');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_BUILT_V)


[GHSL: Global building volume 1975\-2030 (P2023A)](/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_V)

This raster dataset depicts the global distribution of building volume, expressed in cubic metres per 100 m grid cell. The dataset measures the total building volume and the building volume allocated to grid cells of predominant non\-residential (NRES) use. Estimates are based on the built\-up surface and building height products. …

 JRC/GHSL/P2023A/GHS\_BUILT\_V,
 alos,building,built\-environment,copernicus,dem,ghsl,jrc,population,sdg,sentinel2\-derived,srtm,urban

1975\-01\-01T00:00:00Z/2030\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.2905/AB2F107A\-03CD\-47A3\-85E5\-139D8EC63283](https://doi.org/https://ghsl.jrc.ec.europa.eu/ghs_buV2023.php)
* [https://doi.org/10\.2905/AB2F107A\-03CD\-47A3\-85E5\-139D8EC63283](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_V)









