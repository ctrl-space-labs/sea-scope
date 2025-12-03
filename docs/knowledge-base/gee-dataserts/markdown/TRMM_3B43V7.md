



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TRMM 3B43: Monthly Precipitation Estimates


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================








Dataset Availability
1998\-01\-01T00:00:00Z–2019\-12\-01T00:00:00Z
Dataset Provider


[NASA GES DISC at NASA Goddard Space Flight Center](https://doi.org/10.5067/TRMM/TMPA/MONTH/7)



Earth Engine Snippet


`ee.ImageCollection("TRMM/3B43V7")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TRMM/TRMM_3B43V7)





Cadence
1 Month
Tags


[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[jaxa](/earth-engine/datasets/tags/jaxa)
[nasa](/earth-engine/datasets/tags/nasa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[rainfall](/earth-engine/datasets/tags/rainfall)
[trmm](/earth-engine/datasets/tags/trmm)
[weather](/earth-engine/datasets/tags/weather)








#### Description



**This collection is no longer being updated. See
[IMERG monthly](https://developers.google.com/earth-engine/datasets/catalog/NASA_GPM_L3_IMERG_MONTHLY_V06)**


This dataset algorithmically merges microwave data from multiple satellites,
including SSMI, SSMIS, MHS, AMSU\-B and AMSR\-E, each inter\-calibrated to the
TRMM Combined Instrument.


Algorithm 3B43 is executed once per calendar month to produce the single,
best\-estimate precipitation rate and RMS precipitation\-error estimate field
(3B43\) by combining the 3\-hourly merged high\-quality/IR estimates (3B42\)
with the monthly accumulated Global Precipitation Climatology Centre (GPCC)
rain gauge analysis.


All of the global precipitation datasets have some calibrating data source,
which is necessary to control bias differences between contributing
satellites. The multi\-satellite data are averaged to the monthly scale and
combined with the Global Precipitation Climatology Centre's (GPCC) monthly
surface precipitation gauge analysis. In each case the multi\-satellite data
are adjusted to the large\-area mean of the gauge analysis, where available
(mostly over land), and then combined with the gauge analysis using a
simple inverse estimated\-random\-error variance weighting. Regions with poor
gauge coverage, like central Africa and the oceans, have a higher weighting
on the satellite input.


See the [algorithm description](https://trmm.gsfc.nasa.gov/3b43.html)
and the [file specification](https://pps.gsfc.nasa.gov/Documents/filespec.TRMM.V7.pdf)
for details.





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `precipitation` | mm/hr | 0\* | 6\.73\* | Merged microwave/IR precipitation estimate |
| `relativeError` | mm/hr | 0\.001\* | 16\.36\* | Merged microwave/IR precipitation random error estimate |
| `gaugeRelativeWeighting` | % | 0\* | 100\* | Relative weighting of the rain gauges used in calibration |


 \* estimated min or max value


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
vardataset=ee.ImageCollection('TRMM/3B43V7')
.filter(ee.Filter.date('2018-04-01','2018-05-01'));
varprecipitation=dataset.select('precipitation');
varprecipitationVis={
min:0.1,
max:1.2,
palette:['blue','purple','cyan','green','yellow','red'],
};
Map.setCenter(6.746,46.529,3);
Map.addLayer(precipitation,precipitationVis,'Precipitation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TRMM/TRMM_3B43V7)


[TRMM 3B43: Monthly Precipitation Estimates](/earth-engine/datasets/catalog/TRMM_3B43V7)

This collection is no longer being updated. See IMERG monthly This dataset algorithmically merges microwave data from multiple satellites, including SSMI, SSMIS, MHS, AMSU\-B and AMSR\-E, each inter\-calibrated to the TRMM Combined Instrument. Algorithm 3B43 is executed once per calendar month to produce the single, best\-estimate precipitation rate and RMS …

 TRMM/3B43V7,
 climate,geophysical,jaxa,nasa,precipitation,rainfall,trmm,weather

1998\-01\-01T00:00:00Z/2019\-12\-01T00:00:00Z



 \-50 \-180 50 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








