



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

World Settlement Footprint 2015


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================








Dataset Availability
2015\-01\-01T00:00:00Z–2016\-01\-01T00:00:00Z
Dataset Provider


[Deutsches Zentrum für Luft\- und Raumfahrt (DLR)](https://www.dlr.de/)



Earth Engine Snippet


`ee.Image("DLR/WSF/WSF2015/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/DLR/DLR_WSF_WSF2015_v1)





Tags


[landcover](/earth-engine/datasets/tags/landcover)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[population](/earth-engine/datasets/tags/population)
[sentinel1\-derived](/earth-engine/datasets/tags/sentinel1-derived)
[settlement](/earth-engine/datasets/tags/settlement)
[urban](/earth-engine/datasets/tags/urban)








#### Description



The World Settlement Footprint (WSF) 2015 is a 10m resolution binary mask
outlining the extent of human settlements globally derived by means of
2014\-2015 multitemporal Landsat\-8 and Sentinel\-1 imagery (of which \~217,000 and
\~107,000 scenes have been processed, respectively).


The temporal dynamics of human settlements over time are
sensibly different than those of all other non\-settlement information classes.
Hence, given all the multitemporal images available over a region of interest
in the selected time interval, key temporal statistics (i.e., temporal mean,
minimum, maximum, etc.) are extracted for:


* the original backscattering value
in the case of radar data; and
* different spectral indices (e.g., vegetation
index, built\-up index, etc.) derived after performing cloud masking in the case
of optical imagery.


Next, different classification schemes based on Support
Vector Machines (SVMs) are separately applied to the optical and radar temporal
features, respectively, and, finally, the two outputs are properly combined
together.


To quantitatively assess the high accuracy and reliability of the
layer, an extensive validation exercise has been carried out in collaboration
with Google based on a huge amount of ground\-truth samples (i.e., 900,000\)
labeled by crowd\-sourcing photo\-interpretation. A statistically
robust and transparent protocol has been defined following the state\-of\-the\-art
practices currently recommended in the literature.


For all technical details, please refer to
[the publication](https://www.nature.com/articles/s41597-020-00580-5)





### Bands


**Bands**




| Name | Min | Max | Pixel Size | Description |
| --- | --- | --- | --- | --- |
| `settlement` | 255 | 255 | A human settlement area |




### Terms of Use


**Terms of Use**


[CC0\-1\.0](https://spdx.org/licenses/CC0-1.0.html)




### Citations



Citations:
* Marconcini, M., Metz\-Marconcini, A., Üreyen, S., Palacios\-Lopez, D., Hanke, W., Bachofer, F.,
Zeidler, J., Esch, T., Gorelick, N., Kakarla, A., Paganini, M., Strano, E. (2020\).
Outlining where humans live, the World Settlement Footprint 2015\. Scientific Data, 7(1\), 1\-14\.
[doi:10\.1038/s41597\-020\-00580\-5](https://doi.org/10.1038/s41597-020-00580-5)





### DOIs


* [https://doi.org/10\.1038/s41597\-020\-00580\-5](https://doi.org/10.1038/s41597-020-00580-5)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('DLR/WSF/WSF2015/v1');

varopacity=0.75;
varblackBackground=ee.Image(0);
Map.addLayer(blackBackground,null,'Black background',true,opacity);

varvisualization={
min:0,
max:255,
};
Map.addLayer(dataset,visualization,'Human settlement areas');

Map.setCenter(90.45,23.7,7);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/DLR/DLR_WSF_WSF2015_v1)


[World Settlement Footprint 2015](/earth-engine/datasets/catalog/DLR_WSF_WSF2015_v1)

The World Settlement Footprint (WSF) 2015 is a 10m resolution binary mask outlining the extent of human settlements globally derived by means of 2014\-2015 multitemporal Landsat\-8 and Sentinel\-1 imagery (of which \~217,000 and \~107,000 scenes have been processed, respectively). The temporal dynamics of human settlements over time are sensibly different …

 DLR/WSF/WSF2015/v1,
 landcover,landsat\-derived,population,sentinel1\-derived,settlement,urban

2015\-01\-01T00:00:00Z/2016\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1038/s41597\-020\-00580\-5](https://doi.org/https://www.dlr.de/)
* [https://doi.org/10\.1038/s41597\-020\-00580\-5](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/DLR_WSF_WSF2015_v1)









