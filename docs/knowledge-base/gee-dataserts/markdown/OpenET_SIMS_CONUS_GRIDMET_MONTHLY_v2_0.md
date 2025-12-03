



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenET SIMS Monthly Evapotranspiration v2\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================








Dataset Availability
1999\-10\-01T00:00:00Z–2024\-12\-01T00:00:00Z
Dataset Provider


[OpenET, Inc.](https://openetdata.org/)



Earth Engine Snippet


`ee.ImageCollection("OpenET/SIMS/CONUS/GRIDMET/MONTHLY/v2_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_SIMS_CONUS_GRIDMET_MONTHLY_v2_0)





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



Satellite Irrigation Management Support


The NASA Satellite Irrigation Management Support (SIMS) model was originally
developed to support satellite mapping of crop coefficients and
evapotranspiration (ET) from irrigated lands and to increase access to this
data to support use in irrigation scheduling and regional assessment of
agricultural water needs (Melton et al., 2012\). SIMS uses a reflectance
based approach and incorporates the density coefficient described by Allen
and Pereira (2009\) and Pereira et al. (2020\) to compute basal crop
coefficients for each 30 x 30 m pixel. The primary change from the most
recent SIMS publication (Pereira et al., 2020\) for implementation in OpenET
is the integration of a gridded soil water balance model to account for soil
evaporation following precipitation events. Results of the OpenET Phase I
intercomparison and accuracy assessment (Melton et al., 2022\) showed that
SIMS generally performed well for cropland sites during the growing season,
but had a persistent low bias during the winter months or other time periods
with frequent precipitation. This result was anticipated, since the
reflectance\-based approach used by SIMS is not sensitive to soil
evaporation. To correct for this underestimation, a soil water balance model
based on FAO\-56 (Allen et al., 1998\) was implemented on Google Earth Engine
and driven with gridded precipitation data from gridMET to estimate soil
evaporation coefficients. These coefficients were then combined with the
basal crop coefficients calculated by SIMS to calculate total crop
evapotranspiration using the dual crop coefficient approach. In addition,
a modest positive bias was observed in the SIMS data for periods with low
or sparse vegetative cover. To correct for this bias, updates were made to
the equations that calculate the minimum basal crop coefficient to allow
lower minimum basal crop coefficient values to be achieved. Full
documentation of the SIMS model, current algorithms, and details and
equations used in the soil water balance model are included in the
SIMS user manual.


The SIMS model calculates ET under well\-watered conditions for the current
crop growth stage and condition as measured by the satellite data, and SIMS
is generally expected to have a positive bias for deficit irrigated crops
and croplands with short\-term or intermittent crop water stress. At
present, SIMS is only implemented for croplands, and non\-agricultural lands
are masked out in this data collection. Future research will extend the
vegetation density\-crop coefficient approach used within SIMS to other land
cover types.
[Additional information](https://openetdata.org/methodologies/)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `et` | mm | SIMS ET value |
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
* Melton, F., Huntington, J., Grimm, R., Herring, J., Hall, M., Rollison, D.,
Erickson, T., Allen, R., Anderson, M., Fisher, J., Kilic, A., Senay, G.,
volk, J., Hain, C., Johnson, L., Ruhoff, A., Blanenau, P., Bromley, M.,
Carrara, W., Daudert, B., Doherty, C., Dunkerly, C., Friedrichs, M., Guzman,
A., Halverson, G., Hansen, J., Harding, J., Kang, Y., Ketchum, D., Minor,
B., Morton, C., Revelle, P., Ortega\-Salazar, S., Ott, T., Ozdogon, M.,
Schull, M., Wang, T., Yang, Y., Anderson, R., 2021\. "OpenET: Filling a
Critical Data Gap in Water Management for the Western United
States. "Journal of the American Water Resources Association, 58(6\),
pp.971\-994\.
[doi:10\.1111/1752\-1688\.12956](https://doi.org/10.1111/1752-1688.12956)
* Pereira, L.S., P. Paredes, F.S. Melton, L.F. Johnson, R. López\-Urrea,
J. Cancela, and R.G. Allen. 2020\. "Prediction of Basal Crop
Coefficients from Fraction of Ground Cover and Height." Agricultural
Water Management, Special Issue on Updates to the FAO56 Crop Water
Requirements Method 241, 106197\.
[doi:10\.1016/j.agwat.2020\.106197](https://doi.org/10.1016/j.agwat.2020.106197)
* Melton, F.S., L.F. Johnson, C.P. Lund, L.L. Pierce, A.R. Michaelis,
S.H. Hiatt, A. Guzman et al. 2012\. "Satellite Irrigation Management
Support with the Terrestrial Observation and Prediction System: A
Framework for Integration of Satellite and Surface Observations to
Support Improvements in Agricultural Water Resource Management.IEEE
Journal of Selected Topics in Applied Earth Observations and Remote
Sensing 5 (6\): 1709–21\.
[doi:10\.1109/JSTARS.2012\.2214474](https://doi.org/10.1109/JSTARS.2012.2214474)
* Allen, R.G. and Pereira, L.S., 2009\. Estimating crop coefficients from
fraction of ground cover and height. Irrigation Science, 28, pp.17\-34\.
[doi:10\.1007/s00271\-009\-0182\-z](https://doi.org/10.1007/s00271-009-0182-z)
* Allen, R.G., Pereira, L.S., Raes, D. and Smith, M., 1998\. Crop
evapotranspiration\-Guidelines for computing crop water requirements\-FAO
Irrigation and drainage paper 56\. Fao, Rome, 300 (9\), p.D05109\.
[https://www.fao.org/3/x0490e/x0490e00\.htm](https://www.fao.org/3/x0490e/x0490e00.htm)





### DOIs


* [https://doi.org/10\.1111/1752\-1688\.12956](https://doi.org/10.1111/1752-1688.12956)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('OpenET/SIMS/CONUS/GRIDMET/MONTHLY/v2_0')
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

Map.addLayer(et,visualization,'OpenET SIMS Annual ET');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_SIMS_CONUS_GRIDMET_MONTHLY_v2_0)


[OpenET SIMS Monthly Evapotranspiration v2\.0](/earth-engine/datasets/catalog/OpenET_SIMS_CONUS_GRIDMET_MONTHLY_v2_0)

Satellite Irrigation Management Support The NASA Satellite Irrigation Management Support (SIMS) model was originally developed to support satellite mapping of crop coefficients and evapotranspiration (ET) from irrigated lands and to increase access to this data to support use in irrigation scheduling and regional assessment of agricultural water needs (Melton et …

 OpenET/SIMS/CONUS/GRIDMET/MONTHLY/v2\_0,
 evapotranspiration,gridmet\-derived,landsat\-derived,monthly,openet,water,water\-vapor

1999\-10\-01T00:00:00Z/2024\-12\-01T00:00:00Z



 25 \-126 50 \-66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1111/1752\-1688\.12956](https://doi.org/https://openetdata.org/)
* [https://doi.org/10\.1111/1752\-1688\.12956](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenET_SIMS_CONUS_GRIDMET_MONTHLY_v2_0)









