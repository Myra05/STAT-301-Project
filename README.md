# Predicting Airbnb Prices in European Cities
A statistical analysis project investigating the factors associated with Airbnb listing prices in Budapest, London, and Rome using publicly available listing data.

## Overview
This project explores how listing characteristics, location, and other readily available information can be used to predict Airbnb prices. We developed and evaluated multiple linear regression models using the log-transformed listing price as the response variable.

The analysis compares different variable selection approaches, including forward selection, backward selection, and LASSO regression, to identify a model with strong predictive performance while maintaining interpretability.

## Methods
1. **Data cleaning & wrangling**
   - Processed Airbnb listing data from Budapest, London, and Rome
   - Removed redundant and highly correlated variables
   - Converted categorical variables to appropriate factors

2. **Exploratory data analysis**
   - Examined price distributions and relationships between predictors
   - Used geospatial visualizations to explore listings across cities
   - Applied a log transformation to listing price to reduce right skewness

3. **Model development**
   - Built multiple linear regression models using `log(realSum)` as the response
   - Compared forward and backward selection using AIC
   - Applied LASSO regression for variable selection and regularization

4. **Model evaluation**
   - Used a 70/30 train-test split
   - Applied 10-fold cross-validation to compare models
   - Evaluated predictive performance using RMSE and $R^2$
   - Checked linear regression assumptions and multicollinearity

## Key Findings
- The final model achieved an **$R^2$ of 0.6394** and an **RMSE of 0.352** on the test set using the log(price) scale.
- Forward and backward selection produced the same model, with backward selection achieving the lowest average cross-validation RMSE.
- The selected model explained approximately **64% of the variation in log listing prices** on unseen data.
- The log transformation substantially improved the suitability of linear regression by reducing the strong right skew in listing prices.
- Prediction accuracy was limited by factors not captured in the dataset, such as sponsorship, marketability, amenities, and other characteristics of individual listings.

## Tools & Technologies
- R
- tidyverse
- ggplot2
- tidymodels
- MASS
- glmnet
- Multiple Linear Regression
- LASSO Regression
- Cross-Validation
- Exploratory Data Analysis

## Dataset
The dataset contains Airbnb listings from three European cities:
- Budapest
- London
- Rome

Variables include listing price, room type, person capacity, host characteristics, cleanliness and guest satisfaction ratings, location, and other listing-level characteristics.

## Authors
**Group 16 — UBC STAT 301**
Aidan Meharg · Myra Tyagi · Nathan Zhang · Zhihan Dong

