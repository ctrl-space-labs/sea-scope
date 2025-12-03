



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

HYCOM: Hybrid Coordinate Ocean Model, Water Velocity


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================








Dataset Availability
1992\-10\-02T00:00:00Z–2024\-09\-05T09:00:00Z
Dataset Provider


[NOPP](https://hycom.org/)



Earth Engine Snippet


`ee.ImageCollection("HYCOM/sea_water_velocity")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/HYCOM/HYCOM_sea_water_velocity)





Cadence
1 Day
Tags


[hycom](/earth-engine/datasets/tags/hycom)
[nopp](/earth-engine/datasets/tags/nopp)
[ocean](/earth-engine/datasets/tags/ocean)
[oceans](/earth-engine/datasets/tags/oceans)
[velocity](/earth-engine/datasets/tags/velocity)
[water](/earth-engine/datasets/tags/water)








#### Description



The Hybrid Coordinate Ocean Model (HYCOM) is a data\-assimilative hybrid
isopycnal\-sigma\-pressure (generalized) coordinate ocean model. The subset
of HYCOM data hosted in EE contains the variables salinity, temperature,
velocity, and elevation. They have been interpolated to a uniform
0\.08 degree lat/long grid between 80\.48°S and 80\.48°N. The salinity,
temperature, and velocity variables have been interpolated to 40
standard z\-levels.


The HYCOM Consortium, which includes the National Ocean Partnership
Program (NOPP), is part of the U.S. Global Ocean Data Assimilation
Experiment (GODAE).


Funded by the National Ocean Partnership Program, the Office of Naval
Research (ONR), and DoD High Performance Computing Modernization Program.


For more information, see:


* [hycom.org](https://www.hycom.org/)
* [GIS StackExchange hycom](https://gis.stackexchange.com/questions/tagged/hycom)
* Wikipedia [HyCOM](https://en.wikipedia.org/wiki/HyCOM)
* Wikipedia [List of ocean circulation models](https://en.wikipedia.org/wiki/List_of_ocean_circulation_models)
* Wikipedia [Ocean general circulation model (OGCM)](https://en.wikipedia.org/wiki/Ocean_general_circulation_model)





### Bands



**Pixel Size**
  
8905\.6 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `velocity_u_0` | m/s | \-31557\* | 16899\* | 0\.001 | Eastward sea water velocity at a depth of 0m |
| `velocity_v_0` | m/s | \-20004\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 0m |
| `velocity_u_2` | m/s | \-31588\* | 16806\* | 0\.001 | Eastward sea water velocity at a depth of 2m |
| `velocity_v_2` | m/s | \-20000\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 2m |
| `velocity_u_4` | m/s | \-31589\* | 16831\* | 0\.001 | Eastward sea water velocity at a depth of 4m |
| `velocity_v_4` | m/s | \-20000\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 4m |
| `velocity_u_6` | m/s | \-31589\* | 16794\* | 0\.001 | Eastward sea water velocity at a depth of 6m |
| `velocity_v_6` | m/s | \-19991\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 6m |
| `velocity_u_8` | m/s | \-31575\* | 16828\* | 0\.001 | Eastward sea water velocity at a depth of 8m |
| `velocity_v_8` | m/s | \-19792\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 8m |
| `velocity_u_10` | m/s | \-31563\* | 16828\* | 0\.001 | Eastward sea water velocity at a depth of 10m |
| `velocity_v_10` | m/s | \-19582\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 10m |
| `velocity_u_12` | m/s | \-31547\* | 16828\* | 0\.001 | Eastward sea water velocity at a depth of 12m |
| `velocity_v_12` | m/s | \-19582\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 12m |
| `velocity_u_15` | m/s | \-31517\* | 16828\* | 0\.001 | Eastward sea water velocity at a depth of 15m |
| `velocity_v_15` | m/s | \-19582\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 15m |
| `velocity_u_20` | m/s | \-32768\* | 16743\* | 0\.001 | Eastward sea water velocity at a depth of 20m |
| `velocity_v_20` | m/s | \-18593\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 20m |
| `velocity_u_25` | m/s | \-32768\* | 16370\* | 0\.001 | Eastward sea water velocity at a depth of 25m |
| `velocity_v_25` | m/s | \-18131\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 25m |
| `velocity_u_30` | m/s | \-32768\* | 15996\* | 0\.001 | Eastward sea water velocity at a depth of 30m |
| `velocity_v_30` | m/s | \-17489\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 30m |
| `velocity_u_35` | m/s | \-32768\* | 15639\* | 0\.001 | Eastward sea water velocity at a depth of 35m |
| `velocity_v_35` | m/s | \-17409\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 35m |
| `velocity_u_40` | m/s | \-32768\* | 15120\* | 0\.001 | Eastward sea water velocity at a depth of 40m |
| `velocity_v_40` | m/s | \-17386\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 40m |
| `velocity_u_45` | m/s | \-32768\* | 15066\* | 0\.001 | Eastward sea water velocity at a depth of 45m |
| `velocity_v_45` | m/s | \-17302\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 45m |
| `velocity_u_50` | m/s | \-32768\* | 14808\* | 0\.001 | Eastward sea water velocity at a depth of 50m |
| `velocity_v_50` | m/s | \-17302\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 50m |
| `velocity_u_60` | m/s | \-32768\* | 15986\* | 0\.001 | Eastward sea water velocity at a depth of 60m |
| `velocity_v_60` | m/s | \-17070\* | 32767\* | 0\.001 | Northward sea water velocity at a depth of 60m |
| `velocity_u_70` | m/s | \-32768\* | 14406\* | 0\.001 | Eastward sea water velocity at a depth of 70m |
| `velocity_v_70` | m/s | \-16976\* | 22779\* | 0\.001 | Northward sea water velocity at a depth of 70m |
| `velocity_u_80` | m/s | \-32768\* | 27875\* | 0\.001 | Eastward sea water velocity at a depth of 80m |
| `velocity_v_80` | m/s | \-16936\* | 23957\* | 0\.001 | Northward sea water velocity at a depth of 80m |
| `velocity_u_90` | m/s | \-32768\* | 27666\* | 0\.001 | Eastward sea water velocity at a depth of 90m |
| `velocity_v_90` | m/s | \-16757\* | 23947\* | 0\.001 | Northward sea water velocity at a depth of 90m |
| `velocity_u_100` | m/s | \-32768\* | 24932\* | 0\.001 | Eastward sea water velocity at a depth of 100m |
| `velocity_v_100` | m/s | \-16717\* | 23631\* | 0\.001 | Northward sea water velocity at a depth of 100m |
| `velocity_u_125` | m/s | \-32768\* | 24627\* | 0\.001 | Eastward sea water velocity at a depth of 125m |
| `velocity_v_125` | m/s | \-14743\* | 23518\* | 0\.001 | Northward sea water velocity at a depth of 125m |
| `velocity_u_150` | m/s | \-32768\* | 24288\* | 0\.001 | Eastward sea water velocity at a depth of 150m |
| `velocity_v_150` | m/s | \-14700\* | 23444\* | 0\.001 | Northward sea water velocity at a depth of 150m |
| `velocity_u_200` | m/s | \-32768\* | 21844\* | 0\.001 | Eastward sea water velocity at a depth of 200m |
| `velocity_v_200` | m/s | \-13198\* | 23434\* | 0\.001 | Northward sea water velocity at a depth of 200m |
| `velocity_u_250` | m/s | \-32768\* | 21389\* | 0\.001 | Eastward sea water velocity at a depth of 250m |
| `velocity_v_250` | m/s | \-13176\* | 23418\* | 0\.001 | Northward sea water velocity at a depth of 250m |
| `velocity_u_300` | m/s | \-32768\* | 14403\* | 0\.001 | Eastward sea water velocity at a depth of 300m |
| `velocity_v_300` | m/s | \-3218\* | 21128\* | 0\.001 | Northward sea water velocity at a depth of 300m |
| `velocity_u_350` | m/s | \-32768\* | 11257\* | 0\.001 | Eastward sea water velocity at a depth of 350m |
| `velocity_v_350` | m/s | \-3183\* | 20974\* | 0\.001 | Northward sea water velocity at a depth of 350m |
| `velocity_u_400` | m/s | \-32768\* | 14624\* | 0\.001 | Eastward sea water velocity at a depth of 400m |
| `velocity_v_400` | m/s | \-3089\* | 21402\* | 0\.001 | Northward sea water velocity at a depth of 400m |
| `velocity_u_500` | m/s | \-32768\* | 11012\* | 0\.001 | Eastward sea water velocity at a depth of 500m |
| `velocity_v_500` | m/s | \-2848\* | 20965\* | 0\.001 | Northward sea water velocity at a depth of 500m |
| `velocity_u_600` | m/s | \-32768\* | 10572\* | 0\.001 | Eastward sea water velocity at a depth of 600m |
| `velocity_v_600` | m/s | \-2568\* | 20968\* | 0\.001 | Northward sea water velocity at a depth of 600m |
| `velocity_u_700` | m/s | \-32768\* | 10330\* | 0\.001 | Eastward sea water velocity at a depth of 700m |
| `velocity_v_700` | m/s | \-2321\* | 21448\* | 0\.001 | Northward sea water velocity at a depth of 700m |
| `velocity_u_800` | m/s | \-32768\* | 8503\* | 0\.001 | Eastward sea water velocity at a depth of 800m |
| `velocity_v_800` | m/s | \-2333\* | 20965\* | 0\.001 | Northward sea water velocity at a depth of 800m |
| `velocity_u_900` | m/s | \-32768\* | 6941\* | 0\.001 | Eastward sea water velocity at a depth of 900m |
| `velocity_v_900` | m/s | \-2577\* | 20958\* | 0\.001 | Northward sea water velocity at a depth of 900m |
| `velocity_u_1000` | m/s | \-32768\* | 6951\* | 0\.001 | Eastward sea water velocity at a depth of 1000m |
| `velocity_v_1000` | m/s | \-2299\* | 20956\* | 0\.001 | Northward sea water velocity at a depth of 1000m |
| `velocity_u_1250` | m/s | \-32768\* | 8351\* | 0\.001 | Eastward sea water velocity at a depth of 1250m |
| `velocity_v_1250` | m/s | \-2244\* | 20950\* | 0\.001 | Northward sea water velocity at a depth of 1250m |
| `velocity_u_1500` | m/s | \-22775\* | 3659\* | 0\.001 | Eastward sea water velocity at a depth of 1500m |
| `velocity_v_1500` | m/s | \-2154\* | 20937\* | 0\.001 | Northward sea water velocity at a depth of 1500m |
| `velocity_u_2000` | m/s | \-22448\* | 2811\* | 0\.001 | Eastward sea water velocity at a depth of 2000m |
| `velocity_v_2000` | m/s | \-2010\* | 20936\* | 0\.001 | Northward sea water velocity at a depth of 2000m |
| `velocity_u_2500` | m/s | \-32768\* | 1865\* | 0\.001 | Eastward sea water velocity at a depth of 2500m |
| `velocity_v_2500` | m/s | \-1863\* | 18919\* | 0\.001 | Northward sea water velocity at a depth of 2500m |
| `velocity_u_3000` | m/s | \-21841\* | 1677\* | 0\.001 | Eastward sea water velocity at a depth of 3000m |
| `velocity_v_3000` | m/s | \-1819\* | 18923\* | 0\.001 | Northward sea water velocity at a depth of 3000m |
| `velocity_u_4000` | m/s | \-21345\* | 1980\* | 0\.001 | Eastward sea water velocity at a depth of 4000m |
| `velocity_v_4000` | m/s | \-1383\* | 18856\* | 0\.001 | Northward sea water velocity at a depth of 4000m |
| `velocity_u_5000` | m/s | \-21469\* | 2013\* | 0\.001 | Eastward sea water velocity at a depth of 5000m |
| `velocity_v_5000` | m/s | \-971\* | 15383\* | 0\.001 | Northward sea water velocity at a depth of 5000m |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| experiment | STRING | Experiment number |




### Terms of Use


**Terms of Use**


This dataset is freely available with no restrictions.




### Citations



Citations:
* J. A. Cummings and O. M. Smedstad. 2013: Variational Data Assimilation for
the Global Ocean. Data Assimilation for Atmospheric, Oceanic and Hydrologic
Applications vol II, chapter 13, 303\-343\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varvelocity=ee.Image('HYCOM/sea_water_velocity/2014040700').divide(1000);

// Compute speed from velocity.
Map.addLayer(
velocity.select('velocity_u_0').hypot(velocity.select('velocity_v_0')));

Map.setCenter(-60,33,5);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/HYCOM/HYCOM_sea_water_velocity)


[HYCOM: Hybrid Coordinate Ocean Model, Water Velocity](/earth-engine/datasets/catalog/HYCOM_sea_water_velocity)

The Hybrid Coordinate Ocean Model (HYCOM) is a data\-assimilative hybrid isopycnal\-sigma\-pressure (generalized) coordinate ocean model. The subset of HYCOM data hosted in EE contains the variables salinity, temperature, velocity, and elevation. They have been interpolated to a uniform 0\.08 degree lat/long grid between 80\.48°S and 80\.48°N. The salinity, temperature, and …

 HYCOM/sea\_water\_velocity,
 hycom,nopp,ocean,oceans,velocity,water

1992\-10\-02T00:00:00Z/2024\-09\-05T09:00:00Z



 \-80\.48 \-180 80\.48 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








