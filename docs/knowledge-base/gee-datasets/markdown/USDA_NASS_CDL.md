



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

USDA NASS Cropland Data Layers


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================








Dataset Availability
1997\-01\-01T00:00:00Z–2024\-01\-01T00:00:00Z
Dataset Provider


[USDA National Agricultural Statistics Service](https://www.nass.usda.gov/Research_and_Science/Cropland/SARS1a.php)



Earth Engine Snippet


`ee.ImageCollection("USDA/NASS/CDL")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USDA/USDA_NASS_CDL)





Cadence
1 Year
Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[crop](/earth-engine/datasets/tags/crop)
[landcover](/earth-engine/datasets/tags/landcover)
[usda](/earth-engine/datasets/tags/usda)
cdl
nass








#### Description



The Cropland Data Layer (CDL) is a crop\-specific land cover data layer
created annually for the continental United States using moderate
resolution satellite imagery and extensive agricultural ground truth.
The CDL is created by the USDA, National Agricultural Statistics
Service (NASS), Research and Development Division, Geospatial
Information Branch, Spatial Analysis Research Section.


For detailed FAQ please visit [CropScape and Cropland Data
Layers \- FAQs](https://www.nass.usda.gov/Research_and_Science/Cropland/sarsfaqs2.php).


To explore details about the classification accuracies and utility of
the data, see
[state\-level omission and commission errors by crop type and year](https://www.nass.usda.gov/Research_and_Science/Cropland/metadata/meta.php).


The asset date is aligned with the calendar year of harvest. For most crops
the planted and harvest year are the same. Some exceptions: winter wheat is
unique, as it is planted in the prior year. A hay crop like alfalfa could
have been planted years prior.


For winter wheat the data also have a class called
"Double Crop Winter Wheat/Soybeans". Some mid\-latitude areas of the US have
conditions such that a second crop (usually soybeans) can be planted
immediately after the harvest of winter wheat and itself still be harvested
within the same year. So for mapping winter wheat areas use both classes
(use both values 24 and 26\).


While the CDL date is aligned with year of harvest, the map itself is
more representative of what was planted. In other words, a small percentage
of fields on a given year will not be harvested.


Some non\-agricultural categories are duplicate due to
[two very different epochs in methodology](https://www.google.com/url?sa=D&q=https%3A%2F%2Fwww.nass.usda.gov%2FResearch_and_Science%2FCropland%2F).


The non\-ag codes 63\-65 and 81\-88 are holdovers from the older
methodology and will only appear in CDLs from 2007 and earlier. The non\-ag
codes from 111\-195 are from the current methodology which uses the USGS NLCD
as non\-ag training and will only appear in CDLs 2007 and newer.


2007 was a transition year so there may be both sets of categories in the
2007 national product but will not appear within the same state.


**Note:** The 2024 CDL only has the data band. The cultivated and
confidence bands are yet to be released by the provider.



### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `cropland` | 1 | 254 | Main crop\-specific land cover classification. |
| `cultivated` | 1 | 2 | Classification layer for identifying cultivated and non\-cultivated land cover. Available from 2013 to 2023\. |
| `confidence` | 0 | 100 | Per\-pixel predicted confidence of the given classification, with 0 being the least confident and 100 the most confident. Available from 2008 to 2023 (Note: Confidence for Florida and Washington D.C. is unavailable for 2010\). |


**cropland Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#000000 | Background |
| 1 | \#ffd400 | Corn |
| 2 | \#ff2626 | Cotton |
| 3 | \#00a9e6 | Rice |
| 4 | \#ff9e0f | Sorghum |
| 5 | \#267300 | Soybeans |
| 6 | \#ffff00 | Sunflower |
| 10 | \#70a800 | Peanuts |
| 11 | \#00af4d | Tobacco |
| 12 | \#e0a60f | Sweet Corn |
| 13 | \#e0a60f | Pop or Orn Corn |
| 14 | \#80d4ff | Mint |
| 21 | \#e2007f | Barley |
| 22 | \#8a6453 | Durum Wheat |
| 23 | \#d9b56c | Spring Wheat |
| 24 | \#a87000 | Winter Wheat |
| 25 | \#d69dbc | Other Small Grains |
| 26 | \#737300 | Dbl Crop WinWht/Soybeans |
| 27 | \#ae017e | Rye |
| 28 | \#a15889 | Oats |
| 29 | \#73004c | Millet |
| 30 | \#d69dbc | Speltz |
| 31 | \#d1ff00 | Canola |
| 32 | \#8099ff | Flaxseed |
| 33 | \#d6d600 | Safflower |
| 34 | \#d1ff00 | Rape Seed |
| 35 | \#00af4d | Mustard |
| 36 | \#ffa8e3 | Alfalfa |
| 37 | \#a5f58d | Other Hay/Non Alfalfa |
| 38 | \#00af4d | Camelina |
| 39 | \#d69dbc | Buckwheat |
| 41 | \#a900e6 | Sugarbeets |
| 42 | \#a80000 | Dry Beans |
| 43 | \#732600 | Potatoes |
| 44 | \#00af4d | Other Crops |
| 45 | \#b380ff | Sugarcane |
| 46 | \#732600 | Sweet Potatoes |
| 47 | \#ff6666 | Misc Vegs \& Fruits |
| 48 | \#ff6666 | Watermelons |
| 49 | \#ffcc66 | Onions |
| 50 | \#ff6666 | Cucumbers |
| 51 | \#00af4d | Chick Peas |
| 52 | \#00deb0 | Lentils |
| 53 | \#55ff00 | Peas |
| 54 | \#f5a27a | Tomatoes |
| 55 | \#ff6666 | Caneberries |
| 56 | \#00af4d | Hops |
| 57 | \#80d4ff | Herbs |
| 58 | \#e8beff | Clover/Wildflowers |
| 59 | \#b2ffde | Sod/Grass Seed |
| 60 | \#00af4d | Switchgrass |
| 61 | \#bfbf7a | Fallow/Idle Cropland |
| 63 | \#95ce93 | Forest |
| 64 | \#c7d79e | Shrubland |
| 65 | \#ccbfa3 | Barren |
| 66 | \#ff00ff | Cherries |
| 67 | \#ff91ab | Peaches |
| 68 | \#b90050 | Apples |
| 69 | \#704489 | Grapes |
| 70 | \#007878 | Christmas Trees |
| 71 | \#b39c70 | Other Tree Crops |
| 72 | \#ffff80 | Citrus |
| 74 | \#b6705c | Pecans |
| 75 | \#00a884 | Almonds |
| 76 | \#ebd6b0 | Walnuts |
| 77 | \#b39c70 | Pears |
| 81 | \#f7f7f7 | Clouds/No Data |
| 82 | \#9c9c9c | Developed |
| 83 | \#4d70a3 | Water |
| 87 | \#80b3b3 | Wetlands |
| 88 | \#e9ffbe | Nonag/Undefined |
| 92 | \#00ffff | Aquaculture |
| 111 | \#4d70a3 | Open Water |
| 112 | \#d4e3fc | Perennial Ice/Snow |
| 121 | \#9c9c9c | Developed/Open Space |
| 122 | \#9c9c9c | Developed/Low Intensity |
| 123 | \#9c9c9c | Developed/Med Intensity |
| 124 | \#9c9c9c | Developed/High Intensity |
| 131 | \#ccbfa3 | Barren |
| 141 | \#95ce93 | Deciduous Forest |
| 142 | \#95ce93 | Evergreen Forest |
| 143 | \#95ce93 | Mixed Forest |
| 152 | \#c7d79e | Shrubland |
| 176 | \#e9ffbe | Grass/Pasture |
| 190 | \#80b3b3 | Woody Wetlands |
| 195 | \#80b3b3 | Herbaceous Wetlands |
| 204 | \#00ff8c | Pistachios |
| 205 | \#d69dbc | Triticale |
| 206 | \#ff6666 | Carrots |
| 207 | \#ff6666 | Asparagus |
| 208 | \#ff6666 | Garlic |
| 209 | \#ff6666 | Cantaloupes |
| 210 | \#ff91ab | Prunes |
| 211 | \#344a34 | Olives |
| 212 | \#e67525 | Oranges |
| 213 | \#ff6666 | Honeydew Melons |
| 214 | \#ff6666 | Broccoli |
| 215 | \#66994d | Avocados |
| 216 | \#ff6666 | Peppers |
| 217 | \#b39c70 | Pomegranates |
| 218 | \#ff91ab | Nectarines |
| 219 | \#ff6666 | Greens |
| 220 | \#ff91ab | Plums |
| 221 | \#ff6666 | Strawberries |
| 222 | \#ff6666 | Squash |
| 223 | \#ff91ab | Apricots |
| 224 | \#00af4d | Vetch |
| 225 | \#ffd400 | Dbl Crop WinWht/Corn |
| 226 | \#ffd400 | Dbl Crop Oats/Corn |
| 227 | \#ff6666 | Lettuce |
| 228 | \#ffd400 | Dbl Crop Triticale/Corn |
| 229 | \#ff6666 | Pumpkins |
| 230 | \#8a6453 | Dbl Crop Lettuce/Durum Wht |
| 231 | \#ff6666 | Dbl Crop Lettuce/Cantaloupe |
| 232 | \#ff2626 | Dbl Crop Lettuce/Cotton |
| 233 | \#e2007f | Dbl Crop Lettuce/Barley |
| 234 | \#ff9e0f | Dbl Crop Durum Wht/Sorghum |
| 235 | \#ff9e0f | Dbl Crop Barley/Sorghum |
| 236 | \#a87000 | Dbl Crop WinWht/Sorghum |
| 237 | \#ffd400 | Dbl Crop Barley/Corn |
| 238 | \#a87000 | Dbl Crop WinWht/Cotton |
| 239 | \#267300 | Dbl Crop Soybeans/Cotton |
| 240 | \#267300 | Dbl Crop Soybeans/Oats |
| 241 | \#ffd400 | Dbl Crop Corn/Soybeans |
| 242 | \#000099 | Blueberries |
| 243 | \#ff6666 | Cabbage |
| 244 | \#ff6666 | Cauliflower |
| 245 | \#ff6666 | Celery |
| 246 | \#ff6666 | Radishes |
| 247 | \#ff6666 | Turnips |
| 248 | \#ff6666 | Eggplants |
| 249 | \#ff6666 | Gourds |
| 250 | \#ff6666 | Cranberries |
| 254 | \#267300 | Dbl Crop Barley/Soybeans |


**cultivated Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 1 | \#d3d3d3 | Non\-cultivated |
| 2 | \#b1b58c | Cultivated |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| cropland\_class\_names | STRING\_LIST | Array of cropland landcover classification names. |
| cropland\_class\_palette | STRING\_LIST | Array of hex code color strings used for the classification palette. |
| cropland\_class\_values | INT\_LIST | Value of the land cover classification. |
| cultivated\_class\_names | STRING\_LIST | Array of cropland landcover classification names. |
| cultivated\_class\_palette | STRING\_LIST | Array of hex code color strings used for the classification palette. |
| cultivated\_class\_values | INT\_LIST | Value of the land cover classification. |




### Terms of Use


**Terms of Use**


The NASS Cropland Data Layer has no copyright restrictions. The CDL is
considered public domain and free to redistribute. However, NASS would
appreciate acknowledgment for the usage of our CDL product.




### Citations



Citations:
* USDA National Agricultural Statistics Service Cropland Data Layer. {YEAR}.
Published crop\-specific data layer \[Online]. Available at
<https://nassgeodata.gmu.edu/CropScape/>
(accessed {DATE}; verified {DATE}). USDA\-NASS, Washington, DC.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('USDA/NASS/CDL')
.filter(ee.Filter.date('2018-01-01','2019-12-31'))
.first();
varcropLandcover=dataset.select('cropland');
Map.setCenter(-100.55,40.71,4);
Map.addLayer(cropLandcover,{},'Crop Landcover');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USDA/USDA_NASS_CDL)


[USDA NASS Cropland Data Layers](/earth-engine/datasets/catalog/USDA_NASS_CDL)

The Cropland Data Layer (CDL) is a crop\-specific land cover data layer created annually for the continental United States using moderate resolution satellite imagery and extensive agricultural ground truth. The CDL is created by the USDA, National Agricultural Statistics Service (NASS), Research and Development Division, Geospatial Information Branch, Spatial Analysis …

 USDA/NASS/CDL,
 agriculture,crop,landcover,usda

1997\-01\-01T00:00:00Z/2024\-01\-01T00:00:00Z



 24 \-127 51 \-65
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








