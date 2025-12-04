



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

SoilGrids250m 2\.0 \- Volumetric Water Content


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================








Dataset Availability
1905\-04\-01T00:00:00Z–2016\-07\-05T00:00:00Z
Dataset Provider


[ISRIC \- World Soil Information](https://www.isric.org/explore/soilgrids)



Earth Engine Snippet


`ee.ImageCollection("ISRIC/SoilGrids250m/v2_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISRIC/ISRIC_SoilGrids250m_v2_0)





Tags


[soil](/earth-engine/datasets/tags/soil)
[soil\-moisture](/earth-engine/datasets/tags/soil-moisture)
[water](/earth-engine/datasets/tags/water)








#### Description



Volumetric Water Content at 10kPa, 33kPa, and 1500kPa suction in
10^\-3 cm^3/cm^3 (0\.1 v% or 1 mm/m) at 6 standard depths (0\-5cm, 5\-15cm,
15\-30cm, 30\-60cm, 60\-100cm, 100\-200cm). Predictions were derived using a
digital soil mapping approach based on Quantile Random Forest, drawing on a
global compilation of soil profile data and environmental layers.
This dataset includes predictions for three different suction levels,
providing insights into soil water availability.


The dataset is organized into three main assets: `/wv0010`, `/wv0033`,
and `/wv1500`. Each of these assets contains bands representing soil
properties at different depths and quantiles. The band names follow the
pattern `val_<depth>_<quantile>`, where `depth` represents a soil depth
range (e.g., 0\-5cm, 5\-15cm, 15\-30cm, 30\-60cm, 60\-100cm, 100\-200cm) and
`quantile` represents a statistical measure (e.g., mean, Q0\.05, Q0\.5,
Q0\.95\).


The uncertainty band is not yet included. It is possible to calculate
the uncertainty from the ratio between the inter\-quantile range
(90% prediction interval width) and the median: (Q0\.95\-Q0\.05\)/Q0\.50\.


Documentation:


* [Scientific Paper](https://www.sciencedirect.com/science/article/pii/S2095633922000636?via%3Dihub)





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `val_0_5cm_mean` | cm^3/cm^3 | Mean Volumetric Water Content (0\-5cm depth) |
| `val_0_5cm_Q0_05` | cm^3/cm^3 | Q0\.05 Volumetric Water Content (0\-5cm depth) |
| `val_0_5cm_Q0_5` | cm^3/cm^3 | Q0\.5 Volumetric Water Content (0\-5cm depth) |
| `val_0_5cm_Q0_95` | cm^3/cm^3 | Q0\.95 Volumetric Water Content (0\-5cm depth) |
| `val_5_15cm_mean` | cm^3/cm^3 | Mean Volumetric Water Content (5\-15cm depth) |
| `val_5_15cm_Q0_05` | cm^3/cm^3 | Q0\.05 Volumetric Water Content (5\-15cm depth) |
| `val_5_15cm_Q0_5` | cm^3/cm^3 | Q0\.5 Volumetric Water Content (5\-15cm depth) |
| `val_5_15cm_Q0_95` | cm^3/cm^3 | Q0\.95 Volumetric Water Content (5\-15cm depth) |
| `val_15_30cm_mean` | cm^3/cm^3 | Mean Volumetric Water Content (15\-30cm depth) |
| `val_15_30cm_Q0_05` | cm^3/cm^3 | Q0\.05 Volumetric Water Content (15\-30cm depth) |
| `val_15_30cm_Q0_5` | cm^3/cm^3 | Q0\.5 Volumetric Water Content (15\-30cm depth) |
| `val_15_30cm_Q0_95` | cm^3/cm^3 | Q0\.95 Volumetric Water Content (15\-30cm depth) |
| `val_30_60cm_mean` | cm^3/cm^3 | Mean Volumetric Water Content (30\-60cm depth) |
| `val_30_60cm_Q0_05` | cm^3/cm^3 | Q0\.05 Volumetric Water Content (30\-60cm depth) |
| `val_30_60cm_Q0_5` | cm^3/cm^3 | Q0\.5 Volumetric Water Content (30\-60cm depth) |
| `val_30_60cm_Q0_95` | cm^3/cm^3 | Q0\.95 Volumetric Water Content (30\-60cm depth) |
| `val_60_100cm_mean` | cm^3/cm^3 | Mean Volumetric Water Content (60\-100cm depth) |
| `val_60_100cm_Q0_05` | cm^3/cm^3 | Q0\.05 Volumetric Water Content (60\-100cm depth) |
| `val_60_100cm_Q0_5` | cm^3/cm^3 | Q0\.5 Volumetric Water Content (60\-100cm depth) |
| `val_60_100cm_Q0_95` | cm^3/cm^3 | Q0\.95 Volumetric Water Content (60\-100cm depth) |
| `val_100_200cm_mean` | cm^3/cm^3 | Mean Volumetric Water Content (100\-200cm depth) |
| `val_100_200cm_Q0_05` | cm^3/cm^3 | Q0\.05 Volumetric Water Content (100\-200cm depth) |
| `val_100_200cm_Q0_5` | cm^3/cm^3 | Q0\.5 Volumetric Water Content (100\-200cm depth) |
| `val_100_200cm_Q0_95` | cm^3/cm^3 | Q0\.95 Volumetric Water Content (100\-200cm depth) |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Global mapping of volumetric water retention at 100, 330 and 15000 cm
suction using the WoSIS database
Turek M.E., Poggio L., Batjes N.H., Armindo R.A., de Jong van Lier Q.,
de Sousa L., Heuvelink G.B.M. (2023\)
International Soil and Water Conservation Research, 11 (2\), pp. 225\-239\.





### DOIs


* [https://doi.org/10\.1016/j.iswcr.2022\.08\.001](https://doi.org/10.1016/j.iswcr.2022.08.001)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('ISRIC/SoilGrids250m/v2_0/wv0010').select('val_0_5cm_Q0_95');

Map.setCenter(-105.25,52.5,3);

Map.addLayer(
dataset,{
min:-0.061,
max:0.636,
palette:[
'#440154','#482878','#3E4A89','#31688E','#26828E','#1F9E89',
'#35B779','#6DCD59','#B4DE2C','#FDE725'
]
},
'SoilGrids250m 10kPa Q0.95 0-5cm');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISRIC/ISRIC_SoilGrids250m_v2_0)


[SoilGrids250m 2\.0 \- Volumetric Water Content](/earth-engine/datasets/catalog/ISRIC_SoilGrids250m_v2_0)

Volumetric Water Content at 10kPa, 33kPa, and 1500kPa suction in 10^\-3 cm^3/cm^3 (0\.1 v% or 1 mm/m) at 6 standard depths (0\-5cm, 5\-15cm, 15\-30cm, 30\-60cm, 60\-100cm, 100\-200cm). Predictions were derived using a digital soil mapping approach based on Quantile Random Forest, drawing on a global compilation of soil profile data …

 ISRIC/SoilGrids250m/v2\_0,
 soil,soil\-moisture,water

1905\-04\-01T00:00:00Z/2016\-07\-05T00:00:00Z



 \-56 \-180 84 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1016/j.iswcr.2022\.08\.001](https://doi.org/https://www.isric.org/explore/soilgrids)
* [https://doi.org/10\.1016/j.iswcr.2022\.08\.001](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/ISRIC_SoilGrids250m_v2_0)









