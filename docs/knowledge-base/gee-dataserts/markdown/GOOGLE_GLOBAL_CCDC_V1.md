



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Google Global Landsat\-based CCDC Segments (1999\-2019\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================================








Dataset Availability
1999\-01\-01T00:00:00Z–2020\-01\-01T00:00:00Z
Dataset Provider


[Google](https://earthengine.google.com/)



Earth Engine Snippet


`ee.ImageCollection("GOOGLE/GLOBAL_CCDC/V1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_GLOBAL_CCDC_V1)





Tags


[change\-detection](/earth-engine/datasets/tags/change-detection)
[google](/earth-engine/datasets/tags/google)
[landcover](/earth-engine/datasets/tags/landcover)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[landuse](/earth-engine/datasets/tags/landuse)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)








#### Description



This collection contains precomputed results from running the
Continuous Change Detection and Classification (CCDC) algorithm on
20 years of Landsat surface reflectance data. CCDC is a break\-point
finding algorithm that uses harmonic fitting with a dynamic RMSE
threshold to detect breakpoints in time\-series data.


The dataset was created from the Landsat 5, 7, and 8 Collection\-1, Tier\-1,
surface reflectance time series, using all daytime images between 1999\-01\-01
and 2019\-12\-31\. Each image was preprocessed to mask pixels identified as
cloud, shadow, or snow (according to the 'pixel\_qa' band), saturated pixels,
and pixels with an atmospheric opacity \> 300 (as identified by the
'sr\_atmos\_opacity' and 'sr\_aerosol' bands). Pixels repeated in
north/south scene overlap were deduplicated. The results were
output in 2\-degree tiles for all landmasses between \-60° and \+85° latitude.
The images are suitable to simply mosaic() into one global image.


The CCDC algorithm was run with the default algorithm parameters except for
the dateFormat:


* tmaskBands: \['green', 'swir']
* minObservations: 6
* chiSquareProbability: 0\.99
* minNumOfYearsScaler: 1\.33
* dateFormat: 1 (fractional year)
* lambda: 20
* maxIterations: 25000


Each pixel in the output is encoded using variable length arrays. The outer
length of each array (axis 0\) corresponds to the number of breakpoints
found at that location. The coefs bands contain 2\-D arrays, where each inner
array contains the scaling factors for the 8 terms in the linear harmonic
model, in the order: \[offset, t, cos(ωt), sin(ωt), cos(2ωt),
sin(2ωt), cos(3ωt), sin(3ωt)], where ω \= 2Π. The
models are scale to produce refelectance units (0\.0 \- 1\.0\) for the optical
bands and degrees (K) / 100\.0 for the thermal band.


Note that since the output bands are arrays and can only be downsampled
using a SAMPLE pyramiding policy. At lower zoom levels, the
results are usually no longer representative of the full\-resolution data,
and, for instance, tile boundaries can be seen due to the downsampled masks.
It's therefore not recommended to use this dataset at resolutions less than
240m/pixel.


There are no current plans to add post\-2019 assets to this dataset.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Description |
| --- | --- |
| `tStart` | 1\-D Array containing the date of the start of each segment (fractional year). |
| `tEnd` | 1\-D Array containing the date of the end of each segment (fractional year). |
| `tBreak` | 1\-D Array containing the date of the detected breakpoint of each segment (fractional year). |
| `numObs` | 1\-D Array containing the number of observations found in each segment. |
| `changeProb` | A pseudo\-probability of the detected breakpoint being real. |
| `BLUE_coefs` | 2\-D array containing harmonic model coefficients for the blue band, for each segment. |
| `GREEN_coefs` | 2\-D array containing harmonic model coefficients for the green band, for each segment. |
| `RED_coefs` | 2\-D array containing harmonic model coefficients for the red band, for each segment. |
| `NIR_coefs` | 2\-D array containing harmonic model coefficients for the near\-infrared band, for each segment. |
| `SWIR1_coefs` | 2\-D array containing harmonic model coefficients for the shortwave\-infrared (1\.55μm\-1\.75μm) band, for each segment. |
| `SWIR2_coefs` | 2\-D array containing harmonic model coefficients for the shortwave\-infrared (2\.09μm\-2\.35μm) band, for each segment. |
| `TEMP_coefs` | 2\-D array containing harmonic model coefficients for the thermal band, for each segment. |
| `BLUE_rmse` | 1\-D array containing the RMSE of the model for the blue band, for each segment. |
| `GREEN_rmse` | 1\-D array containing the RMSE of the model for the green band, for each segment. |
| `RED_rmse` | 1\-D array containing the RMSE of the model for the red band, for each segment. |
| `NIR_rmse` | 1\-D array containing the RMSE of the model for the near\-infrared band, for each segment. |
| `SWIR1_rmse` | 1\-D array containing the RMSE of the model for the the shortwave\-infrared (1\.55μm\-1\.75μm) band, for each segment. |
| `SWIR2_rmse` | 1\-D array containing the RMSE of the model for the shortwave\-infrared (2\.09μm\-2\.35μm) band, for each segment. |
| `TEMP_rmse` | 1\-D array containing the RMSE of the model for the thermal band, for each segment. |
| `BLUE_magnitude` | 1\-D array containing the magnitude of the detected breakpoint for the blue band, for each segment. |
| `GREEN_magnitude` | 1\-D array containing the magnitude of the detected breakpoint for the green band, for each segment. |
| `RED_magnitude` | 1\-D array containing the magnitude of the detected breakpoint for the red band, for each segment. |
| `NIR_magnitude` | 1\-D array containing the magnitude of the detected breakpoint for the near\-infrared band, for each segment. |
| `SWIR1_magnitude` | 1\-D array containing the magnitude of the detected breakpoint for the shortwave\-infrared\-1 (1\.55μm\-1\.75μm) band, for each segment. |
| `SWIR2_magnitude` | 1\-D array containing the magnitude of the detected breakpoint for the shortwave\-infrared\-2 (2\.09μm\-2\.35μm) band, for each segment. |
| `TEMP_magnitude` | 1\-D array containing the magnitude of the detected breakpoint for the thermal band, for each segment. |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



[Google Global Landsat\-based CCDC Segments (1999\-2019\)](/earth-engine/datasets/catalog/GOOGLE_GLOBAL_CCDC_V1)

This collection contains precomputed results from running the Continuous Change Detection and Classification (CCDC) algorithm on 20 years of Landsat surface reflectance data. CCDC is a break\-point finding algorithm that uses harmonic fitting with a dynamic RMSE threshold to detect breakpoints in time\-series data. The dataset was created from the …

 GOOGLE/GLOBAL\_CCDC/V1,
 change\-detection,google,landcover,landsat\-derived,landuse,landuse\-landcover

1999\-01\-01T00:00:00Z/2020\-01\-01T00:00:00Z



 \-60 \-180 72 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








