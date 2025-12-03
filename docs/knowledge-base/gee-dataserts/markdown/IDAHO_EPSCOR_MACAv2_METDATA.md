



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MACAv2\-METDATA: University of Idaho, Multivariate Adaptive Constructed Analogs Applied to Global Climate Models


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================================================================================








Dataset Availability
1900\-01\-01T00:00:00Z–2100\-12\-31T00:00:00Z
Dataset Provider


[University of California Merced](http://www.climatologylab.org/maca.html)



Earth Engine Snippet


`ee.ImageCollection("IDAHO_EPSCOR/MACAv2_METDATA")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/IDAHO_EPSCOR/IDAHO_EPSCOR_MACAv2_METDATA)





Cadence
1 Day
Tags


[climate](/earth-engine/datasets/tags/climate)
[conus](/earth-engine/datasets/tags/conus)
[geophysical](/earth-engine/datasets/tags/geophysical)
[idaho](/earth-engine/datasets/tags/idaho)
[maca](/earth-engine/datasets/tags/maca)
[monthly](/earth-engine/datasets/tags/monthly)








#### Description



The MACAv2\-METDATA dataset is a collection of 20 global
climate models covering the conterminous USA. The Multivariate Adaptive
Constructed Analogs (MACA) method is a statistical downscaling
method which utilizes a training dataset (i.e. a meteorological
observation dataset) to remove historical biases and match spatial
patterns in climate model output.


The MACA method was used to downscale the model output from 20
global climate models (GCMs) of the Coupled Model Inter\-Comparison
Project 5 (CMIP5\) for the historical GCM forcings (1950\-2005\) and
the future Representative Concentration Pathways (RCPs) RCP 4\.5
and RCP 8\.5 scenarios (2006\-2100\) from the native resolution of
the GCMS to 4km.


The full list of models can be found at:
<https://climate.northwestknowledge.net/MACA/GCMs.php>





### Bands



**Pixel Size**
  
4638\.3 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `tasmax` | K | 222\.4\* | 334\.92\* | Maximum daily temperature near surface |
| `tasmin` | K | 215\.33\* | 315\.61\* | Minimum daily temperature near surface |
| `rhsmax` | % | 1\* | 100\* | Maximum daily relative humidity near surface, not present in models CCSM4 or NorESM1\-M |
| `rhsmin` | % | 1\* | 100\* | Minimum daily relative humidity near surface, not present in models CCSM4 or NorESM1\-M |
| `huss` | Mass fraction | 0\* | 0\.05\* | Average daily specific humidity near surface |
| `pr` | mm | 0\* | 1609\.77\* | Average daily precipitation amount at surface |
| `rsds` | W/m^2 | 9\.06\* | 455\.61\* | Average daily downward shortwave radiation at surface |
| `uas` | m/s | \-29\.74\* | 25\.96\* | Average daily eastward component of wind near surface |
| `vas` | m/s | \-29\.26\* | 33\.06\* | Average daily northward component of wind near surface |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| scenario | STRING | Name of the CMIP5 scenario, one of 'rcp85', 'rcp45', or 'historical' |
| model | STRING | Name of the CMIP5 model, eg 'inmcm4' |
| ensemble | STRING | Either 'r1i1p1' or 'r6i1p1' |




### Terms of Use


**Terms of Use**


The MACA datasets were created with funding from the
US government and are in the public domain in the United States.
For further clarity, unless otherwise noted, the MACA datasets
are made available with a Creative Commons CC0 1\.0 Universal dedication.
In short, John Abatzoglou waives all rights to the work worldwide
under copyright law, including all related and neighboring rights,
to the extent allowed by law. You can copy, modify, distribute,
and perform the work, even for commercial purposes, all without
asking permission. John Abatzoglou makes no warranties about the
work, and disclaims liability for all uses of the work, to the
fullest extent permitted by applicable law. Users should properly
cite the source used in the creation of any reports and publications
resulting from the use of this dataset and note the date when the
data was acquired. For more information refer to the [MACA References
and License](https://climate.northwestknowledge.net/MACA/MACAreferences.php)
page.




### Citations



Citations:
* Abatzoglou J.T. and Brown T.J., A comparison of statistical downscaling
methods suited for wildfire applications, International Journal
of Climatology(2012\) [doi:10\.1002/joc.2312](https://doi.org/10.1002/joc.2312).





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('IDAHO_EPSCOR/MACAv2_METDATA')
.filter(ee.Filter.date('2018-08-01','2018-08-15'));
varmaximumTemperature=dataset.select('tasmax');
varmaximumTemperatureVis={
min:290.0,
max:314.0,
palette:['d8d8d8','4addff','5affa3','f2ff89','ff725c'],
};
Map.setCenter(-84.37,33.5,5);
Map.addLayer(maximumTemperature,maximumTemperatureVis,'Maximum Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/IDAHO_EPSCOR/IDAHO_EPSCOR_MACAv2_METDATA)


[MACAv2\-METDATA: University of Idaho, Multivariate Adaptive Constructed Analogs Applied to Global Climate Models](/earth-engine/datasets/catalog/IDAHO_EPSCOR_MACAv2_METDATA)

The MACAv2\-METDATA dataset is a collection of 20 global climate models covering the conterminous USA. The Multivariate Adaptive Constructed Analogs (MACA) method is a statistical downscaling method which utilizes a training dataset (i.e. a meteorological observation dataset) to remove historical biases and match spatial patterns in climate model output. The …

 IDAHO\_EPSCOR/MACAv2\_METDATA,
 climate,conus,geophysical,idaho,maca,monthly

1900\-01\-01T00:00:00Z/2100\-12\-31T00:00:00Z



 24\.9 \-124\.9 49\.6 \-67
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








