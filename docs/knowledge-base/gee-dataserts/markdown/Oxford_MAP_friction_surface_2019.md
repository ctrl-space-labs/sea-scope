



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global Friction Surface 2019


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================








Dataset Availability
2019\-01\-01T00:00:00Z–2020\-01\-01T00:00:00Z
Dataset Provider


[Malaria Atlas Project](https://malariaatlas.org/research-project/accessibility-to-cities/)



Earth Engine Snippet


`ee.Image("Oxford/MAP/friction_surface_2019")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Oxford/Oxford_MAP_friction_surface_2019)





Tags


[accessibility](/earth-engine/datasets/tags/accessibility)
[jrc](/earth-engine/datasets/tags/jrc)
[map](/earth-engine/datasets/tags/map)
[oxford](/earth-engine/datasets/tags/oxford)
[population](/earth-engine/datasets/tags/population)
[twente](/earth-engine/datasets/tags/twente)
friction








#### Description



This global friction surface enumerates land\-based travel speed for all land pixels between 85 degrees north and 60 degrees south for a nominal year 2019\. It also includes "walking\-only" travel speed, using non\-motorized means of transportation only.
This map was produced through a collaboration between MAP (University of Oxford), Telethon Kids Institute (Perth, Australia), Google, and the University of Twente, Netherlands.
This project builds on previous work published by Weiss et al 2018 ([doi:10\.1038/nature25181](https://doi.org/10.1038/nature25181)). Weiss et al (2018\) utilised datasets for roads (comprising the first ever global\-scale use of Open Street Map and Google roads datasets), railways, rivers, lakes, oceans, topographic conditions (slope and elevation), landcover types, and national borders. These datasets were each allocated a speed or speeds of travel in terms of time to cross each pixel of that type. The datasets were then combined to produce a "friction surface"; a map where every pixel is allocated a nominal overall speed of travel based on the types occurring within that pixel. For the current project, an updated friction surface was created to incorporate recent improvements within OSM roads data.
Differences between this friction surface and the 2015 version (Weiss et al. 2018\) are not necessarily indicative of changes in infrastructure (e.g., new roads being built). Such discrepancies are far more likely to be associated with improved data quality, in particular updates made to OSM road coverage. As a result, comparisons between the friction surfaces and resulting travel time maps should be done cautiously and generally not interpreted as representing changes in access over time.
This map represents the travel speed from this allocation process, expressed in units of minutes required to travel one meter. It forms the underlying dataset behind the global healthcare accessibility map described in the referenced paper.


Source dataset credits are as described in the accompanying paper.





### Bands



**Pixel Size**
  
927\.67 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `friction` | minutes/meter | 0\.000429 | 87\.3075 | Land\-based travel speed. |
| `friction_walking_only` | minutes/meter | 0\.012 | 87\.3075 | Land\-based travel speed using non\-motorized transport. |




### Terms of Use


**Terms of Use**


This work is licensed under a [Creative Commons Attribution
4\.0 International License](https://creativecommons.org/licenses/by/4.0/).




### Citations



Citations:
* D.J. Weiss, A. Nelson, C.A. Vargas\-Ruiz, K. Gligorić, S. Bavadekar,
E. Gabrilovich, A. Bertozzi\-Villa, J. Rozier, H.S. Gibson, T. Shekel,
C. Kamath, A. Lieber, K. Schulman, Y. Shao, V. Qarkaxhija, A.K. Nandi,
S.H. Keddie, S. Rumisha, E. Cameron, K.E. Battle, S. Bhatt, P.W. Gething.
Global maps of travel time to healthcare facilities. Nature Medicine (2020\).





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('Oxford/MAP/friction_surface_2019');
varlandBasedTravelSpeed=dataset.select('friction');
varvisParams={
min:0.0022,
max:0.04,
palette:[
'313695','4575b4','74add1','abd9e9','e0f3f8','ffffbf','fee090',
'fdae61','f46d43','d73027','a50026'
],
};
Map.setCenter(43.55,36.98,4);
Map.addLayer(landBasedTravelSpeed,visParams,'Land-based travel speed');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Oxford/Oxford_MAP_friction_surface_2019)


[Global Friction Surface 2019](/earth-engine/datasets/catalog/Oxford_MAP_friction_surface_2019)

This global friction surface enumerates land\-based travel speed for all land pixels between 85 degrees north and 60 degrees south for a nominal year 2019\. It also includes "walking\-only" travel speed, using non\-motorized means of transportation only. This map was produced through a collaboration between MAP (University of Oxford), Telethon …

 Oxford/MAP/friction\_surface\_2019,
 accessibility,jrc,map,oxford,population,twente

2019\-01\-01T00:00:00Z/2020\-01\-01T00:00:00Z



 \-60 \-180 85 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








