



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TerraClimate: Monthly Climate and Climatic Water Balance for Global Terrestrial Surfaces, University of Idaho


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================================================================================================








Dataset Availability
1958\-01\-01T00:00:00Z–2024\-12\-01T00:00:00Z
Dataset Provider


[University of California Merced](http://www.climatologylab.org/terraclimate.html)



Earth Engine Snippet


`ee.ImageCollection("IDAHO_EPSCOR/TERRACLIMATE")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/IDAHO_EPSCOR/IDAHO_EPSCOR_TERRACLIMATE)





Cadence
1 Month
Tags


[climate](/earth-engine/datasets/tags/climate)
[drought](/earth-engine/datasets/tags/drought)
[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[geophysical](/earth-engine/datasets/tags/geophysical)
[global](/earth-engine/datasets/tags/global)
[merced](/earth-engine/datasets/tags/merced)
[monthly](/earth-engine/datasets/tags/monthly)
[palmer](/earth-engine/datasets/tags/palmer)
[pdsi](/earth-engine/datasets/tags/pdsi)
[precipitation](/earth-engine/datasets/tags/precipitation)
[runoff](/earth-engine/datasets/tags/runoff)
[temperature](/earth-engine/datasets/tags/temperature)
[vapor](/earth-engine/datasets/tags/vapor)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)
[wind](/earth-engine/datasets/tags/wind)








#### Description



TerraClimate is a dataset of monthly climate and climatic water balance for
global terrestrial surfaces. It uses climatically aided interpolation,
combining high\-spatial resolution climatological normals from the
[WorldClim dataset](https://www.worldclim.org/), with coarser spatial
resolution, but time\-varying data from
[CRU Ts4\.0](https://data.ceda.ac.uk/badc/cru/data/cru_ts/) and the
[Japanese 55\-year Reanalysis (JRA55\)](https://jra.kishou.go.jp/JRA-55/index_en.html).
Conceptually, the procedure applies interpolated time\-varying anomalies
from CRU Ts4\.0/JRA55 to the high\-spatial resolution climatology of
WorldClim to create a high\-spatial resolution dataset that covers a broader
temporal record.


Temporal information is inherited from CRU Ts4\.0 for most global land
surfaces for temperature, precipitation, and vapor pressure. However,
JRA55 data is used for regions where CRU data had zero climate stations
contributing (including all of Antarctica, and parts of Africa,
South America, and scattered islands). For primary climate variables of
temperature, vapor pressure, and precipitation, the University of Idaho
provides additional data on the number of stations (between 0 and 8\) that
contributed to the CRU Ts4\.0 data used by TerraClimate. JRA55 was used
exclusively for solar radiation and wind speeds.


TerraClimate additionally produces monthly surface water balance datasets
using a water balance model that incorporates reference evapotranspiration,
precipitation, temperature, and interpolated plant extractable soil water
capacity. A modified Thornthwaite\-Mather climatic water\-balance model and
extractable soil water storage capacity data was used at a 0\.5° grid from
Wang\-Erlandsson et al. (2016\).


Data Limitations:


1. Long\-term trends in data are inherited from parent datasets.
TerraClimate should not be used directly for independent assessments of
trends.
2. TerraClimate will not capture temporal variability at finer scales than
parent datasets and thus is not able to capture variability in
orographic precipitation ratios and inversions.
3. The water balance model is very simple and does not account for
heterogeneity in vegetation types or their physiological response to
changing environmental conditions.
4. Limited validation in data\-sparse regions (e.g., Antarctica).





### Bands



**Pixel Size**
  
4638\.3 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `aet` | mm | 0\* | 3140\* | 0\.1 | Actual evapotranspiration, derived using a one\-dimensional soil water balance model |
| `def` | mm | 0\* | 4548\* | 0\.1 | Climate water deficit, derived using a one\-dimensional soil water balance model |
| `pdsi` | None | \-4317\* | 3418\* | 0\.01 | Palmer Drought Severity Index |
| `pet` | mm | 0\* | 4548\* | 0\.1 | Reference evapotranspiration (ASCE Penman\-Montieth) |
| `pr` | mm | 0\* | 7245\* |  | Precipitation accumulation |
| `ro` | mm | 0\* | 12560\* |  | Runoff, derived using a one\-dimensional soil water balance model |
| `soil` | mm | 0\* | 8882\* | 0\.1 | Soil moisture, derived using a one\-dimensional soil water balance model |
| `srad` | W/m^2 | 0\* | 5477\* | 0\.1 | Downward surface shortwave radiation |
| `swe` | mm | 0\* | 32767\* |  | Snow water equivalent, derived using a one\-dimensional soil water balance model |
| `tmmn` | °C | \-770\* | 387\* | 0\.1 | Minimum temperature |
| `tmmx` | °C | \-670\* | 576\* | 0\.1 | Maximum temperature |
| `vap` | kPa | 0\* | 14749\* | 0\.001 | Vapor pressure |
| `vpd` | kPa | 0\* | 1113\* | 0\.01 | Vapor pressure deficit |
| `vs` | m/s | 0\* | 2923\* | 0\.01 | Wind\-speed at 10m |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| status | STRING | 'provisional' or 'permanent' |




### Terms of Use


**Terms of Use**


The data set is in the public domain as licensed under the Creative Commons
Public Domain (CC0\) license.




### Citations



Citations:
* Abatzoglou, J.T., S.Z. Dobrowski, S.A. Parks, K.C. Hegewisch, 2018,
Terraclimate, a high\-resolution global dataset of monthly climate and
climatic water balance from 1958\-2015, Scientific Data 5:170191,
[doi:10\.1038/sdata.2017\.191](https://doi.org/10.1038/sdata.2017.191)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('IDAHO_EPSCOR/TERRACLIMATE')
.filter(ee.Filter.date('2017-07-01','2017-08-01'));
varmaximumTemperature=dataset.select('tmmx');
varmaximumTemperatureVis={
min:-300.0,
max:300.0,
palette:[
'1a3678','2955bc','5699ff','8dbae9','acd1ff','caebff','e5f9ff',
'fdffb4','ffe6a2','ffc969','ffa12d','ff7c1f','ca531a','ff0000',
'ab0000'
],
};
Map.setCenter(71.72,52.48,3);
Map.addLayer(maximumTemperature,maximumTemperatureVis,'Maximum Temperature');
```




Python setup


See the [Python Environment](/earth-engine/guides/python_install) page for information on the Python API and using
 `geemap` for interactive development.



```
importee
importgeemap.coreasgeemap
```


### Colab (Python)



```
dataset = ee.ImageCollection('IDAHO_EPSCOR/TERRACLIMATE').filter(
    ee.Filter.date('2017-07-01', '2017-08-01')
)
maximum_temperature = dataset.select('tmmx')
maximum_temperature_vis = {
    'min': -300.0,
    'max': 300.0,
    'palette': [
        '1a3678',
        '2955bc',
        '5699ff',
        '8dbae9',
        'acd1ff',
        'caebff',
        'e5f9ff',
        'fdffb4',
        'ffe6a2',
        'ffc969',
        'ffa12d',
        'ff7c1f',
        'ca531a',
        'ff0000',
        'ab0000',
    ],
}

m = geemap.Map()
m.set_center(71.72, 52.48, 3)
m.add_layer(
    maximum_temperature, maximum_temperature_vis, 'Maximum Temperature'
)
m
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/IDAHO_EPSCOR/IDAHO_EPSCOR_TERRACLIMATE)


[TerraClimate: Monthly Climate and Climatic Water Balance for Global Terrestrial Surfaces, University of Idaho](/earth-engine/datasets/catalog/IDAHO_EPSCOR_TERRACLIMATE)

TerraClimate is a dataset of monthly climate and climatic water balance for global terrestrial surfaces. It uses climatically aided interpolation, combining high\-spatial resolution climatological normals from the WorldClim dataset, with coarser spatial resolution, but time\-varying data from CRU Ts4\.0 and the Japanese 55\-year Reanalysis (JRA55\). Conceptually, the procedure applies interpolated …

 IDAHO\_EPSCOR/TERRACLIMATE,
 climate,drought,evapotranspiration,geophysical,global,merced,monthly,palmer,pdsi,precipitation,runoff,temperature,vapor,water\-vapor,wind

1958\-01\-01T00:00:00Z/2024\-12\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








