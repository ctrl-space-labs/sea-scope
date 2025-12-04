



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenET Ensemble Monthly Evapotranspiration v2\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================








Dataset Availability
1999\-10\-01T00:00:00Z–2024\-12\-01T00:00:00Z
Dataset Provider


[OpenET, Inc.](https://openetdata.org/)



Earth Engine Snippet


`ee.ImageCollection("OpenET/ENSEMBLE/CONUS/GRIDMET/MONTHLY/v2_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_ENSEMBLE_CONUS_GRIDMET_MONTHLY_v2_0)





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



The OpenET dataset includes satellite\-based data on the total amount of
water that is transferred from the land surface to the atmosphere through
the process of evapotranspiration (ET). OpenET provides ET data from
multiple satellite\-driven models, and also calculates a single "ensemble
value" from the model ensemble. The models currently included in the OpenET
model ensemble are ALEXI/DisALEXI, eeMETRIC, geeSEBAL, PT\-JPL, SIMS, and
SSEBop. The OpenET ensemble ET value is calculated as the mean of the
ensemble after filtering and removing outliers using the median absolute
deviation approach. All models currently use Landsat satellite data to
produce ET data at a pixel size of 30 meters by 30 meters (0\.22 acres per
pixel). The monthly ET dataset provides data on total ET by month as an
equivalent depth of water in millimeters.


[Additional information](https://openetdata.org/methodologies/)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `et_ensemble_mad` | mm | Ensemble ET value, computed as the mean of the ensemble after filtering outliers using the median absolute deviation (mad) |
| `et_ensemble_mad_min` | mm | The minimum value in the ensemble range, after filtering for outliers using the median absolute deviation (mad) |
| `et_ensemble_mad_max` | mm | The maximum value in the ensemble range, after filtering for outliers using the median absolute deviation (mad) |
| `et_ensemble_mad_count` | None | The number of models used to compute the ensemble ET value, after filtering for outliers using the median absolute deviation (mad) |
| `et_ensemble_mad_index` | None | Bitmask indicating which models were included in the ensemble ET value, after filtering for outliers using the median absolute deviation (mad) |
| Bitmask for et\_ensemble\_mad\_index * Bit 0: DisALEXI included in ensemble 	+ 0: No 	+ 1: Yes * Bit 1: EEMETRIC included in ensemble 	+ 0: No 	+ 1: Yes * Bit 2: GEESEBAL included in ensemble 	+ 0: No 	+ 1: Yes * Bit 3: PTJPL included in ensemble 	+ 0: No 	+ 1: Yes * Bit 4: SIMS included in ensemble 	+ 0: No 	+ 1: Yes * Bit 5: SSEBop included in ensemble 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `et_ensemble_sam` | mm | The simple arithmetic mean (sam) of all six models in the OpenETmodel ensemble |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| build\_date | STRING | Date assets were built |
| core\_version | STRING | OpenET core library version |
| end\_date | STRING | End date of month |
| mgrs\_tile | STRING | MGRS grid zone ID |
| start\_date | STRING | Start date of month |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Melton, F., Huntington, J., Grimm, R., Herring, J., Hall, M., Rollison, D.,
Erickson, T., Allen, R., Anderson, M., Fisher, J., Kilic, A., Senay, G.,
volk, J., Hain, C., Johnson, L., Ruhoff, A., Blankenau, P., Bromley, M.,
Carrara, W., Daudert, B., Doherty, C., Dunkerly, C., Friedrichs, M., Guzman,
A., Halverson, G., Hansen, J., Harding, J., Kang, Y., Ketchum, D., Minor,
B., Morton, C., Revelle, P., Ortega\-Salazar, S., Ott, T., Ozdogon, M.,
Schull, M., Wang, T., Yang, Y., Anderson, R., 2021\. OpenET: Filling a
Critical Data Gap in Water Management for the Western United States.
Journal of the American Water Resources Association, 2021 Nov 2\.
[doi:10\.1111/1752\-1688\.12956](https://doi.org/10.1111/1752-1688.12956)





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
vardataset=ee.ImageCollection('OpenET/ENSEMBLE/CONUS/GRIDMET/MONTHLY/v2_0')
.filterDate('2020-01-01','2021-01-01');

// Compute the annual evapotranspiration (ET) as the sum of the monthly ET
// images for the year.
varet=dataset.select('et_ensemble_mad').sum();

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

Map.addLayer(et,visualization,'OpenET Ensemble Annual ET');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_ENSEMBLE_CONUS_GRIDMET_MONTHLY_v2_0)


[OpenET Ensemble Monthly Evapotranspiration v2\.0](/earth-engine/datasets/catalog/OpenET_ENSEMBLE_CONUS_GRIDMET_MONTHLY_v2_0)

The OpenET dataset includes satellite\-based data on the total amount of water that is transferred from the land surface to the atmosphere through the process of evapotranspiration (ET). OpenET provides ET data from multiple satellite\-driven models, and also calculates a single "ensemble value" from the model ensemble. The models currently …

 OpenET/ENSEMBLE/CONUS/GRIDMET/MONTHLY/v2\_0,
 evapotranspiration,gridmet\-derived,landsat\-derived,monthly,openet,water,water\-vapor

1999\-10\-01T00:00:00Z/2024\-12\-01T00:00:00Z



 25 \-126 50 \-66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1111/1752\-1688\.12956](https://doi.org/https://openetdata.org/)
* [https://doi.org/10\.1111/1752\-1688\.12956](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenET_ENSEMBLE_CONUS_GRIDMET_MONTHLY_v2_0)









