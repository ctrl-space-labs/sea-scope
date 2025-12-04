



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NEX\-GDDP\-CMIP6: NASA Earth Exchange Global Daily Downscaled Climate Projections


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2100\-12\-31T00:00:00Z
Dataset Provider


[NASA / Climate Analytics Group](https://www.nccs.nasa.gov/services/data-collections/land-based-products/nex-gddp-cmip6)



Earth Engine Snippet


`ee.ImageCollection("NASA/GDDP-CMIP6")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GDDP-CMIP6)





Cadence
1 Day
Tags


[cag](/earth-engine/datasets/tags/cag)
[climate](/earth-engine/datasets/tags/climate)
[gddp](/earth-engine/datasets/tags/gddp)
[geophysical](/earth-engine/datasets/tags/geophysical)
[ipcc](/earth-engine/datasets/tags/ipcc)
[nasa](/earth-engine/datasets/tags/nasa)
[nex](/earth-engine/datasets/tags/nex)
[precipitation](/earth-engine/datasets/tags/precipitation)
[temperature](/earth-engine/datasets/tags/temperature)








#### Description



The NEX\-GDDP\-CMIP6 dataset is comprised of global downscaled climate
scenarios derived from the General Circulation Model (GCM) runs conducted
under the Coupled Model Intercomparison Project Phase 6 (CMIP6, see
[Thrasher et al. 2022](https://doi.org/10.7917/OFSG3345)) and across two of
the four "Tier 1" greenhouse gas emissions scenarios known as Shared
Socioeconomic Pathways (SSPs).


The CMIP6 GCM runs were developed in support of the Sixth Assessment Report
of the Intergovernmental Panel on Climate Change (IPCC AR6\). This dataset
includes downscaled projections from ScenarioMIP model runs for which daily
scenarios were produced and distributed through the Earth System Grid
Federation.


This collection contains 34 different models. One model, "GFDL\-CM4," has
data for two different configurations that can be differentiated by further
filtering on the *grid\_label* property.


Bands are replaced as new versions become available and the *version*
property is updated with them.


See also
[the provider tech note](https://www.nccs.nasa.gov/sites/default/files/NEX-GDDP-CMIP6-Tech_Note.pdf).


[You can submit data questions about CMIP6 to the provider](https://airtable.com/shr01weJfA7DYq6jf)
and
[see their answers](https://airtable.com/shrX4mj20TLSH0r2y/tblUMAYpCfCCwucSV).





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `hurs` | % | \-101\.85\* | 179\.44\* | Near\-surface relative humidity. Not present in these models: 'BCC\-CSM2\-MR', 'NESM3', 'KIOST\-ESM' (only for scenario 'ssp245' in 2058\). |
| `huss` | Mass fraction | \-0\.007\* | 11\.76\* | Near\-surface specific humidity. Not present in these models: 'IPSL\-CM6A\-LR', 'MIROC6', 'NESM3'. |
| `pr` | kg/m^2/s | 0\* | 0\.0083\* | Precipitation (mean of the daily precipitation rate) |
| `rlds` | W/m^2 | \-481\.17\* | 908\.96\* | Surface downwelling longwave radiation |
| `rsds` | W/m^2 | \-702710\* | 553087\* | Surface downwelling shortwave radiation |
| `sfcWind` | m/s | \-4\.98\* | 28\.29\* | Daily\-mean near\-surface wind speed |
| `tas` | K | 192\.15\* | 336\.94\* | Daily near\-surface air temperature. Not present in these models: 'NorESM2\-LM' (only for scenario 'ssp585' in 2096\). |
| `tasmin` | K | 163\.66\* | 334\.92\* | Daily minimum near\-surface air temperature. Not present in these models: 'CESM2', 'CESM2\-WACCM', 'IITM\-ESM', 'TaiESM1' (only for scenario 'ssp585' in 2093\). |
| `tasmax` | K | 202\.09\* | 352\.77\* | Daily maximum near\-surface air temperature. Not present in these models: 'CESM2', 'CESM2\-WACCM', 'IITM\-ESM'. |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| model | STRING | Name of the CMIP6 model. It is one of:* ACCESS\-CM2 * ACCESS\-ESM1\-5 * BCC\-CSM2\-MR * CESM2 * CESM2\-WACCM * CMCC\-CM2\-SR5 * CMCC\-ESM2 * CNRM\-CM6\-1 * CNRM\-ESM2\-1 * CanESM5 * EC\-Earth3 * EC\-Earth3\-Veg\-LR * FGOALS\-g3 * GFDL\-CM4 (see *grid\_label* for additional information) * GFDL\-ESM4 * GISS\-E2\-1\-G * HadGEM3\-GC31\-LL * HadGEM3\-GC31\-MM * IITM\-ESM * INM\-CM4\-8 * INM\-CM5\-0 * IPSL\-CM6A\-LR * KACE\-1\-0\-G * KIOST\-ESM * MIROC\-ES2L * MIROC6 * MPI\-ESM1\-2\-HR * MPI\-ESM1\-2\-LR * MRI\-ESM2\-0 * NESM3 * NorESM2\-LM * NorESM2\-MM * TaiESM1 * UKESM1\-0\-LL |
| scenario | STRING | Name of the CMIP6 scenario. It is one of:* historical (retrospective model runs pre\-2015\) * ssp245 * ssp585 |
| year | DOUBLE | Calendar year |
| month | DOUBLE | Calendar month |
| day | DOUBLE | Calendar day |
| grid\_label | STRING | The grid label, which is only set when differentiating simulation results for the 'GFDL\-CM4' model. It is one of:* gr1 * gr2 |
| license | STRING | The license under which a model is released. It will be one of:* CC\-BY\-4\.0 (Creative Commons Attribution 4\.0 International) * CC0\-1\.0 (Creative Commons Zero v1\.0 Universal) |
| interpolated | STRING | Present and 'true' if data for a particular day has been filled in using the value from the previous day. This happens when the simulation does not produce a data band for every day in the year. The following models always duplicate the last day in leap years because they only yield 365 bands: 'BCC\-CSM2\-MR', 'CanESM5', 'CESM2', 'CESM2\-WACCM', 'CMCC\-CM2\-SR5', 'CMCC\-ESM2', 'FGOALS\-g3', 'GFDL\-CM4', 'GFDL\-ESM4', 'GISS\-E2\-1\-G', 'INM\-CM4\-8', 'INM\-CM5\-0', 'KIOST\-ESM', 'NorESM2\-LM', 'NorESM2\-MM', 'TaiESM1'. These models yield 360 bands per year and have the outstanding 5 or 6 days filled by duplicating one every 60\-70 days: 'HadGEM3\-GC31\-LL', 'HadGEM3\-GC31\-MM', 'KACE\-1\-0\-G', 'UKESM1\-0\-LL'. 'IITM\-ESM' only has 364 bands in years divisible by 5 (and does not have data for 2100 at all), so the final day is always duplicated, plus the midpoint day in leap years. |
| version | DOUBLE | The version of the asset, possible values are 1\.0, 1\.1 and 1\.2 |




### Terms of Use


**Terms of Use**


All CMIP6 GCM model inputs and any derivatives work, such as this dataset,
are governed by the original
[Terms of use](https://pcmdi.llnl.gov/CMIP6/TermsOfUse/TermsOfUse6-1.html)
and may have some restrictions on usage. See the "license" property on
each EE Image that notes the specific license the data may fall under.


(Note that while the official Terms of Use mention that some models are
restricted under 'CC\-BY\-SA\-4\.0' (Creative Commons Attribution Share Alike 4\.0 International), models available in EarthEngine either fall
under 'CC\-BY\-4\.0' (Creative Commons Attribution 4\.0 International) or 'CC0\-1\.0' (Creative Commons Zero v1\.0 Universal).)




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
vardataset=ee.ImageCollection('NASA/GDDP-CMIP6')
.filter(ee.Filter.date('2014-07-01','2014-07-02'))
.filter(ee.Filter.eq('model','ACCESS-CM2'));
varminimumAirTemperature=dataset.select('tasmin');
varminimumAirTemperatureVis={
min:240,
max:310,
palette:['blue','purple','cyan','green','yellow','red'],
};
Map.setCenter(71,52,3);
Map.addLayer(
minimumAirTemperature,minimumAirTemperatureVis,
'Minimum Air Temperature (K)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GDDP-CMIP6)


[NEX\-GDDP\-CMIP6: NASA Earth Exchange Global Daily Downscaled Climate Projections](/earth-engine/datasets/catalog/NASA_GDDP-CMIP6)

The NEX\-GDDP\-CMIP6 dataset is comprised of global downscaled climate scenarios derived from the General Circulation Model (GCM) runs conducted under the Coupled Model Intercomparison Project Phase 6 (CMIP6, see Thrasher et al. 2022\) and across two of the four "Tier 1" greenhouse gas emissions scenarios known as Shared Socioeconomic Pathways …

 NASA/GDDP\-CMIP6,
 cag,climate,gddp,geophysical,ipcc,nasa,nex,precipitation,temperature

1950\-01\-01T00:00:00Z/2100\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








