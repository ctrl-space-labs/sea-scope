



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

OpenET eeMETRIC Monthly Evapotranspiration v2\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================================================








Dataset Availability
1999\-10\-01T00:00:00Z–2024\-12\-01T00:00:00Z
Dataset Provider


[OpenET, Inc.](https://openetdata.org/)



Earth Engine Snippet


`ee.ImageCollection("OpenET/EEMETRIC/CONUS/GRIDMET/MONTHLY/v2_0")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_EEMETRIC_CONUS_GRIDMET_MONTHLY_v2_0)





Cadence
1 Month
Tags


[evapotranspiration](/earth-engine/datasets/tags/evapotranspiration)
[gridmet\-derived](/earth-engine/datasets/tags/gridmet-derived)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[monthly](/earth-engine/datasets/tags/monthly)
[openet](/earth-engine/datasets/tags/openet)
[water](/earth-engine/datasets/tags/water)
[water\-vapor](/earth-engine/datasets/tags/water-vapor)








#### Description



Google Earth Engine implementation of the Mapping Evapotranspiration
at high Resolution with Internalized Calibration model (eeMETRIC)


eeMETRIC applies the advanced METRIC algorithms and process of Allen
et al. (2007; 2015\) and Allen et al. (2013b), where a singular
relationship between the near surface air temperature difference (dT)
and delapsed land surface temperature (TsDEM) is used to estimate sensible
heat flux (H) and is applied to each Landsat scene. Automated selection of
the hot and cold pixels for an image generally follows a statistical
isolation procedure described by Allen et al. (2013a) and ReVelle, Kilic
and Allen (2019a,b). The calibration of H in eeMETRIC utilizes alfalfa
reference ET calculated from the NLDAS gridded weather dataset using a
fixed 15% reduction in computed reference ET to account for known biases
in the gridded data set. The fixed reduction does not impact the
calibration accuracy of eeMETRIC and mostly reduces impacts of boundary
layer buoyancy correction.


The identification of candidates for pools of hot and cold pixels has
evolved in the eeMETRIC implementation of METRIC. The new automated
calibration process incorporates the combination of methodologies and
approaches that stem from two development branches of EEFlux (Allen
et al., 2015\). The first branch focused on improving the automated pixel
selection process using standard lapse rates for land surface temperature
(LST) without any further spatial delapsing (ReVelle et al., 2019b). The
second branch incorporated a secondary spatial delapsing of LST as well as
changes to the pixel selection process (ReVelle et al., 2019a). The final,
combined approach is described by Kilic et al. (2021\).


eeMETRIC employs the aerodynamic\-related functions in complex terrain
(mountains) developed by Allen et al. (2013b) to improve estimates for
aerodynamic roughness, wind speed and boundary layer stability as related
to estimated terrain roughness, position on a slope and wind direction.
These functions tend to increase estimates for H (and reduce ET) on
windward slopes and may reduce H (and increase ET) on leeward slopes.
Other METRIC functions employed in eeMETRIC that have been added since
the descriptions provided in Allen et al. (2007 and 2011\) include
reduction in soil heat flux (G) in the presence of organic mulch on the
ground surface, use of an excess aerodynamic resistance for shrublands,
use of the Perrier function for trees identified as forest (Allen et
al., 2018; Santos et al., 2012\) and aerodynamic estimation of evaporation
from open water rather than using energy balance (Jensen and Allen 2016;
Allen et al., 2018\). In 2022, the Perrier function was applied to tree
(orchard) crops and a 3\-source partitioning of bulk surface temperature
into canopy temperature, shaded soil temperature and sunlit soil
temperature was applied to both orchards and vineyards. These latter
applications were made where orchards and vineyards are identified by
CDL or, in California, by a state\-sponsored land use system. These
functions and other enhancements to the original METRIC model are described
in the most current METRIC users manual (Allen et al., 2018\). eeMETRIC uses
the atmospherically corrected surface reflectance and LST from Landsat
Collection 2 Level 2, with fallback to Collection 2 Level 1 when needed for
near real\-time estimates.


[Additional information](https://openetdata.org/methodologies/)





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `et` | mm | eeMETRIC ET value |
| `count` | count | Number of cloud free values |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| build\_date | STRING | Date assets were built |
| cloud\_cover\_max | DOUBLE | Maximum CLOUD\_COVER\_LAND percent value for Landsat images included in interpolation |
| collections | STRING | List of Landsat collections for Landsat images included in the interpolation |
| core\_version | STRING | OpenET core library version |
| end\_date | STRING | End date of month |
| et\_reference\_band | STRING | Band in et\_reference\_source that contains the daily reference ET data |
| et\_reference\_resample | STRING | Spatial interpolation mode to resample daily reference ET data |
| et\_reference\_source | STRING | Collection ID for the daily reference ET data |
| interp\_days | DOUBLE | Maximum number of days before and after each image date to include in interpolation |
| interp\_method | STRING | Method used to interpolate between Landsat model estimates |
| interp\_source\_count | DOUBLE | Number of available images in the interpolation source image collection for the target month |
| mgrs\_tile | STRING | MGRS grid zone ID |
| model\_name | STRING | OpenET model name |
| model\_version | STRING | OpenET model version |
| scale\_factor\_count | DOUBLE | Scaling factor that should be applied to the count band |
| scale\_factor\_et | DOUBLE | Scaling factor that should be applied to the et band |
| start\_date | STRING | Start date of month |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Kilic, A., Allen, R.G., Blankenau, P., ReVelle, P., Ozturk, D. and
Huntington, J., 2021\. Global production and free access to Landsat\-scale
Evapotranspiration with EEFlux and eeMETRIC. In 6th Decennial National
Irrigation Symposium, 6\-8, December 2021, San Diego, California
(p. 1\). American Society of Agricultural and Biological Engineers.
[doi:10\.13031/irrig.2020\-038](https://doi.org/10.13031/irrig.2020-038)
* Allen, R.G., Tasumi, M., Morse, A. and Trezza, R., 2005\. A Landsat\-based
energy balance and evapotranspiration model in Western US water rights
regulation and planning. Irrigation and Drainage systems, 19,
pp.251\-268\.
[doi:10\.1007/s10795\-005\-5187\-z](https://doi.org/10.1007/s10795-005-5187-z)
* Allen, R.G., Tasumi, M. and Trezza, R., 2007\. Satellite\-based energy
balance for mapping evapotranspiration with internalized calibration
(METRIC)—Model. Journal of irrigation and drainage engineering, 133(4\),
pp.380\-394\.
[doi:10\.1029/2006JD007506](https://doi.org/10.1029/2006JD007506)
* Allen, R., Irmak, A., Trezza, R., Hendrickx, J.M., Bastiaanssen, W. and
Kjaersgaard, J., 2011\. Satellite\-based ET estimation in agriculture
using SEBAL and METRIC. Hydrological Processes, 25(26\), pp.4011\-4027\.
[doi:10\.1002/hyp.8408](https://doi.org/10.1002/hyp.8408)
* Allen, R.G., Burnett, B., Kramber, W., Huntington, J., Kjaersgaard, J.,
Kilic, A., Kelly, C. and Trezza, R., 2013a. Automated calibration of the
metric\-landsat evapotranspiration process. JAWRA Journal of the American
Water Resources Association, 49(3\), pp.563\-576\.
[doi:10\.1111/jawr.12056](https://doi.org/10.1111/jawr.12056)
* Allen, R.G., Trezza, R., Kilic, A., Tasumi, M. and Li, H., 2013b.
Sensitivity of Landsat\-scale energy balance to aerodynamic variability
in mountains and complex terrain. JAWRA Journal of the American Water
Resources Association, 49(3\), pp.592\-604\.
[doi:10\.1111/jawr.12055](https://doi.org/10.1111/jawr.12055)
* Allen, R.G., Morton, C., Kamble, B., Kilic, A., Huntington, J., Thau,
D., Gorelick, N., Erickson, T., Moore, R., Trezza, R. and Ratcliffe, I.,
2015\. EEFlux: A Landsat\-based evapotranspiration mapping tool on the
Google Earth Engine. In 2015 ASABE/IA Irrigation Symposium: Emerging
Technologies for Sustainable Irrigation\-A Tribute to the Career of Terry
Howell, Sr. Conference Proceedings (pp. 1\-11\). American Society of
Agricultural and Biological Engineers.
[doi:10\.13031/irrig.20152143511](https://doi.org/10.13031/irrig.20152143511)
* Jensen, M.E. and R.G. Allen (ed.). 2016\. Evaporation,
evapotranspiration, and irrigation water requirements. Manuals of
Practice no. 70 (2nd edition). Task Committee on Revision of Manual 70,
2016, April. American Society of Civil Engineers. Reston, VA. 744 p.
[doi:10\.1061/9780784414057](https://doi.org/10.1061/9780784414057)
* Kilic, A., Allen, R., Trezza, R., Ratcliffe, I., Kamble, B., Robison,
C. and Ozturk, D., 2016\. Sensitivity of evapotranspiration retrievals
from the METRIC processing algorithm to improved radiometric
resolution of Landsat 8 thermal data and to calibration bias in
Landsat 7 and 8 surface temperature. Remote Sensing of Environment,
185, pp.198\-209\.
[doi:10\.1016/j.rse.2016\.07\.011](https://doi.org/10.1016/j.rse.2016.07.011)
* ReVelle, P., A. Kilic and R.G. Allen. 2019a. Updated Calibration
Description: Spatial Delapsing in eeMETRIC. Research Note. School of
Natural Resources, University of Nebraska\-Lincoln and University of
Idaho. 9 p.
* ReVelle, P., A. Kilic and R.G. Allen. 2019b. Updated Calibration
Description: Automated Pixel Selection Method in eeMETRIC. Research
Note. School of Natural Resources, University of Nebraska\-Lincoln and
University of Idaho. 20 p.
* Santos, C., Lorite, I.J., Allen, R.G. and Tasumi, M., 2012\. Aerodynamic
parameterization of the satellite\-based energy balance (METRIC) model
for ET estimation in rainfed olive orchards of Andalusia, Spain. Water
Resources Management, 26, pp.3267\-3283\.
[doi:10\.1007/s11269\-012\-0071\-8](https://doi.org/10.1007/s11269-012-0071-8)





### DOIs


* [https://doi.org/10\.13031/irrig.2020\-038](https://doi.org/10.13031/irrig.2020-038)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('OpenET/EEMETRIC/CONUS/GRIDMET/MONTHLY/v2_0')
.filterDate('2020-01-01','2021-01-01');

// Compute the annual evapotranspiration (ET) as the sum of the monthly ET
// images for the year.
varet=dataset.select('et').sum();

varvisualization={
min:0,
max:1400,
palette:[
'9e6212','ac7d1d','ba9829','c8b434','d6cf40','bed44b','9fcb51',
'80c256','61b95c','42b062','45b677','49bc8d','4dc2a2','51c8b8',
'55cece','4db4ba','459aa7','3d8094','356681','2d4c6e',
]
};

Map.setCenter(-100,38,5);

Map.addLayer(et,visualization,'OpenET eeMETRIC Annual ET');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OpenET/OpenET_EEMETRIC_CONUS_GRIDMET_MONTHLY_v2_0)


[OpenET eeMETRIC Monthly Evapotranspiration v2\.0](/earth-engine/datasets/catalog/OpenET_EEMETRIC_CONUS_GRIDMET_MONTHLY_v2_0)

Google Earth Engine implementation of the Mapping Evapotranspiration at high Resolution with Internalized Calibration model (eeMETRIC) eeMETRIC applies the advanced METRIC algorithms and process of Allen et al. (2007; 2015\) and Allen et al. (2013b), where a singular relationship between the near surface air temperature difference (dT) and delapsed land …

 OpenET/EEMETRIC/CONUS/GRIDMET/MONTHLY/v2\_0,
 evapotranspiration,gridmet\-derived,landsat\-derived,monthly,openet,water,water\-vapor

1999\-10\-01T00:00:00Z/2024\-12\-01T00:00:00Z



 25 \-126 50 \-66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.13031/irrig.2020\-038](https://doi.org/https://openetdata.org/)
* [https://doi.org/10\.13031/irrig.2020\-038](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OpenET_EEMETRIC_CONUS_GRIDMET_MONTHLY_v2_0)









