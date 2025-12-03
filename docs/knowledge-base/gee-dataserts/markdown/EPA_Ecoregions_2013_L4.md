



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

US EPA Ecoregions (Level IV)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================








Dataset Availability
2013\-04\-16T00:00:00Z–2013\-04\-17T00:00:00Z
Dataset Provider


[United States Environmental Protection Agency](https://www.epa.gov/eco-research/level-iii-and-iv-ecoregions-continental-united-states)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("EPA/Ecoregions/2013/L4")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/EPA/EPA_Ecoregions_2013_L4)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("EPA/Ecoregions/2013/L4_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/EPA/EPA_Ecoregions_2013_L4_FeatureView)





Tags


[ecoregions](/earth-engine/datasets/tags/ecoregions)
[ecosystems](/earth-engine/datasets/tags/ecosystems)
[epa](/earth-engine/datasets/tags/epa)
[table](/earth-engine/datasets/tags/table)








#### Description



The U.S. Environmental Protection Agency (USEPA) provides
the Ecoregions dataset to serve as a spatial framework for the
research, assessment, management, and monitoring of ecosystems
and ecosystem components. Ecoregions denote areas of general
similarity in ecosystems and in the type, quality, and quantity
of environmental resources. These general\-purpose regions are
critical for structuring and implementing ecosystem management
strategies across federal agencies, state agencies, and nongovernmental
organizations that are responsible for different types of resources
within the same geographical areas.


The approach used to
compile this map is based on the premise that ecological regions
can be identified through the analysis of patterns of biotic
and abiotic phenomena, including geology, physiography, vegetation,
climate, soils, land use, wildlife, and hydrology. The relative
importance of each characteristic varies from one ecological
region to another.


This dataset includes the USEPA ecoregions
classification scheme, as well as the scheme from the Commission
for Environmental Cooperation (CEC). Ecoregions are hierarchical,
with Level IV being the most detailed and Level I defining the
broadest classifications. Because of this hierarchy, Level III
features retain information from Levels I and II. The CEC divided
all of North America in distinct ecoregions for Levels I, II,
and III, while the USEPA did so only for the United States at
Level III and Level IV. The columns starting with 'us*' belong
to the USEPA scheme, and the columns starting with 'na*' belong
to the CEC scheme. The ingested version of this dataset contains
features for the conterminous United States only (that is, Alaska
and Hawaii are not included). Methods used to define the ecoregions
are explained in Omernik (1995, 2004\), Omernik and others (2000\),
and Gallant and others (1989\).


\*Calculated by the data provider.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| l1\_key | STRING | NA Level I Code and Name |
| l2\_key | STRING | NA Level II Code and Name |
| l3\_key | STRING | US Level III Code and Name |
| na\_l1code | STRING | Code for Level I Ecoregion (North America/CEC) |
| na\_l1name | STRING | Name for Level I Ecoregion (North America/CEC) |
| na\_l2code | STRING | Code for Level II Ecoregion (North America/CEC) |
| na\_l2name | STRING | Name for Level II Ecoregion (North America/CEC) |
| na\_l3code | STRING | Code for Level III Ecoregion (North America/CEC) |
| na\_l3name | STRING | Name for Level III Ecoregion (North America/CEC) |
| shape\_area | DOUBLE | Area of the feature's geometry in its original format |
| shape\_leng | DOUBLE | Length of the edges in the feature's geometry in its original format |
| us\_l3code | STRING | Code for Level III Ecoregion (US/USEPA) |
| us\_l3name | STRING | Name for Level III Ecoregion (US/USEPA) |
| l4\_key | STRING | US Level IV Code and Name |
| us\_l4code | STRING | Code for Level IV Ecoregion (US/USEPA) |
| us\_l4name | STRING | Name for Level IV Ecoregion (US/USEPA) |




### Terms of Use


**Terms of Use**


There are no restrictions on use of this US public domain data.




### Citations



Citations:
* Commission for Environmental Cooperation. 1997\. Ecological regions
of North America: toward a common perspective. Commission for Environmental
Cooperation, Montreal, Quebec, Canada. 71p. Map (scale 1:12,500,000\).
Revised 2006\.
* McMahon, G., S.M. Gregonis, S.W. Waltman, J.M. Omernik, T.D. Thorson,
J.A. Freeouf, A.H. Rorick, and J.E. Keys. 2001\. Developing a spatial
framework of common ecological regions for the conterminous United
States. Environmental Management 28(3\):293\-316\.
* Omernik, J.M. 1987\. Ecoregions of the conterminous United States.
Map (scale 1:7,500,000\). Annals of the Association of American
Geographers 77(1\):118\-125\.
* Omernik, J.M. 1995\. Ecoregions: A spatial framework for environmental
management. In: Biological Assessment and Criteria: Tools for Water
Resource Planning and Decision Making. Davis, W.S. and T.P. Simon
(eds.), Lewis Publishers, Boca Raton, FL. p. 49\-62\.
* Omernik, J.M. 2004\. Perspectives on the nature and definition of
ecological regions. Environmental Management 34(Supplement 1\):S27\-S38\.
* Omernik, J.M. and G.E. Griffith. 2014\. Ecoregions of the conterminous
United States: evolution of a hierarchical spatial framework. Environmental
Management 54(6\):1249\-1266\.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('EPA/Ecoregions/2013/L4');
varvisParams={
palette:['0a3b04','1a9924','15d812'],
min:0.0,
max:67800000000.0,
opacity:0.8,
};
varimage=ee.Image().float().paint(dataset,'shape_area');
Map.setCenter(-99.814,40.166,5);
Map.addLayer(image,visParams,'EPA/Ecoregions/2013/L4');
Map.addLayer(dataset,null,'for Inspector',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/EPA/EPA_Ecoregions_2013_L4)
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
varfvLayer=ui.Map.FeatureViewLayer('EPA/Ecoregions/2013/L4_FeatureView');

varvisParams={
color:{
property:'shape_area',
mode:'linear',
palette:['0a3b04','1a9924','15d812'],
min:0.0,
max:67800000000.0
},
opacity:0.8,
polygonStrokeOpacity:0
};

fvLayer.setVisParams(visParams);
fvLayer.setName('EPA/Ecoregions/2013/L4');

Map.setCenter(-99.814,40.166,5);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/EPA/EPA_Ecoregions_2013_L4_FeatureView)


[US EPA Ecoregions (Level IV)](/earth-engine/datasets/catalog/EPA_Ecoregions_2013_L4)

The U.S. Environmental Protection Agency (USEPA) provides the Ecoregions dataset to serve as a spatial framework for the research, assessment, management, and monitoring of ecosystems and ecosystem components. Ecoregions denote areas of general similarity in ecosystems and in the type, quality, and quantity of environmental resources. These general\-purpose regions are …

 EPA/Ecoregions/2013/L4,
 ecoregions,ecosystems,epa,table

2013\-04\-16T00:00:00Z/2013\-04\-17T00:00:00Z



 24\.5 \-124\.8 49\.4 \-66\.9
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








