



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NCEP\-DOE Reanalysis 2 (Gaussian Grid), Total Cloud Coverage


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================================








Dataset Availability
1979\-01\-01T00:00:00Z–2025\-06\-30T18:00:00Z
Dataset Provider


[NOAA](https://psl.noaa.gov/data/gridded/data.ncep.reanalysis2.html)



Earth Engine Snippet


`ee.ImageCollection("NOAA/NCEP_DOE_RE2/total_cloud_coverage")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_NCEP_DOE_RE2_total_cloud_coverage)





Cadence
6 Hours
Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[cloud](/earth-engine/datasets/tags/cloud)
[geophysical](/earth-engine/datasets/tags/geophysical)
[ncep](/earth-engine/datasets/tags/ncep)
[noaa](/earth-engine/datasets/tags/noaa)
[reanalysis](/earth-engine/datasets/tags/reanalysis)








#### Description



NCEP\-DOE Reanalysis 2 project is using a state\-of\-the\-art analysis/forecast system to perform
data assimilation using past data from 1979 through the previous year.





### Bands



**Pixel Size**
  
278300 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `tcdc` | % | 0\* | 100\* | Total cloud cover |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


There are no restrictions on the use of these datasets.




### Citations



Citations:
* [NCEP\-DOE AMIP\-II Reanalysis (R\-2\): M. Kanamitsu, W. Ebisuzaki, J. Woollen, S\-K Yang,
J.J. Hnilo, M. Fiorino, and G. L. Potter. 1631\-1643, Nov 2002, Bulletin of the American
Meteorological Society.](https://journals.ametsoc.org/view/journals/bams/83/11/bams-83-11-1631.xml).





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Import the dataset, filter the first five months of 2020.
vardataset=ee.ImageCollection('NOAA/NCEP_DOE_RE2/total_cloud_coverage')
.filter(ee.Filter.date('2020-01-01','2020-06-01'));

// Select the total cloud cover band.
vartotalCloudCoverage=dataset.select('tcdc');

// Reduce the image collection to per-pixel mean.
vartotalCloudCoverageMean=totalCloudCoverage.mean();

// Define visualization parameters.
varvis={
min:0,
max:80,// dataset max is 100
palette:['black','white'],
};

// Display the dataset.
Map.setCenter(0,20,2);
Map.addLayer(totalCloudCoverageMean,vis,'Total Cloud Coverage Data',false);

// Display a visualization image with opacity defined by cloud cover.
varvisImg=totalCloudCoverageMean.visualize(vis)
.updateMask(totalCloudCoverageMean.divide(100));
Map.addLayer(visImg,null,'Total Cloud Coverage Vis.',true);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_NCEP_DOE_RE2_total_cloud_coverage)


[NCEP\-DOE Reanalysis 2 (Gaussian Grid), Total Cloud Coverage](/earth-engine/datasets/catalog/NOAA_NCEP_DOE_RE2_total_cloud_coverage)

NCEP\-DOE Reanalysis 2 project is using a state\-of\-the\-art analysis/forecast system to perform data assimilation using past data from 1979 through the previous year.

 NOAA/NCEP\_DOE\_RE2/total\_cloud\_coverage,
 atmosphere,climate,cloud,geophysical,ncep,noaa,reanalysis

1979\-01\-01T00:00:00Z/2025\-06\-30T18:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








