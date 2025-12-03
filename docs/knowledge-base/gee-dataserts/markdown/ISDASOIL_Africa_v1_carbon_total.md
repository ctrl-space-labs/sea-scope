



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil Total Carbon


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/carbon_total")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_carbon_total)





Tags


[africa](/earth-engine/datasets/tags/africa)
[aluminium](/earth-engine/datasets/tags/aluminium)
[isda](/earth-engine/datasets/tags/isda)
[soil](/earth-engine/datasets/tags/soil)








#### Description



Total carbon at soil depths of 0\-20 cm and 20\-50 cm,
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
| `mean_0_20` | g/kg | 0 | 58 | Carbon, total, predicted mean at 0\-20 cm depth |
| `mean_20_50` | g/kg | 0 | 55 | Carbon, total, predicted mean at 20\-50 cm depth |
| `stdev_0_20` | g/kg | 0 | 151 | Carbon, total, standard deviation at 0\-20 cm depth |
| `stdev_20_50` | g/kg | 0 | 150 | Carbon, total, standard deviation at 20\-50 cm depth |




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
'<ColorMapEntry color="#000004" label="0-2" opacity="1" quantity="11"/>'+
'<ColorMapEntry color="#0C0927" label="2-5.7" opacity="1" quantity="19"/>'+
'<ColorMapEntry color="#231151" label="5.7-10" opacity="1" quantity="24"/>'+
'<ColorMapEntry color="#410F75" label="10-12.5" opacity="1" quantity="26"/>'+
'<ColorMapEntry color="#5F187F" label="12.5-13.9" opacity="1" quantity="27"/>'+
'<ColorMapEntry color="#7B2382" label="13.9-15.4" opacity="1" quantity="28"/>'+
'<ColorMapEntry color="#982D80" label="15.4-17.2" opacity="1" quantity="29"/>'+
'<ColorMapEntry color="#B63679" label="17.2-19.1" opacity="1" quantity="30"/>'+
'<ColorMapEntry color="#D3436E" label="19.1-21.2" opacity="1" quantity="31"/>'+
'<ColorMapEntry color="#EB5760" label="21.2-23.5" opacity="1" quantity="32"/>'+
'<ColorMapEntry color="#F8765C" label="23.5-26.1" opacity="1" quantity="33"/>'+
'<ColorMapEntry color="#FD9969" label="26.1-29" opacity="1" quantity="34"/>'+
'<ColorMapEntry color="#FEBA80" label="29-32.1" opacity="1" quantity="35"/>'+
'<ColorMapEntry color="#FDDC9E" label="32.1-35.6" opacity="1" quantity="36"/>'+
'<ColorMapEntry color="#FCFDBF" label="35.6-40" opacity="1" quantity="39"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varmean_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#000004" label="0-2" opacity="1" quantity="11"/>'+
'<ColorMapEntry color="#0C0927" label="2-5.7" opacity="1" quantity="19"/>'+
'<ColorMapEntry color="#231151" label="5.7-10" opacity="1" quantity="24"/>'+
'<ColorMapEntry color="#410F75" label="10-12.5" opacity="1" quantity="26"/>'+
'<ColorMapEntry color="#5F187F" label="12.5-13.9" opacity="1" quantity="27"/>'+
'<ColorMapEntry color="#7B2382" label="13.9-15.4" opacity="1" quantity="28"/>'+
'<ColorMapEntry color="#982D80" label="15.4-17.2" opacity="1" quantity="29"/>'+
'<ColorMapEntry color="#B63679" label="17.2-19.1" opacity="1" quantity="30"/>'+
'<ColorMapEntry color="#D3436E" label="19.1-21.2" opacity="1" quantity="31"/>'+
'<ColorMapEntry color="#EB5760" label="21.2-23.5" opacity="1" quantity="32"/>'+
'<ColorMapEntry color="#F8765C" label="23.5-26.1" opacity="1" quantity="33"/>'+
'<ColorMapEntry color="#FD9969" label="26.1-29" opacity="1" quantity="34"/>'+
'<ColorMapEntry color="#FEBA80" label="29-32.1" opacity="1" quantity="35"/>'+
'<ColorMapEntry color="#FDDC9E" label="32.1-35.6" opacity="1" quantity="36"/>'+
'<ColorMapEntry color="#FCFDBF" label="35.6-40" opacity="1" quantity="39"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varstdev_0_20=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#fde725" label="low" opacity="1" quantity="1"/>'+
'<ColorMapEntry color="#5dc962" label=" " opacity="1" quantity="3"/>'+
'<ColorMapEntry color="#20908d" label=" " opacity="1" quantity="4"/>'+
'<ColorMapEntry color="#3a528b" label=" " opacity="1" quantity="5"/>'+
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="6"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varstdev_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#fde725" label="low" opacity="1" quantity="1"/>'+
'<ColorMapEntry color="#5dc962" label=" " opacity="1" quantity="3"/>'+
'<ColorMapEntry color="#20908d" label=" " opacity="1" quantity="4"/>'+
'<ColorMapEntry color="#3a528b" label=" " opacity="1" quantity="5"/>'+
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="6"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varraw=ee.Image("ISDASOIL/Africa/v1/carbon_total");
Map.addLayer(
raw.select(0).sldStyle(mean_0_20),{},
"Carbon, total, mean visualization, 0-20 cm");
Map.addLayer(
raw.select(1).sldStyle(mean_20_50),{},
"Carbon, total, mean visualization, 20-50 cm");
Map.addLayer(
raw.select(2).sldStyle(stdev_0_20),{},
"Carbon, total, stdev visualization, 0-20 cm");
Map.addLayer(
raw.select(3).sldStyle(stdev_20_50),{},
"Carbon, total, stdev visualization, 20-50 cm");

varconverted=raw.divide(10).exp().subtract(1);

varvisualization={min:0,max:60};

Map.setCenter(25,-3,2);

Map.addLayer(converted.select(0),visualization,"Carbon, total, mean, 0-20 cm");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_carbon_total)


[iSDAsoil Total Carbon](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_carbon_total)

Total carbon at soil depths of 0\-20 cm and 20\-50 cm, predicted mean and standard deviation. Pixel values must be back\-transformed with exp(x/10\)\-1\. In areas of dense jungle (generally over central Africa), model accuracy is low and therefore artifacts such as banding (striping) might be seen. Soil property predictions were …

 ISDASOIL/Africa/v1/carbon\_total,
 africa,aluminium,isda,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








