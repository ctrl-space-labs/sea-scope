



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Fee: USGS GAP PAD\-US v2\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================








Dataset Availability
2018\-09\-01T00:00:00Z–2018\-09\-01T00:00:00Z
Dataset Provider


[US Geological Survey](https://www.usgs.gov/core-science-systems/science-analytics-and-synthesis/gap/science/protected-areas)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("USGS/GAP/PAD-US/v20/fee")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GAP_PAD-US_v20_fee)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("USGS/GAP/PAD-US/v20/fee_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GAP_PAD-US_v20_fee_FeatureView)





Tags


[conservation\-easements](/earth-engine/datasets/tags/conservation-easements)
[designation](/earth-engine/datasets/tags/designation)
[infrastructure\-boundaries](/earth-engine/datasets/tags/infrastructure-boundaries)
[management](/earth-engine/datasets/tags/management)
[ownership](/earth-engine/datasets/tags/ownership)
[protected\-areas](/earth-engine/datasets/tags/protected-areas)
[public\-lands](/earth-engine/datasets/tags/public-lands)
[table](/earth-engine/datasets/tags/table)
[usgs](/earth-engine/datasets/tags/usgs)








#### Description



PAD\-US is America's official national inventory of U.S. terrestrial and
marine protected areas that are dedicated to the preservation of biological
diversity and to other natural, recreation and cultural uses, managed for these
purposes through legal or other effective means. This database is separated
into 4 separate table assets: designation, easement, fee, and proclamation.


The PAD\-US 2\.0 dataset separates fee ownership from other data types (e.g.
management designations, conservation easements). The 'Fee' asset provides a
complete, parcel based inventory representing fee\-owned protected areas without
boundary gaps or overlaps between authoritative datasets provided by agencies.
Data gaps associated with ownership, overlaps, and minor discrepancies
(slivers) between agency boundaries remain as work continues.


The PAD\-US database strives to be a complete inventory of areas dedicated to
the preservation of biological diversity, and other natural (including
extraction), recreational or cultural uses, managed for these purposes through
legal or other effective means. PAD\-US is an aggregation of "best available"
spatial data provided by agencies and organizations at a point in time. This
includes both fee ownership of lands as well as management through leases,
easements, or other binding agreements. The data also tracks Congressional
designations, Executive designations, and administrative designations
identified in management plans (e.g. Bureau of Land Management's 'Area of
Environmental Concern'). These factors provide for a robust dataset offering a
spatial representation of the complex U.S. protected areas network. It is
important to have in mind a specific analysis question when approaching how to
work with the data. As a full inventory of areas aggregated from authoritative
source data, PAD\-US includes overlapping designation types and small boundary
discrepancies between agency datasets. Overlapping designations largely occur
in the Federal estate of the 'Designation' or 'Combined' feature classes (e.g.
'Wilderness Area' over a 'Wild and Scenic River' and 'National Forest').


It is important to note the presence of overlaps, especially when trying to
calculate area statistics; overlapping boundaries count the same area of ground
multiple times. While minor boundary discrepancies remain, most major overlaps
have been removed from the 'Fee' asset and this is the best source for
overall land area calculations by land manager ('Manager Name') within the
PAD\-US database (data gaps limit calculations by fee ownership or 'Owner
Name'). Statistics summarizing 'Public Access' or Protection Status ('GAP
Status Code') by managing agency or organization from an analysis of the PAD\-US
1\.4 'Combined' feature class are [available](https://www.usgs.gov/core-science-systems/science-analytics-and-synthesis/gap/science/pad-us-statistics-and-reports)
and will be updated with PAD\-US 2\.0\. As the PAD\-US database is a direct
aggregation of source data, the PAD\-US development team does not alter spatial
linework. The exception is to "clip" lands data along State boundary lines
(using the authoritative State boundary file provided by the U.S. Census
Bureau) and remove the small segments of boundaries created by this process
associated with State or local lands (not Federal or nonprofit lands). Some
boundary discrepancies (or slivers) remain in the dataset. Data overlaps have
been identified and are shared, along with the U.S. Census Bureau State
jurisdictional boundary file, with agency data stewards to facilitate edits in
source files that will then be incorporated in subsequent PAD\-US versions over
time. The PAD\-US database is built in collaboration with many partners and
data stewards.
[Information regarding data stewards is available](https://www.usgs.gov/core-science-systems/science-analytics-and-synthesis/gap/science/pad-us-data-stewards).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| Agg\_Src | STRING | Source of data aggregator. |
| Category | STRING | The type of protection: designation, easement, fee, marine, other, proclamation, or unknown. |
| Comments | STRING | Additional comments. |
| Date\_Est | STRING | Year protected area established. |
| Des\_Tp | STRING | The detailed type of designation, e.g. 'area of critical environmental concern', 'local park', 'national park', 'wilderness area', etc. |
| EsmtHldr | STRING | The organization that holds the easement. |
| EHoldTyp | STRING | The type of easement holder. |
| FeatClass | DOUBLE | Unique id. |
| GAP\_Sts | STRING | The level of protection or "status":* 1: managed for biodiversity, disturbance events proceed or are mimicked * 2: managed for biodiversity, disturbance events suppressed * 3: managed for multiple uses, subject to extractive (e.g. mining or logging) or OHV use * 4: no known mandate for biodiversity protection. |
| GAPCdDt | STRING | Date the status code was determined. |
| GAPCdSrc | STRING | Source of the status code. |
| GIS\_Acres | DOUBLE | Number of acres of the protected area calculated. |
| GIS\_Src | STRING | The source of the GIS data. |
| Src\_Date | STRING | The date the GIS data represent. |
| IUCN\_Cat | STRING | The level of protection using IUCN protection status:* Ia: Strict nature reserves * Ib: Wilderness areas * II: National park * III: Natural monument or feature * IV: Habitat/species management; Other Conservation Area; Unassigned * V: Protected landscape / seascape * VI: Protected area with sustainable use of natural resources |
| IUCNCtDt | STRING | Date of the IUCN category. |
| IUCNCtSrc | STRING | Source of the IUCN protected status. |
| Loc\_Ds | STRING | Designation of the protected area at the local level. |
| Loc\_Mang | STRING | The manager of the protected area. |
| Loc\_Nm | STRING | The name of the protected area. |
| Loc\_Own | STRING | The owner of the protected area. |
| Mang\_Name | STRING | The name of the managing organization. |
| Mang\_Type | STRING | The manager type. |
| Own\_Name | STRING | The name of the owner of the protected area. |
| Own\_Type | STRING | The type of owner organization. |
| Access | STRING | Accessibility to the protected area. |
| Access\_Dt | STRING | The date of the access. |
| Access\_Src | STRING | The source of the access data. |
| ID | STRING | The id of the protected area. |
| State\_Nm | STRING | State names in two letter abbreviations |
| Unit\_Nm | STRING | Units name |
| WDPA\_Cd | STRING | The site code associated with the WDPA dataset. |




### Terms of Use


**Terms of Use**


The Digital Object Identifier [doi:10\.5066/P955KPLE](https://doi.org/10.5066/P955KPLE) for PAD\-US 2\.0
provides the persistent reference that should be used to obtain the data for
use. The U.S. Geological Survey and all contributing data partners shall not be
held liable for improper or incorrect use of the data described and (or)
contained herein. All information is created with a specific end use or uses in
mind. This is especially true for GIS data, which is expensive to produce and
must be directed to meet the immediate program needs. These data were created
with the expectation that they would be used for other applications; however,
inappropriate uses are listed below. This list is in no way exhaustive but
should serve as a guide to assess whether a proposed use can or cannot be
supported by these data. For many uses, it is unlikely that PAD\-US will provide
the only data needed, and for uses with a regulatory outcome, authoritative
agency data and field surveys should verify the result. PAD\-US is recommended
for users seeking basic information about more than one agency or organizations
lands. Users should seek authoritative source data directly to answer questions
regarding one agency or those requiring more frequent updates. Ultimately, it
will be the responsibility of each data user to determine if these data can
answer the question being asked. Inappropriate uses include: Using PAD\-US for
applications or analyses associated with one agency or a particular unit
(agencies are always the best and authoritative source of their lands data and
many publish updates more frequently than PAD\-US). Using some data to map small
areas (less than thousands of hectares), typically requiring mapping resolution
at 1:24,000 scale (as boundary quality varies by data source) and using aerial
photographs or ground surveys in areas where data are incomplete. Combining
these data with other data finer than 1:100,000 scale to produce new hybrid
maps or answer queries. Generating specific areal measurements from the data
finer than the nearest thousand hectares. Representing boundaries as a legal
representation for regulation or acquisition. Establishing definite occurrence
or non\-occurrence of any feature for an exact geographic area. Determining
abundance, health, or condition of any feature. Using the data without
acquiring and reviewing the metadata.




### Citations



Citations:
* U.S. Geological Survey (USGS) Gap Analysis Project (GAP), 2018,
Protected Areas Database of the United States (PAD\-US): U.S.
Geological Survey data release, [doi:10\.5066/P955KPL](https://doi.org/10.5066/P955KPLE).





### DOIs


* [https://doi.org/10\.5066/P955KPLE](https://doi.org/10.5066/P955KPLE)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('USGS/GAP/PAD-US/v20/fee');

// Encode 'GAP_Sts' (protection level) as a number for visualization.
dataset=dataset.map(function(feature){
returnfeature.set('status',ee.Number.parse(feature.get('GAP_Sts')));
});

// Paint new 'status' value to an image for visualization.
vardatasetVis=ee.Image().byte().paint(dataset,'status');

varvisualization={
min:1,
max:4,
palette:['b1a44e','4eb173','4e5bb1','b14e8c']
};

Map.setCenter(-100.612,43.687,8);
Map.addLayer(datasetVis,visualization,'Protection status');
Map.addLayer(dataset,null,'FeatureCollection',false);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GAP_PAD-US_v20_fee)
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
varfvLayer=ui.Map.FeatureViewLayer('USGS/GAP/PAD-US/v20/fee_FeatureView');

varvisParams={
opacity:1,
color:{
property:'GAP_Sts',
categories:[
['1','b1a44e'],
['2','4eb173'],
['3','4e5bb1'],
['4','b14e8c']
]
}
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Protection status');

Map.setCenter(-100.612,43.687,8);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/USGS/USGS_GAP_PAD-US_v20_fee_FeatureView)


[Fee: USGS GAP PAD\-US v2\.0](/earth-engine/datasets/catalog/USGS_GAP_PAD-US_v20_fee)

PAD\-US is America's official national inventory of U.S. terrestrial and marine protected areas that are dedicated to the preservation of biological diversity and to other natural, recreation and cultural uses, managed for these purposes through legal or other effective means. This database is separated into 4 separate table assets: designation, …

 USGS/GAP/PAD\-US/v20/fee,
 conservation\-easements,designation,infrastructure\-boundaries,management,ownership,protected\-areas,public\-lands,table,usgs

2018\-09\-01T00:00:00Z/2018\-09\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5066/P955KPLE](https://doi.org/https://www.usgs.gov/core-science-systems/science-analytics-and-synthesis/gap/science/protected-areas)
* [https://doi.org/10\.5066/P955KPLE](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/USGS_GAP_PAD-US_v20_fee)









