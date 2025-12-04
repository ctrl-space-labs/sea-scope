



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NASADEM: NASA 30m Digital Elevation Model


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===========================================================================================================================================








Dataset Availability
2000\-02\-11T00:00:00Z–2000\-02\-22T00:00:00Z
Dataset Provider


[NASA / USGS / JPL\-Caltech](https://lpdaac.usgs.gov/products/nasadem_hgtv001/)



Earth Engine Snippet


`ee.Image("NASA/NASADEM_HGT/001")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_NASADEM_HGT_001)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[geophysical](/earth-engine/datasets/tags/geophysical)
[nasa](/earth-engine/datasets/tags/nasa)
[srtm](/earth-engine/datasets/tags/srtm)
[topography](/earth-engine/datasets/tags/topography)
[usgs](/earth-engine/datasets/tags/usgs)
nasadem








#### Description



NASADEM is a reprocessing of SRTM data, with improved accuracy by incorporating auxiliary data
from ASTER GDEM, ICESat GLAS, and PRISM datasets.


The most significant processing improvements involve void reduction through improved
phase unwrapping and using ICESat GLAS data for control.


Documentation:


* [User's Guide](https://lpdaac.usgs.gov/documents/592/NASADEM_User_Guide_V1.pdf)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `elevation` | m | \-512\* | 8768\* | Integer heights in the merged void\-free DEM files are relative to the EGM96 geoid (whereas the floating\-point heights in the SRTM\-only DEM files are relative to the WGS84 ellipsoid). |
| `num` | None | 0 | 255 | Index indicating the data source and the number of source scenes.* 0: Water in corrected SRTM water body data * 1\-23: SRTM 1\-23 (max known is 23\) * 41\-94: PRISM 1\-50 (54 max polar, 37 max elsewhere) * 110\-160: GDEM3 (saturated at 50\) * 170\-220: GDEM2 (saturated at 50\) * 231: SRTMv3 from GDEM3 * 232: SRTMv2 from GDEM3 * 233: SRTMv2 from GDEM2 * 234: SRTM\-with\-NGA\-fill from GDEM2 * 241: NED from GDEM2 (USA) * 242: NED from GDEM3 (USA) * 243: CDED from GDEM2 (Canada) * 244: CDED from GDEM3 (Canada) * 245: Alaska from GDEM2 (Alaska) * 246: Alaska from GDEM3 (Alaska) * 250: Interpolation * 251: Quad edge averaged where two neighboring quads disagreed (generally a GDEM error) * 255: ERROR (if NUM IS MISSING \- none known to exist) |
| `swb` | None | 0 | 255 | Updated SRTM water body data* 0: Land * 255: Water |


 \* estimated min or max value
**swb Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | brown | Land |
| 255 | cadetblue | Water |




### Terms of Use


**Terms of Use**


Unless otherwise noted, all NASA\-produced data may be used for any purpose without
prior permission. For more information and exceptions visit the
[NASA Data \& Information Policy page](https://earthdata.nasa.gov/collaborate/open-data-services-and-software/data-information-policy).




### Citations



Citations:
* NASA JPL (2020\). NASADEM Merged DEM Global 1 arc second V001 \[Data set]. NASA EOSDIS Land
Processes DAAC. Accessed 2020\-12\-30 from [doi:10\.5067/MEaSUREs/NASADEM/NASADEM\_HGT.001](https://doi.org/10.5067/MEaSUREs/NASADEM/NASADEM_HGT.001)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Import the dataset and select the elevation band.
vardataset=ee.Image('NASA/NASADEM_HGT/001');
varelevation=dataset.select('elevation');

// Add a white background image to the map.
varbackground=ee.Image(1);
Map.addLayer(background,{min:0,max:1});

// Set elevation visualization properties.
varelevationVis={
min:0,
max:2000,
};

// Set elevation <= 0 as transparent and add to the map.
Map.addLayer(elevation.updateMask(elevation.gt(0)),elevationVis,'Elevation');
Map.setCenter(17.93,7.71,2);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_NASADEM_HGT_001)


[NASADEM: NASA 30m Digital Elevation Model](/earth-engine/datasets/catalog/NASA_NASADEM_HGT_001)

NASADEM is a reprocessing of SRTM data, with improved accuracy by incorporating auxiliary data from ASTER GDEM, ICESat GLAS, and PRISM datasets. The most significant processing improvements involve void reduction through improved phase unwrapping and using ICESat GLAS data for control. Documentation: User's Guide

 NASA/NASADEM\_HGT/001,
 dem,elevation,elevation\-topography,geophysical,nasa,srtm,topography,usgs

2000\-02\-11T00:00:00Z/2000\-02\-22T00:00:00Z



 \-56 \-180 60 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








