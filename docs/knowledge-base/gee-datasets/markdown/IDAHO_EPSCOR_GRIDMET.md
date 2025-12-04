



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GRIDMET: University of Idaho Gridded Surface Meteorological Dataset


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================================================








Dataset Availability
1979\-01\-01T00:00:00Z–2025\-07\-14T06:00:00Z
Dataset Provider


[University of California Merced](http://www.climatologylab.org/gridmet.html)



Earth Engine Snippet


`ee.ImageCollection("IDAHO_EPSCOR/GRIDMET")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/IDAHO_EPSCOR/IDAHO_EPSCOR_GRIDMET)





Cadence
1 Day
Tags


[climate](/earth-engine/datasets/tags/climate)
[gridmet](/earth-engine/datasets/tags/gridmet)
[humidity](/earth-engine/datasets/tags/humidity)
[merced](/earth-engine/datasets/tags/merced)
[metdata](/earth-engine/datasets/tags/metdata)
[precipitation](/earth-engine/datasets/tags/precipitation)
[radiation](/earth-engine/datasets/tags/radiation)
[temperature](/earth-engine/datasets/tags/temperature)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)
[wind](/earth-engine/datasets/tags/wind)
fireburning
nfdrs








#### Description



The Gridded Surface Meteorological dataset provides
high spatial resolution (\~4\-km) daily surface fields of temperature,
precipitation, winds, humidity and radiation across the contiguous
United States from 1979\. The dataset blends the high resolution
spatial data from PRISM with the high temporal resolution data
from the National Land Data Assimilation System (NLDAS) to produce
spatially and temporally continuous fields that lend themselves
to additional land surface modeling.


This dataset contains provisional products that are replaced with
updated versions when the complete source data become available.
Products can be distinguished by the value of the 'status' property.
At first, assets are ingested with status\='early'. After several
days, they are replaced by assets with status\='provisional'.
After about 2 months, they are replaced by the final assets with
status\='permanent'.





### Bands



**Pixel Size**
  
4638\.3 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `pr` | mm, daily total | 0\* | 690\.44\* | Precipitation amount |
| `rmax` | % | 1\.05\* | 100\* | Maximum relative humidity |
| `rmin` | % | 0\* | 100\* | Minimum relative humidity |
| `sph` | Mass fraction | 0\* | 0\.02\* | Specific humididy |
| `srad` | W/m^2 | 0\* | 455\.61\* | Surface downward shortwave radiation |
| `th` | deg | Wind direction |
| `tmmn` | K | 225\.54\* | 314\.88\* | Minimum temperature |
| `tmmx` | K | 233\.08\* | 327\.14\* | Maximum temperature |
| `vs` | m/s | 0\.14\* | 29\.13\* | Wind velocity at 10m |
| `erc` | NFDRS fire danger index | 0\* | 131\.85\* | Energy release component |
| `eto` | mm | 0\* | 17\.27\* | Daily grass reference evapotranspiration |
| `bi` | NFDRS fire danger index | 0\* | 214\.2\* | Burning index |
| `fm100` | % | 0\.28\* | 33\.2\* | 100\-hour dead fuel moisture |
| `fm1000` | % | 0\.36\* | 47\.52\* | 1000\-hour dead fuel moisture |
| `etr` | mm | 0\* | 27\.02\* | Daily alfalfa reference evapotranspiration |
| `vpd` | kPa | 0\* | 9\.83\* | Mean vapor pressure deficit |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| status | STRING | 'early', 'provisional', or 'permanent' |




### Terms of Use


**Terms of Use**


This work (METDATA, by John Abatzoglou) is in the public
domain and is free of known copyright restrictions. Users should
properly cite the source used in the creation of any reports and
publications resulting from the use of this dataset and note the
date when the data was acquired.




### Citations



Citations:
* Abatzoglou J. T., Development of gridded surface meteorological
data for ecological applications and modelling, International Journal
of Climatology. (2012\) [doi:10\.1002/joc.3413](https://doi.org/10.1002/joc.3413)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('IDAHO_EPSCOR/GRIDMET')
.filter(ee.Filter.date('2018-08-01','2018-08-15'));
varmaximumTemperature=dataset.select('tmmx');
varmaximumTemperatureVis={
min:290.0,
max:314.0,
palette:['d8d8d8','4addff','5affa3','f2ff89','ff725c'],
};
Map.setCenter(-115.356,38.686,5);
Map.addLayer(maximumTemperature,maximumTemperatureVis,'Maximum Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/IDAHO_EPSCOR/IDAHO_EPSCOR_GRIDMET)


[GRIDMET: University of Idaho Gridded Surface Meteorological Dataset](/earth-engine/datasets/catalog/IDAHO_EPSCOR_GRIDMET)

The Gridded Surface Meteorological dataset provides high spatial resolution (\~4\-km) daily surface fields of temperature, precipitation, winds, humidity and radiation across the contiguous United States from 1979\. The dataset blends the high resolution spatial data from PRISM with the high temporal resolution data from the National Land Data Assimilation System …

 IDAHO\_EPSCOR/GRIDMET,
 climate,gridmet,humidity,merced,metdata,precipitation,radiation,temperature,water\-vapor,wind

1979\-01\-01T00:00:00Z/2025\-07\-14T06:00:00Z



 24\.9 \-124\.9 49\.6 \-66\.8
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








