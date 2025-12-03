



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Copernicus Global Land Cover Layers: CGLS\-LC100 Collection 3


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================================================








Dataset Availability
2015\-01\-01T00:00:00Z–2019\-12\-31T23:59:59Z
Dataset Provider


[Copernicus](https://land.copernicus.eu/global/lcviewer)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/Landcover/100m/Proba-V-C3/Global")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_Landcover_100m_Proba-V-C3_Global)





Tags


[copernicus](/earth-engine/datasets/tags/copernicus)
[eea](/earth-engine/datasets/tags/eea)
[esa](/earth-engine/datasets/tags/esa)
[eu](/earth-engine/datasets/tags/eu)
[landcover](/earth-engine/datasets/tags/landcover)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[proba](/earth-engine/datasets/tags/proba)
[probav](/earth-engine/datasets/tags/probav)
[vito](/earth-engine/datasets/tags/vito)








#### Description



The Copernicus Global Land Service (CGLS) is earmarked as a component of
the Land service to operate a multi\-purpose service component that provides
a series of bio\-geophysical products on the status and evolution of land
surface at global scale.


The Dynamic Land Cover map at 100 m resolution (CGLS\-LC100\) is a new product
in the portfolio of the CGLS and delivers a global land cover map at 100 m
spatial resolution. The CGLS Land Cover product provides a primary land
cover scheme. Next to these discrete classes, the product also includes
continuous field layers for all basic land cover classes that provide
proportional estimates for vegetation/ground cover for the land cover types.
This continuous classification scheme may depict areas of heterogeneous
land cover better than the standard classification scheme and, as such,
can be tailored for application use (e.g. forest monitoring, crop monitoring,
biodiversity and conservation, monitoring environment and security in Africa,
climate modelling, etc.).


These consistent Land Cover maps (v3\.0\.1\) are provided for the period
2015\-2019 over the entire Globe, derived from the PROBA\-V 100 m time\-series, a
database of high quality land cover training sites and several ancillary
datasets, reaching an accuracy of 80% at Level1 over all years. It is planned
to provide yearly updates from 2020 through the use of a Sentinel time\-series.


See also:


* [Algorithm Theoretical Basis Document](https://doi.org/10.5281/zenodo.3938968)
* [Product User Manual](https://doi.org/10.5281/zenodo.3938963)
* [Validation Report](https://doi.org/10.5281/zenodo.3938974)





### Bands



**Pixel Size**
  
100 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `discrete_classification` | None | 0 | 200 | Land cover classification |
| `discrete_classification-proba` | % | 0 | 100 | Quality indicator (classification probability) of the discrete classification |
| `forest_type` | None | 0 | 5 | Forest type for all pixels with tree percentage vegetation cover bigger than 1 % |
| `bare-coverfraction` | % | 0 | 100 | Percent vegetation cover for bare\-sparse\-vegetation land cover class |
| `crops-coverfraction` | % | 0 | 100 | Percent vegetation cover for cropland land cover class |
| `grass-coverfraction` | % | 0 | 100 | Percent vegetation cover for herbaceous vegetation land cover class |
| `moss-coverfraction` | % | 0 | 100 | Percent vegetation cover for moss and lichen land cover class |
| `shrub-coverfraction` | % | 0 | 100 | Percent vegetation cover for shrubland land cover class |
| `tree-coverfraction` | % | 0 | 100 | Percent vegetation cover for forest land cover class |
| `snow-coverfraction` | % | 0 | 100 | Percent ground cover for snow and ice land cover class |
| `urban-coverfraction` | % | 0 | 100 | Percent ground cover for built\-up land cover class |
| `water-permanent-coverfraction` | % | 0 | 100 | Percent ground cover for permanent water land cover class |
| `water-seasonal-coverfraction` | % | 0 | 100 | Percent ground cover for seasonal water land cover class |
| `data-density-indicator` | None | 0 | 100 | Data density indicator for algorithm input data |
| `change-confidence` | None | 0 | 3 | This layer is only provided for years after the BaseYear 2015\.* 0 \- No change. No change in discrete class between year and previous year detected. * 1 \- Potential change. BFASTmon detected break in second half of NRT year \- potential change. * 2 \- Medium confidence. Imprint of urban, permanent water, snow or wetland OR change detected by BFAST but HMM model didn't confirm this break in higher resolution OR change detected by BFASTmon in the first half of NRT year. * 3 \- High confidence. BFAST detected a change and HMM confirmed this change in higher resolution. |


**discrete\_classification Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#282828 | Unknown. No or not enough satellite data available. |
| 20 | \#ffbb22 | Shrubs. Woody perennial plants with persistent and woody stems and without any defined main stem being less than 5 m tall. The shrub foliage can be either evergreen or deciduous. |
| 30 | \#ffff4c | Herbaceous vegetation. Plants without persistent stem or shoots above ground and lacking definite firm structure. Tree and shrub cover is less than 10 %. |
| 40 | \#f096ff | Cultivated and managed vegetation / agriculture. Lands covered with temporary crops followed by harvest and a bare soil period (e.g., single and multiple cropping systems). Note that perennial woody crops will be classified as the appropriate forest or shrub land cover type. |
| 50 | \#fa0000 | Urban / built up. Land covered by buildings and other man\-made structures. |
| 60 | \#b4b4b4 | Bare / sparse vegetation. Lands with exposed soil, sand, or rocks and never has more than 10 % vegetated cover during any time of the year. |
| 70 | \#f0f0f0 | Snow and ice. Lands under snow or ice cover throughout the year. |
| 80 | \#0032c8 | Permanent water bodies. Lakes, reservoirs, and rivers. Can be either fresh or salt\-water bodies. |
| 90 | \#0096a0 | Herbaceous wetland. Lands with a permanent mixture of water and herbaceous or woody vegetation. The vegetation can be present in either salt, brackish, or fresh water. |
| 100 | \#fae6a0 | Moss and lichen. |
| 111 | \#58481f | Closed forest, evergreen needle leaf. Tree canopy \>70 %, almost all needle leaf trees remain green all year. Canopy is never without green foliage. |
| 112 | \#009900 | Closed forest, evergreen broad leaf. Tree canopy \>70 %, almost all broadleaf trees remain green year round. Canopy is never without green foliage. |
| 113 | \#70663e | Closed forest, deciduous needle leaf. Tree canopy \>70 %, consists of seasonal needle leaf tree communities with an annual cycle of leaf\-on and leaf\-off periods. |
| 114 | \#00cc00 | Closed forest, deciduous broad leaf. Tree canopy \>70 %, consists of seasonal broadleaf tree communities with an annual cycle of leaf\-on and leaf\-off periods. |
| 115 | \#4e751f | Closed forest, mixed. |
| 116 | \#007800 | Closed forest, not matching any of the other definitions. |
| 121 | \#666000 | Open forest, evergreen needle leaf. Top layer\- trees 15\-70 % and second layer\- mixed of shrubs and grassland, almost all needle leaf trees remain green all year. Canopy is never without green foliage. |
| 122 | \#8db400 | Open forest, evergreen broad leaf. Top layer\- trees 15\-70 % and second layer\- mixed of shrubs and grassland, almost all broadleaf trees remain green year round. Canopy is never without green foliage. |
| 123 | \#8d7400 | Open forest, deciduous needle leaf. Top layer\- trees 15\-70 % and second layer\- mixed of shrubs and grassland, consists of seasonal needle leaf tree communities with an annual cycle of leaf\-on and leaf\-off periods. |
| 124 | \#a0dc00 | Open forest, deciduous broad leaf. Top layer\- trees 15\-70 % and second layer\- mixed of shrubs and grassland, consists of seasonal broadleaf tree communities with an annual cycle of leaf\-on and leaf\-off periods. |
| 125 | \#929900 | Open forest, mixed. |
| 126 | \#648c00 | Open forest, not matching any of the other definitions. |
| 200 | \#000080 | Oceans, seas. Can be either fresh or salt\-water bodies. |


**forest\_type Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#282828 | Unknown |
| 1 | \#666000 | Evergreen needle leaf |
| 2 | \#009900 | Evergreen broad leaf |
| 3 | \#70663e | Deciduous needle leaf |
| 4 | \#a0dc00 | Deciduous broad leaf |
| 5 | \#929900 | Mix of forest types |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| discrete\_classification\_class\_names | STRING\_LIST | Land cover class names |
| discrete\_classification\_class\_palette | STRING\_LIST | Land cover class palette |
| discrete\_classification\_class\_values | INT\_LIST | Value of the land cover classification. |
| forest\_type\_class\_names | STRING\_LIST | forest cover class names |
| forest\_type\_class\_palette | STRING\_LIST | forest cover class palette |
| forest\_type\_class\_values | INT\_LIST | forest cover class values |




### Terms of Use


**Terms of Use**


As official product of the global component of the Copernicus Land Service,
access to this land cover dataset is fully free and open to all users.




### Citations



Citations:
* Buchhorn, M. ; Lesiv, M. ; Tsendbazar, N. \- E. ; Herold, M. ; Bertels, L. ; Smets, B.
Copernicus Global Land Cover Layers\-Collection 2\. Remote Sensing 2020, 12Volume 108, 1044\.
[doi:10\.3390/rs12061044](https://doi.org/10.3390/rs12061044)
* Buchhorn, M., Smets, B., Bertels, L., Roo, B. D., Lesiv, M., Tsendbazar,
N.\-E., Herold, M., \& Fritz, S. (2020\). *Copernicus Global Land
Service: Land Cover 100m: collection 3: epoch 2017: Globe* (Version
V3\.0\.1\) \[Data set]. Zenodo.
* Buchhorn, M., Smets, B., Bertels, L., Roo, B. D., Lesiv, M., Tsendbazar,
N.\-E., Herold, M., \& Fritz, S. (2020\). *Copernicus Global Land
Service: Land Cover 100m: collection 3: epoch 2018: Globe* (Version
V3\.0\.1\) \[Data set]. Zenodo.
* Buchhorn, M., Smets, B., Bertels, L., Roo, B. D., Lesiv, M., Tsendbazar,
N.\-E., Herold, M., \& Fritz, S. (2020\). *Copernicus Global Land
Service: Land Cover 100m: collection 3: epoch 2015: Globe* (Version
V3\.0\.1\) \[Data set]. Zenodo.
* Buchhorn, M., Smets, B., Bertels, L., Roo, B. D., Lesiv, M., Tsendbazar,
N.\-E., Herold, M., \& Fritz, S. (2020\). *Copernicus Global Land
Service: Land Cover 100m: collection 3: epoch 2019: Globe* (Version
V3\.0\.1\) \[Data set]. Zenodo.





### DOIs


* [https://doi.org/10\.5281/ZENODO.3518036](https://doi.org/10.5281/ZENODO.3518036)
* [https://doi.org/10\.5281/ZENODO.3518038](https://doi.org/10.5281/ZENODO.3518038)
* [https://doi.org/10\.5281/ZENODO.3939038](https://doi.org/10.5281/ZENODO.3939038)
* [https://doi.org/10\.5281/ZENODO.3939050](https://doi.org/10.5281/ZENODO.3939050)
* [https://doi.org/10\.5281/zenodo.3518026](https://doi.org/10.5281/zenodo.3518026)
* [https://doi.org/10\.5281/zenodo.3518036](https://doi.org/10.5281/zenodo.3518036)
* [https://doi.org/10\.5281/zenodo.3518038](https://doi.org/10.5281/zenodo.3518038)
* [https://doi.org/10\.5281/zenodo.3939038](https://doi.org/10.5281/zenodo.3939038)
* [https://doi.org/10\.5281/zenodo.3939050](https://doi.org/10.5281/zenodo.3939050)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('COPERNICUS/Landcover/100m/Proba-V-C3/Global/2019')
.select('discrete_classification');

Map.setCenter(-88.6,26.4,1);

Map.addLayer(dataset,{},'Land Cover');
```




Python setup


See the [Python Environment](/earth-engine/guides/python_install) page for information on the Python API and using
 `geemap` for interactive development.



```
importee
importgeemap.coreasgeemap
```


### Colab (Python)



```
dataset = ee.Image('COPERNICUS/Landcover/100m/Proba-V-C3/Global/2019').select(
    'discrete_classification'
)

m = geemap.Map()
m.set_center(-88.6, 26.4, 1)
m.add_layer(dataset, {}, 'Land Cover')
m
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_Landcover_100m_Proba-V-C3_Global)


[Copernicus Global Land Cover Layers: CGLS\-LC100 Collection 3](/earth-engine/datasets/catalog/COPERNICUS_Landcover_100m_Proba-V-C3_Global)

The Copernicus Global Land Service (CGLS) is earmarked as a component of the Land service to operate a multi\-purpose service component that provides a series of bio\-geophysical products on the status and evolution of land surface at global scale. The Dynamic Land Cover map at 100 m resolution (CGLS\-LC100\) is …

 COPERNICUS/Landcover/100m/Proba\-V\-C3/Global,
 copernicus,eea,esa,eu,landcover,landuse\-landcover,proba,probav,vito

2015\-01\-01T00:00:00Z/2019\-12\-31T23:59:59Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.3939050](https://doi.org/https://land.copernicus.eu/global/lcviewer)
* [https://doi.org/10\.5281/zenodo.3939050](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_Landcover_100m_Proba-V-C3_Global)









