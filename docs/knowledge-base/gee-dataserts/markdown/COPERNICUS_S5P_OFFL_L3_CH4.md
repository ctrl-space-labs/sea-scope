



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Sentinel\-5P OFFL CH4: Offline Methane


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================








Dataset Availability
2019\-02\-08T08:13:16Z–2025\-07\-12T19:09:33Z
Dataset Provider


[European Union/ESA/Copernicus](https://sentinel.esa.int/web/sentinel/user-guides/sentinel-5p-tropomi)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/S5P/OFFL/L3_CH4")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_OFFL_L3_CH4)





Revisit Interval
2 Days
Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[copernicus](/earth-engine/datasets/tags/copernicus)
[esa](/earth-engine/datasets/tags/esa)
[eu](/earth-engine/datasets/tags/eu)
[knmi](/earth-engine/datasets/tags/knmi)
[methane](/earth-engine/datasets/tags/methane)
[s5p](/earth-engine/datasets/tags/s5p)
[sentinel](/earth-engine/datasets/tags/sentinel)
[sron](/earth-engine/datasets/tags/sron)
[tropomi](/earth-engine/datasets/tags/tropomi)








#### Description



### OFFL/L3\_CH4


This dataset provides offline high\-resolution imagery of methane
concentrations.


Methane (CH4) is, after carbon dioxide (CO2), the most
important contributor to the anthropogenically enhanced greenhouse effect.
Roughly three\-quarters of methane emissions are anthropogenic and as such, it
is important to continue the record of satellite based measurements. TROPOMI
aims at providing CH4 column concentrations with high sensitivity
to the Earth's surface, good spatiotemporal coverage, and sufficient
accuracy to facilitate inverse modeling of sources and sinks. TROPOMI uses
absorption information from the Oxygen\-A Band (760nm) and the SWIR spectral
range to monitor CH4 abundances in the Earth's atmosphere.
[More information.](http://www.tropomi.eu/data-products/methane)


Currently, the following data quality issues are known, are not covered by
the quality flags, and should be kept in mind when looking at the methane
product and also at preliminary validation results. For more details, see
the [MPC VDAF website](http://mpc-vdaf.tropomi.eu).


Filtering on qa\_value \< 0\.5 does not remove all pixels considered bad.
Some pixels with too low methane concentrations are still present:


* Single TROPOMI overpasses show stripes of erroneous CH4 values
in the flight direction.
* Not all pixels above inland water are filtered.
* Uncertainties for the XCH4 is only based on the single
sounding precision due to measurement noise. For applications requiring
an overall uncertainty estimate, we propose to multiply the provided
error by a factor 2, which reflects the scatter of single sounding errors
in the TCCON validation.
* Data prior to November 2021 only provides XCH4 over land,
after which glint ocean observations were added.
* No data are present between 2022\-07\-26 and 2022\-08\-31 due to a
[provider outage](https://scihub.copernicus.eu/news/News01082).


### OFFL L3 Product


To make our OFFL L3 products, we find which areas within the product's
bounding box contain data by using a command like this:



```
harpconvert --format hdf5 --hdf5-compression 9
-a 'CH4_column_volume_mixing_ratio_dry_air_validity>50;derive(datetime_stop {time})'
S5P_OFFL_L2__CH4____20190223T202409_20190223T220540_07072_01_010202_20190301T221106.nc
grid_info.h5

```

We then merge all the data into one large mosaic (area\-averaging values for
pixels that may have different values for different times). From the
mosaic, we create a set of tiles containing orthorectified raster data.


Example harpconvert invocation for one tile:
`harpconvert --format hdf5 --hdf5-compression 9
-a 'CH4_column_volume_mixing_ratio_dry_air_validity>50;
derive(datetime_stop {time});
bin_spatial(2001, 50.000000, 0.01, 2001, -120.000000, 0.01);
keep(CH4_column_volume_mixing_ratio_dry_air, aerosol_height,
aerosol_optical_depth, sensor_azimuth_angle, sensor_zenith_angle,
solar_azimuth_angle, solar_zenith_angle)'
S5P_OFFL_L2__CH4____20190223T202409_20190223T220540_07072_01_010202_20190301T221106.nc
output.h5`


### Sentinel\-5 Precursor


Sentinel\-5 Precursor is a satellite launched on 13 October 2017
by the European Space Agency to monitor air pollution. The onboard sensor
is frequently referred to as Tropomi (TROPOspheric Monitoring Instrument).


All of the S5P datasets, except CH4, have two versions: Near 
Real\-Time (NRTI) and Offline (OFFL). CH4 is available as OFFL only. 
The NRTI assets cover a smaller area than the OFFL assets, but appear more 
quickly after acquisition. The OFFL assets contain data from a single orbit 
(which, due to half the earth being dark, contains data only for a single 
hemisphere).


Because of noise in the data, negative vertical column values are often
observed in particular over clean regions or for low SO2 emissions. It is
recommended not to filter these values except for outliers, i.e.
for vertical columns lower than \-0\.001 mol/m^2\.


The original Sentinel 5P Level 2 (L2\) data is binned
by time, not by latitude/longitude. To make it possible to ingest the data
into Earth Engine, each Sentinel 5P L2 product is converted to L3, keeping
a single grid per orbit (that is, no aggregation across products
is performed).


Source products spanning the antimeridian are ingested as two Earth Engine
assets, with suffixes \_1 and \_2\.


The conversion to L3 is done by the [harpconvert](https://cdn.rawgit.com/stcorp/harp/master/doc/html/harpconvert.html)
tool using the `bin_spatial` operation. The source data is filtered to
remove pixels with QA values less than:


* 80% for AER\_AI
* 75% for the tropospheric\_NO2\_column\_number\_density band of NO2
* 50% for all other datasets except for O3 and SO2


The O3\_TCL product is ingested directly (without running harpconvert).





### Bands



**Pixel Size**
  
1113\.2 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `CH4_column_volume_mixing_ratio_dry_air` | Mol fraction | 1285\* | 2405\* | Column\-averaged dry air mixing ratio of methane, as parts\-per\-billion |
| `aerosol_height` | m | 906\* | 11251\* | Aerosol height parameter in the CH4 retrieval |
| `aerosol_optical_depth` | None | 0\.00032\* | 0\.2405\* | aerosol optical thickness in the SWIR band |
| `sensor_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the satellite at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `sensor_zenith_angle` | deg | 1\* | 60\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |
| `solar_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the Sun at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `solar_zenith_angle` | deg | 6\* | 70\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |
| `CH4_column_volume_mixing_ratio_dry_air_bias_corrected` | Mol fraction | 1295\* | 2432\* | Column\-averaged dry air mixing ratio of methane, as parts\-per\-billion, corrected for surface albedo |
| `CH4_column_volume_mixing_ratio_dry_air_uncertainty` | Mol fraction | 0\* | 10\* | Uncertainty of the column averaged dry air mixing ratio of methane (1 sigma error) |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| ALGORITHM\_VERSION | STRING | The algorithm version used in L2 processing. It is separate from the processor (framework) version, to accommodate different release schedules for different products. |
| BUILD\_DATE | STRING | The date, expressed as milliseconds since 1 Jan 1970, when the software used to perform L2 processing was built. |
| HARP\_VERSION | INT | The version of the HARP tool used to grid the L2 data into an L3 product. |
| INSTITUTION | STRING | The institution where data processing from L1 to L2 was performed. |
| L3\_PROCESSING\_TIME | INT | The date, expressed as milliseconds since 1 Jan 1970, when Google processed the L2 data into L3 using harpconvert. |
| LAT\_MAX | DOUBLE | The maximum latitude of the asset (degrees). |
| LAT\_MIN | DOUBLE | The minimum latitude of the asset (degrees). |
| LON\_MAX | DOUBLE | The maximum longitude of the asset (degrees). |
| LON\_MIN | DOUBLE | The minimum longitude of the asset (degrees). |
| ORBIT | INT | The orbit number of the satellite when the data was acquired. |
| PLATFORM | STRING | Name of the platform which acquired the data. |
| PROCESSING\_STATUS | STRING | The processing status of the product on a global level, mainly based on the availability of auxiliary input data. Possible values are "Nominal" and "Degraded". |
| PROCESSOR\_VERSION | STRING | The version of the software used for L2 processing, as a string of the form "major.minor.patch". |
| PRODUCT\_ID | STRING | Id of the L2 product used to generate this asset. |
| PRODUCT\_QUALITY | STRING | Indicator that specifies whether the product quality is degraded or not. Allowed values are "Degraded" and "Nominal". |
| SENSOR | STRING | Name of the sensor which acquired the data. |
| SPATIAL\_RESOLUTION | STRING | Spatial resolution at nadir. For most products this is `3.5x7 km2`, except for `L2__O3__PR`, which uses `28x21km2`, and `L2__CO____` and `L2__CH4___`, which both use `7x7 km2`. This attribute originates from the CCI standard. |
| TIME\_REFERENCE\_DAYS\_SINCE\_1950 | INT | Days from 1 Jan 1950 to when the data was acquired. |
| TIME\_REFERENCE\_JULIAN\_DAY | DOUBLE | The Julian day number when the data was acquired. |
| TRACKING\_ID | STRING | UUID for the L2 product file. |




### Terms of Use


**Terms of Use**


The use of Sentinel data is governed by the [Copernicus
Sentinel Data Terms and Conditions.](https://sentinel.esa.int/documents/247904/690755/Sentinel_Data_Legal_Notice)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcollection=ee.ImageCollection('COPERNICUS/S5P/OFFL/L3_CH4')
.select('CH4_column_volume_mixing_ratio_dry_air')
.filterDate('2019-06-01','2019-07-16');

varband_viz={
min:1750,
max:1900,
palette:['black','blue','purple','cyan','green','yellow','red']
};

Map.addLayer(collection.mean(),band_viz,'S5P CH4');
Map.setCenter(0.0,0.0,2);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_OFFL_L3_CH4)


[Sentinel\-5P OFFL CH4: Offline Methane](/earth-engine/datasets/catalog/COPERNICUS_S5P_OFFL_L3_CH4)

OFFL/L3\_CH4 This dataset provides offline high\-resolution imagery of methane concentrations. Methane (CH4\) is, after carbon dioxide (CO2\), the most important contributor to the anthropogenically enhanced greenhouse effect. Roughly three\-quarters of methane emissions are anthropogenic and as such, it is important to continue the record of satellite based measurements. TROPOMI aims …

 COPERNICUS/S5P/OFFL/L3\_CH4,
 atmosphere,climate,copernicus,esa,eu,knmi,methane,s5p,sentinel,sron,tropomi

2019\-02\-08T08:13:16Z/2025\-07\-12T19:09:33Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








