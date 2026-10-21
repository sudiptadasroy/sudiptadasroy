
# 🌍 Sudipta Das Roy

### Geoinformatics | GIS Engineering | Remote Sensing | GeoAI

<p align="center">
  <i>Turning Spatial Data into Meaningful Decisions</i>
</p>

<p align="center">
  <a href="https://github.com/sudiptadasroy">GitHub</a> •
  <a href="https://github.com/sudiptadasroy/GeoRoute-Explorer">GeoRoute Explorer</a> •
  <a href="https://www.linkedin.com/">LinkedIn</a>
</p>

---

## 🐍 Contribution Snake

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sudiptadasroy/sudiptadasroy/output/github-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/sudiptadasroy/sudiptadasroy/output/github-snake.svg">
    <img alt="GitHub contribution snake animation" src="https://raw.githubusercontent.com/sudiptadasroy/sudiptadasroy/output/github-snake.svg" width="100%">
  </picture>
</p>


## 👨‍💻 About Me

I'm an M.Sc. Geoinformatics student at **TERI School of Advanced Studies**, interested in building practical geospatial solutions using GIS, remote sensing, spatial analytics, and GeoAI.

My work focuses on transforming geographic data into useful insights for environmental monitoring, natural-hazard assessment, coastal analysis, and spatial decision-making.

- 🎓 M.Sc. Geoinformatics
- 🛰️ GIS, remote sensing, and satellite data analysis
- 🐍 Python-based geospatial workflows
- 🗺️ Interactive maps and WebGIS applications
- 🤖 Exploring GeoAI and machine learning
- 🎯 Interested in GIS engineering and geospatial developer opportunities

## 🛠️ Technical Skills

| Category | Technologies |
|---|---|
| GIS | QGIS, ArcGIS Pro, Google Earth Pro |
| Remote Sensing | Google Earth Engine, Sentinel-1 SAR, Sentinel-2 MSI, Landsat 8/9, MODIS, Resourcesat-2 LISS-IV, ERDAS IMAGINE, SNAP |
| Remote Sensing Analysis | NDVI, NDWI, MNDWI, LULC Classification, Change Detection, Land Surface Temperature, SAR Analysis |
| Programming | Python, JavaScript, SQL, C++ |
| Python GIS | GeoPandas, Rasterio, Shapely, Pandas, NumPy |
| Web Mapping | Folium, Leaflet, Streamlit |
| Spatial Databases | PostgreSQL, PostGIS |
| WebGIS | GeoServer, spatial data publishing |
| Visualization | Matplotlib, interactive maps, dashboards |

## 🚀 Featured Projects

### 🧭 GeoRoute Explorer

A Python-based GIS dashboard for exploring locations and visualizing geographic data and road routes.

**Stack:** Python · Streamlit · Pandas · Folium · OSRM


**[View Repository →](https://github.com/sudiptadasroy/GeoRoute-Explorer)**


### 🔥 Forest Fire Risk Assessment

Spatial analysis of forest-fire patterns, hotspots, vegetation conditions, and environmental risk factors in Idukki and Palakkad, Kerala.

**Stack:** Google Earth Engine · Sentinel-2 · QGIS · Spatial Analysis

[Explore Repositories →](https://github.com/sudiptadasroy?tab=repositories)

### 🌊 Coastal Shoreline Change

Remote-sensing analysis of shoreline and land-use/land-cover changes at Shivrajpur Beach, Gujarat, and Eden Beach, Puducherry.

**Stack:** Satellite Imagery · GIS · NDVI · NDWI · LULC

[Explore Repositories →](https://github.com/sudiptadasroy?tab=repositories)

### ⛏️ Mine Safety & Spatial Analysis

GIS research exploring mining accidents, spatial patterns, and mine-safety assessment.

**Stack:** QGIS · PostgreSQL · PostGIS · WebGIS

[Explore Repositories →](https://github.com/sudiptadasroy?tab=repositories)


## 🌐 Geospatial Engineering Dashboard

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,js,postgres,github,vscode" alt="Programming and development tools" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/QGIS-GIS-589632?style=for-the-badge&logo=qgis&logoColor=white" />
  <img src="https://img.shields.io/badge/Google_Earth_Engine-Remote_Sensing-4285F4?style=for-the-badge&logo=googleearth&logoColor=white" />
  <img src="https://img.shields.io/badge/PostGIS-Spatial_Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/GeoAI-Machine_Learning-8A2BE2?style=for-the-badge" />
</p>


### 📈 Development Activity

<p align="center">
  <img
    src="https://github-readme-activity-graph.vercel.app/graph?username=sudiptadasroy"
    width="100%"
    alt="Sudipta's GitHub activity graph"
  />
</p>

### 🛰️ My Geospatial Toolkit

| Domain | Focus |
|---|---|
| Remote Sensing | Sentinel-1, Sentinel-2, Landsat |
| Spatial Analytics | Raster analysis, vector analysis, hotspot mapping |
| GeoAI | Machine learning for geospatial applications |
| WebGIS | Leaflet, Streamlit, GeoServer |
| Spatial Databases | PostgreSQL, PostGIS |

<p align="center">
  <i>Building geospatial solutions, one map at a time. 🌍</i>
</p>


## 🌱 Currently Exploring

- GeoAI and machine learning for geospatial applications
- Python automation for GIS and remote sensing
- WebGIS and interactive spatial dashboards
- PostGIS and geospatial data infrastructure
- Publishing and deploying geospatial applications

## 🤝 Let's Connect

I'm interested in collaborating on geospatial projects, applied research, and opportunities in GIS engineering, remote sensing, and GeoAI.

- 💻 GitHub: [@sudiptadasroy](https://github.com/sudiptadasroy)
- 💼 LinkedIn: [Connect with me](linkedin.com/in/sudipta-das-roy-b4ba39352)

---

<p align="center">
  <i>GeoSpatial • Open Source • Real-World Impact</i>
</p>


name: Generate Contribution Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10

    steps:
      - name: Generate contribution snake
        uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
            dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9&color_background=#aaaaaa

      - name: Publish generated files
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

