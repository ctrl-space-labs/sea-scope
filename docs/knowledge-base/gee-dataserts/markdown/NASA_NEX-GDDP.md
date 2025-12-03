



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NEX\-GDDP: NASA Earth Exchange Global Daily Downscaled Climate Projections


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2100\-12\-31T00:00:00Z
Dataset Provider


[NASA / Climate Analytics Group](https://www.nccs.nasa.gov/services/data-collections/land-based-products/nex-gddp)



Earth Engine Snippet


`ee.ImageCollection("NASA/NEX-GDDP")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_NEX-GDDP)





Cadence
1 Day
Tags


[cag](/earth-engine/datasets/tags/cag)
[climate](/earth-engine/datasets/tags/climate)
[cmip5](/earth-engine/datasets/tags/cmip5)
[gddp](/earth-engine/datasets/tags/gddp)
[geophysical](/earth-engine/datasets/tags/geophysical)
[ipcc](/earth-engine/datasets/tags/ipcc)
[nasa](/earth-engine/datasets/tags/nasa)
[nex](/earth-engine/datasets/tags/nex)
[precipitation](/earth-engine/datasets/tags/precipitation)
[temperature](/earth-engine/datasets/tags/temperature)








#### Description



The NASA NEX\-GDDP dataset is comprised of downscaled climate scenarios
for the globe that are derived from the General Circulation Model (GCM)
runs conducted under the Coupled Model Intercomparison Project Phase 5
(CMIP5, see [Taylor et al. 2012](https://journals.ametsoc.org/doi/abs/10.1175/BAMS-D-11-00094.1))
and across two of the four greenhouse gas emissions scenarios known as
Representative Concentration Pathways (RCPs, see [Meinshausen et
al. 2011](https://rd.springer.com/article/10.1007%2Fs10584-011-0156-z#page-1)).
The CMIP5 GCM runs were developed in support of the Fifth Assessment
Report of the Intergovernmental Panel on Climate Change (IPCC AR5\).


This dataset was prepared by the Climate Analytics Group and NASA Ames
Research Center using the NASA Earth Exchange, and distributed by the NASA
Center for Climate Simulation (NCCS).





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `pr` | kg/m^2/s | 0\* | 0\.42\* | Daily mean of precipitation at surface; includes both liquid and solid phases from all types of clouds (both large\-scale and convective) |
| `tasmin` | K | 165\.31\* | 318\.89\* | Daily mean of the daily\-minimum near\-surface air temperature |
| `tasmax` | K | 188\.38\* | 335\.13\* | Daily mean of the daily\-maximum near\-surface air temperature |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| model | STRING | Name of the CMIP5 model. It is one of 'ACCESS1\-0', 'bcc\-csm1\-1', 'BNU\-ESM', 'CanESM2', 'CCSM4', 'CESM1\-BGC', 'CNRM\-CM5', 'CSIRO\-Mk3\-6\-0', 'GFDL\-CM3', 'GFDL\-ESM2G', 'GFDL\-ESM2M', 'inmcm4', 'IPSL\-CM5A\-LR', 'IPSL\-CM5A\-MR', 'MIROC\-ESM', 'MIROC\-ESM\-CHEM', 'MIROC5', 'MPI\-ESM\-LR', 'MPI\-ESM\-MR', 'MRI\-CGCM3', 'NorESM1\-M'. |
| scenario | STRING | Name of the CMIP5 scenario. It is one of: 'historical', 'rcp45', 'rcp85', where 'historical' designates retrospective model runs (pre\-2006\). |
| year | DOUBLE | Calendar year |
| month | DOUBLE | Calendar month |
| day | DOUBLE | Calendar day |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* Thrasher, B., Maurer, E. P., McKellar, C., \& Duffy, P. B., 2012:
Technical Note: Bias correcting climate model simulated daily temperature
extremes with quantile mapping. Hydrology and Earth System Sciences,
16(9\), 3309\-3314\.
[doi:10\.5194/hess\-16\-3309\-2012](https://doi.org/10.5194/hess-16-3309-2012)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/NEX-GDDP')
.filter(ee.Filter.date('2018-07-01','2018-07-02'));
varminimumAirTemperature=dataset.select('tasmin');
varminimumAirTemperatureVis={
min:240.0,
max:300.0,
palette:['blue','purple','cyan','green','yellow','red'],
};
Map.setCenter(71.72,52.48,3.0);
Map.addLayer(
minimumAirTemperature,minimumAirTemperatureVis,'Minimum Air Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_NEX-GDDP)


[NEX\-GDDP: NASA Earth Exchange Global Daily Downscaled Climate Projections](/earth-engine/datasets/catalog/NASA_NEX-GDDP)

The NASA NEX\-GDDP dataset is comprised of downscaled climate scenarios for the globe that are derived from the General Circulation Model (GCM) runs conducted under the Coupled Model Intercomparison Project Phase 5 (CMIP5, see Taylor et al. 2012\) and across two of the four greenhouse gas emissions scenarios known as …

 NASA/NEX\-GDDP,
 cag,climate,cmip5,gddp,geophysical,ipcc,nasa,nex,precipitation,temperature

1950\-01\-01T00:00:00Z/2100\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








