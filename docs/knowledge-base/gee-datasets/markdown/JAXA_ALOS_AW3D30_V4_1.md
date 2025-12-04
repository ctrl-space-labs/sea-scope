



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

ALOS DSM: Global 30m v4\.1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================








Dataset Availability
2006\-01\-24T00:00:00Z–2011\-05\-12T00:00:00Z
Dataset Provider


[JAXA Earth Observation Research Center](https://www.eorc.jaxa.jp/ALOS/en/dataset/aw3d30/aw3d30_e.htm)



Earth Engine Snippet


`ee.ImageCollection("JAXA/ALOS/AW3D30/V4_1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_ALOS_AW3D30_V4_1)





Tags


[alos](/earth-engine/datasets/tags/alos)
[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[geophysical](/earth-engine/datasets/tags/geophysical)
[jaxa](/earth-engine/datasets/tags/jaxa)
[topography](/earth-engine/datasets/tags/topography)








#### Description



ALOS World 3D \- 30m (AW3D30\) is a global digital surface
model (DSM) dataset with a horizontal resolution of approximately
30 meters (1 arcsec mesh). The dataset is based on the DSM dataset
(5\-meter mesh version) of the [World 3D Topographic Data](https://www.aw3d.jp/en/).
More details are available in the dataset [documentation](https://www.eorc.jaxa.jp/ALOS/en/dataset/aw3d30/data/aw3d30v4.1_product_e_1.0.pdf).


This ingested dataset combines data from versions 3\.1, 4\.0, and 4\.1\.


Version 4\.1 (April 2024\): This major update released 19,051 tiles covering
global regions (excluding Antarctica and Japan). It incorporates new
supplementary data for void filling and corrects partial anomalies found in
versions 3\.1 and 3\.2, along with re\-filling voids. For specific tile updates
in v4\.1, please use the v4\.1 filter on map tiles or consult the latest
format description.


Version 4\.0 (April 2023\): This update released 1,886 tiles, improving low
and mid\-latitude regions and areas south of 60 degrees latitude.


Key changes include:
1\. New supplementary data for void filling.
2\. Correction of partial anomalies and re\-filling of voids (2 tiles).
3\. Updated coastlines for regions south of 60 degrees latitude (44 tiles).
4\. Disabled Caspian Sea water mask and supplemented with elevation data
 (54 tiles).
5\. Extracted and corrected new partial anomaly areas in South America
 (1,786 tiles).
6\. For detailed tile information for v4\.0, please use the v4\.0 filter on
 map tiles or refer to the format description.


Version 3\.2, released in January 2021, is an improved version created by
reconsidering the format in the high latitude area, auxiliary data, and
processing method. Different pixel spacing for each latitude zone was
adopted at high latitude area. Coastline data, which is one of the
auxiliary datasets, was changed, and new supplementary data was used. In
addition, as a source data for Japan, AW3D version 3 was also used.
Furthermore, the method of detecting anomalous values in the process was
improved.


**Note:** See the code example for the recommended way of computing slope.
Unlike most DEMs in Earth Engine, this is an image collection due to
multiple resolutions of source files that make it impossible to mosaic them
into a single asset, so the slope computations need a reprojection.
The AW3D DSM elevation is calculated by an image matching process
that uses a stereo pair of optical images. Clouds, snow, and ice are
automatically identified during processing and applied the
mask information. However, mismatched points sometimes
remain especially surrounding (or at the edges of) clouds, snow,
and ice areas, which cause some height errors in the final DSM.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `DSM` | \-433\* | 8768\* | Height above sea level. Signed 16 bits. Elevation (in meter) converted from the ellipsoidal height based on ITRF97 and GRS80, using EGM96†1 geoid model. |
| `STK` | 1\* | 54\* | Stacking number of the scene unit DSM used in producing DSM. The band is derived by resampling the stacking number for 5m resolution DSM to 30m resolution. |
| `MSK` | 8\-bit mask for the band. |
| Bitmask for MSK * Bits 0\-7: Generated from resampled DSM. 	+ 0: Valid 	+ 1: Cloud and snow mask (invalid). 	+ 2: Land water and low correlation mask (valid). 	+ 3: Sea mask (valid). 	+ 4: Void filled with GSI DTM (valid). 	+ 8: Void filled with Shuttle Radar Topography Mission 	SRTM\-1 Version 3 (valid). 	+ 12: Void filled with PRISM DSM (valid). 	+ 16: Void filled with ViewFinder Panoramas DEM (valid). 	+ 24: Void filled with ASTER GDEM v2 (valid). 	+ 28: Void filled with ArcticDEM v2 (valid). 	+ 32: Void filled with TanDEM\-X 90m DEM (valid). 	+ 36: Void filled with ArcticDEM v3 (valid). 	+ 40: Void filled with ASTER GDEM v3 (valid). 	+ 44: Void filled with REMA v1\.1 (valid). 	+ 48: Void filled with Copernicus DEM GLO\-30 (valid). 	+ 52: Void filled with ArcticDEM v4 (valid). 	+ 252: Void filled with applied IDW method (gdal\_fillnodata) (valid) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


This dataset is available to use with no charge under
the conditions specified in the [Terms of use for ALOS Global Digital
Surface Model](https://earth.jaxa.jp/en/data/policy/).




### Citations



Citations:
* T. Tadono, H. Ishida, F. Oda, S. Naito, K. Minakawa, H. Iwamoto
Precise Global DEM Generation By ALOS PRISM, ISPRS Annals of
the Photogrammetry, Remote Sensing and Spatial Information Sciences,
Vol.II\-4, pp.71\-76, 2014\. [PDF file](https://www.isprs-ann-photogramm-remote-sens-spatial-inf-sci.net/II-4/71/2014/isprsannals-II-4-71-2014.pdf)
* J. Takaku, T. Tadono, K. Tsutsui : Generation of High Resolution
Global DSM from ALOS PRISM, The International Archives of the Photogrammetry,
Remote Sensing and Spatial Information Sciences, Vol. XL\-4, pp.243\-248,
ISPRS, 2014\. [PDF file](https://www.int-arch-photogramm-remote-sens-spatial-inf-sci.net/XL-4/243/2014/isprsarchives-XL-4-243-2014.pdf)
* J. Takaku, T. Tadono, K. Tsutsui, M. Ichikawa : Validation of
'AW3D' Global DSM Generated from ALOS PRISM, ISPRS
Annals of the Photogrammetry, Remote Sensing and Spatial Information
Sciences, Vol.III\-4, pp.25\-31, 2016\. [PDF file](https://www.isprs-ann-photogramm-remote-sens-spatial-inf-sci.net/III-4/25/2016/isprs-annals-III-4-25-2016.pdf)
* T. Tadono, H. Nagai, H. Ishida, F. Oda, S. Naito, K. Minakawa,
H. Iwamoto : Initial Validation of the 30 m\-mesh Global Digital
Surface Model Generated by ALOS PRISM, The International Archives
of the Photogrammetry, Remote Sensing and Spatial Information Sciences,
ISPRS, Vol. XLI\-B4, pp.157\-162, 2016\. [PDF file](https://www.int-arch-photogramm-remote-sens-spatial-inf-sci.net/XLI-B4/157/2016/isprs-archives-XLI-B4-157-2016.pdf)
* J. Takaku, T. Tadono, M. Doutsu, F. Ohgushi, and H. Kai, : "Updates of
'AW3D30' ALOS Global Digital Surface Model in Antarctica with Other Open
Access Datasets", Int. Arch. Photogramm. Remote Sens. Spatial Inf. Sci.,
XLIII\-B4\-2021, 401\-408, 2021\. [PDF file](https://www.int-arch-photogramm-remote-sens-spatial-inf-sci.net/XLIII-B4-2021/401/2021/isprs-archives-XLIII-B4-2021-401-2021.pdf)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('JAXA/ALOS/AW3D30/V4_1');
varelevation=dataset.select('DSM');
varelevationVis={
min:0,
max:5000,
palette:['0000ff','00ffff','ffff00','ff0000','ffffff']
};
Map.setCenter(138.73,35.36,11);
Map.addLayer(elevation,elevationVis,'Elevation');

// Reproject an image mosaic using a projection from one of the image tiles,
// rather than using the default projection returned by .mosaic().
varproj=elevation.first().select(0).projection();
varslopeReprojected=ee.Terrain.slope(elevation.mosaic()
.setDefaultProjection(proj));
Map.addLayer(slopeReprojected,{min:0,max:45},'Slope');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_ALOS_AW3D30_V4_1)


[ALOS DSM: Global 30m v4\.1](/earth-engine/datasets/catalog/JAXA_ALOS_AW3D30_V4_1)

ALOS World 3D \- 30m (AW3D30\) is a global digital surface model (DSM) dataset with a horizontal resolution of approximately 30 meters (1 arcsec mesh). The dataset is based on the DSM dataset (5\-meter mesh version) of the World 3D Topographic Data. More details are available in the dataset documentation. …

 JAXA/ALOS/AW3D30/V4\_1,
 alos,dem,elevation,elevation\-topography,geophysical,jaxa,topography

2006\-01\-24T00:00:00Z/2011\-05\-12T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








