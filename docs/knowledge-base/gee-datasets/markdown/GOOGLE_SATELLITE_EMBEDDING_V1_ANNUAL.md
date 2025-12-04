



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Satellite Embedding V1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
========================================================================================================================








Dataset Availability
2017\-01\-01T00:00:00Z–2024\-01\-01T00:00:00Z
Dataset Provider


[Google Earth Engine](https://earthengine.google.com/)


[Google DeepMind](https://deepmind.google/)



Earth Engine Snippet


`ee.ImageCollection("GOOGLE/SATELLITE_EMBEDDING/V1/ANNUAL")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_SATELLITE_EMBEDDING_V1_ANNUAL)





Tags


[annual](/earth-engine/datasets/tags/annual)
[global](/earth-engine/datasets/tags/global)
[google](/earth-engine/datasets/tags/google)
[landsat\-derived](/earth-engine/datasets/tags/landsat-derived)
[satellite\-imagery](/earth-engine/datasets/tags/satellite-imagery)
[sentinel1\-derived](/earth-engine/datasets/tags/sentinel1-derived)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)








#### Description



The Google Satellite Embedding dataset is a global, analysis\-ready
collection of learned geospatial [embeddings](https://developers.google.com/machine-learning/crash-course/embeddings/embedding-space).
Each 10\-meter pixel in this dataset is a 64\-dimensional representation, or
"[embedding vector](https://developers.google.com/machine-learning/glossary#embedding-vector),"
that encodes temporal trajectories of surface conditions at and around that
pixel as measured by various Earth observation instruments and datasets,
over a single calendar year. Unlike conventional spectral inputs and
indices, where bands reflect physical measurements, embeddings are feature
vectors that summarize relationships across multi\-source, multi\-modal
observations in a less directly interpretable, but more powerful way.


The dataset covers terrestrial land surfaces and shallow waters, including
intertidal and reef zones, inland waterways, and coastal waterways.
Coverage at the poles is limited by satellite orbits and instrument
coverage.


The collection is composed of images covering approximately 163,840 meters
by 163,840 meters, and each image has 64 bands `{A00, A01, …, A63}`, one for
each axis of the 64D embedding space. All bands should be used for
downstream analysis as they collectively refer to a 64D coordinate in
the embedding space and are not independently interpretable.


All images are generated in their local Universal Transverse Mercator
projection as indicated by the UTM\_ZONE property, and have
`system:time_start` and `system:time_end` properties that reflect the
calendar year summarized by the embeddings; for example, an embedding image
for 2021 will have a `system:start_time` equal to
`ee.Date('2021-01-01 00:00:00')` and a `system:end_time` equal to
`ee.Date('2022-01-01 00:00:00')`.


The embeddings are unit\-length, meaning they have a magnitude of 1 and
do not require any additional normalization, and are distributed across the
[unit sphere](https://en.wikipedia.org/wiki/Unit_sphere), making them
well\-suited for use with clustering algorithms and tree\-based classifiers.
The embedding space is also consistent across years, and embeddings from
different years can be used for condition change detection by considering
the dot product or angle between two embedding vectors. Furthermore, the
embeddings are designed to be linearly composable, i.e., they can be
aggregated to produce embeddings at coarser spatial resolutions or
transformed with vector arithmetic, and still retain their semantic meaning
and distance relationships.


The embeddings are produced by a geospatial model that assimilates multiple
sources including optical, radar, LiDAR, and other sources (Brown,
Kazmierski, Pasquarella et al., in review).


Because representations are learned across many sensors and images,
embedding representations effectively mitigate common issues such as
clouds, scan lines, sensor artifacts, or missing data, providing seamless
analysis\-ready features that can be directly substituted for other Earth
Observation image sources in classification, regression, and change
detection analyses. While some large scale swath and data availability
artifacts may be noticeable, these typically represent minor vector offsets
and generally do not significantly affect downstream processing or results.





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Units | Min | Max | Description |
| --- | --- | --- | --- | --- |
| `A00` | Dimensionless | \-1 | 1 | The 0th axis of the embedding vector. |
| `A01` | Dimensionless | \-1 | 1 | The 1st axis of the embedding vector. |
| `A02` | Dimensionless | \-1 | 1 | The 2nd axis of the embedding vector. |
| `A03` | Dimensionless | \-1 | 1 | The 3rd axis of the embedding vector. |
| `A04` | Dimensionless | \-1 | 1 | The 4th axis of the embedding vector. |
| `A05` | Dimensionless | \-1 | 1 | The 5th axis of the embedding vector. |
| `A06` | Dimensionless | \-1 | 1 | The 6th axis of the embedding vector. |
| `A07` | Dimensionless | \-1 | 1 | The 7th axis of the embedding vector. |
| `A08` | Dimensionless | \-1 | 1 | The 8th axis of the embedding vector. |
| `A09` | Dimensionless | \-1 | 1 | The 9th axis of the embedding vector. |
| `A10` | Dimensionless | \-1 | 1 | The 10th axis of the embedding vector. |
| `A11` | Dimensionless | \-1 | 1 | The 11th axis of the embedding vector. |
| `A12` | Dimensionless | \-1 | 1 | The 12th axis of the embedding vector. |
| `A13` | Dimensionless | \-1 | 1 | The 13th axis of the embedding vector. |
| `A14` | Dimensionless | \-1 | 1 | The 14th axis of the embedding vector. |
| `A15` | Dimensionless | \-1 | 1 | The 15th axis of the embedding vector. |
| `A16` | Dimensionless | \-1 | 1 | The 16th axis of the embedding vector. |
| `A17` | Dimensionless | \-1 | 1 | The 17th axis of the embedding vector. |
| `A18` | Dimensionless | \-1 | 1 | The 18th axis of the embedding vector. |
| `A19` | Dimensionless | \-1 | 1 | The 19th axis of the embedding vector. |
| `A20` | Dimensionless | \-1 | 1 | The 20th axis of the embedding vector. |
| `A21` | Dimensionless | \-1 | 1 | The 21st axis of the embedding vector. |
| `A22` | Dimensionless | \-1 | 1 | The 22nd axis of the embedding vector. |
| `A23` | Dimensionless | \-1 | 1 | The 23rd axis of the embedding vector. |
| `A24` | Dimensionless | \-1 | 1 | The 24th axis of the embedding vector. |
| `A25` | Dimensionless | \-1 | 1 | The 25th axis of the embedding vector. |
| `A26` | Dimensionless | \-1 | 1 | The 26th axis of the embedding vector. |
| `A27` | Dimensionless | \-1 | 1 | The 27th axis of the embedding vector. |
| `A28` | Dimensionless | \-1 | 1 | The 28th axis of the embedding vector. |
| `A29` | Dimensionless | \-1 | 1 | The 29th axis of the embedding vector. |
| `A30` | Dimensionless | \-1 | 1 | The 30th axis of the embedding vector. |
| `A31` | Dimensionless | \-1 | 1 | The 31st axis of the embedding vector. |
| `A32` | Dimensionless | \-1 | 1 | The 32nd axis of the embedding vector. |
| `A33` | Dimensionless | \-1 | 1 | The 33rd axis of the embedding vector. |
| `A34` | Dimensionless | \-1 | 1 | The 34th axis of the embedding vector. |
| `A35` | Dimensionless | \-1 | 1 | The 35th axis of the embedding vector. |
| `A36` | Dimensionless | \-1 | 1 | The 36th axis of the embedding vector. |
| `A37` | Dimensionless | \-1 | 1 | The 37th axis of the embedding vector. |
| `A38` | Dimensionless | \-1 | 1 | The 38th axis of the embedding vector. |
| `A39` | Dimensionless | \-1 | 1 | The 39th axis of the embedding vector. |
| `A40` | Dimensionless | \-1 | 1 | The 40th axis of the embedding vector. |
| `A41` | Dimensionless | \-1 | 1 | The 41st axis of the embedding vector. |
| `A42` | Dimensionless | \-1 | 1 | The 42nd axis of the embedding vector. |
| `A43` | Dimensionless | \-1 | 1 | The 43rd axis of the embedding vector. |
| `A44` | Dimensionless | \-1 | 1 | The 44th axis of the embedding vector. |
| `A45` | Dimensionless | \-1 | 1 | The 45th axis of the embedding vector. |
| `A46` | Dimensionless | \-1 | 1 | The 46th axis of the embedding vector. |
| `A47` | Dimensionless | \-1 | 1 | The 47th axis of the embedding vector. |
| `A48` | Dimensionless | \-1 | 1 | The 48th axis of the embedding vector. |
| `A49` | Dimensionless | \-1 | 1 | The 49th axis of the embedding vector. |
| `A50` | Dimensionless | \-1 | 1 | The 50th axis of the embedding vector. |
| `A51` | Dimensionless | \-1 | 1 | The 51st axis of the embedding vector. |
| `A52` | Dimensionless | \-1 | 1 | The 52nd axis of the embedding vector. |
| `A53` | Dimensionless | \-1 | 1 | The 53rd axis of the embedding vector. |
| `A54` | Dimensionless | \-1 | 1 | The 54th axis of the embedding vector. |
| `A55` | Dimensionless | \-1 | 1 | The 55th axis of the embedding vector. |
| `A56` | Dimensionless | \-1 | 1 | The 56th axis of the embedding vector. |
| `A57` | Dimensionless | \-1 | 1 | The 57th axis of the embedding vector. |
| `A58` | Dimensionless | \-1 | 1 | The 58th axis of the embedding vector. |
| `A59` | Dimensionless | \-1 | 1 | The 59th axis of the embedding vector. |
| `A60` | Dimensionless | \-1 | 1 | The 60th axis of the embedding vector. |
| `A61` | Dimensionless | \-1 | 1 | The 61st axis of the embedding vector. |
| `A62` | Dimensionless | \-1 | 1 | The 62nd axis of the embedding vector. |
| `A63` | Dimensionless | \-1 | 1 | The 63rd axis of the embedding vector. |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| MODEL\_VERSION | STRING | The version string uniquely identifying the model version used to produce the image. |
| PROCESSING\_SOFTWARE\_VERSION | STRING | The version string uniquely identifying the model data processing software used to produce the image. |
| UTM\_ZONE | STRING | The UTM zone of the coordinate reference system used to produce the image. |
| DATASET\_VERSION | STRING | The dataset version. |




### Terms of Use


**Terms of Use**


This dataset is licensed under
[CC\-BY 4\.0](https://creativecommons.org/licenses/by/4.0/) and requires
the following attribution text: "This dataset is produced by Google and
Google DeepMind."




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Load collection.
vardataset=ee.ImageCollection('GOOGLE/SATELLITE_EMBEDDING/V1/ANNUAL');

// Point of interest.
varpoint=ee.Geometry.Point(-121.8036,39.0372);

// Get embedding images for two years.
varimage1=dataset
.filterDate('2023-01-01','2024-01-01')
.filterBounds(point)
.first();

varimage2=dataset
.filterDate('2024-01-01','2025-01-01')
.filterBounds(point)
.first();

// Visualize three axes of the embedding space as an RGB.
varvisParams={min:-0.3,max:0.3,bands:['A01','A16','A09']};

Map.addLayer(image1,visParams,'2023 embeddings');
Map.addLayer(image2,visParams,'2024 embeddings');

// Calculate dot product as a measure of similarity between embedding vectors.
// Note for vectors with a magnitude of 1, this simplifies to the cosine of the
// angle between embedding vectors.
vardotProd=image1
.multiply(image2)
.reduce(ee.Reducer.sum());

// Add dot product to the map.
Map.addLayer(
dotProd,
{min:0,max:1,palette:['white','black']},
'Similarity between years (brighter = less similar)'
);

Map.centerObject(point,12);
Map.setOptions('SATELLITE');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_SATELLITE_EMBEDDING_V1_ANNUAL)


[Satellite Embedding V1](/earth-engine/datasets/catalog/GOOGLE_SATELLITE_EMBEDDING_V1_ANNUAL)

The Google Satellite Embedding dataset is a global, analysis\-ready collection of learned geospatial embeddings. Each 10\-meter pixel in this dataset is a 64\-dimensional representation, or "embedding vector," that encodes temporal trajectories of surface conditions at and around that pixel as measured by various Earth observation instruments and datasets, over a …

 GOOGLE/SATELLITE\_EMBEDDING/V1/ANNUAL,
 annual,global,google,landsat\-derived,satellite\-imagery,sentinel1\-derived,sentinel2\-derived

2017\-01\-01T00:00:00Z/2024\-01\-01T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








