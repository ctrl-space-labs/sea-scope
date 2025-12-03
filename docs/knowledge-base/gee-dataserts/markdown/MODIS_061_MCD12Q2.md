



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MCD12Q2\.006 Land Cover Dynamics Yearly Global 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2023\-01\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://lpdaac.usgs.gov/products/mcd12q2v061/)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MCD12Q2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD12Q2)





Cadence
1 Year
Tags


[evi](/earth-engine/datasets/tags/evi)
[global](/earth-engine/datasets/tags/global)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[modis](/earth-engine/datasets/tags/modis)
[onset\-greenness](/earth-engine/datasets/tags/onset-greenness)
[phenology](/earth-engine/datasets/tags/phenology)
[usgs](/earth-engine/datasets/tags/usgs)
[yearly](/earth-engine/datasets/tags/yearly)








#### Description



The Terra and Aqua combined Moderate Resolution Imaging Spectroradiometer
(MODIS) Land Cover Dynamics (MCD12Q2\) Version 6\.1 data product provides
global land surface phenology metrics at yearly intervals. The MCD12Q2
Version 6\.1 data product is derived from time series of the 2\-band Enhanced
Vegetation Index (EVI2\) calculated from MODIS Nadir Bidirectional
Reflectance Distribution Function (BRDF)\-Adjusted Reflectance(NBAR).
Vegetation phenology metrics at 500 meter spatial resolution are identified
for up to two detected growing cycles per year. For pixels with more than
two valid vegetation cycles, the data represent the two cycles with the
largest NBAR\-EVI2 amplitudes.


Each asset contains bands are layers for the total number of vegetation
cycles detected for the product year, the onset of greenness, greenup
midpoint, maturity, peak greenness, senescence, greendown midpoint,
dormancy, EVI2 minimum, EVI2 amplitude, integrated EVI2 over a vegetation
cycle, as well as overall and phenology metric\-specific quality information.


For areas where the NBAR\-EVI2 values are missing due to cloud cover or other
reasons, the data gaps are filled with good quality NBAR\-EVI2 values from
the year directly preceding or following the product year.





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- |
| `NumCycles` | 0 | 7 |  | Total number of valid vegetation cycles with peak in product year |
| `Greenup_1` | 11138 | 32766 |  | Date when EVI2 first crossed 15% of the segment EVI2 amplitude, cycle 1\. Days since Jan 1, 1970\. |
| `Greenup_2` | 11138 | 32766 |  | Date when EVI2 first crossed 15% of the segment EVI2 amplitude, cycle 2\. Days since Jan 1, 1970\. |
| `MidGreenup_1` | 11138 | 32766 |  | Date when EVI2 first crossed 50% of the segment EVI2 amplitude, cycle 1\. Days since Jan 1, 1970\. |
| `MidGreenup_2` | 11138 | 32766 |  | Date when EVI2 first crossed 50% of the segment EVI2 amplitude, cycle 2\. Days since Jan 1, 1970\. |
| `Peak_1` | 11138 | 32766 |  | Date when EVI2 reached the segment maximum, cycle 1\. Days since Jan 1, 1970\. |
| `Peak_2` | 11138 | 32766 |  | Date when EVI2 reached the segment maximum, cycle 2\. Days since Jan 1, 1970\. |
| `Maturity_1` | 11138 | 32766 |  | Date when EVI2 first crossed 90% of the segment EVI2 amplitude, cycle 1\. Days since Jan 1, 1970\. |
| `Maturity_2` | 11138 | 32766 |  | Date when EVI2 first crossed 90% of the segment EVI2 amplitude, cycle 2\. Days since Jan 1, 1970\. |
| `MidGreendown_1` | 11138 | 32766 |  | Date when EVI2 last crossed 50% of the segment EVI2 amplitude, cycle 1\. Days since Jan 1, 1970\. |
| `MidGreendown_2` | 11138 | 32766 |  | Date when EVI2 last crossed 50% of the segment EVI2 amplitude, cycle 2\. Days since Jan 1, 1970\. |
| `Senescence_1` | 11138 | 32766 |  | Date when EVI2 last crossed 90% of the segment EVI2 amplitude, cycle 1\. Days since Jan 1, 1970\. |
| `Senescence_2` | 11138 | 32766 |  | Date when EVI2 last crossed 90% of the segment EVI2 amplitude, cycle 2\. Days since Jan 1, 1970\. |
| `Dormancy_1` | 11138 | 32766 |  | Date when EVI2 last crossed 15% of the segment EVI2 amplitude, cycle 1\. Days since Jan 1, 1970\. |
| `Dormancy_2` | 11138 | 32766 |  | Date when EVI2 last crossed 15% of the segment EVI2 amplitude, cycle 2\. Days since Jan 1, 1970\. |
| `EVI_Minimum_1` | 0 | 10000 | 0\.0001 | Segment minimum EVI2 value, cycle 1 |
| `EVI_Minimum_2` | 0 | 10000 | 0\.0001 | Segment minimum EVI2 value, cycle 2 |
| `EVI_Amplitude_1` | 0 | 10000 | 0\.0001 | Segment maximum \- minimum EVI2, cycle 1 |
| `EVI_Amplitude_2` | 0 | 10000 | 0\.0001 | Segment maximum \- minimum EVI2, cycle 2 |
| `EVI_Area_1` | 0 | 3700 | 0\.1 | Sum of daily interpolated EVI2 from Greenup to Dormancy, cycle 1 |
| `EVI_Area_2` | 0 | 3700 | 0\.1 | Sum of daily interpolated EVI2 from Greenup to Dormancy, cycle 2 |
| `QA_Overall_1` | 0 | 3 |  | QA code for entire segment, cycle 1 |
| `QA_Overall_2` | 0 | 3 |  | QA code for entire segment, cycle 2 |
| `QA_Detailed_1` |  | Bit\-packed, SDS\-specific QA codes, cycle 1 |
| Bitmask for QA\_Detailed\_1 * Bits 0\-1: Greenup QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 2\-3: MidGreenup QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 4\-5: Maturity QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 6\-7: Peak QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 8\-9: Senescence QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 10\-11: MidGreendown QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 12\-13: Dormancy QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `QA_Detailed_2` |  | Bit\-packed, SDS\-specific QA codes, cycle 2 |
| Bitmask for QA\_Detailed\_2 * Bits 0\-1: Greenup QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 2\-3: MidGreenup QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 4\-5: Maturity QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 6\-7: Peak QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 8\-9: Senescence QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 10\-11: MidGreendown QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor * Bits 12\-13: Dormancy QA 	+ 0: Best 	+ 1: Good 	+ 2: Fair 	+ 3: Poor | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


**QA\_Overall\_1 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | Best |
| 1 | None | Good |
| 2 | None | Fair |
| 3 | None | Poor |


**QA\_Overall\_2 Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | None | Best |
| 1 | None | Good |
| 2 | None | Fair |
| 3 | None | Poor |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MCD12Q2\.061](https://doi.org/10.5067/MODIS/MCD12Q2.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MCD12Q2')
.filter(ee.Filter.date('2001-01-01','2002-01-01'));
varvegetationPeak=dataset.select('Peak_1');
varvegetationPeakVis={
min:11400,
max:11868,
palette:['0f17ff','b11406','f1ff23'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(
vegetationPeak,vegetationPeakVis,
'Vegetation Peak 2001');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MCD12Q2)


[MCD12Q2\.006 Land Cover Dynamics Yearly Global 500m](/earth-engine/datasets/catalog/MODIS_061_MCD12Q2)

The Terra and Aqua combined Moderate Resolution Imaging Spectroradiometer (MODIS) Land Cover Dynamics (MCD12Q2\) Version 6\.1 data product provides global land surface phenology metrics at yearly intervals. The MCD12Q2 Version 6\.1 data product is derived from time series of the 2\-band Enhanced Vegetation Index (EVI2\) calculated from MODIS Nadir Bidirectional …

 MODIS/061/MCD12Q2,
 evi,global,landuse\-landcover,modis,onset\-greenness,phenology,usgs,yearly

2001\-01\-01T00:00:00Z/2023\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MCD12Q2\.061](https://doi.org/https://lpdaac.usgs.gov/products/mcd12q2v061/)
* [https://doi.org/10\.5067/MODIS/MCD12Q2\.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MCD12Q2)









