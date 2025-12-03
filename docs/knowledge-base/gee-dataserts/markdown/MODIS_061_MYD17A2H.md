



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MYD17A2H.061: Aqua Gross Primary Productivity 8\-Day Global 500m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================================








Dataset Availability
2021\-01\-01T00:00:00Z–2025\-07\-04T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/MODIS/MYD17A2H.061)



Earth Engine Snippet


`ee.ImageCollection("MODIS/061/MYD17A2H")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD17A2H)





Cadence
8 Days
Tags


[8\-day](/earth-engine/datasets/tags/8-day)
[aqua](/earth-engine/datasets/tags/aqua)
[global](/earth-engine/datasets/tags/global)
[gpp](/earth-engine/datasets/tags/gpp)
[modis](/earth-engine/datasets/tags/modis)
[nasa](/earth-engine/datasets/tags/nasa)
[photosynthesis](/earth-engine/datasets/tags/photosynthesis)
[plant\-productivity](/earth-engine/datasets/tags/plant-productivity)
[productivity](/earth-engine/datasets/tags/productivity)
[psn](/earth-engine/datasets/tags/psn)
[usgs](/earth-engine/datasets/tags/usgs)
myd17a2








#### Description



The MYD17A2H V6\.1 Gross Primary Productivity (GPP) product
is a cumulative 8\-day composite with a 500m resolution. The product
is based on the radiation\-use efficiency concept and can be potentially
used as inputs to data models to calculate terrestrial energy,
carbon, water cycle processes, and biogeochemistry of vegetation.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/972/MOD17_User_Guide_V61.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/95/MOD17_ATBD.pdf)
* [General Documentation](https://ladsweb.modaps.eosdis.nasa.gov/filespec/MODIS/6/MYD17A2H)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Units | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- | --- |
| `Gpp` | kg\*C/m^2 | 0 | 3000 | 0\.0001 | Gross primary production |
| `PsnNet` | kg\*C/m^2 | \-3000 | 3000 | 0\.0001 | Net photosynthesis; GPP minus the maintenance respiration (MR) |
| `Psn_QC` | None |  | Quality control bits |
| Bitmask for Psn\_QC * Bit 0: MODLAND QC bits 	+ 0: Good quality 	+ 1: Other quality * Bit 1: Sensor 	+ 0: Terra 	+ 1: Aqua * Bit 2: Dead detector 	+ 0: Detectors apparently fine for up to 50% of channels 1, 2 	+ 1: Dead detectors caused \>50% adjacent detector retrieval * Bits 3\-4: Cloud state 	+ 0: Significant clouds NOT present (clear) 	+ 1: Significant clouds WERE present 	+ 2: Mixed cloud present on pixel 	+ 3: Cloud state not defined, assumed clear * Bits 5\-7: 5\-level confidence quality score 	+ 0: Very best possible 	+ 1: Good, very usable, but not the best 	+ 2: Substandard due to geometry problems \- use with caution 	+ 3: Substandard due to other than geometry problems \- use with caution 	+ 4: Couldn't retrieve pixel (NOT PRODUCED AT ALL \- non\-terrestrial biome) 	+ 7: Fill Value | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


MODIS data and products acquired through the LP DAAC
have no restrictions on subsequent use, sale, or redistribution.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/MODIS/MYD17A2H.061](https://doi.org/10.5067/MODIS/MYD17A2H.061)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('MODIS/061/MYD17A2H')
.filter(ee.Filter.date('2021-01-01','2021-05-01'));
vargpp=dataset.select('Gpp');
vargppVis={
min:0.0,
max:600.0,
palette:['bbe029','0a9501','074b03'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(gpp,gppVis,'GPP');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MODIS/MODIS_061_MYD17A2H)


[MYD17A2H.061: Aqua Gross Primary Productivity 8\-Day Global 500m](/earth-engine/datasets/catalog/MODIS_061_MYD17A2H)

The MYD17A2H V6\.1 Gross Primary Productivity (GPP) product is a cumulative 8\-day composite with a 500m resolution. The product is based on the radiation\-use efficiency concept and can be potentially used as inputs to data models to calculate terrestrial energy, carbon, water cycle processes, and biogeochemistry of vegetation. Documentation: User's …

 MODIS/061/MYD17A2H,
 8\-day,aqua,global,gpp,modis,nasa,photosynthesis,plant\-productivity,productivity,psn,usgs

2021\-01\-01T00:00:00Z/2025\-07\-04T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/MODIS/MYD17A2H.061](https://doi.org/https://doi.org/10.5067/MODIS/MYD17A2H.061)
* [https://doi.org/10\.5067/MODIS/MYD17A2H.061](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MYD17A2H)









