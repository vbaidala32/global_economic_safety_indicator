# Economic Security Index for World Countries (2005–2020)

This repository contains the complete analytical workflow for constructing, validating, and visualizing a composite Economic Security Index for more than 190 countries using World Bank data from 2005 to 2020. The project integrates data preprocessing, indicator standardization, principal component analysis (PCA), sensitivity testing, and dashboard-based interactive visualization.

## Repository Structure

## Description of Files

### LR_3_4.ipynb
An R-based notebook implementing Laboratory Work 3 and 4. It includes:
- Retrieval of World Development Indicators (WDI) data
- Data cleaning, interpolation, and transformation
- Recoding of categorical variables
- Normalization of indicators using z-scores
- Inversion of destimulators
- Construction of the composite Economic Security Index
- Principal Component Analysis (PCA)
- Sensitivity analysis using random weighting schemes
- Export of processed results to `data_index.csv`

### dashboard.ipynb
A Python-based interactive dashboard built with Dash and Plotly. It provides:
- Choropleth map visualizations of the index
- Country ranking tables
- Time-series plots
- PCA scatterplots
- Radar charts of indicator profiles

### dashboard.py
A standalone script version of the dashboard allowing execution outside Jupyter Notebook.

### data_index.csv
The final dataset produced after processing. It contains:
- Standardized indicators
- Inverted destimulators
- PCA-ready numerical variables
- The computed Economic Security Index
- Country rankings across years

### Presentation File
The file `Оцінка рівня економічної безпеки країн світу.pptx` summarizes the theoretical background, indicator selection, methodological workflow, PCA interpretation, index results, and key conclusions.

## Methodology Overview

### Indicator Set
The composite index is constructed from six indicators obtained from the World Development Indicators database:
- Trade (% of GDP)
- Foreign Direct Investment (% of GDP)
- Income group classification
- Lending category classification
- Unemployment rate (%)
- Government debt (% of GDP)

Stimulators are applied directly; destimulators are inverted to ensure that higher transformed values represent higher economic security. All indicators are standardized using z-scores.

### Data Processing
The workflow includes:
- Retrieval of yearly data for 2005–2020
- Removal of aggregated regions
- Sorting and interpolation of country-level time series
- Median imputation for missing observations
- Standardization and transformation of all indicators

### Index Construction
The Economic Security Index is calculated as the average of six standardized indicators. Higher index values correspond to higher economic security.

### Principal Component Analysis
PCA is used to evaluate the internal structure of indicators. The first three components explain approximately 63 percent of total variance and capture dimensions such as:
- Economic development level
- Debt–labour market dynamics
- Investment activity

### Sensitivity Analysis
Robustness testing is performed through:
- Generating random weighting schemes
- Recomputing the index for each weight set
- Correlating results with the baseline index
- Assessing indicator importance through leave-one-out exclusion tests

## Purpose
This repository is intended for academic research, methodological demonstration, policy analysis, and coursework involving composite indicators, PCA, and international economic stability assessment.

## Authors
Kateryna Herasymenko  
Viktoriia Baidala  
Group ZK-32


