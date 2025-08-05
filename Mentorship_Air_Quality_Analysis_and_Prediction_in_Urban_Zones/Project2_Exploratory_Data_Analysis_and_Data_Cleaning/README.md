# 🌎Air Quality Analysis and Prediction in an Urban Area: Multisensor Data Exploration and Predictive Modeling

##Certificate in Data Science, Machine Learning, and its Applications

### Project #2: Exploratory Data Analysis and Data Cleaning 

---

### Overview

Air quality is a critical topic on the global environmental health agenda. According to the World Health Organization (WHO, 2018), air pollutants contribute to 1 in every 9 deaths worldwide. Despite this, many regions lack fundamental air quality data.

This project uses data collected from a gas multisensor device installed in a heavily polluted urban area in Italy. The objective is to explore how environmental factors interact with pollutant concentrations, helping us better understand pollution levels and apply data science techniques to inform strategies for environmental health improvements and public safety.

The dataset was obtained from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/360/air+quality).

---

### Dataset Description

* **Rows:** 9,471
* **Columns:** 17
* **Data span:** March 2004 to April 2005 (hourly averages)
* **Sensors:** Metal oxide chemical sensors (PT08.S1, S2, S3, S4, S5)
* **Missing Data:** Marked as -200

---

### Variables Analyzed

| Variable                    | Description                                                 |
| --------------------------- | ----------------------------------------------------------- |
| Date                        | Date (DD/MM/YYYY)                                           |
| Time                        | Time (HH.MM.SS)                                             |
| CO (GT)                     | Carbon Monoxide concentration in mg/m³ (reference analyzer) |
| PT08.S1 (tin oxide)         | Sensor response nominally targeting CO                      |
| NMHC (GT)                   | Non-methane hydrocarbon concentration in µg/m³ (reference)  |
| C6H6 (GT) (Benzene)         | Benzene concentration in µg/m³ (reference)                  |
| PT08.S2 (titania)           | Sensor response nominally targeting NMHC                    |
| NOx (GT) (Nitrogen Oxides)  | NOx concentration in ppb (reference)                        |
| PT08.S3 (tungsten oxide)    | Sensor response nominally targeting NOx                     |
| NO2 (GT) (Nitrogen Dioxide) | NO2 concentration in µg/m³ (reference)                      |
| PT08.S4 (tungsten oxide)    | Sensor response nominally targeting NO2                     |
| PT08.S5 (indium oxide)      | Sensor response nominally targeting O3                      |
| T                           | Temperature in °C                                           |
| RH                          | Relative Humidity (%)                                       |
| AH                          | Absolute Humidity                                           |

---

### 🎯Key Questions Addressed

1. Are the sensors used in the study specifically associated with the measurement of particular pollutants?

2. Is there a relationship between environmental conditions and the concentration of the analyzed pollutants?

3. Is there a significant correlation between the concentrations of CO, C6H6, NMHC, NOx, and NO2, and the responses of the gas sensors S1, S2, S3, S4, and S5?

---

### 🧹Data Cleaning Considerations

Before answering the questions above, the following points are crucial for cleaning and preparing the data for further modeling (Project #3):

* Handling of missing data: Should we use zero, mean, median, or mode imputation?
* Treatment of outliers: What strategy will be adopted?
* Variable selection: Which variables will be chosen for subsequent analysis and based on what criteria?
* New feature creation: Will we add new calculated columns? If so, will they be combinations of existing variables or incorporate external data (e.g., air pollution indices, health data, traffic flow)?

---

## 💡Conclusions and Insights

### 1. Correlation Analysis Insights

The analysis reveals that sensors are **not exclusively related to their specific target pollutants**. Instead, there are multiple correlations of varying strengths between sensors and pollutants, among pollutants themselves, and even among the sensors.

* **Sensor PT08.S3 (specific to nitrogen oxides)** shows **negative correlations** with nitrogen dioxide and nitric oxide (NO and NOx), which may indicate possible malfunction or calibration issues.
* There are **no significant negative correlations** between pollutants or between pollutants and environmental variables, a factor that could be important for climate-related predictive modeling to understand which variables decrease pollutant levels.
* Generally, sensors correlate with several pollutants, suggesting potential **lack of sensor calibration** or sensor cross-sensitivity.

### 2. Relationship Between Pollutants and Environmental Variables

* **Temperature (T):** Shows very low positive correlation with CO and benzene, but negative correlation with NO2 and NOx.
* **Absolute Humidity (AH):** Exhibits very low positive correlation with CO and benzene, and very low negative correlation with NO2 and NOx.
* **Relative Humidity (RH):** Shows very low positive correlation with CO and NOx, and very low negative correlation with benzene and NO2.

### 3. Sensor-Pollutant Relationship Conclusions

* **PT08.S1 (CO sensor)** effectively measures CO but also correlates strongly with benzene.
* **PT08.S3 (NOx sensor)** shows negative correlations with all pollutants, possibly due to calibration issues.
* **PT08.S4 (NO2 sensor)** correlates more with CO and benzene than with its intended targets.
* **PT08.S5 (O3 sensor)** positively correlates with all pollutants, indicating more general sensitivity.

### 4. Sensor Efficiency

The lack of precise and exclusive positive correlations suggests that some sensors might be **unsuitable for certain pollutants** or require **improved calibration** to function accurately. This insight is crucial when selecting features for predictive modeling and for planning sensor maintenance or upgrades.


---

### Download Dataset

You can download the dataset from the following repository:
[AirQualityUCI.csv](https://github.com/PatriMiranda/Calidad-de-Aire/blob/main/AirQualityUCI.csv)
