



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GCOM\-C/SGLI L3 Chlorophyll\-a Concentration (V3\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================








Dataset Availability
2021\-11\-29T00:00:00Z–2025\-07\-14T00:00:00Z
Dataset Provider


[Global Change Observation Mission (GCOM)](https://suzaku.eorc.jaxa.jp/GCOM/index.html)



Earth Engine Snippet


`ee.ImageCollection("JAXA/GCOM-C/L3/OCEAN/CHLA/V3")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_GCOM-C_L3_OCEAN_CHLA_V3)





Cadence
1 Day
Tags


[chla](/earth-engine/datasets/tags/chla)
[chlorophyll\-a](/earth-engine/datasets/tags/chlorophyll-a)
[g\-portal](/earth-engine/datasets/tags/g-portal)
[gcom](/earth-engine/datasets/tags/gcom)
[gcom\-c](/earth-engine/datasets/tags/gcom-c)
[jaxa](/earth-engine/datasets/tags/jaxa)
[ocean](/earth-engine/datasets/tags/ocean)
[ocean\-color](/earth-engine/datasets/tags/ocean-color)
[oceans](/earth-engine/datasets/tags/oceans)








#### Description



This product is the concentration of the photosynthetic pigment (chlorophyll\-a) in phytoplankton
in the sea surface layer.


This is an ongoing dataset with a latency of 3\-4 days.


GCOM\-C conducts long\-term and continuous global observation and data collection to elucidate the
mechanism behind fluctuations in radiation budget and carbon cycle needed to make accurate
projections regarding future temperature rise. At the same time, cooperating with research
institutions having a climate numerical model, it contributes to reduction of errors in
temperature rise prediction derived from the climate numerical model and improvement of accuracy
of prediction of various environmental changes. SGLI mounted on GCOM\-C is the succession sensor
of the Global Imager (GLI) mounted on ADEOS\-II (MIDORI II) and is the Imaging Radiometer which
measures the radiation from near\-ultraviolet to thermal infrared region (380 nm\-12 um) in 19
channels. Global observation of once for approximately every two days is possible at
mid\-latitude near Japan by observation width at ground greater than 1,000 km. In addition, SGLI
realizes high resolution than the similar global sensor and has a polarized observation function
and a multi\-angle observation function.





### Bands



**Pixel Size**
  
4638\.3 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `CHLA_AVE` | mg/m^3 | 0\* | 4000\* | Concentration of the green pigment (chlorophyll\-a) in phytoplankton in sea surface layer. |
| `CHLA_QA_flag` | None | CHLA QA |
| Bitmask for CHLA\_QA\_flag * Bits 0\-1: Terrain type 	+ 0: water (land fraction \= 0%) 	+ 1: mostly water (0% \< land fraction \< 50%) 	+ 2: mostly coastal (50% \< land fraction \< 100%) 	+ 3: land (land fraction \= 100%) | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| ALGORITHM\_VERSION | STRING | Algorithm version |
| GRID\_INTERVAL | STRING | Spatial resolution |
| GRID\_INTERVAL\_UNIT | STRING | Unit of GRID\_INTERVAL |
| IMAGE\_END\_TIME | STRING | Image acquisition end time |
| IMAGE\_START\_TIME | STRING | Image acquisition start time |
| PROCESSING\_RESULT | STRING | Good, Fair, Poor, NG |
| PROCESSING\_UT | STRING | Processing time |
| PRODUCT\_FILENAME | STRING | Source filename |
| PRODUCT\_VERSION | STRING | Product version |
| SATELLITE\_DIRECTION | STRING | Satellite orbit direction* A: Nighttime data * D: Daytime data |
| CHLA\_AVE\_OFFSET | STRING | Offset |
| CHLA\_AVE\_SLOPE | STRING | Slope |




### Terms of Use


**Terms of Use**


This dataset is free to use without any restrictions (including commercial use). Anyone wishing
to publish analyzed results or value added data products should properly credit the original
G\-Portal data, e.g., "PR data by Japan Aerospace Exploration Agency". For value added data
products, please indicate the credit of the original G\-Portal data, e.g., "Original data for
this value added data product was provided by Japan Aerospace Exploration Agency."


See [G\-Portal's terms of service (Article 7\)](https://gportal.jaxa.jp/gpr/index/eula?lang=en)
for additional information.




### Citations



Citations:
* Murakami, H. (Jan. 2020\). ATBD of GCOM\-C chlorophyll\-a concentration algorithm (Version 2\).
Retrieved from <https://suzaku.eorc.jaxa.jp/GCOM_C/data/ATBD/ver2/V2ATBD_O3AB_Chla_Murakami.pdf>





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('JAXA/GCOM-C/L3/OCEAN/CHLA/V3')
.filterDate('2021-12-01','2022-01-01')
// filter to daytime data only
.filter(ee.Filter.eq('SATELLITE_DIRECTION','D'));

// Multiply with slope coefficient
varimage=dataset.mean().multiply(0.0016).log10();

varvis={
bands:['CHLA_AVE'],
min:-2,
max:2,
palette:[
'3500a8','0800ba','003fd6',
'00aca9','77f800','ff8800',
'b30000','920000','880000'
]
};

Map.addLayer(image,vis,'Chlorophyll-a concentration');

Map.setCenter(128.45,33.33,5);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JAXA/JAXA_GCOM-C_L3_OCEAN_CHLA_V3)


[GCOM\-C/SGLI L3 Chlorophyll\-a Concentration (V3\)](/earth-engine/datasets/catalog/JAXA_GCOM-C_L3_OCEAN_CHLA_V3)

This product is the concentration of the photosynthetic pigment (chlorophyll\-a) in phytoplankton in the sea surface layer. This is an ongoing dataset with a latency of 3\-4 days. GCOM\-C conducts long\-term and continuous global observation and data collection to elucidate the mechanism behind fluctuations in radiation budget and carbon cycle …

 JAXA/GCOM\-C/L3/OCEAN/CHLA/V3,
 chla,chlorophyll\-a,g\-portal,gcom,gcom\-c,jaxa,ocean,ocean\-color,oceans

2021\-11\-29T00:00:00Z/2025\-07\-14T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








