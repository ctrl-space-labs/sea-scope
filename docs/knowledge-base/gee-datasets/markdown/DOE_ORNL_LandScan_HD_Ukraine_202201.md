



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

LandScan High Definition Data for Ukraine, January 2022


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================================








Dataset Availability
2022\-01\-01T00:00:00Z–2022\-02\-01T00:00:00Z
Dataset Provider


[Oak Ridge National Laboratory](https://landscan.ornl.gov/ukraine-landscan-hd-data)



Earth Engine Snippet


`ee.Image("DOE/ORNL/LandScan_HD/Ukraine_202201")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/DOE/DOE_ORNL_LandScan_HD_Ukraine_202201)





Tags


[landscan](/earth-engine/datasets/tags/landscan)
[population](/earth-engine/datasets/tags/population)
ukraine








#### Description



[LandScan High Definition (HD)](https://landscan.ornl.gov)
provides gridded population estimates at 3
arc\-second (\~100m) resolution. Values for each LandScan HD cell represent an
ambient (i.e. 24 hour average) population count estimate. In this way, the
data capture the full potential activity space of people throughout the
course of the day and night rather than just a residential location. The
LandScan HD model incorporates current land use and infrastructure data from
a variety of sources, applies facility occupancy estimates from ORNL's
Population Density Tables (PDT) project, and leverages novel image
processing algorithms developed at ORNL to rapidly map building
structures and neighborhood areas using high\-performance computing
environments.


The source for subnational population counts used in the development of this
data comes from
[State Statistics Service of Ukraine](https://ukrstat.org/en/operativ/operativ2021/ds/kn/arh_kn2021_e.html).


These subnational estimates were adjusted to the country total population
provided by the
[CIA World Factbook](https://www.cia.gov/the-world-factbook/countries/ukraine/#people-and-society).





### Bands



**Pixel Size**
  
100 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `population` | 0\* | 1020\* | 24 hour average population count estimate |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


This dataset is licensed under
[CC\-BY 4\.0](https://creativecommons.org/licenses/by/4.0/).'




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('DOE/ORNL/LandScan_HD/Ukraine_202201');
varvis={
min:0.0,
max:10.0,
palette:['lemonchiffon','khaki','orange','orangered','red','maroon'],
};
Map.centerObject(dataset);
Map.addLayer(dataset,vis,'Population Count');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/DOE/DOE_ORNL_LandScan_HD_Ukraine_202201)


[LandScan High Definition Data for Ukraine, January 2022](/earth-engine/datasets/catalog/DOE_ORNL_LandScan_HD_Ukraine_202201)

LandScan High Definition (HD) provides gridded population estimates at 3 arc\-second (\~100m) resolution. Values for each LandScan HD cell represent an ambient (i.e. 24 hour average) population count estimate. In this way, the data capture the full potential activity space of people throughout the course of the day and night …

 DOE/ORNL/LandScan\_HD/Ukraine\_202201,
 landscan,population

2022\-01\-01T00:00:00Z/2022\-02\-01T00:00:00Z



 44\.175 22\.125 52\.4 40\.225
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








