



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Sentinel\-5P OFFL O3: Offline Ozone


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================








Dataset Availability
2018\-09\-08T21:19:29Z–2025\-07\-12T17:28:04Z
Dataset Provider


[European Union/ESA/Copernicus](https://sentinel.esa.int/web/sentinel/user-guides/sentinel-5p-tropomi)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/S5P/OFFL/L3_O3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_OFFL_L3_O3)





Revisit Interval
2 Days
Tags


[air\-quality](/earth-engine/datasets/tags/air-quality)
[atmosphere](/earth-engine/datasets/tags/atmosphere)
[copernicus](/earth-engine/datasets/tags/copernicus)
[esa](/earth-engine/datasets/tags/esa)
[eu](/earth-engine/datasets/tags/eu)
[o3](/earth-engine/datasets/tags/o3)
[ozone](/earth-engine/datasets/tags/ozone)
[pollution](/earth-engine/datasets/tags/pollution)
[s5p](/earth-engine/datasets/tags/s5p)
[sentinel](/earth-engine/datasets/tags/sentinel)
[tropomi](/earth-engine/datasets/tags/tropomi)








#### Description



### OFFL/L3\_O3


This dataset provides offline high\-resolution imagery of total column ozone
concentrations. See also `COPERNICUS/S5P/OFFL/L3_O3_TCL` for the tropospheric
column data.


In the stratosphere, the ozone layer shields the biosphere from dangerous
solar ultraviolet radiation. In the troposphere, it acts as an efficient
cleansing agent, but at high concentration it also becomes harmful to the
health of humans, animals, and vegetation. Ozone is also an important
greenhouse\-gas contributor to ongoing climate change. Since the discovery
of the Antarctic ozone hole in the 1980s and the subsequent Montreal Protocol
regulating the production of chlorine\-containing ozone\-depleting substances,
ozone has been routinely monitored from the ground and from space.


For this product, there are two algorithms that deliver total ozone: GDP for
the near real\-time and GODFIT for the offline products. GDP is currently
being used for generating the operational total ozone products from GOME,
SCIAMACHY and GOME\-2; while GODFIT is being used in the ESA CCI and the
Copernicus C3S projects.
[More information.](http://www.tropomi.eu/data-products/total-ozone-column)
[Product user manual](https://sentinel.esa.int/documents/247904/2474726/Sentinel-5P-Level-2-Product-User-Manual-Ozone-Total-Column)


### OFFL L3 Product


To make our OFFL L3 products, we find areas within the product's bounding
box with data using a command like this:



```
harpconvert --format hdf5 --hdf5-compression 9
-a 'O3_column_number_density_validity>50;derive(datetime_stop {time})'
S5P_OFFL_L2__O3_____20181005T225147_20181006T003317_05073_01_010102_20181012T001415.nc
grid_info.h5

```

We then merge all the data into one large mosaic (area\-averaging values for
pixels that may have different values for different times). From the
mosaic, we create a set of tiles containing orthorectified raster data.


The qa value is adjusted before running harpconvert to satisfy all of the
following criteria:


* ozone\_total\_vertical\_column in \[0, 0\.45]
* ozone\_effective\_temperature in \[180, 260]
* ring\_scale\_factor in \[0, 0\.15]
* effective\_albedo in \[\-0\.5, 1\.5]


Example harpconvert invocation for one tile:
`harpconvert --format hdf5 --hdf5-compression 9
-a 'O3_column_number_density_validity>50;derive(datetime_stop {time});
bin_spatial(2001, 50.000000, 0.01, 2001, -120.000000, 0.01);
keep(O3_column_number_density,O3_effective_temperature,cloud_fraction,
sensor_altitude,sensor_azimuth_angle, sensor_zenith_angle,
solar_azimuth_angle,solar_zenith_angle)'
S5P_OFFL_L2__O3_____20181005T225147_20181006T003317_05073_01_010102_20181012T001415.nc
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
| `O3_column_number_density` | mol/m^2 | 0\.025\* | 0\.3048\* | Total atmospheric column of O3 between the surface and the top of atmosphere, calculated with the [GODfit algorithm](http://adsabs.harvard.edu/full/2005ESASP.572E.204S). |
| `O3_effective_temperature` | K | 19\.92\* | 428\.11\* | Ozone cross section effective temperature |
| `cloud_fraction` | Fraction | 0\* | 1\* | Effective cloud fraction. See the [Sentinel 5P L2 Input/Output Data Definition Spec](https://sentinels.copernicus.eu/documents/247904/3119978/Sentinel-5P-Level-2-Input-Output-Data-Definition), p.220\. |
| `sensor_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the satellite at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `sensor_zenith_angle` | deg | 0\.098\* | 66\.57\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |
| `solar_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the Sun at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `solar_zenith_angle` | deg | 8\* | 102\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |


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
| STATUS\_MET\_2D | STRING | This dataset uses dynamic auxiliary weather data during L2 processing. This field has a value of "Nominal" if ECMWF dynamic auxiliary data was available or "Fallback" if not. |




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
varcollection=ee.ImageCollection('COPERNICUS/S5P/OFFL/L3_O3')
.select('O3_column_number_density')
.filterDate('2019-06-01','2019-06-05');

varband_viz={
min:0.12,
max:0.15,
palette:['black','blue','purple','cyan','green','yellow','red']
};

Map.addLayer(collection.mean(),band_viz,'S5P O3');
Map.setCenter(0.0,0.0,2);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_OFFL_L3_O3)


[Sentinel\-5P OFFL O3: Offline Ozone](/earth-engine/datasets/catalog/COPERNICUS_S5P_OFFL_L3_O3)

OFFL/L3\_O3 This dataset provides offline high\-resolution imagery of total column ozone concentrations. See also COPERNICUS/S5P/OFFL/L3\_O3\_TCL for the tropospheric column data. In the stratosphere, the ozone layer shields the biosphere from dangerous solar ultraviolet radiation. In the troposphere, it acts as an efficient cleansing agent, but at high concentration it also …

 COPERNICUS/S5P/OFFL/L3\_O3,
 air\-quality,atmosphere,copernicus,esa,eu,o3,ozone,pollution,s5p,sentinel,tropomi

2018\-09\-08T21:19:29Z/2025\-07\-12T17:28:04Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








