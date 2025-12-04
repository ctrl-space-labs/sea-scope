



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global Power Plant Database


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================








Dataset Availability
2018\-06\-11T00:00:00Z–2018\-06\-11T00:00:00Z
Dataset Provider


[World Resources Institute](https://datasets.wri.org/dataset/globalpowerplantdatabase)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("WRI/GPPD/power_plants")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_GPPD_power_plants)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("WRI/GPPD/power_plants_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_GPPD_power_plants_FeatureView)





Tags


[infrastructure\-boundaries](/earth-engine/datasets/tags/infrastructure-boundaries)
[table](/earth-engine/datasets/tags/table)
[wri](/earth-engine/datasets/tags/wri)
energy
infrastructure
power
power\-plants








#### Description



The Global Power Plant Database is a comprehensive, open source
database of power plants around the world. It centralizes
power plant data to make it easier to navigate, compare and draw
insights. Each power plant is geolocated and entries contain
information on plant capacity, generation, ownership, and fuel type.
As of June 2018, the database includes around 28,500 power plants
from 164 countries.
It will be continuously updated as data becomes available.


The methodology for the dataset creation is given in the World Resources
Institute publication
["A Global Database of Power Plants"](https://www.wri.org/publication/global-power-plant-database).


Associated code for the creation of the dataset can be found on
[GitHub](https://github.com/wri/global-power-plant-database).
The bleeding\-edge version of the database (which may contain substantial
differences from the release in Earth Engine) is available on GitHub as well.


If you use this dataset, the provider (WRI) has requested that you
[register your use](https://goo.gl/ivTvkd) and (optionally)
sign up to receive update notifications.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| country | STRING | 3\-character country code corresponding to the ISO 3166\-1 alpha\-3 specs |
| country\_lg | STRING | Longer form of the country designation |
| name | STRING | Name or title of the power plant, generally in Romanized form |
| gppd\_idnr | STRING | 10\- or 12\-character identifier for the power plant |
| capacitymw | DOUBLE | Electrical generating capacity in megawatts |
| latitude | DOUBLE | Geolocation in decimal degrees |
| longitude | DOUBLE | Geolocation in decimal degrees |
| fuel1 | STRING | Energy source used in electricity generation or export |
| fuel2 | STRING | Energy source used in electricity generation or export |
| fuel3 | STRING | Energy source used in electricity generation or export |
| fuel4 | STRING | Energy source used in electricity generation or export |
| comm\_year | STRING | Year of plant operation, weighted by unit\-capacity when data is available |
| owner | STRING | Majority shareholder of the power plant, generally in Romanized form |
| source | STRING | Entity reporting the data; could be an organization, report, or document, generally in Romanized form |
| url | STRING | Web document corresponding to the "source" field |
| src\_latlon | STRING | Attribution for geolocation information |
| cap\_year | DOUBLE | Year the capacity information was reported |
| gwh\_2013 | DOUBLE | Electricity generation in gigawatt\-hours reported for the year 2013 |
| gwh\_2014 | DOUBLE | Electricity generation in gigawatt\-hours reported for the year 2014 |
| gwh\_2015 | DOUBLE | Electricity generation in gigawatt\-hours reported for the year 2015 |
| gwh\_2016 | DOUBLE | Electricity generation in gigawatt\-hours reported for the year 2016 |
| gwh\_estimt | DOUBLE | Estimated annual electricity generation in gigawatt\-hours for the year 2015 |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Global Energy Observatory, Google, KTH Royal Institute of Technology in
Stockholm, University of Groningen, World Resources Institute. 2018\. Global
Power Plant Database. Published on Resource Watch and Google Earth Engine;
<https://resourcewatch.org/>
<https://earthengine.google.com/>





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Visualization for WRI/GPPD/power_plants

vartable=ee.FeatureCollection('WRI/GPPD/power_plants');

// Get a color from a fuel
varfuelColor=ee.Dictionary({
'Coal':'000000',
'Oil':'593704',
'Gas':'bc80bd',
'Hydro':'0565A6',
'Nuclear':'e31a1c',
'Solar':'ff7f00',
'Waste':'6a3d9a',
'Wind':'5ca2d1',
'Geothermal':'fdbf6f',
'Biomass':'229a00'
});

// List of fuels to add to the map
varfuels=[
'Coal','Oil','Gas','Hydro','Nuclear',
'Solar','Waste','Wind','Geothermal','Biomass'];

/**
 * Computes size from capacity and color from fuel type.
 *
 * @param {!ee.Geometry.Point} pt A point
 * @return {!ee.Geometry.Point} Input point with added style dictionary.
 */
functionaddStyle(pt){
varsize=ee.Number(pt.get('capacitymw')).sqrt().divide(10).add(2);
varcolor=fuelColor.get(pt.get('fuel1'));
returnpt.set(
'styleProperty',ee.Dictionary({'pointSize':size,'color':color}));
}

// Make a FeatureCollection out of the power plant data table.
varpp=ee.FeatureCollection(table).map(addStyle);
print(pp.first());

/**
 * Adds power plants of a certain fuel type to the map.
 *
 * @param {string} fuel A fuel type
 */
functionaddLayer(fuel){
print(fuel);
Map.addLayer(
pp.filter(ee.Filter.eq('fuel1',fuel))
.style({styleProperty:'styleProperty',neighborhood:50}),
{},fuel,true,0.65);
}

// Apply `addLayer` to each record in `fuels`.
fuelColor.keys().evaluate(function(fuelsList){
fuelsList.map(addLayer);
});
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_GPPD_power_plants)
### Visualize as a FeatureView



 A `FeatureView` is a view\-only, accelerated representation of a
 `FeatureCollection`. For more details, visit the
 [`FeatureView` documentation.](/earth-engine/guides/featureview_overview) 



**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varfvLayer=ui.Map.FeatureViewLayer('WRI/GPPD/power_plants_FeatureView');

varvisParams={
opacity:0.65,
color:{
property:'fuel1',
categories:[
['Coal','000000'],
['Oil','593704'],
['Gas','bc80bd'],
['Hydro','0565a6'],
['Nuclear','e31a1c'],
['Solar','ff7f00'],
['Waste','6a3d9a'],
['Wind','5ca2d1'],
['Geothermal','fdbf6f'],
['Biomass','229a00']
],
defaultValue:'ffffff'
},
rules:[
{
filter:ee.Filter.expression('capacitymw < 500'),
pointSize:5,
},
{
filter:ee.Filter.expression('capacitymw >= 500 AND capacitymw < 1000'),
pointSize:10,
},
{
filter:ee.Filter.expression('capacitymw >= 1000'),
pointSize:15,
}
]
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Power plant (fuel type and capacity)');

Map.setCenter(16,49,4);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_GPPD_power_plants_FeatureView)


[Global Power Plant Database](/earth-engine/datasets/catalog/WRI_GPPD_power_plants)

The Global Power Plant Database is a comprehensive, open source database of power plants around the world. It centralizes power plant data to make it easier to navigate, compare and draw insights. Each power plant is geolocated and entries contain information on plant capacity, generation, ownership, and fuel type. As …

 WRI/GPPD/power\_plants,
 infrastructure\-boundaries,table,wri

2018\-06\-11T00:00:00Z/2018\-06\-11T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








