# Freight Index Forecasting (NCFI)

### MIT Global SCALE Network Project (Outstanding)

📅 Jan 2025 – Mar 2025

---

## 📌 Overview

This project focuses on forecasting the Ningbo Containerized Freight Index (NCFI) using real-world logistics and macroeconomic data.

The project integrates multiple data sources and applies both statistical and machine learning models to analyze freight rate dynamics.

Developed under the MIT Global SCALE Network Digital Supply Chain Microprogram, it was awarded **Outstanding performance**.

---

## 💼 Business Context

Freight rates are highly volatile and directly affect:

* Shipping pricing strategies
* Logistics planning and cost control
* Supply chain risk management

Accurate forecasting helps anticipate market fluctuations and supports data-driven decision-making.

---

## 📊 Data Sources

The project integrates multiple real-world datasets:

* NCFI freight index (target variable)
* Manufacturing PMI
* CPI (consumer price index)
* Diesel prices
* Port container throughput (TEUs)
* Vessel activity data

---

## ⚙️ Methodology

### Data Processing

* Time-series alignment across multiple datasets
* Handling missing values and scaling
* Construction of supervised learning format

---

### Train-Test Split

The dataset is divided using a chronological split rather than random sampling.

A portion of the earlier time-series data is used for training, while the remaining later portion is used for testing. This is implemented through index-based slicing to ensure temporal consistency.

Such a split simulates real-world forecasting, where models are trained on past data and evaluated on future observations.

---

### Feature Engineering

* Lag features for temporal dependency
* Moving averages (MA)
* Seasonal-Trend decomposition (STL)

---

### Models

#### 1. Linear Regression (Baseline)

* Used as a simple benchmark
* Provides reference for model improvement

---

#### 2. SARIMAX (Core Model)

* Incorporates external variables
* Performs well in capturing temporal structure
* Achieved the most stable performance among all models

---

#### 3. Random Forest

* Captures nonlinear relationships
* Performance observed to be unstable across different periods

---

#### 4. LSTM

* Deep learning model for sequence modeling
* Sensitive to normalization and architecture design
* Shows potential but requires careful tuning

---

## 📊 Results & Observations

* SARIMAX provides the most reliable and stable predictions
* Random Forest struggles with temporal generalization
* LSTM performance improves after tuning but is not consistently superior
* The model tends to learn patterns from previous years (e.g., 2021 → 2022), indicating challenges in regime shifts

---

## 🧠 My Contributions

* Designed and implemented an end-to-end forecasting pipeline
* Integrated multi-source real-world logistics and economic data
* Engineered time-series features including lag variables, MA, and STL decomposition
* Built and compared multiple models (statistical + ML + deep learning)
* Conducted critical analysis of model performance under real-world conditions

---

## 📂 Project Structure

```id="p4j6r8"
├── NCFI_Prediction.ipynb   # main analysis & modeling
├── Table*.xlsx            # raw datasets
└── README.md
```

---

## 🏅 Certification

This project was completed as part of the MIT Global SCALE Network
Digital Supply Chain Microprogram and awarded **Outstanding performance**.

---

## 📎 Notes

This project reflects real-world challenges in freight forecasting, including data heterogeneity, model instability, and market regime shifts.
