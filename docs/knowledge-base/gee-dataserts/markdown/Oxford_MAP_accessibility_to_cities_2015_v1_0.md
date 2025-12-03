



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Accessibility to Cities 2015


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================








Dataset Availability
2015\-01\-01T00:00:00Z–2016\-01\-01T00:00:00Z
Dataset Provider


[Malaria Atlas Project](https://malariaatlas.org/research-project/accessibility-to-cities/)



Earth Engine Snippet


`ee.Image("Oxford/MAP/accessibility_to_cities_2015_v1_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Oxford/Oxford_MAP_accessibility_to_cities_2015_v1_0)





Tags


[accessibility](/earth-engine/datasets/tags/accessibility)
[jrc](/earth-engine/datasets/tags/jrc)
[map](/earth-engine/datasets/tags/map)
[oxford](/earth-engine/datasets/tags/oxford)
[population](/earth-engine/datasets/tags/population)
[twente](/earth-engine/datasets/tags/twente)








#### Description



This global accessibility map enumerates land\-based
travel time to the nearest densely\-populated area for all areas
between 85 degrees north and 60 degrees south for a nominal year 2015\.


Densely\-populated areas are defined as contiguous areas
with 1,500 or more inhabitants per square kilometer or a majority
of built\-up land cover types coincident with a population center
of at least 50,000 inhabitants.


This map was produced through
a collaboration between the University of Oxford Malaria Atlas
Project (MAP), Google, the European Union Joint Research Centre
(JRC), and the University of Twente, Netherlands. The underlying
datasets used to produce the map include roads (comprising the
first ever global\-scale use of Open Street Map and Google roads
datasets), railways, rivers, lakes, oceans, topographic conditions
(slope and elevation), landcover types, and national borders.


These datasets were each allocated a speed or speeds of travel in terms
of time to cross each pixel of that type. The datasets were then
combined to produce a “friction surface”, a map where
every pixel is allocated a nominal overall speed of travel based
on the types occurring within that pixel. Least\-cost\-path algorithms
(running in Google Earth Engine and, for high\-latitude areas, in
R) were used in conjunction with this friction surface to calculate
the time of travel from all locations to the nearest city (by travel
time). Cities were determined using the high\-density\-cover product
created by the Global Human Settlement Project.


Each pixel in the resultant accessibility map thus represents the modeled shortest
time from that location to a city.


Source dataset credits are as described in the accompanying paper.





### Bands


**Bands**




| Name | Units | Min | Max | Pixel Size | Description |
| --- | --- | --- | --- | --- | --- |
| `accessibility` | min | 0 | 41556 | Travel time to the nearest densely\-populated area. |




### Terms of Use


**Terms of Use**


This work is licensed under a [Creative Commons Attribution
4\.0 International License](https://creativecommons.org/licenses/by/4.0/).




### Citations



Citations:
* D.J. Weiss, A. Nelson, H.S. Gibson, W. Temperley, S. Peedell, A.
Lieber, M. Hancher, E. Poyart, S. Belchior, N. Fullman, B. Mappin,
U. Dalrymple, J. Rozier, T.C.D. Lucas, R.E. Howes, L.S. Tusting,
S.Y. Kang, E. Cameron, D. Bisanzio, K.E. Battle, S. Bhatt, and
P.W. Gething. A global map of travel time to cities to assess inequalities
in accessibility in 2015\. Nature (2018\).
[doi:10\.1038/nature25181](https://doi.org/10.1038/nature25181)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('Oxford/MAP/accessibility_to_cities_2015_v1_0');
varaccessibility=dataset.select('accessibility');
varaccessibilityVis={
min:0.0,
max:41556.0,
gamma:4.0,
};
Map.setCenter(18.98,6.66,2);
Map.addLayer(accessibility,accessibilityVis,'Accessibility');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Oxford/Oxford_MAP_accessibility_to_cities_2015_v1_0)


[Accessibility to Cities 2015](/earth-engine/datasets/catalog/Oxford_MAP_accessibility_to_cities_2015_v1_0)

This global accessibility map enumerates land\-based travel time to the nearest densely\-populated area for all areas between 85 degrees north and 60 degrees south for a nominal year 2015\. Densely\-populated areas are defined as contiguous areas with 1,500 or more inhabitants per square kilometer or a majority of built\-up land …

 Oxford/MAP/accessibility\_to\_cities\_2015\_v1\_0,
 accessibility,jrc,map,oxford,population,twente

2015\-01\-01T00:00:00Z/2016\-01\-01T00:00:00Z



 \-60 \-180 85 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








