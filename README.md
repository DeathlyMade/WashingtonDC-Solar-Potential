# Photovoltaic Energy Potential Estimation for Washington DC


<div style="display: flex; justify-content: center; align-items: center; gap: 10px;">
  <img src="qgis-logo.png" alt="Image 1" width="45%" />
  <img src="umep-logo.png" alt="Image 2" width="25%" />
</div>

## Overview

This project estimates the photovoltaic energy potential for buildings in Washington, DC, leveraging high-resolution geospatial data and advanced modeling tools within **QGIS**. The project investigates the feasibility of **Clean Energy DC Omnibus Act**, which targets 100% renewable electricity by 2032, aligning with Washington, DC's commitment to sustainability and clean energy.

## Problem Statement

If solar panels were to be installed on every feasible rooftop of the man-made structures in the city, how much energy can be generated anually?
The adoption of solar energy in urban areas is challenged by complex factors such as diverse building geometries, varying solar exposure, and urban shading effects. To address these issues, this project identifies rooftops with the highest solar potential, providing actionable insights for stakeholders such as city planners, policymakers, and renewable energy companies.

## NOTE  
The data generated by intermediaries has been uploaded unto cloud and link has been provided above. The detailed steps and description of the intermediary data has been provided in the **Photovoltaic_energy_potential_estimation.pdf**. Below is just a brief overview. It is advised to go through **Photovoltaic_energy_potential_estimation.pdf** for clear understanding of the pipeline. 

## Tools and Technologies
- **QGIS**: Core platform for spatial data processing, analysis, and visualization.
- **UMEP Plugin**: Urban Energy Model Processor for solar modeling.
- **Python**: Automating workflows and data processing tasks.
- **LiDAR and GIS Data**: Input datasets for digital surface modeling and analysis.

## Project Workflow

### 1. Data Sources
- **DSM Data**: 1m resolution LiDAR data, timestamped 1st March 2024, to model terrain and structures.
- **Building Footprints**: Planimetric building outlines from a September 2024 update.
- **Solar Irradiance Data**: Hourly solar radiation data (direct, diffuse, and total), spanning from 1st January 2022 to 29th February 2024.

### 2. Methodology
Extensive use of QGIS, alongside the **UMEP plugin** and the **SEBE (Solar Energy on Building Envelopes)** model, facilitated the following processes:
1. **DSM Preparation**: Refinement of raw DSM to ensure accurate building height and slope representation.
2. **Solar Modeling**: Calculation of solar radiation on building envelopes using hourly solar irradiance data.
3. **Rooftop Refinement**: Application of slope and aspect analyses to filter unsuitable roof segments.
4. **Zonal Statistics**: Integration of SEBE outputs with building footprints for spatial analysis and visualization.

### 3. Key Outputs
- Solar energy potential maps for Washington, DC buildings.
- Summary statistics for each rooftop, including solar irradiation, slope, and aspect suitability.
- High-priority zones for solar energy investments.

## Results and Impact
The results provide critical insights into:
- Buildings with optimal conditions for solar panel installations.
- Quantitative metrics for energy potential to guide renewable energy policies (scope of upscaling the solar power generation by as much as 3200%)


## References
- [Clean Energy DC Omnibus Act](https://doee.dc.gov/service/clean-energy-dc-omnibus-amendment-act)
- [NASA POWER Data Access Viewer](https://power.larc.nasa.gov/data-access-viewer/)
- [Open Data DC Building Footprints](https://opendata.dc.gov/datasets/a657b34942564aa8b06f293cb0934cbd_1/explore?location=38.893194,-77.019147,10.50)
- [UMEP Documentation for SEBE Model](https://umep-docs.readthedocs.io/en/latest/processor/Solar%20Radiation%20Solar%20Energy%20on%20Building%20Envelopes%20(SEBE).html)
