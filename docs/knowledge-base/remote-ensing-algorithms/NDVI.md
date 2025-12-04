# **Normalized Difference Vegetation Index (NDVI)**
*Knowledge Base Entry — Earth Observation Techniques*

## **1. Overview**
The **Normalized Difference Vegetation Index (NDVI)** is a spectral index used to quantify vegetation greenness, vigor, and overall plant health.  
It exploits the characteristic reflectance behavior of vegetation: **strong absorption in the red wavelengths** due to chlorophyll and **high reflectance in the near-infrared (NIR)** due to leaf cellular structure.

NDVI ranges between **–1 and +1**, where higher values indicate denser or healthier vegetation.

| NDVI Value | Interpretation |
|------------|----------------|
| < 0        | Water, snow, cloud, built-up features |
| 0–0.2      | Bare soil or sparse vegetation |
| 0.2–0.5    | Moderate vegetation |
| > 0.5      | Dense, healthy vegetation |

---

## **2. Equation**
\[
\text{NDVI} = \frac{\rho_\text{NIR} - \rho_\text{RED}}{\rho_\text{NIR} + \rho_\text{RED}}
\]

Where:
- **ρₙᵢᵣ** = reflectance in a **near-infrared band**
- **ρᵣₑ𝒹** = reflectance in a **red band**

---

## **3. Required Spectral Inputs**

NDVI requires **two spectral bands**:

### **Red Band**
- Wavelength range: **~0.63–0.69 μm**
- Vegetation strongly absorbs red light due to chlorophyll.
- High reflectance → low vegetation density.

### **Near-Infrared (NIR) Band**
- Wavelength range: **~0.76–0.90 μm**
- Vegetation reflects strongly due to internal leaf structure.
- Higher reflectance → healthier vegetation.

These bands are provided by most optical multispectral sensors.

---

## **4. Example Datasets Providing Required Bands**
Several EO datasets include the required **Red** and **NIR** bands and can be used for NDVI computation:

| Dataset | Red Band | NIR Band |
|---------|-----------|-----------|
| **Sentinel-2 MSI** | B4 (665 nm) | B8 (842 nm) |
| **Landsat 8/9 OLI** | B4 (Red) | B5 (NIR) |
| **Landsat 5/7** | B3 (Red) | B4 (NIR) |
| **MODIS** | B1 (Red) | B2 (NIR) |

### **Datasets with Precomputed NDVI**
Some datasets already provide NDVI as a ready-to-use band:

- **MODIS Vegetation Indices** (`MOD13Q1`, `MYD13A1`, etc.)
- **Sentinel-2 Level-2A (MOST platforms)** → NDVI is available through various derived collections (e.g., cloud-normalized)
- **Landsat Surface Reflectance Derived NDVI** (in several third-party collections)

Using precomputed NDVI can reduce processing time, but custom calculation offers flexibility and consistency across sensors.

---

## **5. Applications**
- Vegetation health & stress monitoring
- Crop growth assessment and agricultural decision support
- Deforestation & land-cover change detection
- Drought monitoring and seasonal trend analysis
- Providing vegetation masks for classification tasks
- Input to biomass, productivity, and carbon cycle models

---

## **6. Caveats & Considerations**

### **Atmospheric Effects**
- Use **surface reflectance** products when possible.
- Clouds, shadows, haze, and aerosols contaminate NDVI values.
- Proper masking is essential.

### **Soil Background Influence**
- Sparse vegetation may produce misleading NDVI due to soil reflectance.
- Alternatives: **SAVI**, **MSAVI**, **EVI**.

### **Water & Coastal Boundaries**
- Water surfaces, shallow waters, algae blooms, and sunglint can distort NDVI.
- NDVI is unreliable close to coastlines or in turbid waters.

### **Sensor Variability**
- NDVI is broadly comparable across sensors, but variations in calibration and band placement may cause slight differences.

---

## **7. Google Earth Engine Example (Generic Formula)**

```javascript
// Example NDVI computation using any optical dataset with RED and NIR bands

// Choose a dataset (example: Sentinel-2 SR)
var collection = ee.ImageCollection('COPERNICUS/S2_SR')
  .filterBounds(geometry)
  .filterDate('2024-01-01', '2024-12-31')
  .filter(ee.Filter.lt('CLOUDY_PIXEL_PERCENTAGE', 20));

// Compute NDVI generically
var ndviCollection = collection.map(function(img) {
  var ndvi = img.normalizedDifference(['B8', 'B4']).rename('NDVI');
  return img.addBands(ndvi);
});

// Visualize median NDVI composite
var ndvi = ndviCollection.select('NDVI').median();

Map.addLayer(ndvi, {min: 0, max: 1, palette: ['white','yellow','green']}, 'NDVI');
Map.centerObject(geometry, 10);
```

Modify band names as needed for Landsat or MODIS.

## **8. References**

- Tucker, C. J. (1979). *Red and photographic infrared linear combinations for monitoring vegetation.*
- USGS Landsat Science Documentation
- ESA Sentinel-2 MSI User Handbook
- MODIS Vegetation Index User Guide
