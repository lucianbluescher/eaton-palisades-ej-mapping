# eds220-hwk4
# About
This notebook explores the impacts of the 2025 Eaton and Palisades Fires using remote sensing data. After some data cleaning and exploration we create a false color image of the two fires with boundaries for the affected area in order to visualize the impact of these to wildfires on the surrounding area.

# Data Access
The Data needed for this project can be found in the data/ folder in the repository. Landsat data was given by instructors but can be found on the [Microsoft Planetary Computer](https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2). Perimeter data can be found on LA counties ArcGis [database](https://egis-lacounty.hub.arcgis.com/maps/ad51845ea5fb4eb483bc2a7c38b2370c/about).

# Repository Structure
```
eds220-hwk4
│
├── README.md                               # Project overview and instructions
├── .gitignore                              
├── .Rhistory                               
├── eds220-hwk4.Rproj                       # RStudio project file
├── hwk4-task2-false-color-SCHER.ipynb      # Jupyter notebook for Task 2 false-color analysis
│
├── data/                                   # All datasets
│   ├── Eaton_Perimeter_20250121/           # Shapefile for Eaton fire perimeter
│   ├── Palisades_Perimeter_20250121/       # Shapefile for Palisades fire perimeter
│   └── landsat8-2025-02-23-palisades-eaton.nc   # Landsat 8 surface reflectance bands
│
└── .Rproj.user/                            # RStudio internal project settings (auto-generated)
```
# References

Data:

[1] Palisades and Eaton Dissolved Fire Perimeters (2025). (2025). Arcgis.com. https://egis-lacounty.hub.arcgis.com/maps/ad51845ea5fb4eb483bc2a7c38b2370c/about

‌[2] Microsoft Planetary Computer. (2025). Microsoft.com. https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2

Background information and Landsat band combinations: 

[3] Why is that Forest Red and That Cloud Blue? (2014, March 4). Nasa.gov; NASA Earth Observatory. https://earthobservatory.nasa.gov/features/FalseColor

[4] What are the band designations for the Landsat satellites? (2025, July 11). USGS. https://www.usgs.gov/faqs/what-are-band-designations-landsat-satellites

[5] Common Landsat Band Combinations. (2021, November 12). USGS. https://www.usgs.gov/media/images/common-landsat-band-combinations
