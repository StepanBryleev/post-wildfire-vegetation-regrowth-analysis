# Post-wildfire vegetation regrowth analysis
This is an [Earth Lab](https://earthlab.colorado.edu/) Certificate project by Stepan Bryleev studying post-wildfire vegetation regrowth dynamics and is a continuation of the [Post-Wildfire recovery](https://github.com/AreteY/post-wildfire-recovery) project by [Heidi Yun](https://github.com/AreteY).

## Project goal 
In this project, we explore the post-wildfire vegetation regrowth dynamics for the 2016 Chimney Tops 2 Fire perimeter by using Landsat, NEON LiDAR and NEON hyperspectral reflectance data. All analysis for NEON and Landsat data is performed in a GEE. So our second goal is to create a tutorial for NEON's website which can help Earth scientists to understand the fundamentals of using GEE when working with NEON reflectance data for studying wildfires.

## GEE project page
To run project workflow use this link:


## Data
1. [**NEON Imaging Spectrometer Directional Reflectance data**](https://data.neonscience.org/data-products/DP1.30006.001)
- **Reference:** NEON (National Ecological Observatory Network). Spectrometer orthorectified surface directional reflectance - mosaic (DP3.30006.001), RELEASE-2023. https://doi.org/10.48443/wzwj-nm11. Dataset accessed from https://data.neonscience.org on August 5, 2023
2. [**NEON Lidar Ecosystem Structure data**](https://data.neonscience.org/data-products/DP3.30015.001)
- **Reference:** NEON (National Ecological Observatory Network). Ecosystem structure (DP3.30015.001), RELEASE-2023. https://doi.org/10.48443/y26y-sj42. Dataset accessed from https://data.neonscience.org on August 5, 2023 
3. [**Landsat 8 Surface Reflectance data**](https://www.usgs.gov/landsat-missions/landsat-8)
- **Reference:** Landsat Level-2 Surface Reflectance Science Product, courtesy of the U.S. Geological Survey. Vermote, E., Justice, C., Claverie, M., & Franch, B. (2016). Preliminary analysis of the performance of the Landsat 8/OLI land surface reflectance product. Remote Sensing of Environment. http://dx.doi.org/10.1016/j.rse.2016.04.008.
Dataset accessed from [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2).

4. **Great Smoky Mountains National Park Perimeter**
- **Reference:** National Park Service - Land Resources Division. [Great Smoky Mountains National Park Boundary](https://grsm-nps.opendata.arcgis.com/maps/ab7a3b0981da4b40b97733abdc1a366b/about). \
Data accessed June 1, 2023. More data available: https://grsm-nps.opendata.arcgis.com.

5. **Chimney Tops 2 Fire Perimeter**
- **Reference:** MTBS Data Access: Fire Level Geospatial Data. (2022, February - last revised). MTBS Project (USDA Forest Service/U.S. Geological Survey).  Data accessed June 1, 2023. Available for download from [Post-Wildfire Recovery](https://github.com/AreteY/post-wildfire-recovery) repository as [Release v1.0.1](https://github.com/AreteY/post-wildfire-recovery/releases) ```chimtops2-boundary```. Original source: https://mtbs.gov/direct-download.


## Run the workflow
### Google Earth Engine
First, visit [Google Earth Engine](https://earthengine.google.com/) official web-page to learn more about GEE and GEE Code Editor. GEE Code Editor is a web-based IDE for the Earth Engine JavaScript API. This repository includes .ipynb files containg JS code for analysing and plotting reflectance data. You can find these files in the **notebooks** folder.

### Python environment
To run Python files you need to have python environment installed on your computer. To learn how to install a conda environment from a .yml file that contains a list of desired Python packages visit [this page](https://www.earthdatascience.org/workshops/setup-earth-analytics-python/setup-python-conda-earth-analytics-environment/).

### Project Workflow
**Attention!** Project workflow is subject to update. To see a proposal section and preliminary results clone this repository and run the *vegetation_regrowth_analysis_blog.ipynb* notebook.
