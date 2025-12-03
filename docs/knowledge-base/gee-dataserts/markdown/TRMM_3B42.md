



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TRMM 3B42: 3\-Hourly Precipitation Estimates


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================








Dataset Availability
1998\-01\-01T00:00:00Z–2019\-12\-31T21:00:00Z
Dataset Provider


[NASA GES DISC at NASA Goddard Space Flight Center](https://doi.org/10.5067/TRMM/TMPA/3H/7)



Earth Engine Snippet


`ee.ImageCollection("TRMM/3B42")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TRMM/TRMM_3B42)





Cadence
3 Hours
Tags


[3\-hourly](/earth-engine/datasets/tags/3-hourly)
[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[jaxa](/earth-engine/datasets/tags/jaxa)
[nasa](/earth-engine/datasets/tags/nasa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[rainfall](/earth-engine/datasets/tags/rainfall)
[trmm](/earth-engine/datasets/tags/trmm)
[weather](/earth-engine/datasets/tags/weather)








#### Description



The Tropical Rainfall Measuring Mission (TRMM) is a
joint mission between NASA and the Japan Aerospace Exploration
Agency (JAXA) designed to monitor and study tropical rainfall.
The 34B2 product contains a gridded, TRMM\-adjusted, merged infrared
precipitation (mm/hr) and RMS precipitation\-error estimate, with
a 3\-hour temporal resolution and a 0\.25 degree spatial resolution.


See the [algorithm description](https://trmm.gsfc.nasa.gov/3b42.html)
and the [file specification](https://storm.pps.eosdis.nasa.gov/storm/data/docs/filespec.TRMM.V7.3B42.pdf)
for details.


Documentation:


* [PI Documentation](https://docserver.gesdisc.eosdis.nasa.gov/public/project/GPM/3B42_3B43_doc_V7.pdf)
* [File Specification for TRMM Products](https://pps.gsfc.nasa.gov/Documents/filespec.TRMM.V7.pdf)
* [Comparison between TRMM versions 6 and 7](https://pps.gsfc.nasa.gov/Documents/formatChangesV7.pdf)
* [Readme](https://disc2.gesdisc.eosdis.nasa.gov/data/TRMM_L3/TRMM_3B42/doc/README.TRMM_V7.pdf)
* [Details of the TMPA algorithm used in this product](https://pmm.nasa.gov/sites/default/files/imce/3B42_3B43_TMPA_restart.pdf)
* [TRMM Data Gaps](https://web.archive.org/web/20200701000000*/ftp://gpmweb2.pps.eosdis.nasa.gov/tsdis/AB/docs/anomalous.html)
* [Transition from TMPA to IMERG](https://docserver.gesdisc.eosdis.nasa.gov/public/project/GPM/TMPA-to-IMERG_transition.pdf)





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `precipitation` | mm/hr | 0 | 100 | Merged microwave/IR precipitation estimate |
| `relativeError` | mm/hr | 0 | 100 | Merged microwave/IR precipitation random error estimate |
| `satPrecipitationSource` | None | Flag to show source of data |
| Bitmask for satPrecipitationSource * Bits 0\-5: Source 	+ 0: No observation 	+ 1: AMSU 	+ 2: TMI 	+ 3: AMSR 	+ 4: SSMI 	+ 5: SSMI/S 	+ 6: MHS 	+ 7: TCI 	+ 30: AMSU/MHS average 	+ 31: Conical scanner average 	+ 50: IR | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `HQprecipitation` | mm/hr | 0 | 100 | Pre\-gauge\-adjusted microwave precipitation estimate |
| `IRprecipitation` | mm/hr | 0 | 100 | Pre\-gauge\-adjusted infrared precipitation estimate |
| `satObservationTime` | min | \-90 | 90 | Satellite observation time minus the time of the granule. In case of overlapping satellite observations, the two or more observation times are equal\-weighting averaged. |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* Adler, R.F., G.J. Huffman, A. Chang, R. Ferraro, P. Xie, J. Janowiak,
B. Rudolf, U. Schneider, S. Curtis, D. Bolvin, A. Gruber, J. Susskind,
P. Arkin, E.J. Nelkin, 2003: The Version 2 Global Precipitation
Climatology Project (GPCP) Monthly Precipitation Analysis (1979\-Present).
J. Hydrometeor., 4(6\), 1147\-1167\.
* Huffman, G.J., 1997: Estimates of Root\-Mean\-Square Random Error
for Finite Samples of Estimated Precipitation, J. Appl. Meteor.,
1191\-1201\.
* Huffman, G.J., 2012: Algorithm Theoretical Basis Document (ATBD)
Version 3\.0 for the NASA Global Precipitation Measurement (GPM)
Integrated Multi\-satellitE Retrievals for GPM (I\-MERG). GPM Project,
Greenbelt, MD, 29 pp.
* Huffman, G.J., R.F. Adler, P. Arkin, A. Chang, R. Ferraro, A.
Gruber, J. Janowiak, A. McNab, B. Rudolph, and U. Schneider, 1997:
The Global Precipitation Climatology Project (GPCP) Combined Precipitation
Dataset, Bul. Amer. Meteor. Soc., 78, 5\-20\.
* Huffman, G.J., R.F. Adler, D.T. Bolvin, G. Gu, E.J. Nelkin, K.P.
Bowman, Y. Hong, E.F. Stocker, D.B. Wolff, 2007: The TRMM Multi\-satellite
Precipitation Analysis: Quasi\-Global, Multi\-Year, Combined\-Sensor
Precipitation Estimates at Fine Scale. J. Hydrometeor., 8(1\), 38\-55\.
* Huffman, G.J., R.F. Adler, M. Morrissey, D.T. Bolvin, S. Curtis,
R. Joyce, B McGavock, J. Susskind, 2001: Global Precipitation at
One\-Degree Daily Resolution from Multi\-Satellite Observations. J.
Hydrometeor., 2(1\), 36\-50\.
* Huffman, G.J., R.F. Adler, B. Rudolph, U. Schneider, and P. Keehn,
1995: Global Precipitation Estimates Based on a Technique for Combining
Satellite\-Based Estimates, Rain Gauge Analysis, and NWP Model Precipitation
Information, J. Clim., 8, 1284\-1295\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('TRMM/3B42')
.filter(ee.Filter.date('2018-04-01','2018-04-10'));
varprecipitation=
dataset.select(['precipitation','HQprecipitation','IRprecipitation']);
varprecipitationVis={
min:0,
max:12,
gamma:5,
};
Map.setCenter(-79.98,23.32,4);
Map.addLayer(precipitation,precipitationVis,'Precipitation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TRMM/TRMM_3B42)


[TRMM 3B42: 3\-Hourly Precipitation Estimates](/earth-engine/datasets/catalog/TRMM_3B42)

The Tropical Rainfall Measuring Mission (TRMM) is a joint mission between NASA and the Japan Aerospace Exploration Agency (JAXA) designed to monitor and study tropical rainfall. The 34B2 product contains a gridded, TRMM\-adjusted, merged infrared precipitation (mm/hr) and RMS precipitation\-error estimate, with a 3\-hour temporal resolution and a 0\.25 degree …

 TRMM/3B42,
 3\-hourly,climate,geophysical,jaxa,nasa,precipitation,rainfall,trmm,weather

1998\-01\-01T00:00:00Z/2019\-12\-31T21:00:00Z



 \-50 \-180 50 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








