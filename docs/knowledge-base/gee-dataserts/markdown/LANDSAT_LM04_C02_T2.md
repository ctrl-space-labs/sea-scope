



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

USGS Landsat 4 MSS Collection 2 Tier 2 Raw Scenes


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================








Dataset Availability
1982\-08\-06T20:50:11Z–1992\-10\-15T05:31:24Z
Dataset Provider


[USGS](https://www.usgs.gov/landsat-missions/landsat-collection-2-level-1-data)



Earth Engine Snippet


`ee.ImageCollection("LANDSAT/LM04/C02/T2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_LM04_C02_T2)





Revisit Interval
16 Days
Tags


[c2](/earth-engine/datasets/tags/c2)
[global](/earth-engine/datasets/tags/global)
[l4](/earth-engine/datasets/tags/l4)
[landsat](/earth-engine/datasets/tags/landsat)
[lm4](/earth-engine/datasets/tags/lm4)
[mss](/earth-engine/datasets/tags/mss)
[radiance](/earth-engine/datasets/tags/radiance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[t2](/earth-engine/datasets/tags/t2)
[tier2](/earth-engine/datasets/tags/tier2)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



Landsat 4 MSS Collection 2 Tier 2 DN values, representing scaled, calibrated at\-sensor radiance.
Scenes not meeting Tier 1 criteria during
processing are assigned to Tier 2\. This includes Systematic terrain (L1GT) and
Systematic (L1GS) processed scenes, as well as any L1TP scenes that do not meet
the Tier 1 specifications due to significant cloud cover, insufficient ground
control, and other factors. Users interested in Tier 2 scenes can analyze the
RMSE and other properties to determine the suitability for use in individual
applications and studies. See more information [in the USGS
docs](https://www.usgs.gov/core-science-systems/nli/landsat/landsat-collections).





### Bands


**Bands**




| Name | Pixel Size | Wavelength | Description |
| --- | --- | --- | --- |
| `B1` | 0\.5 \- 0\.6 μm | Green |
| `B2` | 0\.6 \- 0\.7 μm | Red |
| `B3` | 0\.7 \- 0\.8 μm | Near Infrared 1 |
| `B4` | 0\.8 \- 1\.1 μm | Near Infrared 2 |
| `QA_PIXEL` | None | Landsat Collection 2 MSS QA Bitmask |
| Bitmask for QA\_PIXEL * Bit 0: Fill 	+ 0: Image data 	+ 1: Fill data * Bits 1\-2: Unused * Bit 3: Cloud 	+ 0: Not likely to exist 	+ 1: Likely to exist * Bits 4\-7: Unused * Bits 8\-9: Cloud Confidence 	+ 0: No confidence level set 	+ 1: Low confidence 	+ 2: Unused 	+ 3: High confidence | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `QA_RADSAT` | None | Radiometric saturation QA |
| Bitmask for QA\_RADSAT * Bit 0: Band 1 data saturated * Bit 1: Band 2 data saturated * Bit 2: Band 3 data saturated * Bit 3: Band 4 data saturated * Bit 4: Band 5 data saturated * Bit 5: Band 6 data saturated * Bits 6\-8: Unused * Bit 9: Dropped pixel 	+ 0: Pixel present 	+ 1: Detector does not have a value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| CLOUD\_COVER | DOUBLE | Percentage cloud cover (0\-100\), \-1 \= not calculated. |
| CLOUD\_COVER\_LAND | DOUBLE | Percentage cloud cover over land (0\-100\), \-1 \= not calculated. |
| COLLECTION\_CATEGORY | STRING | Tier of scene. (T1 or T2\) |
| COLLECTION\_NUMBER | DOUBLE | Number of collection. |
| CORRECTION\_GAIN\_BAND\_1 | STRING | Internal calibration gain method for band 1\. |
| CORRECTION\_GAIN\_BAND\_2 | STRING | Internal calibration gain method for band 2\. |
| CORRECTION\_GAIN\_BAND\_3 | STRING | Internal calibration gain method for band 3\. |
| CORRECTION\_GAIN\_BAND\_4 | STRING | Internal calibration gain method for band 4\. |
| DATA\_SOURCE\_ELEVATION | STRING | Indicates the source of the DEM used in the correction process. Possible values: "GLS2000", "RAMP", "GTOPO30".' |
| DATA\_TYPE\_L0RP | STRING | Data type identifier string used to create the L0RP product. |
| DATE\_ACQUIRED | STRING | Image acquisition date. "YYYY\-MM\-DD" |
| DATE\_PRODUCT\_GENERATED | INT | Product generation epoch. |
| DATUM | STRING | Datum used in image creation. |
| EARTH\_SUN\_DISTANCE | DOUBLE | Earth sun distance in astronomical units (AU). |
| ELLIPSOID | STRING | Ellipsoid used in image creation. |
| EPHEMERIS\_TYPE | STRING | Ephemeris data type used to perform geometric correction. (Definitive or Predictive) |
| GAIN\_BAND\_1 | STRING | Gain state for Band 1\. (L \= Low gain, H \= High) |
| GAIN\_BAND\_2 | STRING | Gain state for Band 2\. (L \= Low gain, H \= High) |
| GAIN\_BAND\_3 | STRING | Gain state for Band 3\. (L \= Low gain, H \= High) |
| GAIN\_BAND\_4 | STRING | Gain state for Band 4\. (L \= Low gain, H \= High) |
| GEOMETRIC\_RMSE\_MODEL | DOUBLE | Combined Root Mean Square Error (RMSE) of the geometric residuals (meters) in both across\-track and along\-track directions measured on the GCPs used in geometric precision correction. Not present in L1G products. |
| GEOMETRIC\_RMSE\_MODEL\_X | DOUBLE | RMSE of the X direction geometric residuals (in meters) measured on the GCPs used in geometric precision correction. Not present in L1G products. |
| GEOMETRIC\_RMSE\_MODEL\_Y | DOUBLE | RMSE of the Y direction geometric residuals (in meters) measured on the GCPs used in geometric precision correction. Not present in L1G products. |
| GEOMETRIC\_RMSE\_VERIFY | DOUBLE | RMSE of the geometric residuals (pixels) in both line and sample directions measured on the terrain\-corrected product independently using GLS2000\. |
| GEOMETRIC\_RMSE\_VERIFY\_QUAD\_LL | DOUBLE | RMSE of the geometric residuals (pixels) of the lower\-left quadrant measured on the terrain\-corrected product independently using GLS2000\. |
| GEOMETRIC\_RMSE\_VERIFY\_QUAD\_LR | DOUBLE | RMSE of the geometric residuals (pixels) of the lower\-right quadrant measured on the terrain\-corrected product independently using GLS2000\. |
| GEOMETRIC\_RMSE\_VERIFY\_QUAD\_UL | DOUBLE | RMSE of the geometric residuals (pixels) of the upper\-left quadrant measured on the terrain\-corrected product independently using GLS2000\. |
| GEOMETRIC\_RMSE\_VERIFY\_QUAD\_UR | DOUBLE | RMSE of the geometric residuals (pixels) of the upper\-right quadrant measured on the terrain\-corrected product independently using GLS2000\. |
| GRID\_CELL\_SIZE\_REFLECTIVE | DOUBLE | Grid cell size used in creating the image for the reflective band. |
| GROUND\_CONTROL\_POINTS\_MODEL | DOUBLE | The number of ground control points used. Not used in L1GT products. Values: 0 \- 999 (0 is used for L1T products that have used Multi\-scene refinement). |
| GROUND\_CONTROL\_POINTS\_VERIFY | DOUBLE | The number of ground control points used in the verification of the terrain corrected product. Values: \-1 to 1615 (\-1 \= not available) |
| GROUND\_CONTROL\_POINTS\_VERSION | DOUBLE | The number of ground control points used in the verification of the terrain corrected product. Values: \-1 to 1615 (\-1 \= not available) |
| IMAGE\_QUALITY | DOUBLE | Image quality, 0 \= worst, 9 \= best, \-1 \= quality not calculated |
| LANDSAT\_PRODUCT\_ID | STRING | The naming convention of each Landsat Collection 1 Level\-1 image based on acquisition parameters and processing parameters. Format: LXSS\_LLLL\_PPPRRR\_YYYYMMDD\_yyyymmdd\_CC\_TX* L \= Landsat * X \= Sensor (O \= Operational Land Imager, T \= Thermal Infrared Sensor, C \= Combined OLI/TIRS) * SS \= Satellite (08 \= Landsat 8\) * LLLL \= Processing Correction Level (L1TP \= precision and terrain, L1GT \= systematic terrain, L1GS \= systematic) * PPP \= WRS Path * RRR \= WRS Row * YYYYMMDD \= Acquisition Date expressed in Year, Month, Day * yyyymmdd \= Processing Date expressed in Year, Month, Day * CC \= Collection Number (01\) * TX \= Collection Category (RT \= Real Time, T1 \= Tier 1, T2 \= Tier 2\) |
| LANDSAT\_SCENE\_ID | STRING | The Pre\-Collection naming convention of each image is based on acquisition parameters. This was the naming convention used prior to Collection 1\. Format: LXSPPPRRRYYYYDDDGSIVV* L \= Landsat * X \= Sensor (O \= Operational Land Imager, T \= Thermal Infrared Sensor, C \= Combined OLI/TIRS) * S \= Satellite (08 \= Landsat 8\) * PPP \= WRS Path * RRR \= WRS Row * YYYY \= Year of Acquisition * DDD \= Julian Day of Acquisition * GSI \= Ground Station Identifier * VV \= Version |
| MAP\_PROJECTION | STRING | Projection used to represent the 3\-dimensional surface of the earth for the Level\-1 product. |
| MAP\_PROJECTION\_L0RA | STRING | L0RA map projection selectively applied to HDTs based on geographic location. Used for processed archive data. |
| ORIENTATION | STRING | Orientation used in creating the image. Values: NOMINAL \= Nominal Path, NORTH\_UP \= North Up, TRUE\_NORTH \= True North, USER \= User |
| PRESENT\_BAND\_1 | STRING | Presence of Band 1 (Y \= Yes, N \= No, M \= Missing, I \= Unknown) |
| PRESENT\_BAND\_2 | STRING | Presence of Band 2 (Y \= Yes, N \= No, M \= Missing, I \= Unknown) |
| PRESENT\_BAND\_3 | STRING | Presence of Band 3 (Y \= Yes, N \= No, M \= Missing, I \= Unknown) |
| PRESENT\_BAND\_4 | STRING | Presence of Band 4 (Y \= Yes, N \= No, M \= Missing, I \= Unknown) |
| PROCESSING\_LEVEL | DOUBLE | One of L1GS, L1GT, or L1TP. |
| PROCESSING\_SOFTWARE\_VERSION | STRING | Name and version of the processing software used to generate the L1 product. |
| RADIANCE\_ADD\_BAND\_1 | DOUBLE | Additive rescaling factor used to convert calibrated DN to radiance for Band 1\. |
| RADIANCE\_ADD\_BAND\_2 | DOUBLE | Additive rescaling factor used to convert calibrated DN to radiance for Band 2\. |
| RADIANCE\_ADD\_BAND\_3 | DOUBLE | Additive rescaling factor used to convert calibrated DN to radiance for Band 3\. |
| RADIANCE\_ADD\_BAND\_4 | DOUBLE | Additive rescaling factor used to convert calibrated DN to radiance for Band 4\. |
| RADIANCE\_MULT\_BAND\_1 | DOUBLE | Multiplicative rescaling factor used to convert calibrated Band 1 DN to radiance. |
| RADIANCE\_MULT\_BAND\_2 | DOUBLE | Multiplicative rescaling factor used to convert calibrated Band 2 DN to radiance. |
| RADIANCE\_MULT\_BAND\_3 | DOUBLE | Multiplicative rescaling factor used to convert  calibrated Band 3 DN to radiance. |
| RADIANCE\_MULT\_BAND\_4 | DOUBLE | Multiplicative rescaling factor used to convert calibrated Band 4 DN to radiance. |
| REFLECTANCE\_ADD\_BAND\_1 | DOUBLE | Additive rescaling factor used to convert calibrated Band 1 DN to reflectance. |
| REFLECTANCE\_ADD\_BAND\_2 | DOUBLE | Additive rescaling factor used to convert calibrated Band 2 DN to reflectance. |
| REFLECTANCE\_ADD\_BAND\_3 | DOUBLE | Additive rescaling factor used to convert calibrated Band 3 DN to reflectance. |
| REFLECTANCE\_ADD\_BAND\_4 | DOUBLE | Additive rescaling factor used to convert calibrated Band 4 DN to reflectance. |
| REFLECTANCE\_MULT\_BAND\_1 | DOUBLE | Multiplicative factor used to convert calibrated Band 1 DN to reflectance. |
| REFLECTANCE\_MULT\_BAND\_2 | DOUBLE | Multiplicative factor used to convert calibrated Band 2 DN to reflectance. |
| REFLECTANCE\_MULT\_BAND\_3 | DOUBLE | Multiplicative factor used to convert calibrated Band 3 DN to reflectance. |
| REFLECTANCE\_MULT\_BAND\_4 | DOUBLE | Multiplicative factor used to convert calibrated Band 4 DN to reflectance. |
| REFLECTIVE\_LINES | DOUBLE | Number of product lines for the reflective bands. |
| REFLECTIVE\_SAMPLES | DOUBLE | Number of product samples for the reflective bands. |
| REQUEST\_ID | STRING | Request id, nnnyymmdd0000\_0000* nnn \= node number * yy \= year * mm \= month * dd \= day |
| RESAMPLING\_OPTION | STRING | Resampling option used in creating the image. |
| SATURATION\_BAND\_1 | STRING | Flag indicating saturated pixels for band 1 ('Y'/'N') |
| SATURATION\_BAND\_2 | STRING | Flag indicating saturated pixels for band 2 ('Y'/'N') |
| SATURATION\_BAND\_3 | STRING | Flag indicating saturated pixels for band 3 ('Y'/'N') |
| SATURATION\_BAND\_4 | STRING | Flag indicating saturated pixels for band 4 ('Y'/'N') |
| SCENE\_CENTER\_TIME | STRING | Scene center time of acquired image. HH:MM:SS.SSSSSSSZ* HH \= Hour (00\-23\) * MM \= Minutes * SS.SSSSSSS \= Fractional seconds * Z \= "Zulu" time (same as GMT) |
| SENSOR\_ID | STRING | Sensor used to capture data. |
| SPACECRAFT\_ID | STRING | Spacecraft identification. |
| STATION\_ID | STRING | Ground Station/Organisation that received the data. |
| SUN\_AZIMUTH | DOUBLE | Sun azimuth angle in degrees for the image center location at the image center acquisition time. |
| SUN\_ELEVATION | DOUBLE | Sun elevation angle in degrees for the image center location at the image center acquisition time. |
| UTM\_ZONE | DOUBLE | UTM zone number used in product map projection. |
| WRS\_PATH | DOUBLE | The WRS orbital path number (001 \- 251\). |
| WRS\_ROW | DOUBLE | Landsat satellite WRS row (001\-248\). |
| WRS\_TYPE | DOUBLE | World Reference System (WRS) type used for the collection of this scene. |




### Terms of Use


**Terms of Use**


Landsat datasets are federally created data
and therefore reside in the public domain and may be used, transferred, or reproduced without copyright restriction.


Acknowledgement or credit of the USGS as data source should be provided
by including a line of text citation such as the example shown below.


(Product, Image, Photograph, or Dataset Name) courtesy of
the U.S. Geological Survey


Example: Landsat\-7 image courtesy of the U.S. Geological Survey


See the
[USGS Visual Identity System Guidance](https://www.usgs.gov/information-policies-and-instructions/usgs-visual-identity-system)
for further details on proper citation and acknowledgement of USGS products.




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('LANDSAT/LM04/C02/T2')
.filterDate('1989-01-01','1992-12-31');
varnearInfrared321=dataset.select(['B3','B2','B1']);
varnearInfrared321Vis={};
Map.setCenter(6.746,46.529,6);
Map.addLayer(nearInfrared321,nearInfrared321Vis,'Near Infrared (321)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_LM04_C02_T2)


[USGS Landsat 4 MSS Collection 2 Tier 2 Raw Scenes](/earth-engine/datasets/catalog/LANDSAT_LM04_C02_T2)

Landsat 4 MSS Collection 2 Tier 2 DN values, representing scaled, calibrated at\-sensor radiance. Scenes not meeting Tier 1 criteria during processing are assigned to Tier 2\. This includes Systematic terrain (L1GT) and Systematic (L1GS) processed scenes, as well as any L1TP scenes that do not meet the Tier 1 …

 LANDSAT/LM04/C02/T2,
 c2,global,l4,landsat,lm4,mss,radiance,satellite\-imagery,t2,tier2,usgs

1982\-08\-06T20:50:11Z/1992\-10\-15T05:31:24Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








