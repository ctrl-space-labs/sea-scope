



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil Clay Content


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/clay_content")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_clay_content)





Tags


[africa](/earth-engine/datasets/tags/africa)
[clay](/earth-engine/datasets/tags/clay)
[isda](/earth-engine/datasets/tags/isda)
[soil](/earth-engine/datasets/tags/soil)








#### Description



Clay content at soil depths of 0\-20 cm and 20\-50 cm,\\npredicted mean and standard deviation.
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
| `mean_0_20` | % | 0 | 84 | Clay content, predicted mean at 0\-20 cm depth |
| `mean_20_50` | % | 0 | 78 | Clay content, predicted mean at 20\-50 cm depth |
| `stdev_0_20` | % | 0 | 90 | Clay content, standard deviation at 0\-20 cm depth |
| `stdev_20_50` | % | 0 | 90 | Clay content, standard deviation at 20\-50 cm depth |




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
'<ColorMapEntry color="#00204D" label="0-8" opacity="1" quantity="8"/>'+
'<ColorMapEntry color="#002D6C" label="8-14" opacity="1" quantity="14"/>'+
'<ColorMapEntry color="#16396D" label="14-17" opacity="1" quantity="17"/>'+
'<ColorMapEntry color="#36476B" label="17-19" opacity="1" quantity="19"/>'+
'<ColorMapEntry color="#4B546C" label="19-21" opacity="1" quantity="21"/>'+
'<ColorMapEntry color="#5C616E" label="21-22" opacity="1" quantity="22"/>'+
'<ColorMapEntry color="#6C6E72" label="22-24" opacity="1" quantity="24"/>'+
'<ColorMapEntry color="#7C7B78" label="24-25" opacity="1" quantity="25"/>'+
'<ColorMapEntry color="#8E8A79" label="25-26" opacity="1" quantity="26"/>'+
'<ColorMapEntry color="#A09877" label="26-28" opacity="1" quantity="28"/>'+
'<ColorMapEntry color="#B3A772" label="28-30" opacity="1" quantity="30"/>'+
'<ColorMapEntry color="#C6B66B" label="30-31" opacity="1" quantity="31"/>'+
'<ColorMapEntry color="#DBC761" label="31-33" opacity="1" quantity="33"/>'+
'<ColorMapEntry color="#F0D852" label="33-36" opacity="1" quantity="36"/>'+
'<ColorMapEntry color="#FFEA46" label="36-70" opacity="1" quantity="40"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varmean_20_50=
'<RasterSymbolizer>'+
'<ColorMap type="ramp">'+
'<ColorMapEntry color="#00204D" label="0-8" opacity="1" quantity="8"/>'+
'<ColorMapEntry color="#002D6C" label="8-14" opacity="1" quantity="14"/>'+
'<ColorMapEntry color="#16396D" label="14-17" opacity="1" quantity="17"/>'+
'<ColorMapEntry color="#36476B" label="17-19" opacity="1" quantity="19"/>'+
'<ColorMapEntry color="#4B546C" label="19-21" opacity="1" quantity="21"/>'+
'<ColorMapEntry color="#5C616E" label="21-22" opacity="1" quantity="22"/>'+
'<ColorMapEntry color="#6C6E72" label="22-24" opacity="1" quantity="24"/>'+
'<ColorMapEntry color="#7C7B78" label="24-25" opacity="1" quantity="25"/>'+
'<ColorMapEntry color="#8E8A79" label="25-26" opacity="1" quantity="26"/>'+
'<ColorMapEntry color="#A09877" label="26-28" opacity="1" quantity="28"/>'+
'<ColorMapEntry color="#B3A772" label="28-30" opacity="1" quantity="30"/>'+
'<ColorMapEntry color="#C6B66B" label="30-31" opacity="1" quantity="31"/>'+
'<ColorMapEntry color="#DBC761" label="31-33" opacity="1" quantity="33"/>'+
'<ColorMapEntry color="#F0D852" label="33-36" opacity="1" quantity="36"/>'+
'<ColorMapEntry color="#FFEA46" label="36-70" opacity="1" quantity="40"/>'+
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
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="6"/>'+
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
'<ColorMapEntry color="#440154" label="high" opacity="1" quantity="6"/>'+
'</ColorMap>'+
'<ContrastEnhancement/>'+
'</RasterSymbolizer>';

varraw=ee.Image("ISDASOIL/Africa/v1/clay_content");
Map.addLayer(
raw.select(0).sldStyle(mean_0_20),{},
"Clay content, mean visualization, 0-20 cm");
Map.addLayer(
raw.select(1).sldStyle(mean_20_50),{},
"Clay content, mean visualization, 20-50 cm");
Map.addLayer(
raw.select(2).sldStyle(stdev_0_20),{},
"Clay content, stdev visualization, 0-20 cm");
Map.addLayer(
raw.select(3).sldStyle(stdev_20_50),{},
"Clay content, stdev visualization, 20-50 cm");

varconverted=raw.divide(10).exp().subtract(1);

varvisualization={min:0,max:50};

Map.setCenter(25,-3,2);

Map.addLayer(converted.select(0),visualization,"Clay content, mean, 0-20 cm");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_clay_content)


[iSDAsoil Clay Content](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_clay_content)

Clay content at soil depths of 0\-20 cm and 20\-50 cm,\\npredicted mean and standard deviation. In areas of dense jungle (generally over central Africa), model accuracy is low and therefore artifacts such as banding (striping) might be seen. Soil property predictions were made by Innovative Solutions for Decision Agriculture Ltd. …

 ISDASOIL/Africa/v1/clay\_content,
 africa,clay,isda,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








