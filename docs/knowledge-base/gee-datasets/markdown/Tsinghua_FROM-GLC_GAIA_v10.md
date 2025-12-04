



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Tsinghua FROM\-GLC Year of Change to Impervious Surface


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================================








Dataset Availability
1985\-01\-01T00:00:00Z–2018\-12\-31T00:00:00Z
Dataset Provider


[Tsinghua University](http://data.ess.tsinghua.edu.cn/)



Earth Engine Snippet


`ee.Image("Tsinghua/FROM-GLC/GAIA/v10")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Tsinghua/Tsinghua_FROM-GLC_GAIA_v10)





Tags


[built](/earth-engine/datasets/tags/built)
[population](/earth-engine/datasets/tags/population)
[tsinghua](/earth-engine/datasets/tags/tsinghua)
[urban](/earth-engine/datasets/tags/urban)
development
impervious








#### Description



This dataset contains annual change information of global impervious surface area from 1985 to
2018 at a 30m resolution. Change from pervious to impervious was determined using a combined
approach of supervised classification and temporal consistency checking. Impervious pixels are
defined as above 50% impervious. The year of the transition (from pervious to impervious) can
be identified from the pixel value, ranging from 34 (year: 1985\) to 1 (year: 2018\). For
example, the impervious surface in 1990 can be revealed as the pixel value greater than 29
(see the lookup table). This dataset is temporally consistent, following the conversion from
pervious (e.g., non\-urban) to impervious (e.g., urban) monotonically. For more information
about the mapping approach and assessment, see
[Annual maps of global artificial impervious area (GAIA) between 1985 and 2018
(Gong et al. 2020\)](https://doi.org/10.1016/j.rse.2019.111510).





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `change_year_index` | 1\* | 34\* | Year of the transition from from pervious to impervious. From 34 (year: 1985\) to 1 (year: 2018\) |


 \* estimated min or max value
**change\_year\_index Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#014352 | 2018 |
| 2 | \#1a492c | 2017 |
| 3 | \#071ec4 | 2016 |
| 4 | \#b5ca36 | 2015 |
| 5 | \#729eac | 2014 |
| 6 | \#8ea5de | 2013 |
| 7 | \#818991 | 2012 |
| 8 | \#62a3c3 | 2011 |
| 9 | \#ccf4fe | 2010 |
| 10 | \#74f0b9 | 2009 |
| 11 | \#32bc55 | 2008 |
| 12 | \#c72144 | 2007 |
| 13 | \#56613b | 2006 |
| 14 | \#c14683 | 2005 |
| 15 | \#c31c25 | 2004 |
| 16 | \#5f6253 | 2003 |
| 17 | \#11bf85 | 2002 |
| 18 | \#a61b26 | 2001 |
| 19 | \#99fbc5 | 2000 |
| 20 | \#188aaa | 1999 |
| 21 | \#c2d7f1 | 1998 |
| 22 | \#b7d9d8 | 1997 |
| 23 | \#856f96 | 1996 |
| 24 | \#109c6b | 1995 |
| 25 | \#2de3f4 | 1994 |
| 26 | \#9a777d | 1993 |
| 27 | \#151796 | 1992 |
| 28 | \#c033d8 | 1991 |
| 29 | \#510037 | 1990 |
| 30 | \#640c21 | 1989 |
| 31 | \#31a191 | 1988 |
| 32 | \#223ab0 | 1987 |
| 33 | \#b692ac | 1986 |
| 34 | \#2de3f4 | 1985 |




### Terms of Use


**Terms of Use**


This work is licensed under a Creative Commons Attribution 4\.0 International License.
[https://creativecommons.org/licenses/by/4\.0/](https://creativecommons.org/licenses/by/4.0/)




### Citations



Citations:
* Gong, P., Li, X., Wang, J., Bai, Y., Chen, B., Hu, T., ... \& Zhou, Y. (2020\).
Annual maps of global artificial impervious area (GAIA) between 1985 and 2018\.
Remote Sensing of Environment, 236, 111510\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('Tsinghua/FROM-GLC/GAIA/v10');

varvisualization={
bands:['change_year_index'],
min:0,
max:34,
palette:[
'014352','1a492c','071ec4','b5ca36','729eac','8ea5de',
'818991','62a3c3','ccf4fe','74f0b9','32bc55','c72144',
'56613b','c14683','c31c25','5f6253','11bf85','a61b26',
'99fbc5','188aaa','c2d7f1','b7d9d8','856f96','109c6b',
'2de3f4','9a777d','151796','c033d8','510037','640c21',
'31a191','223ab0','b692ac','2de3f4',
]
};

Map.setCenter(-37.62,25.8,2);

Map.addLayer(dataset,visualization,'Change year index');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/Tsinghua/Tsinghua_FROM-GLC_GAIA_v10)


[Tsinghua FROM\-GLC Year of Change to Impervious Surface](/earth-engine/datasets/catalog/Tsinghua_FROM-GLC_GAIA_v10)

This dataset contains annual change information of global impervious surface area from 1985 to 2018 at a 30m resolution. Change from pervious to impervious was determined using a combined approach of supervised classification and temporal consistency checking. Impervious pixels are defined as above 50% impervious. The year of the transition …

 Tsinghua/FROM\-GLC/GAIA/v10,
 built,population,tsinghua,urban

1985\-01\-01T00:00:00Z/2018\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








