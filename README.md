
# BLS Tech Salary Dataset – Exploratory Data Analysis (EDA)

## Project Overview

This notebook is part of the **DS606 Capstone Project** for Summer 2025. The objective of this phase is to perform comprehensive exploratory data analysis (EDA) on the **Occupational Employment and Wage Statistics (OEWS)** dataset provided by the U.S. Bureau of Labor Statistics (BLS). The ultimate goal of the capstone project is to build machine learning models that can predict tech-sector salaries based on job title, region, and industry.

## Dataset Summary

- **Source**: U.S. Bureau of Labor Statistics (BLS)  
- **Dataset**: Occupational Employment and Wage Statistics (OEWS)  
- **File**: `all_data_M_2024.xlsx`  
- **Size**: ~400,000 records, 32 columns  
- **Coverage**: All U.S. states, metro areas, and major occupations

Key columns used in this notebook include:
- `OCC_CODE`, `OCC_TITLE` – Standard Occupational Classification code and title
- `AREA_TITLE` – Region (e.g., state or metropolitan area)
- `NAICS_TITLE` – Industry classification
- `TOT_EMP` – Estimated total employment
- `A_MEDIAN`, `A_MEAN` – Annual median and mean wage

## Notebook Objectives

1. **Load and inspect** the raw Excel dataset
2. **Understand the structure** and coding system of `OCC_CODE` (SOC system)
3. **Clean the data** by removing:
   - Aggregate/suppressed rows (e.g., “All Occupations”)
   - Non-U.S. areas
   - Rows with missing or zero salary values
4. **Filter for relevant tech roles** using SOC major groups (e.g., `15-` prefix)
5. **Generate summary statistics and visualizations** to explore:
   - Regional differences in salary
   - Distribution of employment across tech roles
   - Relationship between employment size and wage
   - Industry-specific trends

## EDA Highlights

- Classification of SOC major groups and mapping to tech-related occupations
- Boxplots and bar charts comparing salary by occupation and region
- Log-scaled plots visualizing employment vs. wage dynamics
- Outlier detection in salary and employment figures
- Heatmaps and correlation matrices for selected features

## Status & Next Steps

This notebook completes the **EDA portion** of the project. Cleaned and transformed data from this analysis will be used to build regression models in the next notebook. Planned features for modeling include:

- Encoded occupation and region names
- Employment figures as numerical features
- Industry classifications (one-hot encoded or grouped)
- Median or mean salary as target variable

Modeling approaches will include:
- Linear Regression
- Random Forest Regressor
- XGBoost

## Tools & Environment

- Python 3.11  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Jupyter Notebook
