# ⚡ Electricity Demand: Time-Series Data Cleaning & Analysis

This project demonstrates an end-to-end data cleaning pipeline for a 5-year hourly electricity demand dataset. The goal was to transform a "dirty" real-world dataset into a structured, model-ready format for time-series forecasting.

## 📊 Dataset Challenges
The raw data contained several issues that would lead to inaccurate models:
- ✔ **Missing Data:** 200 random hours were missing from the timeline.
- ✔ **Duplicates:** 100 duplicate timestamps identified and removed.
- ✔ **Outliers:** 30 extreme outliers (4× spikes) treated to reduce noise.
- ✔ **Null Values:** 150 NaN values requiring interpolation.
- ✔ **Shuffled Rows:** Data was not in chronological order.
- ✔ **Complex Patterns:** Contains daily and yearly seasonality with an upward long-term trend.

## 🛠 Cleaning Workflow
I implemented the following tasks using Python and Pandas:
1. **Datetime Conversion:** Standardized the timestamp format.
2. **Sorting:** Reordered the entire dataset chronologically.
3. **Deduplication:** Identified and removed redundant entries.
4. **Indexing:** Set the timestamp as the primary index for time-series operations.
5. **Reconstructing Timeline:** Used `asfreq('h')` to ensure every hour from 2019–2023 is represented.
6. **Gap Filling:** Handled missing timestamps and NaN values using linear interpolation.
7. **Validation:** Confirmed the data frequency using `pd.infer_freq()`.
8. **Export:** Saved the final cleaned dataset as a CSV for modeling.

## 📈 Visualizing Trends
Below is the visualization of the demand averages across different time scales:

![Demand Averages](demand_averages.png)

## 🛠 Tools Used
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib
