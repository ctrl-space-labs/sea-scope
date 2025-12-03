



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GFS: Global Forecast System 384\-Hour Predicted Atmosphere Data


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================================








Dataset Availability
2015\-07\-01T00:00:00Z–2025\-07\-19T00:00:00Z
Dataset Provider


[NOAA/NCEP/EMC](https://www.ncdc.noaa.gov/data-access/model-data/model-datasets/global-forcast-system-gfs)



Earth Engine Snippet


`ee.ImageCollection("NOAA/GFS0P25")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_GFS0P25)





Cadence
6 Hours
Tags


[climate](/earth-engine/datasets/tags/climate)
[cloud](/earth-engine/datasets/tags/cloud)
[flux](/earth-engine/datasets/tags/flux)
[forecast](/earth-engine/datasets/tags/forecast)
[geophysical](/earth-engine/datasets/tags/geophysical)
[humidity](/earth-engine/datasets/tags/humidity)
[ncep](/earth-engine/datasets/tags/ncep)
[noaa](/earth-engine/datasets/tags/noaa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[radiation](/earth-engine/datasets/tags/radiation)
[temperature](/earth-engine/datasets/tags/temperature)
[vapor](/earth-engine/datasets/tags/vapor)
[weather](/earth-engine/datasets/tags/weather)
[wind](/earth-engine/datasets/tags/wind)
emc
gfs








#### Description



The Global Forecast System (GFS) is a weather forecast model produced by
the National Centers for Environmental Prediction (NCEP). The GFS dataset
consists of selected model outputs (described below) as gridded forecast
variables. The 384\-hour forecasts, with 1\-hour (up to 120 hours)
and 3\-hour (after 120 hours) forecast intervals, are made at 6\-hour temporal
resolution (i.e. updated four times daily). Use the 'creation\_time' and
'forecast\_time' properties to select data of interest.


The GFS is a coupled model, composed of an atmosphere model, an ocean model,
a land/soil model, and a sea ice model which work together to provide an
accurate picture of weather conditions. Note that this model may change;
see [history of recent modifications to the global forecast/analysis system](https://www.emc.ncep.noaa.gov/gmb/STATS/html/model_changes.html)
and the [documentation](https://www.emc.ncep.noaa.gov/emc/pages/numerical_forecast_systems/gfs.php)
for more information. There may be significant hour\-to\-hour and day\-to\-day
fluctuations that require noise\-reduction techniques to be applied to bands
before analysis.


Note that the available forecast hours and intervals have changed over time:


* From 2015/04/01\-2017/07/09: 36\-hour forecasts, excluding hour 0, at
3\-hour intervals.
* From 2017/07/09\-2021/06/11: 384\-hour forecasts, at 1\-hour intervals from
hours 0\-120, at 3\-hour intervals from hours 120\-240, and 12\-hour intervals
from hours 240\-384\.
* From 2021/06/12: 384\-hour forecasts, at 1\-hour intervals from hours 0\-120
and 3\-hour intervals from hours 120\-384\.


Some bands are only available starting on 2025/01/15 as noted in the band
descriptions.





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `temperature_2m_above_ground` | °C | \-69\.18\* | 52\.25\* | Temperature 2m above ground |
| `specific_humidity_2m_above_ground` | Mass fraction | 0\* | 0\.03\* | Specific humidity 2m above ground |
| `dew_point_temperature_2m_above_ground` | °C | \-81\.05\* | 29\.05\* | Dew point temperature 2m above ground (available starting from 2025/01/15\) |
| `relative_humidity_2m_above_ground` | % | 1\* | 100\.05\* | Relative humidity 2m above ground |
| `maximum_temperature_2m_above_ground` | °C | \-60\.73\* | 59\.28\* | Maximum temperature 2m above ground (available starting from 2025/01/15, but only for assets with forecast\_hours \> 0\) |
| `minimum_temperature_2m_above_ground` | °C | \-63\.78\* | 59\.39\* | Minimum temperature 2m above ground (available starting from 2025/01/15, but only for assets with forecast\_hours \> 0\) |
| `u_component_of_wind_10m_above_ground` | m/s | \-60\.73\* | 59\.28\* | U component of wind 10m above ground |
| `v_component_of_wind_10m_above_ground` | m/s | \-63\.78\* | 59\.39\* | V component of wind 10m above ground |
| `total_precipitation_surface` | kg/m^2 | 0\* | 626\.75\* | Cumulative precipitation at surface for the previous 1\-6 hours, depending on the value of the "forecast\_hours" property according to the formula ((F \- 1\) % 6\) \+ 1 (and only for assets with forecast\_hours \> 0\). As a consequence, to calculate the total precipitation by hour X, double\-counting should be avoided by only summing the values for forecast\_hours that are multiples of 6 plus any remainder to reach X. It also means that to determine the precipitation for just hour X, one must subtract the value for the preceding hour unless X is the first hour in a 6\-hour window. |
| `precipitable_water_entire_atmosphere` | kg/m^2 | 0\* | 100\* | Precipitable water for entire atmosphere |
| `u_component_of_wind_planetary_boundary_layer` | m/s | \-66\.8\* | 62\.18\* | U component of wind planetary boundary layer (available starting from 2025/01/15\) |
| `v_component_of_wind_planetary_boundary_layer` | m/s | \-63\.08\* | 57\.6\* | V component of wind planetary boundary layer (available starting from 2025/01/15\) |
| `gust` | m/s | 0\* | 57\.41\* | Wind Speed (Gust) (available starting from 2025/01/15\) |
| `precipitation_rate` | kg/m^2/s | 0\* | 0\.032\* | Precipitation Rate (available starting from 2025/01/15\) |
| `haines_index` | None | 2\* | 6\* | Haines Index (available starting from 2025/01/15\) |
| `ventilation_rate` | m^2/s | 0\* | 234000\* | Ventilation Rate (available starting from 2025/01/15\) |
| `total_cloud_cover_entire_atmosphere` | % | 0\* | 100\* | Total cloud cover for entire atmosphere (previously only for assets with forecast\_hours \> 0, but available for those with forecast\_hours \=\= 0 starting from 2025/01/15\) |
| `downward_shortwave_radiation_flux` | W/m^2 | 0\* | 1230\* | Downward shortwave radiation flux (only for assets with forecast\_hours \> 0\) |
| `downward_longwave_radiation_flux` | W/m^2 | 0\* | 100\* | Downward longwave radiation flux (available starting from 2025/01/15, but only for assets with forecast\_hours \> 0\) |
| `upward_shortwave_radiation_flux` | W/m^2 | 0\* | 1230\* | Upward shortwave radiation flux (available starting from 2025/01/15, but only for assets with forecast\_hours \> 0\) |
| `upward_longwave_radiation_flux` | W/m^2 | 0\* | 100\* | Upward longwave radiation flux (available starting from 2025/01/15, but only for assets with forecast\_hours \> 0\) |
| `planetary_boundary_layer_height` | m | 7\.77\* | 6312\.67\* | Planetary boundary layer height (available starting from 2025/01/15\) |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| creation\_time | DOUBLE | Time of creation |
| forecast\_hours | DOUBLE | Forecast hours |
| forecast\_time | DOUBLE | Forecast time |




### Terms of Use


**Terms of Use**


NOAA data, information, and products, regardless of the method of delivery,
are not subject to copyright and carry no restrictions on their subsequent
use by the public. Once obtained, they may be put to any lawful use. The
forgoing data is in the public domain and is being provided without
restriction on use and distribution.




### Citations



Citations:
* Alpert, J., 2006 Sub\-Grid Scale Mountain Blocking at NCEP, 20th Conf.
WAF/16 Conf. NWP P2\.4\.
* Alpert, J. C., S\-Y. Hong and Y\-J. Kim: 1996, Sensitivity of cyclogenesis
to lower troposphere enhancement of gravity wave drag using the EMC MRF",
Proc. 11 Conf. On NWP, Norfolk, 322\-323\.
* Alpert,J,, M. Kanamitsu, P. M. Caplan, J. G. Sela, G. H. White, and
E. Kalnay, 1988: Mountain induced gravity wave drag parameterization in
the NMC medium\-range forecast model. Pre\-prints, Eighth Conf. on
Numerical Weather Prediction, Baltimore, MD, Amer. Meteor. Soc., 726\-733\.
* Buehner, M., J. Morneau, and C. Charette, 2013: Four\-dimensional
 ensemble\-variational data assimilation for global deterministic weather
 prediction. Nonlinear Processes Geophys., 20, 669\-682\.
* Chun, H.\-Y., and J.\-J. Baik, 1998: Momentum Flux by Thermally Induced
Internal Gravity Waves and Its Approximation for Large\-Scale Models.
J. Atmos. Sci., 55, 3299\-3310\.
* Chun, H.\-Y., Song, I.\-S., Baik, J.\-J. and Y.\-J. Kim. 2004: Impact of a
Convectively Forced Gravity Wave Drag Parameterization in NCAR CCM3\.
J. Climate, 17, 3530\-3547\.
* Chun, H.\-Y., Song, M.\-D., Kim, J.\-W., and J.\-J. Baik, 2001: Effects of
Gravity Wave Drag Induced by Cumulus Convection on the Atmospheric General
Circulation. J. Atmos. Sci., 58, 302\-319\.
* Clough, S.A., M.W. Shephard, E.J. Mlawer, J.S. Delamere, M.J. Iacono,
K.Cady\-Pereira, S. Boukabara, and P.D. Brown, 2005: Atmospheric radiative
transfer modeling: A summary of the AER codes, J. Quant. Spectrosc. Radiat.
Transfer, 91, 233\-244\.
[doi:10\.1016/j.jqsrt.2004\.05\.058](https://doi.org/10.1016/j.jqsrt.2004.05.058)
* Ebert, E.E., and J.A. Curry, 1992: A parameterization of ice cloud optical
properties for climate models. J. Geophys. Res., 97, 3831\-3836\.
* Fu, Q., 1996: An Accurate Parameterization of the Solar Radiative
Properties of Cirrus Clouds for Climate Models. J. Climate, 9, 2058\-2082\.
* Han, J., and H.\-L. Pan, 2006: Sensitivity of hurricane intensity forecast
to convective momentum transport parameterization. Mon. Wea. Rev.,
134, 664\-674\.
* Han, J., and H.\-L. Pan, 2011: Revision of convection and vertical
diffusion schemes in the NCEP global forecast system. Weather and
Forecasting, 26, 520\-533\.
* Han, J., M. Witek, J. Teixeira, R. Sun, H.\-L. Pan, J. K. Fletcher,
and C. S. Bretherton, 2016: Implementation in the NCEP GFS of a hybrid
eddy\-diffusivity mass\-flux (EDMF) boundary layer parameterization with
dissipative heating and modified stable boundary layer mixing. Weather
and Forecasting, 31, 341\-352\.
* Hou, Y., S. Moorthi and K. Campana, 2002: Parameterization of Solar
Radiation Transfer in the NCEP Models, NCEP Office Note \#441, pp46\.
[Available here](https://www.emc.ncep.noaa.gov/officenotes/newernotes/on441.pdf)
* Hu, Y.X., and K. Stamnes, 1993: An accurate parameterization of the
radiative properties of water clouds suitable for use in climate models.
J. Climate, 6, 728\-74\.
* Iacono, M.J., E.J. Mlawer, S.A. Clough, and J.\-J. Morcrette, 2000: Impact
of an improved longwave radiation model, RRTM, on the energy budget and
thermodynamic properties of the NCAR community climate model, CCM3,
J. Geophys. Res., 105(D11\), 14,873\-14,890\.2\.
* Johansson, Ake, 2008: Convectively Forced Gravity Wave Drag in the NCEP
Global Weather and Climate Forecast Systems, SAIC/Environmental Modelling
Center internal report.
* Juang, H\-M, et al. 2014:Regional Spectral Model workshop in memory of
John Roads and Masao Kanamitsu, BAMS, A. Met. Soc, ES61\-ES65\.
* Kim, Y.\-J., and A. Arakawa (1995\), Improvement of orographic gravity wave
parameterization using a mesoscale gravity\-wave model, J. Atmos. Sci.,52,
875\-1902\.
* Kleist, D. T., 2012: An evaluation of hybrid variational\-ensemble data
assimilation for the NCEP GFS , Ph.D. Thesis, Dept. of Atmospheric and
Oceanic Science, University of Maryland\-College Park, 149 pp.
* Lott, F and M. J. Miller: 1997, "A new subgrid\-scale orographic drag
parameterization: Its formulation and testing", QJRMS, 123, pp101\-127\.
* Mlawer, E.J., S.J. Taubman, P.D. Brown, M.J. Iacono, and S.A. Clough,
1997: Radiative transfer for inhomogeneous atmospheres: RRTM, a validated
correlated\-k model for the longwave. J. Geophys. Res., 102, 16663\-16682\.
* Sela, J., 2009: The implementation of the sigma\-pressure hybrid coordinate
into the GFS. NCEP Office Note \#461, pp25\.
* Sela, J., 2010: The derivation of sigmapressure hybrid coordinate
semi\-Lagrangian model equations for the GFS. NCEP Office Note \#462 pp31\.
* Yang, F., 2009: On the Negative Water Vapor in the NCEP GFS: Sources and
Solution. 23rd Conference on Weather Analysis and Forecasting/19th
Conference on Numerical Weather Prediction, 1\-5 June 2009, Omaha, NE.
* Yang, F., K. Mitchell, Y. Hou, Y. Dai, X. Zeng, Z. Wang, and X. Liang,
2008: Dependence of land surface albedo on solar zenith angle: observations
and model parameterizations. Journal of Applied Meteorology and
Climatology.No.11, Vol 47, 2963\-2982\.





### DOIs


* [https://doi.org/10\.1016/j.jqsrt.2004\.05\.058](https://doi.org/10.1016/j.jqsrt.2004.05.058)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/GFS0P25')
.filter(ee.Filter.date('2018-03-01','2018-03-02'));
vartemperatureAboveGround=dataset.select('temperature_2m_above_ground');
varvisParams={
min:-40.0,
max:35.0,
palette:['blue','purple','cyan','green','yellow','red'],
};
Map.setCenter(71.72,52.48,3.0);
Map.addLayer(temperatureAboveGround,visParams,'Temperature Above Ground');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_GFS0P25)


[GFS: Global Forecast System 384\-Hour Predicted Atmosphere Data](/earth-engine/datasets/catalog/NOAA_GFS0P25)

The Global Forecast System (GFS) is a weather forecast model produced by the National Centers for Environmental Prediction (NCEP). The GFS dataset consists of selected model outputs (described below) as gridded forecast variables. The 384\-hour forecasts, with 1\-hour (up to 120 hours) and 3\-hour (after 120 hours) forecast intervals, are …

 NOAA/GFS0P25,
 climate,cloud,flux,forecast,geophysical,humidity,ncep,noaa,precipitation,radiation,temperature,vapor,weather,wind

2015\-07\-01T00:00:00Z/2025\-07\-19T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1016/j.jqsrt.2004\.05\.058](https://doi.org/https://www.ncdc.noaa.gov/data-access/model-data/model-datasets/global-forcast-system-gfs)
* [https://doi.org/10\.1016/j.jqsrt.2004\.05\.058](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_GFS0P25)









