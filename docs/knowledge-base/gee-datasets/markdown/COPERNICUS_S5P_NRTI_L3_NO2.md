



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Sentinel\-5P NRTI NO2: Near Real\-Time Nitrogen Dioxide


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================================








Dataset Availability
2018\-07\-10T10:05:44Z–2025\-07\-14T14:01:39Z
Dataset Provider


[European Union/ESA/Copernicus](https://sentinel.esa.int/web/sentinel/user-guides/sentinel-5p-tropomi)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/S5P/NRTI/L3_NO2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_NRTI_L3_NO2)





Revisit Interval
2 Days
Tags


[air\-quality](/earth-engine/datasets/tags/air-quality)
[atmosphere](/earth-engine/datasets/tags/atmosphere)
[copernicus](/earth-engine/datasets/tags/copernicus)
[esa](/earth-engine/datasets/tags/esa)
[eu](/earth-engine/datasets/tags/eu)
[knmi](/earth-engine/datasets/tags/knmi)
[nitrogen\-dioxide](/earth-engine/datasets/tags/nitrogen-dioxide)
[no2](/earth-engine/datasets/tags/no2)
[pollution](/earth-engine/datasets/tags/pollution)
[s5p](/earth-engine/datasets/tags/s5p)
[sentinel](/earth-engine/datasets/tags/sentinel)
[tropomi](/earth-engine/datasets/tags/tropomi)








#### Description



### NRTI/L3\_NO2


This dataset provides near real\-time high\-resolution imagery of NO2 concentrations.


Nitrogen oxides (NO2 and NO) are important trace gases in the Earth's atmosphere,
present in both the troposphere and the stratosphere. They enter the atmosphere
as a result of anthropogenic activities (notably fossil fuel combustion and
biomass burning) and natural processes (wildfires, lightning, and microbiological processes in
soils). Here, NO2 is used to represent concentrations
of collective nitrogen oxides because during daytime, i.e. in the presence of
sunlight, a photochemical cycle involving ozone (O3) converts NO into NO2
and vice versa on a timescale of minutes. The TROPOMI NO2 processing system is based
on the algorithm developments for the DOMINO\-2 product and for the EU QA4ECV NO2
reprocessed dataset for OMI, and has been adapted for TROPOMI. This
retrieval\-assimilation\-modelling system uses the 3\-dimensional global TM5\-MP
chemistry transport model at a resolution of 1x1 degree as an essential element.
[More information.](http://www.tropomi.eu/data-products/nitrogen-dioxide)


### NRTI L3 Product


To make our NRTI L3 products, we use [harpconvert](https://stcorp.github.io/harp/doc/html/harpconvert.html)
to grid the data.


Example harpconvert invocation for one tile:
`harpconvert --format hdf5 --hdf5-compression 9
-a 'tropospheric_NO2_column_number_density_validity>50;derive(datetime_stop {time});
bin_spatial(2001, 50.000000, 0.01, 2001, -120.000000, 0.01);
keep(NO2_column_number_density,tropospheric_NO2_column_number_density,
 stratospheric_NO2_column_number_density,NO2_slant_column_number_density,
 tropopause_pressure,absorbing_aerosol_index,cloud_fraction,
 sensor_altitude,sensor_azimuth_angle,
 sensor_zenith_angle,solar_azimuth_angle,solar_zenith_angle)'
S5P_NRTI_L2__NO2____20181107T013042_20181107T013542_05529_01_010200_20181107T021824.nc
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
| `NO2_column_number_density` | mol/m^2 | \-0\.0006\* | 0\.0096\* | Total vertical column of NO2 (ratio of the slant column density of NO2 and the total air mass factor). |
| `tropospheric_NO2_column_number_density` | mol/m^2 | \-0\.00064\* | 0\.0096\* | tropospheric vertical column of NO2 |
| `stratospheric_NO2_column_number_density` | mol/m^2 | 8\.7e\-06\* | 0\.0001\* | stratospheric vertical column of NO2 |
| `NO2_slant_column_number_density` | mol/m^2 | 1\.4e\-05\* | 0\.003908\* | NO2 slant column density |
| `tropopause_pressure` | Pa | \-0\.000644\* | 0\.009614\* | topopause pressure |
| `absorbing_aerosol_index` | Dimensionless | \-14\.43\* | 10\.67\* | Aerosol index (at wavelengths 354/388 nm, i.e. the OMI pair) from the AER\_AI level 2 product. See [Level 2 Algorithms \- Ultraviolet Aerosol Index](https://sentinel.esa.int/web/sentinel/data-products/-/asset_publisher/fp37fc19FN8F/content/sentinel-5-precursor-level-2-ultraviolet-aerosol-index). |
| `cloud_fraction` | Fraction | 0\* | 1\* | Effective cloud fraction. See the [Sentinel 5P L2 Input/Output Data Definition Spec](https://sentinels.copernicus.eu/documents/247904/3119978/Sentinel-5P-Level-2-Input-Output-Data-Definition), p.220\. |
| `sensor_altitude` | m | 828543\* | 856078\* | Altitude of the satellite with respect to the geodetic sub\-satellite point (WGS84\). |
| `sensor_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the satellite at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `sensor_zenith_angle` | deg | 0\.098\* | 67\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |
| `solar_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the Sun at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `solar_zenith_angle` | deg | 8\* | 82\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |


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
varcollection=ee.ImageCollection('COPERNICUS/S5P/NRTI/L3_NO2')
.select('NO2_column_number_density')
.filterDate('2019-06-01','2019-06-06');

varband_viz={
min:0,
max:0.0002,
palette:['black','blue','purple','cyan','green','yellow','red']
};

Map.addLayer(collection.mean(),band_viz,'S5P N02');
Map.setCenter(65.27,24.11,4);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_NRTI_L3_NO2)


[Sentinel\-5P NRTI NO2: Near Real\-Time Nitrogen Dioxide](/earth-engine/datasets/catalog/COPERNICUS_S5P_NRTI_L3_NO2)

NRTI/L3\_NO2 This dataset provides near real\-time high\-resolution imagery of NO2 concentrations. Nitrogen oxides (NO2 and NO) are important trace gases in the Earth's atmosphere, present in both the troposphere and the stratosphere. They enter the atmosphere as a result of anthropogenic activities (notably fossil fuel combustion and biomass burning) and …

 COPERNICUS/S5P/NRTI/L3\_NO2,
 air\-quality,atmosphere,copernicus,esa,eu,knmi,nitrogen\-dioxide,no2,pollution,s5p,sentinel,tropomi

2018\-07\-10T10:05:44Z/2025\-07\-14T14:01:39Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








