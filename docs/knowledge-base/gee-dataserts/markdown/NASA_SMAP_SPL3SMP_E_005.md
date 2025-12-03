



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

SPL3SMP\_E.005 SMAP L3 Radiometer Global Daily 9 km Soil Moisture


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================================








Dataset Availability
2015\-03\-31T12:00:00Z–2023\-12\-03T12:00:00Z
Dataset Provider


[Google and NSIDC](https://nsidc.org/data/spl3smp_e/versions/5)



Earth Engine Snippet


`ee.ImageCollection("NASA/SMAP/SPL3SMP_E/005")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_SMAP_SPL3SMP_E_005)





Cadence
1 Day
Tags


[drought](/earth-engine/datasets/tags/drought)
[nasa](/earth-engine/datasets/tags/nasa)
[smap](/earth-engine/datasets/tags/smap)
[soil](/earth-engine/datasets/tags/soil)
[soil\-moisture](/earth-engine/datasets/tags/soil-moisture)
[surface](/earth-engine/datasets/tags/surface)
[weather](/earth-engine/datasets/tags/weather)








#### Description



Data starting from 2023\-12\-04 are available in the
[NASA/SMAP/SPL3SMP\_E/006](/earth-engine/datasets/catalog/NASA_SMAP_SPL3SMP_E_006) collection.


This Level\-3 (L3\) soil moisture product provides a daily composite of global
land surface conditions retrieved by the Soil Moisture Active Passive (SMAP)
L\-Band radiometer. The daily data here were collected from the descending
(local solar time of 6 am) and ascending (local solar time of 6 pm) passes.


The SMAP mission is an orbiting observatory that measures the amount of
water in the surface soil everywhere on Earth. A detailed description can be
found in the
[SMAP Handbook](https://smap.jpl.nasa.gov/system/internal_resources/details/original/178_SMAP_Handbook_FINAL_1_JULY_2014_Web.pdf).
It was launched in January 2015 and started operation in April 2015\. The
radar instrument, ceasing operation in early 2015 due to failure of radar
power supply, collected close to 3 months of science data. The prime mission
phase of three years was completed in 2018, and since then SMAP has been in
extended operation phase.


SMAP measures soil moisture every 2\-3 days. This permits changes around
the world to be observed over time scales ranging from major storms to
repeated measurements of changes over the seasons.


Everywhere on Earth not covered with water or not frozen, SMAP measures how
much water is in the top layer of soil. It also distinguishes between ground
that is frozen or thawed. Where the ground is not frozen, SMAP measures the
amount of water found between the minerals, rocky material, and organic
particles found in soil everywhere in the world (SMAP measures liquid water
in the top layer of ground but is not able to measure the ice.)


SPL3SMP\_E data are transformed to
[geographic coordinates using GDAL libraries](https://github.com/google/earthengine-catalog/blob/main/pipelines/smap_convert_l3.py)
before the data are ingested into Google Earth Engine.


See the
[SMAP L3 Soil Moisture User Guide](https://nsidc.org/sites/default/files/spl3smp_e-v005-userguide.pdf)
and references therein for additional documentation and algorithm details.


See
[basic](https://developers.google.com/earth-engine/tutorials/community/smap-soil-moisture)
and
[advanced](https://developers.google.com/earth-engine/tutorials/community/anomalies-analysis-smo-and-pre)
tutorials to learn how to use SMAP data in Earth Engine.





### Bands



**Pixel Size**
  
9000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `soil_moisture_am` | Volume fraction | Retrieved soil moisture estimate from the disaggregated/downscaled vertical polarization brightness temperature at 9\-km grid cell; AM overpass |
| `tb_h_corrected_am` | K | 0 | 330 | Weighted average of horizontally polarized brightness temperatures. This value represents the corrected land brightness temperature if the water fraction is lower than 0\.9 (otherwise no correction is applied) or represents the corrected water brightness temperature if the water fraction is greater than 0\.1 (otherwise no correction is applied); AM overpass |
| `tb_v_corrected_am` | K | 0 | 330 | Weighted average of vertically polarized brightness temperatures. This value represents the corrected land brightness temperature if the water fraction is lower than 0\.9 (otherwise no correction is applied) or represents the corrected water brightness temperature if the water fraction is greater than 0\.1 (otherwise no correction is applied); AM overpass |
| `vegetation_water_content_am` | kg/m^2 | 0 | 30 | Vegetation water content at 9\-km spatial scale. This parameter is used as input ancillary data parameter to the SPL2SMAP processing software when the baseline algorithm is used. The valid minimum and maximum below are subject to further analysis. AM overpass |
| `retrieval_qual_flag_am` | None | 0 | 65536 | 0 \= Pass: Soil moisture with acceptable quality; 1 \= Fail: Soil moisture does with unacceptable quality; AM overpass |
| `tb_qual_flag_h_am` | None | 0 | 65536 | 0\= brightness temperatures with unacceptable quality; 1\= brightness temperatures with acceptable quality; AM overpass |
| `tb_qual_flag_v_am` | None | 0 | 65536 | 0\= brightness temperatures with unacceptable quality; 1\= brightness temperatures with acceptable quality; AM overpass |
| `soil_moisture_pm` | Volume fraction | Retrieved soil moisture estimate from the disaggregated/downscaled vertical polarization brightness temperature at 9\-km grid cell; PM overpass |
| `tb_h_corrected_pm` | K | 0 | 330 | Weighted average of horizontally polarized brightness temperatures. This value represents the corrected land brightness temperature if the water fraction is lower than 0\.9 (otherwise no correction is applied) or represents the corrected water brightness temperature if the water fraction is greater than 0\.1 (otherwise no correction is applied); PM overpass |
| `tb_v_corrected_pm` | K | 0 | 330 | Weighted average of vertically polarized brightness temperatures. This value represents the corrected land brightness temperature if the water fraction is lower than 0\.9 (otherwise no correction is applied) or represents the corrected water brightness temperature if the water fraction is greater than 0\.1 (otherwise no correction is applied); PM overpass |
| `vegetation_water_content_pm` | kg/m^2 | 0 | 30 | Vegetation water content at 9\-km spatial scale. This parameter is used as input ancillary data parameter to the SPL2SMAP processing software when the baseline algorithm is used. The valid minimum and maximum below are subject to further analysis. PM overpass |
| `retrieval_qual_flag_pm` | None | 0 | 65536 | 0 \= Pass: Soil moisture with acceptable quality; 1 \= Fail: Soil moisture does with unacceptable quality; PM overpass |
| `tb_qual_flag_h_pm` | None | 0 | 65536 | 0\= brightness temperatures with unacceptable quality; 1\= brightness temperatures with acceptable quality; PM overpass |
| `tb_qual_flag_v_pm` | None | 0 | 65536 | 0\= brightness temperatures with unacceptable quality; 1\= brightness temperatures with acceptable quality; PM overpass |
| `soil_moisture_am_anomaly` | None | Experimental. Difference of the 30\-day average of 'soil\_moisture\_am', centered on asset date, relative to the same 30\-day period averaged across years from 2015 to present, excluding asset year. See [this script](https://github.com/google/earthengine-catalog/blob/main/pipelines/smap_convert_l3.py) for anomaly computations. |
| `soil_moisture_pm_anomaly` | None | Experimental. Difference of the 30\-day average of 'soil\_moisture\_pm', centered on asset date, relative to the same 30\-day period averaged across years from 2015 to present, excluding asset year. See [this script](https://github.com/google/earthengine-catalog/blob/main/pipelines/smap_convert_l3.py) for anomaly computations. |




### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* \*\*O'Neill, P. E., S. Chan, E. G. Njoku, T. Jackson, R. Bindlish,
J. Chaubell, and A. Colliander. 2021\. SMAP Enhanced L3 Radiometer Global
and Polar Grid Daily 9 km EASE\-Grid Soil Moisture, Version 5\.
\[Indicate subset used]. Boulder, Colorado USA. NASA National Snow and Ice
Data Center Distributed Active Archive Center.
[doi:10\.5067/4DQ54OUIJ9DL](https://doi.org/10.5067/4DQ54OUIJ9DL)
* Entekhabi et al., 2014
D. Entekhabi, S. Yueh, P. O'Neill, K. Kellogg et al. SMAP Handbook \-
Soil Moisture Active Passive: Mapping Soil Moisture and Freeze/thaw From
Space. SMAP Project, Jet Propulsion Laboratory, Pasadena, CA (2014\)
[SMAP Handbook](https://smap.jpl.nasa.gov/system/internal_resources/details/original/178_SMAP_Handbook_FINAL_1_JULY_2014_Web.pdf)
* Chan, S. K., R. Bindlish, P. E. O'Neill, E. Njoku, T. Jackson,
A. Colliander, F. Chen, M. Burgin, S. Dunbar, J. Piepmeier, S. Yueh,
D. Entekhabi, M. H. Cosh, T. Caldwell, J. Walker, X. Wu, A. Berg,
T. Rowlandson, A. Pacheco, H. McNairn, M. Thibeault,
J. Martinez\-Fernandez, A. Gonzalez\-Zamora, M. Seyfried, D. Bosch,
P. Starks, D. Goodrich, J. Prueger, M. Palecki, E. E. Small, M. Zreda,
J.\-C. Calvet, W. T. Crow, and Y. Kerr. 2016\. "Assessment of the SMAP
Passive Soil Moisture Product" IEEE Transactions on Geoscience and
Remote Sensing, 54 (8\): 4994\-5007
[10\.1109/tgrs.2016\.2561938](https://doi.org/10.1109/tgrs.2016.2561938)
* Chan, S., R. Bindlish, P. O'Neill, T. Jackson, E. Njoku, S. Dunbar,
J. Chaubell, J. Piepmeier, S. Yueh, D. Entekhabi, A. Colliander,
F. Chen, M. Cosh, T. Caldwell, J. Walker, A. Berg, H. McNairn,
M. Thibeault, J. Martínez\-Fernández, F. Uldall,
M. Seyfried, D. Bosch, P. Starks, C. Holifield Collins, J. Prueger,
R. van der Velde, J. Asanuma, M. Palecki, E. Small, M. Zreda, J. Calvet,
W. Crow, and Y. Kerr. 2018\. "Development and assessment of the SMAP
enhanced passive soil moisture product." Remote Sensing of Environment,
204: 931\-941
[10\.1016/j.rse.2017\.08\.025](https://doi.org/10.1016/j.rse.2017.08.025)
* Chaubell, M. J., J. Asanuma, A. A. Berg, D. D. Bosch, T. Caldwell,
M. H. Cosh, C. H. Collins, J. Martinez\-Fernandez, M. Seyfried,
P. J. Starks, Z. Su, S. H. Yueh, M. Thibeault, J. Walker, R. S. Dunbar,
A. Colliander, F. Chen, S. K. Chan, D. Entekhabi, R. Bindlish, and
P. E. O'Neill. 2020\. "Improved SMAP Dual\-Channel Algorithm for the
Retrieval of Soil Moisture." IEEE Transactions on Geoscience and Remote
Sensing, 1\-12
[10\.1109/tgrs.2019\.2959239](https://doi.org/10.1109/tgrs.2019.2959239)





### DOIs


* [https://doi.org/10\.1016/j.rse.2017\.08\.025](https://doi.org/10.1016/j.rse.2017.08.025)
* [https://doi.org/10\.1109/tgrs.2016\.2561938](https://doi.org/10.1109/tgrs.2016.2561938)
* [https://doi.org/10\.1109/tgrs.2019\.2959239](https://doi.org/10.1109/tgrs.2019.2959239)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/SMAP/SPL3SMP_E/005')
.filter(ee.Filter.date('2017-04-01','2017-04-30'));

varsoilMositureSurface=dataset.select('soil_moisture_am');
varsoilMositureSurfaceVis={
min:0.0,
max:0.5,
palette:['0300ff','418504','efff07','efff07','ff0303'],
};
Map.setCenter(-6.746,46.529,2);
Map.addLayer(soilMositureSurface,soilMositureSurfaceVis,'Soil Mositure');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_SMAP_SPL3SMP_E_005)


[SPL3SMP\_E.005 SMAP L3 Radiometer Global Daily 9 km Soil Moisture](/earth-engine/datasets/catalog/NASA_SMAP_SPL3SMP_E_005)

Data starting from 2023\-12\-04 are available in the NASA/SMAP/SPL3SMP\_E/006 collection. This Level\-3 (L3\) soil moisture product provides a daily composite of global land surface conditions retrieved by the Soil Moisture Active Passive (SMAP) L\-Band radiometer. The daily data here were collected from the descending (local solar time of 6 am) …

 NASA/SMAP/SPL3SMP\_E/005,
 drought,nasa,smap,soil,soil\-moisture,surface,weather

2015\-03\-31T12:00:00Z/2023\-12\-03T12:00:00Z



 \-84 \-180 84 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1109/tgrs.2019\.2959239](https://doi.org/https://nsidc.org/data/spl3smp_e/versions/5)
* [https://doi.org/10\.1109/tgrs.2019\.2959239](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_SMAP_SPL3SMP_E_005)









