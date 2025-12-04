



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

TOMS and OMI Merged Ozone Data


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================








Dataset Availability
1978\-11\-01T00:00:00Z–2025\-07\-14T00:00:00Z
Dataset Provider


[NASA / GES DISC](https://disc.gsfc.nasa.gov/information?page=1&keywords=acdisc)



Earth Engine Snippet


`ee.ImageCollection("TOMS/MERGED")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TOMS/TOMS_MERGED)





Cadence
1 Day
Tags


[atmosphere](/earth-engine/datasets/tags/atmosphere)
[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[nasa](/earth-engine/datasets/tags/nasa)
[ozone](/earth-engine/datasets/tags/ozone)
aura
ges\-disc
goddard
omi
toms








#### Description



The Total Ozone Mapping Spectrometer (TOMS) data represent the primary
long\-term, continuous record of satellite\-based observations available for
use in monitoring global and regional trends in total ozone over the past
25 years. The data are produced by the Laboratory for Atmospheres at NASA's
Goddard Space Flight Center. Version 8 TOMS data products include level 3
gridded data (1\.0 x 1\.25 deg). The Ozone Monitoring Instrument (OMI), aboard
the Aura satellite (July 2004 \- current), has a higher resolution
(1\.0 x 1\.0 deg).


These data represent a merged ozone product from TOMS/EarthProbe,
TOMS/Nimbus\-7, TOMS/Meteor\-3, OMI/Aura and USGS\-interpolated data for dates
with no data.


[Additional TOMS and OMI information](https://ozoneaq.gsfc.nasa.gov/missions/)





### Bands



**Pixel Size**
  
111000 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `ozone` | Dobson | 73\* | 983\* | Total column ozone |


 \* estimated min or max value


### Terms of Use


**Terms of Use**


Distribution of data from the Goddard Earth Sciences Data and
Information Services Center (GES DISC) is funded by NASA's Science Mission
Directorate (SMD). Consistent with NASA
[Earth Science Data and Information Policy](https://www.earthdata.nasa.gov/engage/open-data-services-and-software/data-and-information-policy/),
data from the GES DISC archive are available free to the user community.
For more information visit the GES DISC
[Data Policy](https://disc.sci.gsfc.nasa.gov/citing) page.




### Citations



Citations:
* The data set source should be properly cited when the data are used.
A formal reference of the form: \\, 2012, last updated 2013:
\\. NASA/GSFC, Greenbelt, MD, USA, NASA Goddard Earth Sciences
Data and Information Services Center (GES DISC). Accessed
\\ at \\ is suggested following
Parsons et al. (2010\),
[doi:10\.1029/2010EO340001](https://doi.org/10.1029/2010EO340001)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('TOMS/MERGED')
.filter(ee.Filter.date('2018-08-01','2018-08-10'));
varcolumnOzone=dataset.select('ozone');
varcolumnOzoneVis={
min:100,
max:500,
palette:['1621a2','cyan','green','yellow','orange','red'],
};
Map.setCenter(6.75,46.53,2);
Map.addLayer(columnOzone,columnOzoneVis,'Column Ozone');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/TOMS/TOMS_MERGED)


[TOMS and OMI Merged Ozone Data](/earth-engine/datasets/catalog/TOMS_MERGED)

The Total Ozone Mapping Spectrometer (TOMS) data represent the primary long\-term, continuous record of satellite\-based observations available for use in monitoring global and regional trends in total ozone over the past 25 years. The data are produced by the Laboratory for Atmospheres at NASA's Goddard Space Flight Center. Version 8 …

 TOMS/MERGED,
 atmosphere,climate,geophysical,nasa,ozone

1978\-11\-01T00:00:00Z/2025\-07\-14T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








