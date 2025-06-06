# Field Camp Project Repository: CTD, Weather, and Stratification Analysis

## Overview

This repository contains all the data, figures, and notebooks generated as part of the 2025 Field Camp project conducted at Stagecoach Reservoir. The study involved mixed layer depth (MLD) estimation, stratification analysis, weather correlation studies, and physical diffusion modeling using CTD measurements and meteorological data.

## Folder Structure

* **Data/**
  Contains all datasets used in this project, including raw, preprocessed, and finalized files:

  * **Georeference\_TIFF/**: Contains TIFF imagery of Stagecoach Reservoir and its dock.
  * **Pre\_Processed\_CTD\_Data/**: Raw daily ZIP folders of CTD cast CSV files collected from May 14–19, 2025.
  * **Processed\_Dock\_Data/**: Final cleaned and filtered CTD files, including `dock_casts_with_mld_patched.csv`, used across nearly all visualizations.
  * **Weather\_Data/**: Contains weather station files, including:

    * `C3SKI.2025-05-28.xlsx`: Ground truth meteorological data from the C3SKI station (operated by UCSD).
    * `C3KNT.2025-06-02.xlsx`: Secondary nearby weather station.
    * `ERA_Data.grib`: ERA5 model-based regional weather data.

* **Figures/**
  Folder to save plots, diagrams, and generated animations from any notebook.

* **Notebooks/**
  Contains all Jupyter Notebooks used for analysis. Each notebook can be re-run after updating file path directories. See author attributions below.

## Notebook Descriptions and Authorship

* `Diffusion_Modeling.ipynb`
  Simulates vertical heat diffusion in the reservoir using a 1D model with the Thomas algorithm.
  **Author:** Thomas Ho

* `Stratification_Analysis.ipynb`
  Calculates temperature gradients and strength of vertical stratification in CTD profiles.
  **Author:** Thomas Ho

* `MLD_Averages.ipynb`
  Aggregates daily and dock-specific mixed layer depth values for summary statistics and visual comparisons.
  **Author:** Marianna Marquardt

* `Local_Weather_Analysis.ipynb`
  Uses GRIB data to analyze local temperature evolution and compare with C3SKI ground station trends.
  **Author:** Marianna Marquardt

* `Initial_Data_Cleaning.ipynb`
  Extracts and filters raw CTD files from ZIP folders and prepares them for dock-specific filtering.
  **Author:** Seth Reichelt

* `Dock_Organization.ipynb`
  Defines spatial boundaries around docks and filters casts based on geographic location.
  **Author:** Seth Reichelt

* `Daily_Evolution_Animations.ipynb`
  Produces animated daily GIFs of water column temperature structure and MLD evolution.
  **Author:** Seth Reichelt

* `MLD_Horizontal_Dock_Analysis.ipynb`
  Compares MLD across East, Central, and West docks to assess horizontal variability.
  **Author:** Seth Reichelt

* `Failed_MLD_Statistical_Analysis.ipynb`
  Attempts linear and mixed-effects regression to correlate wind metrics with MLD. Results were inconclusive due to small sample size and limited wind variability.
  **Author:** Seth Reichelt

* `Weather_MLD_Analysis.ipynb`
  Explores the impact of short-term weather trends on stratification and MLD, referencing C3SKI weather station data.
  **Author:** Seth Reichelt

## Usage Instructions

1. Update all file path strings in the notebooks to point to the appropriate local directories.
2. All required preprocessed and patched CTD data is available in `dock_casts_with_mld_patched.csv`.
3. Weather data for temporal correlation is located in `Weather_Data/`.
4. Visual outputs (plots and animations) will be generated and can be saved to the `Figures/` folder.
5. All code is compatible with standard Python scientific libraries (NumPy, pandas, matplotlib, seaborn, etc.).

## Contact

For any questions regarding this project:

* **Seth Reichelt** (general analysis, all notebook integration): [sreichelt@ucsd.edu](mailto:sreichelt@ucsd.edu)
* **Marianna Marquardt** (field data handling, weather correlation, MLD analysis): [marianna\_marquardt@mines.edu](mailto:marianna_marquardt@mines.edu)

For future Field Camp projects or clarifications regarding data organization, methodology, or CTD postprocessing, please contact one of the authors above.
