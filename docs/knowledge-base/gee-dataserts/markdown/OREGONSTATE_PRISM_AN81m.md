



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

PRISM Monthly Spatial Climate Dataset AN81m


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=============================================================================================================================================








Dataset Availability
1895\-01\-01T00:00:00Z–2025\-06\-01T00:00:00Z
Dataset Provider


[PRISM / OREGONSTATE](https://www.prism.oregonstate.edu/)



Earth Engine Snippet


`ee.ImageCollection("OREGONSTATE/PRISM/AN81m")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OREGONSTATE/OREGONSTATE_PRISM_AN81m)





Cadence
1 Month
Tags


[climate](/earth-engine/datasets/tags/climate)
[geophysical](/earth-engine/datasets/tags/geophysical)
[monthly](/earth-engine/datasets/tags/monthly)
[oregonstate](/earth-engine/datasets/tags/oregonstate)
[precipitation](/earth-engine/datasets/tags/precipitation)
[pressure](/earth-engine/datasets/tags/pressure)
[prism](/earth-engine/datasets/tags/prism)
[temperature](/earth-engine/datasets/tags/temperature)
[vapor](/earth-engine/datasets/tags/vapor)
[weather](/earth-engine/datasets/tags/weather)








#### Description



The PRISM daily and monthly datasets are gridded climate
datasets for the conterminous United States, produced by the
PRISM Climate Group at Oregon State University.


Grids are
developed using PRISM (Parameter\-elevation Regressions on Independent
Slopes Model). PRISM interpolation routines simulate how weather
and climate vary with elevation, and account for coastal effects,
temperature inversions, and terrain barriers that can cause rain
shadows. Station data are assimilated from many networks across
the country. For more information, see the [Descriptions of PRISM
Spatial Climate Datasets](https://www.prism.oregonstate.edu/documents/PRISM_datasets.pdf).


**Note**


* **Warning**, this dataset should not be
used to calculate century\-long climate trends due to non\-climatic
variations from to station equipment and location changes, openings
and closings, varying observation times, and the use of relatively
short\-term networks. Please see the [dataset
documentation](https://www.prism.oregonstate.edu/documents/PRISM_datasets.pdf)
for more details.
* It takes time for observation networks to conduct quality control
and release station data. Therefore, PRISM datasets are re\-modeled
several times until six months have elapsed, when they are
considered permanent. A [release schedule is
available](https://www.prism.oregonstate.edu/calendar/).
* For use of the 30 arc\-second (\~800 m) version of this dataset
please contact the provider at prism\-questions@nacse.org.





### Bands



**Pixel Size**
  
4638\.3 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `ppt` | mm | 0\* | 2639\.82\* | Monthly total precipitation (including rain and melted snow) |
| `tmean` | °C | \-30\.8\* | 41\.49\* | Monthly average of daily mean temperature (calculated as (tmin\+tmax)/2\) |
| `tmin` | °C | \-35\.11\* | 34\.72\* | Monthly minimum temperature |
| `tmax` | °C | \-29\.8\* | 49\.74\* | Monthly average of daily maximum temperature |
| `tdmean` | °C | \-30\.7\* | 26\.76\* | Monthly average of daily mean dew point temperature |
| `vpdmin` | hPa | 0\* | 44\.79\* | Monthly average of daily minimum vapor pressure deficit |
| `vpdmax` | hPa | 0\.009\* | 110\.06\* | Monthly average of daily maximum vapor pressure deficit |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| PRISM\_CODE\_VERSION | STRING\_LIST | List of code versions per\-band, e.g: the first element is for the first band "ppt", the second element is for the second band "tmean" |
| PRISM\_DATASET\_CREATE\_DATE | STRING\_LIST | List of original creation dates per\-band |
| PRISM\_DATASET\_FILENAME | STRING\_LIST | List of original filenames for each band |
| PRISM\_DATASET\_TYPE | STRING\_LIST | List of dataset types per\-band |
| PRISM\_DATASET\_VERSION | STRING\_LIST | List of dataset versions per\-band e.g: D1 or D2 for daily products; M1, M2 or M3 for monthly products. |
| status | STRING | Data generated within 30 days of observation have the status "early". Data generated within 1\-6 months of observation may have the status "provisional" and data older than 6 months are marked as "permanent". |




### Terms of Use


**Terms of Use**


These PRISM datasets are available without restriction
on use or distribution. PRISM Climate Group does request that the
user give proper attribution and identify PRISM, where applicable,
as the source of the data.




### Citations



Citations:
* [Daly, C., Halbleib, M., Smith, J.I., Gibson, W.P., Doggett, M.K.,
Taylor, G.H., Curtis, J., and Pasteris, P.A. 2008\. Physiographically\-sensitive
mapping of temperature and precipitation across the conterminous
United States. International Journal of Climatology, 28: 2031\-2064](https://www.prism.oregonstate.edu/documents/pubs/2008intjclim_physiographicMapping_daly.pdf)
* \[Daly, C., J.I. Smith, and K.V. Olson. 2015\. Mapping atmospheric
moisture climatologies across the conterminous United States. PloS
ONE 10(10\):e0141140\.
[doi:10\.1371/journal.pone.0141140](https://doi.org/10.1371/journal.pone.0141140).





### DOIs


* [https://doi.org/10\.1371/journal.pone.0141140](https://doi.org/10.1371/journal.pone.0141140)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('OREGONSTATE/PRISM/AN81m')
.filter(ee.Filter.date('2018-07-01','2018-07-31'));
varprecipitation=dataset.select('ppt');
varprecipitationVis={
min:0.0,
max:300.0,
palette:['red','yellow','green','cyan','purple'],
};
Map.setCenter(-100.55,40.71,4);
Map.addLayer(precipitation,precipitationVis,'Precipitation');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/OREGONSTATE/OREGONSTATE_PRISM_AN81m)


[PRISM Monthly Spatial Climate Dataset AN81m](/earth-engine/datasets/catalog/OREGONSTATE_PRISM_AN81m)

The PRISM daily and monthly datasets are gridded climate datasets for the conterminous United States, produced by the PRISM Climate Group at Oregon State University. Grids are developed using PRISM (Parameter\-elevation Regressions on Independent Slopes Model). PRISM interpolation routines simulate how weather and climate vary with elevation, and account for …

 OREGONSTATE/PRISM/AN81m,
 climate,geophysical,monthly,oregonstate,precipitation,pressure,prism,temperature,vapor,weather

1895\-01\-01T00:00:00Z/2025\-06\-01T00:00:00Z



 24 \-125 50 \-66
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1371/journal.pone.0141140](https://doi.org/https://www.prism.oregonstate.edu/)
* [https://doi.org/10\.1371/journal.pone.0141140](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/OREGONSTATE_PRISM_AN81m)









