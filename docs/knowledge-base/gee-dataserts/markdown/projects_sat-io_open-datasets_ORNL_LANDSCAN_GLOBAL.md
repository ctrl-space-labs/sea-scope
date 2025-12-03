



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

LandScan Population Data Global 1km


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=====================================================================================================================================









info


 This dataset is part of a Community Catalog, and not managed by Google Earth Engine.
 
 Contact gee\-community\-catalog@googlegroups.com
 
 for bugs or [view more datasets](https://developers.google.com/earth-engine/datasets/community/sat-io)
 from the Awesome GEE Community Catalog Catalog. [Learn more about Community datasets](/earth-engine/datasets/community).
 






Catalog Owner
Awesome GEE Community Catalog
Dataset Availability
2000\-01\-01T00:00:00Z–2023\-12\-31T00:00:00Z
Dataset Provider


[Oak Ridge National Laboratory](https://www.ornl.gov/)



Earth Engine Snippet


`ee.ImageCollection("projects/sat-io/open-datasets/ORNL/LANDSCAN_GLOBAL")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/sat-io/projects_sat-io_open-datasets_ORNL_LANDSCAN_GLOBAL)





Tags


[community\-dataset](/earth-engine/datasets/tags/community-dataset)
[demography](/earth-engine/datasets/tags/demography)
[landscan](/earth-engine/datasets/tags/landscan)
[population](/earth-engine/datasets/tags/population)
[sat\-io](/earth-engine/datasets/tags/sat-io)








#### Description



The LandScan dataset, provided by the Oak Ridge National Laboratory (ORNL), offers a comprehensive and high\-resolution global population distribution dataset that serves as a valuable resource for a wide range of applications. Leveraging state\-of\-the\-art spatial modeling techniques and advanced geospatial data sources, LandScan provides detailed information on population counts and density at a 30 arc\-second resolution, enabling precise and up\-to\-date insights into human settlement patterns across the globe. With its accuracy and granularity, LandScan supports diverse fields such as urban planning, disaster response, epidemiology, and environmental research, making it an essential tool for decision\-makers and researchers seeking to understand and address various societal and environmental challenges on a global scale.





### Bands



**Pixel Size**
  
1000 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `b1` | 0\* | 21171\* | Estimated Population count |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


Landscan datasets are licensed under the Creative Commons Attribution 4\.0
International License. Users are free to use, copy, distribute, transmit,
and adapt the work for commercial and non\-commercial purposes, without
restriction, as long as clear attribution of the source is provided.




### Citations



Citations:
* Sims, K., Reith, A., Bright, E., Kaufman, J., Pyle, J., Epting, J., Gonzales, J., Adams, D., Powell, E., Urban, M., \& Rose, A. (2023\). LandScan Global 2022 \[Data set]. Oak Ridge National Laboratory. https://doi.org/10\.48690/1529167





### DOIs


* [https://doi.org/10\.48690/1529167](https://doi.org/10.48690/1529167)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varlandscan_global=
ee.ImageCollection('projects/sat-io/open-datasets/ORNL/LANDSCAN_GLOBAL');
varpopcount_intervals='<RasterSymbolizer>'+
' <ColorMap type="intervals" extended="false" >'+
'<ColorMapEntry color="#CCCCCC" quantity="0" label="No Data"/>'+
'<ColorMapEntry color="#FFFFBE" quantity="5" label="Population Count (Estimate)"/>'+
'<ColorMapEntry color="#FEFF73" quantity="25" label="Population Count (Estimate)"/>'+
'<ColorMapEntry color="#FEFF2C" quantity="50" label="Population Count (Estimate)"/>'+
'<ColorMapEntry color="#FFAA27" quantity="100" label="Population Count (Estimate)"/>'+
'<ColorMapEntry color="#FF6625" quantity="500" label="Population Count (Estimate)"/>'+
'<ColorMapEntry color="#FF0023" quantity="2500" label="Population Count (Estimate)"/>'+
'<ColorMapEntry color="#CC001A" quantity="5000" label="Population Count (Estimate)"/>'+
'<ColorMapEntry color="#730009" quantity="185000" label="Population Count (Estimate)"/>'+
'</ColorMap>'+
'</RasterSymbolizer>';

// Define a dictionary which will be used to make legend and visualize image on
// map
vardict={
'names':[
'0','1-5','6-25','26-50','51-100','101-500','501-2500','2501-5000',
'5001-185000'
],
'colors':[
'#CCCCCC','#FFFFBE','#FEFF73','#FEFF2C','#FFAA27','#FF6625','#FF0023',
'#CC001A','#730009'
]
};

// Create a panel to hold the legend widget
varlegend=ui.Panel({style:{position:'bottom-left',padding:'8px 15px'}});

// Function to generate the legend
functionaddCategoricalLegend(panel,dict,title){
// Create and add the legend title.
varlegendTitle=ui.Label({
value:title,
style:{
fontWeight:'bold',
fontSize:'18px',
margin:'0 0 4px 0',
padding:'0'
}
});
panel.add(legendTitle);

varloading=ui.Label('Loading legend...',{margin:'2px 0 4px 0'});
panel.add(loading);

// Creates and styles 1 row of the legend.
varmakeRow=function(color,name){
// Create the label that is actually the colored box.
varcolorBox=ui.Label({
style:{
backgroundColor:color,
// Use padding to give the box height and width.
padding:'8px',
margin:'0 0 4px 0'
}
});

// Create the label filled with the description text.
vardescription=ui.Label({value:name,style:{margin:'0 0 4px 6px'}});

returnui.Panel({
widgets:[colorBox,description],
layout:ui.Panel.Layout.Flow('horizontal')
});
};

// Get the list of palette colors and class names from the image.
varpalette=dict['colors'];
varnames=dict['names'];
loading.style().set('shown',false);

for(vari=0;i < names.length;i++){
panel.add(makeRow(palette[i],names[i]));
}

Map.add(panel);
}

addCategoricalLegend(legend,dict,'Population Count(estimate)');

Map.addLayer(
landscan_global.sort('system:time_start')
.first()
.sldStyle(popcount_intervals),
{},'Population Count Estimate 2000');
Map.addLayer(
landscan_global.sort('system:time_start',false)
.first()
.sldStyle(popcount_intervals),
{},'Population Count Estimate 2022');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/sat-io/projects_sat-io_open-datasets_ORNL_LANDSCAN_GLOBAL)


[LandScan Population Data Global 1km](/earth-engine/datasets/catalog/projects_sat-io_open-datasets_ORNL_LANDSCAN_GLOBAL)

The LandScan dataset, provided by the Oak Ridge National Laboratory (ORNL), offers a comprehensive and high\-resolution global population distribution dataset that serves as a valuable resource for a wide range of applications. Leveraging state\-of\-the\-art spatial modeling techniques and advanced geospatial data sources, LandScan provides detailed information on population counts and …

 projects/sat\-io/open\-datasets/ORNL/LANDSCAN\_GLOBAL,
 community\-dataset,demography,landscan,population,sat\-io

2000\-01\-01T00:00:00Z/2023\-12\-31T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.48690/1529167](https://doi.org/https://www.ornl.gov/)
* [https://doi.org/10\.48690/1529167](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/projects_sat-io_open-datasets_ORNL_LANDSCAN_GLOBAL)









