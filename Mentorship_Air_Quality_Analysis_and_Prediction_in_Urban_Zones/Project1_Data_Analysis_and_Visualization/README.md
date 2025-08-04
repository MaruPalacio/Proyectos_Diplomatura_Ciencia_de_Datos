# 🌍 Air Quality Analysis and Prediction in an Urban Area

**Certificate in Data Science, Machine Learning and its Applications**
**Project #1: Data Analysis and Visualization**

---

## 📌 Project Overview

Air quality is a critical public health concern worldwide. According to the World Health Organization (WHO, 2018), air pollution is responsible for 1 in every 9 deaths. Despite this, many regions still lack access to comprehensive air quality data.

This project focuses on exploring and visualizing air quality data collected from a gas multisensor device installed in a highly polluted urban area in Italy. The objective is to analyze the interaction between environmental factors and pollutant concentrations, uncover trends, identify anomalies, and provide insights that may contribute to the development of strategies for environmental health protection.

---

## 📊 Dataset Description

The dataset was obtained from the UCI Machine Learning Repository:
🔗 [Air Quality Dataset – UCI Repository](https://archive.ics.uci.edu/dataset/360/air+quality)

It contains **9,471 rows** and **17 columns**, representing **hourly averages** of gas concentrations and sensor responses recorded between **March 2004 and April 2005**. The measurements were taken using a certified analyzer with metal oxide chemical sensors (PT08.S1 to PT08.S5).

📁 Dataset for analysis:
🔗 [GitHub - CSV File](https://github.com/PatriMiranda/Calidad-de-Aire/blob/main/AirQualityUCI.csv)

📝 **Note:** Missing values are coded as `-200`.

---

## 📌 Features in the Dataset

| Variable        | Description                                                 |
| --------------- | ----------------------------------------------------------- |
| `Date`          | Date (DD/MM/YYYY)                                           |
| `Time`          | Time (HH.MM.SS)                                             |
| `CO(GT)`        | True CO concentration (mg/m³) - reference analyzer          |
| `PT08.S1(CO)`   | Sensor response (tin oxide, nominally targeted at CO)       |
| `NMHC(GT)`      | True non-methane hydrocarbon concentration (µg/m³)          |
| `C6H6(GT)`      | True benzene concentration (µg/m³)                          |
| `PT08.S2(NMHC)` | Sensor response (titania, nominally targeted at NMHC)       |
| `NOx(GT)`       | True NOx concentration (ppb)                                |
| `PT08.S3(NOx)`  | Sensor response (tungsten oxide, nominally targeted at NOx) |
| `NO2(GT)`       | True NO2 concentration (µg/m³)                              |
| `PT08.S4(NO2)`  | Sensor response (tungsten oxide, nominally targeted at NO2) |
| `PT08.S5(O3)`   | Sensor response (indium oxide, nominally targeted at O3)    |
| `T`             | Temperature (°C)                                            |
| `RH`            | Relative Humidity (%)                                       |
| `AH`            | Absolute Humidity                                           |

---

## ❓ Questions Explored in This Project

* What are the **minimum and maximum** values of each pollutant?
* How do pollutant concentrations **vary throughout the day**?
* What is the **distribution** of each pollutant, and are there **anomalous values** that could impact the analysis?

---

## 📈 Goals

* Perform **data cleaning** and handle missing values appropriately.
* Create **visualizations** to analyze temporal and statistical patterns of pollutants.
* Understand sensor behavior and pollutant interactions.
* Generate actionable insights to inform environmental policies and **health protection strategies**.

---

## ⚙️ Tools Used

* Python (Pandas, NumPy, Matplotlib, Seaborn)
* Jupyter Notebook, GoogleColab

---

## 📬 Contributions

Developed as part of the Certificate in Data Science, Machine Learning and its Applications.

Authors: Mariel Palacio, Alejandro Bringas, Lautaro Cabrera, Juan Carlos Recarey

---

## 📁 **Files**:

* `EN_Project1_Data_Analysis_and_Visualization.ipynb`: Notebook - English version.
* `ES_Project1_Data_Analysis_and_Visualization.ipynb`: Notebook - Spanish version.
* `ES_Presentation_Project1_Data_Analysis_and_Visualization.pptx`: Presentation - Spanish version.


