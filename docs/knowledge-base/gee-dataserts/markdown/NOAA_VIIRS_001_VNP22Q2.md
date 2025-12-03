



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

VNP22Q2: Land Surface Phenology Yearly L3 Global 500m SIN Grid


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================================








Dataset Availability
2013\-01\-01T00:00:00Z–2022\-01\-01T00:00:00Z
Dataset Provider


[NASA LP DAAC at the USGS EROS Center](https://doi.org/10.5067/VIIRS/VNP22Q2.001)



Earth Engine Snippet


`ee.ImageCollection("NOAA/VIIRS/001/VNP22Q2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_VIIRS_001_VNP22Q2)





Cadence
8 Days
Tags


[land](/earth-engine/datasets/tags/land)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[nasa](/earth-engine/datasets/tags/nasa)
[ndvi](/earth-engine/datasets/tags/ndvi)
[noaa](/earth-engine/datasets/tags/noaa)
[npp](/earth-engine/datasets/tags/npp)
[onset\-greenness](/earth-engine/datasets/tags/onset-greenness)
[phenology](/earth-engine/datasets/tags/phenology)
[surface](/earth-engine/datasets/tags/surface)
[vegetation](/earth-engine/datasets/tags/vegetation)
[viirs](/earth-engine/datasets/tags/viirs)








#### Description



The Suomi National Polar\-Orbiting Partnership (Suomi NPP) NASA Visible
Infrared Imaging Radiometer Suite (VIIRS) Land Cover Dynamics data product
provides global land surface phenology (GLSP) metrics at yearly intervals.
The VNP22Q2 data product is derived from time series of the two\-band
Enhanced Vegetation Index (EVI2\) calculated from VIIRS Nadir Bidirectional
Reflectance Distribution Function (BRDF)\-Adjusted Reflectance (NBAR).
Vegetation phenology metrics at 500 meter spatial resolution are identified
for up to two detected growing cycles per year.


The product contains six phenological transition dates: onset of greenness
increase, onset of greenness maximum, onset of greenness decrease, onset of
greenness minimum, dates of mid\-greenup, and senescence phases. The product
also includes the growing season length. The greenness\-related metrics
consist of EVI2 onset of greenness increase, EVI2 onset of greenness
maximum, EVI2 growing season, rate of greenness increase, and rate of
greenness decrease. The confidence of phenology detection is provided as
greenness agreement growing season, proportion of good quality (PGQ)
growing season, PGQ onset greenness increase, PGQ onset greenness maximum,
PGQ onset greenness decrease, and PGQ onset greenness minimum.
The final layer is quality control specifying the overall quality of the
product.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/637/VNP22_User_Guide_V1.pdf)
* [Algorithm Theoretical Basis Document (ATBD)](https://lpdaac.usgs.gov/documents/637/VNP22_User_Guide_V1.pdf)
* [General Documentation](https://lpdaac.usgs.gov/products/vnp22q2v001/)
* [Land Product Quality Assessment website](https://landweb.modaps.eosdis.nasa.gov/browse?sensor=VIIRS&sat=SNPP)





### Bands



**Pixel Size**
  
500 meters



**Bands**




| Name | Description |
| --- | --- |
| `Date_Mid_Greenup_Phase_1` | Date at a mid\-greenup phase |
| `Date_Mid_Senescence_Phase_1` | Date at a mid\-senescence phase |
| `EVI2_Growing_Season_Area_1` | Integrated EVI2 during a growing season |
| `EVI2_Onset_Greenness_Increase_1` | EVI2 value at greenup onset |
| `EVI2_Onset_Greenness_Maximum_1` | EVI2 value at maturity onset |
| `GLSP_QC_1` | Global Land Surface Phenology Quality Control |
| Bitmask for GLSP\_QC\_1 * Bits 0\-2: Mandatory Quality 	+ 0: processed, good quality 	+ 1: processed, other quality 	+ 2: processed, backup algorithm 	+ 3: not processed, bad quality 	+ 4: not processed, other * Bits 3\-4: TBD * Bits 5\-7: Land/Water mask 	+ 0: Shallow ocean 	+ 1: Land (Nothing else but land) 	+ 2: Ocean coastlines and lake shorelines 	+ 3: Shallow inland water 	+ 4: Ephemeral water 	+ 5: Deep inland water 	+ 6: Moderate or continental ocean 	+ 7: Deep ocean | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `Greenness_Agreement_Growing_Season_1` | EVI2 agreement between modeled values and raw observations |
| `Growing_Season_Length_1` | Growing Season Length |
| `Onset_Greenness_Decrease_1` | Date at which canopy greenness begins to decrease |
| `Onset_Greenness_Increase_1` | Date of onset of greenness increase |
| `Onset_Greenness_Maximum_1` | Date at which canopy greenness approaches its seasonal maximum |
| `Onset_Greenness_Minimum_1` | Date at which canopy greenness reaches a minimum |
| `PGQ_Growing_Season_1` | Proportion of good quality of VIIRS observations during a vegetation growing season |
| `PGQ_Onset_Greenness_Decrease_1` | Proportion of good quality around senescence onset |
| `PGQ_Onset_Greenness_Increase_1` | Proportion of good quality around greenup onset |
| `PGQ_Onset_Greenness_Maximum_1` | Proportion of good quality around maturity onset |
| `PGQ_Onset_Greenness_Minimum_1` | Proportion of good quality around dormancy onset |
| `Rate_Greenness_Decrease_1` | Rates of change in EVI2 values during a senescence phase |
| `Rate_Greenness_Increase_1` | Rates of change in EVI2 values during a greenup phase |
| `Date_Mid_Greenup_Phase_2` | Date at a mid\-greenup phase |
| `Date_Mid_Senescence_Phase_2` | Date at a mid\-senescence phase |
| `EVI2_Growing_Season_Area_2` | Integrated EVI2 during a growing season |
| `EVI2_Onset_Greenness_Increase_2` | EVI2 value at greenup onset |
| `EVI2_Onset_Greenness_Maximum_2` | EVI2 value at maturity onset |
| `GLSP_QC_2` | Global Land Surface Phenology Quality Control |
| Bitmask for GLSP\_QC\_2 * Bits 0\-2: Mandatory Quality 	+ 0: processed, good quality 	+ 1: processed, other quality 	+ 2: processed, backup algorithm 	+ 3: not processed, bad quality 	+ 4: not processed, other * Bits 3\-4: TBD * Bits 5\-7: Land/Water mask 	+ 0: Shallow ocean 	+ 1: Land (Nothing else but land) 	+ 2: Ocean coastlines and lake shorelines 	+ 3: Shallow inland water 	+ 4: Ephemeral water 	+ 5: Deep inland water 	+ 6: Moderate or continental ocean 	+ 7: Deep ocean | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| `Greenness_Agreement_Growing_Season_2` | EVI2 agreement between modeled values and raw observations |
| `Growing_Season_Length_2` | Growing Season Length |
| `Onset_Greenness_Decrease_2` | Date at which canopy greenness begins to decrease |
| `Onset_Greenness_Increase_2` | Date of onset of greenness increase |
| `Onset_Greenness_Maximum_2` | Date at which canopy greenness approaches its seasonal maximum |
| `Onset_Greenness_Minimum_2` | Date at which canopy greenness reaches a minimum |
| `PGQ_Growing_Season_2` | Proportion of good quality of VIIRS observations during a vegetation growing season |
| `PGQ_Onset_Greenness_Decrease_2` | Proportion of good quality around senescence onset |
| `PGQ_Onset_Greenness_Increase_2` | Proportion of good quality around greenup onset |
| `PGQ_Onset_Greenness_Maximum_2` | Proportion of good quality around maturity onset |
| `PGQ_Onset_Greenness_Minimum_2` | Proportion of good quality around dormancy onset |
| `Rate_Greenness_Decrease_2` | Rates of change in EVI2 values during a senescence phase |
| `Rate_Greenness_Increase_2` | Rates of change in EVI2 values during a greenup phase |




### Terms of Use


**Terms of Use**


LP DAAC NASA data are freely accessible; however, when an author
publishes these data or works based on the data, it is requested that the
author cite the datasets within the text of the publication and include a
reference to them in the reference list.




### Citations



Citations:
* Please visit [LP DAAC 'Citing Our Data' page](https://lpdaac.usgs.gov/citing_our_data)
for information on citing LP DAAC datasets.





### DOIs


* [https://doi.org/10\.5067/VIIRS/VNP22Q2\.001](https://doi.org/10.5067/VIIRS/VNP22Q2.001)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/VIIRS/001/VNP22Q2')
.filter(ee.Filter.date('2017-01-01','2017-12-31'));
varrgb=dataset.select([
'EVI2_Growing_Season_Area_1',
'PGQ_Growing_Season_1',
'Greenness_Agreement_Growing_Season_1']);
varrgbVis={
min:[0,0,0],
max:[75,150,200],
};
Map.setCenter(17.93,7.71,4);
Map.addLayer(rgb,rgbVis,'False color');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_VIIRS_001_VNP22Q2)


[VNP22Q2: Land Surface Phenology Yearly L3 Global 500m SIN Grid](/earth-engine/datasets/catalog/NOAA_VIIRS_001_VNP22Q2)

The Suomi National Polar\-Orbiting Partnership (Suomi NPP) NASA Visible Infrared Imaging Radiometer Suite (VIIRS) Land Cover Dynamics data product provides global land surface phenology (GLSP) metrics at yearly intervals. The VNP22Q2 data product is derived from time series of the two\-band Enhanced Vegetation Index (EVI2\) calculated from VIIRS Nadir Bidirectional …

 NOAA/VIIRS/001/VNP22Q2,
 land,landuse\-landcover,nasa,ndvi,noaa,npp,onset\-greenness,phenology,surface,vegetation,viirs

2013\-01\-01T00:00:00Z/2022\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5067/VIIRS/VNP22Q2\.001](https://doi.org/https://doi.org/10.5067/VIIRS/VNP22Q2.001)
* [https://doi.org/10\.5067/VIIRS/VNP22Q2\.001](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_VIIRS_001_VNP22Q2)









