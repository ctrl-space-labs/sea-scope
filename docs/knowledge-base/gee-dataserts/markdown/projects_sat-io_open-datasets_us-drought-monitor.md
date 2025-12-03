



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

United States Drought Monitor


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===============================================================================================================================









info


 This dataset is part of a Community Catalog, and not managed by Google Earth Engine.
 
 Contact gee\-community\-catalog@googlegroups.com
 
 for bugs or [view more datasets](https://developers.google.com/earth-engine/datasets/community/sat-io)
 from the Awesome GEE Community Catalog Catalog. [Learn more about Community datasets](/earth-engine/datasets/community).
 






Catalog Owner
Awesome GEE Community Catalog
Dataset Availability
2000\-01\-04T00:00:00Z–2025\-07\-08T00:00:00Z
Dataset Provider


[National Drought Mitigation Center](https://drought.unl.edu/)



Earth Engine Snippet


`ee.ImageCollection("projects/sat-io/open-datasets/us-drought-monitor")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/sat-io/projects_sat-io_open-datasets_us-drought-monitor)





Tags


[community\-dataset](/earth-engine/datasets/tags/community-dataset)
[drought](/earth-engine/datasets/tags/drought)
[noaa](/earth-engine/datasets/tags/noaa)
[precipitation](/earth-engine/datasets/tags/precipitation)
[sat\-io](/earth-engine/datasets/tags/sat-io)
[usda](/earth-engine/datasets/tags/usda)
ndmc








#### Description



The U.S. Drought Monitor is a map released every Thursday, showing parts of the U.S. that are in drought. The map uses five classifications: abnormally dry (D0\), showing areas that may be going into or are coming out of drought, and four levels of drought: moderate (D1\), severe (D2\), extreme (D3\) and exceptional (D4\). The Drought Monitor has been a team effort since its inception in 1999, produced jointly by the National Drought Mitigation Center (NDMC) at the University of Nebraska\-Lincoln, the National Oceanic and Atmospheric Administration (NOAA), and the U.S. Department of Agriculture (USDA). The NDMC hosts the web site of the drought monitor and the associated data, and provides the map and data to NOAA, USDA and other agencies. It is freely available at droughtmonitor.unl.edu.





### Bands



**Pixel Size**
  
250 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `DM` | 0 | 4 | Drought classes |




### Terms of Use


**Terms of Use**


The work is licensed under an Open data license for use. The U.S. Drought Monitor is jointly produced by the National Drought Mitigation Center
at the University of Nebraska\-Lincoln, the United States Department of Agriculture and the National Oceanic and Atmospheric Administration. Map courtesy of NDMC.




### Citations



Citations:
* National Drought Mitigation Center; U.S. Department of Agriculture; National Oceanic and Atmospheric Administration (2023\). United States Drought Monitor. University of Nebraska\-Lincoln. https://droughtmonitor.unl.edu/. Accessed 2023\-09\-17





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varusdm=ee.ImageCollection(
"projects/sat-io/open-datasets/us-drought-monitor"
);
/*
Category	Description
DO	Abnormally Dry
D1	Moderate Drought
D2	Severe Drought
D3	Extreme Drought
D4	Exceptional Drought
*/

varusdm=ee.Image(usdm.toList(usdm.size()).get(-1));

// Define a dictionary which will be used to make legend and visualize image on map
vardict={
names:[
"DO	Abnormally Dry",//1
"D1 Moderate Drought",//2
"D2 Severe Drought",//3
"D3 Extreme Drought",//4
"D4 Exceptional Drought",//5
],
colors:["FFFF00","FCD37F","FFAA00","E60000","730000"],
};

// Create a panel to hold the legend widget
varlegend=ui.Panel({
style:{
position:"bottom-left",
padding:"8px 15px",
},
});

// Function to generate the legend
functionaddCategoricalLegend(panel,dict,title){
// Create and add the legend title.
varlegendTitle=ui.Label({
value:title,
style:{
fontWeight:"bold",
fontSize:"18px",
margin:"0 0 4px 0",
padding:"0",
},
});
panel.add(legendTitle);

varloading=ui.Label("Loading legend...",{margin:"2px 0 4px 0"});
panel.add(loading);

// Creates and styles 1 row of the legend.
varmakeRow=function(color,name){
// Create the label that is actually the colored box.
varcolorBox=ui.Label({
style:{
backgroundColor:color,
// Use padding to give the box height and width.
padding:"8px",
margin:"0 0 4px 0",
},
});

// Create the label filled with the description text.
vardescription=ui.Label({
value:name,
style:{margin:"0 0 4px 6px"},
});

returnui.Panel({
widgets:[colorBox,description],
layout:ui.Panel.Layout.Flow("horizontal"),
});
};

// Get the list of palette colors and class names from the image.
varpalette=dict["colors"];
varnames=dict["names"];
loading.style().set("shown",false);

for(vari=0;i < names.length;i++){
panel.add(makeRow(palette[i],names[i]));
}

Map.add(panel);
}

/*
  // Display map and legend ///////////////////////////////////////////////////////////////////////////////
*/

// Add the legend to the map
addCategoricalLegend(legend,dict,"US Drought Monitor");

// Add USDM Image image to the map
Map.addLayer(
usdm,
{min:0,max:4,palette:dict["colors"]},
usdm.get("system:index").getInfo()
);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/sat-io/projects_sat-io_open-datasets_us-drought-monitor)


[United States Drought Monitor](/earth-engine/datasets/catalog/projects_sat-io_open-datasets_us-drought-monitor)

The U.S. Drought Monitor is a map released every Thursday, showing parts of the U.S. that are in drought. The map uses five classifications: abnormally dry (D0\), showing areas that may be going into or are coming out of drought, and four levels of drought: moderate (D1\), severe (D2\), extreme …

 projects/sat\-io/open\-datasets/us\-drought\-monitor,
 community\-dataset,drought,noaa,precipitation,sat\-io,usda

2000\-01\-04T00:00:00Z/2025\-07\-08T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








