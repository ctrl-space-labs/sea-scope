



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GHSL: Global population surfaces 1975\-2030 (P2023A)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================








Dataset Availability
1975\-01\-01T00:00:00Z–2030\-12\-31T00:00:00Z
Dataset Provider


[EC JRC](https://ghsl.jrc.ec.europa.eu/ghs_pop2023.php)



Earth Engine Snippet


`ee.ImageCollection("JRC/GHSL/P2023A/GHS_POP")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_POP)





Tags


[ghsl](/earth-engine/datasets/tags/ghsl)
[jrc](/earth-engine/datasets/tags/jrc)
[population](/earth-engine/datasets/tags/population)
[sdg](/earth-engine/datasets/tags/sdg)
ciesin\-derived








#### Description



This raster dataset depicts the spatial distribution of residential
population, expressed as the absolute number of inhabitants of the cell.
Residential population estimates between 1975 and 2020 in 5\-year intervals
and projections to 2025 and 2030 derived from CIESIN GPWv4\.11 were
disaggregated from census or administrative units to grid cells, informed by
the distribution, volume, and classification of built\-up area as mapped in
the [global GHSL built\-up surface layers](https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_S)
per epoch.


More information about the GHSL main products can be found in the
[GHSL Data Package 2023 report](https://ghsl.jrc.ec.europa.eu/documents/GHSL_Data_Package_2023.pdf?t=1683540422)


The Global Human Settlement Layer (GHSL) project is supported by the
European Commission, Joint Research Center, and Directorate\-General for
Regional and Urban Policy.





### Bands



**Pixel Size**
  
100 meters



**Bands**




| Name | Description |
| --- | --- |
| `population_count` | Population count by epoch |




### Terms of Use


**Terms of Use**


The GHSL has been produced by the European Commission Joint Research Centre
as open and free data. Reuse is authorised, provided the source is
acknowledged. For more information, please read the use conditions ([European
Commission Reuse and Copyright Notice](https://ec.europa.eu/info/legal-notice_en)).




### Citations



Citations:
* Dataset : Schiavina, Marcello; Freire, Sergio; Alessandra Carioli;
MacManus, Kytt (2023\): GHS\-POP R2023A \- GHS population grid
multitemporal (1975\-2030\). European Commission, Joint Research Centre
(JRC)
[PID: http://data.europa.eu/89h/2ff68a52\-5b5b\-4a22\-8f40\-c41da8332cfe](http://data.europa.eu/89h/2ff68a52-5b5b-4a22-8f40-c41da8332cfe)
[doi:10\.2905/2FF68A52\-5B5B\-4A22\-8F40\-C41DA8332CFE](https://doi.org/10.2905/2FF68A52-5B5B-4A22-8F40-C41DA8332CFE)
* Methodology : Pesaresi, Martino, Marcello Schiavina, Panagiotis Politis,
Sergio Freire, Katarzyna Krasnodebska,
Johannes H. Uhl, Alessandra Carioli, et al. (2024\). Advances on the
Global Human Settlement Layer by Joint Assessment of Earth Observation
and Population Survey Data. International Journal of Digital Earth 17(1\).
[doi:10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454).





### DOIs


* [https://doi.org/10\.1080/17538947\.2024\.2390454](https://doi.org/10.1080/17538947.2024.2390454)
* [https://doi.org/10\.2905/2FF68A52\-5B5B\-4A22\-8F40\-C41DA8332CFE](https://doi.org/10.2905/2FF68A52-5B5B-4A22-8F40-C41DA8332CFE)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varbaseChange=
[{featureType:'all',stylers:[{saturation:-100},{lightness:45}]}];
Map.setOptions('baseChange',{'baseChange':baseChange});
varimage1975=ee.Image('JRC/GHSL/P2023A/GHS_POP/1975');
varimage1990=ee.Image('JRC/GHSL/P2023A/GHS_POP/1990');
varimage2020=ee.Image('JRC/GHSL/P2023A/GHS_POP/2020');
varpopulationCountVis={
min:0.0,
max:100.0,
palette:
['000004','320A5A','781B6C','BB3654','EC6824','FBB41A','FCFFA4']
};
Map.setCenter(8,48,7);
image1975=image1975.updateMask(image1975.gt(0));
image1990=image1990.updateMask(image1990.gt(0));
image2020=image2020.updateMask(image2020.gt(0));
Map.addLayer(image1975,populationCountVis,'Population count, 1975');
Map.addLayer(image1990,populationCountVis,'Population count, 1990');
Map.addLayer(image2020,populationCountVis,'Population count, 2020');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GHSL_P2023A_GHS_POP)


[GHSL: Global population surfaces 1975\-2030 (P2023A)](/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_POP)

This raster dataset depicts the spatial distribution of residential population, expressed as the absolute number of inhabitants of the cell. Residential population estimates between 1975 and 2020 in 5\-year intervals and projections to 2025 and 2030 derived from CIESIN GPWv4\.11 were disaggregated from census or administrative units to grid cells, …

 JRC/GHSL/P2023A/GHS\_POP,
 ghsl,jrc,population,sdg

1975\-01\-01T00:00:00Z/2030\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.2905/2FF68A52\-5B5B\-4A22\-8F40\-C41DA8332CFE](https://doi.org/https://ghsl.jrc.ec.europa.eu/ghs_pop2023.php)
* [https://doi.org/10\.2905/2FF68A52\-5B5B\-4A22\-8F40\-C41DA8332CFE](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_POP)









