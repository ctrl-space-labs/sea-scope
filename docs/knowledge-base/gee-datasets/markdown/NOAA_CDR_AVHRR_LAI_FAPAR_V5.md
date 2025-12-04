



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NOAA CDR AVHRR LAI FAPAR: Leaf Area Index and Fraction of Absorbed Photosynthetically Active Radiation, Version 5


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================================================================================








Dataset Availability
1981\-06\-24T00:00:00Z–2013\-12\-31T00:00:00Z
Dataset Provider


[NOAA](https://www.ncei.noaa.gov/products/climate-data-records/leaf-area-index-and-fapar)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CDR/AVHRR/LAI_FAPAR/V5")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_AVHRR_LAI_FAPAR_V5)





Cadence
1 Day
Tags


[avhrr](/earth-engine/datasets/tags/avhrr)
[cdr](/earth-engine/datasets/tags/cdr)
[daily](/earth-engine/datasets/tags/daily)
[fapar](/earth-engine/datasets/tags/fapar)
[lai](/earth-engine/datasets/tags/lai)
[land](/earth-engine/datasets/tags/land)
[noaa](/earth-engine/datasets/tags/noaa)
[plant\-productivity](/earth-engine/datasets/tags/plant-productivity)








#### Description



The NOAA Climate Data Record (CDR) of AVHRR Leaf Area Index (LAI) and
Fraction of Absorbed Photosynthetically Active Radiation (FAPAR) dataset
contains derived values that characterize the canopy and photosynthetic
activity of plants. This dataset is derived from the NOAA AVHRR Surface
Reflectance product and is gridded at a resolution of 0\.05° on a daily
basis. The values are computed globally over land surfaces, but not over
bare or very sparsely vegetated areas, permanent ice or snow, permanent
wetland, urban areas, or water bodies.


Known issues with this dataset include:


* TIMEOFDAY variable contains values that are too large by 1 day
* Latitude values are not correctly associated with the center of
the grid cell, error is \< 0\.002 degrees
* Longitude values are not correctly associated with the center of
the grid cell, error is \< 0\.02 degrees


See [technical note from the data provider](https://www.ncei.noaa.gov/pub/data/sds/cdr/CDRs/Leaf_Area_Index_and_FAPAR/AVHRR/AlgorithmDescriptionAVHRR_01B-20c.pdf).


Provider's note: the orbital drift of N\-19 (the last NOAA satellite
carrying the AVHRR sensor) began to severely degrade the retrieved
product quality. Therefore, VIIRS is now the primary sensor being used for
these products from 2014\-present.





### Bands



**Pixel Size**
  
5566 meters



**Bands**




| Name | Min | Max | Scale | Description |
| --- | --- | --- | --- | --- |
| `LAI` | 0\* | 6205\* | 0\.001 | Leaf area index |
| `FAPAR` | 0\* | 896\* | 0\.001 | Fraction of absorbed photosynthetic active radiation |
| `QA` |  | Quality control bit flags |
| Bitmask for QA * Bits 0\-1: Quality control 	+ 0: Ok 	+ 1: Input flags as cloudy 	+ 2: Invalid input 	+ 3: Output out of range * Bits 2\-4: Associated class 	+ 1: Needleleaf forest 	+ 2: Broadleaf forest 	+ 4: Grassland \& croplands \& non vegetated 	+ 5: Evergreen broadleaf forest 	+ 6: Water * Bit 5: BRDF corrected 	+ 0: No 	+ 1: Yes * Bits 6\-7: Polygon test 	+ 0: In polygon 	+ 1: Not in polygon 	+ 2: Not tested (water/cloudy) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| status | STRING | 'provisional' or 'permanent' |




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
* Martin Claverie, Eric Vermote, and NOAA CDR Program (2014\): NOAA Climate
Data Record (CDR) of Leaf Area Index (LAI) and Fraction of Absorbed
Photosynthetically Active Radiation (FAPAR), Version 4\. \[indicate subset
used]. NOAA National Climatic Data Center.
[doi:10\.7289/V5M043BX](https://data.nodc.noaa.gov/cgi-bin/iso?id=gov.noaa.ncdc:C00898)





### DOIs


* [https://doi.org/10\.7289/V5M043BX](https://doi.org/10.7289/V5M043BX)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CDR/AVHRR/LAI_FAPAR/V5')
.filter(ee.Filter.date('2018-02-01','2018-03-01'));
varleafAreaIndex=dataset.select('LAI');
varleafAreaIndexVis={
min:0.0,
max:4000.0,
palette:['3b0200','977705','ca9f06','ffca09','006a03','003b02'],
};
Map.setCenter(20,24.5,2);
Map.addLayer(leafAreaIndex,leafAreaIndexVis,'Leaf Area Index');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_AVHRR_LAI_FAPAR_V5)


[NOAA CDR AVHRR LAI FAPAR: Leaf Area Index and Fraction of Absorbed Photosynthetically Active Radiation, Version 5](/earth-engine/datasets/catalog/NOAA_CDR_AVHRR_LAI_FAPAR_V5)

The NOAA Climate Data Record (CDR) of AVHRR Leaf Area Index (LAI) and Fraction of Absorbed Photosynthetically Active Radiation (FAPAR) dataset contains derived values that characterize the canopy and photosynthetic activity of plants. This dataset is derived from the NOAA AVHRR Surface Reflectance product and is gridded at a resolution …

 NOAA/CDR/AVHRR/LAI\_FAPAR/V5,
 avhrr,cdr,daily,fapar,lai,land,noaa,plant\-productivity

1981\-06\-24T00:00:00Z/2013\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7289/V5M043BX](https://doi.org/https://www.ncei.noaa.gov/products/climate-data-records/leaf-area-index-and-fapar)
* [https://doi.org/10\.7289/V5M043BX](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_AVHRR_LAI_FAPAR_V5)









