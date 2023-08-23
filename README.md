# Post-wildfire vegetation regrowth analysis
This is an [Earth Lab](https://earthlab.colorado.edu/) Certificate project by [Stepan Bryleev](https://github.com/StepanBryleev) studying post-wildfire vegetation regrowth dynamics and is a continuation of the [Post-wildfire recovery](https://github.com/AreteY/post-wildfire-recovery) research by [Heidi Yun](https://github.com/AreteY).

## Project goal 
In this project, we explore the post-wildfire vegetation regrowth dynamics for the 2016 Chimney Tops 2 Fire perimeter by using NEON LiDAR, NEON reflectance and Landsat reflectance data. All analysis for NEON and Landsat data is performed in a GEE. So our second goal is to create a tutorial for NEON's website which can help Earth scientists to understand the fundamentals of using GEE when working with NEON reflectance data for studying wildfires.

## GEE project page
To run the project workflow use this link:
**not available yet**

## Data
1. [**NEON Imaging Spectrometer Directional Reflectance data**](https://data.neonscience.org/data-products/DP1.30006.001)
- **Reference:** NEON (National Ecological Observatory Network). Spectrometer orthorectified surface directional reflectance - mosaic (DP3.30006.001), RELEASE-2023. https://doi.org/10.48443/wzwj-nm11. Dataset accessed from https://data.neonscience.org on June 1, 2023
2. [**NEON Lidar Ecosystem Structure data**](https://data.neonscience.org/data-products/DP3.30015.001)
- **Reference:** NEON (National Ecological Observatory Network). Ecosystem structure (DP3.30015.001), RELEASE-2023. https://doi.org/10.48443/y26y-sj42. Dataset accessed from https://data.neonscience.org on June 1, 2023 
3. [**Landsat 8 Surface Reflectance data**](https://www.usgs.gov/landsat-missions/landsat-8)
- **Reference:** Landsat Level-2 Surface Reflectance Science Product, courtesy of the U.S. Geological Survey. Vermote, E., Justice, C., Claverie, M., & Franch, B. (2016). Preliminary analysis of the performance of the Landsat 8/OLI land surface reflectance product. Remote Sensing of Environment. http://dx.doi.org/10.1016/j.rse.2016.04.008.
Dataset accessed from [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2).

4. **Great Smoky Mountains National Park Perimeter**
- **Reference:** National Park Service - Land Resources Division. [Great Smoky Mountains National Park Boundary](https://grsm-nps.opendata.arcgis.com/maps/ab7a3b0981da4b40b97733abdc1a366b/about). \
Data accessed June 1, 2023. More data available: https://grsm-nps.opendata.arcgis.com.

5. **Chimney Tops 2 Fire Perimeter**
- **Reference:** MTBS Data Access: Fire Level Geospatial Data. (2022, February - last revised). MTBS Project (USDA Forest Service/U.S. Geological Survey).  Data accessed June 1, 2023. Available for download from [Post-Wildfire Recovery](https://github.com/AreteY/post-wildfire-recovery) repository as [Release v1.0.1](https://github.com/AreteY/post-wildfire-recovery/releases) ```chimtops2-boundary```. Original source: https://mtbs.gov/direct-download.


## Project Workflow 
Post-wildfire vegetation regrowth analysis is performed for a 36.35 km2 area within the burn perimeter in Great Smokey Mountains. Regrowth dynamics is characterized using Vegetation Indices (such as NBR, NDVI, NDMI, MSI) and Canopy Height Models(CHMs) of difference. Each index and CHMs were calculated in separate files of GEE project. Then all the code from GEE files was duplicated in separated .ipynb files and saved in the ```notebooks``` folder of this repository. To reproduce our analysis on your computer please follow instructions below.

## Run the workflow
### Google Earth Engine
First, visit [Google Earth Engine](https://earthengine.google.com/) official web-page to learn more about GEE and [GEE Code Editor](https://developers.google.com/earth-engine/guides/playground). GEE Code Editor is a web-based IDE for the Earth Engine JavaScript API. Detailed [documentation and guides](https://developers.google.com/earth-engine/) are written for all objects and methods which can be used for JavaScipt in the Code Editor or for Python in Colab (where applicable).

### Python environment
To run .ipynb and other python files you need to have python environment installed on your computer. To learn how to install a conda environment from a .yml file that contains a list of desired Python packages visit [this page](https://www.earthdatascience.org/workshops/setup-earth-analytics-python/setup-python-conda-earth-analytics-environment/).

### Run the code
This repository includes .ipynb files containg JavaScript code from GEE for analysing and plotting NEON and Landsat data. You can find these .ipynb files in the ```notebooks``` folder. Create your own GEE project and use completed JavaScript code from .ipynb files of this repository to reproduce this project.

**Attention!** To plot GRSM National Park and Chimney Tops 2 Fire boundaries you need to add corresponding data files into the Assets tab in your GEE project. You can find these data files in the ```boundaries``` folder of present repository. To learn how to manage GEE assets please visit this GEE [Managing Assets](https://developers.google.com/earth-engine/guides/asset_manager) page.

First, activate your conda environment. Next, proceed to the project directory and then open ```notebooks``` directory. Use Jupyter Notebook to open any .ipynb file in your default web browser. As an example, we have opened the notebook ```nis_grsm_chm.ipynb``` below:
```
$ conda activate earth-analytics-pyhton
$ cd post-wildfire-vegetation-regrowth-analysis
$ cd notebooks
$ jupyter notebook nis_grsm_chm.ipynb
```    
- Run the notebook ```nis_grsm_chm.ipynb``` to find the code for calculating and visualizing interannual CHMs for NEON Lidar data in GEE.
- Run the notebook ```nis_grsm_nbr.ipynb``` and ```ls_grsm_nbr.ipynb``` to find the code for calculating and visualizing interannual NBR values in GEE for NEON and Landsat reflectance data, respectively.
- Run the notebook ```nis_grsm_ndvi.ipynb``` and ```ls_grsm_ndvi.ipynb``` to find the code for calculating and visualizing interannual NDVI values in GEE for NEON and Landsat reflectance data, respectively.
- Run the notebook ```nis_grsm_ndmi.ipynb``` and ```ls_grsm_ndmi.ipynb``` to find the code for calculating and visualizing interannual NDMI values in GEE for NEON and Landsat reflectance data, respectively.
- Run the notebook ```nis_grsm_msi.ipynb``` and ```ls_grsm_msi.ipynb``` to find the code for calculating and visualizing interannual MSI values in GEE for NEON and Landsat reflectance data, respectively.

Just copy the code from the .ipynb file and paste into your GEE project file to make it work.

## License 
The **Post-wildfire vegetation regrowth analysis** project is under the [MIT](https://github.com/StepanBryleev/post-wildfire-vegetation-regrowth-analysis/blob/main/LICENSE) license.

## Citation
```
cff-version: 1.2.0
title: Post-wildfire vegetation regrowth
message: '"If you use this software, please cite it as below"'
type: dataset
authors:
  - given-names: Stepan
    family-names: Bryleev
identifiers:
  - type: doi
    value: 10.5281/zenodo.8222284
repository-code: >-
  https://github.com/StepanBryleev/post-wildfire-vegetation-regrowth-analysis/tree/main
license: MIT
version: '1.0'
```    
