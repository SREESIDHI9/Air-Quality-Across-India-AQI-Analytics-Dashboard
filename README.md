# Air-Quality-Across-India-AQI-Analytics-Dashboard
An end-to-end data analytics and machine learning workflow designed to evaluate, clean, analyze, and extract deep environmental insights from daily air quality records across major metropolitan areas in India.

---

## 📌 Project Overview
Air pollution is a critical public health and environmental challenge. 
This project performs an end-to-end Exploratory Data Analysis (EDA) on a multi-year urban air quality dataset across India (2015–2020 spanning 29,531 records). It covers data cleaning, statistical analysis, and visualization to understand pollution trends, primary toxic contributors, urban disparities, and seasonal environmental health risks. The analysis is done in Python using Pandas, Matplotlib, and Seaborn.

🎯 Objective

To comprehensively clean, analyze, and visualize multi-year urban air quality data across India to uncover pollution trends, identify primary toxic contributors, and evaluate environmental health risks by:
* Cleaning and validating a large air quality dataset, with handling for severe missingness anomalies (e.g., Xylene and PM10) and standardization.
* Running univariate, bivariate, and multivariate analysis using groupby, pivot tables, crosstabs, and correlation matrices.
* Visualizing particulate concentration, gaseous emissions, seasonal cycles, and city-level disparities.
* Turning the findings into practical recommendations for environmental monitoring and policy.

🗂️ Dataset Description

* Source: India Air Quality Data (Kaggle)
* Size: 29,531 rows × 16 initial columns (expanded to 22 columns after feature engineering)
* Format: CSV
* Content: Daily pollutant metrics including PM2.5, PM10, NO, NO2, NOx, NH3, CO, SO2, O3, Benzene, Toluene, Xylene, AQI, and official CPCB AQI Buckets.
* Coverage: Major metropolitan areas across India from 2015 to 2020.
* Mix of types: Numerical (pollutant concentrations, AQI), categorical (City, AQI Bucket, Season, MonthName, DayOfWeek), and date columns.

🔧 Workflow

1. Data Loading & Initial Overview
Loaded the dataset with Pandas and inspected structural integrity, checking for duplicates and missing value distributions across all parameters.

2. Data Cleaning & Preprocessing
* Column pruning & Formatting: Cast date objects into true datetime format and verified temporal properties.
* Missing values: Investigated high missingness rates (such as Xylene at 61.32% and PM10 at 37.72%) and applied robust group-wise imputation strategies.
* Standardization: Engineered temporal features including Year, Month, Day of Week, and Indian Seasons, and populated missing air quality categories using standard Central Pollution Control Board (CPCB) standards.
* Outliers & Validation: Identified extreme maximum outlier values (such as AQI peaking at 2049.0 and PM2.5 reaching 949.99) which were retained as genuine severe pollution events.

3. Exploratory Data Analysis
The EDA is organized to answer core environmental questions:
* Risk & Distribution: What is the distribution of air quality health buckets across the years?
* Pollutant Drivers: Which gases or particulate matters drive dangerous AQI spikes?
* Seasonal & Temporal Patterns: How do seasons and days of the week impact pollution levels?
* Geographic Disparities: Which cities experience the highest average pollution severity?

4. Visualization
Visualizations using Matplotlib and Seaborn including distribution charts, temporal trends, seasonal breakdowns, correlation heatmaps, and city-wise rankings.

5. Insight Generation
Every analysis step is paired with written evidence backed by numbers. Null results or stable patterns (such as uniform day-of-week trends) are reported as findings.

🔍 Key Findings

* Dataset Scale: Analyzed 29,531 daily records across major Indian metropolitan areas from 2015 to 2020.
* General Air Condition: Satisfactory (35.06%) and Moderate (33.32%) conditions make up the majority of daily records, though severe pollution events occur regularly.
* Primary Pollutant Drivers: Carbon Monoxide (CO with r = 0.66) and Fine Particulate Matter (PM2.5 with r = 0.65) share the strongest linear correlation with overall AQI spikes.
* Urban Disparities: Ahmedabad recorded the highest average AQI (approx. 422.6), followed by Delhi, Patna, Gurugram, and Lucknow.
* Seasonal Cycles: Winter and Post-Monsoon periods experience the highest pollution severity (average AQI exceeding 205–213), whereas Monsoon seasons provide substantial cleansing relief (average AQI dropping to 121.28).
* Weekly Trends: Pollution levels remain remarkably uniform across all days of the week, indicating constant structural emission patterns rather than weekend/weekday swings.

💡 Business & Policy Recommendations

* Target High-Risk Winter Windows: Implement aggressive, pre-emptive emission controls and stubble-burning mitigation strategies well ahead of the winter and post-monsoon seasons when AQI severely spikes.
* Prioritize Urban Hotspot Interventions: Focus strict regulatory enforcement and industrial emission caps on severely impacted cities like Ahmedabad, Delhi, Patna, Gurugram, and Lucknow.
* Focus on Particulate Mitigation: Because PM2.5, PM10, and CO are the core drivers of hazardous air quality, policy frameworks should prioritize reducing vehicle exhaust and localized dust sources.
* Enhance Sensor and Data Infrastructure: Address high data missingness in secondary pollutants (like Xylene) through upgraded monitoring equipment and continuous sensor maintenance.

🛠️ Tools & Technologies

* Language: Python
* Libraries: Pandas, NumPy, Matplotlib, Seaborn
* Environment: Jupyter Notebook
* Version Control: Git & GitHub

▶️ How to Run

1. Clone the repository.
2. Install the libraries: pip install pandas numpy matplotlib seaborn jupyter
3. Open the notebook in the notebook/ folder.
4. Ensure the CSV path in the data-loading cell points to your cleaned dataset file.
5. Run Kernel → Restart & Run All.


## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation & Analysis:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn

---

## 📂 Repository Structure
```text

├── notebooks/
│   └── Air Quality Across India & AQI Analytics Dashboard.ipynb  # full analysis notebook  # Jupyter notebooks containing the analytics and dashboard pipeline
├── README.md
├── Raw Data/         # Raw datasets
├── Data Cleaning/                     # cleaned and processed dataset 
    └── cleaned_city_day_air_quality.csv                       

---
