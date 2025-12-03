



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil Extractable Calcium


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/calcium_extractable")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_calcium_extractable)





Tags


[africa](/earth-engine/datasets/tags/africa)
[isda](/earth-engine/datasets/tags/isda)
[soil](/earth-engine/datasets/tags/soil)
calcium








#### Description



Extractable calcium at soil depths of 0\-20 cm and 20\-50 cm,
predicted mean and standard deviation.


Pixel values must be back\-transformed with `exp(x/10)-1`.


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
| `mean_0_20` | ppm | 20 | 100 | Calcium, extractable, predicted mean at 0\-20 cm depth |
| `mean_20_50` | ppm | 14 | 100 | Calcium, extractable, predicted mean at 20\-50 cm depth |
| `stdev_0_20` | ppm | 0 | 62 | Calcium, extractable, standard deviation at 0\-20 cm depth |
| `stdev_20_50` | ppm | 0 | 63 | Calcium, extractable, standard deviation at 20\-50 cm depth |




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
'<ColorMapEntry color="#0D0887" label="0-65.7" opacity="1" quantity="42"/>'+
'<ColorMapEntry color="#350498" label="65.7-120.5" opacity="1" quantity="48"/>'+
'<ColorMapEntry color="#5402A3" label="120.5-163" opacity="1" quantity="51"/>'+
'<ColorMapEntry color="#7000A8" label="163-199.3" opacity="1" quantity="53"/>'+
'<ColorMapEntry color="#8B0AA5" label="199.3-269.4" opacity="1" quantity="56"/>'+
'<ColorMapEntry color="#A31E9A" label="269.4-329.3" opacity="1" quantity="58"/>'+
'<ColorMapEntry color="#B93289" label="329.3-402.4" opacity="1" quantity="60"/>'+
'<ColorMapEntry color="#CC4678" label="402.4-491.7" opacity="1" quantity="62"/>'+
'<ColorMapEntry color="#DB5C68" label="491.7-600.8" opacity="1" quantity="64"/>'+
'<ColorMapEntry color="#E97158" label="600.8-664.1" opacity="1" quantity="65"/>'+
'<ColorMapEntry color="#F48849" label="664.1-811.4" opacity="1" quantity="67"/>'+
'<ColorMapEntry color="#FBA139" label="811.4-896.8" opacity="1" quantity="68"/>'+
'<ColorMapEntry color="#FEBC2A" label="896.8-1095.6" opacity="1" quantity="70"/>'+
'<ColorMapEntry color="#FADA24" label="1095.6-1479.3" opacity="1" quantity="73"/>'+
'<ColorMapEntry color="#F0F921" label="1479.3-12000" opacity="1" quantity="77"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varmean_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#0D0887" label="0-65.7" opacity="1" quantity="42"/>'+
'<ColorMapEntry color="#350498" label="65.7-120.5" opacity="1" quantity="48"/>'+
'<ColorMapEntry color="#5402A3" label="120.5-163" opacity="1" quantity="51"/>'+
'<ColorMapEntry color="#7000A8" label="163-199.3" opacity="1" quantity="53"/>'+
'<ColorMapEntry color="#8B0AA5" label="199.3-269.4" opacity="1" quantity="56"/>'+
'<ColorMapEntry color="#A31E9A" label="269.4-329.3" opacity="1" quantity="58"/>'+
'<ColorMapEntry color="#B93289" label="329.3-402.4" opacity="1" quantity="60"/>'+
'<ColorMapEntry color="#CC4678" label="402.4-491.7" opacity="1" quantity="62"/>'+
'<ColorMapEntry color="#DB5C68" label="491.7-600.8" opacity="1" quantity="64"/>'+
'<ColorMapEntry color="#E97158" label="600.8-664.1" opacity="1" quantity="65"/>'+
'<ColorMapEntry color="#F48849" label="664.1-811.4" opacity="1" quantity="67"/>'+
'<ColorMapEntry color="#FBA139" label="811.4-896.8" opacity="1" quantity="68"/>'+
'<ColorMapEntry color="#FEBC2A" label="896.8-1095.6" opacity="1" quantity="70"/>'+
'<ColorMapEntry color="#FADA24" label="1095.6-1479.3" opacity="1" quantity="73"/>'+
'<ColorMapEntry color="#F0F921" label="1479.3-12000" opacity="1" quantity="77"/>'+
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

varraw=ee.Image("ISDASOIL/Africa/v1/calcium_extractable");
Map.addLayer(
raw.select(0).sldStyle(mean_0_20),{},
"Calcium, extractable, mean visualization, 0-20 cm");
Map.addLayer(
raw.select(1).sldStyle(mean_20_50),{},
"Calcium, extractable, mean visualization, 20-50 cm");
Map.addLayer(
raw.select(2).sldStyle(stdev_0_20),{},
"Calcium, extractable, stdev visualization, 0-20 cm");
Map.addLayer(
raw.select(3).sldStyle(stdev_20_50),{},
"Calcium, extractable, stdev visualization, 20-50 cm");

varconverted=raw.divide(10).exp().subtract(1);

varvisualization={min:100,max:2000};

Map.setCenter(25,-3,2);

Map.addLayer(converted.select(0),visualization,"Calcium, extractable, mean, 0-20 cm");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_calcium_extractable)


[iSDAsoil Extractable Calcium](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_calcium_extractable)

Extractable calcium at soil depths of 0\-20 cm and 20\-50 cm, predicted mean and standard deviation. Pixel values must be back\-transformed with exp(x/10\)\-1\. In areas of dense jungle (generally over central Africa), model accuracy is low and therefore artifacts such as banding (striping) might be seen. Soil property predictions were …

 ISDASOIL/Africa/v1/calcium\_extractable,
 africa,isda,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








