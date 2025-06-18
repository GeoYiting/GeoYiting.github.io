---
title: "Landfill Site Suitability Modeling"
date: 2022-01-07 00:00:00 +0000
categories: [portfolio]
image:
  path: /assets/landfill_model.png
  alt: "Landfill Suitability GIS Model"
---

This project develops a GIS-based **multi-criteria decision analysis (MCDA)** model for identifying optimal landfill locations in Monongalia County, WV. It uses a combination of slope, hydrology, land cover, road proximity, and area size as input criteria to determine the most cost-efficient and environmentally sound sites.

## 🔍 Project Goals

- Identify suitable landfill sites that minimize environmental and social impacts
- Integrate landcover, slope, hydrology, and road networks into a raster-based GIS model
- Use cost-distance analysis to find the optimal path and site with the lowest traveling cost to Morgantown
- Compare results under two different modeling scenarios

## 🧩 Tools and Data

- **GIS Platform:** ArcGIS Pro
- **Key Data Sources:**
  - 30m-resolution DEM for slope analysis
  - Landcover raster (1992)
  - USGS Hydrography data (2000)
  - TIGER/line Roads (2011)
  - WV GIS Tech Center datasets

## 🛠 Methodology

## 🗺 Study Area and Extent
Location of Monongalia County and Morgantown, WV
![Study Area Map](/assets/MapExtent.JPG)


## 🔁 GIS Workflow for Landfill Site Suitability Modeling

Full MCDA-based GIS workflow:
![Model Workflow Diagram](/assets/Workflow.JPG)

### 1. Candidate Site Selection
- **Hydrology:** Exclude areas within 500m (Model 1) and 600m (Model 2) of waterways
- **Landcover:** Only pasture, grassland, or reclaimed mines allowed
- **Minimum Site Area:** 0.04 km²

### 2. Cost Surface Modeling
- Slope and road layers reclassified to assign **traveling cost weights**
- Model 2 uses USDA slope classification for more realistic terrain weighting

| Slope (%) | Model 1 Weight | Model 2 Weight |
|-----------|----------------|----------------|
| 0–5       | 1              | —              |
| 5–10      | 10             | —              |
| 10–15     | 100            | —              |
| >15       | 1000           | —              |
| 0–6       | —              | 1              |
| 6–25      | —              | 10             |
| 25–40     | —              | 100            |
| >40       | —              | 1000           |

### 3. Cost Distance and Optimal Route
- Total cost surface = Slope Cost + Road Cost
- Cost-distance analysis run from Morgantown to each candidate site
- Optimal site = lowest accumulated cost
  
Criteria maps of model 1 (above) and 2 (below):
![Criteria maps of model 1 (above) and 2 (below)](/assets/landfill_model.png)

## 📊 Results Overview

- **Model 1** produced 5 candidate sites, mostly west of Morgantown
- **Model 2** (stricter hydrology and slope criteria) yielded 2 sites, both in Little Indian Creek WMA
- Optimal sites:
  - **Model 1:** Near Cassville (20 min to Morgantown)
  - **Model 2:** Near Glory Barn Road (15 min)

![Candidate Sites Map](/assets/result.JPG)

## 📈 Cost Distance Outputs

Travel cost surfaces derived from road and slope weights:

![Cost Effect Maps](/assets/costeffect.JPG)

## 📈 Discussion

- Model 2 produced more realistic results with lower total cost
- Hydrology proximity had the **strongest influence** on site suitability
- Roads and DEM resolution introduced uncertainty in routing
- Recommendations include:
  - Using higher-resolution DEM
  - Incorporating floodplain, land ownership, and proximity to protected areas

## 🧠 Key Takeaways

> “All models are wrong, but some are useful.” — Box et al. (1978)

- A raster-based GIS model allows systematic, scalable landfill site evaluation
- Integrating MCDA with GIS helps balance environmental and logistical criteria
- Hydrological buffers and slope constraints are essential for public health and cost minimization

## 📂 Downloads

- 📄 [Full Report PDF](/assets/Landfill_Site_Suitability_Model.pdf)

---
