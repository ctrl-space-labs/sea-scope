



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

NOAA CDR GRIDSAT\-B1: Geostationary IR Channel Brightness Temperature


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=======================================================================================================================================================================








Dataset Availability
1980\-01\-01T00:00:00Z–2024\-09\-30T21:00:00Z
Dataset Provider


[NOAA](https://www.ncei.noaa.gov/products/climate-data-records/geostationary-IR-channel-brightness-temperature)



Earth Engine Snippet


`ee.ImageCollection("NOAA/CDR/GRIDSAT-B1/V2")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_GRIDSAT-B1_V2)





Cadence
3 Hours
Tags


[brightness](/earth-engine/datasets/tags/brightness)
[cdr](/earth-engine/datasets/tags/cdr)
[climate](/earth-engine/datasets/tags/climate)
[infrared](/earth-engine/datasets/tags/infrared)
[noaa](/earth-engine/datasets/tags/noaa)
[reflectance](/earth-engine/datasets/tags/reflectance)
[sr](/earth-engine/datasets/tags/sr)
fundamental
geostationary
isccp








#### Description



**Note:** This dataset has not been updated by the provider since 2024\-03\-31
due to ongoing infrastructure updates. There is no current timeline for when
dataset updates will resume.
This dataset provides a high quality Climate Data
Record (CDR) of global infrared measurements from geostationary satellites.


The geostationary satellite data (GridSat\-B1\) provides data from 3
channels: the CDR\-quality infrared window (IRWIN) channel (near 11µm),
the visible channel (near 0\.6µm) and the infrared water vapor (IRWVP)
channel (near 6\.7µm). The GridSat\-B1 data is projected onto a global
0\.07 degree latitude equal\-angle grid with date coverage spanning from
1980\-present. This data is sourced from the 3\-hourly International Satellite
Cloud Climatology Project (ISCCP) B1 data. The satellites included in this
dataset with their longitudinal coverage over time can be seen [here](https://www.ncdc.noaa.gov/gridsat/images/isccp_coverage_VZA60_nolegend.png).
In regions of overlap the CDR methodology merges satellites by selecting
the nadir\-most observations for each grid point.


Notes:


* Mappings from satid to satellite name are contained in the image's
properties as satid\_number: "satellite\_name", e.g. satid\_0: GOES\-13,
satid\_1: GOES\-15, and satid\_2: GOES\-16\.
* IRWIN data has been corrected for view zenith angle, but this correction
is not perfect. It also treats all satellites the same way, whereas the
view zenith angle dependence will vary by satellite. Some VZA residual
will be apparent.
* IRWVP data has no view zenith angle correction and is not CDR quality.
* VSCHN data has no view zenith angle corrections and is not CDR quality.
* Removing the View Zenigth Angle correction for the IRWIN channels can be
done with the following:
Original\_temperature\_observed \= irwin\_cdr \- irwin\_vza\_adj





### Bands



**Pixel Size**
  
7792 meters



**Bands**




| Name | Units | Min | Max | Scale | Offset | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `irwin_cdr` | K | \-2093\* | 13615\* | 0\.01 | 200 | Brightness temperature near 11µm, nadir\-most observation |
| `irwin_2` | K | \-4123\* | 13579\* | 0\.01 | 200 | Brightness temperature near 11µm, second\-best observation (based on view zenith angle) |
| `irwin_3` | K | \-1624\* | 14240\* | 0\.01 | 200 | Brightness temperature, third\-best observation based on view zenith angle |
| `irwvp` | K | \-5907\* | 10219\* | 0\.01 | 200 | Brightness temperature near 6\.7µm, nadir\-most observation |
| `irwvp_2` | K | \-5081\* | 10260\* | 0\.01 | 200 | Brightness temperature near 6\.7µm, second\-best observation based on view zenith angle |
| `vschn` | None | \-25000\* | 4275\* | 4e\-05 | 1 | Visible reflectance near 0\.6µm, nadir\-most observation |
| `vschn_2` | None | \-25000\* | 3800\* | 4e\-05 | 1 | Visible reflectance near 0\.6µm, second\-best observation based on view zenith angle |
| `irwin_vza_adj` | K | 36\* | 171\* | 0\.25 | \-10 | Adjustment made to all IRWIN channels. Provided to allow users to reverse the view zenith correction for the irwin\_cdr variable. |
| `satid_ir1` | None | 0\* | 5\* |  |  | satid values for irwin\_cdr. For this and other satid bands, the mappings of satid to satellite name are given in the properties for each image |
| `satid_ir2` | None | 0\* | 5\* |  |  | satid values per pixel for irwin\_2 |
| `satid_ir3` | None | 0\* | 5\* |  |  | satid values per pixel for irwin\_3 |
| `satid_wv1` | None | 0\* | 5\* |  |  | satid values per pixel for irwvp |
| `satid_wv2` | None | 0\* | 5\* |  |  | satid values per pixel for irwvp2 |
| `satid_vs1` | None | 0\* | 5\* |  |  | satid values per pixel for vischn |
| `satid_vs2` | None | 0\* | 5\* |  |  | satid values per pixel for vischn2 |


 \* estimated min or max value


### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| satid\_0 | STRING | Satellite name (see notes) |
| satid\_1 | STRING | Satellite name (see notes) |
| satid\_2 | STRING | Satellite name (see notes) |
| satid\_3 | STRING | Satellite name (see notes) |
| satid\_4 | STRING | Satellite name (see notes) |
| satid\_5 | STRING | Satellite name (see notes) |




### Terms of Use


**Terms of Use**


The NOAA CDR Program's official distribution point for CDRs is NOAA's
National Climatic Data Center which provides sustained, open access and
active data management of the CDR packages and related information in
keeping with the United States' open data policies and practices as
described in the President's Memorandum on "Open Data Policy" and pursuant
to the Executive Order of May 9, 2013, "Making Open and Machine Readable
the New Default for Government Information". In line with these policies,
the CDR data sets are nonproprietary, publicly available, and no
restrictions are placed upon their use. For more information, see the
[Fair Use of NOAA's CDR Data Sets, Algorithms and Documentation](https://www1.ncdc.noaa.gov/pub/data/sds/cdr/CDRs/Aerosol_Optical_Thickness/UseAgreement_01B-04.pdf)
pdf.




### Citations



Citations:
* Kenneth R. Knapp, and NOAA CDR Program (2014\): NOAA Climate Data Record
(CDR) of Gridded Satellite Data from ISCCP B1 (GridSat\-B1\) 11 micron
Brightness Temperature, Version 2\. \[indicate subset used]. NOAA National
Climatic Data Center. [doi:10\.7289/V59P2ZKR](https://doi.org/10.7289/V59P2ZKR)
\[access date].
* Knapp, K. R., S. Ansari, C. L. Bain, M. A. Bourassa, M. J. Dickinson,
C. Funk, C. N. Helms, C. C. Hennon, C. D. Holmes, G. J. Huffman, J. P.
Kossin, H.\-T. Lee, A. Loew, and G. Magnusdottir, 2011: Globally gridded
satellite (GridSat) observations for climate studies. Bulletin of the
American Meteorological Society, 92, 893\-907\.
[doi:10\.1175/2011BAMS3039\.1](https://doi.org/10.1175/2011BAMS3039.1)





### DOIs


* [https://doi.org/10\.1175/2011BAMS3039\.1](https://doi.org/10.1175/2011BAMS3039.1)
* [https://doi.org/10\.7289/V59P2ZKR](https://doi.org/10.7289/V59P2ZKR)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.ImageCollection('NOAA/CDR/GRIDSAT-B1/V2')
.filter(ee.Filter.date('2017-05-01','2017-05-14'));
varbrightnessTemp=dataset.select(['irwin_cdr','vschn','irwvp']);
varbrightnessTempVis={
min:500.0,
max:10000.0,
};
Map.setCenter(7.71,17.93,2);
Map.addLayer(brightnessTemp,brightnessTempVis,'Brightness Temperature');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NOAA/NOAA_CDR_GRIDSAT-B1_V2)


[NOAA CDR GRIDSAT\-B1: Geostationary IR Channel Brightness Temperature](/earth-engine/datasets/catalog/NOAA_CDR_GRIDSAT-B1_V2)

Note: This dataset has not been updated by the provider since 2024\-03\-31 due to ongoing infrastructure updates. There is no current timeline for when dataset updates will resume. This dataset provides a high quality Climate Data Record (CDR) of global infrared measurements from geostationary satellites. The geostationary satellite data (GridSat\-B1\) …

 NOAA/CDR/GRIDSAT\-B1/V2,
 brightness,cdr,climate,infrared,noaa,reflectance,sr

1980\-01\-01T00:00:00Z/2024\-09\-30T21:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.7289/V59P2ZKR](https://doi.org/https://www.ncei.noaa.gov/products/climate-data-records/geostationary-IR-channel-brightness-temperature)
* [https://doi.org/10\.7289/V59P2ZKR](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_GRIDSAT-B1_V2)









