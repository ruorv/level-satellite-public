<div align="center">

<img src="https://level-satellite.ru/static/logo.png" alt="Уровень-Спутник" width="80"/>

# Уровень-Спутник · Level-Sputnik

**Match satellite imagery to hydrological water levels across Russia**

[![Live](https://img.shields.io/badge/Live-level--satellite.ru-0088cc?style=flat-square)](https://level-satellite.ru)
[![Sentinel-2](https://img.shields.io/badge/Sentinel--2-ESA-green?style=flat-square)](https://sentinel.esa.int)
[![Landsat](https://img.shields.io/badge/Landsat-USGS-blue?style=flat-square)](https://landsat.gsfc.nasa.gov)
[![MPC](https://img.shields.io/badge/Data-Microsoft%20Planetary%20Computer-purple?style=flat-square)](https://planetarycomputer.microsoft.com)

</div>

---

## What is this?

**Level-Sputnik** is a web tool for hydrologists and remote sensing researchers. Given a hydrological gauging station in Russia, it finds Sentinel-2 and Landsat satellite scenes that match specific water level conditions — automatically, in your browser, no GIS software required.

Built on top of **28 million daily observations** from Russian hydrological stations (2008–2023) linked to satellite imagery via **Microsoft Planetary Computer**.

> Freely accessible, no restrictions, no registration required.

---

## Features

### 🛰 Scene Matching (Tab 1 — Подбор сцен)
- Select any of **2,657 gauging stations** on the interactive map
- Set water level range, date range, months, cloud cover threshold
- Get a list of matching Sentinel-2 / Landsat scenes with exact level values
- Preview scenes directly on the map or download as **GeoTIFF**

### 🌊 Watershed (Tab 2 — Водосбор)
- Automatically delineated catchment polygon for **2,451 stations** using **MERIT-Hydro** (90 m global DEM)
- Key basin characteristics per station: area, population (WorldPop 2020), precipitation (CHIRPS), evapotranspiration (MODIS), mean elevation
- Land cover breakdown (ESA WorldCover 2020): forest, cropland, wetland, built-up, open water and more — shown as sorted progress bars
- GRACE / GRACE-FO groundwater storage trend (cm/decade)
- River network total length, major dams count, irrigated area
- Watershed polygon displayed as a toggleable map layer with opacity control
- **Export**: download watershed polygon with full attribute table as GeoJSON

### 📊 Data Analysis (Tab 3 — Анализ данных)
- Time series chart of water level and discharge
- Monthly averages, min/max extremes
- Ice-free period statistics
- Export data as **CSV or XLSX**

### 🗺 Scene Browser (Tab 4 — Снимки)
- Free search by drawn area on the map
- Filter by date range, months, cloud cover
- Independent of station selection

---

## Screenshots

<table>
<tr>
<td><img src="https://level-satellite.ru/static/screen_map.png" width="400" alt="Map with stations"/></td>
<td><img src="https://level-satellite.ru/static/screen_scenes.png" width="400" alt="Scene matching"/></td>
</tr>
<tr>
<td align="center"><em>2,657 hydrological stations across Russia</em></td>
<td align="center"><em>Matched Landsat scene at water level 78 cm</em></td>
</tr>
<tr>
<td><img src="https://level-satellite.ru/static/screen_analysis.png" width="400" alt="Data analysis"/></td>
<td><img src="https://level-satellite.ru/static/screen_chart.png" width="400" alt="Time series"/></td>
</tr>
<tr>
<td align="center"><em>Station statistics and KPI</em></td>
<td align="center"><em>Water level and discharge time series</em></td>
</tr>
</table>

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python · Flask · Gunicorn |
| Database | PostgreSQL · PostGIS · 28M rows |
| Satellite data | Microsoft Planetary Computer API |
| Watershed data | mghydro.com · MERIT-Hydro 90 m |
| Frontend | Vanilla JS · Leaflet.js · Chart.js |
| Infrastructure | Docker · nginx · Let's Encrypt |

---

## Data Coverage

- **Stations**: 2,657 Russian hydrological gauging stations
- **Watersheds**: 2,451 automatically delineated catchment basins (MERIT-Hydro 90 m)
- **Observations**: Daily water level (L) and discharge (Q) measurements
- **Period**: 2008–2023
- **Satellite**: Sentinel-2 L2A, Landsat 8/9 SR via Microsoft Planetary Computer
- **Land cover**: ESA WorldCover 2020 (10 m)
- **Population**: WorldPop 2020
- **Precipitation**: CHIRPS climatology
- **Groundwater**: GRACE / GRACE-FO satellite gravimetry

---

## Authors

<table>
<tr>
<td align="center">
<b>Pavel Golovlev</b><br/>
Founder · Hydrologist<br/>
<a href="mailto:golovlevpp@my.msu.ru">golovlevpp@my.msu.ru</a>
</td>
<td align="center">
<b>Aleksandr Innokентьев</b><br/>
Developer<br/>
<a href="mailto:innokentevai@my.msu.ru">innokentevai@my.msu.ru</a>
</td>
</tr>
</table>

---

## Use the tool

🌐 **[level-satellite.ru](https://level-satellite.ru)**

---

## Citation

If you use this tool in your research, please cite:

```
Golovlev P.P., Innokentev A.I. (2026). Уровень-Спутник: web tool for matching
satellite imagery to hydrological station water levels in Russia.
https://level-satellite.ru
```

---

<div align="center">
<sub>© 2026 Golovlev P.P. · Innokentev A.I. · All rights reserved</sub>
</div>
