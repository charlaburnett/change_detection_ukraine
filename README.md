# Urban Change Detection in Mariupol Using Sentinel-1 SAR

**Author:** [charlaburnett](https://github.com/charlaburnett)  
**Project:** Geospatial analysis of conflict-related urban change using open EO data and Earth Engine

---

## Overview

This project uses Sentinel‑1 Synthetic Aperture Radar (SAR) imagery and the Global Human Settlement Layer (GHSL) to detect and quantify structural changes in the city of Mariupol, Ukraine 
between **early 2021** and **mid‑2022** — the period of Russia’s full-scale invasion.

The analysis identifies radar backscatter increases likely due to **building destruction**, **surface disruption**, and **new construction**.

---

## Key Results

| Metric                             | Value              |
|------------------------------------|--------------------|
| Urban SAR change area              | **64.89 sq km**    |
| Total built-up area (GHSL-defined) | **172.13 sq km**   |
| Percent of city changed            | **37.7%**          |

> SAR change is concentrated in industrial zones, residential blocks, and port-adjacent neighborhoods — consistent with open-source conflict damage reports.

---

## Methodology

1. **AOI:** Defined bounding box around Mariupol
2. **Data Sources:**
   - Sentinel‑1 SAR (VV polarization, pre/post)
   - GHSL Built-Up Grid (2014 baseline)
   - Earth Engine public datasets
3. **Steps:**
   - Filter Sentinel‑1 images (Jan–Mar 2021 vs. May–Jul 2022)
   - Compute log-ratio backscatter change
   - Mask positive change (increase in radar reflectance)
   - Apply GHSL urban mask
   - Compute pixel area & percentage

---

## Visualization

[Change Detection Mariupol Map](http://maps.charlaburnett.com/change_detection_mariupol.html)


---
### Extracted Events

1. **Prisoner Swap and Captures:**
   - Event: Ukrainian soldiers captured by Russia in Mariupol were released.
   - Date: June 27, 2025
   - Confidence: High

2. **Theatre Bombing:**
   - Event: Bombing of Mariupol theatre (referenced in multiple retrospectives)
   - Confidence: High

3. **Prison Terms for Azov Fighters:**
   - Event: Russia sentenced Azov battalion fighters
   - Confidence: Medium (location inferred)

4. **Starvation Tactics:**
   - Event: Accusations of Russia using hunger as a weapon during siege
   - Date: June 12, 2024
   - Confidence: Medium

### Flagged Events Likely Causing SAR-Detected Change

- **Theatre Bombing:** High structural impact
- **Starvation Siege:** Indirect impact via infrastructure degradation

### Extracted Events

1. **Prisoner Swap and Captures:**
   - Event: Ukrainian soldiers captured by Russia in Mariupol were released.
   - Date: June 27, 2025
   - Confidence: High

2. **Theatre Bombing:**
   - Event: Bombing of Mariupol theatre (referenced in multiple retrospectives)
   - Confidence: High

3. **Prison Terms for Azov Fighters:**
   - Event: Russia sentenced Azov battalion fighters
   - Confidence: Medium (location inferred)

4. **Starvation Tactics:**
   - Event: Accusations of Russia using hunger as a weapon during siege
   - Date: June 12, 2024
   - Confidence: Medium

### Flagged Events Likely Causing SAR-Detected Change

- **Theatre Bombing:** High structural impact
- **Starvation Siege:** Indirect impact via infrastructure degradation
  
[Full OSINT Summary](https://github.com/charlaburnett/change_detection_ukraine/blob/main/mariupol_osint.ipynb)
---
## Tools Used

- [Google Earth Engine](https://earthengine.google.com/)
- [Google Colab](https://colab.research.google.com/)
- `geemap`, `folium`, `rasterio`, `ee`
- Sentinel‑1 SAR (Copernicus Open Data)
- [GHSL (JRC)](https://ghsl.jrc.ec.europa.eu/)


*For questions, contact [charlaburnett](https://github.com/charlaburnett) or fork the repo and submit a pull request.*

