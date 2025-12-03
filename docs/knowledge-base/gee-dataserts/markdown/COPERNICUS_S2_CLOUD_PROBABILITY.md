



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Sentinel\-2: Cloud Probability


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
================================================================================================================================








Dataset Availability
2015\-06\-27T00:00:00Z–2025\-07\-19T04:27:31Z
Dataset Provider


[European Union/ESA/Copernicus/SentinelHub](https://sentinel.esa.int/web/sentinel/user-guides/sentinel-2-msi/processing-levels/level-1)



Earth Engine Snippet


`ee.ImageCollection("COPERNICUS/S2_CLOUD_PROBABILITY")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S2_CLOUD_PROBABILITY)





Revisit Interval
5 Days
Tags


[cloud](/earth-engine/datasets/tags/cloud)
[copernicus](/earth-engine/datasets/tags/copernicus)
[esa](/earth-engine/datasets/tags/esa)
[eu](/earth-engine/datasets/tags/eu)
[msi](/earth-engine/datasets/tags/msi)
[radiance](/earth-engine/datasets/tags/radiance)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sentinel](/earth-engine/datasets/tags/sentinel)
sentinelhub








#### Description



The S2 cloud probability is created with the
[sentinel2\-cloud\-detector](https://github.com/sentinel-hub/sentinel2-cloud-detector)
library (using [LightGBM](https://github.com/microsoft/LightGBM)).
All bands are upsampled using bilinear interpolation to 10m resolution
before the gradient boost base algorithm is applied. The resulting
`0..1` floating point probability is scaled to `0..100` and stored as
an UINT8\. Areas missing any or all of the bands are masked out.
Higher values are more likely to be clouds or highly reflective surfaces
(e.g. roof tops or snow).


Sentinel\-2 is a wide\-swath, high\-resolution, multi\-spectral
imaging mission supporting Copernicus Land Monitoring studies,
including the monitoring of vegetation, soil and water cover,
as well as observation of inland waterways and coastal areas.


The Level\-2 data can be found in the collection
[COPERNICUS/S2\_SR\_HARMONIZED](/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED). The Level\-1B data can be found in the collection
[COPERNICUS/S2\_HARMONIZED](/earth-engine/datasets/catalog/COPERNICUS_S2_HARMONIZED). Additional metadata is available on assets in those
collections.


See
[this tutorial](https://developers.google.com/earth-engine/tutorials/community/sentinel-2-s2cloudless)
explaining how to apply the cloud mask.





### Bands


**Bands**




| Name | Min | Max | Pixel Size | Description |
| --- | --- | --- | --- | --- |
| `probability` | 0 | 100 | Probability that the pixel is cloudy. |




### Terms of Use


**Terms of Use**


The use of Sentinel data is governed by the [Copernicus
Sentinel Data Terms and Conditions.](https://scihub.copernicus.eu/twiki/pub/SciHubWebPortal/TermsConditions/Sentinel_Data_Terms_and_Conditions.pdf)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vars2Sr=ee.ImageCollection('COPERNICUS/S2_SR_HARMONIZED');
vars2Clouds=ee.ImageCollection('COPERNICUS/S2_CLOUD_PROBABILITY');

varSTART_DATE=ee.Date('2019-01-01');
varEND_DATE=ee.Date('2019-03-01');
varMAX_CLOUD_PROBABILITY=65;
varregion=
ee.Geometry.Rectangle({coords:[-76.5,2.0,-74,4.0],geodesic:false});
Map.setCenter(-75,3,12);

functionmaskClouds(img){
varclouds=ee.Image(img.get('cloud_mask')).select('probability');
varisNotCloud=clouds.lt(MAX_CLOUD_PROBABILITY);
returnimg.updateMask(isNotCloud);
}

// The masks for the 10m bands sometimes do not exclude bad data at
// scene edges, so we apply masks from the 20m and 60m bands as well.
// Example asset that needs this operation:
// COPERNICUS/S2_CLOUD_PROBABILITY/20190301T000239_20190301T000238_T55GDP
functionmaskEdges(s2_img){
returns2_img.updateMask(
s2_img.select('B8A').mask().updateMask(s2_img.select('B9').mask()));
}

// Filter input collections by desired data range and region.
varcriteria=ee.Filter.and(
ee.Filter.bounds(region),ee.Filter.date(START_DATE,END_DATE));
s2Sr=s2Sr.filter(criteria).map(maskEdges);
s2Clouds=s2Clouds.filter(criteria);

// Join S2 SR with cloud probability dataset to add cloud mask.
vars2SrWithCloudMask=ee.Join.saveFirst('cloud_mask').apply({
primary:s2Sr,
secondary:s2Clouds,
condition:
ee.Filter.equals({leftField:'system:index',rightField:'system:index'})
});

vars2CloudMasked=
ee.ImageCollection(s2SrWithCloudMask).map(maskClouds).median();
varrgbVis={min:0,max:3000,bands:['B4','B3','B2']};

Map.addLayer(
s2CloudMasked,rgbVis,'S2 SR masked at '+MAX_CLOUD_PROBABILITY+'%',
true);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/COPERNICUS/COPERNICUS_S2_CLOUD_PROBABILITY)


[Sentinel\-2: Cloud Probability](/earth-engine/datasets/catalog/COPERNICUS_S2_CLOUD_PROBABILITY)

The S2 cloud probability is created with the sentinel2\-cloud\-detector library (using LightGBM). All bands are upsampled using bilinear interpolation to 10m resolution before the gradient boost base algorithm is applied. The resulting 0\..1 floating point probability is scaled to 0\..100 and stored as an UINT8\. Areas missing any or all …

 COPERNICUS/S2\_CLOUD\_PROBABILITY,
 cloud,copernicus,esa,eu,msi,radiance,satellite\-imagery,sentinel

2015\-06\-27T00:00:00Z/2025\-07\-19T04:27:31Z



 \-56 \-180 83 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








