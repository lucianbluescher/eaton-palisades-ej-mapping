# Los Angeles Wildfire False-Color & EJI Analysis

**Geospatial analysis of the 2025 Palisades and Eaton fires using Landsat multispectral imagery and tract-level poverty from the Environmental Justice Index (EJI).**  
Author: Lucian Scher  
Date: 12/11/2025

## Overview
This repo contains two linked analyses of the 2025 Palisades and Eaton fires. The first (LAfire-mapping.ipynb) maps the fire footprints with Landsat true- and false-color composites to visualize burn extent and severity. The second (LAfire-EJI-analysis.qmd) assesses potential socioeconomic vulnerability by mapping tract-level poverty within each fire perimeter using the the Environmental Justice Index. It provides the notebooks/scripts, data sources, and outputs needed to reproduce both the remote-sensing and poverty overlay.

## Data
We use three datasets:
1) **Fire perimeters (Palisades & Eaton)**  
   Dissolved fire perimeter polygons from FIRIS (Los Angeles County NIFC) via ArcGIS Online, used to clip imagery and intersect census tracts.  
   Link: https://egis-lacounty.hub.arcgis.com/maps/ad51845ea5fb4eb483bc2a7c38b2370c/about (accessed 2025-12-22)

2) **Landsat 8 Collection 2 Level-2 surface reflectance**  
   Multispectral bands from Microsoft Planetary Computer, clipped to the study area for true- and false-color composites and burn visualization. Key bands used:  
   - Red/Green/Blue (Bands 4/3/2) for true color  
   - NIR (Band 5) for vegetation response  
   - SWIR 1/2 (Bands 6/7) for moisture/char sensitivity (burn scars)  
   Link: https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2 (accessed 2025-11-22)

3) **Environmental Justice Index (EJI) – poverty indicator**  
   Tract-level E_POV200 (“Percentage of persons with income below 200% of the federal poverty level”) from the 2018–2022 Census Bureau ACS 5-year data, Table S1701. Used to map socioeconomic vulnerability within each fire perimeter.  
   Link: https://www.census.gov/data/developers/data-sets/acs-5year.html (accessed 2025-11-22)  
   EJI portal: https://www.atsdr.cdc.gov/place-health/php/eji/eji-data-download.html

## Repository Structure
```

├── .gitignore 
├── LAfire-EJI-analysis.qmd # EJI/Poverty analysis (census tracts within fire perimeters)
├── LAfire-mapping.ipynb # True-color / false-color Landsat composites for Palisades & Eaton
└── README.md
```

## How to Access/Run
- **Fire perimeters:** Download from ArcGIS Online if not already local.
- **Landsat:** Fetch from Microsoft Planetary Computer; select the scenes covering the Palisades and Eaton footprints (Landsat 8 L2).
- **EJI/ACS:** Download (ACS 2018–2022 5-year, Table S1701) via the EJI portal or ACS API.
- Open `LAfire-mapping.ipynb` for the imagery composites, and `LAfire-EJI-analysis.qmd` for the tract-level poverty maps. Ensure all datasets are available in your working directory or update the paths accordingly.
- Run all cells (note: .ipynb may require more kernel setup)

## References
- FIRIS / Los Angeles County NIFC fire perimeters: https://egis-lacounty.hub.arcgis.com/maps/ad51845ea5fb4eb483bc2a7c38b2370c/about
- Landsat 8 Collection 2 L2 surface reflectance (Microsoft Planetary Computer): https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2
- EJI poverty indicator (E_POV200) via ACS 2018–2022 5-year, Table S1701: https://www.census.gov/data/developers/data-sets/acs-5year.html; EJI portal: https://www.atsdr.cdc.gov/place-health/php/eji/eji-data-download.html
- Background on Landsat bands and false color:
  - NASA Earth Observatory (2014). “Why is that Forest Red and That Cloud Blue?” https://earthobservatory.nasa.gov/features/FalseColor
  - USGS (2025). “What are the band designations for the Landsat satellites?” https://www.usgs.gov/faqs/what-are-band-designations-landsat-satellites
  - USGS (2021). “Common Landsat Band Combinations.” https://www.usgs.gov/media/images/common-landsat-band-combinations


Course:
Masters of Environmental Data Science (MEDS), Bren School of Environmental Science & Management, University of California, Santa Barbara. EDS 220: Working with Environmental Datasets.
