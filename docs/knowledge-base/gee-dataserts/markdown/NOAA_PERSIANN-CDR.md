



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

PERSIANN\-CDR: Precipitation Estimation From Remotely Sensed Information Using Artificial Neural Networks\-Climate Data Record


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================================================================================================








Dataset Availability
1983\-01\-01T00:00:00Z–2024\-09\-30T00:00:00Z
Dataset Provider


[NOAA NCDC](https://doi.org/10.7289/V51V5BWQ)



Earth Engine Snippet


`ee.ImageCollection("NOAA/PERSIANN-CDR")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_PERSIANN-CDR)





Cadence
1 Day
Tags


[cdr](/earth-engine/datasets/tags/cdr)
[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[noaa](/earth-engine/datasets/tags/noaa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[weather](/earth-engine/datasets/tags/weather)
ncdc
persiann








#### Description



PERSIANN\-CDR is a daily quasi\-global precipitation product
that spans the period from 1983\-01\-01 to present. The data is
produced quarterly, with a typical lag of three months. The product
is developed by the Center for Hydrometeorology and Remote Sensing
at the University of California, Irvine (UC\-IRVINE/CHRS) using
Gridded Satellite (GridSat\-B1\) IR data that are derived from merging
ISCCP B1 IR data, along with GPCP version 2\.2\.





### Bands



**Pixel Size**
  
27830 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `precipitation` | mm | 0\* | 718\.62\* | Estimated daily precipitation |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


CDR data sets are nonproprietary, publicly available,
and no restrictions are placed upon their use. For additional information,
see the [Fair Use of NOAA's CDR Data Sets, Algorithms and Documentation](https://www.ncdc.noaa.gov/sites/default/files/cdr-documentation/UseAgreement_0.pdf)
document.




### Citations



Citations:
* Cite this dataset when used as a source: Sorooshian, Soroosh;
Hsu, Kuolin; Braithwaite, Dan; Ashouri, Hamed; and NOAA CDR Program
(2014\): NOAA Climate Data Record (CDR) of Precipitation Estimation
from Remotely Sensed Information using Artificial Neural Networks
(PERSIANN\-CDR), Version 1 Revision 1\. \[indicate subset used]. NOAA
National Centers for Environmental Information. doi:
[doi:10\.7289/V51V5BWQ](https://doi.org/10.7289/V51V5BWQ)
\[access date].
* Publications using this dataset should also cite the following
journal article: Ashouri H., K. Hsu, S. Sorooshian, D. K. Braithwaite,
K. R. Knapp, L. D. Cecil, B. R. Nelson, and O. P. Prat, 2015: PERSIANN\-CDR:
Daily Precipitation Climate Data Record from Multi\-Satellite Observations
for Hydrological and Climate Studies. Bull. Amer. Meteor. Soc.,
[doi:10\.1175/BAMS\-D\-13\-00068\.1](https://doi.org/10.1175/BAMS-D-13-00068.1).





### DOIs


* [https://doi.org/10\.1175/BAMS\-D\-13\-00068\.1](https://doi.org/10.1175/BAMS-D-13-00068.1)
* [https://doi.org/10\.7289/V51V5BWQ](https://doi.org/10.7289/V51V5BWQ)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/PERSIANN-CDR')
.filter(ee.Filter.date('2017-05-01','2017-05-02'));
varprecipitation=dataset.select('precipitation');
varprecipitationVis={
min:0.0,
max:50.0,
palette:['3907ff','03fff3','28ff25','fbff09','ff1105'],
};
Map.setCenter(113.03,3.34,3);
Map.addLayer(precipitation,precipitationVis,'Precipitation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_PERSIANN-CDR)


[PERSIANN\-CDR: Precipitation Estimation From Remotely Sensed Information Using Artificial Neural Networks\-Climate Data Record](/earth-engine/datasets/catalog/NOAA_PERSIANN-CDR)

PERSIANN\-CDR is a daily quasi\-global precipitation product that spans the period from 1983\-01\-01 to present. The data is produced quarterly, with a typical lag of three months. The product is developed by the Center for Hydrometeorology and Remote Sensing at the University of California, Irvine (UC\-IRVINE/CHRS) using Gridded Satellite (GridSat\-B1\) …

 NOAA/PERSIANN\-CDR,
 cdr,climate,geophysical,noaa,precipitation,weather

1983\-01\-01T00:00:00Z/2024\-09\-30T00:00:00Z



 \-60 \-180 60 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7289/V51V5BWQ](https://doi.org/https://doi.org/10.7289/V51V5BWQ)
* [https://doi.org/10\.7289/V51V5BWQ](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_PERSIANN-CDR)









