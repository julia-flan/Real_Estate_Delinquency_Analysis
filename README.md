# Real Estate Delinquency Analysis

## About 

This project aims to predict whether a taxpayer will be delinquent on their Real Estate tax, given their property characteristics, property assessments, and past delinquency characteristics using classification algorithms such as Decision trees, Random Forest, and XGBoost. 

 

## Table of Contents 
- Required Libraries 
- Data Source 
- Data Preprocessing 
- Data Exploration 
- Modeling 

## Required libraries 

```python
pip install requests 
pip install json 
pip install pandas 
pip install numpy 
pip install matplotlib.pyplot  
pip install seaborn 
pip install scikit-learn 
pip install xgboost 
```
 

## Data Source 

The data used in this project comes from OpenDataPhilly, an online repository containing datasets, visualizations, and APIs related to the Philadelphia region. The datasets used in this analysis are supported by the City of Philadelphia’s Office of Property Assessments and Department of Revenue. The [Properties and Assessment History]( https://opendataphilly.org/datasets/philadelphia-properties-and-assessment-history/) datasets are available for download or request via API. 

Disaggregated information on Real Estate Tax Balances was requested by the Department of Revenue as it is not available on OpenDataPhilly. To access this information, please submit a request to the Department of Revenue. 

 

## Data Preprocessing 

This script queries the OpenDataPhilly API, reads in the Tax Balances dataset, and cleans the Property, Assessment History, and Tax Balances dataset to ensure that no null values exists and features are appropriately scaled. Then, the datasets are joined and additional features are engineered. 

**Inputs**: 
- Tax Balances dataset 

**Return**: 
- Real_estate_2020_2024.csv: Cleaned dataset with one record for every property assessment for years 2020 to 2024. Data contains both the independent and dependent variable for this analysis. 

- X_real_estate_2025: Cleaned dataset with one record for every property assessment for the year 2025. Data contains the independent variable for this analysis. Tax Balance for 2025 will not be available until December 31, 2025. 

 

## Data Exploration 

This script generates descriptive graphs to better understand the variables in this analysis. 

**Inputs:** 
- real_estate_2020_2024.csv 

**Return:** 
- None  

## Modeling 

This script runs hyperparameter tuned Decision Tree, Random Forest, and XGBoost models to predict whether a given property will have a Real Estate Tax Balance at the end of the given year. 

**Inputs:**: 
- real_estate_2020_2024.csv 

**Return:** 
- None 

 

 