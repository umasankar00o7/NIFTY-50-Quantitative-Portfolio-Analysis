# 📈 NIFTY 50 Quantitative Portfolio Optimization & Predictive Machine Learning System

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Power BI](https://img.shields.io/badge/Power_BI-Executive_Dashboard-yellow.svg)
![Machine Learning](https://img.shields.io/badge/ML-Scikit--Learn-green.svg)
![License](https://img.shields.io/badge/License-MIT-purple.svg)

An institutional-grade quantitative data science project analyzing **2+ decades (2000–2021)** of the National Stock Exchange of India (NSE) Nifty 50 constituent stocks. 

---

## 🎯 Executive Project Overview
- **Business Problem:** Financial equities exhibit non-linear volatility regimes and tail-risk crashes. This project engineers a data-driven investment strategy to construct a multi-asset portfolio that optimizes risk-adjusted yield.
- **Data Scope:** 235,192 daily market trading sessions spanning 21.3 years across 52 unique constituent tickers and 14 distinct economic sectors.

---

## 🔬 Key Quantitative Findings

### 1. Task 1: Empirical Drivers of Volatility (2011–2021)
- **Intraday High-Low Range Spread ($r = +0.311$)**: Strongest contemporaneous indicator of volatility regimes.
- **Physical Delivery Ratio (`%Deliverble`) ($r = -0.251$)**: Demonstrates an inverse relationship with volatility. High delivery reflects institutional accumulation that anchors prices; low delivery indicates speculative day-trading that drives unpredictable swings.

### 2. Task 2: Multi-Asset Portfolio Engineering vs. Benchmark
Engineered an equal-weighted 5-stock portfolio diversified across non-overlapping economic sectors:
- **`BAJAJFINSV`** (Financial Services)
- **`SHREECEM`** (Cement & Materials)
- **`HINDUNILVR`** (FMCG / Defensive Anchor)
- **`MARUTI`** (Automobile)
- **`ADANIPORTS`** (Infrastructure & Services)

#### 10-Year Backtest Performance (2011–2021):
| Metric | Selected Portfolio | Nifty 50 Benchmark | Alpha / Outperformance |
| :--- | :--- | :--- | :--- |
| **CAGR (%)** | **27.67%** | 11.25% | **+16.42% p.a.** |
| **Sharpe Ratio ($R_f=6\%$)** | **1.06** | 0.30 | **+0.76 (3.5x superior)** |
| **Max Drawdown** | **-37.87%** | -42.49% | **+4.62% downside cushion** |
| **₹100,000 Final Value** | **₹1,202,761.16** | ₹294,472.03 | **4.08x total wealth** |

---

## 🤖 Task 4: Machine Learning Trend Forecasting
- **Validation Scheme:** Chronological forward validation (Train: 2011–2018 | Test: 2019–2021) with zero look-ahead bias.
- **Model Evaluation:**

| Model Architecture | Test Accuracy (%) | Precision (%) | Recall (%) | ROC-AUC |
| :--- | :--- | :--- | :--- | :--- |
| **Logistic Regression (Baseline)** | 53.50% | 56.00% | 75.08% | 0.514 |
| **Random Forest (Ensemble)** | **54.72%** | 55.43% | **93.38%** | **0.526** |

- **Top Features:** Intermediate Momentum (`Return_5D`: 0.181), Moving Average Alignment (`SMA_Ratio`: 0.146), and Delivery Ratio (`%Deliverble`: 0.131).

---

## 📊 Task 3: Interactive Power BI Executive Dashboard
- **Page 1: Micro Volatility & Portfolio Analytics (2011–2021)** — Wealth accumulation curve, KPI cards, Sharpe ratio rankings, and dynamic equity slicers.
- **Page 2: Macro 2-Decade Multi-Cycle Engine (2000–2021)** — Tracks long-term resilience across three macro crises (2000 Dot-Com crash, 2008 GFC, 2020 COVID shock), sector CAGRs, and multi-decade risk-return scatter profiles.

---

## 📂 Repository File Structure
├── NIFTY_PROJECT.ipynb # Primary master analytical & ML notebook
├── PROJECT_DOCUMENTATION.ipynb # Comprehensive end-to-end technical report
├── NIFTY50_Executive_Dashboard.pbix # Interactive 2-page Power BI dashboard
├── PowerBI_Stock_Metrics.csv # Processed stock metrics dataset
├── PowerBI_Portfolio_Vs_Benchmark.csv # Backtest wealth tracking dataset
└── README.md # Executive project briefing
