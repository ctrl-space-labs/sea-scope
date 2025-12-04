



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Sentinel\-5P NRTI O3: Near Real\-Time Ozone


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================








Dataset Availability
2018\-07\-10T11:02:44Z–2025\-07\-14T14:01:39Z
Dataset Provider


[European Union/ESA/Copernicus](https://sentinel.esa.int/web/sentinel/user-guides/sentinel-5p-tropomi)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/S5P/NRTI/L3_O3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_NRTI_L3_O3)





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



### NRTI/L3\_O3


This dataset provides near\-real\-time high\-resolution imagery of total
column ozone concentrations. See also `COPERNICUS/S5P/OFFL/L3_O3_TCL`
for the tropospheric column data.


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
[More information.](https://www.tropomi.eu/data-products/o/ozone-total-column)
[Product user manual.](https://sentinel.esa.int/documents/247904/2474726/Sentinel-5P-Level-2-Product-User-Manual-Ozone-Total-Column)


### NRTI L3 Product


To make our NRTI L3 products, we use [harpconvert](https://stcorp.github.io/harp/doc/html/harpconvert.html)
to grid the data.


The qa value is adjusted before running harpconvert to satisfy all of the
following criteria:


* ozone\_total\_vertical\_column in \[0, 0\.45]
* ozone\_effective\_temperature in \[180, 260]
* fitted\_root\_mean\_square \<\= 0\.01


Example harpconvert invocation:
`harpconvert --format hdf5 --hdf5-compression 9
-a 'O3_column_number_density_validity>50;derive(datetime_stop {time});
bin_spatial(2001, 50.000000, 0.01, 2001, -120.000000, 0.01);
keep(O3_column_number_density,O3_column_number_density_amf,
O3_slant_column_number_density,O3_effective_temperature,cloud_fraction,
sensor_azimuth_angle,sensor_zenith_angle,solar_azimuth_angle,
solar_zenith_angle)'
S5P_NRTI_L2__O3_____20180710T230038_20180710T230538_03840_01_010000_20180711T005227.nc
output.h5`


* Assets between the dates 2018\-07\-10 and 2018\-07\-18 are missing due to non\-standard structure
of product files.





### Bands



**Pixel Size**
  
1113\.2 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `O3_column_number_density` | mol/m^2 | 0\.0047\* | 0\.272\* | Total atmospheric column of O3 between the surface and the top of atmosphere, calculated with the [DOAS algorithm](http://projects.knmi.nl/omi/research/product/product_generator.php?info=algo&product=Ozone&flavour=OMDOAO3&long=DOAS%20Total%20Ozone%20column). |
| `O3_column_number_density_amf` | mol/m^2 | 1\.92\* | 6\.83\* | Weighted mean of cloudy and clear air mass factor (amf) weighted by intensity\-weighted cloud fraction. |
| `O3_slant_column_number_density` | mol/m^2 | 0\.014\* | 1\.402\* | O3 ring corrected slant column number density |
| `O3_effective_temperature` | K | \-5962\* | 936\* | Ozone cross section effective temperature |
| `cloud_fraction` | Fraction | 0\* | 1\* | Effective cloud fraction. See the [Sentinel 5P L2 Input/Output Data Definition Spec](https://sentinels.copernicus.eu/documents/247904/3119978/Sentinel-5P-Level-2-Input-Output-Data-Definition), p.220\. |
| `sensor_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the satellite at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `sensor_zenith_angle` | deg | 0\.098\* | 66\.44\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |
| `solar_azimuth_angle` | deg | \-180\* | 180\* | Azimuth angle of the Sun at the ground pixel location (WGS84\); angle measured East\-of\-North. |
| `solar_zenith_angle` | deg | 8\* | 80\* | Zenith angle of the satellite at the ground pixel location (WGS84\); angle measured away from the vertical. |


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
varcollection=ee.ImageCollection('COPERNICUS/S5P/NRTI/L3_O3')
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



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S5P_NRTI_L3_O3)


[Sentinel\-5P NRTI O3: Near Real\-Time Ozone](/earth-engine/datasets/catalog/COPERNICUS_S5P_NRTI_L3_O3)

NRTI/L3\_O3 This dataset provides near\-real\-time high\-resolution imagery of total column ozone concentrations. See also COPERNICUS/S5P/OFFL/L3\_O3\_TCL for the tropospheric column data. In the stratosphere, the ozone layer shields the biosphere from dangerous solar ultraviolet radiation. In the troposphere, it acts as an efficient cleansing agent, but at high concentration it also …

 COPERNICUS/S5P/NRTI/L3\_O3,
 air\-quality,atmosphere,copernicus,esa,eu,o3,ozone,pollution,s5p,sentinel,tropomi

2018\-07\-10T11:02:44Z/2025\-07\-14T14:01:39Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








