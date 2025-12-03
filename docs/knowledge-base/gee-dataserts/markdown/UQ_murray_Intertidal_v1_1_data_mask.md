



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Murray Global Intertidal Change Data Mask


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================================








Dataset Availability
1984\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[Murray/UQ/Google/USGS/NASA](https://intertidal.app)



Earth Engine Snippet


`ee.Image("UQ/murray/Intertidal/v1_1/data_mask")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UQ/UQ_murray_Intertidal_v1_1_data_mask)





Tags


[coastal](/earth-engine/datasets/tags/coastal)
[google](/earth-engine/datasets/tags/google)
[intertidal](/earth-engine/datasets/tags/intertidal)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[murray](/earth-engine/datasets/tags/murray)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[tidal\-flats](/earth-engine/datasets/tags/tidal-flats)
[uq](/earth-engine/datasets/tags/uq)








#### Description



The Murray Global Intertidal Change Dataset contains global maps of tidal flat
ecosystems produced via a supervised classification of 707,528 Landsat
Archive images. Each pixel was classified into tidal flat, permanent water
or other with reference to a globally distributed set of training data.


The classification was implemented along the entire global coastline
between 60° North and 60° South from 1 January 1984 to 31 December 2016\.
The image collection consists consists of a time\-series of 11 global maps
of tidal flats at 30m pixel resolution for set time\-periods (1984\-1986;
1987\-1989; 1990\-1992; 1993\-1995; 1996\-1998; 1999\-2001; 2002\-2004;
2005\-2007; 2008\-2010; 2011\-2013; 2014\-2016\)


Flag indicating the spatial limits of the implementation of the tidal flat
classifier as defined by altitudinal (\+100m) and bathymetric (\-100m) limits.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `datamask` | occurrence | A flag to indicate data inclusion. |
| Bitmask for datamask * Bit 0: Data mask 	+ 0: No data 	+ 1: Classified area | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Terms of Use


**Terms of Use**


This work is licensed under a Creative Commons Attribution 4\.0
International License.


Any use of the intertidal data must include proper acknowledgement,
including citing the associated journal article.




### Citations



Citations:
* Murray, N.J., Phinn, S.R., DeWitt, M., Ferrari, R., Johnston, R., Lyons, M.B.,
Clinton, N., Thau, D. \& Fuller, R.A. (2019\) The global distribution and
trajectory of tidal flats. Nature, 565, 222\-225\.
[doi:10\.1038/s41586\-018\-0805\-8](https://doi.org/10.1038/s41586-018-0805-8),
* Murray, N. J., Phinn, S. P., Fuller, R. A., DeWitt, M., Ferrari, R.,
Johnston, R., Clinton, N., \& Lyons, M. B. (2022\). High\-resolution global
maps of tidal flat ecosystems from 1984 to 2019\. Scientific Data,
9(1\).
[doi:10\.1038/s41597\-022\-01635\-5](https://doi.org/10.1038/s41597-022-01635-5),





### DOIs


* [https://doi.org/10\.1038/s41586\-018\-0805\-8](https://doi.org/10.1038/s41586-018-0805-8)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('UQ/murray/Intertidal/v1_1/data_mask');

varvisualization={
bands:['datamask'],
min:0,
max:1,
palette:['000000','ffffff']
};

Map.setCenter(126.6339,37.4394,10);

Map.addLayer(dataset,visualization,'Data mask');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/UQ/UQ_murray_Intertidal_v1_1_data_mask)


[Murray Global Intertidal Change Data Mask](/earth-engine/datasets/catalog/UQ_murray_Intertidal_v1_1_data_mask)

The Murray Global Intertidal Change Dataset contains global maps of tidal flat ecosystems produced via a supervised classification of 707,528 Landsat Archive images. Each pixel was classified into tidal flat, permanent water or other with reference to a globally distributed set of training data. The classification was implemented along the …

 UQ/murray/Intertidal/v1\_1/data\_mask,
 coastal,google,intertidal,landsat\-derived,murray,surface\-ground\-water,tidal\-flats,uq

1984\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-60 \-180 60 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1038/s41586\-018\-0805\-8](https://doi.org/https://intertidal.app)
* [https://doi.org/10\.1038/s41586\-018\-0805\-8](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/UQ_murray_Intertidal_v1_1_data_mask)









