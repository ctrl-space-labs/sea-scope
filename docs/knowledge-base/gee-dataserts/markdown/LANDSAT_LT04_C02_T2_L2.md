



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

USGS Landsat 4 Level 2, Collection 2, Tier 2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================








Dataset Availability
1982\-08\-22T14:18:20Z–1993\-11\-18T14:54:14Z
Dataset Provider


[USGS](https://www.usgs.gov/core-science-systems/nli/landsat/landsat-collection-2-level-2-science-products)



Earth Engine Snippet


`ee.ImageCollection("LANDSAT/LT04/C02/T2_L2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_LT04_C02_T2_L2)





Revisit Interval
16 Days
Tags


[cfmask](/earth-engine/datasets/tags/cfmask)
[cloud](/earth-engine/datasets/tags/cloud)
[fmask](/earth-engine/datasets/tags/fmask)
[global](/earth-engine/datasets/tags/global)
[landsat](/earth-engine/datasets/tags/landsat)
[lasrc](/earth-engine/datasets/tags/lasrc)
[lst](/earth-engine/datasets/tags/lst)
[lt04](/earth-engine/datasets/tags/lt04)
[reflectance](/earth-engine/datasets/tags/reflectance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sr](/earth-engine/datasets/tags/sr)
[tm](/earth-engine/datasets/tags/tm)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



This dataset contains atmospherically corrected
surface reflectance and land surface temperature derived from the data
produced by the Landsat TM sensor.
These images contain 4 visible and near\-infrared (VNIR) bands and
2 short\-wave infrared (SWIR) bands processed to orthorectified surface
reflectance, and one thermal infrared (TIR) band processed to orthorectified
surface temperature. They also contain intermediate bands used in
calculation of the ST products, as well as QA bands.


Landsat 4 and 5 SR products are created with the Landsat Ecosystem Disturbance
Adaptive Processing System (LEDAPS) algorithm (version 3\.4\.0\).
All Collection 2 ST products are created with a single\-channel algorithm
jointly created by the Rochester Institute of Technology (RIT) and
National Aeronautics and Space Administration (NASA)
Jet Propulsion Laboratory (JPL).


Strips of collected data are packaged into overlapping "scenes" covering approximately
170km x 183km using a [standardized reference grid](https://landsat.gsfc.nasa.gov/about/worldwide-reference-system).


Some assets have only SR data, in which case ST bands are present but empty.
For assets with both ST and SR bands, 'PROCESSING\_LEVEL' is set to 'L2SP'.
For assets with only SR bands, 'PROCESSING\_LEVEL' is set to 'L2SR'.


[Additional documentation and usage examples.](/earth-engine/guides/landsat)


Data provider notes:


* Data products must contain both optical and thermal data to be
successfully processed to surface temperature, as ASTER NDVI is
required to temporally adjust the ASTER GED product to the target Landsat
scene. Therefore, night time acquisitions cannot be processed to
surface temperature.
* A known error exists in the surface temperature retrievals relative
to clouds and possibly cloud shadows. The characterization of these
issues has been documented by
[Cook et al., (2014\)](https://doi.org/10.3390/rs61111244).
* ASTER GED contains areas of missing mean emissivity data required for
successful ST product generation. If there is missing ASTER GED
information, there will be missing ST data in those areas.
* The ASTER GED dataset is created from all clear\-sky pixels of ASTER scenes
acquired from 2000 through 2008\. While this dataset has a global spatial
extent, there are areas missing mean emissivity information due to
persistent cloud contamination in the ASTER measurements.
* The USGS further screens unphysical values (emissivity \< 0\.6\) in ASTER
GED to remove any emissivity underestimation due to undetected clouds. For
any given pixel with no ASTER GED input or unphysical emissivity value,
the resulting Landsat ST products have missing pixels. The missing Landsat
ST pixels will be consistent through time (1982\-present) given the static
nature of ASTER GED mean climatology data. For more information refer to
[landsat\-collection\-2\-surface\-temperature\-data\-gaps\-due\-missing](https://www.usgs.gov/landsat-missions/landsat-collection-2-surface-temperature-data-gaps-due-missing-aster-ged)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Scale | Offset | Wavelength | Description |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `SR_B1` | None | 1 | 65455 | 2\.75e\-05 | \-0\.2 | 0\.45\-0\.52 μm | Band 1 (blue) surface reflectance |
| `SR_B2` | None | 1 | 65455 | 2\.75e\-05 | \-0\.2 | 0\.52\-0\.60 μm | Band 2 (green) surface reflectance |
| `SR_B3` | None | 1 | 65455 | 2\.75e\-05 | \-0\.2 | 0\.63\-0\.69 μm | Band 3 (red) surface reflectance |
| `SR_B4` | None | 1 | 65455 | 2\.75e\-05 | \-0\.2 | 0\.77\-0\.90 μm | Band 4 (near infrared) surface reflectance |
| `SR_B5` | None | 1 | 65455 | 2\.75e\-05 | \-0\.2 | 1\.55\-1\.75 μm | Band 5 (shortwave infrared 1\) surface reflectance |
| `SR_B7` | None | 1 | 65455 | 2\.75e\-05 | \-0\.2 | 2\.08\-2\.35 μm | Band 7 (shortwave infrared 2\) surface reflectance |
| `SR_ATMOS_OPACITY` | None | 0 | 10000 | 0\.001 |  | None | A general interpretation of atmospheric opacity generated by LEDAPS and based on the radiance viewed over Dark Dense Vegetation (DDV) within the scene. A general interpretation of atmospheric opacity is that values (after scaling by 0\.001 is applied) less than 0\.1 are clear, 0\.1\-0\.3 are average, and values greater than 0\.3 indicate haze or other cloud situations. SR values from pixels with high atmospheric opacity will be less reliable, especially under high solar zenith angle conditions. The SR\_ATMOS\_OPACITY band is provided for advanced users and for product quality assessment and has not been validated. Most users are advised to instead use the QA\_PIXEL band information for cloud discrimination. |
| `SR_CLOUD_QA` | None |  |  | None | Cloud Quality Assessment |
| Bitmask for SR\_CLOUD\_QA * Bit 0: Dark Dense Vegetation (DDV) * Bit 1: Cloud * Bit 2: Cloud Shadow * Bit 3: Adjacent to Cloud * Bit 4: Snow * Bit 5: Water | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `ST_B6` | K | 0 | 65535 | 0\.00341802 | 149 | 10\.40\-12\.50 μm | Band 6 surface temperature. If 'PROCESSING\_LEVEL' is set to 'L2SR', this band is fully masked out. |
| `ST_ATRAN` | None | 0 | 10000 | 0\.0001 |  | None | Atmospheric Transmittance. If 'PROCESSING\_LEVEL' is set to 'L2SR', this band is fully masked out. |
| `ST_CDIST` | km | 0 | 24000 | 0\.01 |  | None | Pixel distance to cloud. If 'PROCESSING\_LEVEL' is set to 'L2SR', this band is fully masked out. |
| `ST_DRAD` | W/(m^2\*sr\*um)/ DN | 0 | 28000 | 0\.001 |  | None | Downwelled Radiance. If 'PROCESSING\_LEVEL' is set to 'L2SR', this band is fully masked out. |
| `ST_EMIS` | None | 0 | 10000 | 0\.0001 |  | None | Emissivity estimated from ASTER GED. If 'PROCESSING\_LEVEL' is set to 'L2SR', this band is fully masked out. |
| `ST_EMSD` | None | 0 | 10000 | 0\.0001 |  | None | Emissivity standard deviation. If 'PROCESSING\_LEVEL' is set to 'L2SR', this band is fully masked out. |
| `ST_QA` | K | 0 | 32767 | 0\.01 |  | None | Uncertainty of the Surface Temperature band. If 'PROCESSING\_LEVEL' is set to 'L2SR', this band is fully masked out. |
| `ST_TRAD` | W/(m^2\*sr\*um)/ DN | 0 | 22000 | 0\.001 |  | None | Thermal band converted to radiance. If 'PROCESSING\_LEVEL' is set to 'L2SR', this band is fully masked out. |
| `ST_URAD` | W/(m^2\*sr\*um)/ DN | 0 | 28000 | 0\.001 |  | None | Upwelled Radiance. If 'PROCESSING\_LEVEL' is set to 'L2SR', this band is fully masked out. |
| `QA_PIXEL` | None |  |  | None | Pixel quality attributes generated from the CFMASK algorithm. |
| Bitmask for QA\_PIXEL * Bit 0: Fill * Bit 1: Dilated Cloud * Bit 2: Unused * Bit 3: Cloud * Bit 4: Cloud Shadow * Bit 5: Snow * Bit 6: Clear 	+ 0: Cloud or Dilated Cloud bits are set 	+ 1: Cloud and Dilated Cloud bits are not set * Bit 7: Water * Bits 8\-9: Cloud Confidence 	+ 0: None 	+ 1: Low 	+ 2: Medium 	+ 3: High * Bits 10\-11: Cloud Shadow Confidence 	+ 0: None 	+ 1: Low 	+ 2: Medium 	+ 3: High * Bits 12\-13: Snow/Ice Confidence 	+ 0: None 	+ 1: Low 	+ 2: Medium 	+ 3: High * Bits 14\-15: Cirrus Confidence 	+ 0: None 	+ 1: Low 	+ 2: Medium 	+ 3: High | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `QA_RADSAT` | None |  |  | None | Radiometric saturation QA |
| Bitmask for QA\_RADSAT * Bit 0: Band 1 data saturated * Bit 1: Band 2 data saturated * Bit 2: Band 3 data saturated * Bit 3: Band 4 data saturated * Bit 4: Band 5 data saturated * Bit 5: Band 6L data saturated * Bit 6: Band 7 data saturated * Bit 7: Unused * Bit 8: Band 6H data saturated * Bit 9: Dropped pixel 	+ 0: Pixel present 	+ 1: Detector doesn't have a value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| ALGORITHM\_SOURCE\_SURFACE\_REFLECTANCE | STRING | Name and version of the surface reflectance algorithm. |
| ALGORITHM\_SOURCE\_SURFACE\_TEMPERATURE | STRING | Name and version of the surface temperature algorithm. |
| CLOUD\_COVER | DOUBLE | Percentage cloud cover (0\-100\), \-1 \= not calculated. |
| CLOUD\_COVER\_LAND | DOUBLE | Percentage cloud cover over land (0\-100\), \-1 \= not calculated. |
| COLLECTION\_CATEGORY | STRING | Scene collection category, "T1" or "T2". |
| DATA\_SOURCE\_AIR\_TEMPERATURE | STRING | Air temperature data source. |
| DATA\_SOURCE\_ELEVATION | STRING | Elevation data source. |
| DATA\_SOURCE\_OZONE | STRING | Ozone data source. |
| DATA\_SOURCE\_PRESSURE | STRING | Pressure data source. |
| DATA\_SOURCE\_REANALYSIS | STRING | Reanalysis data source. |
| DATA\_SOURCE\_WATER\_VAPOR | STRING | Water vapor data source. |
| DATE\_PRODUCT\_GENERATED | DOUBLE | Timestamp of the date when the product was generated. |
| EARTH\_SUN\_DISTANCE | DOUBLE | Earth\-Sun distance (AU). |
| EPHEMERIS\_TYPE | STRING | Identifier to inform the user of the orbital ephemeris type used: "DEFINITIVE" or "PREDICTIVE". If the field is not present, the user should assume "PREDICTIVE". |
| GEOMETRIC\_RMSE\_MODEL | DOUBLE | Combined RMSE (Root Mean Square Error) of the geometric residuals (meters) in both across\-track and along\-track directions. This parameter is only present if the L1\_PROCESSING\_LEVEL is L1TP. |
| GEOMETRIC\_RMSE\_MODEL\_X | DOUBLE | RMSE (Root Mean Square Error) of the geometric residuals (meters) measured on the GCPs (Ground Control Points) used in geometric precision correction in the across\-track direction. This parameter is only present if the L1\_PROCESSING\_LEVEL is L1TP. |
| GEOMETRIC\_RMSE\_MODEL\_Y | DOUBLE | RMSE (Root Mean Square Error) of the geometric residuals (meters) measured on the GCPs (Ground Control Points) used in geometric precision correction in the along\-track direction. This parameter is only present if the L1\_PROCESSING\_LEVEL is L1TP. |
| GROUND\_CONTROL\_POINTS\_MODEL | DOUBLE | Number of GCPs used in the precision correction process. This parameter is only present if the L1\_PROCESSING\_LEVEL is L1TP. |
| GROUND\_CONTROL\_POINTS\_VERSION | DOUBLE | GCP dataset version used in the precision correction process. This parameter is only present if the L1\_PROCESSING\_LEVEL is L1TP. |
| IMAGE\_QUALITY | INT | Composite image quality for the bands. 0 \= worst, 9 \= best, \-1 \= quality not calculated or assessed. |
| L1\_DATE\_PRODUCT\_GENERATED | STRING | Product generation date for the corresponding L1 product. |
| L1\_LANDSAT\_PRODUCT\_ID | STRING | Landsat Product Identifier for the corresponding L1 product. |
| L1\_PROCESSING\_LEVEL | STRING | Processing Level for the corresponding L1 product. |
| L1\_PROCESSING\_SOFTWARE\_VERSION | STRING | Processing software version for the corresponding L1 product. |
| LANDSAT\_PRODUCT\_ID | STRING | Landsat Product Identifier |
| LANDSAT\_SCENE\_ID | STRING | Short Landsat Scene Identifier |
| PROCESSING\_LEVEL | STRING | "L2SP" when both SR and LST bands are present, or "L2SR" when only SR bands are present. |
| PROCESSING\_SOFTWARE\_VERSION | STRING | The processing software version that created the product. |
| SCENE\_CENTER\_TIME | STRING | Time of the observations as in ISO 8601 string. |
| SENSOR\_ID | STRING | Name of the sensor. |
| SPACECRAFT\_ID | STRING | Name of the spacecraft. |
| SUN\_AZIMUTH | DOUBLE | Sun azimuth angle in degrees for the image center location at the image center acquisition time. A positive value indicates angles to the east or clockwise from the north. A negative value indicates angles to the west or counterclockwise from the north. |
| SUN\_ELEVATION | DOUBLE | Sun elevation angle in degrees for the image center location at the image center acquisition time. A positive value indicates a daytime scene. A negative value indicates a nighttime scene. Note: For reflectance calculation, the sun zenith angle is needed, which is 90 \- sun elevation angle. |
| TEMPERATURE\_MAXIMUM\_BAND\_ST\_B6 | DOUBLE | Maximum achievable temperature value for Band 6\. |
| TEMPERATURE\_MINIMUM\_BAND\_ST\_B6 | DOUBLE | Minimum achievable temperature value for Band 6\. |
| WRS\_PATH | INT | WRS path number of scene. |
| WRS\_ROW | INT | WRS row number of scene. |




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
vardataset=ee.ImageCollection('LANDSAT/LT04/C02/T2_L2')
.filterDate('1990-04-01','1990-05-01');

// Applies scaling factors.
functionapplyScaleFactors(image){
varopticalBands=image.select('SR_B.').multiply(0.0000275).add(-0.2);
varthermalBand=image.select('ST_B6').multiply(0.00341802).add(149.0);
returnimage.addBands(opticalBands,null,true)
.addBands(thermalBand,null,true);
}

dataset=dataset.map(applyScaleFactors);

varvisualization={
bands:['SR_B3','SR_B2','SR_B1'],
min:0.0,
max:0.3,
};

Map.setCenter(-83,24,8);

Map.addLayer(dataset,visualization,'True Color (321)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/LANDSAT/LANDSAT_LT04_C02_T2_L2)


[USGS Landsat 4 Level 2, Collection 2, Tier 2](/earth-engine/datasets/catalog/LANDSAT_LT04_C02_T2_L2)

This dataset contains atmospherically corrected surface reflectance and land surface temperature derived from the data produced by the Landsat TM sensor. These images contain 4 visible and near\-infrared (VNIR) bands and 2 short\-wave infrared (SWIR) bands processed to orthorectified surface reflectance, and one thermal infrared (TIR) band processed to orthorectified …

 LANDSAT/LT04/C02/T2\_L2,
 cfmask,cloud,fmask,global,landsat,lasrc,lst,lt04,reflectance,satellite\-imagery,sr,tm,usgs

1982\-08\-22T14:18:20Z/1993\-11\-18T14:54:14Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








