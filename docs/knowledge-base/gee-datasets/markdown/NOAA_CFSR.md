



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

CFSR: Climate Forecast System Reanalysis


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================








Dataset Availability
2018\-12\-13T00:00:00Z–2025\-07\-16T12:00:00Z
Dataset Provider


[NOAA NWS National Centers for Environmental Prediction (NCEP)](https://cfs.ncep.noaa.gov/cfsr/)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CFSR")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CFSR)





Cadence
6 Hours
Tags


[climate](/earth-engine/datasets/tags/climate)
[daylight](/earth-engine/datasets/tags/daylight)
[flux](/earth-engine/datasets/tags/flux)
[forecast](/earth-engine/datasets/tags/forecast)
[geophysical](/earth-engine/datasets/tags/geophysical)
[ncep](/earth-engine/datasets/tags/ncep)
[noaa](/earth-engine/datasets/tags/noaa)
[nws](/earth-engine/datasets/tags/nws)
[precipitation](/earth-engine/datasets/tags/precipitation)
[radiation](/earth-engine/datasets/tags/radiation)
[snow](/earth-engine/datasets/tags/snow)
[temperature](/earth-engine/datasets/tags/temperature)
[vapor](/earth-engine/datasets/tags/vapor)
[water](/earth-engine/datasets/tags/water)
[weather](/earth-engine/datasets/tags/weather)








#### Description



The National Centers for Environmental Prediction (NCEP) Climate Forecast
System Reanalysis (CFSR) was designed and executed as a global,
high\-resolution, coupled atmosphere\-ocean\-land surface\-sea ice system to
provide the best estimate of the state of these coupled domains over the
32\-year period of record from January 1979 to March 2011\. It has been
extended as an operational real\-time product. The data in Earth Engine are
only present starting from December 13, 2018\.


Forecasts are initialized four times per day (0000, 0600, 1200, and 1800
UTC). We ingest only a subset of bands from files matching
`cdas1.t??z.pgrbh**03|00**.grib2`, i.e. files of only 0\-hour and 3\-hour
forecasts as the others are omitted. The forecast length is indicated by the
'forecast\_hour' metadata field.


Some images contain only a subset of bands. Using this dataset with both
"00" and "03" forecast types will require you to cast the bands across
the collection.





### Bands



**Pixel Size**
  
55660 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `u-component_of_wind_hybrid` | m/s | \-47\.24\* | 44\.33\* | u\-component of wind at Hybrid level for 00 and 03 forecast |
| `v-component_of_wind_hybrid` | m/s | \-45\.45\* | 46\.36\* | v\-component of wind at Hybrid level for 00 and 03 forecast |
| `Albedo_surface_3_Hour_Average` | % | 0\* | 91\.6\* | Albedo 3 hour average at ground or water surface for 03 forecast |
| `Canopy_water_evaporation_surface_3_Hour_Average` | W/m^2 | 0\* | 746\* | Canopy water evaporation 3 hour average at ground or water surface for 03 forecast |
| `Categorical_Rain_surface` | None | 0\* | 1\* | Categorical Rain at ground or water surface for 00 and 03 forecast |
| `Categorical_Rain_surface_3_Hour_Average` | None | 0\* | 1\* | Categorical Rain 3 hour average at ground or water surface for 03 forecast |
| `Categorical_Freezing_Rain_surface_3_Hour_Average` | None | 0\* | 1\* | Categorical freezing rain 3 hour average at ground or water surface for 03 forecast |
| `Categorical_Ice_Pellets_surface_3_Hour_Average` | None | 0\* | 1\* | Categorical ice pellets 3 hour average at ground or water surface for 03 forecast |
| `Categorical_Snow_surface_3_Hour_Average` | None | 0\* | 1\* | Categorical snow 3 hour average at ground or water surface for 03 forecast |
| `Clear_Sky_Downward_Long_Wave_Flux_surface_3_Hour_Average` | W/m^2 | 56\* | 483\* | Clear Sky Downward Long Wave Flux 3 hour average at ground or water surface for 03 forecast |
| `Clear_Sky_Downward_Solar_Flux_surface_3_Hour_Average` | W/m^2 | 0\* | 1142\* | Clear Sky Downward Solar Flux 3 hour average at ground or water surface for 03 forecast |
| `Clear_Sky_Upward_Long_Wave_Flux_surface_3_Hour_Average` | W/m^2 | 78\* | 698\* | Clear Sky Upward Long Wave Flux 3 hour average at ground or water surface for 03 forecast |
| `Clear_Sky_Upward_Solar_Flux_atmosphere_top_3_Hour_Average` | W/m^2 | 0\* | 767\* | Clear Sky Upward Solar Flux 3 hour average at ground or water surface for 03 forecast |
| `Clear_sky_UV-B_Downward_Solar_Flux_surface_3_Hour_Average` | W/m^2 | 0\* | 24\.77\* | Clear Sky UV\-B Downward Solar Flux 3 hour average at ground or water surface for 03 forecast |
| `Cloud_water_entire_atmosphere_single_layer` | kg/m^2 | 0\* | 19\* | Cloud water at entire atmosphere layer for 00 and 03 forecast |
| `Cloud_Work_Function_entire_atmosphere_single_layer_3_Hour_Average` | J/kg | 0\* | 5791\* | Cloud work function 3 hour average at entire atmosphere layer for 03 forecast |
| `Convective_available_potential_energy_surface` | J/kg | 0\* | 6069\* | Convective available potential energy at ground or water surface for 00 and 03 forecast |
| `Convective_available_potential_energy_pressure_difference_layer` | J/kg | 0\* | 5559\* | Convective available potential energy at specified pressure difference from ground to level layer for 03 forecast |
| `Convective_Precipitation_Rate_surface_3_Hour_Average` | kg/m^2/s | 0\* | 0\.002\* | Convective precipitation rate 3 hour average at ground or water surface for 03 forecast |
| `Convective_precipitation_surface_3_Hour_Accumulation` | kg/m^2 | 0\* | 19\.2\* | Convective precipitation 3 hour average at ground or water surface for 03 forecast |
| `Direct_Evaporation_from_Bare_Soil_surface_3_Hour_Average` | W/m^2 | 0\* | 767\* | Direct evaporation from bare soil surface 3 hour average at ground or water surface for 03 forecast |
| `Downward_Long-Wave_Radp_Flux_surface` | W/m^2 | 60\* | 530\* | Downward Long\-Wave Rad. Flux at ground or water surface for 00 and 03 forecast |
| `Downward_Long-Wave_Radp_Flux_surface_3_Hour_Average` | W/m^2 | 60\* | 508\* | Downward Long\-Wave Rad. Flux 3 hour average at ground or water surface for 03 forecast |
| `Downward_Short-Wave_Radiation_Flux_surface` | W/m^2 | 0\* | 1224\* | Downward Short\-Wave Radiation Flux at ground or water surface for 00 and 03 forecast |
| `Downward_Short-Wave_Radiation_Flux_surface_3_Hour_Average` | W/m^2 | 0\* | 1142\* | Downward Short\-Wave Radiation Flux 3 hour average at ground or water surface for 03 forecast |
| `Downward_Short-Wave_Radiation_Flux_atmosphere_top_3_Hour_Average` | W/m^2 | 0\* | 1382\* | Downward Short\-Wave Radiation Flux atmosphere top 3 hour average at ground or water surface for 03 forecast |
| `Exchange_Coefficient_surface` | (kg/m^3\)/(m/s) | 0\* | 0\.69\* | Exchange Coefficient at ground or water surface for 00 and 03 forecast |
| `Frictional_Velocity_surface` | m/s | 0\.002\* | 3\.5\* | Frictional Velocity at ground or water surface for 00 and 03 forecast |
| `Ground_Heat_Flux_surface` | W/m^2 | \-459\* | 683\* | Ground Heat Flux at ground or water surface for 00 and 03 forecast |
| `Ground_Heat_Flux_surface_3_Hour_Average` | W/m^2 | \-170\* | 538\* | Ground Heat Flux 4 hour average at ground or water surface for 03 forecast |
| `Ice_cover_surface` | Area fraction | 0\* | 1\* | Ice cover at ground or water surface for 00 and 03 forecast |
| `Ice_thickness_surface` | m | 0\* | 4\.76\* | Ice thickness at ground or water surface for 00 and 03 forecast |
| `Land_cover_0__sea_1__land_surface` | None | 0\* | 1\* | Land cover (0 \= sea, 1 \= land) at ground or water surface for 00 and 03 forecast |
| `Latent_heat_net_flux_surface` | W/m^2 | \-399\* | 1675\* | Latent heat net flux at ground or water surface for 00 and 03 forecast |
| `Latent_heat_net_flux_surface_3_Hour_Average` | W/m^2 | \-305\* | 1250\* | Latent heat net flux 3 hour average at ground or water surface for 03 forecast |
| `Liquid_Volumetric_Soil_Moisture_non_Frozen_depth_below_surface_layer_5_cm` | None | 0\.03\* | 1\* | Liquid Volumetric Soil Moisture (non Frozen) 5 cm depth below land surface layer |
| `Liquid_Volumetric_Soil_Moisture_non_Frozen_depth_below_surface_layer_25_cm` | None | 0\.028\* | 1\* | Liquid Volumetric Soil Moisture (non Frozen) 25 cm depth below land surface layer |
| `Liquid_Volumetric_Soil_Moisture_non_Frozen_depth_below_surface_layer_70_cm` | None | 0\.028\* | 1\* | Liquid Volumetric Soil Moisture (non Frozen) 50 cm depth below land surface layer |
| `Liquid_Volumetric_Soil_Moisture_non_Frozen_depth_below_surface_layer_150_cm` | None | 0\.028\* | 1\* | Liquid Volumetric Soil Moisture (non Frozen) 150 cm depth below land surface layer |
| `Maximum_temperature_height_above_ground_3_Hour_Interval` | K | 201\.39\* | 327\.7\* | Maximum temperature for 3 Hour Interval at specified height level above ground for 03 forecast |
| `Minimum_temperature_height_above_ground_3_Hour_Interval` | K | 201\* | 321\.89\* | Minimum temperature for 3 Hour Interval at specified height level above ground for 03 forecast |
| `Maximum_specific_humidity_at_2m_height_above_ground_3_Hour_Interval` | Mass fraction | 0\* | 0\.036\* | Maximum specific humidity for 3 Hour Interval at 2m specified height level above ground for 03 forecast |
| `Minimum_specific_humidity_at_2m_height_above_ground_3_Hour_Interval` | Mass fraction | 0\* | 0\.024\* | Minimum specific humidity for 3 Hour Interval at 2m specified height level above ground for 03 forecast |
| `Momentum_flux_u-component_surface_3_Hour_Average` | N/m^2 | \-6\.56\* | 8\.25\* | Momentum flux, u\-component 3 hour average at ground or water surface for 03 forecast |
| `Momentum_flux_v-component_surface_3_Hour_Average` | N/m^2 | \-6\.17\* | 7\.22\* | Momentum flux, u\-component 3 hour average at ground or water surface for 03 forecast |
| `Plant_Canopy_Surface_Water_surface` | kg/m^2 | 0\* | 0\.5\* | Plant Canopy Surface Water at ground or water surface for 00 and 03 forecast |
| `Planetary_Boundary_Layer_Height_surface` | m | 17\* | 6590\* | Planetary Boundary Layer Height at ground or water surface for 00 and 03 forecast |
| `Potential_Evaporation_Rate_surface` | W/m^2 | \-150\* | 5617\* | Potential Evaporation Rate at ground or water surface for 00 and 03 forecast |
| `Potential_Evaporation_Rate_surface_3_Hour_Average` | W/m^2 | \-120\* | 5263\* | Potential Evaporation Rate 3 hour average at ground or water surface for 03 forecast |
| `Precipitation_rate_surface_3_Hour_Average` | kg/m^2/s | 0\* | 0\.022\* | Precipitable rate 3 hour average at ground or water surface for 03 forecast |
| `Precipitable_water_entire_atmosphere_single_layer` | kg/m^2 | \-0\.6\* | 99\.09\* | Precipitable water at entire atmosphere layer for 00 and 03 forecast |
| `Precipitable_water_pressure_difference_layer` | kg/m^2 | 0\* | 7\.94\* | Precipitable water at specified pressure difference from ground to level layer for 00 forecast |
| `Pressure_msl` | Pa | 92406\.4\* | 106908\* | Pressure at Mean sea level for 03 forecast |
| `Pressure_reduced_to_MSL_msl` | Pa | 92492\.8\* | 106668\* | Pressure reduced to MSL at Mean sea level for 00 and 03 forecast |
| `Pressure_surface` | Pa | 48110\* | 105600\* | Pressure at ground or water surface for 00 and 03 forecast |
| `Relative_humidity_entire_atmosphere_single_layer` | % | 0\* | 96\* | Relative humidity at entire atmosphere layer for 00 and 03 forecast |
| `Sensible_heat_net_flux_surface` | W/m^2 | \-1582\* | 2500\* | Sensible heat net flux at ground or water surface for 00 and 03 forecast |
| `Sensible_heat_net_flux_surface_3_Hour_Average` | W/m^2 | \-977\* | 1202\* | Sensible heat net flux 3 hour average at ground or water surface for 03 forecast |
| `Snow_Cover_surface_3_Hour_Average` | % | 0\* | 100\* | Snow cover 3 hour average at ground or water surface for 03 forecast |
| `Snow_depth_surface` | m | 0\* | 4\.55\* | Snow depth at ground or water surface for 00 and 03 forecast |
| `Snow_Phase_Change_Heat_Flux_surface_3_Hour_Average` | W/m^2 | \-405\* | 911\* | Snow phase change hear flux 3 hour average at ground or water surface for 03 forecast |
| `Soil_moisture_content_depth_below_surface_layer` | kg/m^2 | 62\.01\* | 2000\.05\* | Soil moisture content at Depth below land surface layer for 00 and 03 forecast |
| `Soil_type_surface` | None | 1\* | 9\* | Soil type at ground or water surface for 00 and 03 forecast |
| `Storm_Surface_Runoff_surface_3_Hour_Accumulation` | kg/m^2 | 0\* | 193\.12\* | Storm surface runoff 3 hour accumulation at ground or water surface for 03 forecast |
| `Sublimation_evaporation_from_snow_surface_3_Hour_Average` | W/m^2 | 0\* | 742\* | Sublimation (evaporation from snow) 3 hour average at ground or water surface for 03 forecast |
| `Specific_humidity_height_above_ground` | Mass fraction | 0\.001\* | 0\.036\* | Specific humidity at Specified height level above ground for 00 forecast |
| `Surface_Lifted_Index_surface` | K | \-15\.8\* | 57\.2\* | Surface Lifted Index at ground or water surface for 00 and 03 forecast |
| `Surface_roughness_surface` | m | 0\* | 2\.7\* | Surface roughness at ground or water surface for 00 and 03 forecast |
| `Surface_Slope_Type_surface` | index | 1\* | 9\* | Surface Slope Type at ground or water surface for 00 and 03 forecast |
| `Temperature_depth_below_surface_layer_5_cm` | K | 219\.127\* | 323\.104\* | Temperature 5cm depth below land surface layer for 00 and 03 forecast |
| `Temperature_depth_below_surface_layer_25_cm` | K | 220\.288\* | 313\.299\* | Temperature 25cm epth below land surface layer for 00 and 03 forecast |
| `Temperature_depth_below_surface_layer_70_cm` | K | 218\.704\* | 310\.007\* | Temperature 70 cm depth below land surface layer for 00 and 03 forecast |
| `Temperature_depth_below_surface_layer_150_cm` | K | 218\.925\* | 307\.662\* | Temperature 150cm depth below land surface layer for 00 and 03 forecast |
| `Temperature_height_above_ground` | K | 201\.17\* | 325\.763\* | Temperature at Specified height level above ground for 00 forecast |
| `Temperature_surface` | K | 192\.569\* | 339\.173\* | Temperature at ground or water surface for 00 and 03 forecast |
| `Total_cloud_cover_convective_cloud` | % | 0\* | 100\* | Total cloud cover at Convective cloud layer for 00 forecast |
| `Total_ozone_entire_atmosphere_single_layer` | Dobson | 177\* | 571\.4\* | Total ozone at entire atmosphere layer for 00 and 03 forecast |
| `Total_precipitation_surface_3_Hour_Accumulation` | kg/m^2 | 0\* | 239\* | Total precipitation 3 hour average at ground or water surface for 03 forecast |
| `Transpiration_surface_3_Hour_Average` | W/m^2 | 0\* | 680\* | Transpiration surface 3 hour average at ground or water surface for 03 forecast |
| `Upward_Long-Wave_Radp_Flux_surface` | W/m^2 | 135\* | 611\* | Upward Long\-Wave Rad. Flux at ground or water surface for 00 and 03 forecast |
| `Upward_Long-Wave_Radp_Flux_surface_3_Hour_Average` | W/m^2 | 78\* | 703\* | Upward Long\-Wave Radiation Flux 3 hour average at ground or water surface for 03 forecast |
| `Upward_Long-Wave_Radp_Flux_atmosphere_top_3_Hour_Average` | W/m^2 | 69\* | 384\* | Upward Long\-Wave Radiation Flux 3 hour average at nominal top of the atmosphere for 03 forecast |
| `Upward_Short-Wave_Radiation_Flux_surface` | W/m^2 | 0\* | 869\* | Upward Short\-Wave Radiation Flux at ground or water surface for 00 and 03 forecast |
| `Upward_Short-Wave_Radiation_Flux_surface_3_Hour_Average` | W/m^2 | 0\* | 806\* | Upward Short\-Wave Radiation Flux 3 hour average at ground or water surface for 03 forecast |
| `Upward_Short-Wave_Radiation_Flux_atmosphere_top_3_Hour_Average` | W/m^2 | 0\* | 1049\* | Upward Short\-Wave Radiation Flux 3 hour average at nominal top of the atmosphere for 03 forecast |
| `UV-B_Downward_Solar_Flux_surface_3_Hour_Average` | W/m^2 | 0\* | 24\.7\* | UV\-B Downward Solar Flux 3 hour average at ground or water surface for 03 forecast |
| `Vegetation_surface` | % | 0\* | 99\* | Vegetation at ground or water surface for 00 and 03 forecast |
| `Vegetation_Type_surface` | None | 1\* | 13\* | Vegetation Type at ground or water surface for 00 and 03 forecast |
| `Volumetric_Soil_Moisture_Content_depth_below_surface_layer_5_cm` | Fraction | 0\.03\* | 1\* | Volumetric soil moisture content 5cm below surface layer for 00 and 03 forecast |
| `Volumetric_Soil_Moisture_Content_depth_below_surface_layer_25_cm` | Fraction | 0\.028\* | 1\* | Volumetric soil moisture content 25cm below surface layer for 00 and 03 forecast |
| `Volumetric_Soil_Moisture_Content_depth_below_surface_layer_70_cm` | Fraction | 0\.028\* | 1\* | Volumetric soil moisture content 70cm below surface layer for 00 and 03 forecast |
| `Volumetric_Soil_Moisture_Content_depth_below_surface_layer_150_cm` | Fraction | 0\.028\* | 1\* | Volumetric soil moisture content 150cm below surface layer for 00 and 03 forecast |
| `Water_equivalent_of_accumulated_snow_depth_surface` | kg/m^2 | 0\* | 458\.82\* | Water equivalent of accumulated snow depth at ground or water surface for 00 and 03 forecast |
| `Water_runoff_surface_3_Hour_Accumulation` | kg/m^2 | 0\* | 193\.12\* | Water runoff 3 hour accumulation at ground or water surface for 03 forecast |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| forecast\_hour | INT | Duration of forecast in hours |




### Terms of Use


**Terms of Use**


NOAA data, information, and products, regardless of the method of delivery,
are not subject to copyright and carry no restrictions on their subsequent
use by the public. Once obtained, they may be put to any lawful use. The
forgoing data is in the public domain and is being provided without
restriction on use and distribution. For more information visit the
[NWS disclaimer site](https://www.weather.gov/disclaimer/).




### Citations



Citations:
* Saha, S., S. Moorthi, H. Pan, X. Wu, J. Wang, and Coauthors, 2010: The NCEP
Climate Forecast System Reanalysis. Bulletin of the American Meteorological
Society, 91, 1015\-1057\.
[doi:10\.1175/2010BAMS3001\.1](https://doi.org/10.1175/2010BAMS3001.1)





### DOIs


* [https://doi.org/10\.5065/D6513W89](https://doi.org/10.5065/D6513W89)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CFSR')
.filter(ee.Filter.date('2019-04-01','2019-04-07'));
vartemperatureSurface=dataset.select('Temperature_surface');
varvisParams={
min:192,
max:339,
palette:['blue','purple','cyan','green','yellow','red']
};

varsoilType=dataset.select('Soil_type_surface');
varsoilTypeVisParams={
min:1,
max:9,
palette:[
'red','orange','blue','yellow','violet',
'magenta','cadetblue','pink','aquamarine',]
}
Map.addLayer(
soilType,soilTypeVisParams,'Soil type at the surface',true,0.6);
Map.addLayer(
temperatureSurface,visParams,'Temperature at surface (K)',true,0.6);

Map.setCenter(-88.6,26.4,2);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CFSR)


[CFSR: Climate Forecast System Reanalysis](/earth-engine/datasets/catalog/NOAA_CFSR)

The National Centers for Environmental Prediction (NCEP) Climate Forecast System Reanalysis (CFSR) was designed and executed as a global, high\-resolution, coupled atmosphere\-ocean\-land surface\-sea ice system to provide the best estimate of the state of these coupled domains over the 32\-year period of record from January 1979 to March 2011\. It …

 NOAA/CFSR,
 climate,daylight,flux,forecast,geophysical,ncep,noaa,nws,precipitation,radiation,snow,temperature,vapor,water,weather

2018\-12\-13T00:00:00Z/2025\-07\-16T12:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5065/D6513W89](https://doi.org/https://cfs.ncep.noaa.gov/cfsr/)
* [https://doi.org/10\.5065/D6513W89](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CFSR)









