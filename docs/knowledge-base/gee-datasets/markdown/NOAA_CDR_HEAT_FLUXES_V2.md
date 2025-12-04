



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NOAA CDR: Ocean Heat Fluxes, Version 2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================








Dataset Availability
1988\-01\-01T00:00:00Z–2021\-08\-31T00:00:00Z
Dataset Provider


[NOAA](https://www.ncdc.noaa.gov/cdr/atmospheric/ocean-heat-fluxes)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CDR/HEAT_FLUXES/V2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_HEAT_FLUXES_V2)





Cadence
3 Hours
Tags


[atmospheric](/earth-engine/datasets/tags/atmospheric)
[cdr](/earth-engine/datasets/tags/cdr)
[flux](/earth-engine/datasets/tags/flux)
[heat](/earth-engine/datasets/tags/heat)
[hourly](/earth-engine/datasets/tags/hourly)
[noaa](/earth-engine/datasets/tags/noaa)
[ocean](/earth-engine/datasets/tags/ocean)
[oceans](/earth-engine/datasets/tags/oceans)
[osb](/earth-engine/datasets/tags/osb)








#### Description



The Ocean Heat Fluxes dataset is part of the NOAA Ocean Surface Bundle (OSB)
and provides a high quality Climate Data Record (CDR) of the air/ocean heat
fluxes over ice\-free oceans.


This dataset is calculated from the OSB CDR parameters of near\-surface
atmospheric and sea surface temperature using a neural\-network
emulator of the TOGA\-COARE Bulk Air\-Sea Flux Algorithm.





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `surface_upward_latent_heat_flux` | W/m^2 | \-50\* | 500\* | Flux of heat from the Earth's surface to the atmosphere which causes a change in phase of matter, e.g. evaporation of water at the surface and subsequent condensation of water vapor in the troposphere |
| `surface_upward_sensible_heat_flux` | W/m^2 | \-299\.99\* | 1499\.93\* | Flux of heat from the Earth's surface to the atmosphere which causes a change in air temperature, primarily through conduction and convection |
| `fill_missing_qc` | None | Quality control flags |
| Bitmask for fill\_missing\_qc * Bits 0\-2: Quality control flags 	+ 0: Pixel values from neural network 	+ 1: Unused flag 	+ 2: Snow/ice 	+ 3: Over land 	+ 4: Over lake 	+ 5: High winds; wind speed greater than 45 m/s is clamped to 45 m/s 	+ 6: Failed interpolation, fluxes unresolved | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


The NOAA CDR Program's official distribution point for CDRs is NOAA's
National Climatic Data Center which provides sustained, open access and
active data management of the CDR packages and related information in
keeping with the United States' open data policies and practices as
described in the President's Memorandum on "Open Data Policy" and pursuant
to the Executive Order of May 9, 2013, "Making Open and Machine Readable
the New Default for Government Information". In line with these policies,
the CDR data sets are nonproprietary, publicly available, and no
restrictions are placed upon their use. For more information, see the
[Fair Use of NOAA's CDR Data Sets, Algorithms and Documentation](https://www1.ncdc.noaa.gov/pub/data/sds/cdr/CDRs/Aerosol_Optical_Thickness/UseAgreement_01B-04.pdf)
pdf.




### Citations



Citations:
* Clayson, Carol Anne, Brown, Jeremiah, and NOAA CDR Program (2016\). NOAA
Climate Data Record Ocean Surface Bundle (OSB) Climate Data Record (CDR) of
Ocean Heat Fluxes, Version 2\. \[indicate subset used]. NOAA National Climatic
Data Center. [doi:10\.7289/V59K4885](https://doi.org/10.7289/V59K4885).





### DOIs


* [https://doi.org/10\.7289/V59K4885](https://doi.org/10.7289/V59K4885)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CDR/HEAT_FLUXES/V2')
.filter(ee.Filter.date('2017-05-01','2017-05-14'));
varheatFluxVis={
min:-50.0,
max:500.0,
bands:[
'surface_upward_sensible_heat_flux',
'surface_upward_sensible_heat_flux',
'surface_upward_latent_heat_flux',
]
};
Map.setCenter(28.61,-18.98,2);
Map.addLayer(dataset,heatFluxVis,'Heat Flux');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_HEAT_FLUXES_V2)


[NOAA CDR: Ocean Heat Fluxes, Version 2](/earth-engine/datasets/catalog/NOAA_CDR_HEAT_FLUXES_V2)

The Ocean Heat Fluxes dataset is part of the NOAA Ocean Surface Bundle (OSB) and provides a high quality Climate Data Record (CDR) of the air/ocean heat fluxes over ice\-free oceans. This dataset is calculated from the OSB CDR parameters of near\-surface atmospheric and sea surface temperature using a neural\-network …

 NOAA/CDR/HEAT\_FLUXES/V2,
 atmospheric,cdr,flux,heat,hourly,noaa,ocean,oceans,osb

1988\-01\-01T00:00:00Z/2021\-08\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7289/V59K4885](https://doi.org/https://www.ncdc.noaa.gov/cdr/atmospheric/ocean-heat-fluxes)
* [https://doi.org/10\.7289/V59K4885](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_HEAT_FLUXES_V2)









