# Global Sea Level Predictor

### Project Overview
This project analyzes global average sea level changes from 1880 to the present and uses linear regression to predict future sea level rise through the year 2050. This analysis is critical for understanding environmental trends and the accelerating rate of sea-level changes.

### Key Insights & Forecasting
*   **Historical Trend:** Using data since 1880, the model predicts a steady rise in sea levels.
*   **Recent Acceleration:** By analyzing data from 2000 onwards, the second regression line indicates a steeper slope, suggesting that the rate of sea-level rise has accelerated in the 21st century.

---

### Workflow

#### **1. Data Processing**
*   Imported the [CSIRO Global Sea Level dataset](url) using **Pandas**.
*   Cleaned and indexed the data by year to prepare for statistical analysis.

#### **2. Statistical Modeling & Visualization**
*   **Scatter Plot:** Visualized the relationship between years and the CSIRO Adjusted Sea Level using **Matplotlib**.
*   **Full-Range Regression:** Utilized `scipy.stats.linregress` to calculate the line of best fit for the entire dataset (1880–present).
*   **Recent-Trend Regression:** Developed a secondary model focusing on data from **2000 to the present** to capture modern acceleration.
*   **Predictive Analysis:** Extended both regression lines to the year **2050** to forecast future sea levels under different historical contexts.

#### **3. Final Output**
*   **Title:** Rise in Sea Level
*   **X-Axis:** Year
*   **Y-Axis:** Sea Level (inches)

---

### View the Analysis
Detailed code, regression calculations, and the final predictive chart can be found in the notebook:
**[View the Sea Level Analysis Notebook](./SeaLevel00.ipynb)**

### Stack
*   **Language:** Python
*   **Libraries:** Pandas, Matplotlib, Scipy (Stats)