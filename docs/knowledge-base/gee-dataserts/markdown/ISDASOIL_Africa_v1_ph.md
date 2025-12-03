



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil pH


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/ph")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_ph)





Tags


[africa](/earth-engine/datasets/tags/africa)
[isda](/earth-engine/datasets/tags/isda)
[ph](/earth-engine/datasets/tags/ph)
[soil](/earth-engine/datasets/tags/soil)








#### Description



pH at soil depths of 0\-20 cm and 20\-50 cm,
predicted mean and standard deviation.


Pixel values must be back\-transformed with `x/10`.


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




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `mean_0_20` | 35 | 103 | pH, predicted mean at 0\-20 cm depth |
| `mean_20_50` | 35 | 102 | pH, predicted mean at 20\-50 cm depth |
| `stdev_0_20` | 0 | 18 | pH, standard deviation at 0\-20 cm depth |
| `stdev_20_50` | 0 | 18 | pH, standard deviation at 20\-50 cm depth |




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
'<ColorMapEntry color="#CC0000" label="3.5-4.6" opacity="1" quantity="46"/>'+
'<ColorMapEntry color="#FF0000" label="4.6-4.9" opacity="1" quantity="49"/>'+
'<ColorMapEntry color="#FF5500" label="4.9-5.2" opacity="1" quantity="52"/>'+
'<ColorMapEntry color="#FFAA00" label="5.2-5.4" opacity="1" quantity="54"/>'+
'<ColorMapEntry color="#FFFF00" label="5.4-5.5" opacity="1" quantity="55"/>'+
'<ColorMapEntry color="#D4FF2B" label="5.5-5.6" opacity="1" quantity="56"/>'+
'<ColorMapEntry color="#AAFF55" label="5.6-5.7" opacity="1" quantity="57"/>'+
'<ColorMapEntry color="#80FF80" label="5.7-5.9" opacity="1" quantity="59"/>'+
'<ColorMapEntry color="#55FFAA" label="5.9-6" opacity="1" quantity="60"/>'+
'<ColorMapEntry color="#2BFFD5" label="6-6.2" opacity="1" quantity="62"/>'+
'<ColorMapEntry color="#00FFFF" label="6.2-6.3" opacity="1" quantity="63"/>'+
'<ColorMapEntry color="#00AAFF" label="6.3-6.6" opacity="1" quantity="66"/>'+
'<ColorMapEntry color="#0055FF" label="6.6-6.8" opacity="1" quantity="68"/>'+
'<ColorMapEntry color="#0000FF" label="6.8-7.1" opacity="1" quantity="71"/>'+
'<ColorMapEntry color="#0000CC" label="7.1-10.5" opacity="1" quantity="76"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varmean_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#CC0000" label="3.5-4.6" opacity="1" quantity="46"/>'+
'<ColorMapEntry color="#FF0000" label="4.6-4.9" opacity="1" quantity="49"/>'+
'<ColorMapEntry color="#FF5500" label="4.9-5.2" opacity="1" quantity="52"/>'+
'<ColorMapEntry color="#FFAA00" label="5.2-5.4" opacity="1" quantity="54"/>'+
'<ColorMapEntry color="#FFFF00" label="5.4-5.5" opacity="1" quantity="55"/>'+
'<ColorMapEntry color="#D4FF2B" label="5.5-5.6" opacity="1" quantity="56"/>'+
'<ColorMapEntry color="#AAFF55" label="5.6-5.7" opacity="1" quantity="57"/>'+
'<ColorMapEntry color="#80FF80" label="5.7-5.9" opacity="1" quantity="59"/>'+
'<ColorMapEntry color="#55FFAA" label="5.9-6" opacity="1" quantity="60"/>'+
'<ColorMapEntry color="#2BFFD5" label="6-6.2" opacity="1" quantity="62"/>'+
'<ColorMapEntry color="#00FFFF" label="6.2-6.3" opacity="1" quantity="63"/>'+
'<ColorMapEntry color="#00AAFF" label="6.3-6.6" opacity="1" quantity="66"/>'+
'<ColorMapEntry color="#0055FF" label="6.6-6.8" opacity="1" quantity="68"/>'+
'<ColorMapEntry color="#0000FF" label="6.8-7.1" opacity="1" quantity="71"/>'+
'<ColorMapEntry color="#0000CC" label="7.1-10.5" opacity="1" quantity="76"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varstdev_0_20=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#fde725" label="low" opacity="1" quantity="1"/>'+
'<ColorMapEntry color="#5dc962" label=" " opacity="1" quantity="2"/>'+
'<ColorMapEntry color="#20908d" label=" " opacity="1" quantity="3"/>'+
'<ColorMapEntry color="#3a528b" label=" " opacity="1" quantity="4"/>'+
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="5"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varstdev_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#fde725" label="low" opacity="1" quantity="1"/>'+
'<ColorMapEntry color="#5dc962" label=" " opacity="1" quantity="2"/>'+
'<ColorMapEntry color="#20908d" label=" " opacity="1" quantity="3"/>'+
'<ColorMapEntry color="#3a528b" label=" " opacity="1" quantity="4"/>'+
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="5"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';
varraw=ee.Image("ISDASOIL/Africa/v1/ph");
Map.addLayer(
raw.select(0).sldStyle(mean_0_20),{},
"ph, mean visualization, 0-20 cm");
Map.addLayer(
raw.select(1).sldStyle(mean_20_50),{},
"ph, mean visualization, 20-50 cm");
Map.addLayer(
raw.select(2).sldStyle(stdev_0_20),{},
"ph, stdev visualization, 0-20 cm");
Map.addLayer(
raw.select(3).sldStyle(stdev_20_50),{},
"ph, stdev visualization, 20-50 cm");

varconverted=raw.divide(10);

varvisualization={min:4,max:8};

Map.setCenter(25,-3,2);

Map.addLayer(converted.select(0),visualization,"ph, mean, 0-20 cm");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_ph)


[iSDAsoil pH](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_ph)

pH at soil depths of 0\-20 cm and 20\-50 cm, predicted mean and standard deviation. Pixel values must be back\-transformed with x/10\. In areas of dense jungle (generally over central Africa), model accuracy is low and therefore artifacts such as banding (striping) might be seen. Soil property predictions were made …

 ISDASOIL/Africa/v1/ph,
 africa,isda,ph,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








