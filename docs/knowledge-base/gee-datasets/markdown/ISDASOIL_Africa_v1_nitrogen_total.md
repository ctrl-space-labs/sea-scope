



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil Total Nitrogen


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/nitrogen_total")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_nitrogen_total)





Tags


[africa](/earth-engine/datasets/tags/africa)
[isda](/earth-engine/datasets/tags/isda)
[soil](/earth-engine/datasets/tags/soil)
nitrogen








#### Description



Total nitrogen at soil depths of 0\-20 cm and 20\-50 cm,
predicted mean and standard deviation.


Pixel values must be back\-transformed with `exp(x/100)-1`.


In areas of dense jungle (generally over central Africa), model accuracy is
low and therefore artifacts such as banding (striping) might be seen.


Soil property predictions were made by
[Innovative Solutions for Decision Agriculture Ltd. (iSDA)](https://isda-africa.com/)
at 30 m pixel size using machine learning coupled with remote sensing data
and a training set of over 100,000 analyzed soil samples.


Further information can be found in the
[FAQ](https://www.isda-africa.com/isdasoil/faq/) and
[technical information documentation](https://www.isda-africa.com/isdasoil/technical-information/). To submit an issue or request support, please visit
[the iSDAsoil site](https://isda-africa.com/isdasoil).





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `mean_0_20` | g/kg | 3 | 246 | Nitrogen, total, predicted mean at 0\-20 cm depth |
| `mean_20_50` | g/kg | 0 | 254 | Nitrogen, total, predicted mean at 20\-50 cm depth |
| `stdev_0_20` | g/kg | 1 | 124 | Nitrogen, total, standard deviation at 0\-20 cm depth |
| `stdev_20_50` | g/kg | 1 | 125 | Nitrogen, total, standard deviation at 20\-50 cm depth |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Hengl, T., Miller, M.A.E., Križan, J., et al. African soil properties and nutrients
mapped at 30 m spatial resolution using two\-scale ensemble machine learning.
Sci Rep 11, 6130 (2021\).
[doi:10\.1038/s41598\-021\-85639\-y](https://doi.org/10.1038/s41598-021-85639-y)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varmean_0_20=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#000004" label="0-0.2" opacity="1" quantity="20"/>'+
'<ColorMapEntry color="#0C0927" label="0.2-0.3" opacity="1" quantity="30"/>'+
'<ColorMapEntry color="#231151" label="0.3-0.4" opacity="1" quantity="36"/>'+
'<ColorMapEntry color="#410F75" label="0.4-0.5" opacity="1" quantity="43"/>'+
'<ColorMapEntry color="#5F187F" label="0.5-0.6" opacity="1" quantity="48"/>'+
'<ColorMapEntry color="#7B2382" label="0.6-0.7" opacity="1" quantity="52"/>'+
'<ColorMapEntry color="#982D80" label="0.7-0.8" opacity="1" quantity="58"/>'+
'<ColorMapEntry color="#B63679" label="0.8-0.9" opacity="1" quantity="64"/>'+
'<ColorMapEntry color="#D3436E" label="0.9-1" opacity="1" quantity="67"/>'+
'<ColorMapEntry color="#EB5760" label="1-1.1" opacity="1" quantity="75"/>'+
'<ColorMapEntry color="#F8765C" label="1.1-1.2" opacity="1" quantity="79"/>'+
'<ColorMapEntry color="#FD9969" label="1.2-1.3" opacity="1" quantity="83"/>'+
'<ColorMapEntry color="#FEBA80" label="1.3-1.4" opacity="1" quantity="89"/>'+
'<ColorMapEntry color="#FDDC9E" label="1.4-1.5" opacity="1" quantity="93"/>'+
'<ColorMapEntry color="#FCFDBF" label="1.5-10" opacity="1" quantity="99"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varmean_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#000004" label="0-0.2" opacity="1" quantity="20"/>'+
'<ColorMapEntry color="#0C0927" label="0.2-0.3" opacity="1" quantity="30"/>'+
'<ColorMapEntry color="#231151" label="0.3-0.4" opacity="1" quantity="36"/>'+
'<ColorMapEntry color="#410F75" label="0.4-0.5" opacity="1" quantity="43"/>'+
'<ColorMapEntry color="#5F187F" label="0.5-0.6" opacity="1" quantity="48"/>'+
'<ColorMapEntry color="#7B2382" label="0.6-0.7" opacity="1" quantity="52"/>'+
'<ColorMapEntry color="#982D80" label="0.7-0.8" opacity="1" quantity="58"/>'+
'<ColorMapEntry color="#B63679" label="0.8-0.9" opacity="1" quantity="64"/>'+
'<ColorMapEntry color="#D3436E" label="0.9-1" opacity="1" quantity="67"/>'+
'<ColorMapEntry color="#EB5760" label="1-1.1" opacity="1" quantity="75"/>'+
'<ColorMapEntry color="#F8765C" label="1.1-1.2" opacity="1" quantity="79"/>'+
'<ColorMapEntry color="#FD9969" label="1.2-1.3" opacity="1" quantity="83"/>'+
'<ColorMapEntry color="#FEBA80" label="1.3-1.4" opacity="1" quantity="89"/>'+
'<ColorMapEntry color="#FDDC9E" label="1.4-1.5" opacity="1" quantity="93"/>'+
'<ColorMapEntry color="#FCFDBF" label="1.5-10" opacity="1" quantity="99"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varstdev_0_20=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#fde725" label="low" opacity="1" quantity="1"/>'+
'<ColorMapEntry color="#5dc962" label=" " opacity="1" quantity="8"/>'+
'<ColorMapEntry color="#20908d" label=" " opacity="1" quantity="10"/>'+
'<ColorMapEntry color="#3a528b" label=" " opacity="1" quantity="14"/>'+
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="60"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varstdev_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#fde725" label="low" opacity="1" quantity="1"/>'+
'<ColorMapEntry color="#5dc962" label=" " opacity="1" quantity="8"/>'+
'<ColorMapEntry color="#20908d" label=" " opacity="1" quantity="10"/>'+
'<ColorMapEntry color="#3a528b" label=" " opacity="1" quantity="14"/>'+
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="60"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varraw=ee.Image("ISDASOIL/Africa/v1/nitrogen_total");
Map.addLayer(
raw.select(0).sldStyle(mean_0_20),{},
"Nitrogen, total, mean visualization, 0-20 cm");
Map.addLayer(
raw.select(1).sldStyle(mean_20_50),{},
"Nitrogen, total, mean visualization, 20-50 cm");
Map.addLayer(
raw.select(2).sldStyle(stdev_0_20),{},
"Nitrogen, total, stdev visualization, 0-20 cm");
Map.addLayer(
raw.select(3).sldStyle(stdev_20_50),{},
"Nitrogen, total, stdev visualization, 20-50 cm");

varconverted=raw.divide(100).exp().subtract(1);

varvisualization={min:0,max:10000};

Map.setCenter(25,-3,2);

Map.addLayer(converted.select(0),visualization,"Nitrogen, total, mean, 0-20 cm");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_nitrogen_total)


[iSDAsoil Total Nitrogen](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_nitrogen_total)

Total nitrogen at soil depths of 0\-20 cm and 20\-50 cm, predicted mean and standard deviation. Pixel values must be back\-transformed with exp(x/100\)\-1\. In areas of dense jungle (generally over central Africa), model accuracy is low and therefore artifacts such as banding (striping) might be seen. Soil property predictions were …

 ISDASOIL/Africa/v1/nitrogen\_total,
 africa,isda,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








