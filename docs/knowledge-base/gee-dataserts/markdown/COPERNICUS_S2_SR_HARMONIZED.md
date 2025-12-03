



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Harmonized Sentinel\-2 MSI: MultiSpectral Instrument, Level\-2A (SR)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================================








Dataset Availability
2017\-03\-28T00:00:00Z–2025\-07\-19T03:53:26\.973000Z
Dataset Provider


[European Union/ESA/Copernicus](https://sentinel.esa.int/web/sentinel/user-guides/sentinel-2-msi/processing-levels/level-2)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/S2_SR_HARMONIZED")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S2_SR_HARMONIZED)





Revisit Interval
5 Days
Tags


[copernicus](/earth-engine/datasets/tags/copernicus)
[esa](/earth-engine/datasets/tags/esa)
[eu](/earth-engine/datasets/tags/eu)
[msi](/earth-engine/datasets/tags/msi)
[reflectance](/earth-engine/datasets/tags/reflectance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sentinel](/earth-engine/datasets/tags/sentinel)
[sr](/earth-engine/datasets/tags/sr)








#### Description



After 2022\-01\-25, Sentinel\-2 scenes with PROCESSING\_BASELINE '04\.00' or above
have their DN (value) range shifted by 1000\. The HARMONIZED collection
shifts data in newer scenes to be in the same range as in older scenes.


Sentinel\-2 is a wide\-swath, high\-resolution, multi\-spectral
imaging mission supporting Copernicus Land Monitoring studies,
including the monitoring of vegetation, soil and water cover,
as well as observation of inland waterways and coastal areas.


The Sentinel\-2 L2 data are downloaded from CDSE. They were
computed by running sen2cor. WARNING: 2017\-2018 L2 coverage
in the EE collection is not yet global.


The assets contain
12 UINT16 spectral bands representing SR scaled by 10000 (unlike in L1 data,
there is no B10\). There are also several more L2\-specific bands (see band
list for details). See the
[Sentinel\-2 User Handbook](https://sentinel.esa.int/documents/247904/685211/Sentinel-2_User_Handbook)
for details.


QA60 is a bitmask band that contained rasterized cloud mask
polygons until 2022\-01\-25, when these polygons stopped being produced.
Starting 2024\-02\-28, legacy\-consistent QA60 bands are constructed from
the MSK\_CLASSI cloud classification bands.
For more details,
[see the full explanation of how cloud masks are computed.](https://sentinel.esa.int/web/sentinel/technical-guides/sentinel-2-msi/level-1c/cloud-masks)


EE asset ids for Sentinel\-2 L2 assets have the following format:
COPERNICUS/S2\_SR/20151128T002653\_20151128T102149\_T56MNN. Here the
first numeric part represents the sensing date and time, the
second numeric part represents the product generation date and
time, and the final 6\-character string is a unique granule identifier
indicating its UTM grid reference (see [MGRS](https://en.wikipedia.org/wiki/Military_Grid_Reference_System)).


For datasets to assist with cloud and/or cloud shadow detection, see [COPERNICUS/S2\_CLOUD\_PROBABILITY](/earth-engine/datasets/catalog/COPERNICUS_S2_CLOUD_PROBABILITY)
and [GOOGLE/CLOUD\_SCORE\_PLUS/V1/S2\_HARMONIZED](/earth-engine/datasets/catalog/GOOGLE_CLOUD_SCORE_PLUS_V1_S2_HARMONIZED).


For more details on Sentinel\-2 radiometric resolution, [see this page](https://sentinel.esa.int/web/sentinel/user-guides/sentinel-2-msi/resolutions/radiometric).





### Bands


**Bands**




| Name | Units | Min | Max | Scale | Pixel Size | Wavelength | Description |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `B1` | None | 0\.0001 | 443\.9nm (S2A) / 442\.3nm (S2B) | Aerosols |
| `B2` | None | 0\.0001 | 496\.6nm (S2A) / 492\.1nm (S2B) | Blue |
| `B3` | None | 0\.0001 | 560nm (S2A) / 559nm (S2B) | Green |
| `B4` | None | 0\.0001 | 664\.5nm (S2A) / 665nm (S2B) | Red |
| `B5` | None | 0\.0001 | 703\.9nm (S2A) / 703\.8nm (S2B) | Red Edge 1 |
| `B6` | None | 0\.0001 | 740\.2nm (S2A) / 739\.1nm (S2B) | Red Edge 2 |
| `B7` | None | 0\.0001 | 782\.5nm (S2A) / 779\.7nm (S2B) | Red Edge 3 |
| `B8` | None | 0\.0001 | 835\.1nm (S2A) / 833nm (S2B) | NIR |
| `B8A` | None | 0\.0001 | 864\.8nm (S2A) / 864nm (S2B) | Red Edge 4 |
| `B9` | None | 0\.0001 | 945nm (S2A) / 943\.2nm (S2B) | Water vapor |
| `B11` | None | 0\.0001 | 1613\.7nm (S2A) / 1610\.4nm (S2B) | SWIR 1 |
| `B12` | None | 0\.0001 | 2202\.4nm (S2A) / 2185\.7nm (S2B) | SWIR 2 |
| `AOT` | None | 0\.001 | None | Aerosol Optical Thickness |
| `WVP` | cm | 0\.001 | None | Water Vapor Pressure. The height the water would occupy if the vapor were condensed into liquid and spread evenly across the column. |
| `SCL` | None | 1 | 11 |  | None | Scene Classification Map (The "No Data" value of 0 is masked out) |
| `TCI_R` | None |  | None | True Color Image, Red channel |
| `TCI_G` | None |  | None | True Color Image, Green channel |
| `TCI_B` | None |  | None | True Color Image, Blue channel |
| `MSK_CLDPRB` | None | 0 | 100 |  | None | Cloud Probability Map (missing in some products) |
| `MSK_SNWPRB` | None | 0 | 100 |  | None | Snow Probability Map (missing in some products) |
| `QA10` | None |  | None | Always empty |
| `QA20` | None |  | None | Always empty |
| `QA60` | None |  | None | Cloud mask. Masked out between 2022\-01\-25 to 2024\-02\-28 inclusive. |
| Bitmask for QA60 * Bits 0\-9: Unused * Bit 10: Opaque clouds 	+ 0: No opaque clouds 	+ 1: Opaque clouds present * Bit 11: Cirrus clouds 	+ 0: No cirrus clouds 	+ 1: Cirrus clouds present | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `MSK_CLASSI_OPAQUE` | None |  | None | Opaque clouds classification band (0\=no clouds, 1\=clouds). Masked out before February 2024\. |
| `MSK_CLASSI_CIRRUS` | None |  | None | Cirrus clouds classification band (0\=no clouds, 1\=clouds). Masked out before February 2024\. |
| `MSK_CLASSI_SNOW_ICE` | None |  | None | Snow/ice classification band (0\=no snow/ice, 1\=snow/ice). Masked out before February 2024\. |


**SCL Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#ff0004 | Saturated or defective |
| 2 | \#868686 | Dark Area Pixels |
| 3 | \#774b0a | Cloud Shadows |
| 4 | \#10d22c | Vegetation |
| 5 | \#ffff52 | Bare Soils |
| 6 | \#0000ff | Water |
| 7 | \#818181 | Clouds Low Probability / Unclassified |
| 8 | \#c0c0c0 | Clouds Medium Probability |
| 9 | \#f1f1f1 | Clouds High Probability |
| 10 | \#bac5eb | Cirrus |
| 11 | \#52fff9 | Snow / Ice |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| AOT\_RETRIEVAL\_ACCURACY | DOUBLE | Accuracy of Aerosol Optical thickness model |
| CLOUDY\_PIXEL\_PERCENTAGE | DOUBLE | Granule\-specific cloudy pixel percentage taken from the original metadata |
| CLOUD\_COVERAGE\_ASSESSMENT | DOUBLE | Cloudy pixel percentage for the whole archive that contains this granule. Taken from the original metadata |
| CLOUDY\_SHADOW\_PERCENTAGE | DOUBLE | Percentage of pixels classified as cloud shadow |
| DARK\_FEATURES\_PERCENTAGE | DOUBLE | Percentage of pixels classified as dark features or shadows |
| DATASTRIP\_ID | STRING | Unique identifier of the datastrip Product Data Item (PDI) |
| DATATAKE\_IDENTIFIER | STRING | Uniquely identifies a given Datatake. The ID contains the Sentinel\-2 satellite, start date and time, absolute orbit number, and processing baseline. |
| DATATAKE\_TYPE | STRING | MSI operation mode |
| DEGRADED\_MSI\_DATA\_PERCENTAGE | DOUBLE | Percentage of degraded MSI and ancillary data |
| FORMAT\_CORRECTNESS | STRING | Synthesis of the On\-Line Quality Control (OLQC) checks performed at granule (Product\_Syntax) and datastrip (Product Syntax and DS\_Consistency) levels |
| GENERAL\_QUALITY | STRING | Synthesis of the OLQC checks performed at the datastrip level (Relative\_Orbit\_Number) |
| GENERATION\_TIME | DOUBLE | Product generation time |
| GEOMETRIC\_QUALITY | STRING | Synthesis of the OLQC checks performed at the datastrip level (Attitude\_Quality\_Indicator) |
| GRANULE\_ID | STRING | Unique identifier of the granule PDI (PDI\_ID) |
| HIGH\_PROBA\_CLOUDS\_PERCENTAGE | DOUBLE | Percentage of pixels classified as high probability clouds |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B1 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B1 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B2 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B2 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B3 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B3 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B4 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B4 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B5 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B5 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B6 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B6 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B7 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B7 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B8 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B8 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B8A | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B8a and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B9 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B9 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B10 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B10 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B11 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B11 and for all detectors |
| MEAN\_INCIDENCE\_AZIMUTH\_ANGLE\_B12 | DOUBLE | Mean value containing viewing incidence azimuth angle average for band B12 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B1 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B1 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B2 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B2 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B3 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B3 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B4 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B4 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B5 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B5 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B6 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B6 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B7 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B7 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B8 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B8 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B8A | DOUBLE | Mean value containing viewing incidence zenith angle average for band B8a and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B9 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B9 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B10 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B10 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B11 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B11 and for all detectors |
| MEAN\_INCIDENCE\_ZENITH\_ANGLE\_B12 | DOUBLE | Mean value containing viewing incidence zenith angle average for band B12 and for all detectors |
| MEAN\_SOLAR\_AZIMUTH\_ANGLE | DOUBLE | Mean value containing sun azimuth angle average for all bands and detectors |
| MEAN\_SOLAR\_ZENITH\_ANGLE | DOUBLE | Mean value containing sun zenith angle average for all bands and detectors |
| MEDIUM\_PROBA\_CLOUDS\_PERCENTAGE | DOUBLE | Percentage of pixels classified as medium probability clouds |
| MGRS\_TILE | STRING | US\-Military Grid Reference System (MGRS) tile |
| NODATA\_PIXEL\_PERCENTAGE | DOUBLE | Percentage of No Data pixels |
| NOT\_VEGETATED\_PERCENTAGE | DOUBLE | Percentage of pixels classified as non\-vegetated |
| PROCESSING\_BASELINE | STRING | Configuration baseline used at the time of the product generation in terms of processor software version and major Ground Image Processing Parameters (GIPP) version |
| PRODUCT\_ID | STRING | The full id of the original Sentinel\-2 product |
| RADIATIVE\_TRANSFER\_ACCURACY | DOUBLE | Accuracy of radiative transfer model |
| RADIOMETRIC\_QUALITY | STRING | Based on the OLQC reports contained in the Datastrips/QI\_DATA with RADIOMETRIC\_QUALITY checklist name |
| REFLECTANCE\_CONVERSION\_CORRECTION | DOUBLE | Earth\-Sun distance correction factor |
| SATURATED\_DEFECTIVE\_PIXEL\_PERCENTAGE | DOUBLE | Percentage of saturated or defective pixels |
| SENSING\_ORBIT\_DIRECTION | STRING | Imaging orbit direction |
| SENSING\_ORBIT\_NUMBER | DOUBLE | Imaging orbit number |
| SENSOR\_QUALITY | STRING | Synthesis of the OLQC checks performed at granule (Missing\_Lines, Corrupted\_ISP, and Sensing\_Time) and datastrip (Degraded\_SAD and Datation\_Model) levels |
| SOLAR\_IRRADIANCE\_B1 | DOUBLE | Mean solar exoatmospheric irradiance for band B1 |
| SOLAR\_IRRADIANCE\_B2 | DOUBLE | Mean solar exoatmospheric irradiance for band B2 |
| SOLAR\_IRRADIANCE\_B3 | DOUBLE | Mean solar exoatmospheric irradiance for band B3 |
| SOLAR\_IRRADIANCE\_B4 | DOUBLE | Mean solar exoatmospheric irradiance for band B4 |
| SOLAR\_IRRADIANCE\_B5 | DOUBLE | Mean solar exoatmospheric irradiance for band B5 |
| SOLAR\_IRRADIANCE\_B6 | DOUBLE | Mean solar exoatmospheric irradiance for band B6 |
| SOLAR\_IRRADIANCE\_B7 | DOUBLE | Mean solar exoatmospheric irradiance for band B7 |
| SOLAR\_IRRADIANCE\_B8 | DOUBLE | Mean solar exoatmospheric irradiance for band B8 |
| SOLAR\_IRRADIANCE\_B8A | DOUBLE | Mean solar exoatmospheric irradiance for band B8a |
| SOLAR\_IRRADIANCE\_B9 | DOUBLE | Mean solar exoatmospheric irradiance for band B9 |
| SOLAR\_IRRADIANCE\_B10 | DOUBLE | Mean solar exoatmospheric irradiance for band B10 |
| SOLAR\_IRRADIANCE\_B11 | DOUBLE | Mean solar exoatmospheric irradiance for band B11 |
| SOLAR\_IRRADIANCE\_B12 | DOUBLE | Mean solar exoatmospheric irradiance for band B12 |
| SNOW\_ICE\_PERCENTAGE | DOUBLE | Percentage of pixels classified as snow or ice |
| SPACECRAFT\_NAME | STRING | Sentinel\-2 spacecraft name: Sentinel\-2A, Sentinel\-2B |
| THIN\_CIRRUS\_PERCENTAGE | DOUBLE | Percentage of pixels classified as thin cirrus clouds |
| UNCLASSIFIED\_PERCENTAGE | DOUBLE | Percentage of unclassified pixels |
| VEGETATION\_PERCENTAGE | DOUBLE | Percentage of pixels classified as vegetation |
| WATER\_PERCENTAGE | DOUBLE | Percentage of pixels classified as water |
| WATER\_VAPOUR\_RETRIEVAL\_ACCURACY | DOUBLE | Declared accuracy of the Water Vapor model |




### Terms of Use


**Terms of Use**


The use of Sentinel data is governed by the [Copernicus
Sentinel Data Terms and Conditions.](https://scihub.copernicus.eu/twiki/pub/SciHubWebPortal/TermsConditions/Sentinel_Data_Terms_and_Conditions.pdf)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
/**
 * Function to mask clouds using the Sentinel-2 QA band
 * @param {ee.Image} image Sentinel-2 image
 * @return {ee.Image} cloud masked Sentinel-2 image
 */
functionmaskS2clouds(image){
varqa=image.select('QA60');

// Bits 10 and 11 are clouds and cirrus, respectively.
varcloudBitMask=1 << 10;
varcirrusBitMask=1 << 11;

// Both flags should be set to zero, indicating clear conditions.
varmask=qa.bitwiseAnd(cloudBitMask).eq(0)
.and(qa.bitwiseAnd(cirrusBitMask).eq(0));

returnimage.updateMask(mask).divide(10000);
}

vardataset=ee.ImageCollection('COPERNICUS/S2_SR_HARMONIZED')
.filterDate('2020-01-01','2020-01-30')
// Pre-filter to get less cloudy granules.
.filter(ee.Filter.lt('CLOUDY_PIXEL_PERCENTAGE',20))
.map(maskS2clouds);

varvisualization={
min:0.0,
max:0.3,
bands:['B4','B3','B2'],
};

Map.setCenter(83.277,17.7009,12);

Map.addLayer(dataset.mean(),visualization,'RGB');
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
defmask_s2_clouds(image):
"""Masks clouds in a Sentinel-2 image using the QA band.

  Args:
      image (ee.Image): A Sentinel-2 image.

  Returns:
      ee.Image: A cloud-masked Sentinel-2 image.
  """
  qa = image.select('QA60')

  # Bits 10 and 11 are clouds and cirrus, respectively.
  cloud_bit_mask = 1 << 10
  cirrus_bit_mask = 1 << 11

  # Both flags should be set to zero, indicating clear conditions.
  mask = (
      qa.bitwiseAnd(cloud_bit_mask)
      .eq(0)
      .And(qa.bitwiseAnd(cirrus_bit_mask).eq(0))
  )

  return image.updateMask(mask).divide(10000)


dataset = (
    ee.ImageCollection('COPERNICUS/S2_SR_HARMONIZED')
    .filterDate('2020-01-01', '2020-01-30')
    # Pre-filter to get less cloudy granules.
    .filter(ee.Filter.lt('CLOUDY_PIXEL_PERCENTAGE', 20))
    .map(mask_s2_clouds)
)

visualization = {
    'min': 0.0,
    'max': 0.3,
    'bands': ['B4', 'B3', 'B2'],
}

m = geemap.Map()
m.set_center(83.277, 17.7009, 12)
m.add_layer(dataset.mean(), visualization, 'RGB')
m
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S2_SR_HARMONIZED)


[Harmonized Sentinel\-2 MSI: MultiSpectral Instrument, Level\-2A (SR)](/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)

After 2022\-01\-25, Sentinel\-2 scenes with PROCESSING\_BASELINE '04\.00' or above have their DN (value) range shifted by 1000\. The HARMONIZED collection shifts data in newer scenes to be in the same range as in older scenes. Sentinel\-2 is a wide\-swath, high\-resolution, multi\-spectral imaging mission supporting Copernicus Land Monitoring studies, including the …

 COPERNICUS/S2\_SR\_HARMONIZED,
 copernicus,esa,eu,msi,reflectance,satellite\-imagery,sentinel,sr

2017\-03\-28T00:00:00Z/2025\-07\-19T03:53:26\.973000Z



 \-56 \-180 83 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








