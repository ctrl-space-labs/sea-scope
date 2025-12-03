



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Earth Surface Mineral Dust Source Investigation\- Methane Plume Complexes


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================================================================








Dataset Availability
2022\-08\-10T00:00:00Z–2024\-10\-26T17:21:33Z
Dataset Provider


[NASA Jet Propulsion Laboratory](https://earth.jpl.nasa.gov/emit/data/data-products/)



Earth Engine Snippet


`ee.ImageCollection("NASA/EMIT/L2B/CH4PLM")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_EMIT_L2B_CH4PLM)





Cadence
1 Day
Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[daily](/earth-engine/datasets/tags/daily)
[emit](/earth-engine/datasets/tags/emit)
[methane](/earth-engine/datasets/tags/methane)
[nasa](/earth-engine/datasets/tags/nasa)








#### Description



The EMIT Project is part of the Earth Venture\-Instrument (EV\-I) Program
directed by the Program Director of the NASA Earth Science Division (ESD).
EMIT is comprised of a VSWIR Infrared Dyson imaging spectrometer adapted for
installation on the International Space Station (ISS). EMIT measures
radiance between 380 and 2500 nanometers, with an approximate 7 nm bandpass.
Data are collected in a swath that is approximately 75 km wide at the
equator, with an approximate ground sampling distance of 60 m. See the
provider's [NASA EMIT Overview](https://lpdaac.usgs.gov/documents/1695/EMIT_L2B_GHG_User_Guide_V1.pdf)
for more details.


EMIT was a particularly useful tool for mapping out greenhouse gases,
including methane, carbon dioxide, and water vapor. This is consistent with
previous findings from airborne data, but global nature, revisit frequency
and wide swath of EMIT provided an unprecedented opportunity to investigate
greenhouse gas retrievals.


The EMIT Level 2B Estimated Methane Plume Complexes (EMITL2BCH4PLM) Version
1 data product provides estimated methane plume complexes in parts per
million meter (ppm m) along with uncertainty data. The EMITL2BCH4PLM data
product will only be generated where methane plume complexes have been
identified.





### Bands



**Pixel Size**
  
72000 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `methane_plume_complex` | ppm m | Estimated Methane plume complex. |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| global\_plume\_identifier | STRING | Global Plume Identification Number |
| Concentration\_Uncertainty | DOUBLE | Uncertainity in Concentration |
| DAAC\_Scene\_Names | STRING\_LIST | DAAC Scene Names |
| DAAC\_Scene\_Numbers | STRING\_LIST | DAAC Scene Numbers |
| DCID | STRING | Data Collection Identifier |
| Latitude\_of\_max\_concentration | DOUBLE | Latitute with maximum concentration |
| Longitude\_of\_max\_concentration | DOUBLE | Longitude with maximum concentration |
| Max\_Plume\_Concentration | DOUBLE | Maximum Plume Concentration |
| Orbit | STRING | Unique orbit number |
| Plume\_ID | STRING | Unique Plume Identification number |
| Scene\_FIDs | STRING\_LIST | Scene FIDs |




### Terms of Use


**Terms of Use**


NASA EMIT data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Green, R., Thorpe, A., Brodrick, P., Chadwick, D., Elder, C.,
Villanueva\-Weeks, C., Fahlen, J., Coleman, R., Jensen, D., Olsen\-Duvall, W.,
Lundeen, S., Lopez, A., Thompson, D. (2023\). EMIT L2B Estimated Methane
Plume Complexes 60 m V001 \[Data set]. NASA EOSDIS Land Processes Distributed
Active Archive Center. Accessed 2024\-03\-06 from
[https://doi.org/10\.5067/EMIT/EMITL2BCH4PLM.001](https://doi.org/10.5067/EMIT/EMITL2BCH4PLM.001)





### DOIs


* [https://doi.org/10\.5067/EMIT/EMITL2BCH4PLM.001](https://doi.org/10.5067/EMIT/EMITL2BCH4PLM.001)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/EMIT/L2B/CH4PLM');
varemitEnhancement=dataset.select('methane_plume_complex');
varemitEnhancementVis={
min:0,
max:100.0,
palette:['d7191c','fdae61','ffffbf','abd9e9','2c7bb6'],
};
Map.setCenter(53.99,39.11,8);
Map.addLayer(
emitEnhancement,emitEnhancementVis,
'Emit Enhancement');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_EMIT_L2B_CH4PLM)


[Earth Surface Mineral Dust Source Investigation\- Methane Plume Complexes](/earth-engine/datasets/catalog/NASA_EMIT_L2B_CH4PLM)

The EMIT Project is part of the Earth Venture\-Instrument (EV\-I) Program directed by the Program Director of the NASA Earth Science Division (ESD). EMIT is comprised of a VSWIR Infrared Dyson imaging spectrometer adapted for installation on the International Space Station (ISS). EMIT measures radiance between 380 and 2500 nanometers, …

 NASA/EMIT/L2B/CH4PLM,
 atmosphere,daily,emit,methane,nasa

2022\-08\-10T00:00:00Z/2024\-10\-26T17:21:33Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/EMIT/EMITL2BCH4PLM.001](https://doi.org/https://earth.jpl.nasa.gov/emit/data/data-products/)
* [https://doi.org/10\.5067/EMIT/EMITL2BCH4PLM.001](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_EMIT_L2B_CH4PLM)









