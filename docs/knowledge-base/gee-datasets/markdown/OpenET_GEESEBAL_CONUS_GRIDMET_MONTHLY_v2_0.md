



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenET geeSEBAL Monthly Evapotranspiration v2\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================








Dataset Availability
1999\-10\-01T00:00:00Z–2024\-12\-01T00:00:00Z
Dataset Provider


[OpenET, Inc.](https://openetdata.org/)



Earth Engine Snippet


`ee.ImageCollection("OpenET/GEESEBAL/CONUS/GRIDMET/MONTHLY/v2_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_GEESEBAL_CONUS_GRIDMET_MONTHLY_v2_0)





Cadence
1 Month
Tags


[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[gridmet\-derived](/earth-engine/datasets/tags/gridmet-derived)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[monthly](/earth-engine/datasets/tags/monthly)
[openet](/earth-engine/datasets/tags/openet)
[water](/earth-engine/datasets/tags/water)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)








#### Description



Implementation of geeSEBAL was recently completed within the OpenET
framework and an overview of the current geeSEBAL version can be found
in Laipelt et al. (2021\), which is based on the original algorithms
developed by Bastiaanssen et al. (1998\). The OpenET geeSEBAL implementation
uses land surface temperature (LST) data from Landsat Collection 2, in
addition to NLDAS and gridMET datasets as instantaneous and daily
meteorological inputs, respectively. The automated statistical algorithm
to select the hot and cold endmembers is based on a simplified version of
the Calibration using Inverse Modeling at Extreme Conditions (CIMEC)
algorithm proposed by Allen et al. (2013\), where quantiles of LST and the
normalized difference vegetation index (NDVI) values are used to select
endmember candidates in the Landsat domain area. The cold and wet endmember
candidates are selected in well vegetated areas, while the hot and dry
endmember candidates are selected in the least vegetated cropland areas.
Based on the selected endmembers, geeSEBAL assumes that in the cold and
wet endmember all available energy is converted to latent heat (with high
rates of transpiration), while in the hot and dry endmember all available
energy is converted to sensible heat. Finally, estimates of daily
evapotranspiration are upscaled from instantaneous estimates based on the
evaporative fraction, assuming it is constant during the daytime without
significant changes in soil moisture and advection. Based on the results
from the OpenET Accuracy Assessment and Intercomparison study, the OpenET
geeSEBAL algorithm was modified as follows: (i) the simplified version of
CIMEC was improved by using additional filters to select the endmembers,
including the use of the USDA Cropland Data Layer (CDL) and filters for
NDVI, LST and albedo; (ii) corrections to LST for endmembers based on
antecedent precipitation; (iii) definition of NLDAS wind speed thresholds
to reduce model instability during the atmospheric correction; and, (iv)
improvements to estimate daily net radiation, using FAO\-56 as reference
(Allen et al., 1998\). Overall, geeSEBAL performance is dependent on
topographic, climate, and meteorological conditions, with higher
sensitivity and uncertainty related to hot and cold endmember selections
for the CIMEC automated calibration, and lower sensitivity and uncertainty
related to meteorological inputs (Laipelt et al., 2021 and Kayser
et al., 2022\). To reduce uncertainties related to complex terrain,
improvements were added to correct LST and global (incident) radiation on
the surface (including the environmental lapse rate, elevation slope
and aspect) to represent the effects of topographic features on the
model’s endmember selection algorithm and ET estimates.


[Additional information](https://openetdata.org/methodologies/)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `et` | mm | geeSEBAL ET value |
| `count` | count | Number of cloud free values |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| build\_date | STRING | Date assets were built |
| cloud\_cover\_max | DOUBLE | Maximum CLOUD\_COVER\_LAND percent value for Landsat images included in interpolation |
| collections | STRING | List of Landsat collections for Landsat images included in the interpolation |
| core\_version | STRING | OpenET core library version |
| end\_date | STRING | End date of month |
| et\_reference\_band | STRING | Band in et\_reference\_source that contains the daily reference ET data |
| et\_reference\_resample | STRING | Spatial interpolation mode to resample daily reference ET data |
| et\_reference\_source | STRING | Collection ID for the daily reference ET data |
| interp\_days | DOUBLE | Maximum number of days before and after each image date to include in interpolation |
| interp\_method | STRING | Method used to interpolate between Landsat model estimates |
| interp\_source\_count | DOUBLE | Number of available images in the interpolation source image collection for the target month |
| mgrs\_tile | STRING | MGRS grid zone ID |
| model\_name | STRING | OpenET model name |
| model\_version | STRING | OpenET model version |
| scale\_factor\_count | DOUBLE | Scaling factor that should be applied to the count band |
| scale\_factor\_et | DOUBLE | Scaling factor that should be applied to the et band |
| start\_date | STRING | Start date of month |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Laipelt, L., Kayser, R.H.B., Fleischmann, A.S., Ruhoff, A., Bastiaanssen,
W., Erickson, T.A. and Melton, F., 2021\. Long\-term monitoring of
evapotranspiration using the SEBAL algorithm and Google Earth Engine cloud
computing. ISPRS Journal of Photogrammetry and Remote Sensing, 178,
pp.81\-96\.
[doi:10\.1016/j.isprsjprs.2021\.05\.018](https://doi.org/10.1016/j.isprsjprs.2021.05.018)
* Bastiaanssen, W.G., Menenti, M., Feddes, R.A. and Holtslag, A.A.M.,
1998\. A remote sensing surface energy balance algorithm for land
(SEBAL). 1\. Formulation. Journal of hydrology, 212, pp.198\-212\.
[doi:S0022\-1694(98\)00253\-4](https://doi.org/10.1016/S0022-1694(98)00253-4)
* Kayser, R.H., Ruhoff, A., Laipelt, L., de Mello Kich, E., Roberti, D.
R., de Arruda Souza, V., Rubert, G.C.D., Collischonn, W. and Neale,
C.M.U., 2022\. Assessing geeSEBAL automated calibration and
meteorological reanalysis uncertainties to estimate evapotranspiration
in subtropical humid climates. Agricultural and Forest Meteorology,
314, p.108775\.
[doi:10\.1016/j.agrformet.2021\.108775](https://doi.org/10.1016/j.agrformet.2021.108775)
* Allen, R.G., Burnett, B., Kramber, W., Huntington, J., Kjaersgaard, J.,
Kilic, A., Kelly, C. and Trezza, R., 2013\. Automated calibration of the
metric\-landsat evapotranspiration process. JAWRA Journal of the American
Water Resources Association, 49(3\), pp.563\-576\.
[doi:10\.1111/jawr.12056](https://doi.org/10.1111/jawr.12056)





### DOIs


* [https://doi.org/10\.1016/j.isprsjprs.2021\.05\.018](https://doi.org/10.1016/j.isprsjprs.2021.05.018)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('OpenET/GEESEBAL/CONUS/GRIDMET/MONTHLY/v2_0')
.filterDate('2020-01-01','2021-01-01');

// Compute the annual evapotranspiration (ET) as the sum of the monthly ET
// images for the year.
varet=dataset.select('et').sum();

varvisualization={
min:0,
max:1400,
palette:[
'9e6212','ac7d1d','ba9829','c8b434','d6cf40','bed44b','9fcb51',
'80c256','61b95c','42b062','45b677','49bc8d','4dc2a2','51c8b8',
'55cece','4db4ba','459aa7','3d8094','356681','2d4c6e',
]
};

Map.setCenter(-100,38,5);

Map.addLayer(et,visualization,'OpenET geeSEBAL Annual ET');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_GEESEBAL_CONUS_GRIDMET_MONTHLY_v2_0)


[OpenET geeSEBAL Monthly Evapotranspiration v2\.0](/earth-engine/datasets/catalog/OpenET_GEESEBAL_CONUS_GRIDMET_MONTHLY_v2_0)

Implementation of geeSEBAL was recently completed within the OpenET framework and an overview of the current geeSEBAL version can be found in Laipelt et al. (2021\), which is based on the original algorithms developed by Bastiaanssen et al. (1998\). The OpenET geeSEBAL implementation uses land surface temperature (LST) data from …

 OpenET/GEESEBAL/CONUS/GRIDMET/MONTHLY/v2\_0,
 evapotranspiration,gridmet\-derived,landsat\-derived,monthly,openet,water,water\-vapor

1999\-10\-01T00:00:00Z/2024\-12\-01T00:00:00Z



 25 \-126 50 \-66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1016/j.isprsjprs.2021\.05\.018](https://doi.org/https://openetdata.org/)
* [https://doi.org/10\.1016/j.isprsjprs.2021\.05\.018](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenET_GEESEBAL_CONUS_GRIDMET_MONTHLY_v2_0)









