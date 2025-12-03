



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WDOECM: Other Effective Area\-based Conservation Measures (polygons)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
======================================================================================================================================================================








Dataset Availability
2024\-05\-01T00:00:00Z–2030\-01\-01T00:00:00Z
Dataset Provider


[UN Environment World Conservation Monitoring Centre (UNEP\-WCMC) / Protected Planet](https://www.protectedplanet.net/)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("WCMC/WDOECM/current/polygons")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WCMC/WCMC_WDOECM_current_polygons)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("WCMC/WDOECM/current/polygons_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WCMC/WCMC_WDOECM_current_polygons_FeatureView)





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
| CONS\_OBJ | STRING | It refers to the primacy of conservation objectives. The field provides an indication of whether an OECM is managed with biodiversity conservation as a primary objective, secondary objective, or without conservation as an explicit objective. |
| DESIG | STRING | Designation of the OECMs in the native language. |
| DESIG\_ENG | STRING | Designation of the protected area or OECM in English. If the original language is English, this field will contain the same value as DESIG. No fixed values for national\-level designations. |
| DESIG\_TYPE | STRING | Designation type, one of: national, regional, international, or not applicable |
| GIS\_AREA | DOUBLE | Protected area total extent, including both marine (if applicable) and terrestrial areas, in square kilometers calculated by UNEP\-WCMC projecting the protected area polygon in the standard Mollweide projection and using GIS software tools. |
| GIS\_M\_AREA | DOUBLE | Protected area marine extent in square kilometers calculated by UNEP\-WCMC projecting the protected area polygon in the standard Mollweide projection and using GIS software tools. |
| GOV\_TYPE | STRING | Description of the decision\-making structure of a PA. One of: federal or national ministry or agency, sub\-national ministry or agency, government\-delegated management, transboundary governance, collaborative governance, joint governance, individual landowners, non\-profit organizations, for\-profit organizations, indigenous peoples, local communities, or not reported. |
| INT\_CRIT | STRING | International criteria, assigned by UNEP\-WCMC. For World Heritage and Ramsar sites only. |
| ISO3 | STRING | ISO3 Code. [ISO 3166\-3 character code](https://en.wikipedia.org/wiki/ISO_3166-3) of the country or territory where the OECM is located. |
| IUCN\_CAT | STRING | IUCN management category, one of: Ia (strict nature reserve), Ib (wilderness area), II (national park), III (natural monument or feature), IV (habitat/species management area), V (protected landscape/seascape), VI (PA with sustainable use of natural resources), not applicable, not assigned, or not reported. |
| MANG\_AUTH | STRING | Management authority. Agency, organization, individual or group that manages the OECM. |
| MANG\_PLAN | STRING | Link or reference to the PAs management plan. |
| MARINE | STRING | This field describes whether a PA falls totally or partially within the marine environment, one of: 0 (100% terrestrial PA), 1 (coastal: marine and terrestrial PA), or 2 (100% marine PA). |
| METADATAID | INT | Metadata ID, assigned by UNEP\-WCMC. Link to WDPA source table. |
| NAME | STRING | Name of the OECM as provided by the data provider. |
| NO\_TAKE | STRING | No take means that the taking of living or dead natural resources, inclusive of all methods of fishing, extraction, dumping, dredging and construction, is strictly prohibited in all or part of a marine PA. This is only applicable to PAs where the field marine \= 1 or 2\. One of: all, part, none, not reported, or not applicable (if MARINE field \= 0\). |
| NO\_TK\_AREA | DOUBLE | Area of the marine no\-take area in square kilometers. |
| ORIG\_NAME | STRING | Name of the PA in the original language. |
| OWN\_TYPE | STRING | Ownership type, one of: state, communal, individual landowners, for\-profit organizations, non\-profit organizations, joint ownership, multiple ownership, contested, or not Reported. |
| PARENT\_ISO | STRING | Parent ISO3 code. [ISO 3166\-3 character code](https://en.wikipedia.org/wiki/ISO_3166-3) of country where the PA is located. |
| PA\_DEF | STRING | PA definition. Whether this site meets the IUCN and/or CBD definition of a PA: 1\=yes, 0\=no (currently stored outside WDPA). |
| REP\_AREA | DOUBLE | The total OECMs extent, including both marine (if applicable) and terrestrial areas, in square kilometers provided by data provider as specified in the legal text for the site. |
| REP\_M\_AREA | DOUBLE | Marine area in square kilometers provided by the data provider. |
| STATUS | STRING | Status of a PA, one of: proposed, inscribed, adopted, designated, or established. |
| STATUS\_YR | INT | Year of enactment of status in the STATUS field. |
| SUB\_LOC | STRING | Sub\-national location. [ISO 3166\-2 sub\-national code](https://en.wikipedia.org/wiki/ISO_3166-2) where the PA is located. If the PA is in more than one state, province, region etc., multiple ISO\-3166\-2 codes can be listed separated by a comma and space. |
| SUPP\_INFO | STRING | Supplementary information supporting the categorization of the site as an OECM. |
| VERIF | STRING | Verification status, assigned by UNEP\-WCMC. One of: state verified, expert verified, not reported (for unverified data that was already in the WDPA prior to the inclusion of the ''Verification'' field). |
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
vartable=ee.FeatureCollection('WCMC/WDOECM/current/polygons');

varimage=table.reduceToImage({
properties:['REP_AREA'],
reducer:ee.Reducer.first()
});

varvisParams={
min:50000.0,
max:800000.0,
palette:['2ed033','5aff05','67b9ff','5844ff','0a7618','2c05ff'],
opacity:0.8
};

Map.setCenter(-4.14,27.33,5);

Map.addLayer(image,visParams,'Total OECMs extent');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WCMC/WCMC_WDOECM_current_polygons)
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
varfvLayer=ui.Map.FeatureViewLayer('WCMC/WDOECM/current/polygons_FeatureView');

varvisParams={
color:{
property:'REP_AREA',
mode:'linear',
palette:['2ed033','5aff05','67b9ff','5844ff','0a7618','2c05ff'],
min:0.0,
max:1550000.0
},
opacity:0.8
};

fvLayer.setVisParams(visParams);
fvLayer.setName('WCMC/WDOECM/current/polygons');

Map.setCenter(-4.14,27.33,5);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WCMC/WCMC_WDOECM_current_polygons_FeatureView)


[WDOECM: Other Effective Area\-based Conservation Measures (polygons)](/earth-engine/datasets/catalog/WCMC_WDOECM_current_polygons)

A geographically defined area other than a Protected Area, which is governed and managed in ways that achieve positive and sustained long\-term outcomes for the in situ conservation of biodiversity, with associated ecosystem functions and services and where applicable, cultural, spiritual, socio\-economic, and other locally relevant values. The WDOECM has …

 WCMC/WDOECM/current/polygons,
 boundaries,ecosystems,iucn,marine,mpa,protected,table,wcmc,wdpa

2024\-05\-01T00:00:00Z/2030\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








