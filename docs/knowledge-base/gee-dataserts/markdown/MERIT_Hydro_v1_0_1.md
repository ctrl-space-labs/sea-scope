



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

MERIT Hydro: Global Hydrography Datasets


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==========================================================================================================================================








Dataset Availability
1987\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[Dai Yamazaki (University of Tokyo)](http://hydro.iis.u-tokyo.ac.jp/~yamadai/MERIT_Hydro/index.html)



Earth Engine Snippet


`ee.Image("MERIT/Hydro/v1_0_1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MERIT/MERIT_Hydro_v1_0_1)





Tags


[dem](/earth-engine/datasets/tags/dem)
[elevation](/earth-engine/datasets/tags/elevation)
[flow\-direction](/earth-engine/datasets/tags/flow-direction)
[hand](/earth-engine/datasets/tags/hand)
[hydrography](/earth-engine/datasets/tags/hydrography)
[hydrosheds](/earth-engine/datasets/tags/hydrosheds)
[merit](/earth-engine/datasets/tags/merit)
[river\-width](/earth-engine/datasets/tags/river-width)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[upstream\-drainage\-area](/earth-engine/datasets/tags/upstream-drainage-area)








#### Description



MERIT Hydro is a new global flow direction map at 3 arc\-second resolution (\~90
m at the equator) derived from the version 1\.0\.3 of the MERIT DEM elevation data
and water body datasets (G1WBM, GSWO and OpenStreetMap).


MERIT Hydro contains the output of a new algorithm that
extracts river networks near\-automatically by separating actual inland basins from
noise caused by the errors in input elevation data. After a minimum
amount of hand\-editing, the constructed hydrography map shows good agreement with
existing quality\-controlled river network datasets in terms of flow accumulation
area and river basin shape (see Figure 9a in the paper). The location of river
streamlines was realistically aligned with existing satellite\-based global
river channel data (see Figure 10a in the paper). Relative error
in the drainage area was smaller than 0\.05 for 90% of GRDC gauges, confirming
the accuracy of the delineated global river networks. Discrepancies in flow accumulation
area were found mostly in arid river basins containing depressions that are occasionally
connected at high water levels and thus resulting in uncertain watershed boundaries.


MERIT Hydro improves on existing global hydrography datasets in terms of spatial
coverage (between 90N and 60S) and representation of small streams, mainly due
to increased availability of high\-quality baseline geospatial datasets.


[You can use this web app to visualize MERIT Hydro data.](https://meritdataset.users.earthengine.app/view/merit-hydro-visualization-and-interactive-map)
[The app's source code is available.](https://github.com/google/earthengine-community/blob/master/datasets/scripts/Hydro_Visualization.js)


Known Problems:


* River width (Update from GWD\-LR v1\): Width algorithm was updated to consider
sub\-pixel water fraction. Now, 30 m water map is used for width calculation at
90 m resolution. Currently river width is calculated for each channel separately
in braided/anabranching sections. Merged river width should be calculated.
* Water body map: There are some inconsistencies between the DEM land sea mask and
wate body data (such as new islands along the coast). The quality of OpenStreeetMap
water body layer is not uniform in all areas.
* Channel bifurcations: Channel bifurcation is not well represented in the current
version. Each pixel is assumed to have only one downstream direction. Secondary
(or multiple) downstream direction should be considered, to represent complex
river networks in the delta regions, floodplains, and braided rivers.
* Underground rivers/tunnels: Major underground rivers/tunnels should be implemented
to improve large\-scale water balance.
* River/lake separation: Rivers and lakes need to be separated better for some applications.
* Below\-sea\-level areas: The areas below sea level in coastal regions are not well
represented in adjusted elevation data.
* Flow direction over glaciers: Flow direction over glaciers is not well represented,
because the elevation of glacier centerline is higher than glacier edge.
* Supplementary data: It would be better to add location of GRDC gauging stations, water
falls, reservoirs, etc.


Data Sources:


* [U\-Tokyo MERIT DEM](http://hydro.iis.u-tokyo.ac.jp/%7Eyamadai/MERIT_DEM/index.html)
* [U\-Tokyo G1WBM water body data](http://hydro.iis.u-tokyo.ac.jp/%7Eyamadai/G3WBM/index.html)
* [OpenStreetMap water body layer](http://hydro.iis.u-tokyo.ac.jp/%7Eyamadai/OSM_water/index.html)
* [EC\-JRC Global Surface Water Occurrence](http://hydro.iis.u-tokyo.ac.jp/%7Eyamadai/G3WBM/index.html)
* [U\-Maryland Landsat forest cover data](https://glad.earthengine.app/view/global-forest-change)





### Bands



**Pixel Size**
  
92\.77 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `elv` | m | Elevation |
| `dir` | None | Flow Direction (Local Drainage Direction)* 1: east * 2: southeast * 4: south * 8: southwest * 16: west * 32: northwest * 64: north * 128: northeast * 0: river mouth * \-1: inland depression |
| `wth` | None | River channel width at the channel centerlines. River channel width is calculated by the method described in \[Yamazaki et al. 2012, WRR], with some improvements/changes on the algorithm. |
| `wat` | None | Land and permanent water* 0: Land * 1: permanent water |
| `upa` | km^2 | Upstream drainage area (flow accumulation area) |
| `upg` | Number of upstream pixels | Upstream drainage pixel (flow accumulation grid). |
| `hnd` | m | Hydrologically adjusted elevations, also know as "hand" (height above the nearest drainage). The elevations are adjusted to satisfy the condition "downstream is not higher than its upstream" while minimizing the required modifications from the original DEM. The elevation above EGM96 geoid is represented in meters, and the vertical increment is set to 10cm. For detailed method, see \[Yamazaki et al., 2012, WRR]. |
| `viswth` | None | Visualization of the river channel width. |




### Terms of Use


**Terms of Use**


Citation to the paper is adequate if you simply use MERIT Hydro. If you
asked for help for additional handling/editing of the dataset, or if your research
outcome highly depends on the product, the developer would request co\-authorship.


MERIT Hydro is licensed under a Creative Commons "CC\-BY\-NC 4\.0" or Open
Data Commons "Open Database License (ODbL 1\.0\)". With a dual license, you can
choose an appropriate license for you.


To view a copy of these license, please visit:


* [CC\-BY\-NC 4\.0 license](https://creativecommons.org/licenses/by-nc/4.0/):
Non\-Commercial Use with less restriction.
* [ODbL 1\.0 license](https://opendatacommons.org/licenses/odbl/summary/):
Commectial Use is OK, but the derived data based on MERIT Hydro should be made
publicly available under the same ODbL license. For example, if you create a
flood hazard map using MERIT Hydro and you would like to provide a COMMERCIAL
service based on that, you have to make the hazard map PUBLICLY AVAILABLE under
OdBL license.


Note that the above license terms are applied to the "derived data" based
on MERIT Hydro, while they are not applied to "produced work / artwork" created
with MERIT Hydro (such as figures in a journal paper). The users may have a
copyright of the artwork and may assign any license, when the produced work
is not considered as "derived data".


By downloading and using the data the user agrees to the terms and
conditions of the license. Notwithstanding this free license, we ask users to
refrain from redistributing the data in whole in its original format on other
websites without the explicit written permission from the authors.


The copyright of MERIT Hydro is held by the developers, 2019, all rights reserved.




### Citations



Citations:
* Yamazaki D., D. Ikeshima, J. Sosa, P.D. Bates, G.H. Allen, T.M. Pavelsky.
MERIT Hydro: A high\-resolution global hydrography map based on latest
topography datasets
Water Resources Research, vol.55, pp.5053\-5073, 2019,
[doi:10\.1029/2019WR024873](https://doi.org/10.1029/2019WR024873)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('MERIT/Hydro/v1_0_1');

varvisualization={
bands:['viswth'],
};

Map.setCenter(90.301,23.052,10);

Map.addLayer(dataset,visualization,'River width');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/MERIT/MERIT_Hydro_v1_0_1)


[MERIT Hydro: Global Hydrography Datasets](/earth-engine/datasets/catalog/MERIT_Hydro_v1_0_1)

MERIT Hydro is a new global flow direction map at 3 arc\-second resolution (\~90 m at the equator) derived from the version 1\.0\.3 of the MERIT DEM elevation data and water body datasets (G1WBM, GSWO and OpenStreetMap). MERIT Hydro contains the output of a new algorithm that extracts river networks …

 MERIT/Hydro/v1\_0\_1,
 dem,elevation,flow\-direction,hand,hydrography,hydrosheds,merit,river\-width,surface\-ground\-water,upstream\-drainage\-area

1987\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








