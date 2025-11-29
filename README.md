# Sentinel-5P-NO-yearly-extraction-2018-2025-using-GEE.
🌏 Bangladesh NO₂ (Nitrogen Dioxide) Yearly Analysis (2018–2025)
Google Earth Engine • Sentinel-5P OFFL + NRTI • NO₂ Concentration Mapping

This repository contains a complete Google Earth Engine (GEE) workflow for generating yearly NO₂ pollution maps, CSV statistics, time-series charts, and GeoTIFF exports for Bangladesh using the Sentinel-5P TROPOMI dataset.

The workflow produces:

✔ Yearly NO₂ mean images (2018–2025)
✔ Maps visualized on GEE
✔ CSV table of yearly mean NO₂
✔ Line chart (time-series)
✔ Yearly GeoTIFF exports (1113 m resolution)
✔ OFFL & NRTI datasets supported

📌 Dataset Overview

Primary Dataset:
COPERNICUS/S5P/OFFL/L3_NO2
Secondary Dataset (TIFF Export):
COPERNICUS/S5P/NRTI/L3_NO2

Key Band Used:

NO2_column_number_density — total NO₂ column density (mol/m²)

Native Resolution:
≈ 1113.2 meters

🎯 Objectives

This study aims to:

Analyze long-term atmospheric NO₂ levels over Bangladesh

Identify annual variations from 2018 to 2025

Generate TIFF maps for spatial visualization

Create a CSV summary for statistical analysis

Visualize temporal trends using a time-series chart

📁 Repository Contents
File/Folder	Description
NO2_Analysis_2018_2025.js	Full GEE script for yearly mapping & export
README.md	Documentation file
Bangladesh_NO2_TIFF/	Folder for exported yearly GeoTIFFs
Bangladesh_NO2_Yearly_2018_2025.csv	Exported CSV summary of NO₂ mean values
🛰 Methodology
1. Data Filtering

For each year (2018–2025):

Filter Sentinel-5P images over the Bangladesh boundary

Select the NO₂ band

Compute annual mean using ImageCollection.mean()

2. Visualization

Each year's NO₂ map is displayed using a color scale:

['black','blue','purple','cyan','green','yellow','red']

3. Statistics

Mean NO₂ for Bangladesh is extracted using:

reduceRegion()


with:

Scale: 1113.2 m

Reducer: mean

Results are exported as CSV.

4. TIFF Export

Using the NRTI dataset, yearly mean NO₂ images are exported as GeoTIFF for offline GIS use.

📈 Outputs
✔ Time-Series Chart

Shows year-wise changes in NO₂ concentration (mol/m²).

✔ CSV Table

Contains:

year	NO2_mean
2018	...
2019	...
…	…
2025	...
✔ GeoTIFF Maps

Suitable for:

ArcGIS / QGIS

Research / publication

Policy analysis

🔧 Requirements

To run this project:

A Google Earth Engine account

Copy the script into https://code.earthengine.google.com

No installation required.

🚀 How to Use
1. Open Google Earth Engine

Go to:
https://code.earthengine.google.com

2. Paste the Script

Copy the .js code into GEE Code Editor.

3. Run to Generate Maps & CSV

The script will automatically:

Render yearly maps

Print time-series graph

Generate CSV table

Start TIFF exports

📜 Citation (Suggested)

If you use this repository in research:

Hazera, B. (2025). Bangladesh NO₂ Analysis (2018–2025) using Sentinel-5P TROPOMI & Google Earth Engine. GitHub Repository.

📧 Contact

For clarification or collaboration:

Author: Bibi Hazera
Research Area: Remote sensing, Air quality, GIS, Climate change

📄 License

MIT License — free to use, modify, cite.
