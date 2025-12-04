



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

ERA5 Monthly Aggregates \- Latest Climate Reanalysis Produced by ECMWF / Copernicus Climate Change Service


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================================================================================








Dataset Availability
1979\-01\-01T00:00:00Z–2020\-06\-01T00:00:00Z
Dataset Provider


[ECMWF / Copernicus Climate Change Service](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels-monthly-means?tab=overview)



Earth Engine Snippet


`ee.ImageCollection("ECMWF/ERA5/MONTHLY")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ECMWF/ECMWF_ERA5_MONTHLY)





Cadence
1 Month
Tags


[climate](/earth-engine/datasets/tags/climate)
[copernicus](/earth-engine/datasets/tags/copernicus)
[dewpoint](/earth-engine/datasets/tags/dewpoint)
[ecmwf](/earth-engine/datasets/tags/ecmwf)
[era5](/earth-engine/datasets/tags/era5)
[precipitation](/earth-engine/datasets/tags/precipitation)
[pressure](/earth-engine/datasets/tags/pressure)
[reanalysis](/earth-engine/datasets/tags/reanalysis)
[surface](/earth-engine/datasets/tags/surface)
[temperature](/earth-engine/datasets/tags/temperature)
[wind](/earth-engine/datasets/tags/wind)








#### Description



ERA5 is the fifth generation ECMWF atmospheric reanalysis of the global climate.
Reanalysis combines model data with observations from across the world into
a globally complete and consistent dataset. ERA5 replaces its predecessor,
the ERA\-Interim reanalysis.


ERA5 MONTHLY provides aggregated values for each month for seven ERA5
climate reanalysis parameters: 2m air temperature, 2m dewpoint temperature,
total precipitation,
mean sea level pressure, surface pressure, 10m u\-component of wind and
10m v\-component of wind. Additionally, monthly minimum and maximum air
temperature at 2m has been calculated based on the hourly 2m air temperature
data. Monthly total precipitation values are given as monthly sums.
All other parameters are provided as monthly averages.


ERA5 data is available from 1940 to three months from real\-time, the version in the EE Data Catalog is available from 1979\. More information
and more ERA5 atmospheric parameters can be found at the
[Copernicus Climate Data Store](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels-monthly-means?tab=overview).


Provider's Note: Monthly aggregates have been calculated based on the ERA5 hourly values
of each parameter.





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `mean_2m_air_temperature` | K | 224\* | 304\* | Average air temperature at 2m height (monthly average) |
| `minimum_2m_air_temperature` | K | 213\.1\* | 298\.9\* | Minimum air temperature at 2m height (monthly minimum) |
| `maximum_2m_air_temperature` | K | 233\.8\* | 314\.3\* | Maximum air temperature at 2m height (monthly maximum) |
| `dewpoint_2m_temperature` | K | 219\.8\* | 297\.6\* | Dewpoint temperature at 2m height (monthly average) |
| `total_precipitation` | m | 0\* | 0\.4\* | Total precipitation (monthly sums) |
| `surface_pressure` | Pa | 65256\.9\* | 102427\* | Surface pressure (monthly average) |
| `mean_sea_level_pressure` | Pa | 98206\.4\* | 102943\* | Mean sea level pressure (monthly average) |
| `u_component_of_wind_10m` | m/s | \-8\.7\* | 8\.7\* | 10m u\-component of wind (monthly average) |
| `v_component_of_wind_10m` | m/s | \-6\.8\* | 6\.8\* | 10m v\-component of wind (monthly average) |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| month | INT | Month of the data |
| year | INT | Year of the data |




### Terms of Use


**Terms of Use**


Please acknowledge the use of ERA5 as stated in the [Copernicus C3S/CAMS License agreement](https://apps.ecmwf.int/datasets/licences/copernicus/):


* 5\.1\.1 Where the Licensee communicates or distributes Copernicus Products to the public,
the Licensee shall inform the recipients of the source by using the following or any similar notice: "Generated using
Copernicus Climate Change Service information (Year)".
* 5\.1\.2 Where the Licensee makes or contributes to a publication or distribution containing adapted or
modified Copernicus Products, the Licensee shall provide the following or any similar notice: "Contains modified Copernicus
Climate Change Service information (Year)".
* 5\.1\.3 Any such publication or distribution covered by clauses 5\.1\.1 and 5\.1\.2 shall state that neither the European Commission
nor ECMWF is responsible for any use that may be made of the Copernicus information or Data it contains.




### Citations



Citations:
* Copernicus Climate Change Service (C3S) (2017\): ERA5: Fifth generation of ECMWF atmospheric reanalyses of the global climate.
Copernicus Climate Change Service Climate Data Store (CDS), (date of access), [https://cds.climate.copernicus.eu/cdsapp\#!/home](https://cds.climate.copernicus.eu/cdsapp#!/home)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('ECMWF/ERA5/MONTHLY');

varvisualization={
bands:['mean_2m_air_temperature'],
min:250.0,
max:320.0,
palette:[
'000080','0000d9','4000ff','8000ff','0080ff','00ffff',
'00ff80','80ff00','daff00','ffff00','fff500','ffda00',
'ffb000','ffa400','ff4f00','ff2500','ff0a00','ff00ff',
]
};

Map.setCenter(22.2,21.2,0);

Map.addLayer(dataset,visualization,'Monthly average air temperature [K] at 2m height');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ECMWF/ECMWF_ERA5_MONTHLY)


[ERA5 Monthly Aggregates \- Latest Climate Reanalysis Produced by ECMWF / Copernicus Climate Change Service](/earth-engine/datasets/catalog/ECMWF_ERA5_MONTHLY)

ERA5 is the fifth generation ECMWF atmospheric reanalysis of the global climate. Reanalysis combines model data with observations from across the world into a globally complete and consistent dataset. ERA5 replaces its predecessor, the ERA\-Interim reanalysis. ERA5 MONTHLY provides aggregated values for each month for seven ERA5 climate reanalysis parameters: …

 ECMWF/ERA5/MONTHLY,
 climate,copernicus,dewpoint,ecmwf,era5,precipitation,pressure,reanalysis,surface,temperature,wind

1979\-01\-01T00:00:00Z/2020\-06\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








