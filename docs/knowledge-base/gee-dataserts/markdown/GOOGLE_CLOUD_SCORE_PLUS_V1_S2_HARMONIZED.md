



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Cloud Score\+ S2\_HARMONIZED V1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=================================================================================================================================








Dataset Availability
2015\-06\-27T00:00:00Z–2025\-07\-19T02:22:07\.412000Z
Dataset Provider


[Google Earth Engine](https://earthengine.google.com/)



Earth Engine Snippet


`ee.ImageCollection("GOOGLE/CLOUD_SCORE_PLUS/V1/S2_HARMONIZED")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_CLOUD_SCORE_PLUS_V1_S2_HARMONIZED)





Tags


[cloud](/earth-engine/datasets/tags/cloud)
[google](/earth-engine/datasets/tags/google)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)








#### Description



Cloud Score\+ is a quality assessment (QA) processor for medium\-to\-high
resolution optical satellite imagery. The Cloud Score\+ S2\_HARMONIZED
dataset is being operationally produced from the
[harmonized Sentinel\-2 L1C collection](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_HARMONIZED),
and Cloud Score\+ outputs can be used to identify relatively clear pixels and
effectively remove clouds and cloud shadows from [L1C (Top\-of\-Atmosphere)](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_HARMONIZED)
or [L2A (Surface Reflectance)](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)
imagery.


The Cloud Score\+ S2\_HARMONIZED dataset includes two QA bands, `cs` and
`cs_cdf`, that both grade the usability of individual pixels with respect to
surface visibility on a continuous scale between 0 and 1, where 0 represents
"not clear" (occluded), while 1 represents "clear" (unoccluded) observations.
The `cs` band scores QA based on a spectral distance between the observed
pixel and a (theoretical) clear reference observation, while the `cs_cdf` band
represents the likelihood an observed pixel is clear based on an estimated
cumulative distribution of scores for a given location through time. In
other words, `cs` can be thought of as a more instantaneous atmospheric
similarity score (i.e., how similar is this pixel to what we'd expect to
see in a perfectly a clear reference), while `cs_cdf` captures an expectation
of the estimated score through time (i.e., if we had all the scores for this
pixel through time, how would this score rank?).


Images in the Cloud Score\+ S2\_HARMONIZED collection have the same id and
`system:index` properties as the individual [Sentinel\-2 L1C](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_HARMONIZED)
assets from which they were produced such that Cloud Score\+ bands can be
linked to source images based on their shared `system:index`.


Cloud Score\+ backfill for the entire Sentinel\-2 archive is currently in
progress and Dataset Availability dates will be updated periodically as new
results are added to the Cloud Score\+ collection.


For more information about the Cloud Score\+ dataset and modelling
approach, see
[this Medium post](https://medium.com/google-earth/all-clear-with-cloud-score-bd6ee2e2235e).





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `cs` | Dimensionless | 0 | 1 | Pixel quality score based on spectral distance from a (theoretical) clear reference |
| `cs_cdf` | Dimensionless | 0 | 1 | Value of the cumulative distribution function of possible `cs` values for the estimated `cs` value |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| DATE\_PRODUCT\_GENERATED | STRING | Production date. |
| MGRS\_TILE | STRING | Sentinel\-2 Military Grid Reference System ID. |
| MODEL\_VERSION | STRING | Cloud Score\+ model version. |
| NO\_CONTEXT\_FRACTION | DOUBLE | Fraction of subtiles processed with no temporal context. |
| PROCESSING\_SOFTWARE\_VERSION | STRING | Cloud Score\+ processing software version. |
| SOURCE\_ASSET\_ID | STRING | Earth Engine Asset ID for source image. |
| SOURCE\_PRODUCT\_ID | STRING | Sentinel\-2 Product ID for source image. |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Pasquarella, V. J., Brown, C. F., Czerwinski, W., \& Rucklidge, W. J. (2023\)
Comprehensive Quality Assessment of Optical Satellite Imagery Using Weakly
Supervised Video Learning. In Proceedings of the IEEE/CVF Conference on
Computer Vision and Pattern Recognition (pp. 2124\-2134\).
[PDF](https://openaccess.thecvf.com/content/CVPR2023W/EarthVision/html/Pasquarella_Comprehensive_Quality_Assessment_of_Optical_Satellite_Imagery_Using_Weakly_Supervised_CVPRW_2023_paper.html)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Harmonized Sentinel-2 Level 2A collection.
vars2=ee.ImageCollection('COPERNICUS/S2_SR_HARMONIZED');

// Cloud Score+ image collection. Note Cloud Score+ is produced from Sentinel-2
// Level 1C data and can be applied to either L1C or L2A collections.
varcsPlus=ee.ImageCollection('GOOGLE/CLOUD_SCORE_PLUS/V1/S2_HARMONIZED');

// Region of interest.
varROI=ee.Geometry.Point(-119.9087,37.4159);

// Use 'cs' or 'cs_cdf', depending on your use case; see docs for guidance.
varQA_BAND='cs_cdf';

// The threshold for masking; values between 0.50 and 0.65 generally work well.
// Higher values will remove thin clouds, haze & cirrus shadows.
varCLEAR_THRESHOLD=0.60;

// Make a clear median composite.
varcomposite=s2
.filterBounds(ROI)
.filterDate('2023-01-01','2023-02-01')
.linkCollection(csPlus,[QA_BAND])
.map(function(img){
returnimg.updateMask(img.select(QA_BAND).gte(CLEAR_THRESHOLD));
})
.median();

// Sentinel-2 visualization parameters.
vars2Viz={bands:['B4','B3','B2'],min:0,max:2500};

Map.addLayer(composite,s2Viz,'median composite');
Map.centerObject(ROI,11);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_CLOUD_SCORE_PLUS_V1_S2_HARMONIZED)


[Cloud Score\+ S2\_HARMONIZED V1](/earth-engine/datasets/catalog/GOOGLE_CLOUD_SCORE_PLUS_V1_S2_HARMONIZED)

Cloud Score\+ is a quality assessment (QA) processor for medium\-to\-high resolution optical satellite imagery. The Cloud Score\+ S2\_HARMONIZED dataset is being operationally produced from the harmonized Sentinel\-2 L1C collection, and Cloud Score\+ outputs can be used to identify relatively clear pixels and effectively remove clouds and cloud shadows from L1C …

 GOOGLE/CLOUD\_SCORE\_PLUS/V1/S2\_HARMONIZED,
 cloud,google,satellite\-imagery,sentinel2\-derived

2015\-06\-27T00:00:00Z/2025\-07\-19T02:22:07\.412000Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








