



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NOAA CDR WHOI: Sea Surface Temperature, Version 2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================








Dataset Availability
1988\-01\-01T00:00:00Z–2021\-08\-31T00:00:00Z
Dataset Provider


[NOAA](https://www.ncdc.noaa.gov/cdr/oceanic/sea-surface-temperature-whoi)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CDR/SST_WHOI/V2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_SST_WHOI_V2)





Cadence
3 Hours
Tags


[atmospheric](/earth-engine/datasets/tags/atmospheric)
[cdr](/earth-engine/datasets/tags/cdr)
[hourly](/earth-engine/datasets/tags/hourly)
[noaa](/earth-engine/datasets/tags/noaa)
[ocean](/earth-engine/datasets/tags/ocean)
[oceans](/earth-engine/datasets/tags/oceans)
[oisst](/earth-engine/datasets/tags/oisst)
[osb](/earth-engine/datasets/tags/osb)
[sst](/earth-engine/datasets/tags/sst)
whoi








#### Description



The Sea Surface Temperature \- WHOI dataset is part of the NOAA Ocean Surface
Bundle (OSB) and provides a high quality Climate Data Record (CDR) of sea
surface temperature over ice\-free oceans.


The SST values are found through modeling the diurnal variability in
combination with AVHRR observations of sea surface temperature.





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `sea_surface_temperature` | °C | \-1\.79\* | 35\* | Optimum Interpolation Sea Surface Temperature (OISST), with a diurnal warming correction |
| `fill_missing_qc` | None | Quality control flags |
| Bitmask for fill\_missing\_qc * Bits 0\-2: Quality control flags 	+ 0: Pixel values from neural network 	+ 1: Unused flag 	+ 2: Snow/ice 	+ 3: Over land 	+ 4: Over lake 	+ 5: SST missing, SST unresolved | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


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
Sea Surface Temperature \- WHOI, Version 2\. \[indicate subset used]. NOAA
National Climatic Data Center. [doi:10\.7289/V5FB510W](https://doi.org/10.7289/V5FB510W).





### DOIs


* [https://doi.org/10\.7289/V5FB510W](https://doi.org/10.7289/V5FB510W)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CDR/SST_WHOI/V2')
.filter(ee.Filter.date('2018-03-01','2018-03-14'));
varseaSurfaceTemperature=dataset.select('sea_surface_temperature');
varvisParams={
min:0.0,
max:30.0,
palette:[
'040274','040281','0502a3','0502b8','0502ce','0502e6',
'0602ff','235cb1','307ef3','269db1','30c8e2','32d3ef',
'3be285','3ff38f','86e26f','3ae237','b5e22e','d6e21f',
'fff705','ffd611','ffb613','ff8b13','ff6e08','ff500d',
'ff0000','de0101','c21301','a71001','911003'
],
};
Map.setCenter(-4.92,-21.09,2);
Map.addLayer(seaSurfaceTemperature,visParams,'Sea Surface Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_SST_WHOI_V2)


[NOAA CDR WHOI: Sea Surface Temperature, Version 2](/earth-engine/datasets/catalog/NOAA_CDR_SST_WHOI_V2)

The Sea Surface Temperature \- WHOI dataset is part of the NOAA Ocean Surface Bundle (OSB) and provides a high quality Climate Data Record (CDR) of sea surface temperature over ice\-free oceans. The SST values are found through modeling the diurnal variability in combination with AVHRR observations of sea surface …

 NOAA/CDR/SST\_WHOI/V2,
 atmospheric,cdr,hourly,noaa,ocean,oceans,oisst,osb,sst

1988\-01\-01T00:00:00Z/2021\-08\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7289/V5FB510W](https://doi.org/https://www.ncdc.noaa.gov/cdr/oceanic/sea-surface-temperature-whoi)
* [https://doi.org/10\.7289/V5FB510W](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_SST_WHOI_V2)









