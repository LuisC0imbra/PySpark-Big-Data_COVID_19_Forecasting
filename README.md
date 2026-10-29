# COVID-19 Global Forecasting - Big Data Analysis

### Academic Big Data Project | Python | PySpark | Time Series Forecasting | Machine Learning

## Project Overview

This project was developed as part of the **Big Data** course and focuses on analyzing and forecasting the global evolution of COVID-19 using Python and Apache Spark.

The main objective was to explore historical COVID-19 data, understand the progression of confirmed cases and fatalities across different countries, and apply statistical forecasting and machine learning techniques to estimate future trends.

The project is divided into three main components:

1. **Exploratory Data Analysis (EDA)** - Understanding global COVID-19 trends and geographical differences.
2. **Time Series Forecasting** - Applying statistical forecasting models to predict confirmed cases and fatalities.
3. **Big Data and Machine Learning with PySpark** - Exploring distributed data processing and regression-based prediction models.

The analysis combines traditional Python data science libraries with Apache Spark to explore different approaches to handling and modeling time-dependent data.

## Dataset

The project uses the **COVID-19 Global Forecasting (Week 3)** dataset from a Kaggle forecasting competition.

The dataset contains historical COVID-19 information for countries and regions worldwide, including confirmed cases and reported fatalities.

| Dataset | Description |
|---|---|
| `train.csv` | Historical COVID-19 observations used for analysis and model development |
| `test.csv` | Country, region, and date combinations requiring predictions |
| `submission.csv` | Competition submission-format data |

The main variables include:

- `Country_Region` - Country associated with each observation.
- `Province_State` - State or province, where applicable.
- `Date` - Observation date.
- `ConfirmedCases` - Cumulative number of confirmed COVID-19 cases.
- `Fatalities` - Cumulative number of reported deaths.

**Important:** Confirmed cases and fatalities are cumulative values. Daily new cases and deaths must be calculated from differences between consecutive observations rather than by summing cumulative records across dates.

## Project Objectives

- Analyze the global distribution and progression of COVID-19.
- Identify countries with the highest and lowest reported cases and fatalities.
- Calculate daily new cases and deaths from cumulative observations.
- Visualize historical trends and compare countries.
- Develop time series forecasting models for confirmed cases and fatalities.
- Explore forecast residuals and model behavior.
- Apply Apache Spark for distributed data analysis.
- Implement regression-based machine learning models using PySpark.
- Compare different approaches to predicting COVID-19 trends.

## Methodology

### 1. Exploratory Data Analysis

The first stage focuses on understanding the dataset and identifying patterns in the historical evolution of COVID-19.

The analysis includes:

- Dataset structure, quality, and descriptive statistics.
- Number of countries and observation dates.
- Global confirmed cases and fatalities.
- Daily new cases and deaths.
- Top 10 countries by confirmed cases and fatalities.
- Countries with the fewest reported cases and fatalities.
- Cumulative case trends.
- Country-level comparisons, including Portugal.
- Relationships between confirmed cases and fatalities.

This stage uses Pandas and visualization libraries to transform raw data into interpretable insights.

### 2. Time Series Forecasting

The second stage explores statistical forecasting methods to estimate the evolution of confirmed cases and fatalities.

The notebook uses **StatsForecast** and examines three forecasting approaches.

**Naive Forecasting**

Uses the most recent observation as the forecast for future periods. It provides a simple baseline against which other methods can be compared.

**Seasonal Naive Forecasting**

Uses historical observations from corresponding seasonal periods to estimate future values.

**AutoARIMA**

Automatically searches for an appropriate ARIMA model configuration to represent patterns in the time series.

Forecasting is explored for several countries, including:

- China
- United States
- Italy
- Spain
- Germany
- France
- Iran
- United Kingdom
- South Korea
- Switzerland
- Portugal

The analysis covers both confirmed cases and fatalities, with a forecasting horizon of **90 days**.

**Forecast Residual Analysis**

Residuals are examined to understand the differences between model predictions and observed historical values, helping identify potential forecasting limitations.

### 3. Big Data Analysis with PySpark

The third stage introduces **Apache Spark**, using PySpark to process and analyze COVID-19 data.

The analysis revisits several exploratory tasks in a distributed data processing environment, including:

- Loading and inspecting training and test datasets.
- Counting countries and dates.
- Aggregating confirmed cases and fatalities.
- Identifying countries with the highest and lowest reported values.
- Creating a previous-observation forecasting baseline.

This stage demonstrates how analytical operations can be expressed using Spark DataFrames.

### 4. Machine Learning with PySpark

The project also explores regression-based machine learning models using Spark MLlib.

| Model | Purpose |
|---|---|
| Linear Regression | Model relationships between input features and numerical targets |
| Random Forest Regression | Explore nonlinear relationships using an ensemble of decision trees |
| Decision Tree Regression | Generate predictions using rule-based splits |
| Naive Baseline | Provide a simple reference for prediction behavior |

These methods demonstrate alternative approaches to forecasting numerical outcomes and provide practical experience with machine learning workflows in PySpark.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and exploratory analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Plotly | Interactive visualizations |
| StatsForecast | Time series forecasting |
| Apache Spark / PySpark | Distributed data processing |
| Spark MLlib | Machine learning models |
| Jupyter Notebook | Analysis, experimentation, and documentation |

## Repository Structure

```text
Big-Data-COVID19-Forecasting/
│
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── submission.csv
│
├── notebooks/
│   └── Big_Data_COVID19_Forecasting_English.ipynb
│
└── README.md
```

## How to Run the Project

1. Clone or download the repository.
2. Install the required Python libraries, including Pandas, NumPy, Matplotlib, Seaborn, Plotly, StatsForecast, and PySpark.
3. Ensure the CSV files are available inside the `data/` directory.
4. Open the notebook located in `notebooks/`.
5. Run the cells sequentially, starting with the exploratory analysis.
6. Review the forecasting and PySpark machine learning sections.

The notebook uses relative paths such as `../data/train.csv`, so it should be executed with the notebook directory as the working directory.

**Execution note:** The code has been reviewed and corrected in several sections, but the complete notebook has not yet been executed and validated end-to-end in the updated environment. Some forecasting and Spark dependencies may require compatible library versions.

## Key Learning Outcomes

This project provided practical experience in several areas of Data Science and Big Data:

- Processing and analyzing time-dependent datasets.
- Understanding cumulative versus daily observations.
- Developing and interpreting time series forecasts.
- Exploring statistical forecasting models and residuals.
- Using PySpark DataFrames for analytical operations.
- Applying machine learning regression models with Spark MLlib.
- Working with country-level historical data.
- Understanding the challenges of forecasting during rapidly changing events.

## Limitations

COVID-19 forecasting presents significant challenges because reported cases and fatalities depend on factors such as testing policies, reporting practices, interventions, and changes in disease transmission.

The models explored in this project are academic implementations and should not be interpreted as reliable real-world epidemiological predictions.

Additionally, model comparisons require consistent validation procedures and appropriate forecasting metrics before conclusions can be drawn about predictive accuracy.

## Academic Information

| Field | Details |
|---|---|
| Course | Big Data |
| Project Type | Academic Data Science Project |
| Main Focus | COVID-19 Analysis and Forecasting |
| Author | Luís Coimbra |
| Programming Language | Python |
| Main Framework | Apache Spark / PySpark |

## Skills Demonstrated

- Big Data Analytics
- Exploratory Data Analysis (EDA)
- Time Series Analysis
- Statistical Forecasting
- ARIMA Modeling
- Data Visualization
- PySpark DataFrames
- Spark MLlib
- Linear Regression
- Random Forest Regression
- Decision Tree Regression
- Python Programming

## Final Considerations

This project combines statistical forecasting, machine learning, and distributed data processing to explore different ways of analyzing historical COVID-19 data.

It provided an opportunity to move beyond traditional Pandas-based analysis and gain practical experience with **Apache Spark and PySpark**, while also developing a stronger understanding of time series forecasting and predictive modeling.

The project represents part of my academic foundation in Data Science and Big Data, supporting my continued development in **Data Engineering, Machine Learning, and AI**.
