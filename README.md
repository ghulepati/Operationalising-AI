# Operationalising-AI
# Traffic Flow Prediction - Exploratory Data Analysis & Modeling

## Overview
This repository contains the code and documentation for analyzing traffic flow data using time series analysis techniques. The objective is to understand traffic patterns and develop a predictive model for forecasting future traffic flow.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Feature Engineering](#feature-engineering)
- [Predictive Modeling](#predictive-modeling)
- [Results](#results)
- [Future Improvements](#future-improvements)
- [How to Use](#how-to-use)
- [Citations](#citations)

## Introduction
Traffic flow prediction is crucial for urban planning and traffic management. This project explores historical traffic data, performs exploratory data analysis, engineers relevant features, and builds a predictive model using regression techniques.

## Dataset
The dataset consists of traffic flow measurements collected over multiple nodes and time periods. The primary data preprocessing steps include:
- Removing missing values
- Extracting time-based features
- Creating rolling averages and lagged features

## Exploratory Data Analysis (EDA)
EDA was conducted to identify patterns and insights, including:
- **Traffic Flow Over Time**: Identified daily and weekly trends
- **Traffic Distribution**: Skewed distribution with occasional high-traffic periods
- **Heatmap Analysis**: Peak traffic times and weekday/weekend variations
- **Autocorrelation Analysis**: Seasonal patterns detected through ACF and PACF plots

## Feature Engineering
Key features engineered for predictive modeling:
- **Hour of the Day, Day of the Week, Weekend Indicator**
- **24-hour Rolling Mean & 24-hour Lag**
- **Seasonal and Trend Components**
- **Rush Hour & Night Indicators**

## Predictive Modeling
A Ridge Regression model was used due to its ability to handle multicollinearity and prevent overfitting. Time series cross-validation was employed to evaluate model performance.

## Results
Model performance metrics:
- **Mean Absolute Error (MAE)**: 0.4466
- **Root Mean Squared Error (RMSE)**: 0.5396
- **R² Score**: 0.7088
- **Feature Importance**: 24-hour lag, rolling mean, and hour of the day were the most significant predictors.

## Future Improvements
To enhance model accuracy, future iterations could:
- Explore non-linear models (e.g., Random Forests, LSTMs)
- Incorporate external factors like weather, events, and holidays
- Optimize feature selection and engineering

## How to Use
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo-name.git
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the analysis:
   ```sh
   python analysis.py
   ```
4. Train the model:
   ```sh
   python train_model.py
   ```

## Citations
- Zhao, L. (2019). Traffic Flow Forecasting [Dataset]. UCI Machine Learning Repository. [DOI](https://doi.org/10.24432/C57897)
- Perplexity AI (2024). [Perplexity](https://www.perplexity.ai)

---
For any queries, feel free to reach out!

