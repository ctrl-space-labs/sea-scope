



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GPM: Monthly Global Precipitation Measurement (GPM) v6


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================








Dataset Availability
2000\-06\-01T00:00:00Z–2021\-09\-01T00:00:00Z
Dataset Provider


[NASA GES DISC at NASA Goddard Space Flight Center](https://doi.org/10.5067/GPM/IMERG/3B-MONTH/06)



Earth Engine Snippet


`ee.ImageCollection("NASA/GPM_L3/IMERG_MONTHLY_V06")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GPM_L3_IMERG_MONTHLY_V06)





Cadence
1 Month
Tags


[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[gpm](/earth-engine/datasets/tags/gpm)
[imerg](/earth-engine/datasets/tags/imerg)
[jaxa](/earth-engine/datasets/tags/jaxa)
[monthly](/earth-engine/datasets/tags/monthly)
[nasa](/earth-engine/datasets/tags/nasa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[weather](/earth-engine/datasets/tags/weather)








#### Description



IMERG\-Final version "06" stopped being produced in September, 2021\.
Version "07" is expected to be released in September 2022


Global Precipitation Measurement (GPM) is an international
satellite mission to provide next\-generation observations of
rain and snow worldwide every three hours. The Integrated Multi\-satellitE
Retrievals for GPM (IMERG) is the unified algorithm that provides
rainfall estimates combining data from all passive\-microwave
instruments in the GPM Constellation.


This algorithm is intended to intercalibrate, merge, and interpolate
all satellite microwave precipitation estimates, together with
microwave\-calibrated infrared (IR) satellite estimates, precipitation
gauge analyses, and potentially other precipitation estimators at fine
time and space scales for the TRMM and GPM eras over the entire globe.
The system is run several times for each observation time, first
giving a quick estimate and successively providing better estimates
as more data arrive. The final step uses monthly gauge data to
create research\-level products. See [IMERG Technical Documentation](https://pmm.nasa.gov/sites/default/files/document_files/IMERG_doc.pdf)
for more details on the algorithm.


Documentation:


* [Algorithm Theoretical Basis Document](https://docserver.gesdisc.eosdis.nasa.gov/public/project/GPM/IMERG_ATBD_V06.pdf)
* [IMERG Quality Index](https://docserver.gesdisc.eosdis.nasa.gov/public/project/GPM/IMERGV06_QI.pdf)
* [Caveats for IMERG extension into TRMM era](https://docserver.gesdisc.eosdis.nasa.gov/public/project/GPM/IMERGV06_TRMMera-caveats.pdf)
* [IMERG Technical Documentation](https://docserver.gesdisc.eosdis.nasa.gov/public/project/GPM/IMERG_doc.06.pdf)
* [Release notes; New Morphing algorithm](https://docserver.gesdisc.eosdis.nasa.gov/public/project/GPM/MorphingInV06IMERG.pdf)
* [Remote\-Sensing Reflectance](https://gpm1.gesdisc.eosdis.nasa.gov/data/GPM_L3/doc/README.GPM.pdf)
* [Anomalies](https://gpmweb2https.pps.eosdis.nasa.gov/tsdis/AB/docs/gpm_anomalous.html)





### Bands



**Pixel Size**
  
11132 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `gaugeRelativeWeighting` | % | Weighting of gauge precipitation relative to the multi\-satellite precipitation |
| `precipitation` | mm/hr | Merged satellite\-gauge precipitation estimate |
| `precipitationQualityIndex` | Equivalent gauges per 2\.5 degree box | Quality Index for precipitation field |
| `probabilityLiquidPrecipitation` | % | Accumulation\-weighted probability of liquid precipitation phase |
| `randomError` | mm/hr | Random error for merged satellite\-gauge precipitation |




### Terms of Use


**Terms of Use**


All NASA\-produced data from the GPM mission is made freely available for the public to use.




### Citations



Citations:
* Huffman, G.J., E.F. Stocker, D.T. Bolvin, E.J. Nelkin, Jackson Tan (2019\),
GPM IMERG Final Precipitation L3 1 month 0\.1 degree x 0\.1 degree V06,
Greenbelt, MD, Goddard Earth Sciences Data and Information Services Center
(GES DISC), Accessed: \[Data Access Date], 10\.5067/GPM/IMERG/3B\-MONTH/06





### DOIs


* [https://doi.org/10\.5067/GPM/IMERG/3B\-MONTH/06](https://doi.org/10.5067/GPM/IMERG/3B-MONTH/06)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/GPM_L3/IMERG_MONTHLY_V06')
.filterDate('2019-01-01','2020-01-01');

// Select the max precipitation and mask out low precipitation values.
varprecipitation=dataset.select('precipitation').max();
varmask=precipitation.gt(0.25);
varprecipitation=precipitation.updateMask(mask);

varpalette=[
'000096','0064ff','00b4ff','33db80','9beb4a',
'ffeb00','ffb300','ff6400','eb1e00','af0000'
];
varprecipitationVis={min:0.0,max:1.5,palette:palette};
Map.addLayer(precipitation,precipitationVis,'Precipitation (mm/hr)');
Map.setCenter(-76,33,3);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GPM_L3_IMERG_MONTHLY_V06)


[GPM: Monthly Global Precipitation Measurement (GPM) v6](/earth-engine/datasets/catalog/NASA_GPM_L3_IMERG_MONTHLY_V06)

IMERG\-Final version "06" stopped being produced in September, 2021\. Version "07" is expected to be released in September 2022 Global Precipitation Measurement (GPM) is an international satellite mission to provide next\-generation observations of rain and snow worldwide every three hours. The Integrated Multi\-satellitE Retrievals for GPM (IMERG) is the unified …

 NASA/GPM\_L3/IMERG\_MONTHLY\_V06,
 climate,geophysical,gpm,imerg,jaxa,monthly,nasa,precipitation,weather

2000\-06\-01T00:00:00Z/2021\-09\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/GPM/IMERG/3B\-MONTH/06](https://doi.org/https://doi.org/10.5067/GPM/IMERG/3B-MONTH/06)
* [https://doi.org/10\.5067/GPM/IMERG/3B\-MONTH/06](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_GPM_L3_IMERG_MONTHLY_V06)









