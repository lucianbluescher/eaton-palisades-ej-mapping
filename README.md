# Los Angeles Wildfire false color mapping
### EDS 220: Working with Environmental Datasets: Homework 4
### Lucian Scher - 11/25/25

## About
This notebook containst the 4th assignment for EDS 220, a course in the MEDS program. This project explores the impacts of the 2025 Eaton and Palisades Fires using remote sensing data. After data cleaning and exploration we create a true color and false color image of the two fires with boundaries for the affected area in order to visualize the impact and scale of wildfires on the Los Angeles Area. 

## Data Access
The first data needed for this project is a simplified collection of bands (red, green, blue, near-infrared and shortwave infrared) from the Landsat Collection 2 Level-2 atmosperically corrected surface reflectance data, collected by the Landsat 8 satellite. Landsat data was accessed 11/15/25 from a drive given by instructors but can be found on at [Microsoft Planetary Computer](https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2). Eaton and Palisades fire Perimeter data can be found on LA counties ArcGis, and was accessed 11/15/25 [database](https://egis-lacounty.hub.arcgis.com/maps/ad51845ea5fb4eb483bc2a7c38b2370c/about).

## Repository Structure
```
eds220-hwk4
│
├── .gitignore                              
├── README.md                               # Project overview and instruction                  
├── hwk4-task2-false-color-SCHER.ipynb      # Jupyter notebook for false-color analysis
```
## References

Data:

_Fire Perimeter Data_:

[1] Palisades and Eaton Dissolved Fire Perimeters (2025). (2025). Arcgis.com. https://egis-lacounty.hub.arcgis.com/maps/ad51845ea5fb4eb483bc2a7c38b2370c/about

_Landsat 08 geospatial data_:

‌[2] Microsoft Planetary Computer. (2025). Microsoft.com. https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2

Background information and Landsat band combinations: 

[3] Why is that Forest Red and That Cloud Blue? (2014, March 4). Nasa.gov; NASA Earth Observatory. https://earthobservatory.nasa.gov/features/FalseColor

[4] What are the band designations for the Landsat satellites? (2025, July 11). USGS. https://www.usgs.gov/faqs/what-are-band-designations-landsat-satellites

[5] Common Landsat Band Combinations. (2021, November 12). USGS. https://www.usgs.gov/media/images/common-landsat-band-combinations
