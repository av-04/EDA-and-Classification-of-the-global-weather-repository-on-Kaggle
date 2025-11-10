# ☁️ Global Weather Repository Data Science Analysis

## Project Overview

This repository documents a comprehensive data science analysis of the **Global Weather Repository** dataset (sourced from Kaggle). The project demonstrates proficiency in foundational data science skills, including robust data cleaning, detailed Exploratory Data Analysis (EDA), advanced anomaly detection, spatial analysis, and time series forecasting.

---

## 🎯 Objectives

1.  **Data Quality:** Implement data cleaning techniques (handling outliers, normalization) to prepare the data for modeling.
2.  **EDA & Pattern Discovery:** Uncover geographical patterns, temporal trends, correlations, and feature distributions.
3.  **Basic Forecasting:** Build and evaluate a time series model for predicting global average temperature.

---

## 🛠️ Analysis Steps and Key Findings

### 1. Data Cleaning & Preprocessing

| Step | Details |
| :--- | :--- |
| **Missing Data** | The dataset was found to be **100% complete** (no missing values). |
| **Outlier Handling** | Outliers in temperature and precipitation were identified using the **IQR method** and corrected via **clipping**. |
| **Normalization** | Key numerical features were scaled using **Min-Max Scaling** to the $[0, 1]$ range for effective model training. |

### 2. Exploratory Data Analysis (EDA)

| Analysis Type | Key Findings |
| :--- | :--- |
| **Time Series Trends** | **Temperature** shows a clear **seasonal cycle** over the analysis period. |
| **Correlation** | Moderate **negative correlation** ($\mathbf{-0.45}$) between $\mathbf{\text{temperature\_celsius}}$ and $\mathbf{\text{humidity}}$. |
| **Distribution** | **Humidity** exhibits a **bimodal** distribution, representing a mix of dry/moderate and highly humid climates. |
| **Spatial Analysis** | **Temperature** follows a strong **zonal pattern** (decreasing from the Equator). **Precipitation** is clustered in tropical and coastal areas. |

### 3. Anomaly Detection (Isolation Forest)

* The **Isolation Forest** model identified **extreme weather events** as the primary type of multi-dimensional outlier.
* Anomalous records were characterized by extreme feature combinations: **high wind speeds, heavy precipitation, and low atmospheric pressure**.

### 4. Time Series Forecasting (SARIMA)

A **SARIMA** (Seasonal AutoRegressive Integrated Moving Average) model was used to forecast the **Global Daily Average Temperature**.

| Metric | Value | Interpretation |
| :--- | :--- | :--- |
| **Mean Absolute Error (MAE)** | $4.25^\circ\text{C}$ | The average magnitude of the forecast error. |
| **Root Mean Squared Error (RMSE)** | $5.09^\circ\text{C}$ | The typical prediction error, indicating a reasonable baseline performance for a complex global time series. |

---

## 📂 Repository Structure

| File/Folder | Description |
| :--- | :--- |
| `GlobalWeatherRepository.csv` | The original dataset used for all analyses. |
| `global_weather_trends.png` | Visualization of global daily average temperature and precipitation time series. |
| `correlation_heatmap.png` | Heatmap illustrating relationships between core weather features. |
| `basic_forecasting_model.png` | Plot comparing the SARIMA forecast against the actual test data. |
| `spatial_analysis_weather.png` | Geographical plots of average temperature and precipitation. |
| ... | Other intermediate files and plots generated during the analysis. |
