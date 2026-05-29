---
name: thermal_heat_skills
version: 1.0.0
description: Compact reference for generic thermal remote sensing and urban heat studies in Google Earth Engine. It provides reusable building blocks for LST processing, QA masking, temperature conversion, contextual indices, spatial summaries, and basic interpretation checks. It avoids task-specific recipes and is intended to support code generation for heat-related Earth Observation workflows.
metadata:
  category: remote-sensing
  topics:
    - land-surface-temperature
    - lst
    - thermal-remote-sensing
    - urban-heat
    - surface-urban-heat-island
    - landsat
    - modis
    - sentinel-2
    - google-earth-engine
---

# Thermal Heat Remote Sensing Skills

## **Land Surface Temperature (LST)**

### 1. Overview

**Land Surface Temperature (LST)** describes the radiative “skin” temperature of the land surface. It is widely used in urban heat studies to analyze surface heating patterns, compare land-cover types, and support heat-related indicators.

LST is not the same as near-surface air temperature. LST responds strongly to surface materials, vegetation, moisture, radiation, and observation time.

**Goal:** analyze surface thermal behavior  
**Common products:** Landsat Collection 2 Level-2, MODIS LST  
**Common output unit:** Celsius  
**Required preprocessing:** QA masking, scale/offset conversion, temporal filtering

### 2. Basic conversion

$$
LST_{^\circ C}=LST_K-273.15
$$

---

## **Landsat Collection 2 Level-2 LST**

### 1. Overview

Landsat 8/9 Collection 2 Level-2 is commonly used for urban thermal analysis because it provides both surface reflectance and surface temperature bands.

**Dataset IDs:**
```javascript
var l8 = ee.ImageCollection('LANDSAT/LC08/C02/T1_L2');
var l9 = ee.ImageCollection('LANDSAT/LC09/C02/T1_L2');
```

**Useful bands:**

- `ST_B10`: surface temperature
- `SR_B4`: red
- `SR_B5`: near infrared
- `SR_B6`: SWIR1
- `QA_PIXEL`: quality mask

### 2. LST scale and conversion

$$
LST_K = DN \times 0.00341802 + 149.0
$$

```javascript
function addLSTCelsius(img) {
  var lstC = img.select('ST_B10')
    .multiply(0.00341802)
    .add(149.0)
    .subtract(273.15)
    .rename('LST_C');

  return img.addBands(lstC);
}
```

### 3. QA mask

```javascript
function maskLandsatL2(img) {
  var qa = img.select('QA_PIXEL');

  var dilatedCloud = 1 << 1;
  var cirrus = 1 << 2;
  var cloud = 1 << 3;
  var cloudShadow = 1 << 4;
  var snow = 1 << 5;

  var mask = qa.bitwiseAnd(dilatedCloud).eq(0)
    .and(qa.bitwiseAnd(cirrus).eq(0))
    .and(qa.bitwiseAnd(cloud).eq(0))
    .and(qa.bitwiseAnd(cloudShadow).eq(0))
    .and(qa.bitwiseAnd(snow).eq(0));

  return img.updateMask(mask).copyProperties(img, img.propertyNames());
}
```

### 4. Collection preparation

```javascript
var landsat = l8.merge(l9)
  .filterBounds(geometry)
  .filterDate('2023-06-01', '2023-08-31')
  .map(maskLandsatL2)
  .map(addLSTCelsius)
  .select('LST_C');
```

---

## **MODIS LST**

### 1. Overview

MODIS LST is useful for broader-scale and time-series heat studies. It has coarser spatial resolution than Landsat but higher temporal frequency.

**Dataset examples:**
```javascript
var modisTerra = ee.ImageCollection('MODIS/061/MOD11A2');
var modisAqua = ee.ImageCollection('MODIS/061/MYD11A2');
```

**Useful bands:**

- `LST_Day_1km`
- `LST_Night_1km`
- `QC_Day`
- `QC_Night`

### 2. Scale and conversion

$$
LST_K = DN \times 0.02
$$

```javascript
function modisDayLSTC(img) {
  return img.select('LST_Day_1km')
    .multiply(0.02)
    .subtract(273.15)
    .rename('LST_Day_C')
    .copyProperties(img, img.propertyNames());
}
```

### 3. Collection preparation

```javascript
var modisLST = ee.ImageCollection('MODIS/061/MOD11A2')
  .filterBounds(geometry)
  .filterDate('2023-06-01', '2023-08-31')
  .map(modisDayLSTC);
```

---

# Contextual Indices for Heat Studies

## **NDVI**

### 1. Overview

**NDVI** describes vegetation presence and vigor. In heat studies, it is often used to interpret LST patterns because vegetated areas tend to be cooler than impervious surfaces.

$$
NDVI = \frac{NIR - Red}{NIR + Red}
$$

### 2. Sentinel-2 snippet

```javascript
var ndvi = img.normalizedDifference(['B8', 'B4']).rename('NDVI');
```

### 3. Landsat L2 snippet

```javascript
function addLandsatNDVI(img) {
  var red = img.select('SR_B4').multiply(0.0000275).add(-0.2);
  var nir = img.select('SR_B5').multiply(0.0000275).add(-0.2);

  var ndvi = nir.subtract(red).divide(nir.add(red)).rename('NDVI');
  return img.addBands(ndvi);
}
```

---

## **NDWI / Moisture Context**

### 1. Overview

NDWI has multiple formulations. For heat studies, it is mainly used either to identify water bodies or to provide a moisture-related context.

### 2. Open-water NDWI

$$
NDWI = \frac{Green - NIR}{Green + NIR}
$$

```javascript
var ndwiWater = img.normalizedDifference(['B3', 'B8']).rename('NDWI_water');
```

### 3. Moisture-sensitive NDWI / NDMI

$$
NDWI_{moisture} = \frac{NIR - SWIR}{NIR + SWIR}
$$

```javascript
var ndwiMoisture = img.normalizedDifference(['B8', 'B11']).rename('NDWI_moisture');
```

---

# Generic Thermal Building Blocks

## **Filter by Date and AOI**

```javascript
var filtered = imageCollection
  .filterBounds(geometry)
  .filterDate('2023-06-01', '2023-08-31');
```

## **Check Collection Size**

```javascript
print('Collection size:', imageCollection.size());
```

## **Mean Composite**

```javascript
var meanImage = imageCollection.mean().clip(geometry);
```

## **Median Composite**

```javascript
var medianImage = imageCollection.median().clip(geometry);
```

## **Percentile Composite**

```javascript
var p90 = imageCollection.reduce(ee.Reducer.percentile([90]));
```

## **Map Visualization**

```javascript
Map.centerObject(geometry, 11);

Map.addLayer(
  lstImage,
  {min: 20, max: 45, palette: ['blue', 'cyan', 'yellow', 'orange', 'red']},
  'LST Celsius'
);
```

## **Mean Value over AOI**

```javascript
var meanValue = image.reduceRegion({
  reducer: ee.Reducer.mean(),
  geometry: geometry,
  scale: 30,
  maxPixels: 1e8
});

print('Mean value:', meanValue);
```

## **Zonal Statistics**

```javascript
var zonal = image.reduceRegions({
  collection: zones,
  reducer: ee.Reducer.mean(),
  scale: 30
});

print(zonal.limit(10));
```

## **Export Image**

```javascript
Export.image.toDrive({
  image: image,
  description: 'thermal_image_export',
  region: geometry,
  scale: 30,
  maxPixels: 1e8
});
```

## **Export Table**

```javascript
Export.table.toDrive({
  collection: zonal,
  description: 'thermal_zonal_statistics',
  fileFormat: 'CSV'
});
```

---

# Simple Masks for Heat Studies

## **Water Mask**

```javascript
var worldCover = ee.ImageCollection('ESA/WorldCover/v200').first().select('Map');
var water = worldCover.eq(80);
```

## **Land Mask**

```javascript
var land = water.not();
var landOnlyImage = image.updateMask(land);
```

## **Built-up Mask**

```javascript
var worldCover = ee.ImageCollection('ESA/WorldCover/v200').first().select('Map');
var builtUp = worldCover.eq(50);
```

## **Vegetation Mask**

```javascript
var worldCover = ee.ImageCollection('ESA/WorldCover/v200').first().select('Map');

var vegetation = worldCover.eq(10)  // trees
  .or(worldCover.eq(20))            // shrubland
  .or(worldCover.eq(30))            // grassland
  .or(worldCover.eq(40));           // cropland
```

---

# Generic Thermal Indicators

## **Temperature Difference**

```javascript
var difference = imageA.subtract(imageB).rename('temperature_difference');
```

## **Pixel Threshold**

```javascript
var hotPixels = lstImage.gt(40).rename('hot_pixels');
Map.addLayer(hotPixels.selfMask(), {palette: ['red']}, 'Hot pixels');
```

## **Percentile Threshold**

```javascript
var p90 = ee.Number(
  lstImage.reduceRegion({
    reducer: ee.Reducer.percentile([90]),
    geometry: geometry,
    scale: 30,
    maxPixels: 1e8
  }).get('LST_C_p90')
);

var highLST = lstImage.gte(p90).rename('high_LST');
```

## **Anomaly**

```javascript
var anomaly = targetImage.subtract(baselineImage).rename('LST_anomaly_C');
```

## **Area of a Binary Mask**

```javascript
var pixelArea = ee.Image.pixelArea();

var area = binaryMask.multiply(pixelArea).reduceRegion({
  reducer: ee.Reducer.sum(),
  geometry: geometry,
  scale: 30,
  maxPixels: 1e8
});

print('Area in square meters:', area);
```

---

# Important Methodological Notes

- Apply QA masks before compositing.
- Convert scaled digital numbers into physical units before interpretation.
- Report the dataset ID, date range, temporal aggregation method, scale, and unit.
- Do not use Sentinel-2 to directly calculate LST.
- Do not mix daytime and nighttime LST unless the analysis explicitly requires it.
- Use scale values appropriate to the product, e.g. around 30 m for Landsat and around 1000 m for MODIS.
- Exclude water pixels when they would distort land-focused urban heat summaries.
- Interpret LST as surface temperature, not air temperature or direct human heat exposure.

---

# Common AI Code Generation Mistakes

## **Using raw `ST_B10` values**

Incorrect:
```javascript
var lst = img.select('ST_B10');
```

Correct:
```javascript
var lst = img.select('ST_B10')
  .multiply(0.00341802)
  .add(149.0)
  .subtract(273.15)
  .rename('LST_C');
```

## **Using Sentinel-2 as a thermal sensor**

Sentinel-2 has no thermal infrared band. Use it for NDVI, NDWI, moisture, and land-cover context, not direct LST.

## **Wrong reducer scale**

Avoid using 10 m for MODIS LST or 1000 m for fine Landsat summaries unless the choice is intentional and explained.

## **Masking after compositing**

Incorrect:
```javascript
var composite = collection.mean();
var masked = composite.updateMask(mask);
```

Better:
```javascript
var composite = collection.map(maskFunction).mean();
```

## **Unclear NDWI formulation**

Always name whether NDWI means open-water NDWI or moisture-sensitive NDWI/NDMI.

---

# Documentation Targets

Use authoritative documentation when grounding outputs:

- Google Earth Engine Data Catalog: Landsat Collection 2 Level-2
- Google Earth Engine Data Catalog: MODIS MOD11A2 / MYD11A2
- Google Earth Engine Data Catalog: Sentinel-2 Surface Reflectance Harmonized
- Google Earth Engine Data Catalog: ESA WorldCover
- Landsat Collection 2 Level-2 Science Product Guide
- MODIS LST product documentation

---
