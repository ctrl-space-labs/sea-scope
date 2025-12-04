



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

HYCOM: Hybrid Coordinate Ocean Model, Water Temperature and Salinity


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================================








Dataset Availability
1992\-10\-02T00:00:00Z–2024\-09\-05T09:00:00Z
Dataset Provider


[NOPP](https://hycom.org/)



Earth Engine Snippet


`ee.ImageCollection("HYCOM/sea_temp_salinity")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/HYCOM/HYCOM_sea_temp_salinity)





Cadence
1 Day
Tags


[hycom](/earth-engine/datasets/tags/hycom)
[nopp](/earth-engine/datasets/tags/nopp)
[ocean](/earth-engine/datasets/tags/ocean)
[oceans](/earth-engine/datasets/tags/oceans)
[sst](/earth-engine/datasets/tags/sst)
[water](/earth-engine/datasets/tags/water)
salinity
water\-temp








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




| Name | Units | Min | Max | Scale | Offset | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `water_temp_0` | °C | \-32768\* | 32763\* | 0\.001 | 20 | Sea water temperature at a depth of 0m |
| `salinity_0` | psu | \-20009\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 0m |
| `water_temp_2` | °C | \-32768\* | 32755\* | 0\.001 | 20 | Sea water temperature at a depth of 2m |
| `salinity_2` | psu | \-20002\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 2m |
| `water_temp_4` | °C | \-32768\* | 32746\* | 0\.001 | 20 | Sea water temperature at a depth of 4m |
| `salinity_4` | psu | \-20001\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 4m |
| `water_temp_6` | °C | \-32768\* | 32742\* | 0\.001 | 20 | Sea water temperature at a depth of 6m |
| `salinity_6` | psu | \-19991\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 6m |
| `water_temp_8` | °C | \-32768\* | 32741\* | 0\.001 | 20 | Sea water temperature at a depth of 8m |
| `salinity_8` | psu | \-19795\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 8m |
| `water_temp_10` | °C | \-32768\* | 32738\* | 0\.001 | 20 | Sea water temperature at a depth of 10m |
| `salinity_10` | psu | \-19624\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 10m |
| `water_temp_12` | °C | \-32768\* | 32735\* | 0\.001 | 20 | Sea water temperature at a depth of 12m |
| `salinity_12` | psu | \-19624\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 12m |
| `water_temp_15` | °C | \-32768\* | 32763\* | 0\.001 | 20 | Sea water temperature at a depth of 15m |
| `salinity_15` | psu | \-19624\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 15m |
| `water_temp_20` | °C | \-32768\* | 32715\* | 0\.001 | 20 | Sea water temperature at a depth of 20m |
| `salinity_20` | psu | \-18606\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 20m |
| `water_temp_25` | °C | \-32768\* | 32737\* | 0\.001 | 20 | Sea water temperature at a depth of 25m |
| `salinity_25` | psu | \-18131\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 25m |
| `water_temp_30` | °C | \-32768\* | 32754\* | 0\.001 | 20 | Sea water temperature at a depth of 30m |
| `salinity_30` | psu | \-17892\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 30m |
| `water_temp_35` | °C | \-32768\* | 32754\* | 0\.001 | 20 | Sea water temperature at a depth of 35m |
| `salinity_35` | psu | \-17874\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 35m |
| `water_temp_40` | °C | \-32768\* | 32674\* | 0\.001 | 20 | Sea water temperature at a depth of 40m |
| `salinity_40` | psu | \-17831\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 40m |
| `water_temp_45` | °C | \-32768\* | 32701\* | 0\.001 | 20 | Sea water temperature at a depth of 45m |
| `salinity_45` | psu | \-17831\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 45m |
| `water_temp_50` | °C | \-32768\* | 32237\* | 0\.001 | 20 | Sea water temperature at a depth of 50m |
| `salinity_50` | psu | \-17738\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 50m |
| `water_temp_60` | °C | \-32768\* | 32630\* | 0\.001 | 20 | Sea water temperature at a depth of 60m |
| `salinity_60` | psu | \-17733\* | 32767\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 60m |
| `water_temp_70` | °C | \-32768\* | 23172\* | 0\.001 | 20 | Sea water temperature at a depth of 70m |
| `salinity_70` | psu | \-17423\* | 24303\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 70m |
| `water_temp_80` | °C | \-32768\* | 27875\* | 0\.001 | 20 | Sea water temperature at a depth of 80m |
| `salinity_80` | psu | \-17326\* | 25320\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 80m |
| `water_temp_90` | °C | \-32768\* | 32393\* | 0\.001 | 20 | Sea water temperature at a depth of 90m |
| `salinity_90` | psu | \-16787\* | 26604\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 90m |
| `water_temp_100` | °C | \-32768\* | 31847\* | 0\.001 | 20 | Sea water temperature at a depth of 100m |
| `salinity_100` | psu | \-16717\* | 27143\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 100m |
| `water_temp_125` | °C | \-32768\* | 31469\* | 0\.001 | 20 | Sea water temperature at a depth of 125m |
| `salinity_125` | psu | \-14896\* | 30131\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 125m |
| `water_temp_150` | °C | \-32768\* | 31335\* | 0\.001 | 20 | Sea water temperature at a depth of 150m |
| `salinity_150` | psu | \-14712\* | 31215\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 150m |
| `water_temp_200` | °C | \-32768\* | 30029\* | 0\.001 | 20 | Sea water temperature at a depth of 200m |
| `salinity_200` | psu | \-14567\* | 30979\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 200m |
| `water_temp_250` | °C | \-32768\* | 21629\* | 0\.001 | 20 | Sea water temperature at a depth of 250m |
| `salinity_250` | psu | \-13198\* | 27945\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 250m |
| `water_temp_300` | °C | \-32768\* | 22796\* | 0\.001 | 20 | Sea water temperature at a depth of 300m |
| `salinity_300` | psu | \-220\* | 27712\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 300m |
| `water_temp_350` | °C | \-32768\* | 18501\* | 0\.001 | 20 | Sea water temperature at a depth of 350m |
| `salinity_350` | psu | \-136\* | 21866\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 350m |
| `water_temp_400` | °C | \-32768\* | 23875\* | 0\.001 | 20 | Sea water temperature at a depth of 400m |
| `salinity_400` | psu | 0\* | 24711\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 400m |
| `water_temp_500` | °C | \-32768\* | 18663\* | 0\.001 | 20 | Sea water temperature at a depth of 500m |
| `salinity_500` | psu | 0\* | 24929\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 500m |
| `water_temp_600` | °C | \-32768\* | 14251\* | 0\.001 | 20 | Sea water temperature at a depth of 600m |
| `salinity_600` | psu | 0\* | 24128\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 600m |
| `water_temp_700` | °C | \-32768\* | 11300\* | 0\.001 | 20 | Sea water temperature at a depth of 700m |
| `salinity_700` | psu | 0\* | 22350\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 700m |
| `water_temp_800` | °C | \-32768\* | 8630\* | 0\.001 | 20 | Sea water temperature at a depth of 800m |
| `salinity_800` | psu | 0\* | 21959\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 800m |
| `water_temp_900` | °C | \-32768\* | 9544\* | 0\.001 | 20 | Sea water temperature at a depth of 900m |
| `salinity_900` | psu | 0\* | 21965\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 900m |
| `water_temp_1000` | °C | \-32768\* | 7050\* | 0\.001 | 20 | Sea water temperature at a depth of 1000m |
| `salinity_1000` | psu | 0\* | 21982\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 1000m |
| `water_temp_1250` | °C | \-32768\* | 8837\* | 0\.001 | 20 | Sea water temperature at a depth of 1250m |
| `salinity_1250` | psu | 0\* | 22075\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 1250m |
| `water_temp_1500` | °C | \-23069\* | 12933\* | 0\.001 | 20 | Sea water temperature at a depth of 1500m |
| `salinity_1500` | psu | 0\* | 20937\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 1500m |
| `water_temp_2000` | °C | \-25670\* | 4925\* | 0\.001 | 20 | Sea water temperature at a depth of 2000m |
| `salinity_2000` | psu | 0\* | 20936\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 2000m |
| `water_temp_2500` | °C | \-32768\* | 0\.001 | 20 | Sea water temperature at a depth of 2500m |
| `salinity_2500` | psu | 0\* | 19073\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 2500m |
| `water_temp_3000` | °C | \-22062\* | 0\.001 | 20 | Sea water temperature at a depth of 3000m |
| `salinity_3000` | psu | 0\* | 19057\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 3000m |
| `water_temp_4000` | °C | \-21564\* | 0\.001 | 20 | Sea water temperature at a depth of 4000m |
| `salinity_4000` | psu | 0\* | 19012\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 4000m |
| `water_temp_5000` | °C | \-21469\* | 0\.001 | 20 | Sea water temperature at a depth of 5000m |
| `salinity_5000` | psu | 0\* | 15583\* | 0\.001 | 20 | Sea water salinity, in practical salinity units, at a depth of 5000m |


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
// Import the time series of global images, filter 15 days in August, 2018.
vardataset=ee.ImageCollection('HYCOM/sea_temp_salinity')
.filter(ee.Filter.date('2018-08-01','2018-08-15'));

// Select water temperature at 0 meters and scale to degrees C.
varseaWaterTemperature=dataset.select('water_temp_0')
.map(functionscaleAndOffset(image){
returnee.Image(image).multiply(0.001).add(20);
});

// Define visualization parameters.
varvisParams={
min:-2.0,// Degrees C
max:34.0,
palette:['000000','005aff','43c8c8','fff700','ff0000'],
};

// Display mean 15-day temperature on the map.
Map.setCenter(-88.6,26.4,1);
Map.addLayer(seaWaterTemperature.mean(),visParams,'Sea Water Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/HYCOM/HYCOM_sea_temp_salinity)


[HYCOM: Hybrid Coordinate Ocean Model, Water Temperature and Salinity](/earth-engine/datasets/catalog/HYCOM_sea_temp_salinity)

The Hybrid Coordinate Ocean Model (HYCOM) is a data\-assimilative hybrid isopycnal\-sigma\-pressure (generalized) coordinate ocean model. The subset of HYCOM data hosted in EE contains the variables salinity, temperature, velocity, and elevation. They have been interpolated to a uniform 0\.08 degree lat/long grid between 80\.48°S and 80\.48°N. The salinity, temperature, and …

 HYCOM/sea\_temp\_salinity,
 hycom,nopp,ocean,oceans,sst,water

1992\-10\-02T00:00:00Z/2024\-09\-05T09:00:00Z



 \-80\.48 \-180 80\.48 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








