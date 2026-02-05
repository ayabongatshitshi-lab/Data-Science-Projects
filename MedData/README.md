# Medical Examination Data Visualizer

### Project Overview
This project involves exploring and visualizing medical examination data to uncover relationships between cardiac disease, body measurements, blood markers, and lifestyle choices. I performed data normalization, feature engineering, and complex cleaning to ensure statistical integrity before generating multi-panel categorical plots and correlation heatmaps.

### Key Insights
*   **Feature Engineering:** Successfully implemented an `overweight` indicator based on BMI calculations ($kg/m^2$).
*   **Data Normalization:** Standardized health markers (`cholesterol`, `gluc`) into a binary "Good (0) vs. Bad (1)" format for consistent comparison.
*   **Correlation Analysis:** Identified key variables linked to cardiac disease using a Pearson correlation matrix, masked for readability.

---

### Technical Methodology

#### **1. Data Pre-processing & Feature Engineering**
*   **BMI Calculation:** Created an `overweight` column by calculating BMI and categorizing values > 25 as 1 (overweight).
*   **Normalization:** Applied conditional logic to `cholesterol` and `gluc` columns, mapping healthy levels to 0 and elevated levels to 1.

#### **2. Categorical Analysis (Categorical Plot)**
*   Transformed data into **Long Format** using `pd.melt`.
*   Generated a multi-panel categorical plot using **Seaborn's `catplot`** to compare the counts of "Good" vs "Bad" outcomes for `active`, `alco`, `cholesterol`, `gluc`, `overweight`, and `smoke`, split by cardiovascular health (`cardio`).

#### **3. Data Cleaning & Statistical Visualization (Heat Map)**
*   **Statistical Filtering:** Cleaned the dataset by removing outliers based on:
    *   Blood pressure anomalies (diastolic > systolic).
    *   Height and weight outside the **2.5th to 97.5th percentile** range.
*   **Correlation Matrix:** Calculated the correlation between all variables and visualized it using a **Seaborn Heat Map**, featuring a mask for the upper triangle to highlight unique relationships.

---

### View the Analysis
You can view the full Python implementation, data transformations, and final visualizations here:
**[View the Medical Data Analysis Notebook](./MedData00.ipynb)**

### Stack
*   **Libraries:** Pandas, Seaborn, Matplotlib