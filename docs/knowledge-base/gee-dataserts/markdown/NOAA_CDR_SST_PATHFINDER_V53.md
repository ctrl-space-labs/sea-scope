



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NOAA AVHRR Pathfinder Version 5\.3 Collated Global 4km Sea Surface Temperature


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================================================================








Dataset Availability
1981\-08\-24T00:00:00Z–2023\-12\-30T21:35:08Z
Dataset Provider


[NOAA](https://www.ncei.noaa.gov/products/avhrr-pathfinder-sst)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CDR/SST_PATHFINDER/V53")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_SST_PATHFINDER_V53)





Cadence
12 Hours
Tags


[avhrr](/earth-engine/datasets/tags/avhrr)
[noaa](/earth-engine/datasets/tags/noaa)
[oceans](/earth-engine/datasets/tags/oceans)
[sst](/earth-engine/datasets/tags/sst)
[temperature](/earth-engine/datasets/tags/temperature)
[wind](/earth-engine/datasets/tags/wind)
pathfinder
sea\-ice








#### Description



The AVHRR Pathfinder Version 5\.3 Sea Surface Temperature dataset (PFV53\)
is a collection of global, twice\-daily 4km sea surface temperature data
produced in a partnership by the NOAA National Oceanographic Data Center
and the University of Miami's Rosenstiel School of Marine and Atmospheric
Science. PFV53 was computed from data from the AVHRR instruments
on board NOAA's polar orbiting satellite series using an entirely
modernized system based on SeaDAS. PFV53 data are nearly 100%
compliant with the GHRSST Data Specification Version 2\.0 for L3C
products and only deviate from that standard in that 'sses\_bias',
'sses\_standard\_deviation', and 'sst\_dtime' variables are empty and hence
not included into EE assets. PFV53 data were collected through the
operational periods of the NOAA\-7 through NOAA\-19 Polar Operational
Environmental Satellites (POES), and are available from 1981 to 2014\.
Additional information is available at the
[NOAA Pathfinder site](https://www.nodc.noaa.gov/satellitedata/pathfinder4km53/).


Additional band details can be found in the
[Tech Specs](https://www.ncei.noaa.gov/pub/data/sds/cdr/CDRs/Sea_Surface_Temperature_Pathfinder/AlgorithmDescription_01B-08.pdf)
page.


These data were provided by GHRSST and the US NOAA National
Centers for Environmental Information (NCEI). This project was
supported in part by a grant from the NOAA Climate Data Record (CDR)
Program for satellites.





### Bands



**Pixel Size**
  
4000 meters



**Bands**




| Name | Units | Min | Max | Scale | Offset | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `sea_surface_temperature` | K | \-300\* | 3999\* | 0\.01 | 273\.15 | Skin temperature of the ocean |
| `dt_analysis` | K | \-127\* | 127\* | 0\.1 |  | The difference between this SST and the previous day's. |
| `wind_speed` | m/s | 0\* | 47\* |  |  | These wind speeds were created by NCEP\-DOE Atmospheric Model Intercomparison Project (AMIP\-II) reanalysis (R\-2\) and represent winds at 10 meters above the sea surface. |
| `sea_ice_fraction` | None | 8\* | 100\* | 0\.01 |  | Sea ice concentration data are taken from the EUMETSAT Ocean and Sea Ice Satellite Application Facility (OSISAF) [Global Daily Sea Ice Concentration Reprocessing Data Set accession.nodc.noaa.gov/0068294](https://data.cnra.ca.gov/dataset/global-daily-sea-ice-concentration-reprocessing-data-set-for-1978-2007-from-the-eumetsat-ocean-) when these data are available. The data are reprojected and interpolated from their original polar stereographic projection at 10km spatial resolution to the 4km Pathfinder Version 5\.3 grid. When the OSISAF data are not available for both hemispheres on a given day, the sea ice concentration data are taken from the sea\_ice\_fraction variable found in the L4 GHRSST DailyOI SST product from NOAA/NCDC, and are interpolated from the 25km DailyOI grid to the 4km Pathfinder Version 5\.3 grid. |
| `aerosol_dynamic_indicator` | None | \-127\* | 127\* | 0\.01 | 1\.1 | Aerosol optical thickness (100 KM) data are taken from the CLASS AERO100 products, which are created from AVHRR channel 1 optical thickness retrievals from AVHRR global area coverage (GAC) data. The aerosol optical thickness measurements are interpolated from their original 1 degree x 1 degree resolution to the 4km Pathfinder Version 5\.3 grid. |
| `quality_level` | None | 0 | 5 |  |  | Note, the native Pathfinder processing system returns quality levels ranging from 0 to 7 (7 is best quality; \-1 represents missing data) and has been converted to the extent possible into the six levels required by the GDS2 (ranging from 0 to 5, where 5 is best). Below is the conversion table:* GDS2 required quality\_level 5 \= native Pathfinder quality level 7 \=\= best\_quality * GDS2 required quality\_level 4 \= native Pathfinder quality level 4\-6 \=\= acceptable\_quality * GDS2 required quality\_level 3 \= native Pathfinder quality level 2\-3 \=\= low\_quality * GDS2 required quality\_level 2 \= native Pathfinder quality level 1 \=\= worst\_quality * GDS2 required quality\_level 1 \= native Pathfinder quality level 0 \= bad\_data * GDS2 required quality\_level 0 \= native Pathfinder quality level \-1 \= missing\_data  The original Pathfinder quality level is recorded in the optional variable pathfinder\_quality\_level. |
| `pathfinder_quality_level` | None | 0 | 7 |  |  | The native Pathfinder processing system quality levels, ranging from 0 to 7, where 0 is worst and 7 is best. |
| `l2p_flags` | None |  |  | Used to specify the type of input SST data and pass through native flags from the input L2 SST data set. |
| Bitmask for l2p\_flags * Bit 0: Type of input SST data. 	+ 0: Always set to zero to indicate infrared data. * Bit 1: Land 	+ 0: Input pixel is classified as over ocean. 	+ 1: Pixel area is \>\= 50% land as determined by 	rasterizing the Global Self\-consistent Hierarchical High\-resolution 	Shoreline (GSHHS) Database from the NOAA National Geophysical Data 	Center. * Bit 2: Sea ice fraction 	+ 0: 'sea\_ice\_fraction' is less than 0\.15\. 	+ 1: 'sea\_ice\_fraction' is 0\.15 or greater. * Bit 3: Lake 	+ 0: Pixel area is \< 50% lake covered. 	+ 1: Pixel area is \>\= 50% lake covered as determined from 	rasterizing US World Wildlife Fund's Global Lakes and Wetlands 	Database. * Bit 4: River 	+ 0: Pixel area is \< 50% river covered. 	+ 1: Pixel area is \>\= 50% river covered as determined form 	rasterizing US World Wildlife Fund's Global Lakes and Wetlands 	Database. | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| aerosol\_dynamic\_indicator\_offset | DOUBLE | Aerosol dynamic indicator offset |
| aerosol\_dynamic\_indicator\_scale | DOUBLE | Aerosol dynamic indicator scale |
| date\_created | DOUBLE | Date created |
| day\_or\_night | STRING | Day or night |
| dt\_analysis\_scale | DOUBLE | Dt analysis scale |
| orbit\_node | STRING | Orbit node |
| platform | STRING | Platform |
| principal\_day\_for\_collated\_orbits | STRING | Principal day for collated orbits |
| principal\_year\_for\_collated\_orbits | DOUBLE | Principal year for collated orbits |
| sea\_ice\_fraction\_scale | DOUBLE | Sea ice fraction scale |
| sea\_surface\_temperature\_offset | DOUBLE | Sea surface temperature offset |
| sea\_surface\_temperature\_scale | DOUBLE | Sea surface temperature scale |
| uuid | STRING | Universal unique identifier |




### Terms of Use


**Terms of Use**


NOAA data, information, and products, regardless of the method of delivery,
are not subject to copyright and carry no restrictions on their subsequent
use by the public. Once obtained, they may be put to any lawful use. The
forgoing data is in the public domain and is being provided without
restriction on use and distribution. For more information see the
'constraints' section in
[https://data.nodc.noaa.gov/cgi\-bin/iso?id\=gov.noaa.nodc:AVHRR\_Pathfinder\-NCEI\-L3C\-v5\.3](https://data.nodc.noaa.gov/cgi-bin/iso?id=gov.noaa.nodc:AVHRR_Pathfinder-NCEI-L3C-v5.3).




### Citations



Citations:
* Baker\-Yeboah, S., K. Saha, D. Zhang, K. S. Casey, R. Evans,
and K. A. Kilpatrick (2016\). 'Pathfinder Version 5\.3 AVHRR Sea Surface
Temperature Climate Data Record', Fall AGU 2016 Poster
(manuscript in progress)





### DOIs


* [https://doi.org/10\.7289/V52J68XX](https://doi.org/10.7289/V52J68XX)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CDR/SST_PATHFINDER/V53')
.filter(ee.Filter.date('2014-05-01','2014-05-14'));
varseaSurfaceTemperature=dataset.select('sea_surface_temperature');
varvisParams={
min:0.0,
max:2500.0,
palette:[
'030d81','0519ff','05e8ff','11ff01','fbff01','ff9901','ff0000',
'ad0000'
],
};
Map.setCenter(-121.99,-2.11,2);
Map.addLayer(seaSurfaceTemperature,visParams,'Sea Surface Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_SST_PATHFINDER_V53)


[NOAA AVHRR Pathfinder Version 5\.3 Collated Global 4km Sea Surface Temperature](/earth-engine/datasets/catalog/NOAA_CDR_SST_PATHFINDER_V53)

The AVHRR Pathfinder Version 5\.3 Sea Surface Temperature dataset (PFV53\) is a collection of global, twice\-daily 4km sea surface temperature data produced in a partnership by the NOAA National Oceanographic Data Center and the University of Miami's Rosenstiel School of Marine and Atmospheric Science. PFV53 was computed from data from …

 NOAA/CDR/SST\_PATHFINDER/V53,
 avhrr,noaa,oceans,sst,temperature,wind

1981\-08\-24T00:00:00Z/2023\-12\-30T21:35:08Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7289/V52J68XX](https://doi.org/https://www.ncei.noaa.gov/products/avhrr-pathfinder-sst)
* [https://doi.org/10\.7289/V52J68XX](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_SST_PATHFINDER_V53)









