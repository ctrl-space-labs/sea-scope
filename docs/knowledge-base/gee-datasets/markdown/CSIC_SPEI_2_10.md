



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

SPEIbase: Standardised Precipitation\-Evapotranspiration Index database, Version 2\.10


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================================================








Dataset Availability
1901\-01\-01T00:00:00Z–2023\-01\-01T00:00:00Z
Dataset Provider


[Spanish National Research Council (CSIC)](https://spei.csic.es/)



Earth Engine Snippet


`ee.ImageCollection("CSIC/SPEI/2_10")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSIC/CSIC_SPEI_2_10)





Cadence
1 Month
Tags


[climate](/earth-engine/datasets/tags/climate)
[climate\-change](/earth-engine/datasets/tags/climate-change)
[drought](/earth-engine/datasets/tags/drought)
[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[global](/earth-engine/datasets/tags/global)
[monthly](/earth-engine/datasets/tags/monthly)
[palmer](/earth-engine/datasets/tags/palmer)
[precipitation](/earth-engine/datasets/tags/precipitation)
[temperature](/earth-engine/datasets/tags/temperature)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)








#### Description



The Global SPEI database (SPEIbase) offers long\-time robust information
about drought conditions at the global scale, with a 0\.5 degree pixel size
and monthly cadence. It provides SPEI time scales from 1 to 48 months.


The Standardized Precipitation\-Evapotranspiration Index (SPEI) expresses,
as a standardized variate (mean zero and unit variance), the deviations of
the current climatic balance (precipitation minus evapotranspiration
potential) with respect to the long\-term balance. The reference period for
the calculation in the SPEIbase corresponds to the whole study period.
Being a standardized variate means that the SPEI condition can be compared
across space and time.


The SPEIbase is based on the
[FAO\-56 Penman\-Monteith estimation](https://www.fao.org/3/x0490e/x0490e06.htm)
estimation of potential evapotranspiration.
This is a major difference with respect to the SPEI Global Drought Monitor,
that uses the Thornthwaite PET estimation.
The Penman\-Monteith method is considered a superior method, so the
SPEIbase is recommended for most uses including long\-term climatological
analysis.





### Bands



**Pixel Size**
  
55660 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `SPEI_01_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous month |
| `SPEI_02_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 2 months |
| `SPEI_03_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 3 months |
| `SPEI_04_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 4 months |
| `SPEI_05_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 5 months |
| `SPEI_06_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 6 months |
| `SPEI_07_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 7 months |
| `SPEI_08_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 8 months |
| `SPEI_09_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 9 months |
| `SPEI_10_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 10 months |
| `SPEI_11_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 11 months |
| `SPEI_12_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 12 months |
| `SPEI_13_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 13 months |
| `SPEI_14_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 14 months |
| `SPEI_15_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 15 months |
| `SPEI_16_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 16 months |
| `SPEI_17_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 17 months |
| `SPEI_18_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 18 months |
| `SPEI_19_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 19 months |
| `SPEI_20_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 20 months |
| `SPEI_21_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 21 months |
| `SPEI_22_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 22 months |
| `SPEI_23_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 23 months |
| `SPEI_24_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 24 months |
| `SPEI_25_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 25 months |
| `SPEI_26_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 26 months |
| `SPEI_27_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 27 months |
| `SPEI_28_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 28 months |
| `SPEI_29_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 29 months |
| `SPEI_30_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 30 months |
| `SPEI_31_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 31 months |
| `SPEI_32_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 32 months |
| `SPEI_33_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 33 months |
| `SPEI_34_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 34 months |
| `SPEI_35_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 35 months |
| `SPEI_36_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 36 months |
| `SPEI_37_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 37 months |
| `SPEI_38_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 38 months |
| `SPEI_39_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 39 months |
| `SPEI_40_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 40 months |
| `SPEI_41_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 41 months |
| `SPEI_42_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 42 months |
| `SPEI_43_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 43 months |
| `SPEI_44_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 44 months |
| `SPEI_45_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 45 months |
| `SPEI_46_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 46 months |
| `SPEI_47_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 47 months |
| `SPEI_48_month` | \-2\.33 | 2\.33 | Standardized Precipitation\-Evapotranspiration Index (SPEI) where precipitation and evapotranspiration data was accumulated over the previous 48 months |




### Terms of Use


**Terms of Use**


The SPEI database is available under the
[CC\-BY 4\.0 license](https://creativecommons.org/licenses/by/4.0/).


Any public use of the database or works derived from it must include
proper attribution.
Attribution should be given by referencing the document titled:
Beguería, Santiago; Vicente Serrano, Sergio M.; Reig\-Gracia, Fergus;
Latorre Garcés, Borja; 2023;
SPEIbase v.2\.9 \[Dataset]; DIGITAL.CSIC; Version 2\.9\.
[doi:10\.20350/digitalCSIC/15470](https://doi.org/10.20350/digitalCSIC/15470)




### Citations



Citations:
* Reig\-Gracia, Fergus; Latorre Garcés, Borja; 2023;
SPEIbase v.2\.9 \[Dataset]; DIGITAL.CSIC; Version 2\.9\.
[doi:10\.20350/digitalCSIC/15470](https://doi.org/10.20350/digitalCSIC/15470)
* Related publication: Vicente\-Serrano S.M., Beguería S.,
López\-Moreno J.I. (2010\):
A Multi\-scalar drought index sensitive to global warming:
The Standardized Precipitation Evapotranspiration Index \- SPEI.
Journal of Climate 23(7\), 1696\-1718\.
[doi:10\.1175/2009JCLI2909\.1](https://doi.org/10.1175/2009JCLI2909.1)





### DOIs


* [https://doi.org/10\.1175/2009JCLI2909\.1](https://doi.org/10.1175/2009JCLI2909.1)
* [https://doi.org/10\.20350/digitalCSIC/15121](https://doi.org/10.20350/digitalCSIC/15121)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Retrieve the last date from the SPEI dataset.
vardataset=ee.ImageCollection("CSIC/SPEI/2_10").
filterDate('2022-12-01','2023-01-01');

// Select the 24-month analysis.
varspei24=dataset.select('SPEI_24_month');

// Set the visualization ranges and color palette.
varvisParams={
min:-2.33,
max:2.33,
palette:[
'8b1a1a','de2929','f3641d',
'fdc404','9afa94','03f2fd',
'12adf3','1771de','00008b',
]
};

// Set the map center to Spain's location.
Map.setCenter(-3.75,40.47,4);

// Display the SPEI 24-month layer.
Map.addLayer(spei24,visParams,'SPEI 24 month');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CSIC/CSIC_SPEI_2_10)


[SPEIbase: Standardised Precipitation\-Evapotranspiration Index database, Version 2\.10](/earth-engine/datasets/catalog/CSIC_SPEI_2_10)

The Global SPEI database (SPEIbase) offers long\-time robust information about drought conditions at the global scale, with a 0\.5 degree pixel size and monthly cadence. It provides SPEI time scales from 1 to 48 months. The Standardized Precipitation\-Evapotranspiration Index (SPEI) expresses, as a standardized variate (mean zero and unit variance), …

 CSIC/SPEI/2\_10,
 climate,climate\-change,drought,evapotranspiration,global,monthly,palmer,precipitation,temperature,water\-vapor

1901\-01\-01T00:00:00Z/2023\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.20350/digitalCSIC/15121](https://doi.org/https://spei.csic.es/)
* [https://doi.org/10\.20350/digitalCSIC/15121](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/CSIC_SPEI_2_10)









