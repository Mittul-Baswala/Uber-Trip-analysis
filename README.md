# 🚕 Uber Trip Analysis ML

This project performs an analysis of Uber trip data and develops machine learning models to forecast **hourly trip counts**. The workflow includes data preprocessing, exploratory data analysis (EDA) to identify temporal patterns, and the implementation of three different regression models: **LightGBM, Random Forest, and XGBoost**.

---

## 🚀 Project Overview

The primary goal of this project is to **predict the number of Uber trips** based on time-related features extracted from the timestamp of the trip data.

### 🔑 Key Steps
- **Data Loading & Preprocessing**  
  - Read raw data and convert the date column to proper datetime format.
- **Feature Engineering & Resampling**  
  - Convert daily-level data to hourly intervals.  
  - Extract time-based features: Hour, Day of Week, Month, etc.
- **Exploratory Data Analysis (EDA)**  
  - Visualize temporal patterns (heatmap of trips by hour and day).
- **Model Building**  
  - Train three ensemble models: LightGBM, Random Forest, XGBoost.
- **Model Evaluation & Comparison**  
  - Assess performance using regression metrics (R², MAE, RMSE).

---

## 💾 Dataset

- **File Used:** `Uber-Jan-Feb-FOIL.csv`  
- **Original Columns:**
  - `dispatching_base_number`
  - `date`
  - `active_vehicles`
  - `trips`

The dataset is resampled to an **hourly frequency** and focuses on predicting trip counts based on extracted time features.

---

## 🛠️ Libraries Used

- **Core Libraries**
  - `pandas`
  - `numpy`

- **Visualization**
  - `matplotlib`
  - `seaborn`
  - `plotly.express`

- **Machine Learning & Metrics**
  - `scikit-learn`  
    - `train_test_split`  
    - `mean_absolute_error`  
    - `mean_squared_error`  
    - `r2_score`
  - `lightgbm`
  - `xgboost`

- **Utilities**
  - `glob`

---

## ✨ Analysis & Results

### 1. Trip Pattern Analysis (EDA)
- **Heatmap Visualization** reveals clear hourly and daily demand patterns.
- **Peak Hours:** 4 PM – 8 PM (late afternoon/evening).
- **Peak Days:** Higher demand during weekdays (Monday–Friday).

### 2. Model Performance

| Model          | R² Score | MAE              | RMSE             |
|----------------|----------|------------------|------------------|
| Random Forest  | 1.000    | 0.000000e+00     | 0.000000e+00     |
| LightGBM       | 1.000    | 3.82e-16         | 1.84e-15         |
| XGBoost        | 1.000    | 1.17e-05         | 2.91e-05         |

### 3. Visual Comparison of Forecasts
- Predictions from all three models closely track actual values.  
- Confirms strong performance on this dataset.
