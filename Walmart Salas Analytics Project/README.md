# 🛒 Walmart Sales Data Analysis
### A Real-World Data Analyst Simulation Project

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-1.5%2B-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.6%2B-orange)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Project Overview

This project simulates a **real data analyst scenario at Walmart**. Rather than just running generic analysis, this project is framed as an actual business problem: the senior manager has flagged concerns about sales performance and needs data-backed answers by **Thursday's meeting**.

The analysis covers **45 Walmart stores** across **143 weeks** (Feb 2010 – Oct 2012), answering real business questions with Python, charts, and actionable recommendations.

---

## 🗂️ Repository Structure

```
walmart-sales-analysis/
│
├── data/
│   └── Walmart_Sales.csv          # Raw dataset (6,435 records)
│
├── src/
│   └── walmart_analyst_project.py # Main analysis script (fully commented)
│
├── notebooks/
│   └── walmart_analysis.ipynb     # Jupyter notebook version
│
├── charts/                        # Auto-generated visualizations
│   ├── chart1_store_performance.png
│   ├── chart2_holiday_impact.png
│   ├── chart3_economic_factors.png
│   └── chart4_seasonal_trends.png
│
├── requirements.txt               # Python dependencies
├── .gitignore
└── README.md
```

---

## 🧠 The Business Problem

> *"Hey, I need you to look into our sales data before Thursday's meeting. A few things are bugging me..."*  
> — Senior Manager, Retail Analytics

The manager asked four specific questions:

| # | Manager's Question | Section in Code |
|---|---|---|
| 1 | Which stores are underperforming and why? | Section 2 |
| 2 | Holiday weeks should drive more sales — are they? | Section 3 |
| 3 | When unemployment rises, do our sales dip? | Section 4 |
| 4 | Which months are strongest/weakest? When to run promotions? | Section 5 |

---

## 📊 Dataset Description

**File:** `data/Walmart_Sales.csv`  
**Source:** [Kaggle — Walmart Sales Forecasting](https://www.kaggle.com/datasets/yasserh/walmart-dataset)

| Column | Description |
|---|---|
| `Store` | Store number (1–45) |
| `Date` | Week start date |
| `Weekly_Sales` | Sales revenue for that store that week ($) |
| `Holiday_Flag` | 1 = holiday week, 0 = normal week |
| `Temperature` | Average temperature in the region (°F) |
| `Fuel_Price` | Cost of fuel in the region ($/gallon) |
| `CPI` | Consumer Price Index (inflation indicator) |
| `Unemployment` | Regional unemployment rate (%) |

**Quick Stats:**
- 📦 6,435 total records
- 🏪 45 unique stores
- 📅 Feb 5, 2010 → Oct 26, 2012
- 💰 Total revenue across all stores: **$6.74 Billion**
- 🔴 Missing values: **0** (clean dataset)

---

## 🔍 Key Findings

### 1. 🏪 Store Performance Gap is Massive
- **Top stores** (Store 20, 4, 14) average **~$2.1M/week**
- **Bottom stores** (Store 33, 38, 3) average **~$385K–$400K/week**
- That's an **8x performance gap** between best and worst stores
- Annually, top stores outperform bottom stores by **~$82M/year per store**

### 2. 🎄 Holiday Weeks Deliver a Real Lift
- Holiday weeks avg **$1.12M** vs **$1.04M** for non-holiday weeks
- That's a **+7.8% sales lift** during holiday periods
- **December** is the single strongest month **(+22.4% above annual average)**
- **January** is the weakest month **(-11.8% below annual average)**

### 3. 📉 Unemployment Has a Weak Negative Effect
- Correlation between unemployment and weekly sales: **r = -0.106**
- As unemployment rises, sales slightly decrease — but the effect is mild
- Walmart's *"Everyday Low Price"* positioning provides natural **recession resilience**
- Customers trade down to Walmart during economic hardship

### 4. 📅 Seasonal Patterns Are Highly Predictable
| Quarter | Avg Weekly Sales | vs Annual Avg |
|---|---|---|
| Q1 (Jan–Mar) | $1,006,136 | -3.9% |
| Q2 (Apr–Jun) | $1,040,806 | -0.6% |
| Q3 (Jul–Sep) | $1,023,251 | -2.3% |
| **Q4 (Oct–Dec)** | **$1,128,774** | **+7.8%** |

### 5. ⚡ Year-over-Year Trend (Concern)
- 2010 → 2011: **-1.27%** decline
- 2011 → 2012: **-1.20%** decline
- Gradual sales erosion across the 3-year period warrants further investigation

---

## ✅ Actionable Recommendations

### 🔴 Recommendation 1 — Store Performance Intervention *(Urgent)*
> Bottom 10 stores generate less than 30% of what top stores earn.

**Action:** Conduct on-site operational audits at Stores 33, 44, and 5. Benchmark their layouts, staffing levels, and inventory mix against top performers. Pilot a targeted store reset by Q2.

---

### 🟡 Recommendation 2 — Maximize Holiday Revenue Windows
> Holiday lift is real (+7.8%) but there's room to grow. Super Bowl weeks underperform vs other holidays.

**Action:** Launch targeted pre-event promotions 2 weeks before Super Bowl (snack/beverage displays, electronics, party goods). Estimated potential lift: +3–5% additional revenue.

---

### 🟢 Recommendation 3 — January Recovery Campaign
> January is our weakest month — customers are post-holiday budget-constrained.

**Action:** Launch a *"New Year Savings"* campaign in January with clearance pricing and everyday essentials. This builds foot traffic during the dead zone and prepares for Q1 recovery.

---

## 📈 Charts

All charts are auto-generated when you run the script and saved to the `/charts` folder.

| Chart | What It Shows |
|---|---|
| `chart1_store_performance.png` | Average weekly sales for all 45 stores, color-coded by tier |
| `chart2_holiday_impact.png` | Holiday vs non-holiday comparison + breakdown by holiday type |
| `chart3_economic_factors.png` | Scatter plots of Temperature, Fuel Price, CPI, Unemployment vs Sales |
| `chart4_seasonal_trends.png` | Monthly averages + full 3-year weekly sales timeline |

---

## 🚀 How to Run This Project

### Step 1: Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/walmart-sales-analysis.git
cd walmart-sales-analysis
```

### Step 2: Set Up a Virtual Environment (Recommended)
```bash
# Create virtual environment
python -m venv venv

# Activate it
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Run the Analysis
```bash
cd src
python walmart_analyst_project.py
```

> ⚠️ Make sure `Walmart_Sales.csv` is inside the `data/` folder before running.

### Optional: Run in Jupyter Notebook
```bash
jupyter notebook notebooks/walmart_analysis.ipynb
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python 3.8+** | Core programming language |
| **Pandas** | Data loading, cleaning, aggregation |
| **Matplotlib** | Chart creation and styling |
| **Seaborn** | Statistical visualizations |
| **NumPy** | Numerical operations and trend lines |
| **Jupyter** | Interactive notebook environment |

---

## 📚 What I Learned / Skills Demonstrated

- ✅ **Data Cleaning** — Parsing dates, checking nulls, type casting
- ✅ **Exploratory Data Analysis (EDA)** — Distributions, aggregations, groupby
- ✅ **Business Framing** — Translating manager questions into data queries
- ✅ **Statistical Analysis** — Correlation analysis, coefficient of variation
- ✅ **Data Visualization** — Multi-chart dashboards with Matplotlib
- ✅ **Storytelling with Data** — Insights structured for executive presentation
- ✅ **Actionable Recommendations** — Moving from findings to business decisions

---

## 📁 Data Source

Dataset sourced from Kaggle:  
🔗 [Walmart Dataset — Kaggle](https://www.kaggle.com/datasets/yasserh/walmart-dataset)

---

## 👤 Author

**[Subham Maity]**  
Aspiring Data Analyst | Python • SQL • Data Visualization

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/YOUR_PROFILE)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/YOUR_USERNAME)

---

## 📄 License

This project is licensed under the MIT License — feel free to use, modify, and share with attribution.

---

*⭐ If you found this project useful, please consider giving it a star!*
