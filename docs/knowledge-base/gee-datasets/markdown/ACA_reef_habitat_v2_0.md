



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Allen Coral Atlas (ACA) \- Geomorphic Zonation and Benthic Habitat \- v2\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================================================








Dataset Availability
2018\-01\-01T00:00:00Z–2021\-01\-01T00:00:00Z
Dataset Provider


[Allen Coral Atlas Partnership (ACA)](https://allencoralatlas.org/)


[University of Queensland (UQ)](https://www.uq.edu.au/)


[Arizona State University Center for Global Discovery and Conservation Science (ASU GDCS)](https://gdcs.asu.edu/)


[Coral Reef Alliance (CORAL)](https://coral.org/en/)


[Planet](https://www.planet.com/)


[Vulcan Inc. (Vulcan)](https://vulcan.com/)



Earth Engine Snippet


`ee.Image("ACA/reef_habitat/v2_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ACA/ACA_reef_habitat_v2_0)





Tags


[ocean](/earth-engine/datasets/tags/ocean)
[oceans](/earth-engine/datasets/tags/oceans)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)
coral
planet\-derived
reef
seagrass








#### Description



The [Allen Coral Atlas](https://allencoralatlas.org/) dataset maps the geomorphic
zonation and benthic habitat for the world's shallow coral reefs at 5 m pixel
resolution. Also included is a global reef extent product that maps additional
reef areas unable to be explicitly included in the geomorphic and benthic mapping.
The underlying satellite image data are temporal composites of [PlanetScope
satellite](https://www.planet.com/products/basemap/) imagery spanning 2018\-2020\.
The habitat maps are created via a machine learning approach with contextual
editing, using a range of imagery, bathymetry and derived products as input data,
trained via a globally consistent reference data set. A full description of the
methods and approaches can be found in the methods section of the [Allen Coral
Atlas website](https://allencoralatlas.org/methods/).


The first version
([v1\.0](https://developers.google.com/earth-engine/datasets/catalog/ACA_reef_habitat_v1_0))
of the Allen Coral Atlas was completed in Q4 2021, and this new version (v2\.0\) has
a wide range of improvements across the globe that incorporated both user feedback
on v1\.0 and new technical developments in mapping methodology. A brief overview of
the changes can be found
[here](https://allencoralatlas.org/blog/geomorphic-and-benthic-maps-2022-update/)
and a more comprehensive technical summary can be found
[here](https://storage.googleapis.com/coral-atlas-static-files/resources-page-materials/Allen_Coral_Atlas_2022_habitat_map_revisions.pdf).


The Allen Coral Atlas was funded by [Vulcan Inc.](https://vulcan.com/) and is
managed by the [Arizona State University Center for Global Discovery and
Conservation Science](https://gdcs.asu.edu/). Partners include
[Planet](https://www.planet.com/), the
[University of Queensland](https://www.uq.edu.au/), and the
[Coral Reef Alliance](https://coral.org/en/).


Scientific background publications:


* Lyons, M. B., Roelfsema, C. M., Kennedy, E. V., Kovacs, E. M., Borrego\-Acevedo, R., Markey, K., ... \& Murray, N. J. (2020\). Mapping the world's coral reefs using a global multiscale earth observation framework. Remote Sensing in Ecology and Conservation, 6(4\), 557\-568\. [doi:10\.1002/rse2\.157](https://doi.org/10.1002/rse2.157)
* Kennedy, E. V., Roelfsema, C. M., Lyons, M. B., Kovacs, E. M., Borrego\-Acevedo, R., Roe, M., ... \& Tudman, P. (2021\). Reef Cover, a coral reef classification for global habitat mapping from remote sensing. Scientific Data, 8(1\), 1\-20\. [doi:10\.1038/s41597\-021\-00958\-z](https://doi.org/10.1038/s41597-021-00958-z)
* Roelfsema, C. M., Lyons, M., Murray, N., Kovacs, E. M., Kennedy, E., Markey, K., ... \& Phinn, S. R. (2021\). Workflow for the generation of expert\-derived training and validation data: a view to global scale habitat mapping. Frontiers in Marine Science. [doi:10\.3389/fmars.2021\.643381](https://doi.org/10.3389/fmars.2021.643381)
* Li, J., Knapp, D. E., Lyons, M., Roelfsema, C., Phinn, S., Schill, S. R., \& Asner, G. P. (2021\). Automated global shallow water bathymetry mapping using Google Earth Engine. Remote Sensing, 13(8\), 1469\. [doi:10\.3390/rs13081469](https://doi.org/10.3390/rs13081469)
* Li, J., Knapp, D. E., Fabina, N. S., Kennedy, E. V., Larsen, K., Lyons, M. B., ... \& Asner, G. P. (2020\). A global coral reef probability map generated using convolutional neural networks. Coral Reefs, 39(6\), 1805\-1815\. [doi:10\.1007/s00338\-020\-02005\-6](https://doi.org/10.1007/s00338-020-02005-6)


Allen Coral Atlas maps, bathymetry and map statistics are © 2023 Allen
Coral Atlas Partnership and Vulcan, Inc.





### Bands



**Pixel Size**
  
5 meters



**Bands**




| Name | Description |
| --- | --- |
| `geomorphic` | Classification of geomorphic zonation. |
| `benthic` | Classification of dominant benthic composition. |
| `reef_mask` | Globally standardised reef extent product that integrates a number of global reef classification and bahtymetry products ("Reef Extent" on the Atlas portal). |


**geomorphic Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#000000 | Unmapped |
| 11 | \#77d0fc | Shallow Lagoon \- Shallow Lagoon is any closed to semi\-enclosed, sheltered, flat\-bottomed shallow sediment\-dominated lagoon area. |
| 12 | \#2ca2f9 | Deep Lagoon \- Deep Lagoon is any sheltered broad body of water semi\-enclosed to enclosed by reef, with a variable depth (but shallower than surrounding ocean) and a soft bottom dominated by reef\-derived sediment. |
| 13 | \#c5a7cb | Inner Reef Flat \- Inner Reef Flat is a low energy, sediment\-dominated, horizontal to gently sloping platform behind the Outer Reef Flat. |
| 14 | \#92739d | Outer Reef Flat \- Adjacent to the seaward edge of the reef, Outer Reef Flat is a level (near horizontal), broad and shallow platform that displays strong wave\-driven zonation |
| 15 | \#614272 | Reef Crest \- Reef Crest is a zone marking the boundary between the reef flat and the reef slope, generally shallow and characterized by highest wave energy absorbance. |
| 16 | \#fbdefb | Terrestrial Reef Flat \- Terrestrial Reef Flat is a broad, flat, shallow to semi\-exposed area of fringing reef found directly attached to land at one side, and subject to freshwater run\-off, nutrients and sediment. |
| 21 | \#10bda6 | Sheltered Reef Slope \- Sheltered Reef Slope is any submerged, sloping area extending into Deep Water but protected from strong directional prevailing wind or current, either by land or by opposing reef structures. |
| 22 | \#288471 | Reef Slope \- Reef Slope is a submerged, sloping area extending seaward from the Reef Crest (or Flat) towards the shelf break. Windward facing, or any direction if no dominant prevailing wind or current exists. |
| 23 | \#cd6812 | Plateau \- Plateau is any deeper submerged, hard\-bottomed, horizontal to gently sloping seaward facing reef feature. |
| 24 | \#befbff | Back Reef Slope \- Back Reef Slope is a complex, interior, \- often gently sloping \- reef zone occurring behind the Reef Flat. Of variable depth (but deeper than Reef Flat and more sloped), it is sheltered, sediment\-dominated and often punctuated by coral outcrops. |
| 25 | \#ffba15 | Patch Reef \- Patch Reef is any small, detached to semi\-detached lagoonal coral outcrop arising from sand\-bottomed area. |


**benthic Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#000000 | Unmapped |
| 11 | \#ffffbe | Sand \- Sand is any soft\-bottom area dominated by fine unconsolidated sediments. |
| 12 | \#e0d05e | Rubble \- Rubble is any habitat featuring loose, rough fragments of broken reef material. |
| 13 | \#b19c3a | Rock \- Rock is any exposed area of hard bare substrate. |
| 14 | \#668438 | Seagrass \- Seagrass is any habitat where seagrass is the dominant biota. |
| 15 | \#ff6161 | Coral/Algae \- Coral/Algae is any hard\-bottom area supporting living coral and/or algae. |
| 18 | \#9bcc4f | Microalgal Mats \- Microalgal Mats are any visible accumulations of microscopic algae in sandy sediments. |


**reef\_mask Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#000000 | Not reef |
| 1 | \#ffffff | Reef |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Allen Coral Atlas (2020\). Imagery, maps and monitoring of the world's tropical coral reefs. Zenodo. [doi:10\.5281/zenodo.3833242](https://doi.org/10.5281/zenodo.3833242)





### DOIs


* [https://doi.org/10\.5281/zenodo.3833242](https://doi.org/10.5281/zenodo.3833242)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('ACA/reef_habitat/v2_0');

// Teti'aroa, an atoll in French Polynesia.
Map.setCenter(-149.56194,-17.00872,13);
Map.setOptions('SATELLITE');

// The visualizations are baked into the image properties.

// Example mask application.
varreefExtent=dataset.select('reef_mask').selfMask();
Map.addLayer(reefExtent,{},'Global reef extent');

// Geomorphic zonation classification.
vargeomorphicZonation=dataset.select('geomorphic').selfMask();
Map.addLayer(geomorphicZonation,{},'Geomorphic zonation');

// Benthic habitat classification.
varbenthicHabitat=dataset.select('benthic').selfMask();
Map.addLayer(benthicHabitat,{},'Benthic habitat');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ACA/ACA_reef_habitat_v2_0)


[Allen Coral Atlas (ACA) \- Geomorphic Zonation and Benthic Habitat \- v2\.0](/earth-engine/datasets/catalog/ACA_reef_habitat_v2_0)

The Allen Coral Atlas dataset maps the geomorphic zonation and benthic habitat for the world's shallow coral reefs at 5 m pixel resolution. Also included is a global reef extent product that maps additional reef areas unable to be explicitly included in the geomorphic and benthic mapping. The underlying satellite …

 ACA/reef\_habitat/v2\_0,
 ocean,oceans,sentinel2\-derived

2018\-01\-01T00:00:00Z/2021\-01\-01T00:00:00Z



 \-33 \-180 33 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.5281/zenodo.3833242](https://doi.org/https://allencoralatlas.org/)
* [https://doi.org/10\.5281/zenodo.3833242](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/ACA_reef_habitat_v2_0)
* [https://doi.org/10\.5281/zenodo.3833242](https://doi.org/https://www.uq.edu.au/)
* [https://doi.org/10\.5281/zenodo.3833242](https://doi.org/https://gdcs.asu.edu/)
* [https://doi.org/10\.5281/zenodo.3833242](https://doi.org/https://coral.org/en/)
* [https://doi.org/10\.5281/zenodo.3833242](https://doi.org/https://www.planet.com/)
* [https://doi.org/10\.5281/zenodo.3833242](https://doi.org/https://vulcan.com/)
* [https://doi.org/10\.5281/zenodo.3833242](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/ACA_reef_habitat_v2_0)









