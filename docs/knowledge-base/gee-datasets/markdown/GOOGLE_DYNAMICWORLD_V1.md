



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

Dynamic World V1


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==================================================================================================================








Dataset Availability
2015\-06\-27T00:00:00Z–2025\-07\-19T03:39:26\.559000Z
Dataset Provider


[World Resources Institute](https://www.wri.org/)


[Google](https://research.google.com/)



Earth Engine Snippet


`ee.ImageCollection("GOOGLE/DYNAMICWORLD/V1")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_DYNAMICWORLD_V1)





Tags


[global](/earth-engine/datasets/tags/global)
[google](/earth-engine/datasets/tags/google)
[landcover](/earth-engine/datasets/tags/landcover)
[landuse](/earth-engine/datasets/tags/landuse)
[landuse\-landcover](/earth-engine/datasets/tags/landuse-landcover)
[nrt](/earth-engine/datasets/tags/nrt)
[sentinel2\-derived](/earth-engine/datasets/tags/sentinel2-derived)








#### Description



Dynamic World is a 10m near\-real\-time (NRT) Land Use/Land Cover (LULC)
dataset that includes class probabilities and label information for nine
classes.


Dynamic World predictions are available for the Sentinel\-2 L1C collection
from 2015\-06\-27 to present. The revisit frequency of Sentinel\-2 is between
2\-5 days depending on latitude. Dynamic World predictions are generated for
Sentinel\-2 L1C images with CLOUDY\_PIXEL\_PERCENTAGE \<\= 35%.
Predictions are masked to remove clouds and cloud shadows using
a combination of S2 Cloud Probability, Cloud Displacement Index, and
Directional Distance Transform.


Images in the Dynamic World collection have names matching the individual
Sentinel\-2 L1C asset names from which they were derived, e.g:


ee.Image('COPERNICUS/S2/20160711T084022\_20160711T084751\_T35PKT')


has a matching Dynamic World image named:
 ee.Image('GOOGLE/DYNAMICWORLD/V1/20160711T084022\_20160711T084751\_T35PKT').


All probability bands except the "label" band collectively sum to 1\.


To learn more about the Dynamic World dataset and see examples for
generating composites, calculating regional statistics, and working with the
time series, see the [Introduction to Dynamic World](https://developers.google.com/earth-engine/tutorials/community/introduction-to-dynamic-world-pt-1) tutorial series.


Given Dynamic World class estimations are derived from single images using a
spatial context from a small moving window, top\-1 "probabilities" for
predicted land covers that are in\-part defined by cover over time, like
crops, can be comparatively low in the absence of obvious distinguishing
features. High\-return surfaces in arid climates, sand, sunglint, etc may
also exhibit this phenomenon.


To select only pixels that confidently belong to a Dynamic World class,
it is recommended to mask Dynamic World outputs by thresholding the
estimated "probability" of the top\-1 prediction.





### Bands



**Pixel Size**
  
10 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `water` | 0 | 1 | Estimated probability of complete coverage by water |
| `trees` | 0 | 1 | Estimated probability of complete coverage by trees |
| `grass` | 0 | 1 | Estimated probability of complete coverage by grass |
| `flooded_vegetation` | 0 | 1 | Estimated probability of complete coverage by flooded vegetation |
| `crops` | 0 | 1 | Estimated probability of complete coverage by crops |
| `shrub_and_scrub` | 0 | 1 | Estimated probability of complete coverage by shrub and scrub |
| `built` | 0 | 1 | Estimated probability of complete coverage by built |
| `bare` | 0 | 1 | Estimated probability of complete coverage by bare |
| `snow_and_ice` | 0 | 1 | Estimated probability of complete coverage by snow and ice |
| `label` | 0 | 8 | Index of the band with the highest estimated probability |


**label Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#419bdf | water |
| 1 | \#397d49 | trees |
| 2 | \#88b053 | grass |
| 3 | \#7a87c6 | flooded\_vegetation |
| 4 | \#e49635 | crops |
| 5 | \#dfc35a | shrub\_and\_scrub |
| 6 | \#c4281b | built |
| 7 | \#a59b8f | bare |
| 8 | \#b39fe1 | snow\_and\_ice |




### Image Properties


**Image Properties**




| Name | Type | Description |
| --- | --- | --- |
| dynamicworld\_algorithm\_version | STRING | The version string uniquely identifying the Dynamic World model and inference process used to produce the image. |
| qa\_algorithm\_version | STRING | The version string uniquely identifying the cloud masking process used to produce the image. |




### Terms of Use


**Terms of Use**


This dataset is licensed under
[CC\-BY 4\.0](https://creativecommons.org/licenses/by/4.0/) and requires the
following attribution: "This dataset is produced for the Dynamic World
Project by Google in partnership with National Geographic Society and the
World Resources Institute."


Contains modified Copernicus Sentinel data \[2015\-present].
See the [Sentinel Data Legal Notice](https://sentinels.copernicus.eu/documents/247904/690755/Sentinel_Data_Legal_Notice).




### Citations



Citations:
* Brown, C.F., Brumby, S.P., Guzder\-Williams, B. et al. Dynamic World, Near
real\-time global 10 m land use land cover mapping. Sci Data 9, 251 (2022\).
[doi:10\.1038/s41597\-022\-01307\-4](https://doi.org/10.1038/s41597-022-01307-4)





### DOIs


* [https://doi.org/10\.1038/s41597\-022\-01307\-4](https://doi.org/10.1038/s41597-022-01307-4)




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
// Construct a collection of corresponding Dynamic World and Sentinel-2 for
// inspection. Filter by region and date.
varSTART=ee.Date('2021-04-02');
varEND=START.advance(1,'day');

varcolFilter=ee.Filter.and(
ee.Filter.bounds(ee.Geometry.Point(20.6729,52.4305)),
ee.Filter.date(START,END));

vardwCol=ee.ImageCollection('GOOGLE/DYNAMICWORLD/V1').filter(colFilter);
vars2Col=ee.ImageCollection('COPERNICUS/S2_HARMONIZED');

// Link DW and S2 source images.
varlinkedCol=dwCol.linkCollection(s2Col,s2Col.first().bandNames());

// Get example DW image with linked S2 image.
varlinkedImg=ee.Image(linkedCol.first());

// Create a visualization that blends DW class label with probability.
// Define list pairs of DW LULC label and color.
varCLASS_NAMES=[
'water','trees','grass','flooded_vegetation','crops',
'shrub_and_scrub','built','bare','snow_and_ice'];

varVIS_PALETTE=[
'419bdf','397d49','88b053','7a87c6','e49635','dfc35a','c4281b',
'a59b8f','b39fe1'];

// Create an RGB image of the label (most likely class) on [0, 1].
vardwRgb=linkedImg
.select('label')
.visualize({min:0,max:8,palette:VIS_PALETTE})
.divide(255);

// Get the most likely class probability.
vartop1Prob=linkedImg.select(CLASS_NAMES).reduce(ee.Reducer.max());

// Create a hillshade of the most likely class probability on [0, 1];
vartop1ProbHillshade=
ee.Terrain.hillshade(top1Prob.multiply(100))
.divide(255);

// Combine the RGB image with the hillshade.
vardwRgbHillshade=dwRgb.multiply(top1ProbHillshade);

// Display the Dynamic World visualization with the source Sentinel-2 image.
Map.setCenter(20.6729,52.4305,12);
Map.addLayer(
linkedImg,{min:0,max:3000,bands:['B4','B3','B2']},'Sentinel-2 L1C');
Map.addLayer(
dwRgbHillshade,{min:0,max:0.65},'Dynamic World V1 - label hillshade');
```




Python setup


See the [Python Environment](/earth-engine/guides/python_install) page for information on the Python API and using
 `geemap` for interactive development.



```
importee
importgeemap.coreasgeemap
```


### Colab (Python)



```
# Construct a collection of corresponding Dynamic World and Sentinel-2 for
# inspection. Filter by region and date.
START = ee.Date('2021-04-02')
END = START.advance(1, 'day')

col_filter = ee.Filter.And(
    ee.Filter.bounds(ee.Geometry.Point(20.6729, 52.4305)),
    ee.Filter.date(START, END),
)

dw_col = ee.ImageCollection('GOOGLE/DYNAMICWORLD/V1').filter(col_filter)
s2_col = ee.ImageCollection('COPERNICUS/S2_HARMONIZED');

# Link DW and S2 source images.
linked_col = dw_col.linkCollection(s2_col, s2_col.first().bandNames());

# Get example DW image with linked S2 image.
linked_image = ee.Image(linked_col.first())

# Create a visualization that blends DW class label with probability.
# Define list pairs of DW LULC label and color.
CLASS_NAMES = [
    'water',
    'trees',
    'grass',
    'flooded_vegetation',
    'crops',
    'shrub_and_scrub',
    'built',
    'bare',
    'snow_and_ice',
]

VIS_PALETTE = [
    '419bdf',
    '397d49',
    '88b053',
    '7a87c6',
    'e49635',
    'dfc35a',
    'c4281b',
    'a59b8f',
    'b39fe1',
]

# Create an RGB image of the label (most likely class) on [0, 1].
dw_rgb = (
    linked_image.select('label')
    .visualize(min=0, max=8, palette=VIS_PALETTE)
    .divide(255)
)

# Get the most likely class probability.
top1_prob = linked_image.select(CLASS_NAMES).reduce(ee.Reducer.max())

# Create a hillshade of the most likely class probability on [0, 1]
top1_prob_hillshade = ee.Terrain.hillshade(top1_prob.multiply(100)).divide(255)

# Combine the RGB image with the hillshade.
dw_rgb_hillshade = dw_rgb.multiply(top1_prob_hillshade)

# Display the Dynamic World visualization with the source Sentinel-2 image.
m = geemap.Map()
m.set_center(20.6729, 52.4305, 12)
m.add_layer(
    linked_image,
    {'min': 0, 'max': 3000, 'bands': ['B4', 'B3', 'B2']},
    'Sentinel-2 L1C',
)
m.add_layer(
    dw_rgb_hillshade,
    {'min': 0, 'max': 0.65},
    'Dynamic World V1 - label hillshade',
)
m
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/GOOGLE/GOOGLE_DYNAMICWORLD_V1)


[Dynamic World V1](/earth-engine/datasets/catalog/GOOGLE_DYNAMICWORLD_V1)

Dynamic World is a 10m near\-real\-time (NRT) Land Use/Land Cover (LULC) dataset that includes class probabilities and label information for nine classes. Dynamic World predictions are available for the Sentinel\-2 L1C collection from 2015\-06\-27 to present. The revisit frequency of Sentinel\-2 is between 2\-5 days depending on latitude. Dynamic World …

 GOOGLE/DYNAMICWORLD/V1,
 global,google,landcover,landuse,landuse\-landcover,nrt,sentinel2\-derived

2015\-06\-27T00:00:00Z/2025\-07\-19T03:39:26\.559000Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets

* [https://doi.org/10\.1038/s41597\-022\-01307\-4](https://doi.org/https://www.wri.org/)
* [https://doi.org/10\.1038/s41597\-022\-01307\-4](https://doi.org/https://research.google.com/)
* [https://doi.org/10\.1038/s41597\-022\-01307\-4](https://doi.org/https://developers.google.com/earth-engine/datasets/catalog/GOOGLE_DYNAMICWORLD_V1)









