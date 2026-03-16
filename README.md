# Exploratory-Data-Analysis-Python
End-to-end Python EDA project focusing on retail revenue trends and automated entity segmentation using Pandas and Seaborn. #python #pandas #eda #data-analytics #data-visualization

#  Data Analysis & Feature Engineering Portfolio

**Author:** Peter Krupčík | **Role:** Aspiring Data Analyst

---

##  Project Objective
The aim of this project was to conduct a comprehensive **Exploratory Data Analysis (EDA)** on two separate datasets: **Retail Sales** and **Character Attributes**. 

The emphasis was placed on:
* **Data Cleaning:** Systematic removal of noise and error handling.
* **Integrity Management:** Resolving technical inconsistencies.
* **Business Intelligence:** Creating visualizations suitable for stakeholder decision-making.

---

## 🛠 Technical Stack
* **Python 3.12**
* **Pandas:** Data manipulation & Schema normalization.
* **Matplotlib & Seaborn:** Statistical data visualization.
* **NumPy:** Mathematical operations & Imputation.

---

##  Technical Challenges & Resolutions
During development, I faced several real-world data issues. Here is how I addressed them:

### 1. External Source Inconsistency (HTTP 404 Error)
* **Issue:** Remote datasets hosted on external URLs were moved or became inaccessible during runtime, causing the pipeline to fail.
* **Resolution:** I developed a **Robust Data Ingestion Pipeline**. I transitioned to local data generation to guarantee 100% uptime and enclosed the loading process within `try-except` blocks. This approach prevents the script from crashing if an external resource fails.

### 2. Imputation Failures (NaN Output Issue)
* **Issue:** When calculating the median for the Retail dataset, the output returned `NaN` instead of a numeric value. This was due to data type inconsistencies (Mixed types) in the column after null values were injected.
* **Resolution:** I implemented **Explicit Type Casting**. By applying `pd.to_numeric(errors='coerce')`, I converted the column to a float format before computing the median. This ensured that the statistical imputation was accurate, reliable, and production-ready.

---

##  Key Modules & Findings

### Module A: Retail Revenue Analysis
* **Methodology:** Aggregated daily revenue and performed **Median Imputation** to handle missing records without skewing the distribution.
* **Insight:** Identified a strong performance surge during weekend cycles (Saturday/Sunday), suggesting a need for increased staffing or targeted marketing during these peaks.

### Module B: Multi-Factor Segmentation
* **Methodology:** Developed a custom **Classification Algorithm** to segment entities into 'Legendary', 'Elite', and 'Standard' tiers based on weighted composite scores (Attack + Speed).
* **Insight:** Correlation analysis ($r = 0.36$) proved that offensive power and mobility are independent drivers, requiring separate strategic focuses for character optimization.

---

## Visualizations Included
* **Daily Revenue Matrix:** Bar charts for trend identification.
* **Correlation Heatmaps:** Identifying feature relationships and multicollinearity.
* **Frequency Distribution:** Analyzing the spread of performance tiers across the population
