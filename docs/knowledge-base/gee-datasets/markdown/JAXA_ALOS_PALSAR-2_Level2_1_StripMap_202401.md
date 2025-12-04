



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

ALOS\-2 PALSAR\-2 StripMap Level 2\.1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================








Dataset Availability
2022\-09\-26T00:00:00Z–2024\-01\-08T00:00:00Z
Dataset Provider


[JAXA EORC](https://www.eorc.jaxa.jp/ALOS/en/dataset/palsar2_l22_e.htm)



Earth Engine Snippet


`ee.ImageCollection("JAXA/ALOS/PALSAR-2/Level2_1/StripMap_202401")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_ALOS_PALSAR-2_Level2_1_StripMap_202401)





Tags


[alos2](/earth-engine/datasets/tags/alos2)
[eroc](/earth-engine/datasets/tags/eroc)
[jaxa](/earth-engine/datasets/tags/jaxa)
[palsar2](/earth-engine/datasets/tags/palsar2)
[radar](/earth-engine/datasets/tags/radar)
[sar](/earth-engine/datasets/tags/sar)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)








#### Description



Starting from the night of January 1st, 2024, based on the request from
Japanese ministries and related organization, JAXA implemented ALOS\-2
PALSAR\-2 emergency observation. Since JAXA expects these emergency
observation data to be extremely useful for disaster
management, JAXA decided to open these data on Google Earth Engine for
public and research usage.


JAXA released PALSAR\-2 Level 2\.1 strip map mode observation data with 3m
single polarization for January 1\-3 and January 8 2024, together with
some archive
data. PALSAR\-2 Level 2\.1 data is orthorectified from level 1\.1 data by using
digital elevation model. The DN values can be converted to sigma naught
values in decibel unit (dB) using the following equation:


* σ0 \= 10\*log10(DN2) \- 83\.0 dB


Below are the dates for which the dataset has data.




| Obs date | Frame | Beam | A/D |
| --- | --- | --- | --- |
| 2024/01/01 and 2022/09/26 | 0750, 0760, 0770 | U2\-6L | Asc. |
| 2024/01/02 and 2023/06/06 | 2820, 2830, 2840 | U2\-8L | Desc. |
| 2024/01/08, 2024/01/03 and 2023/12/06 | 0720, 0730 | U2\-9R | Asc. |





### Bands



**Pixel Size**
  
3 meters



**Bands**




| Name | Description |
| --- | --- |
| `b1` | HH polarization Terrain\-flattened Gamma\-Nought backscatter coefficient. |




### Terms of Use


**Terms of Use**


Anyone can use this data free of charge subject to non\-commercial use only.
For detailed terms of use see JAXA
[G\-Portal Terms of service](https://gportal.jaxa.jp/gpr/index/eula?lang=en)
(Section 7\. Condition concerning of G\-Portal data).




### Citations



Citations:
* The data used for this paper have been provided by Earth Observation
Research Center (EORC) of Japan Aerospace Exploration Agency (JAXA).





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varcoll=ee.ImageCollection('JAXA/ALOS/PALSAR-2/Level2_1/StripMap_202401');

varvis={min:0,max:8000};

// Visualize different date ranges
varvisualizeDateRange=function(startDate,endDate,layerName){
vardateRange=coll.filterDate(startDate,endDate);
Map.addLayer(dateRange,vis,layerName);
};

visualizeDateRange('2023-06-06','2023-06-07','Before-2023-06-06');
visualizeDateRange('2023-06-12','2023-06-13','Before-2023-06-12');
visualizeDateRange('2022-09-26','2022-09-27','Before-2022-09-26');
visualizeDateRange('2023-12-06','2023-12-07','Before-2023-12-06');
visualizeDateRange('2024-01-01','2024-01-02','After-2024-01-01');
visualizeDateRange('2024-01-02','2024-01-03','After-2024-01-02');
visualizeDateRange('2024-01-03','2024-01-04','After-2024-01-03');
visualizeDateRange('2024-01-08','2024-01-09','After-2024-01-08');

Map.setCenter(137.2228,37.1204,8);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_ALOS_PALSAR-2_Level2_1_StripMap_202401)


[ALOS\-2 PALSAR\-2 StripMap Level 2\.1](/earth-engine/datasets/catalog/JAXA_ALOS_PALSAR-2_Level2_1_StripMap_202401)

Starting from the night of January 1st, 2024, based on the request from Japanese ministries and related organization, JAXA implemented ALOS\-2 PALSAR\-2 emergency observation. Since JAXA expects these emergency observation data to be extremely useful for disaster management, JAXA decided to open these data on Google Earth Engine for public …

 JAXA/ALOS/PALSAR\-2/Level2\_1/StripMap\_202401,
 alos2,eroc,jaxa,palsar2,radar,sar,satellite\-imagery

2022\-09\-26T00:00:00Z/2024\-01\-08T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








