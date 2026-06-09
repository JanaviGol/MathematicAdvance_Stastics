# 🎯 Spread Locator: E-Commerce Statistical Distribution Model

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg?style=for-the-badge&logo=python)](https://www.python.org)
[![Data Analysis](https://img.shields.io/badge/Analysis-Scipy%20%7C%20Seaborn-orange.svg?style=for-the-badge)](https://scipy.org)
[![Status](https://img.shields.io/badge/Project-Complete-success.svg?style=for-the-badge)](https://github.)

An advanced statistical data modeling pipeline designed to analyze customer purchase frequencies, operational workloads, and transactional value limits using probability distributions and engineering transformations.

---

## 📊 Dataset Operational Overview
The model processes a production transactional log containing key customer behaviors:
* **Total Audited Records:** 220 unique transaction events
* **Primary Target Indicators:** `transaction_amount` (Continuous) & `transaction_count` (Discrete)
* **Binary Status Metric:** `transaction_status` (Success vs. Fail tracking)

---

## 🛠️ Tech Stack & Processing Engines
The pipeline leverages core mathematical and statistical computing libraries:
* **Core Pipeline:** `pandas` & `numpy` (Vectorized computations)
* **Statistical Logic:** `scipy.stats` & `statsmodels` (Distribution fitting & transformations)
* **Visualization Layer:** `matplotlib` & `seaborn` (Advanced mathematical plots)

---

## 🚀 Key Pipeline Implementations

### 🩺 1. Baseline Summary Metrics
Extracts structural parameters to understand basic central tendencies.
> **In short:** This code calculates the mean, standard deviation, and min/max ranges to show the overall numerical summary of our transaction counts and amounts.

### 🪙 2. Success-Failure Probability (Bernoulli Distribution)
Evaluates independent transaction states to pinpoint platform operational baselines.
* **Core Conversion Prob ($p$):** 0.45
* **In short:** This code counts successful versus failed transactions to find the exact probability of a successful order on the platform.

### 🔄 3. Success Cycles (Binomial Distribution)
Tracks user behavior patterns over bounded intervals to establish standard active shopping loops.
* **Calculated Metrics:** Individual transaction success probability ($p = 0.32$) over fixed intervals.
* **In short:** This code creates a probability histogram to visually show how frequently customers complete a specific number of successful transactions.

### ⏱️ 4. Incoming Server Workload (Poisson Distribution)
Models random time-independent transaction frequencies to optimize server operational loads.
* **Platform Arrival Rate ($\lambda$):** Average 2.85 transactions per monitored unit.
* **In short:** This code overlays a theoretical Poisson line curve to check how closely our daily transactional frequencies follow a mathematically random arrival pattern.

### 📉 5. Spending Densities (Log-Normal vs. Power-Law)
Fits non-linear continuous distribution lines onto heavily skewed transaction values to capture high-value customer segments.
* **In short:** This code plots density curves to visually compare how well Log-Normal and Power-Law models overlay against our actual right-skewed spending data.

### 📉 6. Normality & Residual Verification (Q-Q Plot)
Generates empirical quantile mappings to prove distribution variations from baseline models.
* **In short:** This code generates a Q-Q plot to visually test for normality, showing that our transaction data significantly deviates from the red normal distribution reference line.

### 🧪 7. Skewness Correction (Box-Cox Transformation)
Executes complex variance stabilization transformations to normalize skewed transactional variance curves.
* **In short:** This code plots side-by-side density graphs to visually show how our highly right-skewed transaction data gets successfully transformed into a perfectly symmetrical, normal-like curve.

### 🎯 8. Risk Management Thresholds (Z-Score & Tail Probabilities)
Computes precise mathematical probabilities for high-tier anomalous sales values using standardized standard deviation distances.
* **Target Metric Range:** Estimation for transactions exceeding the ₹5,000 threshold.
* **Tail Area Probability:** 20.52% probability of high-value order occurrences.
* **In short:** This code calculates standard Z-scores to determine the exact mathematical probability (20.52%) of a transaction amount exceeding the ₹5,000 threshold.

### 📊 9. Continuous Accumulation Analysis (PDF & CDF)
Maps continuous density alongside dynamic running percentiles to extract accurate commercial spending constraints.
* **In short:** This code plots the PDF curve to show where transaction amounts are most heavily concentrated, alongside the CDF curve to track the cumulative probability percentages.

---

## 🏆 Business Intelligence Insights Summary

| Analytics Layer | Modeled Distribution | Business Value & Actions |
| :--- | :--- | :--- |
| **Operational Health** | **Bernoulli ($p=0.45$)** | Sets baseline transactional stability for customer checkout funnels. |
| **Capacity Forecasting** | **Poisson ($\lambda=2.85$)** | Maps resource deployment metrics to handle high peak-volume frequencies. |
| **Pricing Models** | **Log-Normal / Power-Law** | Identifies optimal premium product pricing and customer spending limits. |
| **Risk & Scaling** | **Z-Score Probability** | Estimates precise transaction volume ratios exceeding the ₹5000 tier. |

---

## 📂 Project Repository Structure
```text
├── spread_locator_dataset.csv     # Raw transaction dataset
├── spread_locator_notebook.ipynb  # Interactive statistical pipeline notebook
└── README.md                      # Advanced project summary