



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil Organic Carbon


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/carbon_organic")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_carbon_organic)





Tags


[africa](/earth-engine/datasets/tags/africa)
[carbon](/earth-engine/datasets/tags/carbon)
[isda](/earth-engine/datasets/tags/isda)
[soil](/earth-engine/datasets/tags/soil)
carbon\-organic








#### Description



Organic carbon at soil depths of 0\-20 cm and 20\-50 cm,
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
| `mean_0_20` | g/kg | 1 | 46 | Carbon, organic, predicted mean at 0\-20 cm depth |
| `mean_20_50` | g/kg | 0 | 46 | Carbon, organic, predicted mean at 20\-50 cm depth |
| `stdev_0_20` | g/kg | 0 | 12 | Carbon, organic, standard deviation at 0\-20 cm depth |
| `stdev_20_50` | g/kg | 0 | 13 | Carbon, organic, standard deviation at 20\-50 cm depth |




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
'<ColorMapEntry color="#000004" label="0-2.3" opacity="1" quantity="12"/>'+
'<ColorMapEntry color="#0C0927" label="2.3-3.5" opacity="1" quantity="15"/>'+
'<ColorMapEntry color="#231151" label="3.5-4" opacity="1" quantity="16"/>'+
'<ColorMapEntry color="#410F75" label="4-4.5" opacity="1" quantity="17"/>'+
'<ColorMapEntry color="#5F187F" label="4.5-5" opacity="1" quantity="18"/>'+
'<ColorMapEntry color="#7B2382" label="5-5.7" opacity="1" quantity="19"/>'+
'<ColorMapEntry color="#982D80" label="5.7-6.4" opacity="1" quantity="20"/>'+
'<ColorMapEntry color="#B63679" label="6.4-7.2" opacity="1" quantity="21"/>'+
'<ColorMapEntry color="#D3436E" label="7.2-8" opacity="1" quantity="22"/>'+
'<ColorMapEntry color="#EB5760" label="8-9" opacity="1" quantity="23"/>'+
'<ColorMapEntry color="#F8765C" label="9-10" opacity="1" quantity="24"/>'+
'<ColorMapEntry color="#FD9969" label="10-11.2" opacity="1" quantity="25"/>'+
'<ColorMapEntry color="#FEBA80" label="11.2-12.5" opacity="1" quantity="26"/>'+
'<ColorMapEntry color="#FDDC9E" label="12.5-13.9" opacity="1" quantity="27"/>'+
'<ColorMapEntry color="#FCFDBF" label="13.9-40" opacity="1" quantity="28"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varmean_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#000004" label="0-2.3" opacity="1" quantity="12"/>'+
'<ColorMapEntry color="#0C0927" label="2.3-3.5" opacity="1" quantity="15"/>'+
'<ColorMapEntry color="#231151" label="3.5-4" opacity="1" quantity="16"/>'+
'<ColorMapEntry color="#410F75" label="4-4.5" opacity="1" quantity="17"/>'+
'<ColorMapEntry color="#5F187F" label="4.5-5" opacity="1" quantity="18"/>'+
'<ColorMapEntry color="#7B2382" label="5-5.7" opacity="1" quantity="19"/>'+
'<ColorMapEntry color="#982D80" label="5.7-6.4" opacity="1" quantity="20"/>'+
'<ColorMapEntry color="#B63679" label="6.4-7.2" opacity="1" quantity="21"/>'+
'<ColorMapEntry color="#D3436E" label="7.2-8" opacity="1" quantity="22"/>'+
'<ColorMapEntry color="#EB5760" label="8-9" opacity="1" quantity="23"/>'+
'<ColorMapEntry color="#F8765C" label="9-10" opacity="1" quantity="24"/>'+
'<ColorMapEntry color="#FD9969" label="10-11.2" opacity="1" quantity="25"/>'+
'<ColorMapEntry color="#FEBA80" label="11.2-12.5" opacity="1" quantity="26"/>'+
'<ColorMapEntry color="#FDDC9E" label="12.5-13.9" opacity="1" quantity="27"/>'+
'<ColorMapEntry color="#FCFDBF" label="13.9-40" opacity="1" quantity="28"/>'+
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

varraw=ee.Image("ISDASOIL/Africa/v1/carbon_organic");
Map.addLayer(
raw.select(0).sldStyle(mean_0_20),{},
"Carbon, organic, mean visualization, 0-20 cm");
Map.addLayer(
raw.select(1).sldStyle(mean_20_50),{},
"Carbon, organic, mean visualization, 20-50 cm");
Map.addLayer(
raw.select(2).sldStyle(stdev_0_20),{},
"Carbon, organic, stdev visualization, 0-20 cm");
Map.addLayer(
raw.select(3).sldStyle(stdev_20_50),{},
"Carbon, organic, stdev visualization, 20-50 cm");

varconverted=raw.divide(10).exp().subtract(1);

varvisualization={min:0,max:20};

Map.setCenter(25,-3,2);

Map.addLayer(converted.select(0),visualization,"Carbon, organic, mean, 0-20 cm");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_carbon_organic)


[iSDAsoil Organic Carbon](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_carbon_organic)

Organic carbon at soil depths of 0\-20 cm and 20\-50 cm, predicted mean and standard deviation. Pixel values must be back\-transformed with exp(x/10\)\-1\. In areas of dense jungle (generally over central Africa), model accuracy is low and therefore artifacts such as banding (striping) might be seen. Soil property predictions were …

 ISDASOIL/Africa/v1/carbon\_organic,
 africa,carbon,isda,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








