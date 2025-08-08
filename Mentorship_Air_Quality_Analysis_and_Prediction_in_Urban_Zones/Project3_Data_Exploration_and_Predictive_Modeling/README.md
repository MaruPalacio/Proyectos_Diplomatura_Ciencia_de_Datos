# 🌎 Air Quality Analysis and Prediction in an Urban Area: Multisensor Data Exploration and Predictive Modeling


* **Diploma:** Diploma in Data Science, Machine Learning and Applications
* **Project Assignment:** #3 - Supervised and Unsupervised Learning


## Project Overview

Air quality is a critical topic on the global environmental health agenda. According to the WHO (2018), atmospheric pollutants are responsible for 1 in 9 deaths worldwide. However, many parts of the world lack basic air quality data.

This dataset contains responses from a multisensor gas device installed in a highly polluted area in Italy. The objective is to examine how environmental factors and pollutant concentrations interact, which will allow us to understand the urban area's pollution level and use data science to inform environmental health strategies and project recommendations to improve air quality and protect residents' health.

The data was obtained from: [UCI Air Quality Dataset](https://archive.ics.uci.edu/dataset/360/air+quality)

To download the dataset, access this repository:
[GitHub - AirQualityUCI.csv](https://github.com/PatriMiranda/Calidad-de-Aire/blob/main/AirQualityUCI.csv)

---

## Objective of Project #3

In this third project on supervised and/or unsupervised learning, we apply classification, regression, decision tree models, or more advanced machine learning models such as XGBoost, LightGBM, or any other considered model. The goal is to extract the most relevant and meaningful insights presented by the dataset.

The purpose is to evaluate and compare different models to determine which provide the best accuracy and predictive power relative to the initially posed questions. Through this analysis, we aim to propose effective actions to mitigate public health and environmental impacts related to air pollution.

---

## Dataset Description

* **Rows:** 9471
* **Columns:** 17
* **Content:** Hourly averages of sensor responses and gas concentrations obtained by a certified analyzer with metal oxide chemical sensors (PT08.S1, S2, S3, S4, S5) over one year (March 2004 - April 2005).
* **Missing Data:** Encoded as -200.

---

## Variables to Analyze

* **Date:** (DD/MM/YYYY)
* **Time:** (HH.MM.SS)
* **CO (GT):** Hourly average real concentration of CO in mg/m³ (reference analyzer)
* **PT08.S1 (Tin oxide):** Hourly average sensor response (nominally targeting CO)
* **NMHC (GT):** Hourly average total non-methane hydrocarbons in µg/m³ (reference analyzer)
* **C6H6 (GT):** Hourly average benzene concentration in µg/m³ (reference analyzer)
* **PT08.S2 (Titania):** Hourly average sensor response (targeting NMHC)
* **NOx (GT):** Hourly average NOx concentration in ppb (reference analyzer)
* **PT08.S3 (Tungsten oxide):** Hourly average sensor response (targeting NOx)
* **NO2 (GT):** Hourly average NO2 concentration in µg/m³ (reference analyzer)
* **PT08.S4 (Tungsten oxide):** Hourly average sensor response (targeting NO2)
* **PT08.S5 (Indium oxide):** Hourly average sensor response (targeting O3)
* **T:** Temperature (°C)
* **HR:** Relative Humidity (%)
* **AH:** Absolute Humidity

---

## Questions to Address in Project #3

1. **Which predictive model offers the best fit to predict pollutant concentrations based on environmental factors and/or sensor responses?**

   * Models to apply: Multiple linear regression, Ridge, Lasso, Random Forest, Gradient Boosting, XGBoost, LightGBM, PCA, clustering, neural networks, etc.

2. **What factors most influence pollutant concentrations (CO, NO2, NOx)?**

   * Identify variables with the highest impact, e.g., temperature, humidity, sensor responses.

3. **How to predict pollutant concentrations (CO, NO2, NOx, C6H6) based on environmental and sensor variables?**

   * Identify models for prediction such as Linear Regression, XGBoost, LightGBM.

4. **What environmental conditions precede high pollutant levels (CO, NO2, NOx, C6H6)?**

   * Identify environmental variables most related to pollutants using Random Forest, Gradient Boosting.

5. **Can air quality be predicted based on pollutant concentrations and environmental conditions?**

   * Use classification models like neural networks, random forest, PCA, alongside regression models.

---

## General Conclusions

1. **Best Models & Metrics:** Decision tree-based models consistently showed the best metrics for all pollutants analyzed, capturing data relationships more effectively.
2. **Time Series:** Benzene showed the best metrics, aligning with feature importance results from decision tree models.
3. **Human Impact:** Environmental variables showed low impact on pollutant concentrations, suggesting pollutant levels are mainly explained by human activities (traffic, factories, etc.) in the studied city.
4. **Overfitting Tendency:** Models show potential but tend to overfit, which may be mitigated by more data and expert domain consultation.

---

## Best Model Results for Each Pollutant

| Pollutant | Model           | R2       | MAE      | RMSE     |
| --------- | --------------- | -------- | -------- | -------- |
| CO        | LightGBM\_Hyper | 0.962864 | 0.119678 | 0.184711 |
| C6H6      | XGBoost\_Hyper  | 0.987646 | 0.074713 | 0.108374 |
| NO2       | LightGBM\_Hyper | 0.945469 | 0.154374 | 0.22604  |
| NOx       | LightGBM\_Hyper | 0.962408 | 0.11337  | 0.182087 |



