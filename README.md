# Air-Quality-Across-India-AQI-Analytics-Dashboard
To comprehensively clean, analyze, and visualize multi-year urban air quality data across India to uncover pollution trends, identify primary toxic contributors, and evaluate environmental health risks.

An end-to-end data analytics and machine learning workflow designed to evaluate, clean, analyze, and extract deep environmental insights from daily air quality records across major metropolitan areas in India.

---

## 📌 Project Overview
Air pollution is a critical public health and environmental challenge. This project leverages historical daily air quality logs (2015–2020) to audit data integrity, handle severe missingness anomalies, engineer temporal features, and identify key pollution drivers, heavy pollutant hotspots, and seasonal trends across urban India.

---

## 🚀 Key Features & Pipeline Steps
* **Data Quality Assessment (DQA):** Audited raw datasets containing nearly 30,000 records for structural anomalies, missing values (such as Xylene and PM10), incorrect data types, and duplicate rows.
* **Data Cleaning & Imputation:** Implemented group-wise imputation strategies and standardized date and categorical fields.
* **Feature Engineering:** Extracted temporal attributes (Year, Month, Day of Week, and Indian Seasons) and programmatically mapped values to official Central Pollution Control Board (CPCB) air quality health buckets.
* **Exploratory Data Analysis (EDA):** Uncovered patterns in particulate matter concentration ($PM_{2.5}$, $PM_{10}$), gaseous pollutants ($CO, NO_2, SO_2$), and calculated multivariate correlation matrices to isolate primary toxicity drivers.
* **Advanced Aggregations:** Grouped metrics by city and season to highlight urban disparities and seasonal pollution peaks.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation & Analysis:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn

---

## 📂 Repository Structure
```text
├── data/                                 # Raw and cleaned datasets (e.g., cleaned_city_day_air_quality.csv)
├── notebooks/                            # Jupyter notebooks containing the analytics and dashboard pipeline
├── README.md                             # Project documentation
└── requirements.txt                      # Python dependencies
