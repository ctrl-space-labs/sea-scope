



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Copernicus Atmosphere Monitoring Service (CAMS) Global Near\-Real\-Time


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================================================








Dataset Availability
2016\-06\-22T12:00:00Z–2025\-07\-22T12:00:00Z
Dataset Provider


[European Centre for Medium\-Range Weather Forecasts (ECMWF)](https://ads.atmosphere.copernicus.eu/cdsapp#!/dataset/cams-global-atmospheric-composition-forecasts)



Earth Engine Snippet


`ee.ImageCollection("ECMWF/CAMS/NRT")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ECMWF/ECMWF_CAMS_NRT)





Cadence
1 Day
Tags


[aerosol](/earth-engine/datasets/tags/aerosol)
[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[copernicus](/earth-engine/datasets/tags/copernicus)
[ecmwf](/earth-engine/datasets/tags/ecmwf)
[forecast](/earth-engine/datasets/tags/forecast)
particulate\-matter








#### Description



The Copernicus Atmosphere Monitoring Service provides the capacity to
continuously monitor the composition of the Earth's atmosphere at global and
regional scales. The main global near\-real\-time production system is a data
assimilation and forecasting suite providing two 5\-day forecasts per day for
aerosols and chemical compounds that are part of the chemical scheme.


Prior to 2021\-07\-01 only two parameters were available,
1\. Total Aerosol Optical Depth at 550 nm surface
2\. Particulate matter d \< 25 um surface
Note that system:time\_start refers to forecast time.





### Bands



**Pixel Size**
  
44528 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `total_aerosol_optical_depth_at_550nm_surface` | None | 9\.6e\-05\* | 3\.58255\* | Total Aerosol Optical Depth at 550 nm |
| `particulate_matter_d_less_than_25_um_surface` | kg/m^3 | 0\* | 7\.6e\-05\* | Particulate matter d \< 2\.5 um |
| `total_column_nitrogen_dioxide_surface` | kg/m^2 | Total column Nitrogen dioxide surface |
| `total_column_sulphur_dioxide_surface` | kg/m^2 | Total column Sulfur dioxide surface |
| `total_column_carbon_monoxide_surface` | kg/m^2 | Total column Carbon monoxide surface |
| `total_column_formaldehyde_surface` | kg/m^2 | Total column Formaldehyde surface |
| `gems_total_column_ozone_surface` | None | Gems Total column ozone surface |
| `sea_salt_aerosol_optical_depth_at_550nm_surface` | None | Sea Salt Aerosol Optical Depth at 550 nm surface |
| `dust_aerosol_optical_depth_at_550nm_surface` | None | Dust Aerosol Optical Depth at 550 nm surface |
| `organic_matter_aerosol_optical_depth_at_550nm_surface` | None | Organic Matter Aerosol Optical Depth at 550 nm surface |
| `black_carbon_aerosol_optical_depth_at_550nm_surface` | None | Black Carbon Aerosol Optical Depth at 550 nm surface |
| `sulphate_aerosol_optical_depth_at_550nm_surface` | None | Sulfate Aerosol Optical Depth at 550 nm surface |
| `total_aerosol_optical_depth_at_469nm_surface` | None | Total Aerosol Optical Depth at 469 nm surface |
| `total_aerosol_optical_depth_at_670nm_surface` | None | Total Aerosol Optical Depth at 670 nm surface |
| `total_aerosol_optical_depth_at_865nm_surface` | None | Total Aerosol Optical Depth at 865nm surface |
| `total_aerosol_optical_depth_at_1240nm_surface` | None | Total Aerosol Optical Depth at 1240 nm surface |
| `var98-0-210-250_surface` | None | Nitrate aerosol optical depth at 550 nm |
| `var98-0-210-251_surface` | None | Ammonium aerosol optical depth at 550 nm |
| `particulate_matter_d_less_than_1_um_surface` | kg/m^3 | Particulate matter d \< 1 um surface |
| `particulate_matter_d_less_than_10_um_surface` | kg/m^3 | Particulate matter d \< 10 um surface |
| `uv_biologically_effective_dose_surface` | W/m^2 | UV biologically effective dose surface |
| `total_column__peroxyacetyl_nitrate_surface` | kg/m^2 | Total column peroxyacetyl nitrate surface |
| `total_column__isoprene_surface` | kg/m^2 | Total column isoprene surface |
| `total_column_nitrogen_monoxide_surface` | kg/m^2 | Total column nitrogen monoxide surface |
| `total_column_hydrogen_peroxide_surface` | kg/m^2 | Total column hydrogen peroxide surface |
| `total_column_hydroxyl_radical_surface` | kg/m^2 | Total column hydroxyl radical surface |
| `total_column_methane_surface` | kg/m^2 | Total column methane surface |
| `total_column__ethane_surface` | None | Total column ethane surface |
| `total_column_propane_surface` | kg/m^2 | Total column propane surface |
| `total_column_nitric_acid_surface` | kg/m^2 | Total column nitric acid surface |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| model\_initialization\_hour | INT | Product creation hour |
| model\_initialization\_datetime | STRING | Product creation time and date |
| model\_forecast\_hour | INT | Product forecast hour |




### Terms of Use


**Terms of Use**


There is no restriction on use or reproduction and redistribution, with or
without adaptation, for commercial or non\-commercial purposes. This data
policy applies to the data and information generated within the Copernicus
programme, i.e., Sentinel mission data and Copernicus service information.


See the
[full COPERNICUS data license](https://ads.atmosphere.copernicus.eu/api/v2/terms/static/licence-to-use-copernicus-products.pdf).


The license clauses with attribution requirements are shown below:


5\.1\.1\. Where the Licensee communicates or distributes Copernicus Products to
the public, the Licensee shall inform the recipients of the source by using
the following or any similar notice:


* 'Generated using Copernicus Climate Change Service information \[Year]'
and/or
* 'Generated using Copernicus Atmosphere Monitoring Service information
\[Year]'.


5\.1\.2\. Where the Licensee makes or contributes to a publication or
distribution containing adapted or modified Copernicus Products, the
Licensee shall provide the following or any similar notice:


* 'Contains modified Copernicus Climate Change Service information \[Year]';
and/or
* 'Contains modified Copernicus Atmosphere Monitoring Service information
\[Year]'


5\.1\.3\. Any such publication or distribution covered by clauses 5\.1\.1 and


5\.1\.2 shall state that neither the European Commission nor ECMWF is
responsible for any use that may be made of the Copernicus information or
data it contains.




### Citations



Citations:
* Benedetti, A., and Coauthors, 2009: Aerosol analysis and forecast in the
ECMWF Integrated Forecast System. Part II : Data assimilation,
J. Geophys. Res., 114, D13205
[doi:10\.1029/2008JD011115](https://doi.org/10.1029/2008JD011115).
* Morcrette, and Coauthors, 2009: Aerosol analysis and forecast in the
ECMWF Integrated Forecast System. Part I: Forward modelling,
J. Geophys. Res., 114, D06206\.
[doi:10\.1029/2008JD011235](https://doi.org/10.1029/2008JD011235)





### DOIs


* [https://doi.org/10\.1029/2008JD011115](https://doi.org/10.1029/2008JD011115)
* [https://doi.org/10\.1029/2008JD011235](https://doi.org/10.1029/2008JD011235)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Get data generated from model hour 0 for January 1st, 2019.
vardataset=ee.ImageCollection('ECMWF/CAMS/NRT')
.filterDate('2019-01-01','2019-01-02')
.filter('model_initialization_hour == 0');

// Select first and last forecast hours.
varhour00=dataset.filter('model_forecast_hour == 0').first();
varhour21=dataset.filter('model_forecast_hour == 21').first();

// Visualization parameters for specified aerosol band.
varvisParams={
bands:['total_aerosol_optical_depth_at_550nm_surface'],
min:0.0,
max:3.6,
palette:[
'5e4fa2','3288bd','66c2a5','abe0a4','e6f598','ffffbf',
'fee08b','fdae61','f46d43','d53e4f','9e0142'
]
};

// Display forecasts on the map.
Map.setCenter(70,45,3);
Map.addLayer(hour00,visParams,'Total Aerosal Optical Depth - H00',true,0.8);
Map.addLayer(hour21,visParams,'Total Aerosal Optical Depth - H21',true,0.8);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ECMWF/ECMWF_CAMS_NRT)


[Copernicus Atmosphere Monitoring Service (CAMS) Global Near\-Real\-Time](/earth-engine/datasets/catalog/ECMWF_CAMS_NRT)

The Copernicus Atmosphere Monitoring Service provides the capacity to continuously monitor the composition of the Earth's atmosphere at global and regional scales. The main global near\-real\-time production system is a data assimilation and forecasting suite providing two 5\-day forecasts per day for aerosols and chemical compounds that are part of …

 ECMWF/CAMS/NRT,
 aerosol,atmosphere,climate,copernicus,ecmwf,forecast

2016\-06\-22T12:00:00Z/2025\-07\-22T12:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1029/2008JD011235](https://doi.org/https://ads.atmosphere.copernicus.eu/cdsapp#!/dataset/cams-global-atmospheric-composition-forecasts)
* [https://doi.org/10\.1029/2008JD011235](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/ECMWF_CAMS_NRT)









