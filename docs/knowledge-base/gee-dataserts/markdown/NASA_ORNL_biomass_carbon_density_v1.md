



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Global Aboveground and Belowground Biomass Carbon Density Maps


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2010\-12\-31T00:00:00Z
Dataset Provider


[NASA ORNL DAAC at Oak Ridge National Laboratory](https://doi.org/10.3334/ORNLDAAC/1763)



Earth Engine Snippet


`ee.ImageCollection("NASA/ORNL/biomass_carbon_density/v1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_ORNL_biomass_carbon_density_v1)





Cadence
1 Year
Tags


[aboveground](/earth-engine/datasets/tags/aboveground)
[biomass](/earth-engine/datasets/tags/biomass)
[carbon](/earth-engine/datasets/tags/carbon)
[density](/earth-engine/datasets/tags/density)
[forest](/earth-engine/datasets/tags/forest)
[forest\-biomass](/earth-engine/datasets/tags/forest-biomass)
[nasa](/earth-engine/datasets/tags/nasa)
[ornl](/earth-engine/datasets/tags/ornl)
[vegetation](/earth-engine/datasets/tags/vegetation)
belowground








#### Description



This dataset provides temporally consistent and harmonized global maps of aboveground and
belowground biomass carbon density for the year 2010 at a 300\-m spatial resolution. The
aboveground biomass map integrates land\-cover specific, remotely sensed maps of woody,
grassland, cropland, and tundra biomass. Input maps were amassed from the published literature
and, where necessary, updated to cover the focal extent or time period. The belowground biomass
map similarly integrates matching maps derived from each aboveground biomass map and land\-cover
specific empirical models. Aboveground and belowground maps were then integrated separately
using ancillary maps of percent tree cover and landcover and a rule\-based decision tree. Maps
reporting the accumulated uncertainty of pixel\-level estimates are also provided.


Provider's note: The UN Environment Programme World Conservation Monitoring
Centre (UNEP\-WCMC) carbon biomass dataset
represents conditions between 1982 and 2010 depending on land cover type. The relative patterns
of carbon stocks are well represented with this dataset. The [NASA/ORNL carbon biomass dataset](https://daac.ornl.gov/VEGETATION/guides/Global_Maps_C_Density_2010.html)
represents biomass conditions for 2010, with uncertainty estimates at the pixel\-level.
Additional biomass of non\-dominant land cover types are represented within each pixel. For more
detailed information, please refer to the papers describing each dataset: [WCMC](/earth-engine/datasets/catalog/WCMC_biomass_carbon_density_v1_0)
[(Soto\-Navarro et al. 2020\)](https://royalsocietypublishing.org/doi/full/10.1098/rstb.2019.0128)
and NASA/ORNL [(Spawn et al. 2020\)](https://www.nature.com/articles/s41597-020-0444-4).





### Bands



**Pixel Size**
  
300 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `agb` | Mg/ha | 0\* | 129\* | Aboveground living biomass carbon stock density of combined woody and herbaceous cover in 2010\. This includes carbon stored in living plant tissues that are located above the earth's surface (stems, bark, branches, twigs). This does not include leaf litter or coarse woody debris that were once attached to living plants but have since been deposited and are no longer living. |
| `agb_uncertainty` | Mg/ha | 0\* | 85\* | Uncertainty of estimated aboveground living biomass carbon density of combined woody and herbaceous cover in 2010\. Uncertainty represents the cumulative standard error that has been propagated through the harmonization process using summation in quadrature. |
| `bgb` | Mg/ha | 0\* | 57\* | Belowground living biomass carbon stock density of combined woody and herbaceous cover in 2010\. This includes carbon stored in living plant tissues that are located below the earth's surface (roots). This does not include dead and/or dislocated root tissue, nor does it include soil organic matter. |
| `bgb_uncertainty` | Mg/ha | 0\* | 37\* | Uncertainty of estimated belowground living biomass carbon density of combined woody and herbaceous cover in 2010\. Uncertainty represents the cumulative standard error that has been propagated through the harmonization process using summation in quadrature. |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


This dataset is in the public domain and is available
without restriction on use and distribution. See [NASA's
Earth Science Data \& Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy)
for additional information.




### Citations



Citations:
* Spawn, S.A., Sullivan, C.C., Lark, T.J. et al. Harmonized global maps of above and
belowground biomass carbon density in the year 2010\. Sci Data 7, 112 (2020\).
[doi:10\.1038/s41597\-020\-0444\-4](https://doi.org/10.1038/s41597-020-0444-4)
* Spawn, S.A., and H.K. Gibbs. 2020\. Global Aboveground and Belowground
Biomass Carbon Density Maps for the Year 2010\. ORNL DAAC, Oak Ridge, Tennessee, USA.





### DOIs


* [https://doi.org/10\.3334/ORNLDAAC/1763](https://doi.org/10.3334/ORNLDAAC/1763)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NASA/ORNL/biomass_carbon_density/v1');

varvisualization={
bands:['agb'],
min:-50.0,
max:80.0,
palette:['d9f0a3','addd8e','78c679','41ab5d','238443','005a32']
};

Map.setCenter(-60.0,7.0,4);

Map.addLayer(dataset,visualization,'Aboveground biomass carbon');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_ORNL_biomass_carbon_density_v1)


[Global Aboveground and Belowground Biomass Carbon Density Maps](/earth-engine/datasets/catalog/NASA_ORNL_biomass_carbon_density_v1)

This dataset provides temporally consistent and harmonized global maps of aboveground and belowground biomass carbon density for the year 2010 at a 300\-m spatial resolution. The aboveground biomass map integrates land\-cover specific, remotely sensed maps of woody, grassland, cropland, and tundra biomass. Input maps were amassed from the published literature …

 NASA/ORNL/biomass\_carbon\_density/v1,
 aboveground,biomass,carbon,density,forest,forest\-biomass,nasa,ornl,vegetation

2010\-01\-01T00:00:00Z/2010\-12\-31T00:00:00Z



 \-61\.1 \-180 84 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.3334/ORNLDAAC/1763](https://doi.org/https://doi.org/10.3334/ORNLDAAC/1763)
* [https://doi.org/10\.3334/ORNLDAAC/1763](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_ORNL_biomass_carbon_density_v1)









