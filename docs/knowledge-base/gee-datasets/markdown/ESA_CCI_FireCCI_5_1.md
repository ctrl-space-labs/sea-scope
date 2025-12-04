



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

FireCCI51: MODIS Fire\_cci Burned Area Pixel Product, Version 5\.1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2020\-12\-01T00:00:00Z
Dataset Provider


[European Space Agency (ESA) Climate Change Initiative (CCI) Programme, Fire ECV](https://climate.esa.int/en/projects/fire/)



Earth Engine Snippet


`ee.ImageCollection("ESA/CCI/FireCCI/5_1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ESA/ESA_CCI_FireCCI_5_1)





Cadence
1 Month
Tags


[burn](/earth-engine/datasets/tags/burn)
[climate\-change](/earth-engine/datasets/tags/climate-change)
[copernicus](/earth-engine/datasets/tags/copernicus)
[esa](/earth-engine/datasets/tags/esa)
[fire](/earth-engine/datasets/tags/fire)
[fragmentation](/earth-engine/datasets/tags/fragmentation)
[geophysical](/earth-engine/datasets/tags/geophysical)
[global](/earth-engine/datasets/tags/global)
[human\-modification](/earth-engine/datasets/tags/human-modification)
[landcover](/earth-engine/datasets/tags/landcover)
[landscape\-gradient](/earth-engine/datasets/tags/landscape-gradient)
[modis](/earth-engine/datasets/tags/modis)
[monthly](/earth-engine/datasets/tags/monthly)
[stressors](/earth-engine/datasets/tags/stressors)
c3s
cci
firecci
firecci51
gcos








#### Description



The MODIS Fire\_cci Burned Area pixel product version 5\.1 (FireCCI51\)
is a monthly global \~250m spatial resolution dataset
containing information on burned area as well as ancillary data. It is based
on surface reflectance in the Near Infrared (NIR) band from the MODIS
instrument onboard the Terra satellite, as well as active fire information from
the same sensor of the Terra and Aqua satellites.


The burned area algorithm uses a two\-phase hybrid approach. In a first step
pixels with a high probability of being burned (called "seeds") are detected
based on the active fires. In a second one, a contextual growing is applied to
completely detect the fire patch. This growing phase is controlled by an
adaptive thresholding, where thresholds are computed based on the specific
characteristics of the area surrounding each seed. The variable used to guide
the whole detection process is the NIR drop between pre\- and post\-fire images.


The dataset includes for each pixel the estimated day of the first detection of
the fire, the confidence level of that detection, and the land cover that has
been burned (extracted from the ESA CCI Land Cover dataset v2\.0\.7\). In addition,
an observation flag is provided to identify the pixels that were not processed due
to the lack of valid observations or because they belong to a non\-burnable land
cover.


FireCCI51 was developed as part of the ESA Climate Change Initiative (CCI)
Programme, and it is also part of the Copernicus Climate Change Service (C3S).





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `BurnDate` | None | 1 | 366 | Estimated day of the year of the first detection of the burn |
| `ConfidenceLevel` | % | 1 | 100 | Probability of detecting a pixel as burned, expressing the uncertainty of the detection for all pixels, even if they are classified as unburned. |
| `LandCover` | None | Land cover category of the burned pixels, extracted from the CCI LandCover v2\.0\.7 product. See Defourny, P., Lamarche, C., Bontemps, S., De Maet, T., Van Bogaert, E., Moreau, I., Brockmann, C., Boettcher, M., Kirches, G., Wevers, J., Santoro, M., Ramoino, F., \& Arino, O. (2017\). Land Cover Climate Change Initiative \- Product User Guide v2\. Issue 2\.0\. \[online] Available at: [https://maps.elie.ucl.ac.be/CCI/viewer/download/ESACCI\-LC\-Ph2\-PUGv2\_2\.0\.pdf](https://maps.elie.ucl.ac.be/CCI/viewer/download/ESACCI-LC-Ph2-PUGv2_2.0.pdf) accessed: July 2020\. © ESA Climate Change Initiative \- Land Cover led by UCLouvain (2017\). |
| `ObservedFlag` | None | Flags indicating why a pixel was not processed.* \-2: the pixel is not burnable (water bodies, bare areas, urban areas, permanent snow and ice) * \-1: the pixel has not been observed during the month (due to clouds, cloud shadows or sensor failure) |


**LandCover Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#000000 | No Data |
| 10 | \#ffff64 | Cropland, rainfed |
| 20 | \#aaf0f0 | Cropland, irrigated or post\-flooding |
| 30 | \#dcf064 | Mosaic cropland (\>50%) / natural vegetation (tree, shrub, herbaceous cover) (\<50%) |
| 40 | \#c8c864 | Mosaic natural vegetation (tree, shrub, herbaceous cover) (\>50%) / cropland (\<50%) |
| 50 | \#006400 | Tree cover, broadleaved, evergreen, closed to open (\>15%) |
| 60 | \#00a000 | Tree cover, broadleaved, deciduous, closed to open (\>15%) |
| 70 | \#003c00 | Tree cover, needleleaved, evergreen, closed to open (\>15%) |
| 80 | \#285000 | Tree cover, needleleaved, deciduous, closed to open (\>15%) |
| 90 | \#788200 | Tree cover, mixed leaf type (broadleaved and needleleaved) |
| 100 | \#8ca000 | Mosaic tree and shrub (\>50%) / herbaceous cover (\<50%) |
| 110 | \#be9600 | Mosaic herbaceous cover (\>50%) / tree and shrub (\<50%) |
| 120 | \#966400 | Shrubland |
| 130 | \#ffb432 | Grassland |
| 140 | \#ffdcd2 | Lichens and mosses |
| 150 | \#ffebaf | Sparse vegetation (tree, shrub, herbaceous cover) (\<15%) |
| 170 | \#009678 | Tree cover, flooded, saline water |
| 180 | \#00dc82 | Shrub or herbaceous cover, flooded, fresh/saline/brackish water |




### Terms of Use


**Terms of Use**


This dataset is free and open to all users for any purpose, with the following
terms and conditions:


* Users of the data are required to acknowledge the ESA
Climate Change Initiative and the Fire CCI project together with the individual
data providers if the data are used in a presentation or publication. Please
also cite any relevant dataset DOIs.
* Intellectual property rights (IPR) in the CCI data lie with the researchers and
organisations producing the data.
* Liability: no warranty is given as to the quality or the accuracy of the CCI
data or its suitability for any use. All implied conditions relating to the
quality or suitability of the information, and all liabilities arising from the
supply of the information (including any liability arising in negligence) are
excluded to the fullest extent permitted by law.




### Citations



Citations:
* Padilla Parellada, M. (2018\): ESA Fire Climate Change Initiative
(Fire\_cci): MODIS Fire\_cci Burned Area Pixel product, version 5\.1\. Centre for
Environmental Data Analysis, 01 November 2018\.
[https://doi.org/10\.5285/58f00d8814064b79a0c49662ad3af537](https://doi.org/10.5285/58f00d8814064b79a0c49662ad3af537).
* Related publication: Lizundia\-Loiola, J., Otón, G., Ramo, R., Chuvieco, E.
(2020\): A spatio\-temporal active\-fire clustering approach for global burned
area mapping at 250m from MODIS data. Remote Sensing of Environment, 236,
111493\. [https://doi.org/10\.1016/j.rse.2019\.111493](https://doi.org/10.1016/j.rse.2019.111493)





### DOIs


* [https://doi.org/10\.1016/j.rse.2019\.111493](https://doi.org/10.1016/j.rse.2019.111493)
* [https://doi.org/10\.5285/58f00d8814064b79a0c49662ad3af537](https://doi.org/10.5285/58f00d8814064b79a0c49662ad3af537)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Visualize FireCCI51 for one year
vardataset=ee.ImageCollection('ESA/CCI/FireCCI/5_1')
.filterDate('2020-01-01','2020-12-31');
varburnedArea=dataset.select('BurnDate');

// Use a circular palette to assign colors to date of first detection
varbaVis={
min:1,
max:366,
palette:[
'ff0000','fd4100','fb8200','f9c400','f2ff00','b6ff05',
'7aff0a','3eff0f','02ff15','00ff55','00ff99','00ffdd',
'00ddff','0098ff','0052ff','0210ff','3a0dfb','7209f6',
'a905f1','e102ed','ff00cc','ff0089','ff0047','ff0004'
]
};
varmaxBA=burnedArea.max();

Map.setCenter(0,18,2.1);
Map.addLayer(maxBA,baVis,'Burned Area');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ESA/ESA_CCI_FireCCI_5_1)


[FireCCI51: MODIS Fire\_cci Burned Area Pixel Product, Version 5\.1](/earth-engine/datasets/catalog/ESA_CCI_FireCCI_5_1)

The MODIS Fire\_cci Burned Area pixel product version 5\.1 (FireCCI51\) is a monthly global \~250m spatial resolution dataset containing information on burned area as well as ancillary data. It is based on surface reflectance in the Near Infrared (NIR) band from the MODIS instrument onboard the Terra satellite, as well …

 ESA/CCI/FireCCI/5\_1,
 burn,climate\-change,copernicus,esa,fire,fragmentation,geophysical,global,human\-modification,landcover,landscape\-gradient,modis,monthly,stressors

2001\-01\-01T00:00:00Z/2020\-12\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5285/58f00d8814064b79a0c49662ad3af537](https://doi.org/https://climate.esa.int/en/projects/fire/)
* [https://doi.org/10\.5285/58f00d8814064b79a0c49662ad3af537](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/ESA_CCI_FireCCI_5_1)









