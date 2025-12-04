



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GlobFire Daily Fire Event Detection Based on MCD64A1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2021\-01\-01T00:00:00Z
Dataset Provider


[European Commission, Joint Research Centre, Global Wildfire Information System](https://doi.org/10.1038/s41597-019-0312-2)




Tags


[area](/earth-engine/datasets/tags/area)
[burnt](/earth-engine/datasets/tags/burnt)
[disaster](/earth-engine/datasets/tags/disaster)
[fire](/earth-engine/datasets/tags/fire)
[globfire](/earth-engine/datasets/tags/globfire)
[mcd64a1](/earth-engine/datasets/tags/mcd64a1)
[modis\-derived](/earth-engine/datasets/tags/modis-derived)
[wildfire](/earth-engine/datasets/tags/wildfire)








#### Description



Fire boundaries based on the MODIS dataset MCD64A1\. The data were computed
based on an algorithm that relies on encoding in a graph structure
a space\-time relationship among patches of burned areas.


Each fire has a unique number identifying the event.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| Id | INT | Numeric id of the fire |
| InitialDate | INT | Initial fire date in milliseconds since 1970\-01\-01 |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Artés, T., Oom, D., De Rigo, D., Durrant, T. H., Maianti, P., Libertà, G., \&
San\-Miguel\-Ayanz, J. (2019\). A global wildfire dataset for the analysis of
fire regimes and fire behaviour. Scientific data, 6(1\), 1\-11\.
[doi:10\.1038/s41597\-019\-0312\-2](https://doi.org/10.1038/s41597-019-0312-2)





### DOIs


* [https://doi.org/10\.1038/s41597\-019\-0312\-2](https://doi.org/10.1038/s41597-019-0312-2)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Folder name for a series of tables.
varfolder='JRC/GWIS/GlobFire/v2/DailyPerimeters';

// List available tables using ee.data.listAssets with asynchronous callback.
functionprintAssetList(listAssetsOutput){
print('Asset list:',listAssetsOutput['assets']);
}
ee.data.listAssets(folder,{},printAssetList);

// Define a table name (table id) identified from the list of available tables.
vartableName='JRC/GWIS/GlobFire/v2/DailyPerimeters/2020';

varcomputeArea=function(f){
returnf.set({'area':f.area()});
};

// Import a selected table as a FeatureCollection.
varfeatures=ee.FeatureCollection(tableName).map(computeArea);

// Visualization parameters for linear fire area gradient.
varvisParams={
palette:['f5ff64','b5ffb4','beeaff','ffc0e8','8e8dff','adadad'],
min:0,
max:600000000,
opacity:0.8,
};

// Paint fire perimeters to an image using computed fire area as the value property.
varimage=ee.Image().float().paint(features,'area');

// Display the image to the map (include features for exploring with Inspector).
Map.addLayer(image,visParams,'GlobFire 2020');
Map.addLayer(features,null,'For Inspector',false);
Map.setCenter(-121.23,39.7,12);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/JRC/JRC_GWIS_GlobFire_v2_DailyPerimeters)


[GlobFire Daily Fire Event Detection Based on MCD64A1](/earth-engine/datasets/catalog/JRC_GWIS_GlobFire_v2_DailyPerimeters)

Fire boundaries based on the MODIS dataset MCD64A1\. The data were computed based on an algorithm that relies on encoding in a graph structure a space\-time relationship among patches of burned areas. Each fire has a unique number identifying the event.

 JRC/GWIS/GlobFire/v2/DailyPerimeters,
 area,burnt,disaster,fire,globfire,mcd64a1,modis\-derived,wildfire

2001\-01\-01T00:00:00Z/2021\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1038/s41597\-019\-0312\-2](https://doi.org/https://doi.org/10.1038/s41597-019-0312-2)
* [https://doi.org/10\.1038/s41597\-019\-0312\-2](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/JRC_GWIS_GlobFire_v2_DailyPerimeters)









