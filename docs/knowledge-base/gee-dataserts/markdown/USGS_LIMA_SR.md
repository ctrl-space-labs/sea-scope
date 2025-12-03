



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Landsat Image Mosaic of Antarctica (LIMA) \- Processed Landsat Scenes (16 bit)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================================================








Dataset Availability
1999\-06\-30T00:00:00Z–2002\-09\-04T00:00:00Z
Dataset Provider


[USGS](https://lima.usgs.gov/index.php)



Earth Engine Snippet


`ee.ImageCollection("USGS/LIMA/SR")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_LIMA_SR)





Tags


[antarctica](/earth-engine/datasets/tags/antarctica)
[ice](/earth-engine/datasets/tags/ice)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[lima](/earth-engine/datasets/tags/lima)
[mosaic](/earth-engine/datasets/tags/mosaic)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sr](/earth-engine/datasets/tags/sr)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



The Landsat Image Mosaic of Antarctica (LIMA) is a seamless
and virtually cloudless mosaic created from processed
Landsat 7 ETM\+ scenes.


Processed Landsat Scenes (16 bit) are Level 1Gt NLAPS
scenes converted to 16 bit, processed with sun\-angle
correction, and converted to reflectance values
([Bindschadler 2008](https://lima.usgs.gov/LIMA_paper.pdf)).


Each Landsat scene is processed with elevation
data and sun\-angle correction to ensure surface features
were accurately represented. The sun's angle in Antarctica
gives the appearance of a setting sun. Because of the low
sun angle, as Landsat passes over Antarctica, the outer
edges of the continent appear brighter than areas closer
to the South Pole, so scenes have bright and dark areas.
Inconsistent sun angles and shadows where corrected for
these scenes. Without this process, mosaicking would produce
a patchwork of scenes since each scene would have a brighter
and a darker side.


Users can find individual image metadata available as a table at:
[USGS/LIMA/SR\_METADATA](/earth-engine/datasets/catalog/USGS_LIMA_SR_METADATA)





### Bands


**Bands**




| Name | Pixel Size | Wavelength | Description |
| --- | --- | --- | --- |
| `B1` | 0\.45 \- 0\.52 μm | Blue |
| `B2` | 0\.52 \- 0\.60 μm | Green |
| `B3` | 0\.63 \- 0\.69 μm | Red |
| `B4` | 0\.77 \- 0\.90 μm | Near infrared |
| `B5` | 1\.55 \- 1\.75 μm | Shortwave infrared 1 |
| `B7` | 2\.08 \- 2\.35 μm | Shortwave infrared 2 |
| `B8` | 0\.52 \- 0\.90 μm | Panchromatic |




### Terms of Use


**Terms of Use**


These images are in the public domain and can be used freely
and without acknowledgement. However, credit to the Landsat
Image Mosaic of Antarctica (LIMA) Project is greatly appreciated.




### Citations



Citations:
* Bindschadler, R., Vornberger, P., Fleming, A., Fox, A., Mullins, J.,
Binnie, D., Paulson, S., Granneman, B., and Gorodetzky, D., 2008,
The Landsat Image Mosaic of Antarctica, Remote Sensing of
Environment, 112, pp. 4214\-4226\.
[PDF](https://lima.usgs.gov/LIMA_paper.pdf)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('USGS/LIMA/SR');
varantarctica=dataset.select(['B3','B2','B1']);
varantarcticaVis={
min:0.0,
max:10000.0,
};
Map.setCenter(164.619,-77.99,7);
Map.addLayer(antarctica,antarcticaVis,'Antartica Imagery (RGB)');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_LIMA_SR)


[Landsat Image Mosaic of Antarctica (LIMA) \- Processed Landsat Scenes (16 bit)](/earth-engine/datasets/catalog/USGS_LIMA_SR)

The Landsat Image Mosaic of Antarctica (LIMA) is a seamless and virtually cloudless mosaic created from processed Landsat 7 ETM\+ scenes. Processed Landsat Scenes (16 bit) are Level 1Gt NLAPS scenes converted to 16 bit, processed with sun\-angle correction, and converted to reflectance values (Bindschadler 2008\). Each Landsat scene is …

 USGS/LIMA/SR,
 antarctica,ice,landsat\-derived,lima,mosaic,satellite\-imagery,sr,usgs

1999\-06\-30T00:00:00Z/2002\-09\-04T00:00:00Z



 \-90 \-180 \-55 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








