



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenLandMap USDA Soil Taxonomy Great Groups


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================








Dataset Availability
1950\-01\-01T00:00:00Z–2018\-01\-01T00:00:00Z
Dataset Provider


[EnvirometriX Ltd](https://doi.org/10.5281/zenodo.1476844)



Earth Engine Snippet


`ee.Image("OpenLandMap/SOL/SOL_GRTGROUP_USDA-SOILTAX_C/v01")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_GRTGROUP_USDA-SOILTAX_C_v01)





Tags


[envirometrix](/earth-engine/datasets/tags/envirometrix)
[opengeohub](/earth-engine/datasets/tags/opengeohub)
[openlandmap](/earth-engine/datasets/tags/openlandmap)
[soil](/earth-engine/datasets/tags/soil)
[usda](/earth-engine/datasets/tags/usda)
taxonomy








#### Description



Predicted USDA soil great group probabilities at 250m.


Distribution of the USDA soil great groups based on machine learning predictions
from global compilation of soil profiles. To learn more about soil great groups
please refer to the [Illustrated Guide to Soil Taxonomy \- NRCS \- USDA](https://www.nrcs.usda.gov/wps/PA_NRCSConsumption/download/?cid=stelprdb1247203.pdf).


* Processing steps are described in detail [here](https://gitlab.com/openlandmap/global-layers/tree/master/soil)
* Antarctica is not included.


To access and visualize maps outside of Earth Engine, use [this page](https://opengeohub.org/about-openlandmap).


If you discover a bug, artifact or inconsistency in the LandGIS maps
or if you have a question please use the following channels:


* [Technical issues and questions about the code](https://gitlab.com/openlandmap/global-layers/issues)
* [General questions and comments](https://disqus.com/home/forums/landgis/)





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Description |
| --- | --- |
| `grtgroup` | USDA soil taxonomy great groups |


**grtgroup Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#ffffff | NODATA |
| 1 | \#adff2d | Albaqualfs |
| 2 | \#adff22 | Cryaqualfs |
| 4 | \#a5ff2f | Durixeralfs |
| 6 | \#87ff37 | Endoaqualfs |
| 7 | \#baf019 | Epiaqualfs |
| 9 | \#87ff19 | Fragiaqualfs |
| 10 | \#96f03d | Fragiudalfs |
| 11 | \#a3f52f | Fragixeralfs |
| 12 | \#aff319 | Fraglossudalfs |
| 13 | \#91ff37 | Glossaqualfs |
| 14 | \#9cf319 | Glossocryalfs |
| 15 | \#9bff37 | Glossudalfs |
| 16 | \#91ff19 | Haplocryalfs |
| 17 | \#71ff37 | Haploxeralfs |
| 18 | \#86ff19 | Hapludalfs |
| 19 | \#a9d42d | Haplustalfs |
| 25 | \#aff519 | Natraqualfs |
| 26 | \#9bff19 | Natrixeralfs |
| 27 | \#9af024 | Natrudalfs |
| 28 | \#a5fd2f | Natrustalfs |
| 29 | \#88ff37 | Palecryalfs |
| 30 | \#afed19 | Paleudalfs |
| 31 | \#71ff19 | Paleustalfs |
| 32 | \#aff026 | Palexeralfs |
| 38 | \#8cf537 | Rhodustalfs |
| 39 | \#b7ff19 | Vermaqualfs |
| 41 | \#7177c0 | Eutroboralfs |
| 42 | \#9a85ec | Ochraqualfs |
| 43 | \#f5f5e1 | Glossoboralfs |
| 44 | \#52cf5a | Cryoboralfs |
| 45 | \#e42777 | Natriboralfs |
| 46 | \#4ef76d | Paleboralfs |
| 50 | \#ff00fb | Cryaquands |
| 58 | \#eb05eb | Fulvicryands |
| 59 | \#fa04fa | Fulvudands |
| 61 | \#fc04f5 | Haplocryands |
| 63 | \#f50df0 | Haploxerands |
| 64 | \#f118f1 | Hapludands |
| 74 | \#fa0cfa | Udivitrands |
| 75 | \#fc05e1 | Ustivitrands |
| 76 | \#f100d5 | Vitraquands |
| 77 | \#eb09e6 | Vitricryands |
| 80 | \#fa22fa | Vitrixerands |
| 82 | \#ffdab9 | Aquicambids |
| 83 | \#f5d2bb | Aquisalids |
| 85 | \#e8c9b8 | Argidurids |
| 86 | \#ffddc4 | Argigypsids |
| 87 | \#e7cbc0 | Calciargids |
| 89 | \#ffd2c3 | Calcigypsids |
| 90 | \#f5d6bb | Gypsiargids |
| 92 | \#d5d3b9 | Haplargids |
| 93 | \#e8d4b8 | Haplocalcids |
| 94 | \#e7cdc0 | Haplocambids |
| 96 | \#f3eac8 | Haplodurids |
| 97 | \#a0c4ba | Haplogypsids |
| 98 | \#ffd2b9 | Haplosalids |
| 99 | \#f5dabb | Natrargids |
| 100 | \#f5d5b9 | Natridurids |
| 101 | \#e8ebb8 | Natrigypsids |
| 102 | \#ffddc2 | Paleargids |
| 103 | \#e7ffc0 | Petroargids |
| 104 | \#f3e6c8 | Petrocalcids |
| 105 | \#ffdab9 | Petrocambids |
| 107 | \#f5cdb9 | Petrogypsids |
| 110 | \#a91d30 | Calciorthids |
| 111 | \#796578 | Camborthids |
| 112 | \#d8ff6e | Paleorthids |
| 113 | \#177548 | Durorthids |
| 114 | \#43efd6 | Durargids |
| 115 | \#8496a9 | Gypsiorthids |
| 116 | \#296819 | Nadurargids |
| 118 | \#73ffd4 | Cryaquents |
| 119 | \#6fffc8 | Cryofluvents |
| 120 | \#75fbc9 | Cryopsamments |
| 121 | \#86f5d1 | Cryorthents |
| 122 | \#82ffd2 | Endoaquents |
| 123 | \#88eec8 | Epiaquents |
| 124 | \#80ffd4 | Fluvaquents |
| 126 | \#6bffc9 | Frasiwassents |
| 131 | \#88eec8 | Hydraquents |
| 133 | \#7fffc8 | Psammaquents |
| 134 | \#81ffd2 | Psammowassents |
| 135 | \#86f0d4 | Quartzipsamments |
| 136 | \#67ffc8 | Sulfaquents |
| 137 | \#88eec8 | Sulfiwassents |
| 138 | \#7ffbcb | Torrifluvents |
| 139 | \#87ffd2 | Torriorthents |
| 140 | \#8af5ce | Torripsamments |
| 141 | \#6bfad2 | Udifluvents |
| 142 | \#78f0d4 | Udipsamments |
| 143 | \#88eec8 | Udorthents |
| 144 | \#7ffbd4 | Ustifluvents |
| 145 | \#73f5cd | Ustipsamments |
| 146 | \#88c8d2 | Ustorthents |
| 147 | \#91f0cd | Xerofluvents |
| 148 | \#73cdd2 | Xeropsamments |
| 149 | \#88eec8 | Xerorthents |
| 153 | \#fb849b | Udarents |
| 154 | \#dd4479 | Torriarents |
| 155 | \#61388b | Xerarents |
| 179 | \#a52a30 | Cryofibrists |
| 180 | \#722328 | Cryofolists |
| 181 | \#d81419 | Cryohemists |
| 182 | \#a42828 | Cryosaprists |
| 183 | \#82f5cd | Frasiwassists |
| 184 | \#a54c2e | Haplofibrists |
| 185 | \#c11919 | Haplohemists |
| 186 | \#b91419 | Haplosaprists |
| 189 | \#21b199 | Sphagnofibrists |
| 190 | \#702028 | Sulfihemists |
| 191 | \#b41919 | Sulfisaprists |
| 196 | \#b22328 | Udifolists |
| 201 | \#a2c7eb | Borosaprists |
| 202 | \#36ba79 | Medisaprists |
| 203 | \#806797 | Borohemists |
| 206 | \#cb5b5f | Calcicryepts |
| 207 | \#cd5c5c | Calciustepts |
| 208 | \#d94335 | Calcixerepts |
| 209 | \#d35740 | Cryaquepts |
| 210 | \#e05a5d | Durixerepts |
| 212 | \#cf5b5c | Durustepts |
| 213 | \#ca5964 | Dystrocryepts |
| 215 | \#ca5d5f | Dystroxerepts |
| 216 | \#cd5e5a | Dystrudepts |
| 217 | \#ca5969 | Dystrustepts |
| 218 | \#d95a35 | Endoaquepts |
| 219 | \#d36240 | Epiaquepts |
| 220 | \#e05c43 | Eutrudepts |
| 221 | \#d64755 | Fragiaquepts |
| 222 | \#cf595c | Fragiudepts |
| 225 | \#ff5f5f | Halaquepts |
| 226 | \#cd6058 | Haplocryepts |
| 228 | \#d95f35 | Haploxerepts |
| 229 | \#d35140 | Haplustepts |
| 230 | \#d65a55 | Humaquepts |
| 231 | \#e05c59 | Humicryepts |
| 233 | \#cf525e | Humixerepts |
| 234 | \#c65978 | Humudepts |
| 235 | \#f5615f | Humustepts |
| 245 | \#826f9a | Ustochrepts |
| 246 | \#cff41a | Eutrochrepts |
| 247 | \#4a6f31 | Dystrochrepts |
| 248 | \#a96989 | Eutrocryepts |
| 249 | \#e16438 | Haplaquepts |
| 250 | \#24f640 | Xerochrepts |
| 251 | \#88c1f9 | Cryochrepts |
| 252 | \#f5d25c | Fragiochrepts |
| 253 | \#d74322 | Haplumbrepts |
| 254 | \#7f939e | Cryumbrepts |
| 255 | \#41a545 | Dystropepts |
| 256 | \#8f8340 | Vitrandepts |
| 268 | \#09fe03 | Argialbolls |
| 269 | \#0aff00 | Argiaquolls |
| 270 | \#0ff30f | Argicryolls |
| 271 | \#02f00a | Argiudolls |
| 272 | \#0fc903 | Argiustolls |
| 273 | \#17f000 | Argixerolls |
| 274 | \#0cff00 | Calciaquolls |
| 275 | \#0ac814 | Calcicryolls |
| 276 | \#0cfe00 | Calciudolls |
| 277 | \#0aff0a | Calciustolls |
| 278 | \#03ff05 | Calcixerolls |
| 279 | \#1cf31c | Cryaquolls |
| 280 | \#24f000 | Cryrendolls |
| 283 | \#00ff0c | Durixerolls |
| 284 | \#14c814 | Durustolls |
| 285 | \#00fe4c | Endoaquolls |
| 286 | \#14ff96 | Epiaquolls |
| 287 | \#44d205 | Haplocryolls |
| 289 | \#05f305 | Haploxerolls |
| 290 | \#62f00a | Hapludolls |
| 291 | \#0fcd03 | Haplustolls |
| 292 | \#00d20f | Haprendolls |
| 294 | \#1add11 | Natraquolls |
| 296 | \#09ff0c | Natrixerolls |
| 297 | \#03ff05 | Natrudolls |
| 298 | \#05e700 | Natrustolls |
| 299 | \#02f00a | Palecryolls |
| 300 | \#0fea03 | Paleudolls |
| 301 | \#00f000 | Paleustolls |
| 302 | \#0ccb0c | Palexerolls |
| 303 | \#14dd14 | Vermudolls |
| 306 | \#6a685d | Haploborolls |
| 307 | \#fae6b9 | Argiborolls |
| 308 | \#769a34 | Haplaquolls |
| 309 | \#6ff2df | Cryoborolls |
| 310 | \#ca7fc6 | Natriborolls |
| 311 | \#d8228f | Calciborolls |
| 312 | \#c01bf0 | Paleborolls |
| 342 | \#d2bad3 | Alaquods |
| 343 | \#d8c3cb | Alorthods |
| 345 | \#d4c6d4 | Duraquods |
| 348 | \#d5bed5 | Durorthods |
| 349 | \#ddb9dd | Endoaquods |
| 350 | \#d8d2d8 | Epiaquods |
| 351 | \#d4c9d4 | Fragiaquods |
| 353 | \#d2bad5 | Fragiorthods |
| 354 | \#d5bad5 | Haplocryods |
| 356 | \#d5b2d5 | Haplohumods |
| 357 | \#d8c8d2 | Haplorthods |
| 358 | \#d4cbd4 | Humicryods |
| 367 | \#552638 | Haplaquods |
| 368 | \#2571eb | Cryorthods |
| 370 | \#ffa514 | Albaquults |
| 371 | \#f3a502 | Endoaquults |
| 372 | \#fb7b00 | Epiaquults |
| 373 | \#f0b405 | Fragiaquults |
| 374 | \#f7a80f | Fragiudults |
| 375 | \#fb9113 | Haplohumults |
| 376 | \#ffa519 | Haploxerults |
| 377 | \#f3a702 | Hapludults |
| 378 | \#fbba07 | Haplustults |
| 381 | \#f7970f | Kandiudults |
| 385 | \#f3a702 | Kanhapludults |
| 387 | \#fb5a00 | Paleaquults |
| 388 | \#f0c005 | Palehumults |
| 389 | \#f7810f | Paleudults |
| 390 | \#ff9c00 | Paleustults |
| 391 | \#f3b002 | Palexerults |
| 396 | \#f0b005 | Rhodudults |
| 399 | \#f7980f | Umbraquults |
| 401 | \#4d7cfc | Ochraquults |
| 403 | \#ffff00 | Calciaquerts |
| 405 | \#fafa05 | Calciusterts |
| 406 | \#ebeb22 | Calcixererts |
| 409 | \#ffff14 | Dystraquerts |
| 410 | \#f1f10a | Dystruderts |
| 412 | \#fafa05 | Endoaquerts |
| 413 | \#ebeb1e | Epiaquerts |
| 414 | \#f5eb0c | Gypsitorrerts |
| 415 | \#eef506 | Gypsiusterts |
| 417 | \#f1f129 | Haplotorrerts |
| 418 | \#fafa05 | Haploxererts |
| 419 | \#ebeb0c | Hapluderts |
| 420 | \#f5d202 | Haplusterts |
| 422 | \#ffd700 | Natraquerts |
| 424 | \#f1f12b | Salitorrerts |
| 429 | \#a91fac | Chromusterts |
| 430 | \#2da468 | Pellusterts |
| 431 | \#9a8b71 | Chromoxererts |
| 432 | \#76b989 | Pelluderts |
| 433 | \#713959 | Torrerts |




### Terms of Use


**Terms of Use**


[CC\-BY\-SA\-4\.0](https://spdx.org/licenses/CC-BY-SA-4.0.html)




### Citations



Citations:
* Tomislav Hengl, \& Travis Nauman. (2018\). Predicted USDA soil great groups at
250 m (probabilities) (Version v01\) \[Data set]. Zenodo.
[10\.5281/zenodo.1476844](https://doi.org/10.5281/zenodo.1476844)





### DOIs


* [https://doi.org/10\.5281/zenodo.1476844](https://doi.org/10.5281/zenodo.1476844)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('OpenLandMap/SOL/SOL_GRTGROUP_USDA-SOILTAX_C/v01');

varvisualization={
bands:['grtgroup'],
min:0,
max:433,
palette:[
'ffffff','adff2d','adff22','a5ff2f','87ff37','baf019',
'87ff19','96f03d','a3f52f','aff319','91ff37','9cf319',
'9bff37','91ff19','71ff37','86ff19','a9d42d','aff519',
'9bff19','9af024','a5fd2f','88ff37','afed19','71ff19',
'aff026','8cf537','b7ff19','7177c0','9a85ec','f5f5e1',
'52cf5a','e42777','4ef76d','ff00fb','eb05eb','fa04fa',
'fc04f5','f50df0','f118f1','fa0cfa','fc05e1','f100d5',
'eb09e6','fa22fa','ffdab9','f5d2bb','e8c9b8','ffddc4',
'e7cbc0','ffd2c3','f5d6bb','d5d3b9','e8d4b8','e7cdc0',
'f3eac8','a0c4ba','ffd2b9','f5dabb','f5d5b9','e8ebb8',
'ffddc2','e7ffc0','f3e6c8','ffdab9','f5cdb9','a91d30',
'796578','d8ff6e','177548','43efd6','8496a9','296819',
'73ffd4','6fffc8','75fbc9','86f5d1','82ffd2','88eec8',
'80ffd4','6bffc9','88eec8','7fffc8','81ffd2','86f0d4',
'67ffc8','88eec8','7ffbcb','87ffd2','8af5ce','6bfad2',
'78f0d4','88eec8','7ffbd4','73f5cd','88c8d2','91f0cd',
'73cdd2','88eec8','fb849b','dd4479','61388b','a52a30',
'722328','d81419','a42828','82f5cd','a54c2e','c11919',
'b91419','21b199','702028','b41919','b22328','a2c7eb',
'36ba79','806797','cb5b5f','cd5c5c','d94335','d35740',
'e05a5d','cf5b5c','ca5964','ca5d5f','cd5e5a','ca5969',
'd95a35','d36240','e05c43','d64755','cf595c','ff5f5f',
'cd6058','d95f35','d35140','d65a55','e05c59','cf525e',
'c65978','f5615f','826f9a','cff41a','4a6f31','a96989',
'e16438','24f640','88c1f9','f5d25c','d74322','7f939e',
'41a545','8f8340','09fe03','0aff00','0ff30f','02f00a',
'0fc903','17f000','0cff00','0ac814','0cfe00','0aff0a',
'03ff05','1cf31c','24f000','00ff0c','14c814','00fe4c',
'14ff96','44d205','05f305','62f00a','0fcd03','00d20f',
'1add11','09ff0c','03ff05','05e700','02f00a','0fea03',
'00f000','0ccb0c','14dd14','6a685d','fae6b9','769a34',
'6ff2df','ca7fc6','d8228f','c01bf0','d2bad3','d8c3cb',
'd4c6d4','d5bed5','ddb9dd','d8d2d8','d4c9d4','d2bad5',
'd5bad5','d5b2d5','d8c8d2','d4cbd4','552638','2571eb',
'ffa514','f3a502','fb7b00','f0b405','f7a80f','fb9113',
'ffa519','f3a702','fbba07','f7970f','f3a702','fb5a00',
'f0c005','f7810f','ff9c00','f3b002','f0b005','f7980f',
'4d7cfc','ffff00','fafa05','ebeb22','ffff14','f1f10a',
'fafa05','ebeb1e','f5eb0c','eef506','f1f129','fafa05',
'ebeb0c','f5d202','ffd700','f1f12b','a91fac','2da468',
'9a8b71','76b989','713959',
]
};

Map.centerObject(dataset);

Map.addLayer(dataset,visualization,'USDA soil taxonomy great groups');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenLandMap/OpenLandMap_SOL_SOL_GRTGROUP_USDA-SOILTAX_C_v01)


[OpenLandMap USDA Soil Taxonomy Great Groups](/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_GRTGROUP_USDA-SOILTAX_C_v01)

Predicted USDA soil great group probabilities at 250m. Distribution of the USDA soil great groups based on machine learning predictions from global compilation of soil profiles. To learn more about soil great groups please refer to the Illustrated Guide to Soil Taxonomy \- NRCS \- USDA. Processing steps are described …

 OpenLandMap/SOL/SOL\_GRTGROUP\_USDA\-SOILTAX\_C/v01,
 envirometrix,opengeohub,openlandmap,soil,usda

1950\-01\-01T00:00:00Z/2018\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.1476844](https://doi.org/https://doi.org/10.5281/zenodo.1476844)
* [https://doi.org/10\.5281/zenodo.1476844](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenLandMap_SOL_SOL_GRTGROUP_USDA-SOILTAX_C_v01)









