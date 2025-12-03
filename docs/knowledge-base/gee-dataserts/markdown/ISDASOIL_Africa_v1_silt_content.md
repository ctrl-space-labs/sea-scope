



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil Silt Content


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/silt_content")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_silt_content)





Tags


[africa](/earth-engine/datasets/tags/africa)
[isda](/earth-engine/datasets/tags/isda)
[soil](/earth-engine/datasets/tags/soil)
silt








#### Description



Silt content at soil depths of 0\-20 cm and 20\-50 cm,
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
| `mean_0_20` | % | 1 | 61 | Silt content, predicted mean at 0\-20 cm depth |
| `mean_20_50` | % | 0 | 62 | Silt content, predicted mean at 20\-50 cm depth |
| `stdev_0_20` | % | 0 | 38 | Silt content, standard deviation at 0\-20 cm depth |
| `stdev_20_50` | % | 0 | 38 | Silt content, standard deviation at 20\-50 cm depth |




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
'<ColorMapEntry color="#00204D" label="0-7" opacity="1" quantity="7"/>'+
'<ColorMapEntry color="#002D6C" label="7-9" opacity="1" quantity="9"/>'+
'<ColorMapEntry color="#16396D" label="9-10" opacity="1" quantity="10"/>'+
'<ColorMapEntry color="#36476B" label="10-11" opacity="1" quantity="11"/>'+
'<ColorMapEntry color="#4B546C" label="11-12" opacity="1" quantity="12"/>'+
'<ColorMapEntry color="#5C616E" label="12-13" opacity="1" quantity="13"/>'+
'<ColorMapEntry color="#6C6E72" label="13-14" opacity="1" quantity="14"/>'+
'<ColorMapEntry color="#7C7B78" label="14-15" opacity="1" quantity="15"/>'+
'<ColorMapEntry color="#8E8A79" label="15-16" opacity="1" quantity="16"/>'+
'<ColorMapEntry color="#A09877" label="16-17" opacity="1" quantity="17"/>'+
'<ColorMapEntry color="#B3A772" label="17-18" opacity="1" quantity="18"/>'+
'<ColorMapEntry color="#C6B66B" label="18-19" opacity="1" quantity="19"/>'+
'<ColorMapEntry color="#DBC761" label="19-20" opacity="1" quantity="20"/>'+
'<ColorMapEntry color="#F0D852" label="20-22" opacity="1" quantity="22"/>'+
'<ColorMapEntry color="#FFEA46" label="22-70" opacity="1" quantity="24"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varmean_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#00204D" label="0-7" opacity="1" quantity="7"/>'+
'<ColorMapEntry color="#002D6C" label="7-9" opacity="1" quantity="9"/>'+
'<ColorMapEntry color="#16396D" label="9-10" opacity="1" quantity="10"/>'+
'<ColorMapEntry color="#36476B" label="10-11" opacity="1" quantity="11"/>'+
'<ColorMapEntry color="#4B546C" label="11-12" opacity="1" quantity="12"/>'+
'<ColorMapEntry color="#5C616E" label="12-13" opacity="1" quantity="13"/>'+
'<ColorMapEntry color="#6C6E72" label="13-14" opacity="1" quantity="14"/>'+
'<ColorMapEntry color="#7C7B78" label="14-15" opacity="1" quantity="15"/>'+
'<ColorMapEntry color="#8E8A79" label="15-16" opacity="1" quantity="16"/>'+
'<ColorMapEntry color="#A09877" label="16-17" opacity="1" quantity="17"/>'+
'<ColorMapEntry color="#B3A772" label="17-18" opacity="1" quantity="18"/>'+
'<ColorMapEntry color="#C6B66B" label="18-19" opacity="1" quantity="19"/>'+
'<ColorMapEntry color="#DBC761" label="19-20" opacity="1" quantity="20"/>'+
'<ColorMapEntry color="#F0D852" label="20-22" opacity="1" quantity="22"/>'+
'<ColorMapEntry color="#FFEA46" label="22-70" opacity="1" quantity="24"/>'+
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
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="4.19000000000005"/>'+
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
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="4.19000000000005"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varraw=ee.Image("ISDASOIL/Africa/v1/silt_content");
Map.addLayer(
raw.select(0).sldStyle(mean_0_20),{},
"Silt content, mean visualization, 0-20 cm");
Map.addLayer(
raw.select(1).sldStyle(mean_20_50),{},
"Silt content, mean visualization, 20-50 cm");
Map.addLayer(
raw.select(2).sldStyle(stdev_0_20),{},
"Silt content, stdev visualization, 0-20 cm");
Map.addLayer(
raw.select(3).sldStyle(stdev_20_50),{},
"Silt content, stdev visualization, 20-50 cm");

varconverted=raw.divide(10).exp().subtract(1);

varvisualization={min:0,max:15};

Map.setCenter(25,-3,2);

Map.addLayer(converted.select(0),visualization,"Silt content, mean, 0-20 cm");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_silt_content)


[iSDAsoil Silt Content](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_silt_content)

Silt content at soil depths of 0\-20 cm and 20\-50 cm, predicted mean and standard deviation. Pixel values must be back\-transformed with exp(x/10\)\-1\. In areas of dense jungle (generally over central Africa), model accuracy is low and therefore artifacts such as banding (striping) might be seen. Soil property predictions were …

 ISDASOIL/Africa/v1/silt\_content,
 africa,isda,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








