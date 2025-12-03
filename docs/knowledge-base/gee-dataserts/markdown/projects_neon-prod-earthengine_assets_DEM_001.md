



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NEON Digital Elevation Model (DEM)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================









info


 This dataset is part of a Publisher Catalog, and not managed by Google Earth Engine.
 
 Contact listaopgee@battelleecology.org
 
 for bugs or [view more datasets](https://developers.google.com/earth-engine/datasets/publisher/neon-prod-earthengine)
 from the National Ecological Observatory Network Catalog. [Learn more about Publisher datasets](/earth-engine/datasets/publisher).
 






Catalog Owner
National Ecological Observatory Network
Dataset Availability
2013\-01\-01T00:00:00Z–2024\-09\-08T16:03:42Z
Dataset Provider


[NEON](https://data.neonscience.org/data-products/DP3.30024.001)



Earth Engine Snippet


`ee.ImageCollection("projects/neon-prod-earthengine/assets/DEM/001")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/neon-prod-earthengine/projects_neon-prod-earthengine_assets_DEM_001)





Tags


[airborne](/earth-engine/datasets/tags/airborne)
[dem](/earth-engine/datasets/tags/dem)
[elevation\-topography](/earth-engine/datasets/tags/elevation-topography)
[forest](/earth-engine/datasets/tags/forest)
[lidar](/earth-engine/datasets/tags/lidar)
[neon](/earth-engine/datasets/tags/neon)
[neon\-prod\-earthengine](/earth-engine/datasets/tags/neon-prod-earthengine)
[publisher\-dataset](/earth-engine/datasets/tags/publisher-dataset)
[vegetation](/earth-engine/datasets/tags/vegetation)








#### Description



Digital models of the surface (DSM) and terrain (DTM) derived from [NEON LiDAR data](https://www.neonscience.org/data-collection/lidar). DSM: Surface features (topographic
information with vegetation and man\-made structures present). DTM: Bare earth elevation
(topographic information with vegetation and man\-made structures removed). Images are
given in meters above mean sea level and mosaicked onto a spatially uniform grid at
1 m resolution. Availability in GEE may not represent full availability in the NEON
Data Portal (linked below). Additional sites and years can be added to GEE upon request
by emailing listaopgee@battelleecology.org.


See [NEON Data Product DP3\.30024\.001](https://data.neonscience.org/data-products/DP3.30024.001) for more details.


Documentation: [Elevation \- LiDAR (DP3\.30024\.001\) Quick Start Guide](https://data.neonscience.org/api/v0/documents/quick-start-guides/NEON.QSG.DP3.30024.001v1?inline=true&fallback=html)


Get started by exploring the [Intro to AOP Data in Google Earth Engine Tutorial Series](https://www.neonscience.org/resources/learning-hub/tutorials/intro-aop-data-google-earth-engine-tutorial-series)


Browse and interact with AOP data in the [NEON AOP GEE Data Viewer App](https://neon-prod-earthengine.projects.earthengine.app/view/neon-aop-gee-data-viewer---desktop)





### Bands



**Pixel Size**
  
1 meter



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `DTM` | m | 0 | 3500 | Digital Terrain Model |
| `DSM` | m | 0 | 3500 | Digital Surface Model |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| AOP\_VISIT\_NUMBER | INT | Unique visit number to the NEON site. |
| CITATION | STRING | Data citation. See [NEON Data Policies and Citation Guidelines](https://www.neonscience.org/data-samples/data-policies-citation). |
| DOI | STRING | Digital Object Identifier. NEON data that have been released are assigned a DOI. |
| FLIGHT\_YEAR | INT | Year the data were collected. |
| NEON\_DOMAIN | STRING | NEON eco\-climatic domain code, "D01" to "D20". See [NEON Field Sites and Domains](https://www.neonscience.org/field-sites/about-field-sites). |
| NEON\_SITE | STRING | NEON four\-digit site code. See [NEON Field Sites](https://www.neonscience.org/field-sites/). |
| NEON\_SITE\_NAME | STRING | Full name of the NEON site. See [NEON Field Sites](https://www.neonscience.org/field-sites/). |
| NEON\_DATA\_PROD\_URL | STRING | NEON data product url. Always set to: [https://data.neonscience.org/data\-products/DP3\.30024\.001](https://data.neonscience.org/data-products/DP3.30024.001). |
| SENSOR\_NAME | STRING | Make and model of the lidar sensor: "Optech Galaxy Prime", "Optech Gemini", "Riegl Q780". |
| SENSOR\_SERIAL | STRING | Serial number of the lidar sensor: "11SEN287", "12SEN311", "5060445", "220855". |
| PROVISIONAL\_RELEASED | STRING | Whether the data are Provisional or Released. See [https://www.neonscience.org/data\-samples/data\-management/data\-revisions\-releases](https://www.neonscience.org/data-samples/data-management/data-revisions-releases). |
| RELEASE\_YEAR | INT | If data are released, the year of the NEON Release Tag. |




### Terms of Use


**Terms of Use**


All data collected by NEON and provided as data products, with the exception
of data related to rare, threatened, or endangered (RTE) species, are
released to the public domain under [Creative Commons CC0 1\.0 "No Rights
Reserved"](https://creativecommons.org/publicdomain/zero/1.0/). No
copyright has been applied to NEON data; any person may copy, modify, or
distribute the data, for commercial or non\-commercial purposes, without
asking for permission. NEON data may still be subject to other laws or
rights such as for privacy, and NEON makes no warranties about the data and
disclaims all liability. When using or citing NEON data, no implication
should be made about endorsement by NEON. In most countries, data and facts
are not copyrightable. By putting NEON data into the public domain, we
encourage broad use, particularly in scientific analyses and data
aggregations. However, please be aware of the following scholarly norms:
NEON data should be used in a way that is mindful of the limitations of the
data, using the documentation associated with the data packages as a guide. 
Please refer to [NEON Data Guidelines and Policies](https://www.neonscience.org/data-samples/guidelines-policies)
for detailed information on how to properly use and cite NEON data, as well as
best practices for publishing research that uses NEON data.




### Citations



Citations:
* See [NEON citation guidelines](https://www.neonscience.org/data-samples/guidelines-policies/citing)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Read in the NEON AOP DEM Image Collection
vardem=ee.ImageCollection(
'projects/neon-prod-earthengine/assets/DEM/001');

// Display available images in the DEM/001 Image Collection
print('NEON DEM Images',dem.aggregate_array('system:index'))

// Specify the start and end dates and filter by date range
varstartDate=ee.Date('2021-01-01');
varendDate=startDate.advance(1,'year');
vardem2021=dem.filterDate(startDate,endDate);

// Filter by NEON site name (see https://www.neonscience.org/field-sites/explore-field-sites)
vardemSOAP_2021=dem2021.filter('NEON_SITE == "SOAP"');

// Select the DTM and DSM bands in order to display each layer
varsoapDTM=dem2021.select('DTM');
varsoapDSM=dem2021.select('DSM');

// Define the color palette and visualization parameters
varpalettes=require('users/gena/packages:palettes');
vardem_palette=palettes.colorbrewer.BrBG[9].reverse();
vardemVis={min:700,max:2300,palette:dem_palette};

// Add the DTM and DSM layers and center on the site
Map.addLayer(soapDTM,demVis,'SOAP 2021 Digital Terrain Model (m)');
Map.addLayer(soapDSM,demVis,'SOAP 2021 Digital Surface Model (m)');
Map.setCenter(-119.25,37.06,12);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/neon-prod-earthengine/projects_neon-prod-earthengine_assets_DEM_001)


[NEON Digital Elevation Model (DEM)](/earth-engine/datasets/catalog/projects_neon-prod-earthengine_assets_DEM_001)

Digital models of the surface (DSM) and terrain (DTM) derived from NEON LiDAR data. DSM: Surface features (topographic information with vegetation and man\-made structures present). DTM: Bare earth elevation (topographic information with vegetation and man\-made structures removed). Images are given in meters above mean sea level and mosaicked onto a …

 projects/neon\-prod\-earthengine/assets/DEM/001,
 airborne,dem,elevation\-topography,forest,lidar,neon,neon\-prod\-earthengine,publisher\-dataset,vegetation

2013\-01\-01T00:00:00Z/2024\-09\-08T16:03:42Z



 16 \-170 73 \-66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








