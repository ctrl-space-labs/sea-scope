



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenET SSEBop Monthly Evapotranspiration v2\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================








Dataset Availability
1999\-10\-01T00:00:00Z–2024\-12\-01T00:00:00Z
Dataset Provider


[OpenET, Inc.](https://openetdata.org/)



Earth Engine Snippet


`ee.ImageCollection("OpenET/SSEBOP/CONUS/GRIDMET/MONTHLY/v2_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_SSEBOP_CONUS_GRIDMET_MONTHLY_v2_0)





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



Operational Simplified Surface Energy Balance (SSEBop)


The Operational Simplified Surface Energy Balance (SSEBop) model by Senay
et al. (2013, 2017\) is a thermal\-based simplified surface energy model for
estimating actual ET based on the principles of satellite psychrometry
(Senay 2018\). The OpenET SSEBop implementation uses land surface temperature
(Ts) from Landsat (Collection 2 Level\-2 Science Products) with key model
parameters (cold/wet\-bulb reference, Tc, and surface psychrometric
constant, 1/dT) derived from a combination of observed surface temperature,
normalized difference vegetation index (NDVI), climatological average
(1980\-2017\) daily maximum air temperature (Ta, 1\-km) from Daymet, and
net radiation data from ERA\-5\. This model implementation uses the Google
Earth Engine processing framework for connecting key SSEBop ET functions
and algorithms together when generating both intermediate and aggregated ET
results. A detailed study and evaluation of the SSEBop model across CONUS
(Senay et al., 2022\) informs both cloud implementation and assessment for
water balance applications at broad scales. Notable model (v0\.2\.6\)
enhancements and performance against previous versions include additional
compatibility with Landsat 9 (launched Sep 2021\), global model
extensibility, and improved parameterization of SSEBop using
FANO (Forcing and Normalizing Operation) to better estimate ET
in all landscapes and all seasons regardless of vegetation cover density,
thereby improving model accuracy by avoiding extrapolation of Tc to
non\-calibration regions.


[Additional information](https://openetdata.org/methodologies/)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `et` | mm | SSEBop ET value |
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
* Senay, G.B., Parrish, G.E., Schauer, M., Friedrichs, M., Khand, K., Boiko,
O., Kagone, S., Dittmeier, R., Arab, S. and Ji, L., 2023\. Improving the
Operational Simplified Surface Energy Balance Evapotranspiration Model Using
the Forcing and Normalizing Operation. Remote Sensing, 15(1\), p.260\.
[doi:10\.3390/rs15010260](https://doi.org/10.3390/rs15010260)
* Senay, G.B., Bohms, S., Singh, R.K., Gowda, P.H., Velpuri, N.M., Alemu,
H. and Verdin, J.P., 2013\. Operational evapotranspiration mapping using
remote sensing and weather datasets: A new parameterization for the SSEB
approach. JAWRA Journal of the American Water Resources Association,
49(3\), pp.577\-591\.
[doi:10\.1111/jawr.12057](https://doi.org/10.1111/jawr.12057)
* Senay, G.B., Schauer, M., Friedrichs, M., Velpuri, N.M. and Singh, R.K.,
2017\. Satellite\-based water use dynamics using historical Landsat data
(1984–2014\) in the southwestern United States. Remote Sensing of
Environment, 202, pp.98\-112\.
[doi:10\.1016/j.rse.2017\.05\.005c](https://doi.org/10.1016/j.rse.2017.05.005)
* Senay, G.B., 2018\. Satellite psychrometric formulation of the
Operational Simplified Surface Energy Balance (SSEBop) model for
quantifying and mapping evapotranspiration. Applied Engineering in
Agriculture, 34(3\), pp.555\-566\.
[doi:10\.13031/aea.12614](https://doi.org/10.13031/aea.12614)
* Senay, G.B., Friedrichs, M., Morton, C., Parrish, G.E., Schauer, M.,
Khand, K., Kagone, S., Boiko, O. and Huntington, J., 2022\. Mapping
actual evapotranspiration using Landsat for the conterminous United
States: Google Earth Engine implementation and assessment of the SSEBop
model. Remote Sensing of Environment, 275, p.113011\.
[doi:10\.1016/j.rse.2022\.113011](https://doi.org/10.1016/j.rse.2022.113011)





### DOIs


* [https://doi.org/10\.3390/rs15010260](https://doi.org/10.3390/rs15010260)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('OpenET/SSEBOP/CONUS/GRIDMET/MONTHLY/v2_0')
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

Map.addLayer(et,visualization,'OpenET SSEBop Annual ET');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_SSEBOP_CONUS_GRIDMET_MONTHLY_v2_0)


[OpenET SSEBop Monthly Evapotranspiration v2\.0](/earth-engine/datasets/catalog/OpenET_SSEBOP_CONUS_GRIDMET_MONTHLY_v2_0)

Operational Simplified Surface Energy Balance (SSEBop) The Operational Simplified Surface Energy Balance (SSEBop) model by Senay et al. (2013, 2017\) is a thermal\-based simplified surface energy model for estimating actual ET based on the principles of satellite psychrometry (Senay 2018\). The OpenET SSEBop implementation uses land surface temperature (Ts) from …

 OpenET/SSEBOP/CONUS/GRIDMET/MONTHLY/v2\_0,
 evapotranspiration,gridmet\-derived,landsat\-derived,monthly,openet,water,water\-vapor

1999\-10\-01T00:00:00Z/2024\-12\-01T00:00:00Z



 25 \-126 50 \-66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.3390/rs15010260](https://doi.org/https://openetdata.org/)
* [https://doi.org/10\.3390/rs15010260](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenET_SSEBOP_CONUS_GRIDMET_MONTHLY_v2_0)









