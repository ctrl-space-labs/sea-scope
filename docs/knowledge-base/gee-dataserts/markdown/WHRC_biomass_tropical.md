



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WHRC Pantropical National Level Carbon Stock Dataset


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================








Dataset Availability
2012\-01\-29T00:00:00Z–2012\-01\-29T00:00:00Z
Dataset Provider


[WHRC](https://www.woodwellclimate.org/)



Earth Engine Snippet


`ee.Image("WHRC/biomass/tropical")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WHRC/WHRC_biomass_tropical)





Tags


[aboveground](/earth-engine/datasets/tags/aboveground)
[biomass](/earth-engine/datasets/tags/biomass)
[carbon](/earth-engine/datasets/tags/carbon)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[geophysical](/earth-engine/datasets/tags/geophysical)
[umd](/earth-engine/datasets/tags/umd)
pantropical
tropical
whrc








#### Description



A national\-level map of above\-ground live woody biomass density for
tropical countries at 500m. This dataset was assembled from a combination
of co\-located field measurements, LiDAR observations, and imagery recorded
from the Moderate Resolution Imaging Spectroradiometer (MODIS).





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `Mg` | Mg/ha | 0\* | 503\* | Megagrams of aboveground live woody biomass per Hectare |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


* The national level dataset is freely available for use for
scientific, conservation, and educational purposes.
* Users acknowledge that they themselves are responsible for determining
whether the dataset is of sufficient quality and appropriateness for
their objectives.
* Users agree that they will make reasonable efforts to provide appropriate
feedbacks and notification of any significant errors that they identify
in the dataset.




### Citations



Citations:
* A. Baccini, S J. Goetz, W.S. Walker, N. T. Laporte, M. Sun, D.
Sulla\-Menashe, J. Hackler, P.S.A. Beck, R. Dubayah, M.A. Friedl, S. Samanta
and R. A. Houghton. Estimated carbon dioxide emissions from tropical
deforestation improved by carbon\-density maps. 2012 Nature Climate Change,
[doi:10\.1038/NCLIMATE1354](https://doi.org/10.1038/NCLIMATE1354)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('WHRC/biomass/tropical');
// Show results only over land.
varlandMask=ee.Image('NOAA/NGDC/ETOPO1').select('bedrock').gt(0);
varliveWoodyBiomass=dataset.updateMask(landMask);

varvisParams={
min:0,
max:350,
palette:[
'ffffff','ce7e45','df923d','f1b555','fcd163','99b718','74a901',
'66a000','529400','3e8601','207401','056201','004c00','023b01',
'012e01','011d01','011301'
],
};
Map.addLayer(
liveWoodyBiomass,visParams,'Aboveground Live Woody Biomass (Mg/ha)');

Map.setCenter(-69.4,0.3,3);
Map.setOptions('SATELLITE');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WHRC/WHRC_biomass_tropical)


[WHRC Pantropical National Level Carbon Stock Dataset](/earth-engine/datasets/catalog/WHRC_biomass_tropical)

A national\-level map of above\-ground live woody biomass density for tropical countries at 500m. This dataset was assembled from a combination of co\-located field measurements, LiDAR observations, and imagery recorded from the Moderate Resolution Imaging Spectroradiometer (MODIS).

 WHRC/biomass/tropical,
 aboveground,biomass,carbon,forest\-biomass,geophysical,umd

2012\-01\-29T00:00:00Z/2012\-01\-29T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








