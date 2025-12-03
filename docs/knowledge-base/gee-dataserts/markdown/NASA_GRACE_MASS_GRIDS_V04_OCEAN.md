



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

GRACE Monthly Mass Grids Release 06 Version 04 \- Ocean


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================================================








Dataset Availability
2002\-04\-04T00:00:00Z–2017\-10\-25T00:00:00Z
Dataset Provider


[NASA Jet Propulsion Laboratory](https://grace.jpl.nasa.gov/data/get-data/monthly-mass-grids-ocean/)



Earth Engine Snippet


`ee.ImageCollection("NASA/GRACE/MASS_GRIDS_V04/OCEAN")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GRACE_MASS_GRIDS_V04_OCEAN)





Tags


[crs](/earth-engine/datasets/tags/crs)
[gfz](/earth-engine/datasets/tags/gfz)
[grace](/earth-engine/datasets/tags/grace)
[gravity](/earth-engine/datasets/tags/gravity)
[jpl](/earth-engine/datasets/tags/jpl)
[mass](/earth-engine/datasets/tags/mass)
[nasa](/earth-engine/datasets/tags/nasa)
[ocean](/earth-engine/datasets/tags/ocean)
[oceans](/earth-engine/datasets/tags/oceans)
[tellus](/earth-engine/datasets/tags/tellus)
[water](/earth-engine/datasets/tags/water)








#### Description



GRACE Tellus Monthly Mass Grids provides monthly
gravitational anomalies relative to a 2004\-2010 time\-mean baseline.
The data contained in this dataset are units of "Equivalent Water Thickness"
which represent the deviations of mass in terms of vertical extent
of water in centimeters. See the provider's [Monthly Mass
Grids Overview](https://grace.jpl.nasa.gov/data/monthly-mass-grids/)
for more details.


The GRACE Tellus (GRCTellus) Monthly Mass Grids Ocean dataset is produced
by three centers: CSR (U. Texas / Center for Space Research),
GFZ (GeoForschungsZentrum Potsdam), and JPL
(NASA Jet Propulsion Laboratory). Each center is a part
of the GRACE Ground System and generates Level\-2 data
(spherical harmonic fields) used in this dataset.
The output includes spherical harmonic coefficients
of the gravity field and of the dealiasing fields used to compute them.
Since each center independently produces the coefficients, the results
may be slightly different. It is recommended for most users to
use the mean of all three datasets. See the provider's [choosing a
solution](https://grace.jpl.nasa.gov/data/choosing-a-solution/) page
for more details.


**Note**


* Land leakage correction: Ocean signals are typically weaker
than land signals, by factors of 2 and more, on seasonal and
interannual time scales. To minimize leakage from high land
signals onto ocean signals, a destriping filter has been applied
which may cause cause correlations over much larger distances.
* The GRCTellus Ocean datasets are optimized to examine regional
ocean bottom pressure, but NOT intended to be spatially
averaged to determine global mean ocean mass.





### Bands



**Pixel Size**
  
111320 meters



**Bands**




| Name | Units | Description |
| --- | --- | --- |
| `lwe_thickness_csr` | cm | Equivalent liquid water thickness in centimeters calculated by CSR. |
| `lwe_thickness_gfz` | cm | Equivalent liquid water thickness in centimeters calculated by GFZ. |
| `lwe_thickness_jpl` | cm | Equivalent liquid water thickness in centimeters calculated by JPL. |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| CSR\_END\_TIME | DOUBLE | End date in milliseconds of spherical harmonics solution from CSR. |
| CSR\_START\_TIME | DOUBLE | Start date in milliseconds of spherical harmonics solution from CSR. |
| GFZ\_END\_TIME | DOUBLE | End date in milliseconds of spherical harmonics solution from GFZ. |
| GFZ\_START\_TIME | DOUBLE | Start date in milliseconds of spherical harmonics solution from GFZ. |
| JPL\_END\_TIME | DOUBLE | End date in milliseconds of spherical harmonics solution from JPL. |
| JPL\_START\_TIME | DOUBLE | Start date in milliseconds of spherical harmonics solution from JPL. |




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
* D.P. Chambers. 2012\. GRACE MONTHLY OCEAN MASS GRIDS NETCDF
RELEASE 6\.0\. Ver. 4\.0\. PO.DAAC, CA, USA. Dataset accessed
\[YYYY\-MM\-DD] at [https://doi.org/10\.5067/TEOCN\-3AC64](https://doi.org/10.5067/TEOCN-3AC64).
* Chambers, D.P. and J.A. Bonin: Evaluation of Release 05
time\-variable gravity coefficients over the ocean. Ocean Science 8,
859\-868, 2012\.
[https://www.ocean\-sci.net/8/859/2012](https://www.ocean-sci.net/8/859/2012).
* Chambers D.P. and J. K. Willis: A Global Evaluation of Ocean Bottom
Pressure from GRACE, OMCT, and Steric\-Corrected Altimetry. J.
of Oceanic and Atmosph. Technology, vol 27, pp 1395\-1402\.
[doi:10\.1175/2010JTECHO738\.1](https://doi.org/10.1175/2010JTECHO738.1),
2010\.





### DOIs


* [https://doi.org/10\.1175/2010JTECHO738\.1](https://doi.org/10.1175/2010JTECHO738.1)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=ee.Image('NASA/GRACE/MASS_GRIDS_V04/OCEAN/20020403_20020430');
varequivalentWaterThicknessCsr=dataset.select('lwe_thickness_csr');
varequivalentWaterThicknessCsrVis={
min:-0.0799629208930322,
max:0.07938676715178997,
palette:['001137','01abab','e7eb05','620500']
};
Map.setCenter(6.746,46.529,1);
Map.addLayer(
equivalentWaterThicknessCsr,equivalentWaterThicknessCsrVis,
'Equivalent Water Thickness CSR');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/NASA/NASA_GRACE_MASS_GRIDS_V04_OCEAN)


[GRACE Monthly Mass Grids Release 06 Version 04 \- Ocean](/earth-engine/datasets/catalog/NASA_GRACE_MASS_GRIDS_V04_OCEAN)

GRACE Tellus Monthly Mass Grids provides monthly gravitational anomalies relative to a 2004\-2010 time\-mean baseline. The data contained in this dataset are units of "Equivalent Water Thickness" which represent the deviations of mass in terms of vertical extent of water in centimeters. See the provider's Monthly Mass Grids Overview for …

 NASA/GRACE/MASS\_GRIDS\_V04/OCEAN,
 crs,gfz,grace,gravity,jpl,mass,nasa,ocean,oceans,tellus,water

2002\-04\-04T00:00:00Z/2017\-10\-25T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1175/2010JTECHO738\.1](https://doi.org/https://grace.jpl.nasa.gov/data/get-data/monthly-mass-grids-ocean/)
* [https://doi.org/10\.1175/2010JTECHO738\.1](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/NASA_GRACE_MASS_GRIDS_V04_OCEAN)









