



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

RGE ALTI: IGN RGE ALTI Digital Elevation 1m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================








Dataset Availability
2009\-01\-01T00:00:00Z–2021\-01\-01T00:00:00Z
Dataset Provider


[IGN](https://geoservices.ign.fr/rgealti)



Earth Engine Snippet


`ee.ImageCollection("IGN/RGE_ALTI/1M/2_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/IGN/IGN_RGE_ALTI_1M_2_0)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[geophysical](/earth-engine/datasets/tags/geophysical)








#### Description



The RGE ALTI dataset describes the digital elevation model (DEM) of France
with the pixel size of 1m. It was created from surveys obtained by airborne
lidar or by correlation of aerial images.


Lidar was deployed for flood\-prone, coastal, and large forest
areas. The vertical accuracy of the DEM in these areas is between
0\.2m and 0\.5m. Radar was used in mountain areas (Alps, Pyrenees,
Cevennes, Corsica). Caution: in areas with steep slopes, the average
vertical accuracy is the order of 7m.


The accuracy of these fields has been checked against various sources:
the road and hydrographic networks of the
[BD TOPO](https://geoservices.ign.fr/bdtopo), geodetic terminals and
points calculated on the ground.


Aerial photo correlation techniques are used in the rest of the territory.
On certain zones treated by correlation, ground measurements are absent
over large extents due to the presence of vegetation
(wooded areas, for example). 1987\-2001 altimetry data (BD Alti) are used
to fill these gaps. The vertical accuracy of the DEM on these areas
is between 0\.5m and 0\.7m.


Currently the collection includes a single image IGN/RGE\_ALTI/1M/2\_0/FXX
showing metropolitan France.


This dataset was prepared and ingested with the support of Guillaume Attard
and Julien Bardonnet ([AGEOCE](https://www.ageoce.com)).
The preparation process is
[described here](https://medium.com/@gui.attard/pre-processing-the-dem-of-france-rge-alti-5m-for-implementation-into-earth-engine-de9a0778e0d9).


See also:
[user's guide](https://geoservices.ign.fr/sites/default/files/2021-07/DC_RGEALTI_2-0.pdf).





### Bands



**Pixel Size**
  
1 meter



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `MNT` | m | \-40\* | 4810\* | Terrain elevation in meters. |
| `SRC` | None | The main source of the data used to calculate the altitude of the node. See Appendix B page 26 in the [user guide](https://geoservices.ign.fr/sites/default/files/2021-07/DC_RGEALTI_2-0.pdf). |
| `DST` | m | 0 | 255 | The distance in meters between the node and the nearest point used to calculate its altitude. |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


[etalab\-2\.0](https://spdx.org/licenses/etalab-2.0.html)




### Citations



Citations:
* IGN (2021\). RGE ALTI 1m \[Data set]. Accessed 2022\-07\-01 from
[IGN website](https://geoservices.ign.fr/rgealti#telechargement1m)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('IGN/RGE_ALTI/1M/2_0/FXX');
varelevation=dataset.select('MNT');

varelevationVis={
min:0,
max:1000,
palette:['006600','002200','fff700','ab7634','c4d0ff','ffffff']
};

Map.addLayer(elevation,elevationVis,'Elevation');
Map.setCenter(3,47,5);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/IGN/IGN_RGE_ALTI_1M_2_0)


[RGE ALTI: IGN RGE ALTI Digital Elevation 1m](/earth-engine/datasets/catalog/IGN_RGE_ALTI_1M_2_0)

The RGE ALTI dataset describes the digital elevation model (DEM) of France with the pixel size of 1m. It was created from surveys obtained by airborne lidar or by correlation of aerial images. Lidar was deployed for flood\-prone, coastal, and large forest areas. The vertical accuracy of the DEM in …

 IGN/RGE\_ALTI/1M/2\_0,
 dem,elevation,elevation\-topography,geophysical

2009\-01\-01T00:00:00Z/2021\-01\-01T00:00:00Z



 41\.35 \-5\.2 51\.14 9\.85
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








