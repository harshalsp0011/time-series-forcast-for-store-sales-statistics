# Time Series Forecast & Statistical Analysis 📊📈

**A collection of advanced R-based statistical projects focusing on Time Series Forecasting, Principal Component Analysis (PCA), and Machine Learning Clustering.**

![R](https://img.shields.io/badge/Language-R-blue) ![Forecasting](https://img.shields.io/badge/Task-Time_Series_Forecasting-green) ![Clustering](https://img.shields.io/badge/Task-Clustering_%26_PCA-orange)

---

## 📂 Repository Contents

This repository is divided into two major statistical phases:

1.  **Project 1: Obesity Data Analysis** (Multivariate Analysis, PCA, K-Means Clustering)
2.  **Project 2: Time Series Forecasting** (ETS, Holt-Winters, ARIMA modeling on Oil Prices)

---

## 🧬 Project 1: Obesity Data Analysis (Clustering)

**Location:** `/P1`

### 📝 Overview
This project explores a dataset of 2,111 individuals to identify patterns in obesity levels based on lifestyle habits (exercise, diet) and physical characteristics. The goal was to reduce dimensionality and segregate individuals into distinct health profiles.

### 🔑 Key Techniques
* **Data Cleaning:** Implemented IQR-based outlier capping for robust analysis.
* **Exploratory Data Analysis (EDA):** Correlation matrices and boxplots to understand variable relationships (e.g., Height vs. Weight).
* **Principal Component Analysis (PCA):** Reduced 8 standardized numeric variables into principal components. **PC1 and PC2 explained ~41% of the variance**, effectively summarizing the data.
* **K-Means Clustering:** Used the **Elbow Method** to determine the optimal number of clusters ($k=3$).
* **Validation:** Assessed cluster quality using **Silhouette Scores** (Avg Width: 0.38).

### 📊 Results
* **Cluster 1 (Blue):** Lower values in PC1/PC2 (distinct profile).
* **Cluster 2 (Yellow):** Intermediate profile.
* **Cluster 3 (Gray):** Higher values in PC1, indicating higher weight/height metrics.

---

## 📉 Project 2: Time Series Forecasting (Oil Prices)

**Location:** `/p2`

### 📝 Overview
This phase focuses on forecasting Daily Oil Prices, a critical external factor often used in Store Sales forecasting. The analysis involves handling missing data, detecting trends, and comparing multiple statistical forecasting models.

### 🔑 Key Techniques
* **Imputation:** Used **Linear Interpolation** to fill missing time-series data while preserving trends.
* **Trend & Seasonality Analysis:** Detected a clear downward trend (2014–2016) with no significant seasonality.
* **Modeling:**
    * **ETS (Error, Trend, Seasonality):** Specifically **Holt’s Linear Trend Method (ETS A,A,N)**.
    * **Holt-Winters:** Applied for comparison.
    * **ARIMA:** Benchmark model (`auto.arima`).
* **Evaluation:** Models compared using **RMSE** and **AIC**.

### 📊 Results & Recommendation
* **ARIMA(0,1,0):** RMSE: 1.1768 | AIC: 3852.85
* **ETS(A,A,N):** RMSE: 1.1756
* **Conclusion:** The **ETS(A,A,N)** model was selected as the best fit because it explicitly modeled the downward trend and offered slightly better forecast accuracy than ARIMA.

---

## 🛠️ Technologies & Libraries

The projects utilize the following **R** libraries:

| Project | Key Libraries |
| :--- | :--- |
| **Data Manipulation** | `tidyverse`, `dplyr`, `tidyr`, `lubridate`, `readr` |
| **Visualization** | `ggplot2`, `corrplot`, `factoextra` |
| **Modeling** | `forecast`, `cluster`, `tseries`, `imputeTS`, `car` |

---

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/harshalsp0011/time-series-forcast-for-store-sales-statistics.git](https://github.com/harshalsp0011/time-series-forcast-for-store-sales-statistics.git)
    ```

2.  **Open the Projects in RStudio:**
    * For **Obesity Analysis**, open `P1/StatPro.Rmd`.
    * For **Time Series**, open `p2/Stats-ProjectPhase-02/Stats-ProjectPhase-02/code.Rmd`.

3.  **Install Dependencies:**
    Run the following R command to install necessary packages:
    ```r
    install.packages(c("tidyverse", "cluster", "factoextra", "corrplot", "car", "forecast", "tseries", "imputeTS"))
    ```

4.  **Knit the Files:**
    Click the **Knit** button in RStudio to generate the HTML or PDF reports.

---

## 👤 Author

* **Harshal**
* *Statistical Analysis & Data Science Portfolio*
