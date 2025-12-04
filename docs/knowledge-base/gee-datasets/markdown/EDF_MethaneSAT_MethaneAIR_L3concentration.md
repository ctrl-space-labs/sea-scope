



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MethaneAIR L3 Concentration v1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================








Dataset Availability
2021\-08\-06T00:00:00Z–2023\-10\-14T00:00:00Z
Dataset Provider


[Environmental Defense Fund \- MethaneSAT](https://methanesat.org)



Earth Engine Snippet


`ee.ImageCollection("EDF/MethaneSAT/MethaneAIR/L3concentration")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/EDF/EDF_MethaneSAT_MethaneAIR_L3concentration)





Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[edf](/earth-engine/datasets/tags/edf)
[emissions](/earth-engine/datasets/tags/emissions)
[ghg](/earth-engine/datasets/tags/ghg)
[methane](/earth-engine/datasets/tags/methane)
[methaneair](/earth-engine/datasets/tags/methaneair)
[methanesat](/earth-engine/datasets/tags/methanesat)








#### Description



This dataset provides geospatial data for the total column dry air mole
fraction of methane in the atmosphere, "XCH4", as observed by the MethaneAIR
imaging spectrometer. XCH4 is defined as the total column amount (number of
molecules) of methane ("CH4") divided by the total amount of air (number of
molecules, water vapor amount removed) along the line of sight from the
airborne spectrometer to the earth's surface and back up to the sun.
Additional data layers are provided for reference: observed albedo at 1622
nm, surface pressure, and terrain height.


Methane is a potent greenhouse gas that has more than 80 times the warming power
of carbon dioxide over the first 20 years after it reaches the atmosphere. At
least 30% of today's global warming is driven by methane from human actions.
Cutting methane emissions associated with human activities \- including avoidable
emissions from oil and gas operations, agriculture, and waste management \- is
the single fastest way to slow the rate of global warming.


The aircraft was flown at 11\.5 \- 13 km altitude (37,000 \- 43,000 feet),
acquiring 10 frames per second with a swath of 4\.5 \- 4\.8 km with a 25 degree
field of view and 896 pixels across track, giving a native pixel size at
nadir of approximately 25m along track and 5 m across track. The
spectroscopic data are aggregated by 5 across track, giving a mean pixel
size of 25m x 25m. Concentrations (XCH4\) are retrieved from these high
resolution (0\.1 nm sampling, 0\.3nm resolution), spatially distributed
spectra ([Chan Miller et al. (2024\)](https://doi.org/10.5194/egusphere-2023-1962)),
then gridded on a 0\.0001 x 0\.0001 degree grid (approximately 10m x 8m over
the US). The precision of the gridded data is approximately 25 parts per
billion (1s, about 1\.3%), and a spatial correlation length (1/e) of about
70m. There are some variations from flight\-to\-flight according to operating
conditions, look angle and surface albedo.


The flight pattern was typically a series of oval swaths in a Zamboni
pattern to cover a region, typically about 70 km x 100 km, over a 2 \- 3 hour
interval. The data presented here are averaged where flight tracks overlap,
typically at the edges of each swath and in the urns at the top and bottom
of the Zamboni pattern.


This dataset was generated using MethaneAIR measurements taken on flights
between 30 July 2021 and 13 October 2023\. MethaneAIR is an airborne precursor of
the MethaneSAT satellite mission, managed by [MethaneSAT LLC](https://www.methanesat.org/),
a wholly owned subsidiary of Environmental Defense Fund. Methane emission fluxes were produced using a geostatistical inverse
modeling framework on each of these Zamboni swaths.


For additional information about the MethaneAIR instrument, instrument
calibration and emission detections, please refer to recent publications by
[Loughner et al. (2021\)](https://doi.org/10.1175/JAMC-D-20-0158.1),
[Staebell et al. (2021\)](https://doi.org/10.5194/amt-14-3737-2021),
[Conway et al. (2023\)](https://doi.org/10.5194/amt-2023-111),
[Chulakadabba et al. (2023\)](https://doi.org/10.5194/egusphere-2023-822),
[Abbadi et al. (2023\)](https://doi.org/10.31223/X51D4C),
[Omara et al. (2023\)](https://doi.org/10.5194/essd-15-3761-2023),
and [Miller et al. (2023\)](https://doi.org/10.5194/egusphere-2023-1962).


Contact the data provider for more information about the project at this
link: <https://www.methanesat.org/contact/>





### Bands



**Pixel Size**
  
10\.2 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `XCH4` | ppb | 1894\* | 2114\.65\* | Retrieved column\-averaged dry\-air CH4 mole fraction. |
| `albedo` | None | 0 | 1 | Ratio of solar radiance at the ground to observed radiance at the sensor. |
| `surface_pressure` | hPa | 725\.95\* | 1011\.33\* | Air pressure at the surface. |
| `terrain_height` | km | 0\.026\* | 2\.915\* | Elevation with respect to WGS84 reference ellipsoid. |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| flight\_id | STRING | Research flight number. |
| basin | STRING | Oil and Gas basin (e.g. Permian) or area of interest (e.g. New York City). |
| time\_coverage\_start | STRING | Data collection start time in YYYY\-MM\-DDThh:mm:ssZ format STRING (ISO 8601\). |
| time\_coverage\_end | STRING | Data collection end time in YYYY\-MM\-DDThh:mm:ssZ format STRING (ISO 8601\). |
| processing\_id | STRING | (internal) Processing run identifier that represents the calculations that led to the features. It is not an attribute describing the flight, but the processing pipeline. |




### Terms of Use


**Terms of Use**


Use of this data is subject to [MethaneSAT's Content License Terms of
Use](https://www.methanesat.org/sites/default/files/2025-02/MethaneSAT%20-%20Content%20License%20Terms%20of%20Use%20%28Revised%202-12-2025%29%5B25%5D.pdf).




### Citations



Citations:
* Chan Miller, C., Roche, S., Wilzewski, J. S., Liu, X., Chance, K., Souri,
A. H., Conway, E., Luo, B., Samra, J., Hawthorne, J., Sun, K., Staebell, C.,
Chulakadabba, A., Sargent, M., Benmergui, J. S., Franklin, J. E., Daube, B.
C., Li, Y., Laughner, J. L., Baier, B. C., Gautam, R., Omara, M., and Wofsy,
S. C. 2023\. Methane retrieval from MethaneAIR using the CO2 Proxy Approach:
A demonstration for the upcoming MethaneSAT mission, EGUsphere \[preprint].
[doi:10\.5194/egusphere\-2023\-19623](https://doi.org/10.5194/egusphere-2023-1962),





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection("EDF/MethaneSAT/MethaneAIR/L3concentration");

varfluxVisParams={
bands:['XCH4'],
min:1870,
max:2030,
palette:['#070088','#a3069b','#cc4e64','#ffa826','#edfb59'],
};

// Center on one of the available areas of interests.
Map.setCenter(-102.9,32,8);
Map.addLayer(dataset,fluxVisParams,'Retrieved column-averaged dry-air CH4 mole fraction');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/EDF/EDF_MethaneSAT_MethaneAIR_L3concentration)


[MethaneAIR L3 Concentration v1](/earth-engine/datasets/catalog/EDF_MethaneSAT_MethaneAIR_L3concentration)

This dataset provides geospatial data for the total column dry air mole fraction of methane in the atmosphere, "XCH4", as observed by the MethaneAIR imaging spectrometer. XCH4 is defined as the total column amount (number of molecules) of methane ("CH4") divided by the total amount of air (number of molecules, …

 EDF/MethaneSAT/MethaneAIR/L3concentration,
 atmosphere,climate,edf,emissions,ghg,methane,methaneair,methanesat

2021\-08\-06T00:00:00Z/2023\-10\-14T00:00:00Z



 27\.62 \-118\.42 54\.6 \-73\.44
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








