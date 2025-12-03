



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Sentinel\-3 OLCI EFR: Ocean and Land Color Instrument Earth Observation Full Resolution


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================================================================








Dataset Availability
2016\-10\-18T19:25:42Z–2025\-07\-18T08:16:52Z
Dataset Provider


[European Union/ESA/Copernicus](https://sentinel.esa.int/web/sentinel/user-guides/sentinel-3-olci)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/S3/OLCI")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S3_OLCI)





Revisit Interval
2 Days
Tags


[copernicus](/earth-engine/datasets/tags/copernicus)
[esa](/earth-engine/datasets/tags/esa)
[eu](/earth-engine/datasets/tags/eu)
[radiance](/earth-engine/datasets/tags/radiance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sentinel](/earth-engine/datasets/tags/sentinel)
[toa](/earth-engine/datasets/tags/toa)
olci








#### Description



The Ocean and Land Color Instrument (OLCI) Earth Observation
Full Resolution (EFR) dataset contains top of atmosphere radiances
at 21 spectral bands with center wavelengths ranging between
0\.4µm and 1\.02µm at spatial resolution of 300m with
worldwide coverage every \~2 days.


OLCI is one of the instruments
in the ESA/EUMETSAT Sentinel\-3 mission for measuring sea\-surface
topography, sea\- and land\-surface temperature, ocean color and
land color with high\-end accuracy and reliability to support
ocean forecasting systems, as well as environmental and climate
monitoring.


The Sentinel\-3 OLCI instrument is based on the
optomechanical and imaging design of ENVISAT's MERIS. It is designed
to retrieve the spectral distribution of upwelling radiance just
above the sea surface (the water\-leaving radiance).


OLCI observation is performed simultaneously in 21 spectral bands
ranging from the visible to the near\-infrared (400 to 1029 nm).





### Bands



**Pixel Size**
  
300 meters



**Bands**




| Name | Units | Scale | Wavelength | Description |
| --- | --- | --- | --- | --- |
| `Oa01_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.0139465 | 400nm/15nm | Aerosol correction, improved water constituent retrieval |
| `Oa02_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.0133873 | 412\.5nm/10nm | Yellow substance and detrital pigments (turbidity) |
| `Oa03_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.0121481 | 442\.5nm/10nm | Chl absorption max., biogeochemistry, vegetation |
| `Oa04_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.0115198 | 490nm/10nm | High Chl, other pigments |
| `Oa05_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.0100953 | 510nm/10nm | Chl, sediment, turbidity, red tide |
| `Oa06_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.0123538 | 560nm/10nm | Chlorophyll reference (Chl minimum) |
| `Oa07_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00879161 | 620nm/10nm | Sediment loading |
| `Oa08_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00876539 | 665nm/10nm | Chl (2^nd Chl abs. max.), sediment, yellow substance/vegetation |
| `Oa09_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.0095103 | 673\.75nm/7\.5nm | For improved fluorescence retrieval and to better account for [smile](https://sentinels.copernicus.eu/web/sentinel/technical-guides/sentinel-3-olci/level-2/smile-correction) together with the bands 665 and 680nm |
| `Oa10_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00773378 | 681\.25nm/7\.5nm | Chl fluorescence peak, red edge |
| `Oa11_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00675523 | 708\.75nm/10nm | Chl fluorescence baseline, red edge transition |
| `Oa12_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.0071996 | 753\.75nm/7\.5nm | O2 absorption/clouds, vegetation |
| `Oa13_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00749684 | 761\.25nm/7\.5nm | O2 absorption band/aerosol correction |
| `Oa14_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.0086512 | 764\.375nm/3\.75nm | Atmospheric correction |
| `Oa15_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00526779 | 767\.5nm/2\.5nm | O2A used for cloud top pressure, fluorescence over land |
| `Oa16_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00530267 | 778\.75nm/15nm | Atmospheric correction/aerosol correction |
| `Oa17_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00493004 | 865nm/20nm | Atmospheric correction/aerosol correction, clouds, pixel co\-registration |
| `Oa18_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00549962 | 885nm/10nm | Water vapor absorption reference band. Common reference band with SLSTR instrument. Vegetation monitoring |
| `Oa19_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00502847 | 900nm/10nm | Water vapor absorption/vegetation monitoring (max. reflectance) |
| `Oa20_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00326378 | 940nm/20nm | Water vapor absorption, atmospheric/aerosol correction |
| `Oa21_radiance` | W m^\-2 sr^\-1 µm^\-1 | 0\.00324118 | 1029nm/40nm | Atmospheric/aerosol correction |
| `quality_flags` | None |  | None | Quality flags |
| Bitmask for quality\_flags * Bit 0: Saturated at Oa21 	+ 0: The sample of Oa21 is not saturated 	+ 1: The sample of Oa21 is saturated * Bit 1: Saturated at Oa20 	+ 0: The sample of Oa20 is not saturated 	+ 1: The sample of Oa20 is saturated * Bit 2: Saturated at Oa19 	+ 0: The sample of Oa19 is not saturated 	+ 1: The sample of Oa19 is saturated * Bit 3: Saturated at Oa18 	+ 0: The sample of Oa18 is not saturated 	+ 1: The sample of Oa18 is saturated * Bit 4: Saturated at Oa17 	+ 0: The sample of Oa17 is not saturated 	+ 1: The sample of Oa17 is saturated * Bit 5: Saturated at Oa16 	+ 0: The sample of Oa16 is not saturated 	+ 1: The sample of Oa16 is saturated * Bit 6: Saturated at Oa15 	+ 0: The sample of Oa15 is not saturated 	+ 1: The sample of Oa15 is saturated * Bit 7: Saturated at Oa14 	+ 0: The sample of Oa14 is not saturated 	+ 1: The sample of Oa14 is saturated * Bit 8: Saturated at Oa13 	+ 0: The sample of Oa13 is not saturated 	+ 1: The sample of Oa13 is saturated * Bit 9: Saturated at Oa12 	+ 0: The sample of Oa12 is not saturated 	+ 1: The sample of Oa12 is saturated * Bit 10: Saturated at Oa11 	+ 0: The sample of Oa11 is not saturated 	+ 1: The sample of Oa11 is saturated * Bit 11: Saturated at Oa10 	+ 0: The sample of Oa10 is not saturated 	+ 1: The sample of Oa10 is saturated * Bit 12: Saturated at Oa09 	+ 0: The sample of Oa09 is not saturated 	+ 1: The sample of Oa09 is saturated * Bit 13: Saturated at Oa08 	+ 0: The sample of Oa08 is not saturated 	+ 1: The sample of Oa08 is saturated * Bit 14: Saturated at Oa07 	+ 0: The sample of Oa07 is not saturated 	+ 1: The sample of Oa07 is saturated * Bit 15: Saturated at Oa06 	+ 0: The sample of Oa06 is not saturated 	+ 1: The sample of Oa06 is saturated * Bit 16: Saturated at Oa05 	+ 0: The sample of Oa05 is not saturated 	+ 1: The sample of Oa05 is saturated * Bit 17: Saturated at Oa04 	+ 0: The sample of Oa04 is not saturated 	+ 1: The sample of Oa04 is saturated * Bit 18: Saturated at Oa03 	+ 0: The sample of Oa03 is not saturated 	+ 1: The sample of Oa03 is saturated * Bit 19: Saturated at Oa02 	+ 0: The sample of Oa02 is not saturated 	+ 1: The sample of Oa02 is saturated * Bit 20: Saturated at Oa01 	+ 0: The sample of Oa01 is not saturated 	+ 1: The sample of Oa01 is saturated * Bit 21: Dubious 	+ 0: Any pixel's sample is not contaminated 	by a neighbor saturated sample or the Instrument Source 	Packet it was extracted from is not corrupted 	+ 1: Any pixel's sample is potentially contaminated 	by a neighbor saturated sample or the Instrument Source 	Packet it was extracted from is corrupted * Bit 22: Sun\-glint risk 	+ 0: The viewing and wind conditions are such that 	the Sun may not cause glint to occur on pixels over water 	surfaces 	+ 1: The viewing and wind conditions are such that 	the Sun may cause glint to occur on pixels over water surfaces 	(this flag is set only on the basis of sun and viewing 	angles taking into account wind conditions, but it is not 	set according to radiometric data) * Bit 23: Duplicate 	+ 0: Pixel is not derived from the same instrument 	pixel as one of its neighbors during the re\-sampling process 	+ 1: Pixel is derived from the same instrument pixel 	as one of its neighbors during the re\-sampling process * Bit 24: Cosmetic 	+ 0: Pixel has not been filled with cosmetic values 	+ 1: Pixel has been filled with cosmetic values * Bit 25: Invalid 	+ 0: Pixel is valid 	+ 1: Pixel is invalid, i.e. its value is missing 	either because it is out of the instrument swath or because 	of missing or unusable Level 0 data * Bit 26: Straylight risk 	+ 0: Stray light correction (of the Ground Imager) quality is not degraded 	+ 1: Stray light correction (of the Ground Imager) 	quality is degraded because not enough neighbor pixels 	were available for its estimation * Bit 27: Bright 	+ 0: Pixel is not bright 	+ 1: Pixel is bright * Bit 28: Tidal region 	+ 0: Pixel is not over a tidal region 	+ 1: Pixel is over a tidal region * Bit 29: Fresh inland water 	+ 0: Pixel is not over fresh water, rivers, or lakes 	+ 1: Pixel is over fresh water, rivers, or lakes * Bit 30: Coastline 	+ 0: Pixel is not on coastline 	+ 1: Pixel is on coastline * Bit 31: Land 	+ 0: Pixel is over water 	+ 1: Pixel is over land | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| SNAP\_Graph\_Processing\_Framework\_GPF\_vers | STRING | Sentinel Application Platform (SNAP) version |
| SNAP\_Raster\_Operators\_vers | STRING | SNAP version |
| processing\_facility\_country | STRING | Name of the country where the facility is located. This element is configurable within the IPF. |
| processing\_facility\_name | STRING | Name of the facility where the processing step was performed. This element is configurable within the IPF. |
| processing\_facility\_organisation | STRING | Name of the organisation responsible for the facility. This element is configurable within the IPF. |
| processing\_facility\_site | STRING | Geographical location of the facility. This element is configurable within the IPF. |
| processing\_hardware | STRING | Name of the hardware in the facility used for the processing. |
| processing\_software\_name | STRING | Name of the software component. |
| processing\_software\_version | DOUBLE | The version or release identifier of the software |
| processing\_time | DOUBLE | The time the product was processed in 'epoch' format |
| product | STRING | This is always `OL_1_EFR__` |
| PRODUCT\_ID | STRING | The full id of the original Sentinel\-3 product |
| productQuality | STRING | PASSED or empty |
| cycle\_num | DOUBLE | The cycle number is the number of times the satellite passed over the same geographical point on the ground. In the SENTINEL\-3 operational phase (after launch and commissioning phases), the orbit cycle is 27 days. |
| orbitNumber | DOUBLE | The absolute orbit number considers the orbits elapsed since the first ascending node crossing after launch. |
| relative\_orbit\_num | DOUBLE | The relative orbit number is the orbit number within a cycle. Every time a cycle starts, the relative orbit number is reset to zero. |
| groundTrackDirection | STRING | Direction of the trace made by the sub\-satellite point on the surface of the Earth's reference ellipsoid due to the motion of the satellite along its orbit. |
| spacecraft | STRING | Sentinel\-3 spacecraft name: S3A, S3B |
| status | STRING | Status of the file |
| timeliness | STRING | Timeliness of processing being analysed |
| salineWaterPixelsPercent | DOUBLE | Pixel quality information |
| coastalPixelsPercent | DOUBLE | Pixel quality information |
| freshInlandWaterPixelsPercent | DOUBLE | Pixel quality information |
| tidalRegionPixelsPercent | DOUBLE | Pixel quality information |
| brightPixelsPercent | DOUBLE | Pixel quality information |
| invalidPixelsPercent | DOUBLE | Pixel quality information |
| cosmeticPixelsPercent | DOUBLE | Pixel quality information |
| duplicatedPixelsPercent | DOUBLE | Pixel quality information |
| dubiousSamplesPercent | DOUBLE | Pixel quality information |
| saturatedPixelsPercent | DOUBLE | Pixel quality information |




### Terms of Use


**Terms of Use**


The use of Sentinel data is governed by the [Copernicus
Sentinel Data Terms and Conditions.](https://sentinel.esa.int/documents/247904/690755/Sentinel_Data_Legal_Notice)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('COPERNICUS/S3/OLCI')
.filterDate('2018-04-01','2018-04-04');

// Select bands for visualization and apply band-specific scale factors.
varrgb=dataset.select(['Oa08_radiance','Oa06_radiance','Oa04_radiance'])
.median()
// Convert to radiance units.
.multiply(ee.Image([0.00876539,0.0123538,0.0115198]));

varvisParams={
min:0,
max:6,
gamma:1.5,
};

Map.setCenter(46.043,1.45,5);
Map.addLayer(rgb,visParams,'RGB');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S3_OLCI)


[Sentinel\-3 OLCI EFR: Ocean and Land Color Instrument Earth Observation Full Resolution](/earth-engine/datasets/catalog/COPERNICUS_S3_OLCI)

The Ocean and Land Color Instrument (OLCI) Earth Observation Full Resolution (EFR) dataset contains top of atmosphere radiances at 21 spectral bands with center wavelengths ranging between 0\.4µm and 1\.02µm at spatial resolution of 300m with worldwide coverage every \~2 days. OLCI is one of the instruments in the ESA/EUMETSAT …

 COPERNICUS/S3/OLCI,
 copernicus,esa,eu,radiance,satellite\-imagery,sentinel,toa

2016\-10\-18T19:25:42Z/2025\-07\-18T08:16:52Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








