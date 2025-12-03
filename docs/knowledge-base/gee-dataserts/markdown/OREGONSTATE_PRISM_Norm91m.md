



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

PRISM Long\-Term Average Climate Dataset Norm91m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================








Dataset Availability
1991\-01\-01T00:00:00Z–2020\-12\-31T00:00:00Z
Dataset Provider


[PRISM / OREGONSTATE](https://www.prism.oregonstate.edu/)



Earth Engine Snippet


`ee.ImageCollection("OREGONSTATE/PRISM/Norm91m")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OREGONSTATE/OREGONSTATE_PRISM_Norm91m)





Climatological Interval
1 Month
Tags


[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[oregonstate](/earth-engine/datasets/tags/oregonstate)
[precipitation](/earth-engine/datasets/tags/precipitation)
[pressure](/earth-engine/datasets/tags/pressure)
[prism](/earth-engine/datasets/tags/prism)
[temperature](/earth-engine/datasets/tags/temperature)
[vapor](/earth-engine/datasets/tags/vapor)
[weather](/earth-engine/datasets/tags/weather)
30\-year








#### Description



The PRISM daily and monthly datasets are gridded climate
datasets for the conterminous United States, produced by the
PRISM Climate Group at Oregon State University.


Grids are
developed using PRISM (Parameter\-elevation Regressions on Independent
Slopes Model). PRISM interpolation routines simulate how weather
and climate vary with elevation, and account for coastal effects,
temperature inversions, and terrain barriers that can cause rain
shadows. Station data are assimilated from many networks across
the country. For more information, see the [Descriptions of PRISM
Spatial Climate Datasets](https://www.prism.oregonstate.edu/documents/PRISM_datasets.pdf).





### Bands



**Pixel Size**
  
928 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `ppt` | mm | 0\.03\* | 1046\.09\* | 30\-year average of monthly total precipitation (including rain and melted snow) |
| `tmean` | °C | \-16\.15\* | 37\.88\* | 30\-year average of monthly mean temperature (calculated as (tmin\+tmax)/2\) |
| `tmin` | °C | \-21\.9\* | 29\.79\* | 30\-year average of monthly minimum temperature |
| `tmax` | °C | \-10\.78\* | 46\.63\* | 30\-year average of monthly maximum temperature |
| `tdmean` | °C | \-19\.07\* | 25\.22\* | 30\-year average of monthly mean dew point temperature |
| `vpdmin` | hPa | 0\* | 33\.11\* | 30\-year average of monthly minimum vapor pressure deficit |
| `vpdmax` | hPa | 0\.37\* | 94\.11\* | 30\-year average of monthly maximum vapor pressure deficit |
| `solclear` | MJ m^\-2 day^\-1 | 30\-year average of monthly global shortwave solar radiation received on a horizontal surface under clear sky conditions |
| `solslope` | MJ m^\-2 day^\-1 | 30\-year average of monthly global shortwave solar radiation received on a sloped surface |
| `soltotal` | MJ m^\-2 day^\-1 | 30\-year average of monthly global shortwave solar radiation received on a horizontal surface |
| `soltrans` | Fraction | 30\-year average of atmospheric transmittance (cloudiness) |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| PRISM\_DATASET\_CREATE\_DATE | STRING\_LIST | List of original creation dates for each band, e.g: the first element is for the first band "ppt", the second element is for the second band "tmean" |
| PRISM\_DATASET\_TYPE | STRING\_LIST | List of dataset types per\-band |
| PRISM\_CODE\_VERSION | STRING\_LIST | List of code versions per\-band |
| PRISM\_DATASET\_FILENAME | STRING\_LIST | List of original filenames per\-band |




### Terms of Use


**Terms of Use**


These PRISM datasets are available without restriction
on use or distribution. PRISM Climate Group does request that the
user give proper attribution and identify PRISM, where applicable,
as the source of the data.
<https://prism.oregonstate.edu/terms/>




### Citations



Citations:
* Daly, C., Halbleib, M., Smith, J.I., Gibson, W.P., Doggett, M.K.,
Taylor, G.H., Curtis, J., and Pasteris, P.A. 2008\. Physiographically\-sensitive
mapping of temperature and precipitation across the conterminous
United States. International Journal of Climatology, 28: 2031\-2064
[doi:10\.1002/joc.1688](https://doi.org/10.1002/joc.1688)
[pdf](https://www.prism.oregonstate.edu/documents/pubs/2008intjclim_physiographicMapping_daly.pdf).
* \[Daly, C., J.I. Smith, and K.V. Olson. 2015\. Mapping atmospheric
moisture climatologies across the conterminous United States. PloS
ONE 10(10\):e0141140\.
[doi:10\.1371/journal.pone.0141140](https://doi.org/10.1371/journal.pone.0141140).





### DOIs


* [https://doi.org/10\.1371/journal.pone.0141140](https://doi.org/10.1371/journal.pone.0141140)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('OREGONSTATE/PRISM/Norm91m');
varprecipitation=dataset.select('ppt');
varprecipitationVis={
min:0.0,
max:300.0,
palette:['red','yellow','green','cyan','purple'],
};
Map.setCenter(-100.55,40.71,0);
Map.addLayer(precipitation,precipitationVis,'Precipitation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OREGONSTATE/OREGONSTATE_PRISM_Norm91m)


[PRISM Long\-Term Average Climate Dataset Norm91m](/earth-engine/datasets/catalog/OREGONSTATE_PRISM_Norm91m)

The PRISM daily and monthly datasets are gridded climate datasets for the conterminous United States, produced by the PRISM Climate Group at Oregon State University. Grids are developed using PRISM (Parameter\-elevation Regressions on Independent Slopes Model). PRISM interpolation routines simulate how weather and climate vary with elevation, and account for …

 OREGONSTATE/PRISM/Norm91m,
 climate,geophysical,oregonstate,precipitation,pressure,prism,temperature,vapor,weather

1991\-01\-01T00:00:00Z/2020\-12\-31T00:00:00Z



 24 \-125 50 \-66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1371/journal.pone.0141140](https://doi.org/https://www.prism.oregonstate.edu/)
* [https://doi.org/10\.1371/journal.pone.0141140](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OREGONSTATE_PRISM_Norm91m)









