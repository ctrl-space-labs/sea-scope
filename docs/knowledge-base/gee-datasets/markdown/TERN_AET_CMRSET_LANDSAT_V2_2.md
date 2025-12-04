



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Actual Evapotranspiration for Australia (CMRSET Landsat V2\.2\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================================================








Dataset Availability
2000\-02\-01T00:00:00Z–2024\-06\-01T00:00:00Z
Dataset Provider


[TERN Landscapes / CSIRO Land and Water](https://portal.tern.org.au/actual-evapotranspiration-australia-cmrset-algorithm/21915)



Earth Engine Snippet


`ee.ImageCollection("TERN/AET/CMRSET_LANDSAT_V2_2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TERN/TERN_AET_CMRSET_LANDSAT_V2_2)





Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[australia](/earth-engine/datasets/tags/australia)
[csiro](/earth-engine/datasets/tags/csiro)
[evaporation](/earth-engine/datasets/tags/evaporation)
[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[tern](/earth-engine/datasets/tags/tern)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)
viirs\-derived








#### Description



This dataset provides accurate actual evapotranspiration (AET or ETa) for
Australia using the CMRSET algorithm. The AET band (named 'ETa') contains
the average daily value from the CMRSET model for all cloud\-free Landsat
observations in that month (indicated with value 3 in the AET Data Source QA
bits). After the Landsat 7 ETM\+ Scan Line Corrector (SLC) failed on 31 May
2003, Landsat 7 ETM\+ data are only used if there are no cloud\-free Landsat 5
TM or Landsat 8 OLI data for that month. If there is no cloud\-free Landsat
data available, pixels are infilled with blended data. The blended data will
be blended Landsat\-MODIS until Feb 2012, then blended Landsat\-VIIRS onwards
(indicated with value 2 in the AET Data Source QA bits). If there is no
blended data available in a month, then missing monthly AET values are
linearly interpolated (indicated with value 1 in the AET Data Source QA
bits). This means monthly 30 m AET data covering all Australia, with no gaps
due to cloud, are available and ready to use.


Accurate AET information is important for irrigation, food security, and
environmental management. Like many other parts of the world, water
availability in Australia is limited and AET is the largest consumptive
component of the water balance. In Australia 70% of available water is used
for crop and pasture irrigation. Better monitoring will support improved
water use efficiency in this sector, with any water savings available as
environmental flows. Additionally, ground\-water dependent ecosystems (GDE)
occupy a small area yet are "biodiversity hotspots". Knowing their water
needs enables enhanced management of these critical areas. AET can also be
used to model the catchment water balance. If used in water balance (mass
balance) calculations, then this AET value needs to be multiplied by the
number of days in the month.


To let the developers know you are using this dataset, to get information on
updates, or if you have any questions please contact: tim.mcvicar@csiro.au,
tom.vanniel@csiro.au, jamie.vleeshouwer@csiro.au.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `ETa` | mm/d | Average daily evapotranspiration |
| `pixel_qa` | None | Pixel QA attributes |
| Bitmask for pixel\_qa * Bits 0\-1: AET Data Source 	+ 0: N/A (i.e., surrounding oceans) 	+ 1: AET value was linearly interpolated. 	+ 2: AET value was from data blending. 	(CMRSET\_MCD43\_C6\_LANDSAT\_V2\_0 until Feb 2012, then 	CMRSET\_VIIRS\_LANDSAT\_V2\_0 onwards) 	+ 3: AET value was from CMRSET\_LANDSAT\_V2\_0 * Bit 2: Condensation Adjustment 	+ 0: AET value was not adjusted. 	+ 1: AET value was adjusted to 0 mm/day (due to a negative value). * Bits 3\-6: Number of Landsat observations used for this pixel (0\-15\). * Bit 7: SLC\-Off 	+ 0: SLC\-Off was not applied. 	+ 1: SLC\-Off was applied to Landsat 7 (may contain sensor artifacts). | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Juan P. Guerschman, Tim R. McVicar, Jamie Vleeshower, Thomas G. Van Niel,
Jorge L. Peña\-Arancibia, Yun Chen. Estimating actual evapotranspiration at
field\-to\-continent scales by calibrating the CMRSET algorithm with MODIS,
VIIRS, Landsat and Sentinel\-2 data, Journal of Hydrology, Volume 605, 2022,
127318,
[doi:10\.1016/j.jhydrol.2021\.127318](https://doi.org/10.1016/j.jhydrol.2021.127318).





### DOIs


* [https://doi.org/10\.1016/j.jhydrol.2021\.127318](https://doi.org/10.1016/j.jhydrol.2021.127318)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('TERN/AET/CMRSET_LANDSAT_V2_2');

varvisualization={
bands:['ETa'],
min:0,
max:7,
palette:['d7191c','fdae61','ffffbf','abd9e9','2c7bb6']
};

Map.setCenter(132,-27,4);

Map.addLayer(
dataset,visualization,'Average daily evapotranspiration (mm/day)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TERN/TERN_AET_CMRSET_LANDSAT_V2_2)


[Actual Evapotranspiration for Australia (CMRSET Landsat V2\.2\)](/earth-engine/datasets/catalog/TERN_AET_CMRSET_LANDSAT_V2_2)

This dataset provides accurate actual evapotranspiration (AET or ETa) for Australia using the CMRSET algorithm. The AET band (named 'ETa') contains the average daily value from the CMRSET model for all cloud\-free Landsat observations in that month (indicated with value 3 in the AET Data Source QA bits). After the …

 TERN/AET/CMRSET\_LANDSAT\_V2\_2,
 agriculture,australia,csiro,evaporation,evapotranspiration,landsat\-derived,tern,water\-vapor

2000\-02\-01T00:00:00Z/2024\-06\-01T00:00:00Z



 \-45 110 \-10 155
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1016/j.jhydrol.2021\.127318](https://doi.org/https://portal.tern.org.au/actual-evapotranspiration-australia-cmrset-algorithm/21915)
* [https://doi.org/10\.1016/j.jhydrol.2021\.127318](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/TERN_AET_CMRSET_LANDSAT_V2_2)









