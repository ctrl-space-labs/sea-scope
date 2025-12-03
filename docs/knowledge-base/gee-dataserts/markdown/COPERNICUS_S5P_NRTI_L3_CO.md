



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Sentinel\-5P NRTI CO: Near Real\-Time Carbon Monoxide


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================================








Dataset Availability
2018\-11\-22T12:00:13Z–2025\-07\-14T14:01:39Z
Dataset Provider


[European Union/ESA/Copernicus](https://sentinel.esa.int/web/sentinel/user-guides/sentinel-5p-tropomi)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/S5P/NRTI/L3_CO")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_NRTI_L3_CO)





Revisit Interval
2 Days
Tags


[air\-quality](/earth-engine/datasets/tags/air-quality)
[atmosphere](/earth-engine/datasets/tags/atmosphere)
[carbon\-monoxide](/earth-engine/datasets/tags/carbon-monoxide)
[copernicus](/earth-engine/datasets/tags/copernicus)
[esa](/earth-engine/datasets/tags/esa)
[eu](/earth-engine/datasets/tags/eu)
[knmi](/earth-engine/datasets/tags/knmi)
[pollution](/earth-engine/datasets/tags/pollution)
[s5p](/earth-engine/datasets/tags/s5p)
[sentinel](/earth-engine/datasets/tags/sentinel)
[sron](/earth-engine/datasets/tags/sron)
[tropomi](/earth-engine/datasets/tags/tropomi)








#### Description



### NRTI/L3\_CO


This dataset provides near real\-time high\-resolution imagery of CO
concentrations.


Carbon monoxide (CO) is an important atmospheric trace gas for understanding
tropospheric chemistry. In certain urban areas, it is a major atmospheric
pollutant. Main sources of CO are combustion of fossil fuels, biomass burning,
and atmospheric oxidation of methane and other hydrocarbons. Whereas fossil
fuel combustion is the main source of CO at northern mid\-latitudes, the oxidation
of isoprene and biomass burning play an important role in the tropics. TROPOMI
on the Sentinel 5 Precursor (S5P) satellite observes the CO global abundance
exploiting clear\-sky and cloudy\-sky Earth radiance measurements in the 2\.3 μm
spectral range of the shortwave infrared (SWIR) part of the solar spectrum.
TROPOMI clear sky observations provide CO total columns with sensitivity to the
tropospheric boundary layer. For cloudy atmospheres, the column sensitivity
changes according to the light path.
[More information.](http://www.tropomi.eu/data-products/carbon-monoxide)


### NRTI L3 Product


To make our NRTI L3 products, we use [harpconvert](https://stcorp.github.io/harp/doc/html/harpconvert.html)
to grid the data.


Example harpconvert invocation for one tile:
`harpconvert --format hdf5 --hdf5-compression 9
-a 'CO_column_number_density_validity>50;derive(datetime_stop {time});
bin_spatial(2001, 50.000000, 0.01, 2001, -120.000000, 0.01);
keep(CO_column_number_density,H2O_column_number_density,cloud_height,
sensor_altitude,sensor_azimuth_angle, sensor_zenith_angle,
solar_azimuth_angle,solar_zenith_angle)'
S5P_NRTI_L2__CO_____20181122T000018_20181122T000518_05741_01_010200_20181122T004844.nc
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
| `CO_column_number_density` | mol/m^2 | \-279\* | 4\.64\* | Vertically integrated CO column density. |
| `H2O_column_number_density` | mol/m^2 | \-465360\* | 3\.45844e\+07\* | Water vapor column. |
| `cloud_height` | m | \-8341\* | 5000\* | Scattering layer height. |
| `sensor_altitude` | m | 828542\* | 856078\* | Altitude of the satellite with respect to the geodetic sub\-satellite point (WGS84\). |
| `sensor_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the satellite at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `sensor_zenith_angle` | deg | 1\* | 66\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |
| `solar_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the Sun at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `solar_zenith_angle` | deg | 9\* | 80\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |


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
varcollection=ee.ImageCollection('COPERNICUS/S5P/NRTI/L3_CO')
.select('CO_column_number_density')
.filterDate('2019-06-01','2019-06-11');

varband_viz={
min:0,
max:0.05,
palette:['black','blue','purple','cyan','green','yellow','red']
};

Map.addLayer(collection.mean(),band_viz,'S5P CO');
Map.setCenter(-25.01,-4.28,4);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_NRTI_L3_CO)


[Sentinel\-5P NRTI CO: Near Real\-Time Carbon Monoxide](/earth-engine/datasets/catalog/COPERNICUS_S5P_NRTI_L3_CO)

NRTI/L3\_CO This dataset provides near real\-time high\-resolution imagery of CO concentrations. Carbon monoxide (CO) is an important atmospheric trace gas for understanding tropospheric chemistry. In certain urban areas, it is a major atmospheric pollutant. Main sources of CO are combustion of fossil fuels, biomass burning, and atmospheric oxidation of methane …

 COPERNICUS/S5P/NRTI/L3\_CO,
 air\-quality,atmosphere,carbon\-monoxide,copernicus,esa,eu,knmi,pollution,s5p,sentinel,sron,tropomi

2018\-11\-22T12:00:13Z/2025\-07\-14T14:01:39Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








