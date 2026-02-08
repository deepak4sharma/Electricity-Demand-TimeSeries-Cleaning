# ⚡ Electricity Demand: Time-Series Data Cleaning
This project focuses on the "messy" part of Data Science. I took 5 years of raw hourly electricity data and performed an end-to-end cleaning process to make it ready for forecasting.

### 🔍 Problems Solved:
* **Missing Data:** Reconstructed 200+ missing hourly timestamps using `.asfreq()`.
* **Duplicates:** Identified and removed 100 duplicate records.
* **Outliers:** Handled extreme demand spikes (4x normal levels) that would skew models.
* **Feature Engineering:** Added lag features and rolling means to help the model "see" patterns.

### 🛠 Tools Used:
`Python`, `Pandas`, `NumPy`, `Matplotlib`
