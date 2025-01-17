# Washington DC Solar Potential Estimation


<div style="display: flex; justify-content: center; align-items: center; gap: 10px;">
  <img src="qgis-logo.png" alt="Image 1" width="45%" />
  <img src="image2.webp" alt="Image 2" width="45%" />
</div>
## Overview

This project estimates the photovoltaic energy potential for buildings in Washington, DC, leveraging high-resolution geospatial data and advanced modeling tools within **QGIS**. The initiative supports the **Clean Energy DC Omnibus Act**, which targets 100% renewable electricity by 2032, aligning with Washington, DC's commitment to sustainability and clean energy.

## Problem Statement

The adoption of solar energy in urban areas is challenged by complex factors such as diverse building geometries, varying solar exposure, and urban shading effects. To address these issues, this project identifies rooftops with the highest solar potential, providing actionable insights for stakeholders such as city planners, policymakers, and renewable energy companies.

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

## Tools and Technologies
- **QGIS**: Core platform for spatial data processing, analysis, and visualization.
- **UMEP Plugin**: Urban Energy Model Processor for solar modeling.
- **Python**: Automating workflows and data processing tasks.
- **LiDAR and GIS Data**: Input datasets for digital surface modeling and analysis.

## Results and Impact
The results provide critical insights into:
- Buildings with optimal conditions for solar panel installations.
- Quantitative metrics for energy potential to guide renewable energy policies.
- Opportunities for achieving Washington, DC’s clean energy goals.

## References
- [Clean Energy DC Omnibus Act](https://doee.dc.gov/service/clean-energy-dc-omnibus-amendment-act)
- [NASA POWER Data Access Viewer](https://power.larc.nasa.gov/data-access-viewer/)
- [Open Data DC Building Footprints](https://opendata.dc.gov/datasets/a657b34942564aa8b06f293cb0934cbd_1/explore?location=38.893194,-77.019147,10.50)
- [UMEP Documentation for SEBE Model](https://umep-docs.readthedocs.io/en/latest/processor/Solar%20Radiation%20Solar%20Energy%20on%20Building%20Envelopes%20(SEBE).html)
