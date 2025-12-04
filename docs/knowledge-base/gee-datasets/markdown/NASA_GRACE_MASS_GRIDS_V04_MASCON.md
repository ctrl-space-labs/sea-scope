



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GRACE Monthly Mass Grids Release 6\.3 Version 4 \- Global Mascons


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
===================================================================================================================================================================








Dataset Availability
2002\-03\-31T00:00:00Z–2024\-09\-30T00:00:00Z
Dataset Provider


[NASA Jet Propulsion Laboratory](https://grace.jpl.nasa.gov/data/get-data/jpl_global_mascons/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GRACE/MASS_GRIDS_V04/MASCON")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GRACE_MASS_GRIDS_V04_MASCON)





Tags


[grace](/earth-engine/datasets/tags/grace)
[gravity](/earth-engine/datasets/tags/gravity)
[jpl](/earth-engine/datasets/tags/jpl)
[mascon](/earth-engine/datasets/tags/mascon)
[mass](/earth-engine/datasets/tags/mass)
[nasa](/earth-engine/datasets/tags/nasa)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[tellus](/earth-engine/datasets/tags/tellus)
[water](/earth-engine/datasets/tags/water)








#### Description



This dataset contains gridded monthly global water storage/height anomalies
relative to a time\-mean, derived from GRACE and GRACE\-FO and processed at
JPL using the Mascon approach (RL06\.3Mv04\). These data are provided in a
single data file in netCDF format, and can be used for analysis for ocean,
ice, and hydrology phenomena. The water storage/height anomalies are given
in equivalent water thickness units (cm). The solution provided here is
derived from solving for monthly gravity field variations in terms of
geolocated spherical cap mass concentration functions, rather than global
spherical harmonic coefficients. Additionally, realistic geophysical
information is introduced during the solution inversion to intrinsically
remove correlated error. Thus, these Mascon grids do not need to be
de\-correlated or smoothed, like traditional spherical harmonic gravity
solutions.


The complete Mascon solution consists of 4,551 relatively
independent estimates of surface mass change that have been derived using an
equal\-area 3\-degree grid of individual mascons. It should be noted that this
dataset does not correct for leakage errors across coastlines; it is
therefore recommended only for users who want to apply their own algorithm
to separate between land and ocean mass very near coastlines.


For more information, please visit [GRACE page](https://grace.jpl.nasa.gov/data/get-data/jpl_global_mascons/).
For a detailed description on the Mascon solution, including
the mathematical derivation, implementation of geophysical constraints, and
solution validation, please see [Watkins et al., 2015](https://doi.org/10.1002/2014JB011547).
This product is intended for expert use only; other users are encouraged to
use the [CRI\-filtered Mascon dataset](https://podaac.jpl.nasa.gov/dataset/TELLUS_GRAC-GRFO_MASCON_CRI_GRID_RL06.3_V4).


This RL06\.3Mv04 is an updated version of the previous [Tellus JPL Mascon
RL06\.1Mv03](https://doi.org/10.5067/TEMSC-3MJ63).





### Bands



**Pixel Size**
  
55660 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `lwe_thickness` | cm | Equivalent liquid water thickness in centimeters. |
| `uncertainty` | None | 1\-sigma uncertainty for each 3\-degree mascon estimate. The provided estimates of uncertainty are regarded to be conservative. See the provider's [Error \& Uncertainty Estimates section](https://grace.jpl.nasa.gov/data/get-data/jpl_global_mascons/) |




### Terms of Use


**Terms of Use**


All NASA\-produced data from the GRACE mission is made freely available
for the public to use. When using any of the GRCTellus data, please
add an acknowledgment: "GRACE land are available at
<https://grace.jpl.nasa.gov>,
supported by the NASA MEaSUREs Program." and cite with the
citations provided.




### Citations



Citations:
* D. N. Wiese, D.\-N. Yuan, C. Boening, F. W. Landerer, M. M. Watkins. 2023\.
JPL GRACE and GRACE\-FO Mascon Ocean, Ice, and Hydrology Equivalent Water
Height JPL RL06\.3Mv04\. Ver. RL06\.3Mv04\. PO.DAAC, CA, USA. Dataset accessed
\[YYYY\-MM\-DD] at
[https://doi.org/10\.5067/TEMSC\-3MJ634](https://doi.org/10.5067/TEMSC-3MJ634).
* Watkins, M. M., D. N. Wiese, D.\-N. Yuan, C. Boening, and F. W.
Landerer (2015\), Improved methods for observing Earth's time variable mass,
mass distribution with GRACE using spherical cap mascons, J. Geophys. Res
Solid Earth, 120,
[doi:10\.1002/2014JB011547](https://doi.org/10.1002/2014JB011547).
* Wiese, D. N., F. W. Landerer, and M. M. Watkins (2016\),
Quantifying and reducing leakage errors in the JPL RL05M GRACE
mascon solution, Water Resour. Res., 52, 7490\-7502,
[doi:10\.1002/2016WR019344](https://doi.org/10.1002/2016WR019344).





### DOIs


* [https://doi.org/10\.1002/2014JB011547](https://doi.org/10.1002/2014JB011547)
* [https://doi.org/10\.1002/2016WR019344](https://doi.org/10.1002/2016WR019344)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/GRACE/MASS_GRIDS_V04/MASCON')
.filter(ee.Filter.date('2016-08-01','2016-08-30'));
varequivalentWaterThickness=dataset.select('lwe_thickness');
varequivalentWaterThicknessVis={
min:-25.0,
max:25.0,
palette:['001137','01abab','e7eb05','620500'],
};
Map.setCenter(6.746,46.529,2);
Map.addLayer(
equivalentWaterThickness,equivalentWaterThicknessVis,
'Equivalent Water Thickness');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GRACE_MASS_GRIDS_V04_MASCON)


[GRACE Monthly Mass Grids Release 6\.3 Version 4 \- Global Mascons](/earth-engine/datasets/catalog/NASA_GRACE_MASS_GRIDS_V04_MASCON)

This dataset contains gridded monthly global water storage/height anomalies relative to a time\-mean, derived from GRACE and GRACE\-FO and processed at JPL using the Mascon approach (RL06\.3Mv04\). These data are provided in a single data file in netCDF format, and can be used for analysis for ocean, ice, and hydrology …

 NASA/GRACE/MASS\_GRIDS\_V04/MASCON,
 grace,gravity,jpl,mascon,mass,nasa,surface\-ground\-water,tellus,water

2002\-03\-31T00:00:00Z/2024\-09\-30T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1002/2016WR019344](https://doi.org/https://grace.jpl.nasa.gov/data/get-data/jpl_global_mascons/)
* [https://doi.org/10\.1002/2016WR019344](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_GRACE_MASS_GRIDS_V04_MASCON)









