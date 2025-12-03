



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MOD16A2: MODIS Global Terrestrial Evapotranspiration 8\-Day Global 1km


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================================================








Dataset Availability
2000\-01\-01T00:00:00Z–2014\-12\-27T00:00:00Z
Dataset Provider


[Numerical Terradynamic Simulation Group, The University of Montana](https://www.ntsg.umt.edu/project/modis/mod16.php)



Earth Engine Snippet


`ee.ImageCollection("MODIS/NTSG/MOD16A2/105")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_NTSG_MOD16A2_105)





Cadence
8 Days
Tags


[8\-day](/earth-engine/datasets/tags/8-day)
[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[global](/earth-engine/datasets/tags/global)
[mod16a2](/earth-engine/datasets/tags/mod16a2)
[modis](/earth-engine/datasets/tags/modis)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)








#### Description



The MOD16A2 V105 product provides information about
8\-day global terrestrial evapotranspiration at 1km pixel resolution.
Evapotranspiration (ET) is the sum of evaporation and plant transpiration
from the Earth's surface to the atmosphere. With long\-term ET
data, the effects of changes in climate, land use, and ecosystems
disturbances can be quantified.


The MOD16A2 product is produced by the Numerical Terradynamic Simulation
Group [NTSG](https://www.ntsg.umt.edu/),
University of Montana (UMT) in conjunction with NASA Earth Observing
System. For more details about the algorithm used see the [algorithm
theoretical basis document](https://scholarworks.umt.edu/cgi/viewcontent.cgi?article=1267&context=ntsg_pubs).


* The period of coverage is 8 days with the exception of
the last period at the end of the year which is either 5 or 6 days.
ET/PET units are 0\.1mm/5\-day for December 27\-31 of 2001, 2002,
2003, 2005, 2006, 2007, 2009, 2010, and 0\.1mm/6\-day for December
26\-31 of 2000, 2004, 2008 (leap years).


\*\* For some pixels in African
rainforest, the MODIS albedo data from MCD43B2/MCD43B3 have no
cloud\-free data throughout an entire year. As a result, pixels
for that year in all data bands are masked out.





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `ET` | kg/m^2 | \-5\* | 453\* | 0\.1 | Evapotranspiration, aggregated for period of coverage. |
| `LE` | J/m^2/day | \-20\* | 1671\* | 10000 | Latent heat flux, averaged daily over the period of coverage. |
| `PET` | kg/m^2 | \-8\* | 793\* | 0\.1 | Potential evapotranspiration, aggregated for period of coverage. |
| `PLE` | J/m^2/day | \-40\* | 3174\* | 10000 | Potential Latent Heat Flux, averaged daily over the period ofcoverage. |
| `ET_QC` | None |  | ET quality control. |
| Bitmask for ET\_QC * Bit 0: MODLAND\_QC bits 	+ 0: Good quality (main algorithm with or without saturation) 	+ 1: Other quality (back\-up algorithm or fill values) * Bit 1: Sensor 	+ 0: Terra 	+ 1: Aqua * Bit 2: Dead detector 	+ 0: Detectors fine for up to 50% of channels 1, 2 	+ 1: Dead detectors caused \>50% adjacent detector retrieval * Bits 3\-4: Cloud state 	+ 0: Significant clouds NOT present (clear) 	+ 1: Significant clouds WERE present 	+ 2: Mixed cloud present on pixel 	+ 3: Cloud state not defined, assumed clear * Bits 5\-7: SCF\_QC (five level confidence score) 	+ 0: Main method used, best result possible (no saturation) 	+ 1: Main method used, good and very usable (with saturation) 	+ 2: Main method failed due to bad geometry, empirical algorithm used 	+ 3: Main method failed due to problems other than geometry, empirical algorithm used 	+ 4: Pixel not produced at all, value couldn't be retrieved | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| days\_of\_coverage | DOUBLE | Number of days covered by each image since the period of coverage for the last asset of the year can be of varying length |




### Terms of Use


**Terms of Use**


All NTSG data distributed through this [site](http://files.ntsg.umt.edu/)
has no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Qiaozhen Mu, Maosheng Zhao, Steven W. Running and Numerical Terradynamic
Simulation Group (2014\): MODIS Global Terrestrial Evapotranspiration
(ET) Product MOD16A2 Collection 5\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/NTSG/MOD16A2/105')
.filter(ee.Filter.date('2014-04-01','2014-06-01'));
varevapotranspiration=dataset.select('ET');
varevapotranspirationVis={
min:0,
max:300,
palette:
['a50000','ff4f1a','f1e342','c7ef1f','05fff3','1707ff','d90bff'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(evapotranspiration,evapotranspirationVis,'Evapotranspiration');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_NTSG_MOD16A2_105)


[MOD16A2: MODIS Global Terrestrial Evapotranspiration 8\-Day Global 1km](/earth-engine/datasets/catalog/MODIS_NTSG_MOD16A2_105)

The MOD16A2 V105 product provides information about 8\-day global terrestrial evapotranspiration at 1km pixel resolution. Evapotranspiration (ET) is the sum of evaporation and plant transpiration from the Earth's surface to the atmosphere. With long\-term ET data, the effects of changes in climate, land use, and ecosystems disturbances can be quantified. …

 MODIS/NTSG/MOD16A2/105,
 8\-day,evapotranspiration,global,mod16a2,modis,water\-vapor

2000\-01\-01T00:00:00Z/2014\-12\-27T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








