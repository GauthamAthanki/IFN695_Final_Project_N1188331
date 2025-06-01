# IFN695 Final Project - Electricity Price Anomaly Detection (NSW1 Region)

## Project Overview

This project investigates **electricity price anomalies** within Australia's National Electricity Market (NEM), focusing on the **NSW1 region**. By leveraging weather, demand, and generation data, we detect, analyze, and forecast abnormal behaviors in price trends to better understand underlying drivers like demand spikes, renewable energy imbalance, and supply-demand margins.

---

## Objectives

- Detect anomalous pricing behavior using a **hybrid approach** (threshold + isolation forest)
- Identify **key features driving anomalies** using interpretable ML models
- Forecast anomaly-triggering features like **generation margin** using **SARIMA** and **LSTM**
- Provide recommendations to support **energy planning and grid stability**

---

## Project Structure

```bash
|-- IFN695_Gautham_Athanki_N11338831.ipynb      # Main Jupyter notebook with full pipeline
|-- /Data                                       # Raw and processed datasets
|-- /Plots                                      # Visual outputs and model results
|-- README.md                                   # Project summary (this file)

## Methods & Models Used
**Data Processing**
Data extraction from NEM files: DISPATCHPRICE, DISPATCHREGIONSUM

Hourly weather alignment (Sydney Observatory Hill as proxy)

Feature engineering: gen_margin, price_change, demand_delta, is_peak

 **Anomaly Detection**
Hybrid Labeling: RRP 85th percentile + Isolation Forest

**Supervised Models:**

Random Forest - Best performer

XGBoost -  Best performer

Logistic Regression, SGD, Naïve Bayes, Decision Trees

**Time Series Forecasting**
SARIMA and LSTM applied on gen_margin to detect future anomaly risk

**Evaluation Metrics**
Precision, Recall, F1-Score for both anomaly and normal classes

MAPE and RMSE for time series models

Feature Importance Rankings to identify major anomaly triggers

**Key Findings**
gen_margin, is_peak, and price_change were most influential features

Random Forest and XGBoost showed strongest anomaly detection performance

LSTM outperformed SARIMA for gen_margin forecasting (MAPE ~11.53%)

**Recommendations**
Broader integration of weather features across multiple stations would improve spatial anomaly resolution.

Inclusion of renewable energy mix, outage data, and network constraints would allow better contextual modeling of price anomalies.

Appendix
Full code and visualizations are documented in the Jupyter Notebook.
Access here: IFN695_Final_Project_N11338831.ipynb

GitHub Repository:
https://github.com/GauthamAthanki/IFN695_Final_Project_N11338831

Author
Gautham Athanki
Student ID: N11338831
Queensland University of Technology
Master of Data Analytics


