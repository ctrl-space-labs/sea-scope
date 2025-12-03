



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WDOECM: Other Effective Area\-based Conservation Measures (points)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
====================================================================================================================================================================








Dataset Availability
2024\-05\-01T00:00:00Z–2030\-01\-01T00:00:00Z
Dataset Provider


[UN Environment World Conservation Monitoring Centre (UNEP\-WCMC) / Protected Planet](https://www.protectedplanet.net/)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("WCMC/WDOECM/current/points")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WCMC/WCMC_WDOECM_current_points)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("WCMC/WDOECM/current/points_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WCMC/WCMC_WDOECM_current_points_FeatureView)





Tags


[boundaries](/earth-engine/datasets/tags/boundaries)
[ecosystems](/earth-engine/datasets/tags/ecosystems)
[iucn](/earth-engine/datasets/tags/iucn)
[marine](/earth-engine/datasets/tags/marine)
[mpa](/earth-engine/datasets/tags/mpa)
[protected](/earth-engine/datasets/tags/protected)
[table](/earth-engine/datasets/tags/table)
[wcmc](/earth-engine/datasets/tags/wcmc)
[wdpa](/earth-engine/datasets/tags/wdpa)








#### Description



A geographically defined area other than a Protected Area, which is governed
and managed in ways that achieve positive and sustained long\-term outcomes
for the in situ conservation of biodiversity, with associated ecosystem
functions and services and where applicable, cultural, spiritual,
socio\-economic, and other locally relevant values.


The WDOECM has two feature classes with associated spatial
and tabular data.
The World Database on Other Effective Area\-based Conservation Measures
(WDOECM) is a global repository of information on Other Effective
Area\-based Conservation Measures (OECMs). It is managed by the United
Nations Environment Programme's World Conservation Monitoring Centre
(UNEP\-WCMC) with support from the Convention on Biological Diversity
(CBD).


**WDOECM User Manual.** For details including methodologies,standards, data
providers, metadata field definitions and descriptions, refer
to the [WDOECM User Manual](https://wdpa.s3-eu-west-1.amazonaws.com/WDPA_Manual/English/WDPA_WDOECM_Manual_1_6.pdf).


**Asset Naming Conventions.** WCMC updates the WDOECM on a
monthly basis. The most recent version is always available as
WCMC/WDOECM/current/polygons and WCMC/WDOECM/current/points. Historical
versions, starting with May 2024, are available in the format
WCMC/WDOECM/YYYYMM/polygons and WCMC/WDOECM/YYYYMM/points.


Please see the [WDOECM User Manual](https://wdpa.s3-eu-west-1.amazonaws.com/WDPA_Manual/English/WDPA_WDOECM_Manual_1_6.pdf)
for additional details on the field list.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| CONS\_OBJ | STRING | Designation type, categorized as National, Regional, International, or Not Applicable. |
| DESIG | STRING | Designation of the protected area or OECM in the native language, provided by the data provider. |
| DESIG\_ENG | STRING | Designation of the protected area or OECM in English. If the original language is English, this field will contain the same value as DESIG. No fixed values for national\-level designations. |
| DESIG\_TYPE | STRING | Designation type, categorized as National, Regional, International, or Not Applicable. |
| GOV\_TYPE | STRING | Governance type under which the protected area or OECM operates, such as Federal or National Ministry or Agency, Sub\-national Ministry or Agency, Collaborative governance, etc. |
| INT\_CRIT | STRING | International criteria used for World Heritage Sites and Ramsar sites, assigned by UNEP\-WCMC. |
| ISO3 | STRING | ISO3 Code. [ISO 3166\-3 character code](https://en.wikipedia.org/wiki/ISO_3166-3) of the country or territory where the protected area or OECM is located. |
| IUCN\_CAT | STRING | IUCN management category classifies protected areas according to their management objectives. Categories include Ia (Strict Nature Reserve), II (National Park), VI (Protected Area with sustainable use of natural resources), etc. |
| MANG\_AUTH | STRING | Management authority responsible for managing the protected area or OECM. |
| MANG\_PLAN | STRING | Indicates whether a management plan exists for the protected area or OECM. |
| MARINE | STRING | Indicates whether the area is terrestrial or marine. Values: 0 for terrestrial, 1 for coastal, and 2 for marine. Essential for understanding the nature of the protected area. |
| METADATAID | INT | Unique identifier for the metadata record associated with the protected area or OECM. |
| NAME | STRING | Legal name or other name assigned to the protected area or OECM in Latin characters. |
| NO\_TAKE | STRING | No\-take areas within the protected area or OECM where extractive activities are prohibited. Values include All, Part, None, Not Reported, and Not Applicable. |
| NO\_TK\_AREA | DOUBLE | Area of the no\-take zone within the protected area or OECM, measured in square kilometers. |
| ORIG\_NAME | STRING | Original name of the protected area or OECM in its original language or characters. |
| OWN\_TYPE | STRING | Ownership type of the land and/or waters within the protected area or OECM. Accepted values include State, Communal, Individual landowners, For\-profit organizations, etc. |
| PARENT\_ISO | STRING | Parent ISO3 code. [ISO 3166\-3 character code](https://en.wikipedia.org/wiki/ISO_3166-3) of the parent country if the protected area or OECM spans multiple countries. |
| PA\_DEF | STRING | Indicates whether the area meets the IUCN definition of a protected area. Values: 1 for yes, 0 for no (stored outside WDPA). |
| REP\_AREA | DOUBLE | The total reported area of the protected area or OECM in square kilometers, including both marine (if applicable) and terrestrial areas, as specified in the legal text. |
| REP\_M\_AREA | DOUBLE | Reported marine area in square kilometers within the protected area or OECM. |
| STATUS | STRING | Current status of the protected area or OECM, such as Proposed, Designated, or Established. |
| STATUS\_YR | INT | Year when the current status of the protected area or OECM was enacted. |
| SUB\_LOC | STRING | Sub\-national location or administrative region where the protected area or OECM is situated. If the PA is in more than one region, multiple ISO\-3166\-2 codes can be listed. |
| SUPP\_INFO | STRING | Supplementary information supporting the categorization of the site as an OECM. |
| VERIF | STRING | Verification status of the data, indicating whether it has been verified by state authorities or other recognized entities. Values: State Verified, Expert Verified, or Not Reported. |
| WDPAID | DOUBLE | Unique identifier for a protected area (PA), assigned by UNEP\-WCMC. |
| WDPA\_PID | STRING | Unique identifier for parcels or zones within a PA, assigned by UNEP\-WCMC. |




### Terms of Use


**Terms of Use**


Please visit the [full terms and conditions page](https://www.protectedplanet.net/c/terms-and-conditions)
of Protected Planet. Select highlights below:


**No Commercial Use.** Neither (a) the WDOECM Materials nor (b) any work
derived from or based upon the WDOECM Materials ("Derivative Works")
may be put to Commercial Use without the prior written permission
of UNEP\-WCMC. "Commercial Use" means a) any use by, on behalf
of, or to inform or assist the activities of, a commercial entity
(an entity that operates 'for profit') or b) use by any individual
or non\-profit entity for the purposes of revenue generation.


**Disclaimer.** The designations of geographical entities
in any Data Set do not imply the expression of any view or opinion
whatsoever on the part of UNEP or WCMC concerning the legal status
of any country, territory, or area, or of its authorities, or
concerning the delimitation of its frontiers or boundaries.


**Attribution.** You must ensure that the citation is always
clearly reproduced in any publication or analysis involving the
WDOECM Materials in any derived form or format.




### Citations



Citations:
* UNEP\-WCMC and IUCN (year), Protected Planet: The World Database
on OECM Database \[On\-line], \[insert month/year of the
version used], Cambridge, UK: UNEP\-WCMC and IUCN Available at:
www.protectedplanet.net.





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.FeatureCollection('WCMC/WDOECM/current/points');

dataset=dataset.style({
color:'0000FF',
pointSize:3,
});

Map.setCenter(124.49,11.63,6);

Map.addLayer(dataset,{},'OECMs points');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WCMC/WCMC_WDOECM_current_points)
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
varfvLayer=ui.Map.FeatureViewLayer('WCMC/WDOECM/current/points_FeatureView');

varvisParams={
color:'4285F4',
pointShape:'circle',
pointSize:6,
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Protected Area Points');

Map.setCenter(124.49,11.63,6);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WCMC/WCMC_WDOECM_current_points_FeatureView)


[WDOECM: Other Effective Area\-based Conservation Measures (points)](/earth-engine/datasets/catalog/WCMC_WDOECM_current_points)

A geographically defined area other than a Protected Area, which is governed and managed in ways that achieve positive and sustained long\-term outcomes for the in situ conservation of biodiversity, with associated ecosystem functions and services and where applicable, cultural, spiritual, socio\-economic, and other locally relevant values. The WDOECM has …

 WCMC/WDOECM/current/points,
 boundaries,ecosystems,iucn,marine,mpa,protected,table,wcmc,wdpa

2024\-05\-01T00:00:00Z/2030\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








