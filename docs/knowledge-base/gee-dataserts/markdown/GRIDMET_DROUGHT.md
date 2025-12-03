



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GRIDMET DROUGHT: CONUS Drought Indices


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================








Dataset Availability
1980\-01\-05T00:00:00Z–2025\-07\-09T06:00:00Z
Dataset Provider


[University of California Merced](http://www.climatologylab.org/gridmet.html)



Earth Engine Snippet


`ee.ImageCollection("GRIDMET/DROUGHT")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GRIDMET/GRIDMET_DROUGHT)





Cadence
5 Days
Tags


[climate](/earth-engine/datasets/tags/climate)
[conus](/earth-engine/datasets/tags/conus)
[crop](/earth-engine/datasets/tags/crop)
[drought](/earth-engine/datasets/tags/drought)
[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[geophysical](/earth-engine/datasets/tags/geophysical)
[gridmet](/earth-engine/datasets/tags/gridmet)
[merced](/earth-engine/datasets/tags/merced)
[metdata](/earth-engine/datasets/tags/metdata)
[palmer](/earth-engine/datasets/tags/palmer)
[pdsi](/earth-engine/datasets/tags/pdsi)
[precipitation](/earth-engine/datasets/tags/precipitation)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)
climatic\-water\-balance
eddi
spei
spi








#### Description



This dataset contains drought indices derived from the 4\-km daily Gridded
Surface Meteorological (GRIDMET) dataset. The drought indices provided include
the standardized precipitation index (SPI), the evaporative drought demand
index (EDDI), the standardized precipitation evapotranspiration index (SPEI),
the Palmer Drought Severity Index (PDSI) and Palmer Z Index (Z).


SPI, EDDI, and SPEI are supplied on different time scales corresponding to the
time aggregation of precipitation, reference evapotranspiration, and
precipitation minus reference evapotranspiration, respectively. The time scales
include 14 day, 30 day, 90 day, 180 day, 270 day, 1 year, 2 years and 5 years.
The standardization is done by using a non\-parametric standardized probability
based method where plotting positions are used to obtain probabilities which
are transformed to indices assuming an inverse\-normal distribution. All data
are standardized over a common time period of 1981\-2016\.


PDSI and Z are calculated using a modified version of the Palmer formula which
uses reference evapotranspiration and precipitation from GRIDMET, and a static
soil water holding capacity layer (top 1500mm) from STATSGO. Modifications to
the coefficients of the original Palmer formula are applied to calculate PDSI.
The baseline period for PDSI and Z calculations is 1979\-2018\.


Interpretation of the drought indices in this dataset is different for PDSI and
Z than for SPI, SPEI and EDDI. Utilizing the interpretation from the US Drought
monitor, values of these drought indices have the following meaning:


PDSI and z:


* 5\.0 or more (extremely wet)
* 4\.0 to 4\.99 (very wet)
* 3\.0 to 3\.99 (moderately wet),
* 2\.0 to 2\.99 (slightly wet)
* 1\.0 to 1\.99 (incipient wet spell)
* \-0\.99 to 0\.99(near normal)
* \-1\.99 to \-1\.00 (incipient dry spell)
* \-2\.99 to \-2\.00 (mild drought)
* \-3\.99 to \-3\.00 (moderate drought)
* \-4\.99 to \-4\.00 (severe drought)
* \-5\.0 or less (extreme drought)


SPI/SPEI/EDDI:


* 2\.0 or more (extremely wet)
* 1\.6 to 1\.99 (very wet)
* 1\.3 to 1\.59 (moderately wet),
* 0\.8 to 1\.29 (slightly wet)
* 0\.5 to 0\.79 (incipient wet spell)
* \-0\.49 to 0\.49(near normal),
* \-0\.79 to \-0\.5 (incipient dry spell)
* \-1\.29 to \-0\.8 (mild drought)
* \-1\.59 to \-1\.3 (moderate drought)
* \-1\.99 to \-1\.6 (severe drought)
* \-2\.0 or less (extreme drought).


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




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `spi14d` | \-6\* | 6\* | Standardized Precipitation Index (SPI) where precipitation was aggregated for the last 14 days |
| `spi30d` | \-6\* | 6\* | Standardized Precipitation Index (SPI) where precipitation was aggregated for the last 30 days |
| `spi90d` | \-6\* | 6\* | Standardized Precipitation Index (SPI) where precipitation was aggregated for the last 90 days |
| `spi180d` | \-6\* | 6\* | Standardized Precipitation Index (SPI) where precipitation was aggregated for the last 180 days |
| `spi270d` | \-6\* | 6\* | Standardized Precipitation Index (SPI) where precipitation was aggregated for the last 270 days |
| `spi1y` | \-6\* | 6\* | Standardized Precipitation Index (SPI) where precipitation was aggregated for the last 1 year |
| `spi2y` | \-6\* | 6\* | Standardized Precipitation Index (SPI) where precipitation was aggregated for the last 2 years |
| `spi5y` | \-6\* | 6\* | Standardized Precipitation Index (SPI) where precipitation was aggregated for the last 5 years |
| `eddi14d` | \-6\* | 6\* | Evaporative Drought Demand Index (EDDI) where potential evapotranspiration was aggregated for the last 14 days |
| `eddi30d` | \-6\* | 6\* | Evaporative Drought Demand Index (EDDI) where potential evapotranspiration was aggregated for the last 30 days |
| `eddi90d` | \-6\* | 6\* | Evaporative Drought Demand Index (EDDI) where potential evapotranspiration was aggregated for the last 90 days |
| `eddi180d` | \-6\* | 6\* | Evaporative Drought Demand Index (EDDI) where potential evapotranspiration was aggregated for the last 180 days |
| `eddi270d` | \-6\* | 6\* | Evaporative Drought Demand Index (EDDI) where potential evapotranspiration was aggregated for the last 270 days |
| `eddi1y` | \-6\* | 6\* | Evaporative Drought Demand Index (EDDI) where potential evapotranspiration was aggregated for the last 1 year |
| `eddi2y` | \-6\* | 6\* | Evaporative Drought Demand Index (EDDI) where potential evapotranspiration was aggregated for the last 2 years |
| `eddi5y` | \-6\* | 6\* | Evaporative Drought Demand Index (EDDI) where potential evapotranspiration was aggregated for the last 5 years |
| `spei14d` | \-6\* | 6\* | Standardized Precipitation Evapotranspiration Index (SPEI) where climatic water balance was aggregated for the last 14 days |
| `spei30d` | \-6\* | 6\* | Standardized Precipitation Evapotranspiration Index (SPEI) where climatic water balance was aggregated for the last 30 days |
| `spei90d` | \-6\* | 6\* | Standardized Precipitation Evapotranspiration Index (SPEI) where climatic water balance was aggregated for the last 90 days |
| `spei180d` | \-6\* | 6\* | Standardized Precipitation Evapotranspiration Index (SPEI) where climatic water balance was aggregated for the last 180 days |
| `spei270d` | \-6\* | 6\* | Standardized Precipitation Evapotranspiration Index (SPEI) where climatic water balance was aggregated for the last 270 days |
| `spei1y` | \-6\* | 6\* | Standardized Precipitation Evapotranspiration Index (SPEI) where climatic water balance was aggregated for the last 1 year |
| `spei2y` | \-6\* | 6\* | Standardized Precipitation Evapotranspiration Index (SPEI) where climatic water balance was aggregated for the last 2 years |
| `spei5y` | \-6\* | 6\* | Standardized Precipitation Evapotranspiration Index (SPEI) where climatic water balance was aggregated for the last 5 years |
| `pdsi` | \-15\* | 15\* | Palmer Drought Severity Index |
| `z` | \-15\* | 15\* | Palmer Z Index |


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
* Abatzoglou J. T., Development of gridded surface meteorological data for
ecological applications and modelling, International Journal of
Climatology. (2012\)
[doi:10\.1002/joc.3413](https://doi.org/10.1002/joc.3413)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcollection=ee.ImageCollection('GRIDMET/DROUGHT');
print(collection);

// Filter by date
vardS='2020-03-30';
vardE='2020-03-30';
vardSUTC=ee.Date(dS,'GMT');
vardEUTC=ee.Date(dE,'GMT');
varfiltered=collection.filterDate(dSUTC,dEUTC.advance(1,'day'));
print(collection.aggregate_array('system:index'));

// Select variables pdsi and z
varPDSI=filtered.select('pdsi');
varZ=filtered.select('z');

// Select variables for SPI/SPEI/EDDI
// Note that possible timescales for SPI/SPEI/EDDI are:
// 14d (14 day), 30d (30 day), 90d (90 day), 180d (180 day),
// 1y (1 year), 2y (2 year), 5y (5 year)
// Here we choose 2years = 48 months
varSPI2y=filtered.select('spi2y');
varSPEI2y=filtered.select('spei2y');
varEDDI2y=filtered.select('spei2y');

// Make a color palette that is similar to USDM drought classification
varusdmColors='0000aa,0000ff,00aaff,00ffff,aaff55,ffffff,ffff00,fcd37f,ffaa00,e60000,730000';

// Make color options for standardized variables spi/spei/eddi
varminColorbar=-2.5;
varmaxColorbar=2.5;
varcolorbarOptions1={
'min':minColorbar,
'max':maxColorbar,
'palette':usdmColors
};

// Make color options for Palmer variables psdi/z
varminColorbar=-6;
varmaxColorbar=6;
varcolorbarOptions2={
'min':minColorbar,
'max':maxColorbar,
'palette':usdmColors
};

// Add map layers to Google Map
Map.addLayer(ee.Image(PDSI.first()),colorbarOptions2,'PDSI');
Map.addLayer(ee.Image(Z.first()),colorbarOptions2,'Palmer-Z');
Map.addLayer(ee.Image(SPI2y.first()),colorbarOptions1,'SPI-48months');
Map.addLayer(ee.Image(SPEI2y.first()),colorbarOptions1,'SPEI-48months');
Map.addLayer(ee.Image(EDDI2y.first()),colorbarOptions1,'EDDI-48months');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GRIDMET/GRIDMET_DROUGHT)


[GRIDMET DROUGHT: CONUS Drought Indices](/earth-engine/datasets/catalog/GRIDMET_DROUGHT)

This dataset contains drought indices derived from the 4\-km daily Gridded Surface Meteorological (GRIDMET) dataset. The drought indices provided include the standardized precipitation index (SPI), the evaporative drought demand index (EDDI), the standardized precipitation evapotranspiration index (SPEI), the Palmer Drought Severity Index (PDSI) and Palmer Z Index (Z). SPI, EDDI, …

 GRIDMET/DROUGHT,
 climate,conus,crop,drought,evapotranspiration,geophysical,gridmet,merced,metdata,palmer,pdsi,precipitation,surface\-ground\-water,water\-vapor

1980\-01\-05T00:00:00Z/2025\-07\-09T06:00:00Z



 24\.9 \-124\.9 49\.6 \-66\.8
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








