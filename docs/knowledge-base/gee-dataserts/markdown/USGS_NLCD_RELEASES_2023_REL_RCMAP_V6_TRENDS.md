



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

RCMAP Rangeland Trends for Component Timeseries (1985\-2023\), v06


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================================








Dataset Availability
1985\-01\-01T00:00:00Z–2023\-12\-31T00:00:00Z
Dataset Provider


[United States Geological Survey and Bureau of Land Management](https://www.mrlc.gov/)



Earth Engine Snippet


`ee.Image("USGS/NLCD_RELEASES/2023_REL/RCMAP/V6/TRENDS")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_NLCD_RELEASES_2023_REL_RCMAP_V6_TRENDS)





Tags


[climate\-change](/earth-engine/datasets/tags/climate-change)
[disturbance](/earth-engine/datasets/tags/disturbance)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[nlcd](/earth-engine/datasets/tags/nlcd)
[rangeland](/earth-engine/datasets/tags/rangeland)
[trends](/earth-engine/datasets/tags/trends)








#### Description



The RCMAP (Rangeland Condition Monitoring Assessment and Projection)
dataset quantifies the percent cover of rangeland components across
western North America using Landsat imagery from 1985\-2023\. The RCMAP
product suite consists of ten fractional components: annual herbaceous,
bare ground, herbaceous, litter, non\-sagebrush shrub, perennial herbaceous,
sagebrush, shrub, tree, and shrub height in addition to the temporal
trends of each component. Several enhancements were made to the RCMAP
process relative to prior generations. First, high\-resolution training
was revised using an improved neural\-net classifier and modelling approach.
These data serve as foundation to the RCMAP approach. The training
database was further improved by incorporating additional datasets. Next,
the Landsat compositing approach was improved to better capture the range
of conditions from across each year and through time. These composites are
based on Collection 2 Landsat data with improved geolocation accuracy and
dynamic range. Finally, the Canadian portion of the sagebrush biome was
included, which expanded the study area by 29,199 km2\.


Processing efficiency has been increased using open\-source software and
USGS High\-Performance Computing (HPC) resources. The mapping area included
eight regions which were subsequently mosaicked. These data can be used to
answer critical questions regarding the influence of climate change and
the suitability of management practices. Component products can be
downloaded at
[Multi\-Resolution Land Characteristics Consortium](https://www.mrlc.gov/data).


The temporal patterns were assessed in each RCMAP component with two
approaches, 1\) linear trends and 2\) a breaks and stable states method
with an 8\-year temporal moving window based on structural change at the
pixel level. Linear trend products include slope and p\-value calculated
from least squares linear regression. The slope represents the average
percent cover change per year over the times\-series and the p\-value
reflects the confidence of change in each pixel. The structural change
method partitions the time\-series into segments of similar slope values,
with statistically significant breakpoints indicating perturbations to the
prior trajectory. The break point trends analysis suite relies on
structural break methods, resulting in the identification of the number
and timing of breaks in the time\-series, and the significance of each
segment. The following statistics were produced: 1\) for each component,
each year, the presence/absence of breaks, 2\) the slope, p\-value, and
standard error of the segment occurring in each year, 3\) the overall
model R2 (quality of model fit to the temporal profile), and 4\) an index,
Total Change Intensity. This index reflects the total amount of change
occurring across components in that pixel. The linear and structural
change methods generally agreed on patterns of change, but the latter
found breaks more often, with at least one break point in most pixels.
The structural change model provides more robust statistics on the
significant minority of pixels with non\-monotonic trends, while
detrending some interannual signal potentially superfluous from a
long\-term perspective.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `annual_herbaceous_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the annual herbaceous time series |
| `bare_ground_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the bare ground time series |
| `herbaceous_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the herbaceous time series |
| `litter_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the litter time series |
| `sagebrush_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the sagebrush time series |
| `shrub_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the shrub time series |
| `shrub_height_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the shrub height time series |
| `non_sagebrush_shrub_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the non sagebrush shrub time series |
| `perennial_herbaceous_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the perennial herbaceous time series |
| `tree_break_point` | count | 0 | 3 |  | Number of structural breaks observed in the tree time series |
| `annual_herbaceous_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for annual herbaceous time series |
| `bare_ground_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for bare ground time series |
| `herbaceous_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for herbaceous time series |
| `litter_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for litter time series |
| `sagebrush_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for sagebrush time series |
| `shrub_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for shrub time series |
| `shrub_height_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for shrub height time series |
| `non_sagebrush_shrub_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for non sagebrush shrub time series |
| `perennial_herbaceous_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for perennial herbaceous time series |
| `tree_linear_model_pvalue` | P\-value | 0 | 100 | 0\.01 | P\-value of linear trends model for tree time series |
| `annual_herbaceous_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for annual herbaceous time series |
| `bare_ground_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for bare ground time series |
| `herbaceous_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for herbaceous time series |
| `litter_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for litter time series |
| `sagebrush_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for sagebrush time series |
| `shrub_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for shrub time series |
| `shrub_height_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for shrub height time series |
| `non_sagebrush_shrub_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for non sagebrush shrub time series |
| `perennial_herbaceous_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for perennial herbaceous time series |
| `tree_linear_model_slope` | % change/y | \-383 | 351 | 0\.01 | Slope of linear trends model for tree time series |
| `annual_herbaceous_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of annual herbaceous time series |
| `bare_ground_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of bare ground time series |
| `herbaceous_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of herbaceous time series |
| `litter_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of litter time series |
| `sagebrush_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of sagebrush time series |
| `shrub_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of shrub time series |
| `shrub_height_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of shrub height time series |
| `non_sagebrush_shrub_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of non sagebrush shrub time series |
| `perennial_herbaceous_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of perennial herbaceous time series |
| `tree_most_recent_break_point` | y | 1985 | 2023 |  | Year of most recent break in the time\-series for each component of tree time series |
| `total_change_intensity_index` | Dimensionless | 0 | 100 |  | Total Change Intensity is a derivative index designed to highlight the total amount of change across primary components (shrub, bare ground, litter, and herbaceous). Change indicates the slope values from the structural change analysis. Values are constructed so that 100 means the maximum observed change across all components and 0 means no change. |




### Terms of Use


**Terms of Use**


This work was authored as part of the Contributor's official duties as an
Employee of the United States Government and is therefore a work of the
United States Government. In accordance with 17 U.S.C. 105, no copyright
protection is available for such works under U.S. Law. This is an Open
Access article that has been identified as being free of known restrictions
under copyright law, including all related and neighboring rights
(https://creativecommons.org/publicdomain/mark/1\.0/). You can copy, modify,
distribute and perform the work, even for commercial purposes, all without
asking permission.




### Citations



Citations:
* Rigge, M.B., Bunde, B., Postma, K., and Shi, H., 2024,
Rangeland Condition Monitoring Assessment and Projection (RCMAP)
Fractional Component Time\-Series Across the Western U.S. 1985\-2023:
U.S. Geological Survey data release,
[doi:10\.5066/P9SJXUI1](https://doi.org/10.5066/P9SJXUI1).
* Rigge, M., H. Shi, C. Homer, P. Danielson, and B. Granneman. 2019\.
Long\-term trajectories of fractional component change in the Northern
Great Basin, USA. Ecosphere 10(6\):e02762\.
[doi:10\.1002/ecs2\.2762](https://doi.org/10.1002/ecs2.2762)
* Rigge, M., C. Homer, L. Cleeves, D. K. Meyer, B. Bunde, H. Shi, G. Xian,
S. Schell, and M. Bobo. 2020\. Quantifying western U.S. rangelands as
fractional components with multi\-resolution remote sensing and in situ
data. Remote Sensing 12\.
[doi:10\.3390/rs12030412](https://doi.org/10.3390/rs12030412)
* Rigge, M., C. Homer, H. Shi, D. Meyer, B. Bunde, B. Granneman,
K. Postma, P. Danielson, A. Case, and G. Xian.
2021\. Rangeland Fractional Components Across the Western United States
from 1985 to 2018\. Remote Sensing 13:813\.
[doi:10\.3390/rs13040813](https://doi.org/10.3390/rs13040813)





### DOIs


* [https://doi.org/10\.1002/ecs2\.2762](https://doi.org/10.1002/ecs2.2762)
* [https://doi.org/10\.3390/rs12030412](https://doi.org/10.3390/rs12030412)
* [https://doi.org/10\.3390/rs13040813](https://doi.org/10.3390/rs13040813)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Import the NLCD RCMAP TRENDS image.
vardataset=ee.Image('USGS/NLCD_RELEASES/2023_REL/RCMAP/V6/TRENDS');
vartrends=dataset.select('annual_herbaceous_break_point');
varvis={
min:[0],
max:[5],
'palette':[
'000000','f9e8b7','f7e3ac','f0dfa3','eedf9c','eada91','e8d687',
'e0d281','ddd077','d6cc6d','d3c667','d0c55e','cfc555','c6bd4f',
'c4ba46','bdb83a','bbb534','b7b02c','b0ad1f','adac17','aaaa0a',
'a3a700','9fa700','9aa700','92a700','8fa700','87a700','85a700',
'82aa00','7aaa00','77aa00','70aa00','6caa00','67aa00','5fa700',
'57a700','52a700','4fa700','4aa700','42a700','3ca700','37a700',
'37a300','36a000','369f00','349d00','339900','339900','2f9200',
'2d9100','2d8f00','2c8a00','2c8800','2c8500','2c8400','2b8200',
'297d00','297a00','297900','277700','247400','247000','29700f',
'2c6d1c','2d6d24','336d2d','366c39','376c44','396a4a','396a55',
'3a6a5f','3a696a','396774','3a6782','39668a','376292','34629f',
'2f62ac','2c5fb7','245ec4','1e5ed0','115cdd','005ae0','0057dd',
'0152d6','0151d0','014fcc','014ac4','0147bd','0144b8','0142b0',
'0141ac','013da7','013aa0','01399d','013693','013491','012f8a',
'012d85','012c82','01297a'
]
};
// Display the image on the map.
Map.setCenter(-114,38,6);
Map.addLayer(trends,vis,'annual herbaceous breakpoint in integer');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_NLCD_RELEASES_2023_REL_RCMAP_V6_TRENDS)


[RCMAP Rangeland Trends for Component Timeseries (1985\-2023\), v06](/earth-engine/datasets/catalog/USGS_NLCD_RELEASES_2023_REL_RCMAP_V6_TRENDS)

The RCMAP (Rangeland Condition Monitoring Assessment and Projection) dataset quantifies the percent cover of rangeland components across western North America using Landsat imagery from 1985\-2023\. The RCMAP product suite consists of ten fractional components: annual herbaceous, bare ground, herbaceous, litter, non\-sagebrush shrub, perennial herbaceous, sagebrush, shrub, tree, and shrub height …

 USGS/NLCD\_RELEASES/2023\_REL/RCMAP/V6/TRENDS,
 climate\-change,disturbance,landsat\-derived,landuse\-landcover,nlcd,rangeland,trends

1985\-01\-01T00:00:00Z/2023\-12\-31T00:00:00Z



 26\.5157 \-128\.0026 51\.5761 \-99\.6758
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.3390/rs13040813](https://doi.org/https://www.mrlc.gov/)
* [https://doi.org/10\.3390/rs13040813](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/USGS_NLCD_RELEASES_2023_REL_RCMAP_V6_TRENDS)
* [https://doi.org/10\.3390/rs13040813](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/USGS_NLCD_RELEASES_2023_REL_RCMAP_V6_TRENDS)









