



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NEX\-DCP30: Ensemble Stats for NASA Earth Exchange Downscaled Climate Projections


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2099\-12\-01T00:00:00Z
Dataset Provider


[NASA / Climate Analytics Group](https://www.nccs.nasa.gov/services/data-collections/land-based-products/nex-dcp30)



Earth Engine Snippet


`ee.ImageCollection("NASA/NEX-DCP30_ENSEMBLE_STATS")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_NEX-DCP30_ENSEMBLE_STATS)





Cadence
1 Month
Tags


[cag](/earth-engine/datasets/tags/cag)
[climate](/earth-engine/datasets/tags/climate)
[cmip5](/earth-engine/datasets/tags/cmip5)
[geophysical](/earth-engine/datasets/tags/geophysical)
[ipcc](/earth-engine/datasets/tags/ipcc)
[nasa](/earth-engine/datasets/tags/nasa)
[nex](/earth-engine/datasets/tags/nex)
[precipitation](/earth-engine/datasets/tags/precipitation)
[temperature](/earth-engine/datasets/tags/temperature)








#### Description



The NASA NEX\-DCP30 dataset is comprised of downscaled climate scenarios
for the conterminous United States that are derived from the General
Circulation Model (GCM) runs conducted under the Coupled Model
Intercomparison Project Phase 5 (CMIP5, see [Taylor et al. 2012](https://journals.ametsoc.org/doi/abs/10.1175/BAMS-D-11-00094.1))
and across the four greenhouse gas emissions scenarios known as
Representative Concentration Pathways (RCPs, see [Meinshausen et al. 2011](https://rd.springer.com/article/10.1007%2Fs10584-011-0156-z#page-1))
developed for the Fifth Assessment Report of the Intergovernmental Panel
on Climate Change (IPCC AR5\). The purpose of these datasets is to provide
a set of high resolution, bias\-corrected climate change projections that
can be used to evaluate climate change impacts on processes that are
sensitive to finer\-scale climate gradients and the effects of local
topography on climate conditions.


The dataset contains monthly projections covering the periods from 1950
through 2005 (Retrospective Run) and from 2006 to 2099 (Prospective Run).
It includes ensemble statistics calculated for each RCP from all model
runs available for the pr, tasmin, and tasmax bands.


NEX\-DCP30 was prepared by the Climate Analytics Group and NASA Ames
Research Center using the NASA Earth Exchange, and distributed by the NASA
Center for Climate Simulation (NCCS).





### Bands



**Pixel Size**
  
927\.67 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `pr_mean` | kg/m^2/s | 0\* | 0\.0006\* | Monthly mean of the daily precipitation rate at surface; includes both liquid and solid phases from all types of clouds (both large\-scale and convective) |
| `pr_quartile25` | kg/m^2/s | 0\* | 0\.0004\* | 25th quartile of the precipitation at surface; includes both liquid and solid phases from all types of clouds (both large\-scale and convective) |
| `pr_median` | kg/m^2/s | 0\* | 0\.0006\* | Median of precipitation at surface; includes both liquid and solid phases from all types of clouds (both large\-scale and convective) |
| `pr_quartile75` | kg/m^2/s | 0\* | 0\.0008\* | 75th quartile of the precipitation at surface; includes both liquid and solid phases from all types of clouds (both large\-scale and convective) |
| `tasmin_mean` | K | 247\.58\* | 311\.09\* | Monthly mean of the daily\-minimum near\-surface air temperature |
| `tasmin_quartile25` | K | 243\.28\* | 310\.06\* | 25th quartile the daily\-minimum near\-surface air temperature |
| `tasmin_median` | K | 246\.87\* | 311\.12\* | Median of the daily\-minimum near\-surface air temperature |
| `tasmin_quartile75` | K | 248\.42\* | 312\.59\* | 75th quartile of the daily\-minimum near\-surface air temperature |
| `tasmax_mean` | K | 258\.47\* | 326\.48\* | Monthly mean of the daily\-maximum near\-surface air temperature |
| `tasmax_quartile25` | K | 256\.13\* | 325\.52\* | 25th quartile of the daily\-maximum near\-surface air temperature |
| `tasmax_median` | K | 257\.89\* | 326\.28\* | Median of the daily\-maximum near\-surface air temperature |
| `tasmax_quartile75` | K | 260\.2\* | 328\.2\* | 75th quartile of the daily\-maximum near\-surface air temperature |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| scenario | STRING | Name of the CMIP5 scenario. It is one of: 'historical', 'rcp26', 'rcp45', 'rcp60', 'rcp85', where 'historical' designates retrospective model runs (pre\-2006\). |
| month | DOUBLE | Calendar month |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* Thrasher, B., J. Xiong, W. Wang, F. Melton, A. Michaelis and R. Nemani
(2013\), Downscaled Climate Projections Suitable for Resource Management,
Eos Trans. AGU, 94(37\), 321\.
[doi:10\.1002/2013EO370002](https://doi.org/10.1002/2013EO370002)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/NEX-DCP30_ENSEMBLE_STATS')
.filter(ee.Filter.date('2018-07-01','2018-07-30'));
varmonthlyMeanMinimumAirTemperature=dataset.select('tasmin_mean');
varmonthlyMeanMinimumAirTemperatureVis={
min:247.0,
max:311.0,
palette:['blue','purple','cyan','green','yellow','red'],
};
Map.setCenter(-115.356,38.686,5);
Map.addLayer(
monthlyMeanMinimumAirTemperature,monthlyMeanMinimumAirTemperatureVis,
'Monthly Mean Minimum Air Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_NEX-DCP30_ENSEMBLE_STATS)


[NEX\-DCP30: Ensemble Stats for NASA Earth Exchange Downscaled Climate Projections](/earth-engine/datasets/catalog/NASA_NEX-DCP30_ENSEMBLE_STATS)

The NASA NEX\-DCP30 dataset is comprised of downscaled climate scenarios for the conterminous United States that are derived from the General Circulation Model (GCM) runs conducted under the Coupled Model Intercomparison Project Phase 5 (CMIP5, see Taylor et al. 2012\) and across the four greenhouse gas emissions scenarios known as …

 NASA/NEX\-DCP30\_ENSEMBLE\_STATS,
 cag,climate,cmip5,geophysical,ipcc,nasa,nex,precipitation,temperature

1950\-01\-01T00:00:00Z/2099\-12\-01T00:00:00Z



 24\.07 \-125\.03 49\.93 \-66\.47
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








