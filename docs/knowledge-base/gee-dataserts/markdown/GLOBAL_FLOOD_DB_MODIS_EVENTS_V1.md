



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global Flood Database v1 (2000\-2018\)


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================================








Dataset Availability
2000\-02\-17T00:00:00Z–2018\-12\-10T00:00:00Z
Dataset Provider


[Cloud to Street (C2S) / Dartmouth Flood Observatory (DFO)](http://global-flood-database.cloudtostreet.info/)



Earth Engine Snippet


`ee.ImageCollection("GLOBAL_FLOOD_DB/MODIS_EVENTS/V1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GLOBAL_FLOOD_DB/GLOBAL_FLOOD_DB_MODIS_EVENTS_V1)





Tags


[flood](/earth-engine/datasets/tags/flood)
[surface](/earth-engine/datasets/tags/surface)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[water](/earth-engine/datasets/tags/water)
c2s
cloudtostreet
dartmouth
dfo
gfd
inundation








#### Description



The Global Flood Database contains maps of the extent and
temporal distribution of 913 flood events occurring between 2000\-2018\. For more
information, see
[the associated journal article](https://doi.org/10.1038/s41586-021-03695-w).


Flood events were collected from
the [Dartmouth Flood Observatory](https://floodobservatory.colorado.edu/)
and used to collect MODIS imagery. The selected
913 events are those that were successfully mapped (passed quality control as
having significant inundation beyond permanent water) using 12,719 scenes from
Terra and Aqua MODIS sensors. Each pixel was classified as water or non\-water
at 250\-meter resolution during the full date range of each flood event and
subsequent data products were generated including maximum flood extent
("flooded" band) and the duration of inundation in days ("duration" band).
Water and non\-water classifications during a flood event include permanent
water (here resampling the 30\-meter
[JRC Global Surface Water dataset](https://global-surface-water.appspot.com/)
representing permanent water to 250\-meter resolution), which can be
masked out to isolate flood water using the "jrc\_perm\_water" band.
Extra data quality
bands were added representing cloud conditions during the flood event (e.g.,
"clear\_views" representing the number of clear days the flood was observed
between its start and end dates and "clear\_perc" representing the percentage of
clear day observation of the total event duration in days).


Each image in the ImageCollection represents the map of an individual flood.
The collection can be filtered
by date, country, or Dartmouth Flood Observatory original ID.





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `flooded` | None | 0 | 1 | Maximum extent of flood water during an event.* 1 \- area of surface water * 0 \- no water |
| `duration` | d | 0 | 65535 | Duration of surface water during an event in days. Pixel values indicate the number of composite days a pixel's area was considered water during an event. 3\-day MODIS composites were used. |
| `clear_views` | d | 0 | 65535 | Number of cloud\-free observations in days between the start and end day of each event. Cloud coverage is determined by the MODIS Quality Assurance band ('state\_1km'). |
| `clear_perc` | % | 0 | 100 | Percentage of clear view observations during a given flood event. This is equivalent to the 'clear\_views' band but normalized to the number of MODIS images per flood event. Cloud coverage is determined by the MODIS Quality Assurance band ('state\_1km'). |
| `jrc_perm_water` | None | 0 | 1 | Permanent water determined by the JRC Global Surface Water dataset using the 'transition' band. Resolution is maintained as the original 30\-meter resolution of the JRC dataset.* 1 \- permanent water * 0 \- non\-water. |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| id | INT | Unique catalog ID of flood event that aligns with the Dartmouth Flood Observatory (DFO). |
| cc | STRING | Three\-letter ISO country codes (in a list) for countries for which flood water was detected in watersheds intersecting the DFO event polygon. |
| countries | STRING | Country names (in a list) for countries for which flood water was detected in watersheds intersecting the DFO event polygon. |
| dfo\_centroid\_x | DOUBLE | Centroid longitude of DFO polygon estimating the location of a flood event (DFO database). |
| dfo\_centroid\_y | DOUBLE | Centroid latitude of DFO polygon estimating the location of a flood event (DFO database). |
| dfo\_country | STRING | Primary country of flooding (DFO database). |
| dfo\_other\_country | STRING | Secondary country of flooding (DFO database). |
| dfo\_displaced | INT | Estimated total number of people left homeless or evacuated after a flood event (DFO database). |
| dfo\_main\_cause | STRING | The main cause of a flood event in the DFO database. Not normalized. |
| dfo\_severity | DOUBLE | Severity of a flood event (DFO database):* 1 \- large flood events, significant damage to structure or agriculture, fatalities, and/or 5\-15 year reported interval since the last similar event * 1\.5 \- very large events: \>15 year but \<100 year recurrence interval * 2 \- extreme events: recurrence interval \>100 years) |
| dfo\_dead | INT | Estimated fatalities due to a flood event (DFO database). |
| dfo\_validation\_type | STRING | Primary source of flood event confirmation (DFO database). Not normalized. |
| glide\_index | STRING | [GLobal IDEntifier Number](https://glidenumber.net/glide/public/about.jsp). |
| gfd\_country\_code | STRING | Comma\-separated list of two\-letter FIPS country codes for countries intersecting with the watershed used as the area of interest in the water detection algorithm. |
| gfd\_country\_name | STRING | Country names (in a list) for countries intersecting with the watershed used as the area of interest in the water detection algorithm. |
| composite\_type | STRING | Number of days used for compositing in water detection algorithm. |
| threshold\_type | STRING | Type of thresholds used to classify water/ non\-water in water detection algorithm \- "otsu" or "standard". |
| threshold\_b1b2 | DOUBLE | Threshold value applied to the b2b1\-ratio used in the water detection algorithm. |
| threshold\_b7 | DOUBLE | Threshold value applied to band 7 (SWIR) used in the water detection algorithm. |
| otsu\_sample\_res | DOUBLE | Spatial resolution (in m) of the reducer used to build MODIS mosaic from which to then sample and estimate an otsu threshold (only available for flood events which used an otsu and not the default threshold). |
| slope\_threshold | DOUBLE | Value used to mask steep areas from water detection algorithm to minimize error from terrain shadows. |




### Terms of Use


**Terms of Use**


This work is licensed under the Creative Commons Attribution Non Commercial 4\.0
International license.




### Citations



Citations:
* Tellman, B., J.A. Sullivan, C. Kuhn, A.J. Kettner, C.S. Doyle, G.R.
Brakenridge, T. Erickson, D.A. Slayback. (Accepted.)
Satellites observe increasing proportion of population exposed
to floods. Nature.
[doi:10\.1038/s41586\-021\-03695\-w](https://doi.org/10.1038/s41586-021-03695-w)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vargfd=ee.ImageCollection('GLOBAL_FLOOD_DB/MODIS_EVENTS/V1');

// An individual flood event - flooding due to Hurricane Isaac in the USA.
varhurricaneIsaacDartmouthId=3977;
varhurricaneIsaacUsa=ee.Image(
gfd.filterMetadata('id','equals',hurricaneIsaacDartmouthId).first());
Map.setOptions('SATELLITE');
Map.setCenter(-90.2922,29.4064,9);
Map.addLayer(
hurricaneIsaacUsa.select('flooded').selfMask(),
{min:0,max:1,palette:'001133'},
'Hurricane Isaac - Inundation Extent');

// The duration (number of days a flood event lasted).
vardurationPalette=['c3effe','1341e8','051cb0','001133'];
Map.addLayer(
hurricaneIsaacUsa.select('duration').selfMask(),
{min:0,max:4,palette:durationPalette},
'Hurricane Isaac - Duration');

// Map all floods to generate the satellite-observed historical flood plain.
vargfdFloodedSum=gfd.select('flooded').sum();
Map.addLayer(
gfdFloodedSum.selfMask(),
{min:0,max:10,palette:durationPalette},
'GFD Satellite Observed Flood Plain');

// Overlay permanent water to distinguish flood water.
varjrc=gfd.select('jrc_perm_water').sum().gte(1);
Map.addLayer(
jrc.selfMask(),
{min:0,max:1,palette:'C3EFFE'},
'JRC Permanent Water');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GLOBAL_FLOOD_DB/GLOBAL_FLOOD_DB_MODIS_EVENTS_V1)


[Global Flood Database v1 (2000\-2018\)](/earth-engine/datasets/catalog/GLOBAL_FLOOD_DB_MODIS_EVENTS_V1)

The Global Flood Database contains maps of the extent and temporal distribution of 913 flood events occurring between 2000\-2018\. For more information, see the associated journal article. Flood events were collected from the Dartmouth Flood Observatory and used to collect MODIS imagery. The selected 913 events are those that were …

 GLOBAL\_FLOOD\_DB/MODIS\_EVENTS/V1,
 flood,surface,surface\-ground\-water,water

2000\-02\-17T00:00:00Z/2018\-12\-10T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








