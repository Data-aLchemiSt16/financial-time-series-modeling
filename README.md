# 📈 Fortune 500 Stock Risk & Volatility Analysis

A comprehensive financial time-series analysis project using historical daily stock market data from Fortune 500 companies.  
The project focuses on return behavior, volatility modeling, and walk-forward forecasting with an emphasis on realistic evaluation and risk diagnostics.

> **Key idea:** Short-term returns are difficult to predict, while volatility exhibits persistence and structure that can be modeled more reliably.

---

## 📌 Project Objectives

- Analyze daily stock returns and volatility across Fortune 500 companies
- Perform rigorous exploratory data analysis (EDA) and risk profiling
- Build lag-based baseline models for return forecasting
- Implement walk-forward validation to avoid look-ahead bias
- Compare volatility forecasting models against a naive baseline
- Produce reproducible, publication-quality visualizations

---

## 📂 Dataset Overview

- **Universe:** Publicly traded Fortune 500 companies  
- **Frequency:** Daily  
- **Features:** Open, High, Low, Close, Adjusted Close, Volume  
- **Time Span:** Varies by company (IPO dates and availability)
- **Source:** Yahoo Finance (via API)

> ⚠️ This dataset is intended for **educational and research purposes only** and does not constitute financial advice.

---

## 🧱 Project Structure


---

## 🔹 Step-by-Step Workflow

### 1️⃣ Data Ingestion & Consolidation
- Load hundreds of individual stock CSV files
- Standardize schema and timestamps
- Combine into a single time-series dataset

### 2️⃣ Data Cleaning & Feature Engineering
- Enforce numeric data types
- Compute:
  - Daily returns
  - Log returns
  - Rolling 30-day annualized volatility
- Generate company-level summary statistics

### 3️⃣ Exploratory Data Analysis (EDA) & Risk Profiling
- Outlier inspection using boxplots (top volatile stocks)
- Distribution analysis of returns and volatility
- Risk–return scatter analysis
- Sector-wise volatility comparison
- Visualization of non-stationarity and volatility clustering

### 4️⃣ Return Forecasting (Baseline)
- Case study: **NVIDIA (NVDA)**
- Lag-based features (1, 5, 10, 20 days)
- Time-aware train/test split (no shuffling)
- Linear Regression baseline
- Evaluation using MAE and RMSE

**Finding:**  
Short-term returns converge toward zero, reflecting market efficiency and high noise.

### 5️⃣ Walk-Forward Forecasting & Volatility Modeling
- Walk-forward (expanding window) validation
- Volatility target: 30-day realized volatility (annualized)
- Features:
  - Lagged volatility
  - Lagged absolute returns
- Linear regression volatility model
- Comparison against a naive persistence baseline

**Finding:**  
Volatility is significantly more predictable than returns, though strong baselines remain difficult to outperform.

---

## 📊 Key Results

- ✔ Returns show limited short-horizon predictability  
- ✔ Volatility exhibits persistence and clustering  
- ✔ Walk-forward validation provides realistic performance estimates  
- ✔ Naive baselines are strong and essential for fair comparison  

> In efficient markets, **risk is more predictable than returns**.

---

## 🛠️ Tools & Libraries

- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

---

## 📌 Key Concepts Demonstrated

- Financial time-series preprocessing
- Lag-based feature engineering
- Walk-forward validation
- Risk vs return diagnostics
- Volatility modeling and benchmarking
- Reproducible research workflows

---

## ⚠️ Disclaimer

This project is for **educational and research purposes only**.  
It does **not** constitute investment advice or a trading strategy.

---

## 📜 License

This project is licensed under the **MIT License**.  
See the `LICENSE` file for details.

---

## 👤 Author

**Avi Sharma**  
Aspiring Data Scientist | Financial Time-Series Analysis

---

## ⭐ If You Found This Useful

Feel free to star the repository or fork it for learning purposes.
