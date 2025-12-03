



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

PALSAR\-2 ScanSAR Level 2\.2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================








Dataset Availability
2014\-08\-04T00:00:00Z–2025\-06\-28T15:48:15\.364000Z
Dataset Provider


[JAXA EORC](https://www.eorc.jaxa.jp/ALOS/en/dataset/palsar2_l22_e.htm)



Earth Engine Snippet


`ee.ImageCollection("JAXA/ALOS/PALSAR-2/Level2_2/ScanSAR")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_ALOS_PALSAR-2_Level2_2_ScanSAR)





Tags


[alos2](/earth-engine/datasets/tags/alos2)
[eroc](/earth-engine/datasets/tags/eroc)
[jaxa](/earth-engine/datasets/tags/jaxa)
[palsar2](/earth-engine/datasets/tags/palsar2)
[radar](/earth-engine/datasets/tags/radar)
[sar](/earth-engine/datasets/tags/sar)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)








#### Description



The 25 m PALSAR\-2 ScanSAR is normalized backscatter data
of PALSAR\-2 broad area observation mode with observation width of 350 km.
The SAR imagery was ortho\-rectificatied and slope corrected
using the ALOS World 3D \- 30 m (AW3D30\) Digital Surface Model.
Polarization data are stored as 16\-bit digital numbers (DN).
The DN values can be converted to gamma naught values in decibel unit (dB)
using the following equation:


* γ0 \= 10\*log10(DN2) \- 83\.0 dB


Level 2\.2 data are ortho\-rectified and radiometrically terrain\-corrected.


This dataset is compatible with the
[Committee on Earth Observation (CEOS)](https://ceos.org/)
[Analysis Ready Data for LAND (CARD4L)](https://ceos.org/ard/files/PFS/NRB/v5.5/CARD4L-PFS_NRB_v5.5.pdf) standard.





### Bands



**Pixel Size**
  
25 meters



**Bands**




| Name | Units | Scale | Description |
| --- | --- | --- | --- |
| `HH` | None |  | HH polarization Terrain\-flattened Gamma\-Nought backscatter coefficient. |
| `HV` | None |  | HV polarization Terrain\-flattened Gamma\-Nought backscatter coefficient. |
| `LIN` | deg | 0\.01 | Local incidence angle. The angle formed by the radar irradiation direction and the normal of the slope. |
| `MSK` | None |  | Data quality bitmask. |
| Bitmask for MSK * Bits 0\-2: Data quality 	+ 1: Valid data 	+ 2: Layover 	+ 3: Shadowing 	+ 4: Ocean water 	+ 5: Invalid data | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| AntennaPointing | STRING | Antenna pointing direction ("Right" or "Left"). |
| AzimuthPixelSpacing | DOUBLE | Azimuth pixel spacing. |
| AzimuthResolution | DOUBLE | Azimuth resolution. |
| BeamID | STRING | Beam ID. |
| DataAccess\_ProcessingTime | STRING | Processing time of this product (ISO8601 string). |
| DataAccess\_SoftwareVersion | STRING | Software version of this product. |
| DigitalElevationModel | STRING | Type of DEM used ("Elevation" or "Surface"). |
| EasternBias | DOUBLE | Bias of easting error. |
| EasternSTDev | DOUBLE | Standard deviation of easting error. |
| Easting\_LR | DOUBLE | Easting of Lower Right of Product. |
| Easting\_UL | DOUBLE | Easting of upper left of product. |
| Estimates\_HH | DOUBLE | Estimated HH value in Noise Equivalent Intensity (NESZ). |
| Estimates\_HV | DOUBLE | Estimated HV value in Noise Equivalent Intensity (NESZ). |
| FilterApplied | STRING | Whether a filter was applied ("TRUE" or "FALSE"). |
| FilterType | STRING | Filter type (N/A if no filtering was applied). |
| FirstAcquisitionDate | STRING | Observation date of the first acquisition (ISO8601 string). |
| IDCMethod | STRING | Ionospheric delay correction ("TEC model" or "Coregistration"). |
| IncAngleFarRange | DOUBLE | Incident angle in far range. |
| IncAngleNearRange | DOUBLE | Incident angle in near range. |
| IonosphericDelayCorrectionApplied | DOUBLE | Whether ionospheric delay correction was applied ("TRUE" or "FALSE"). |
| LastAcquisitionDate | STRING | Observation date of the last acquisition (ISO 8601 string). |
| NRAlgorithm | STRING | Noise removal algorithm. |
| NoiseRemovalApplied | STRING | Whether noise removal algorithm was applied ("TRUE" or "FALSE"). |
| NorthernBias | DOUBLE | Bias of northing error. |
| NorthernSTDev | DOUBLE | Standard deviation of northing error. |
| Northing\_LR | DOUBLE | Northing of lower right of product. |
| Northing\_UL | DOUBLE | Northing of upper left of product. |
| ObservationMode | STRING | Observation mode. |
| OrbitDataSource | STRING | Orbit data source (e.g., predicted, definite, precise, downlinked). |
| PassDirection | STRING | Pass direction ("Ascending" or "Descending"). |
| Polarizations | STRING\_LIST | Transmit/Receive polarisation for the data. There is one element for each Tx/Rx combination: \['VV'], \['HH'], \['VV', 'VH'], or \['HH', 'HV']. |
| ProductColumnSpacing | DOUBLE | Product column spacing. |
| ProductRowSpacing | DOUBLE | Product row spacing. |
| Product\_Version | DOUBLE | Product version. |
| RSP\_Frame\_Number | INT | Scene frame number. |
| RSP\_Path\_Number | INT | Scene path number. |
| RadarCenterFrequency | DOUBLE | Center frequency. |
| RangePixelSpacing | DOUBLE | Range pixel spacing. |
| RangeResolution | INT | Range resolution. |
| SlantRangeCorrection | INT\_LIST | The correction for each scan described from the first scan. |
| SourceProcParam\_ProcessingDate | STRING | Processing date of the source product (ISO8601 string). |
| SourceProcParam\_ProcessingFacility | STRING | Processing facility of the source product. |
| SourceProcParam\_ProductID | STRING | Product ID of the source product. |
| SourceProcParam\_SoftwareVersion | DOUBLE | Software version of the source product. |




### Terms of Use


**Terms of Use**


Anyone can use this data free of charge subject to the to the attribution
requirements. For detailed terms of use see JAXA
[G\-Portal Terms of service](https://gportal.jaxa.jp/gpr/index/eula?lang=en)
(Section 7\. Condition concerning of G\-Portal data).




### Citations



Citations:
* The data used for this paper have been provided by Earth Observation
Research Center (EORC) of Japan Aerospace Exploration Agency (JAXA).





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcollection=ee.ImageCollection('JAXA/ALOS/PALSAR-2/Level2_2/ScanSAR')
.filterBounds(ee.Geometry.Point(143,-5));
varimage=collection.first();

Map.addLayer(image.select(['HH']),{min:0,max:8000},'HH polarization');
Map.centerObject(image);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_ALOS_PALSAR-2_Level2_2_ScanSAR)


[PALSAR\-2 ScanSAR Level 2\.2](/earth-engine/datasets/catalog/JAXA_ALOS_PALSAR-2_Level2_2_ScanSAR)

The 25 m PALSAR\-2 ScanSAR is normalized backscatter data of PALSAR\-2 broad area observation mode with observation width of 350 km. The SAR imagery was ortho\-rectificatied and slope corrected using the ALOS World 3D \- 30 m (AW3D30\) Digital Surface Model. Polarization data are stored as 16\-bit digital numbers (DN). …

 JAXA/ALOS/PALSAR\-2/Level2\_2/ScanSAR,
 alos2,eroc,jaxa,palsar2,radar,sar,satellite\-imagery

2014\-08\-04T00:00:00Z/2025\-06\-28T15:48:15\.364000Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








