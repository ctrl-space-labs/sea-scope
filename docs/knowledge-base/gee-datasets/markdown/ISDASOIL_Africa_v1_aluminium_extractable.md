



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil extractable Aluminium


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/aluminium_extractable")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_aluminium_extractable)





Tags


[africa](/earth-engine/datasets/tags/africa)
[aluminium](/earth-engine/datasets/tags/aluminium)
[isda](/earth-engine/datasets/tags/isda)
[soil](/earth-engine/datasets/tags/soil)








#### Description



Extractable aluminium at soil depths of 0\-20 cm and 20\-50 cm,
predicted mean and standard deviation.


Pixel values must be back\-transformed with `exp(x/10)-1`.


Soil property predictions were made by
[Innovative Solutions for Decision Agriculture Ltd. (iSDA)](https://isda-africa.com/)
at 30 m pixel size using machine learning coupled with remote sensing data
and a training set of over 100,000 analyzed soil samples.


Further information can be found in the
[FAQ](https://www.isda-africa.com/isdasoil/faq/) and
[technical information documentation](https://www.isda-africa.com/isdasoil/technical-information/). To submit an issue or request support, please visit
[the iSDAsoil site](https://isda-africa.com/isdasoil).


In areas of dense jungle (generally over central Africa), model accuracy is
low and therefore artifacts such as banding (striping) might be seen.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `mean_0_20` | ppm | 3 | 80 | Aluminium, extractable, predicted mean at 0\-20 cm depth |
| `mean_20_50` | ppm | 4 | 79 | Aluminium, extractable, predicted mean at 20\-50 cm depth |
| `stdev_0_20` | ppm | 1 | 53 | Aluminium, extractable, standard deviation at 0\-20 cm depth |
| `stdev_20_50` | ppm | 1 | 51 | Aluminium, extractable, standard deviation at 20\-50 cm depth |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Hengl, T., Miller, M.A.E., Križan, J., et al. African soil properties and nutrients
mapped at 30 m spatial resolution using two\-scale ensemble machine learning.
Sci Rep 11, 6130 (2021\).
[doi:10\.1038/s41598\-021\-85639\-y](https://doi.org/10.1038/s41598-021-85639-y)
* Hengl, T., Miller, M.A.E., Križan, J., et al. African soil properties and nutrients
mapped at 30 m spatial resolution using two\-scale ensemble machine learning.
Sci Rep 11, 6130 (2021\).
[doi:10\.1038/s41598\-021\-85639\-y](https://doi.org/10.1038/s41598-021-85639-y)





### DOIs


* [https://doi.org/10\.1038/s41598\-021\-85639\-y](https://doi.org/10.1038/s41598-021-85639-y)




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
'<ColorMapEntry color="#000004" label="0-21.2" opacity="1" quantity="31"/>'+
'<ColorMapEntry color="#0C0927" label="21.2-35.6" opacity="1" quantity="36"/>'+
'<ColorMapEntry color="#231151" label="35.6-53.6" opacity="1" quantity="40"/>'+
'<ColorMapEntry color="#410F75" label="53.6-65.7" opacity="1" quantity="42"/>'+
'<ColorMapEntry color="#5F187F" label="65.7-72.7" opacity="1" quantity="43"/>'+
'<ColorMapEntry color="#7B2382" label="72.7-80.5" opacity="1" quantity="44"/>'+
'<ColorMapEntry color="#982D80" label="80.5-89" opacity="1" quantity="45"/>'+
'<ColorMapEntry color="#B63679" label="89-98.5" opacity="1" quantity="46"/>'+
'<ColorMapEntry color="#D3436E" label="98.5-108.9" opacity="1" quantity="47"/>'+
'<ColorMapEntry color="#EB5760" label="108.9-120.5" opacity="1" quantity="48"/>'+
'<ColorMapEntry color="#F8765C" label="120.5-133.3" opacity="1" quantity="49"/>'+
'<ColorMapEntry color="#FD9969" label="133.3-147.4" opacity="1" quantity="50"/>'+
'<ColorMapEntry color="#FEBA80" label="147.4-163" opacity="1" quantity="51"/>'+
'<ColorMapEntry color="#FDDC9E" label="163-199.3" opacity="1" quantity="53"/>'+
'<ColorMapEntry color="#FCFDBF" label="199.3-1800" opacity="1" quantity="55"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varmean_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#000004" label="0-21.2" opacity="1" quantity="31"/>'+
'<ColorMapEntry color="#0C0927" label="21.2-35.6" opacity="1" quantity="36"/>'+
'<ColorMapEntry color="#231151" label="35.6-53.6" opacity="1" quantity="40"/>'+
'<ColorMapEntry color="#410F75" label="53.6-65.7" opacity="1" quantity="42"/>'+
'<ColorMapEntry color="#5F187F" label="65.7-72.7" opacity="1" quantity="43"/>'+
'<ColorMapEntry color="#7B2382" label="72.7-80.5" opacity="1" quantity="44"/>'+
'<ColorMapEntry color="#982D80" label="80.5-89" opacity="1" quantity="45"/>'+
'<ColorMapEntry color="#B63679" label="89-98.5" opacity="1" quantity="46"/>'+
'<ColorMapEntry color="#D3436E" label="98.5-108.9" opacity="1" quantity="47"/>'+
'<ColorMapEntry color="#EB5760" label="108.9-120.5" opacity="1" quantity="48"/>'+
'<ColorMapEntry color="#F8765C" label="120.5-133.3" opacity="1" quantity="49"/>'+
'<ColorMapEntry color="#FD9969" label="133.3-147.4" opacity="1" quantity="50"/>'+
'<ColorMapEntry color="#FEBA80" label="147.4-163" opacity="1" quantity="51"/>'+
'<ColorMapEntry color="#FDDC9E" label="163-199.3" opacity="1" quantity="53"/>'+
'<ColorMapEntry color="#FCFDBF" label="199.3-1800" opacity="1" quantity="55"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varstdev_0_20=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#fde725" label="low" opacity="1" quantity="5"/>'+
'<ColorMapEntry color="#5dc962" label=" " opacity="1" quantity="9"/>'+
'<ColorMapEntry color="#20908d" label=" " opacity="1" quantity="10"/>'+
'<ColorMapEntry color="#3a528b" label=" " opacity="1" quantity="12"/>'+
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="14"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varstdev_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#fde725" label="low" opacity="1" quantity="5"/>'+
'<ColorMapEntry color="#5dc962" label=" " opacity="1" quantity="9"/>'+
'<ColorMapEntry color="#20908d" label=" " opacity="1" quantity="10"/>'+
'<ColorMapEntry color="#3a528b" label=" " opacity="1" quantity="12"/>'+
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="14"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

Map.setCenter(25,-3,2);

varraw=ee.Image("ISDASOIL/Africa/v1/aluminium_extractable");
Map.addLayer(
raw.select(0).sldStyle(mean_0_20),{},
"Aluminium, extractable, mean visualization, 0-20 cm");
Map.addLayer(
raw.select(1).sldStyle(mean_20_50),{},
"Aluminium, extractable, mean visualization, 20-50 cm");
Map.addLayer(
raw.select(2).sldStyle(stdev_0_20),{},
"Aluminium, extractable, stdev visualization, 0-20 cm");
Map.addLayer(
raw.select(3).sldStyle(stdev_20_50),{},
"Aluminium, extractable, stdev visualization, 20-50 cm");

varconverted=raw.divide(10).exp().subtract(1);
Map.addLayer(
converted.select(0),{min:0,max:100},
"Aluminium, extractable, mean, 0-20 cm");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_aluminium_extractable)


[iSDAsoil extractable Aluminium](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_aluminium_extractable)

Extractable aluminium at soil depths of 0\-20 cm and 20\-50 cm, predicted mean and standard deviation. Pixel values must be back\-transformed with exp(x/10\)\-1\. Soil property predictions were made by Innovative Solutions for Decision Agriculture Ltd. (iSDA) at 30 m pixel size using machine learning coupled with remote sensing data and …

 ISDASOIL/Africa/v1/aluminium\_extractable,
 africa,aluminium,isda,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1038/s41598\-021\-85639\-y](https://doi.org/https://isda-africa.com/)
* [https://doi.org/10\.1038/s41598\-021\-85639\-y](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_aluminium_extractable)









