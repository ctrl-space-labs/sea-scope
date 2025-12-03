



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

SRTM Digital Elevation Data Version 4


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================








Dataset Availability
2000\-02\-11T00:00:00Z–2000\-02\-22T00:00:00Z
Dataset Provider


[NASA/CGIAR](https://srtm.csi.cgiar.org/)



Earth Engine Snippet


`ee.Image("CGIAR/SRTM90_V4")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CGIAR/CGIAR_SRTM90_V4)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[geophysical](/earth-engine/datasets/tags/geophysical)
[srtm](/earth-engine/datasets/tags/srtm)
[topography](/earth-engine/datasets/tags/topography)
cgiar








#### Description



The Shuttle Radar Topography Mission (SRTM) digital
elevation dataset was originally produced to provide consistent,
high\-quality elevation data at near global scope. This version
of the SRTM digital elevation data has been processed to fill data
voids, and to facilitate its ease of use.





### Bands


**Bands**




| Name | Units | Min | Max | Pixel Size | Description |
| --- | --- | --- | --- | --- | --- |
| `elevation` | m | \-444\* | 8806\* | Elevation |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


DISTRIBUTION. Users are prohibited from any commercial, non\-free resale, or
redistribution without explicit written permission from CIAT. Users should
acknowledge CIAT as the source used in the creation of any reports,
publications, new datasets, derived products, or services resulting from the
use of this dataset. CIAT also request reprints of any publications and
notification of any redistributing efforts. For commercial access to
the data, send requests to [Andy Jarvis](mailto:a.jarvis@cgiar.org).


NO WARRANTY OR LIABILITY. CIAT provides these data without any warranty of
any kind whatsoever, either express or implied, including warranties of
merchantability and fitness for a particular purpose. CIAT shall not be
liable for incidental, consequential, or special damages arising out of
the use of any data.


ACKNOWLEDGMENT AND CITATION. Any users are kindly asked to cite this data
in any published material produced using this data, and if possible link
web pages to the [CIAT\-CSI SRTM website](https://srtm.csi.cgiar.org).




### Citations



Citations:
* Jarvis, A., H.I. Reuter, A. Nelson, E. Guevara. 2008\. Hole\-filled
SRTM for the globe Version 4, available from the CGIAR\-CSI SRTM
90m Database: <https://srtm.csi.cgiar.org>.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('CGIAR/SRTM90_V4');
varelevation=dataset.select('elevation');
varslope=ee.Terrain.slope(elevation);
Map.setCenter(-112.8598,36.2841,10);
Map.addLayer(slope,{min:0,max:60},'slope');
```




Python setup


See the [Python Environment](/earth-engine/guides/python_install) page for information on the Python API and using
 `geemap` for interactive development.



```
importee
importgeemap.coreasgeemap
```


### Colab (Python)



```
dataset = ee.Image('CGIAR/SRTM90_V4')
elevation = dataset.select('elevation')
slope = ee.Terrain.slope(elevation)

m = geemap.Map()
m.set_center(-112.8598, 36.2841, 10)
m.add_layer(slope, {'min': 0, 'max': 60}, 'slope')
m
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/CGIAR/CGIAR_SRTM90_V4)


[SRTM Digital Elevation Data Version 4](/earth-engine/datasets/catalog/CGIAR_SRTM90_V4)

The Shuttle Radar Topography Mission (SRTM) digital elevation dataset was originally produced to provide consistent, high\-quality elevation data at near global scope. This version of the SRTM digital elevation data has been processed to fill data voids, and to facilitate its ease of use.

 CGIAR/SRTM90\_V4,
 dem,elevation,elevation\-topography,geophysical,srtm,topography

2000\-02\-11T00:00:00Z/2000\-02\-22T00:00:00Z



 \-56 \-180 60 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








