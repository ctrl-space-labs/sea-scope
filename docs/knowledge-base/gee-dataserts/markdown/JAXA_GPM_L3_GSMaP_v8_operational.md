



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GSMaP Operational: Global Satellite Mapping of Precipitation \- V8


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================================








Dataset Availability
1998\-01\-01T00:00:00Z–2025\-07\-16T14:00:00Z
Dataset Provider


[JAXA Earth Observation Research Center](https://sharaku.eorc.jaxa.jp/GSMaP/)



Earth Engine Snippet


`ee.ImageCollection("JAXA/GPM_L3/GSMaP/v8/operational")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_GPM_L3_GSMaP_v8_operational)





Cadence
1 Hour
Tags


[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[gpm](/earth-engine/datasets/tags/gpm)
[hourly](/earth-engine/datasets/tags/hourly)
[jaxa](/earth-engine/datasets/tags/jaxa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[weather](/earth-engine/datasets/tags/weather)








#### Description



Global Satellite Mapping of Precipitation (GSMaP) provides
a global hourly rain rate with a 0\.1 x 0\.1 degree resolution. GSMaP
is a product of the Global Precipitation Measurement (GPM) mission,
which provides global precipitation observations at three hour
intervals. Values are estimated using multi\-band passive microwave
and infrared radiometers from the GPM Core Observatory satellite
and with the assistance of a constellation of other satellites. GPM's
precipitation rate retrieval algorithm is based on a radiative
transfer model. The gauge\-adjusted rate is calculated based on
the optimization of the 24h accumulation of GSMaP hourly rain rate
to daily precipitation by NOAA/CPC gauge measurement.
This dataset is processed by GSMaP algorithm version 8 (product version 5\).
See [GSMaP Technical Documentation](https://www.eorc.jaxa.jp/GPM/doc/product/format/en/07.GPM_GSMaP_Product_Format_V5_E.pdf)
for more details.


This dataset contains provisional products GSMaP\_NRT that are
regularly replaced with updated versions when the GSMaP\_MVK data
become available.
The products are marked with a metadata property called ''status''.
When a product is initially made available, the property value
is ''provisional''. Once a provisional product has been updated
with the final version, this value is updated to ''permanent''.
For more information please refer
[General Documentation](https://eolp.jaxa.jp/GSMaP_Hourly.html)





### Bands



**Pixel Size**
  
11132 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `hourlyPrecipRate` | mm/hr | 0\* | 204\.88\* | Snapshot of hourly precipitation rate |
| `hourlyPrecipRateGC` | mm/hr | 0\* | 200\.36\* | Snapshot of hourly precipitation rate adjusted to rain gauge |
| `observationTimeFlag` | h | \-124\.72\* | 16\.06\* | Relative time from the starting time of the file to the time of microwave radiometer (imager/sounder) observing. If no observation exists within the hourly window, the time will be the negative number of hours since the last observation. |
| `satelliteInfoFlag` | None | Satellite/sensor used |
| Bitmask for satelliteInfoFlag * Bit 0: NOAA/CPC Globally Merged IR data 	+ 0: No 	+ 1: Yes * Bit 1: TRMM/TMI 	+ 0: No 	+ 1: Yes * Bit 2: GPM\-Core/GMI 	+ 0: No 	+ 1: Yes * Bit 3: Megha\-Tropiques/MADRAS 	+ 0: No 	+ 1: Yes * Bit 4: Megha\-Tropiques/SAPHIR 	+ 0: No 	+ 1: Yes * Bit 5: ADEOS\-II/AMSR 	+ 0: No 	+ 1: Yes * Bit 6: Aqua/AMSR\-E 	+ 0: No 	+ 1: Yes * Bit 7: GCOM\-W1/AMSR2 	+ 0: No 	+ 1: Yes * Bit 8: GCOM\-W2/AMSR2 	+ 0: No 	+ 1: Yes * Bit 9: GCOM\-W3/AMSR2 	+ 0: No 	+ 1: Yes * Bit 10: DMSP\-F11/SSM/I 	+ 0: No 	+ 1: Yes * Bit 11: DMSP\-F13/SSM/I 	+ 0: No 	+ 1: Yes * Bit 12: DMSP\-F14/SSM/I 	+ 0: No 	+ 1: Yes * Bit 13: DMSP\-F15/SSM/I 	+ 0: No 	+ 1: Yes * Bit 14: DMSP\-F16/SSM/I 	+ 0: No 	+ 1: Yes * Bit 15: DMSP\-F17/SSM/I 	+ 0: No 	+ 1: Yes * Bit 16: DMSP\-F18/SSM/I 	+ 0: No 	+ 1: Yes * Bit 17: DMSP\-F19/SSM/I 	+ 0: No 	+ 1: Yes * Bit 18: DMSP\-F20/SSM/I 	+ 0: No 	+ 1: Yes * Bit 19: NOAA\-15/AMSU\-A/B 	+ 0: No 	+ 1: Yes * Bit 20: NOAA\-16/AMSU\-A/B 	+ 0: No 	+ 1: Yes * Bit 21: NOAA\-17/AMSU\-A/B 	+ 0: No 	+ 1: Yes * Bit 22: NOAA\-18/AMSU\-A/B 	+ 0: No 	+ 1: Yes * Bit 23: NOAA\-19/AMSU\-A/B 	+ 0: No 	+ 1: Yes * Bit 24: NPP/ATMS 	+ 0: No 	+ 1: Yes * Bit 25: JPSS\-1/ATMS 	+ 0: No 	+ 1: Yes * Bit 26: MetOp\-A/AMSU\-A/MHS 	+ 0: No 	+ 1: Yes * Bit 27: MetOp\-B/AMSU\-A/MHS 	+ 0: No 	+ 1: Yes * Bit 28: MetOp\-C/AMSU\-A/MHS 	+ 0: No 	+ 1: Yes | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `gaugeQualityInfo` | count/d | 0\* | 121\* | Existence of gauge adjustment when the status is 'provisional', 1 indicates adjusted and 0 is non\-adjusted. When the status is 'permanent', the pixel value is the daily average of number of gauges used for adjustment in the pixel. |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| AlgorithmID | STRING | The algorithm that generated this product, e.g., 3GSMAPH |
| AlgorithmVersion | STRING | The version of the algorithm that generated this product |
| ProductVersion | STRING | The data version assigned by the processing system |
| GenerationDateTime | STRING | The date and time this granule was generated |
| status | STRING | Permanent or provisional |




### Terms of Use


**Terms of Use**


Anyone wishing to publish any results using the data
from the JAXA Global Rainfall Watch System should clearly acknowledge
the ownership of the data in the publication (for example, ' Global
Rainfall Map in Near\-Real\-Time (GSMaP\_NRT) by JAXA Global Rainfall
Watch' was produced and distributed by the Earth Observation Research
Center, Japan Aerospace Exploration Agency). If you have benefited
from GSMaP rainfall products, please cite the major papers listed
below. For additional information, please visit the [JAXA Site
Policy](https://global.jaxa.jp/policy.html) and the [Users Guide](https://sharaku.eorc.jaxa.jp/GSMaP/guide.html).




### Citations



Citations:
* Kubota, T., K. Aonashi, T. Ushio, S. Shige, Y. N. Takayabu, M. Kachi,
Y. Arai, T. Tashima, T. Masaki, N. Kawamoto, T. Mega, M. K. Yamamoto,
A. Hamada, M. Yamaji, G. Liu and R. Oki 2020: Global Satellite Mapping of
Precipitation (GSMaP) products in the GPM era, Satellite precipitation
measurement, Springer, https://doi.org/10\.1007/978\-3\-030\-24568\-9\_20\.





### DOIs


* [https://doi.org/10\.57746/EO.01gs73bkt358gfpy92y2qns5e9](https://doi.org/10.57746/EO.01gs73bkt358gfpy92y2qns5e9)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('JAXA/GPM_L3/GSMaP/v8/operational')
.filter(ee.Filter.date('2023-09-12','2023-09-13'));
varprecipitation=dataset.select('hourlyPrecipRate');
varprecipitationVis={
min:0.0,
max:10.0,
palette:
['1621a2','ffffff','03ffff','13ff03','efff00','ffb103','ff2300'],
};
Map.setCenter(-90.7,26.12,3);
Map.addLayer(precipitation,precipitationVis,'Precipitation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_GPM_L3_GSMaP_v8_operational)


[GSMaP Operational: Global Satellite Mapping of Precipitation \- V8](/earth-engine/datasets/catalog/JAXA_GPM_L3_GSMaP_v8_operational)

Global Satellite Mapping of Precipitation (GSMaP) provides a global hourly rain rate with a 0\.1 x 0\.1 degree resolution. GSMaP is a product of the Global Precipitation Measurement (GPM) mission, which provides global precipitation observations at three hour intervals. Values are estimated using multi\-band passive microwave and infrared radiometers from …

 JAXA/GPM\_L3/GSMaP/v8/operational,
 climate,geophysical,gpm,hourly,jaxa,precipitation,weather

1998\-01\-01T00:00:00Z/2025\-07\-16T14:00:00Z



 \-60 \-180 60 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.57746/EO.01gs73bkt358gfpy92y2qns5e9](https://doi.org/https://sharaku.eorc.jaxa.jp/GSMaP/)
* [https://doi.org/10\.57746/EO.01gs73bkt358gfpy92y2qns5e9](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JAXA_GPM_L3_GSMaP_v8_operational)









