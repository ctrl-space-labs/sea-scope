



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NOAA CDR: Ocean Near\-Surface Atmospheric Properties, Version 2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================================








Dataset Availability
1988\-01\-01T00:00:00Z–2021\-08\-31T00:00:00Z
Dataset Provider


[NOAA](https://www.ncdc.noaa.gov/cdr/atmospheric/ocean-near-surface-atmospheric-properties)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CDR/ATMOS_NEAR_SURFACE/V2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_ATMOS_NEAR_SURFACE_V2)





Cadence
3 Hours
Tags


[atmospheric](/earth-engine/datasets/tags/atmospheric)
[cdr](/earth-engine/datasets/tags/cdr)
[hourly](/earth-engine/datasets/tags/hourly)
[humidity](/earth-engine/datasets/tags/humidity)
[noaa](/earth-engine/datasets/tags/noaa)
[ocean](/earth-engine/datasets/tags/ocean)
[oceans](/earth-engine/datasets/tags/oceans)
[osb](/earth-engine/datasets/tags/osb)
[wind](/earth-engine/datasets/tags/wind)
air\-temperature








#### Description



The Ocean Near\-Surface Atmospheric Properties dataset is part of the NOAA
Ocean Surface Bundle (OSB) and provides a high quality Climate Data Record
(CDR) of air temperature, wind speed, and specific humidity over ice\-free
ocean surfaces.


These atmospheric properties are calculated based on brightness temperature
data from the Special Sensor Microwave/Imager (SSM/I) and the Special Sensor
Microwave/Imager Sounder (SSMIS) on the Defense Meteorological Satellite
Program (DMSP) spacecraft, using a neural network.





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `air_temperature` | °C | \-42\.16\* | 42\.77\* | Air temperature at 10m |
| `specific_humidity` | g/kg | 0\.07\* | 37\.06\* | Specific humidity at 10m |
| `wind_speed` | m/s | 0\.13\* | 71\.45\* | Wind speed at 10m |
| `fill_missing_qc` | None | Quality control flags |
| Bitmask for fill\_missing\_qc * Bits 0\-2: Quality control flags 	+ 0: Pixel values from neural network 	+ 1: Unused flag 	+ 2: Snow/ice 	+ 3: Over land 	+ 4: Over lake 	+ 5: Failed interpolation | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


The NOAA CDR Program's official distribution point for CDRs is NOAA's
National Climatic Data Center which provides sustained, open access and
active data management of the CDR packages and related information in
keeping with the United States' open data policies and practices as
described in the President's Memorandum on "Open Data Policy" and pursuant
to the Executive Order of May 9, 2013, "Making Open and Machine Readable
the New Default for Government Information". In line with these policies,
the CDR data sets are nonproprietary, publicly available, and no
restrictions are placed upon their use. For more information, see the
[Fair Use of NOAA's CDR Data Sets, Algorithms and Documentation](https://www1.ncdc.noaa.gov/pub/data/sds/cdr/CDRs/Aerosol_Optical_Thickness/UseAgreement_01B-04.pdf)
pdf.




### Citations



Citations:
* Clayson, Carol Anne, Brown, Jeremiah, and NOAA CDR Program (2016\). NOAA
Climate Data Record Ocean Surface Bundle (OSB) Climate Data Record
(CDR) of Near\-surface Atmospheric Properties, Version 2\. \[indicate subset
used]. NOAA National ClimaticData Center. [doi:10\.7289/V55T3HH0](https://doi.org/10.7289/V55T3HH0).





### DOIs


* [https://doi.org/10\.7289/V55T3HH0](https://doi.org/10.7289/V55T3HH0)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CDR/ATMOS_NEAR_SURFACE/V2')
.filter(ee.Filter.date('2017-05-01','2017-05-02'));
varairTemperature=dataset.select('air_temperature');
varairTemperatureVis={
min:0.0,
max:30.0,
palette:[
'040274','040281','0502a3','0502b8','0502ce','0502e6',
'0602ff','235cb1','307ef3','269db1','30c8e2','32d3ef',
'3be285','3ff38f','86e26f','3ae237','b5e22e','d6e21f',
'fff705','ffd611','ffb613','ff8b13','ff6e08','ff500d',
'ff0000','de0101','c21301','a71001','911003'
],
};
Map.setCenter(28.3,-28.1,1);
Map.addLayer(airTemperature,airTemperatureVis,'Air Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_ATMOS_NEAR_SURFACE_V2)


[NOAA CDR: Ocean Near\-Surface Atmospheric Properties, Version 2](/earth-engine/datasets/catalog/NOAA_CDR_ATMOS_NEAR_SURFACE_V2)

The Ocean Near\-Surface Atmospheric Properties dataset is part of the NOAA Ocean Surface Bundle (OSB) and provides a high quality Climate Data Record (CDR) of air temperature, wind speed, and specific humidity over ice\-free ocean surfaces. These atmospheric properties are calculated based on brightness temperature data from the Special Sensor …

 NOAA/CDR/ATMOS\_NEAR\_SURFACE/V2,
 atmospheric,cdr,hourly,humidity,noaa,ocean,oceans,osb,wind

1988\-01\-01T00:00:00Z/2021\-08\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7289/V55T3HH0](https://doi.org/https://www.ncdc.noaa.gov/cdr/atmospheric/ocean-near-surface-atmospheric-properties)
* [https://doi.org/10\.7289/V55T3HH0](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_ATMOS_NEAR_SURFACE_V2)









