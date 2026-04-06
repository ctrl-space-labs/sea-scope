---
name: spectral_indices_skills
version: 2.0.0
description: Reference for Sentinel remote sensing indices, marine monitoring methods, and Google Earth Engine snippets. It contains practical guidance for Earth observation workflows in Google Earth Engine, focused on Sentinel-1, Sentinel-2, and Sentinel-5P data. It documents spectral indices such as NDWI, NDTI, NDVI, and FDI, along with methodology, detection logic, limitations, and ready-to-use code snippets for applications including water quality, turbidity, oil spills, ship detection, macroplastics, and air quality near ports.
metadata:
  category: remote-sensing
  topics:
    - ndwi
    - ndti
    - fdi
    - sentinel-1
    - sentinel-2
    - sentinel-5p
    - google-earth-engine
    - marine-monitoring
---

# Spectral Indices

## **Normalized Difference Water Index (NDWI)**

### 1. Overview

**Normalized Difference Water Index (NDWI)** is a spectral index used to enhance and delineate open water features in satellite imagery.

It is computed from the green and near-infrared (NIR) bands, leveraging the strong absorption of water in the NIR portion of the spectrum and its relatively higher reflectance in the green wavelengths.

NDWI values range from −1 to +1, where positive values are typically associated with open water, while values near zero or negative are generally associated with vegetation, soil, or built-up surfaces.

**Goal:** Highlight open water in satellite imagery  
**Sensor:** Sentinel-2 (10 m)  
**Bands:** Green (B3), NIR (B8)  
**Formula:** NDWI = (Green - NIR) / (Green + NIR)  
**Range & interpretation:** [-1, 1], positive often water.  
**Required preprocessing:** Cloud mask, Water mask

### 2. Equation

$$
\mathrm{NDWI}=\frac{Green-NIR}{Green+NIR}
$$
<br>

### 3. Google Earth Engine Example

```javascript
// Computing NDWI from Sentinel-2

var ndwi = ee.ImageCollection("COPERNICUS/S2_SR_HARMONIZED")
   .normalizedDifference(['B3', 'B8'])
   .rename('NDWI');
```

---

## **Normalized Difference Turbidity Index (NDTI)**

### 1. Overview

**Normalized Difference Turbidity Index (NDTI)** is a spectral index used to estimate relative water turbidity in satellite imagery.  

It is computed from the red and green bands, exploiting the increased reflectance in the red wavelengths that is commonly associated with suspended sediments and turbid waters.  

NDTI values range from −1 to +1, where lower values generally correspond to clearer water conditions, while higher values typically indicate increased turbidity.

**Goal:** estimate water turbidity in satellite imagery  
**Sensor:** Sentinel-2 (10 m)  
**Bands:** Green (B3), Red (B4)  
**Formula:** NDTI = (Red - Green) / (Red + Green)  
**Range & interpretation:** [-1, 1], positive often turbid water  
**Required preprocessing:** Cloud mask, Water mask

### 2. Equation

$$
\mathrm{NDTI}=\frac{Red-Green}{Red+Green}
$$
<br>


### 3. Google Earth Engine Example

```javascript
// Computing NDTI from Sentinel-2

var ndti = ee.ImageCollection("COPERNICUS/S2_SR_HARMONIZED")
   .normalizedDifference(['B4', 'B3'])
   .rename('NDTI');
```

### 4. Notes

**Water Turbidity** represents water clarity by describing the cloudiness or haziness caused by suspended particles such as silt, clay, algae, plankton, organic matter, and microorganisms. In Google Earth Engine (GEE), turbidity can be estimated using Sentinel-2 surface reflectance (SR) imagery.

In addition to NDTI, the Sentinel-2 red band (B4) reflectance provides complementary information for turbidity assessment. Elevated concentrations of suspended particles typically increase water-leaving reflectance in the red spectral region. Therefore, B4 alone may serve as a practical turbidity proxy in situations where index-based metrics are affected by masking limitations, low signal levels, or band-ratio instabilities.

---

## **Floating Debris Index (FDI)**

### 1. Overview

**Floating Debris Index (FDI)** is a spectral index designed to enhance the detection of floating material at the water surface, such as macroplastics, seaweed, sea foam or spume and wood, in Sentinel-2 imagery.  

It exploits the strong absorption of deep, optically clear water in the NIR–SWIR region, while floating targets typically exhibit elevated NIR reflectance relative to a baseline spectral continuum. Consequently, FDI is particularly suited for identifying floating materials, including sub-pixel signals under favorable conditions.  

Individual pieces of marine litter generally remain below detection limits until oceanic features such as fronts, eddies, or other submesoscale processes aggregate multiple items into larger patches. 

In marine environments, natural and anthropogenic materials often co-occur, forming mixed debris accumulations that may include both organic matter and macroplastics. Once aggregated into sufficiently large and coherent patches, detection using Sentinel-2 imagery becomes feasible.

#### FDI values

FDI values typically range between 0 and 0.1.  

<u>Slightly negative values:</u> may occur due to sensor noise or atmospheric and illumination–viewing geometry effects.  
<u>Low values (≈0):</u> generally correspond to clean water or water-dominated pixels, where the NIR signal does not deviate from the expected background continuum.  
<u>High (positive) values:</u> indicate that NIR reflectance exceeds the baseline continuum level, consistent with the presence of floating or near-surface material that enhances NIR backscatter or reflectance.

Typical ranges include:

Seawater: ~0.000 to ~0.01  
Plastics: ~0.02 to ~0.05  
Sea foam: ~0.03 to ~0.06  
Timber: ~0.03 to ~0.10  
Seaweed: ~0.04 to ~0.09  


### 2. Equation

$$
\begin{array}{lll}FDI & = & {R}_{rs,NIR}-{{R}^{{\prime} }}_{rs,NIR}\\ {{R}^{{\prime} }}_{rs,NIR} & = & {R}_{rs,RE2}+({R}_{rs,SWIR1}-{R}_{rs,RE2})\times \frac{({\lambda }_{NIR}-{\lambda }_{RED})}{({\lambda }_{SWIR1}-{\lambda }_{RED})}\times 10\end{array}
$$


### 3. Google Earth Engine Example
```javascript
function addFDI(img) {
  var RED = img.select('B4');
  var RE2 = img.select('B6');
  var NIR = img.select('B8');
  var SWIR1 = img.select('B11');

  var lambdaRED = 665;
  var lambdaNIR = 833;
  var lambdaSWIR1 = 1610;

  var ratio = ((lambdaNIR - lambdaRED) / (lambdaSWIR1 - lambdaRED)) * 10;
  var nirPrime = RE2.add(SWIR1.subtract(RE2).multiply(ratio));

  var fdi = NIR.subtract(nirPrime).rename('FDI');
  return img.addBands(fdi);
}
```

### 4. Notes

FDI response is largely controlled by sub-pixel fractional cover. Increasing areal coverage of floating material within a pixel generally produces progressively higher FDI values.

A key limitation is that FDI is not uniquely diagnostic of plastics. Elevated values may arise from various floating targets, such as seaweed, foam, or driftwood, that enhance NIR reflectance above the background continuum. 

For this reason, FDI is commonly combined with NDVI and additional spectral features when necessary to improve class discrimination, particularly between vegetation-like and non-vegetated floating debris. 
<br><br>

# Methodology and Key points
## **Sentinel-1**
**Methodology:**
Initially, an Image Collection is selected and subsequently filtered by the area of interest and the acquisition dates. From Sentinel-1, the Interferometric Wide swath (IW) acquisition mode is selected, as it is the most commonly used mode over land and coastal/marine environments. IW provides broad spatial coverage (swath width of approximately 250 km) while maintaining an adequate spatial resolution (about 10 m for GRD products available in Google Earth Engine). In addition, the analysis is restricted to VV polarization (transmitterReceiverPolarisation = VV), meaning that the radar transmits and receives in vertical polarization. Over the ocean surface, VV backscatter is typically stronger and more stable than alternative channels, which makes it a frequent choice for detecting dark slick-like features associated with oil contamination. Finally, the orbitProperties_pass filter (ascending vs. descending) is applied. While neither pass direction is inherently superior, it is important to use a consistent viewing geometry within each case study, since differences in acquisition geometry (incidence angle and look direction) can affect backscatter levels and, consequently, the comparability of results.

## **Sentinel-2**
**Methodology:**
For each case study a cloud mask is first applied to retain the clearest possible observations and minimize cloud-related noise. The Image Collection is then filtered to the area of interest and a selected time period, and a median composite is generated to reduce residual clouds and limit data gaps arising from masked pixels.

## **Oil spills**
**Methodology:**
For oil-spill detection, Sentinel-1 SAR imagery is used following the same general workflow (i.e., selection of an appropriate Image Collection and filtering by the study area and acquisition dates). The core detection logic relies on the well-established observation that oil spills often appear as dark regions in SAR (Synthetic Aperture Radar) imagery relative to the surrounding sea surface, due to reduced radar backscatter. Therefore, a simple thresholding approach is employed, flagging pixels with very low backscatter as potential oil-spill candidates (e.g., σ⁰(VV) < −25 dB). In addition, the mean near-surface wind speed over the study region can be estimated from ERA-5 reanalysis data to help interpret whether observed dark features might be attributable to natural slicks or wind-related damping effects, rather than anthropogenic oil pollution.

**Key points:**
- Calm wind conditions hinder oil-spill detection. When near-calm winds prevail over the area of interest, the sea surface appears uniformly dark in Sentinel-1 SAR imagery, reducing contrast between an oil spill and the surrounding water. This is a key limitation in the Cyprus cases, where wind speeds are frequently low.

- High winds also reduce detectability. Under strong wind conditions, increased surface roughness and enhanced vertical mixing promote dispersion and partial submergence of oil within the water column. This decreases the extent of the surface slick and weakens its SAR signature.

- Event frequency and oil spill size affect observability. Oil-spill incidents around Cyprus are relatively infrequent and, when they occur, they are often small. If Sentinel-1 does not acquire imagery on the same day, cleanup operations by the competent authorities may remove a substantial fraction of the surface residues before the next satellite overpass, further limiting detectability.

- Optimal detection conditions are moderate winds and proximity to the oil-spill source. The most favorable wind regime for SAR-based oil-slick detection is typically 3–10 m s⁻¹, which provides sufficient sea-surface roughness for contrast while allowing oil to maintain a coherent surface film. Detection is further strengthened when the slick is observed near a plausible source, particularly if a bright point target consistent with a ship is visible at one end of the feature.

- Complementary optical imagery can support nearshore interpretation. In coastal waters, Sentinel-2 RGB composites may provide useful corroboration, as the dark coloration of oil can sometimes be distinguishable against the lighter blue tones of shallow coastal waters—an advantage that is generally absent over the open ocean.

- Look-alikes remain a major source of false positives. Several oceanographic and environmental phenomena can produce slick-like dark signatures, including natural slicks, newly formed sea ice, low-wind patches, internal waves, upwelling features, and algal blooms. These confounders highlight the need for contextual information (e.g., wind fields) and, where possible, multi-sensor validation.

## **Ship detection**
**Methodology:** 
For ship detection, Sentinel-1 SAR imagery is used following the same general workflow (i.e., selection of an appropriate ImageCollection and filtering by the study area and acquisition dates). The key difference is that ships typically appear as bright targets in SAR images relative to the surrounding sea surface, due to strong radar backscatter from metallic structures and angular surfaces. Accordingly, a simple intensity threshold is applied, flagging pixels with backscatter values greater than −5 dB as potential ship candidates. In addition, a water mask is incorporated to restrict the analysis to marine areas located more than 100 m from the coastline. This offshore constraint helps mitigate coastal-zone effects and reduces spurious detections and noise in the ship-detection results.

**Key points:**
- Limited revisit time constrains detectability. If a ship remains in the area only briefly, whether it is captured by Sentinel-1 is largely dependent on acquisition timing, given the satellite’s finite revisit frequency.

- SAR detections alone cannot confirm illegal fishing. Verification typically requires complementary ship-tracking information (e.g., AIS/MarineTraffic or equivalent sources) to assess ship identity, activity patterns, and compliance with regulations.

## **Water Quality and Turbidity**
**Methodology:** 
For turbidity detection, Sentinel-2 optical imagery is used following the same general workflow (i.e., selection of an appropriate ImageCollection and filtering by the study area and acquisition dates). Subsequently, the Normalized Difference Water Index (NDWI) and the Normalized Difference Turbidity Index (NDTI) are computed. In addition to the NDTI, Sentinel-2 Band 4 (red reflectance) can be used as a complementary proxy for turbidity.

**Key points:**
- Shallow-water bottom effects can bias turbidity estimates. In clear but shallow waters, reflectance from sandy or rocky substrates can artificially increase the signal, causing indices such as NDTI to indicate elevated turbidity even when the water column is not turbid.

- Coastal mixed pixels can inflate red reflectance. Nearshore pixels that include both land and water (land–water adjacency/mixed-pixel effect) may increase Sentinel-2 Band 4 (red) reflectance and lead to false turbidity indications in otherwise clear waters.

- Residual cloud contamination may persist. Even with cloud masking, thin clouds, haze, or cloud-edge artefacts can remain in the composite and introduce spurious signals, potentially degrading turbidity retrievals and index reliability.

## **Macroplastics detection**
**Methodology:** 
For plastic detection, Sentinel-2 optical imagery is used following the same general workflow (i.e., selection of an appropriate ImageCollection and filtering by the study area and acquisition dates). Floating debris is then assessed using the Floating Debris Index (FDI), which is designed to enhance the spectral signature of floating materials at the sea surface, including potential macroplastic accumulations. In practice, FDI is commonly combined with the Normalized Difference Vegetation Index (NDVI) to better discriminate plastics from natural floating matter (e.g., seaweed, driftwood). Candidate plastic targets are identified using empirical ranges: NDVI > 0 and NDVI < 0.3, together with FDI > 0.01 and FDI < 0.07, which aim to exclude dense vegetation-like signals while retaining moderate positive FDI responses consistent with floating debris.

**Key points:**
- FDI is not uniquely diagnostic of plastics. Elevated FDI values may arise from a range of floating targets—such as seaweed and other floating vegetation, foam, driftwood, or mixed debris—because these features can increase NIR reflectance relative to the surrounding water “background continuum”. For this reason, FDI is commonly used in combination with NDVI to reduce ambiguity.

- Independent validation is often required. In many cases, it is not possible to confirm with certainty whether a detected target corresponds to floating plastic or a ship. Therefore, ancillary information (e.g., AIS/MarineTraffic or equivalent ship-tracking datasets) can be valuable for screening ship-related detections and improving interpretation.

## **Air quality near ports**
**Methodology:** 
For air quality near ports, satellite observations from Sentinel-5P are used. The spatial distribution of the NO₂ vertical column density (VCD) is then mapped, as this quantity is commonly used as an indicator of atmospheric NO₂ loading and can be linked to combustion-related emissions, including ship exhaust in the vicinity of major ports. Interpretation depends on meteorological conditions and data resolution.
<br><br>

# GEE Code Snippets and Info
## **Filter ImageCollection by Date**
**Code Snippet:**
```javascript
var Sentinel2_date = Sentinel2.filterDate("2019-01-01", "2019-01-20"); //.filterDate(start, end)
```

## **Filter ImageCollection by Geographic Location**
**Code Snippet:**
```javascript
var Sentinel2_loc = Sentinel2.filterBounds(geometry);
```

## **Sort ImageCollection by Cloud Cover and Select the Most Cloud Free Image**
**Code Snippet:**
```javascript
var Sentinel2_cloud = Sentinel2.sort("CLOUD_COVERAGE_ASSESSMENT", true);
var Sentinel2_img = Sentinel2_cloud.first();
```


## **Clip to AOI**
**Use:** Restrict processing/visualization to the area of interest.

**Code Snippet:**
```javascript
// Clip a single image
var clippedImg = img.clip(geometry);

// Clip every image in a collection
var clippedCol = col.map(function(img){ return img.clip(geometry); });
```

## **Filter by metadata (general pattern)**
**Use:** Filter collections using any property (e.g., orbit pass).

**Code Snippet:**
```javascript
var filtered = col.filter(ee.Filter.eq('orbitProperties_pass', 'ASCENDING'));
```

## **Scale or convert bands (Sentinel-2 SR)**
**Use:** Convert integer SR bands to reflectance (0–1) consistently.

**Code Snippet:**
```javascript
var s2Scaled = s2.map(function(img){
  return img.divide(10000).copyProperties(img, img.propertyNames());
});
```

## **Zoom**
**Code Snippet:**
```javascript
Map.centerObject(variable, 9);
```

## **Get a Single Image from an ImageCollection**
**Use:**
- To take the first image in an ImageCollection, use .first(). It returns the first image in the collection (based on the collection’s current ordering) as an ee.Image.
- To compute the per-pixel mean across the collection, use .mean(). It averages values (sum divided by count) and smooths noise, but it can blur features. It is very sensitive to outliers (extreme values).
- To compute the per-pixel median across the collection, use .median(). It sorts the values and selects the middle one. It is robust to outliers, such as residual clouds.
- To merge images by taking, for each pixel, the first valid (unmasked) value in stack order, use .mosaic(). It can fill gaps using subsequent images, and the result depends on the collection order.

**Notes:**
The use of mosaic() in Sentinel-2 ImageCollections can be particularly useful after applying a cloud mask. Specifically, where an image is masked due to clouds, mosaic() selects the first available unmasked pixel value from the remaining images in the collection, thereby filling data gaps with observations from other acquisition dates. However, the output is effectively a composite that may merge information from different days and different satellite overpasses. Consequently, the resulting pixels can originate from different observation times—potentially under varying illumination, atmospheric conditions, viewing geometry, and surface state—which may introduce visual discontinuities or spatial “inhomogeneities” in the final image. This effect can be especially apparent in dynamic environments such as coastal zones.

**Code Snippet:**
```javascript
var image = imageCollection.first()
var image1 = imageCollection1.median()
var image2 = imageCollection2.mosaic()
var image3 = imageCollection3.mean()
```

## **Cloud Mask**
**Use:** The cloud mask is applied to remove cloud contaminated pixels, ensuring that subsequent analysis is based on clear-sky observations and reducing cloud-related noise in derived products.

**Code Snippet:**
```javascript
// Applying a Cloud Mask to Sentinel-2
function maskS2clouds(image) {
  var qa = image.select('QA60');

  // Bits 10 and 11 are clouds and cirrus, respectively.
  var cloudBitMask = 1 << 10;
  var cirrusBitMask = 1 << 11;

  // Both flags should be set to zero, indicating clear conditions.
  var mask = qa.bitwiseAnd(cloudBitMask).eq(0)
      .and(qa.bitwiseAnd(cirrusBitMask).eq(0));

  return image.updateMask(mask).divide(10000);
}

var dataset = ee.ImageCollection('COPERNICUS/S2_SR_HARMONIZED')
                  .filter(ee.Filter.lt('CLOUDY_PIXEL_PERCENTAGE',10)) // Pre-filter to get less cloudy granules.
                  .map(maskS2clouds);
```

## **Water mask**
**Use:** The water mask is used to retain only water pixels and optionally ocean-like no-data so that all subsequent processing is restricted to permanent water areas.

**Code Snippet:**
```javascript
var worldCover = ee.ImageCollection('ESA/WorldCover/v200').first().select('Map');

var worldCover0 = worldCover.unmask(0);  // Replace masked/no-data pixels with value 0
var permanentWater = worldCover0.eq(80);          
var openOcean = worldCover0.eq(0);       // Pixels that were originally masked/no-data (treated here as open ocean)
var waterMask = permanentWater.or(openOcean);

//Add Layer
Map.addLayer(waterMask.selfMask().clip(geometry), {palette:['0000ff']}, 'Water');
```

## **Land mask**
**Use:** The land mask is used to retain only land pixels (excluding permanent water and ocean-like no-data) so that all subsequent processing is restricted to terrestrial areas. 

**Notes:** It can be used after creating the water mask variable.

**Code Snippet:**
```javascript
var land = waterMask.not().selfMask();

//Add Layer
Map.addLayer(land.selfMask().clip(geometry), {palette:['61f527']}, 'Land');
```

## **Apply a Mask to Every Image in an ImageCollection**
**Use:** Apply the same pixel mask (e.g., water mask, land mask, cloud mask) to every image in an ImageCollection, so all downstream steps operate only on valid pixels.

**Code Snippet:**
```javascript
var s1 = s1.map(function(img) {
   return img.updateMask(waterMask);
});
```

## **Apply a Mask on a Single Image**
**Use:** Restrict an ee.Image to pixels that satisfy a condition (e.g., keep only water, keep only water). Masked pixels are ignored in visualization and reducers.

**Code Snippet:**
```javascript
var variable = variable.updateMask(waterMask)
```

## **Distance-from-land Mask**
**Use:** Refines a water mask by excluding pixels close to land. Computes the distance-to-land (meters) and keeps only water pixels farther than a given threshold (e.g., >100 m).

**Code Snippet:**
```javascript
var distToLand = land
   .fastDistanceTransform(500) // 500 px ≈ 5 km
   .sqrt()
   .multiply(10);              // meters

// Refine the water mask
var waterMask = waterMask.updateMask(
   distToLand.gt(100)  // keep pixels farther than 100 m from land
);
```

## **NDWI**
**Code Snippet:**
```javascript
// Computing NDWI from Sentinel-2

var ndwi = img.normalizedDifference(['B3', 'B8'])
   .rename('NDWI');
```

## **NDTI**
**Code Snippet:**
```javascript
// Computing NDTI from Sentinel-2

var ndti = img.normalizedDifference(['B4', 'B3'])
   .rename('NDTI');
   ```

## **NDVI**
**Code Snippet:**
```javascript
// Computing NDVI from Sentinel-2

var ndvi = img.normalizedDifference(['B8','B4']).rename('NDVI');
```

## **FDI**
**Code Snippet:**
```javascript
function addFDI(img) {
  var RED = img.select('B4');
  var RE2 = img.select('B6');
  var NIR = img.select('B8');
  var SWIR1 = img.select('B11');

  var lambdaRED = 665;
  var lambdaNIR = 833;
  var lambdaSWIR1 = 1610;

  var ratio = ((lambdaNIR - lambdaRED) / (lambdaSWIR1 - lambdaRED)) * 10;
  var nirPrime = RE2.add(SWIR1.subtract(RE2).multiply(ratio));

  var fdi = NIR.subtract(nirPrime).rename('FDI');
  return img.addBands(fdi);
}
```

## **Selecting a Sentinel-1 image**
**Code Snippet:**
```javascript
var s1 = ee.ImageCollection('COPERNICUS/S1_GRD')
        .filter(ee.Filter.listContains('transmitterReceiverPolarisation', 'VV'))
        .filter(ee.Filter.eq('instrumentMode', 'IW'))
        .filterBounds(boundary)
        .filterDate('2019-01-06', '2019-01-07')
        .select('VV')
        .filter(ee.Filter.eq('orbitProperties_pass', 'DESCENDING'));
```

## **Ship detection**
**Use:** Higher dB values (closer to 0) appear brighter in radar imagery (e.g., ships).

**Notes:** The code snippet is used after selecting a Sentinel-1 image and creating water mask and distance-from-land mask.

**Code Snippet:**
```javascript
var thres = -5;
var ships = s1_img.gt(thres);
```

## **Oil spills**
**Use:** Lower dB values (closer to -25) appear darker in radar imagery (e.g., oil spills).

**Notes:** The code snippet is used after selecting a Sentinel-1 image and creating water mask and distance-from-land mask.

**Code Snippet:**
```javascript 
var thres = -25;
var oil_spill = img.lt(thres);
```

## **Plastics**
**Notes:** The code snippet is used after selecting a Sentinel-2 image, creating cloud mask and calculating NDVI and FDI.

**Code Snippet:**
```javascript
var ndvi = img.select('NDVI');
var fdi  = img.select('FDI');
var cond = ndvi.gte(0).and(ndvi.lte(0.3))
  .and(fdi.gte(0.01).and(fdi.lte(0.07)));

var redPixels = ee.Image(1).updateMask(cond);
Map.addLayer(redPixels, {palette: ['red']}, 'NDVI[0-0.3] & FDI[0.01-0.07]');
```

## **Air quality near ports**
**Code Snippet:**
```javascript
var NO2 = ee.ImageCollection("COPERNICUS/S5P/OFFL/L3_NO2")
   .select('tropospheric_NO2_column_number_density');
```

## **Image time**
**Use:** Retrieve the image acquisition timestamp in UTC for temporal filtering, synchronization with ancillary datasets (e.g., ERA5), and consistent time-based analysis.

**Code Snippet:**
```javascript
var tS1 = ee.Date(s1_img.get('system:time_start'));
```

## **Wind ERA5 hourly**
**Code Snippet:**
```javascript
var era5 = ee.ImageCollection('ECMWF/ERA5/HOURLY')
  .select(['u_component_of_wind_10m', 'v_component_of_wind_10m']);
```

## **Closest hour to the acquisition time**
**Code Snippet:**
```javascript
var eraNearest = ee.Image(
  era5.filterDate(tS1.advance(-3, 'hour'), tS1.advance(3, 'hour'))
      .map(function(img){
        var diff = ee.Number(img.get('system:time_start')).subtract(tS1.millis()).abs();
        return img.set('diff', diff);
      })
      .sort('diff')
      .first()
);
```

## **Wind speed**
**Code Snippet:**
```javascript
var u = img.select('u_component_of_wind_10m');
var v = img.select('v_component_of_wind_10m');
var ws = u.pow(2).add(v.pow(2)).sqrt().rename('ws');
```

## **Mean Wind Speed**
**Use:** Mean wind speed is computed in a region (e.g., from ERA5 near the satellite acquisition time) to characterize sea-state conditions and support interpretation of SAR dark features. Wind speed is computed as an additional check on detectability, since oil-spill signatures in SAR are less reliable under very low or very high wind conditions.

**Code Snippet:**
```javascript
var meanWs = ws.reduceRegion({
  reducer: ee.Reducer.mean(),
  geometry: geometry,
  scale: 30000,     // ERA5 ~ 31km
  maxPixels: 1e13
}).getNumber('ws');
```

<br><br>

#  References

- Lauren Biermann et al. (2020) - Finding Plastic Patches in Coastal Waters using Optical Satellite Data  

- Malin Johansson (2022) - Oil Spill Detection 

--- 