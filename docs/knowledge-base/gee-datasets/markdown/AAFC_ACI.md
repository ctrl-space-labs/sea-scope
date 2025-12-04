



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Canada AAFC Annual Crop Inventory


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================








Dataset Availability
2009\-01\-01T00:00:00Z–2023\-01\-01T00:00:00Z
Dataset Provider


[Agriculture and Agri\-Food Canada](https://open.canada.ca/data/en/dataset/ba2645d5-4458-414d-b196-6303ac06c1c9)



Earth Engine Snippet


`ee.ImageCollection("AAFC/ACI")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/AAFC/AAFC_ACI)





Cadence
1 Year
Tags


[agriculture](/earth-engine/datasets/tags/agriculture)
[canada](/earth-engine/datasets/tags/canada)
[crop](/earth-engine/datasets/tags/crop)
[landcover](/earth-engine/datasets/tags/landcover)
aafc








#### Description



Starting in 2009, the Earth Observation Team of the Science and Technology
Branch (STB) at Agriculture and Agri\-Food Canada (AAFC) began the process
of generating annual crop type digital maps. Focusing on the Prairie
Provinces in 2009 and 2010, a Decision Tree (DT) based methodology was
applied using optical (Landsat\-5, AWiFS, DMC) and radar (Radarsat\-2\) based
satellite images. Beginning with the 2011 growing season, this activity has
been extended to other provinces in support of a national crop inventory.
To date this approach can consistently deliver a crop inventory that meets
the overall target accuracy of at least 85% at a final spatial resolution of
30m (56m in 2009 and 2010\).





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `landcover` | 1 | 255 | Main crop\-specific land cover classification. |


**landcover Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 10 | \#000000 | Cloud |
| 20 | \#3333ff | Water |
| 30 | \#996666 | Exposed Land and Barren |
| 34 | \#cc6699 | Urban and Developed |
| 35 | \#e1e1e1 | Greenhouses |
| 50 | \#ffff00 | Shrubland |
| 80 | \#993399 | Wetland |
| 85 | \#501b50 | Peatland |
| 110 | \#cccc00 | Grassland |
| 120 | \#cc6600 | Agriculture (undifferentiated) |
| 122 | \#ffcc33 | Pasture and Forages |
| 130 | \#7899f6 | Too Wet to be Seeded |
| 131 | \#ff9900 | Fallow |
| 132 | \#660000 | Cereals |
| 133 | \#dae31d | Barley |
| 134 | \#d6cc00 | Other Grains |
| 135 | \#d2db25 | Millet |
| 136 | \#d1d52b | Oats |
| 137 | \#cace32 | Rye |
| 138 | \#c3c63a | Spelt |
| 139 | \#b9bc44 | Triticale |
| 140 | \#a7b34d | Wheat |
| 141 | \#b9c64e | Switchgrass |
| 142 | \#999900 | Sorghum |
| 143 | \#e9e2b1 | Quinoa |
| 145 | \#92a55b | Winter Wheat |
| 146 | \#809769 | Spring Wheat |
| 147 | \#ffff99 | Corn |
| 148 | \#98887c | Tobacco |
| 149 | \#799b93 | Ginseng |
| 150 | \#5ea263 | Oilseeds |
| 151 | \#52ae77 | Borage |
| 152 | \#41bf7a | Camelina |
| 153 | \#d6ff70 | Canola and Rapeseed |
| 154 | \#8c8cff | Flaxseed |
| 155 | \#d6cc00 | Mustard |
| 156 | \#ff7f00 | Safflower |
| 157 | \#315491 | Sunflower |
| 158 | \#cc9933 | Soybeans |
| 160 | \#896e43 | Pulses |
| 161 | \#996633 | Other Pulses |
| 162 | \#8f6c3d | Peas |
| 163 | \#b6a472 | Chickpeas |
| 167 | \#82654a | Beans |
| 168 | \#a39069 | Fababeans |
| 174 | \#b85900 | Lentils |
| 175 | \#b74b15 | Vegetables |
| 176 | \#ff8a8a | Tomatoes |
| 177 | \#ffcccc | Potatoes |
| 178 | \#6f55ca | Sugarbeets |
| 179 | \#ffccff | Other Vegetables |
| 180 | \#dc5424 | Fruits |
| 181 | \#d05a30 | Berries |
| 182 | \#d20000 | Blueberry |
| 183 | \#cc0000 | Cranberry |
| 185 | \#dc3200 | Other Berry |
| 188 | \#ff6666 | Orchards |
| 189 | \#c5453b | Other Fruits |
| 190 | \#7442bd | Vineyards |
| 191 | \#ffcccc | Hops |
| 192 | \#b5fb05 | Sod |
| 193 | \#ccff05 | Herbs |
| 194 | \#07f98c | Nursery |
| 195 | \#00ffcc | Buckwheat |
| 196 | \#cc33cc | Canaryseed |
| 197 | \#8e7672 | Hemp |
| 198 | \#b1954f | Vetch |
| 199 | \#749a66 | Other Crops |
| 200 | \#009900 | Forest (undifferentiated) |
| 210 | \#006600 | Coniferous |
| 220 | \#00cc00 | Broadleaf |
| 230 | \#cc9900 | Mixedwood |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| landcover\_class\_names | STRING\_LIST | Array of cropland landcover classification names. |
| landcover\_class\_palette | STRING\_LIST | Array of hex code color strings used for the classification palette. |
| landcover\_class\_values | INT\_LIST | Value of the land cover classification. |




### Terms of Use


**Terms of Use**


[OGL\-Canada\-2\.0](https://spdx.org/licenses/OGL-Canada-2.0.html)




### Citations



Citations:
* Agriculture and Agri\-Food Canada Annual Crop Inventory. {YEAR}





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('AAFC/ACI');
varcrop2016=dataset
.filter(ee.Filter.date('2016-01-01','2016-12-31'))
.first();
Map.setCenter(-103.8881,53.0372,10);
Map.addLayer(crop2016,{},'2016 Canada AAFC Annual Crop Inventory');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/AAFC/AAFC_ACI)


[Canada AAFC Annual Crop Inventory](/earth-engine/datasets/catalog/AAFC_ACI)

Starting in 2009, the Earth Observation Team of the Science and Technology Branch (STB) at Agriculture and Agri\-Food Canada (AAFC) began the process of generating annual crop type digital maps. Focusing on the Prairie Provinces in 2009 and 2010, a Decision Tree (DT) based methodology was applied using optical (Landsat\-5, …

 AAFC/ACI,
 agriculture,canada,crop,landcover

2009\-01\-01T00:00:00Z/2023\-01\-01T00:00:00Z



 36\.83 \-135\.17 62\.25 \-51\.24
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








