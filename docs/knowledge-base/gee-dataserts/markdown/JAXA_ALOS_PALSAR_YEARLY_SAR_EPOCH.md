



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global PALSAR\-2/PALSAR Yearly Mosaic, version 2


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================








Dataset Availability
2015\-01\-01T00:00:00Z–2023\-01\-01T00:00:00Z
Dataset Provider


[JAXA EORC](https://www.eorc.jaxa.jp/ALOS/en/dataset/fnf_e.htm)



Earth Engine Snippet


`ee.ImageCollection("JAXA/ALOS/PALSAR/YEARLY/SAR_EPOCH")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_ALOS_PALSAR_YEARLY_SAR_EPOCH)





Tags


[alos](/earth-engine/datasets/tags/alos)
[alos2](/earth-engine/datasets/tags/alos2)
[eroc](/earth-engine/datasets/tags/eroc)
[jaxa](/earth-engine/datasets/tags/jaxa)
[palsar](/earth-engine/datasets/tags/palsar)
[palsar2](/earth-engine/datasets/tags/palsar2)
[sar](/earth-engine/datasets/tags/sar)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)








#### Description



The global 25m PALSAR/PALSAR\-2 mosaic is a seamless global
SAR image created by mosaicking strips of SAR imagery
from PALSAR/PALSAR\-2\. For each year and location,
the strip data were selected through visual inspection of the
browse mosaics available over the period, with those showing minimum
response to surface moisture preferentially used.
Only data from the target year have been used for each annual mosaic,
and hence no gap\-filling using data from previous years in case of gaps
in the annual global coverage.


There is no data for 2011\-2014 due to the gap between ALOS and ALOS\-2
temporal coverage.


The SAR imagery was ortho\-rectificatied and slope corrected using the
digital surface model ALOS World 3D \- 30m (AW3D30\).


A destriping process (Shimada \& Isoguchi, 2002, 2010\) was applied
to equalize the intensity differences between neighboring strips,
occurring largely due to seasonal and daily differences
in surface moisture conditions.


Polarization data are stored as 16\-bit digital numbers (DN).
The DN values can be converted to gamma naught values
in decibel unit (dB) using the following equation:


* γ₀ \= 10log₁₀(DN²) \- 83\.0 dB


Attention:


* Backscatter values may vary significantly from path to path
over high latitude forest areas. This is due to the change of
backscattering intensity caused by freezing trees in winter.


More information is available in the provider's
[Dataset Description](https://www.eorc.jaxa.jp/ALOS/en/dataset/pdf/DatasetDescription_PALSAR2_Mosaic_ver212.pdf).





### Bands



**Pixel Size**
  
25 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `HH` | None | HH polarization backscattering coefficient, 16\-bit DN. |
| `HV` | None | HV polarization backscattering coefficient, 16\-bit DN. |
| `angle` | deg | Local incidence angle. |
| `epoch` | None | Observation date timestamp (milliseconds since Jan 1, 1970\). This band is computed on the fly from the 'date' band of the raw data, which represents the difference in days between 2014\-05\-24 and the observation date. |
| `qa` | None | Processing information. |


**qa Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#000000 | No data |
| 50 | \#0000ff | Ocean and water |
| 100 | \#aaaa00 | Radar layover |
| 150 | \#005555 | Radar shadowing |
| 255 | \#aa9988 | Land |




### Terms of Use


**Terms of Use**


JAXA retains ownership of the dataset and cannot guarantee
any problem caused by or possibly caused by using the datasets.
Anyone wishing to publish any results using the datasets should
clearly acknowledge the ownership of the data in the publication.




### Citations



Citations:
* Masanobu Shimada, Takuya Itoh, Takeshi Motooka, Manabu Watanabe,
Shiraishi Tomohiro, Rajesh Thapa, and Richard Lucas, "New Global
Forest/Non\-forest Maps from ALOS PALSAR Data (2007\-2010\)", Remote Sensing
of Environment, 155, pp. 13\-31, December 2014\.
[doi:10\.1016/j.rse.2014\.04\.014\.](https://doi.org/10.1016/j.rse.2014.04.014)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('JAXA/ALOS/PALSAR/YEARLY/SAR_EPOCH')
.filter(ee.Filter.date('2017-01-01','2018-01-01'));
varsarHh=dataset.select('HH');
varsarHhVis={
min:0.0,
max:10000.0,
};
Map.setCenter(136.85,37.37,4);
Map.addLayer(sarHh,sarHhVis,'SAR HH');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_ALOS_PALSAR_YEARLY_SAR_EPOCH)


[Global PALSAR\-2/PALSAR Yearly Mosaic, version 2](/earth-engine/datasets/catalog/JAXA_ALOS_PALSAR_YEARLY_SAR_EPOCH)

The global 25m PALSAR/PALSAR\-2 mosaic is a seamless global SAR image created by mosaicking strips of SAR imagery from PALSAR/PALSAR\-2\. For each year and location, the strip data were selected through visual inspection of the browse mosaics available over the period, with those showing minimum response to surface moisture preferentially …

 JAXA/ALOS/PALSAR/YEARLY/SAR\_EPOCH,
 alos,alos2,eroc,jaxa,palsar,palsar2,sar,satellite\-imagery

2015\-01\-01T00:00:00Z/2023\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








