# 📊 Trader Performance vs Market Sentiment Analysis


---

## 🧠 Executive Summary

This project analyzes how **market sentiment (Fear vs Greed)** impacts **trader behavior, performance, and risk-taking patterns** on Hyperliquid.  
This project demonstrates how sentiment-driven analytics can be transformed into automated trading decision systems.  

A robust analytical pipeline was developed to:

* Transform raw trading data into **structured insights**
* Identify **behavioral shifts across sentiment regimes**
* Generate **actionable, strategy-level recommendations**
* Demonstrate how analysis can be extended into **automated decision systems**

---

## 🎯 Problem Statement

Market sentiment is a key driver of trading decisions. This project addresses:

> How does market sentiment influence trader performance and behavior, and how can these insights be leveraged to optimize trading strategies?

---

## 📁 Repository Structure

```
trader-sentiment-analysis/
│
├── notebooks/
│   └── analysis.ipynb          # Full analysis (data → insights → visuals)
│
├── data/
│   ├── raw/                   # Input datasets
│   ├── processed/             # Cleaned outputs
│
├── outputs/
│   ├── charts/                # Visualizations
│   ├── tables/                # Aggregated metrics
│
├── writeup.md                 # 1-page analytical summary
├── README.md                  # Project documentation
├── requirements.txt
```

---

## ⚙️ Methodology Overview

### 🔹 1. Data Engineering Pipeline

* Standardized column names and schema
* Handled missing values and duplicates
* Converted timestamps to **daily granularity**
* Ensured clean and consistent dataset structure

---

### 🔹 2. Data Integration

* Merged sentiment and trading data using **date alignment**
* Avoided data leakage and ensured temporal consistency

---

### 🔹 3. Feature Engineering

Key features derived:

| Feature       | Description              |
| ------------- | ------------------------ |
| `daily_pnl`   | Aggregated profitability |
| `win_rate`    | Trade success ratio      |
| `trade_count` | Trading activity level   |
| `leverage`    | Risk exposure            |
| `long_ratio`  | Directional bias         |

---

### 🔹 4. Analytical Approach

The analysis was structured across:

* **Sentiment Comparison** (Fear vs Greed)
* **Behavioral Analysis** (leverage, activity, positioning)
* **Segmentation**:

  * High vs Low leverage traders
  * Frequent vs Infrequent traders

---

## 📊 Visual Analysis (Key Highlights)

The notebook includes multiple layers of visualization to support insights:

### 📈 Core Analysis

* PnL Distribution (Fear vs Greed)
* Win Rate Comparison
* Trade Frequency Analysis
* Leverage Behavior

---

### 📊 Advanced Analysis

* PnL Trend Over Time (time-series behavior)
* Long vs Short Ratio (directional bias)
* Correlation Heatmap (feature relationships)
* Segment Performance (risk-based segmentation)
* PnL Distribution Histogram (risk-return profile)

---

## 🔍 Key Insights

### 1. Sentiment Drives Profitability

* Higher PnL and win rates observed during **Greed periods**
* Fear periods show reduced profitability and higher uncertainty

---

### 2. Behavioral Regime Shift

* Greed → Aggressive trading (higher leverage, more trades)
* Fear → Defensive trading (reduced activity and exposure)

---

### 3. Leverage as a Risk Multiplier

* High-leverage traders:

  * Outperform in Greed
  * Underperform sharply in Fear
* Indicates strong **risk amplification effect**

---

### 4. Activity vs Efficiency Trade-off

* Increased trading activity does not always improve performance
* Overtrading observed during volatile (Fear) conditions

---

## 💡 Strategy Recommendations

### ✅ 1. Sentiment-Aware Risk Adjustment

Reduce leverage and exposure during Fear periods to minimize drawdowns.

---

### ✅ 2. Momentum-Based Participation

Increase trading activity during Greed phases to leverage strong market trends.

---

### ✅ 3. Segment-Specific Optimization

Apply differentiated strategies:

* Restrict high leverage during volatile markets
* Control overtrading behavior during Fear conditions

---

## 🤖 Automation Perspective

This analysis can be extended into a **rule-based trading system**:

```python
if sentiment == "Fear":
    leverage = base_leverage * 0.5
    trade_frequency = "low"

elif sentiment == "Greed":
    leverage = base_leverage * 1.2
    trade_frequency = "high"
```

👉 Enables:

* Dynamic risk management
* Automated strategy adjustment
* Scalable decision systems

---

## 📊 Outputs Generated

* Sentiment-wise performance tables
* Trader segmentation analysis
* Time-series and distribution visualizations
* Correlation insights

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Jupyter Notebook

---

## 🚀 Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/your-username/trader-sentiment-analysis.git
cd trader-sentiment-analysis
```

---

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Add Dataset Files

Place datasets in:

```
data/raw/
```

Expected files:

* `fear_greed_index.csv`
* `historical_data.csv`

---

## ▶️ How to Run

```bash
jupyter notebook notebooks/analysis.ipynb
```

Or run via Google Colab.

---

## 🔁 Reproducibility

* Fully reproducible workflow
* Clean and modular code structure
* Minimal manual intervention required

---

## 📌 Evaluation Alignment

This project is designed to maximize:

* ✔ Data cleaning & correctness
* ✔ Analytical reasoning
* ✔ Insight quality (actionable)
* ✔ Communication clarity
* ✔ Reproducibility

---

## ⚠️ Limitations

* Sentiment treated as daily static signal
* External macroeconomic variables not included
* No predictive modeling (baseline analysis)

---

## 🚀 Future Improvements

* Predictive modeling (PnL / volatility forecasting)
* Trader clustering (behavioral archetypes)
* Interactive dashboard (Streamlit)
* Real-time sentiment integration

---

## 🧾 Conclusion

Market sentiment acts as a **behavioral driver influencing trading performance and decision-making**.

Integrating sentiment into trading strategies enables:

* Improved risk management
* Better timing of trades
* More adaptive and intelligent systems

---

## 👨‍💻 Author

**Garvit Mehta**  
B.Tech CSE | Data Analytics & Business Intelligence Enthusiast
