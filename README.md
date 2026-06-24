# E-Commerce Business Analysis - 2019

A comprehensive data analysis project exploring customer acquisition, retention, revenue optimization and behavioral patterns using transactional e-commerce data from January to December 2019.

---

## Project Overview

This project performs an end-to-end business analysis across five interconnected datasets covering 52,924 transactions from 1,468 unique customers. The analysis addresses 20 business questions spanning customer lifecycle management, marketing effectiveness, product performance and statistical hypothesis testing.

---

## Business Questions Addressed

| Category | Questions |
|---|---|
| **Customer Acquisition** | Monthly acquisition trends, high/low performing months |
| **Retention Analysis** | Monthly retention rates, cohort behavior patterns |
| **Revenue Analysis** | New vs existing customer revenue, coupon impact |
| **Marketing ROI** | Spend vs revenue correlation, channel effectiveness |
| **Product Performance** | Top performing products and categories |
| **RFM Segmentation** | Premium, Gold, Silver, Standard customer segments |
| **Cohort Analysis** | Retention rates by acquisition month |
| **Customer Lifetime Value** | CLV by acquisition cohort |
| **Statistical Testing** | Hypothesis tests on coupon usage and demographics |
| **Seasonal Trends** | Daily, monthly and category-level patterns |

---

## Dataset Description

| File | Description | Rows |
|---|---|---|
| `Online_Sales.csv` | Transaction-level sales data | 52,924 |
| `CustomersData.xlsx` | Customer demographics | 1,468 |
| `Discount_Coupon.csv` | Monthly coupon codes by category | 204 |
| `Marketing_Spend.csv` | Daily offline and online spend | 365 |
| `Tax_amount.xlsx` | GST rates by product category | 20 |

---

## Key Findings

- **January** recorded highest customer acquisition (215) while **November** recorded lowest (68) — a 3x gap despite November having one of the highest marketing spends
- **H1 builds, H2 monetises** — new customer revenue dominates H1 while existing customer revenue dominates H2, peaking at 72% in July
- **Premium segment** (408 customers, 27.8%) drives **63.9% of total revenue** with average spend of ₹8,503 per customer
- **Coupon users spend less** — statistically significant (T=-12.19, p≈0.000) difference of ₹19.35 per transaction vs non-users
- **July delivers best marketing ROI** (3.77x) at one of the lowest spend levels; December has highest spend but only 2.82x ROI
- **Nest-USA dominates revenue** — 26.5% of transactions but 50.4% of total revenue
- **Delivery charges significantly impact order value** (F=173.70, p≈0.000) — High tier customers spend ₹168.83 avg vs ₹83.61 for Low tier
- **Demographics don't drive spending** — no significant difference by gender, location or tenure (all p > 0.05)

---

## Technical Approach

### Libraries Used
```python
pandas | numpy | matplotlib | seaborn | scipy
```

### Analysis Techniques
- **RFM Segmentation** — Recency, Frequency, Monetary scoring with quartile-based classification
- **Cohort Analysis** — Month-of-acquisition retention matrix
- **Statistical Hypothesis Testing** — Independent T-Test and One-Way ANOVA
- **Revenue Modeling** — Multi-table joins with discount and GST calculations
- **CLV Analysis** — Customer Lifetime Value by acquisition cohort

### Revenue Formula
```
Revenue = (Avg_Price × Quantity × (1 - Discount%)) 
        + Delivery_Charges 
        + (Avg_Price × Quantity × GST%)
```

---

## Project Structure

```
ecommerce-business-analysis/
│
├── Data/
│   ├── Online_Sales.csv
│   ├── CustomersData.xlsx
│   ├── Discount_Coupon.csv
│   ├── Marketing_Spend.csv
│   └── Tax_amount.xlsx
│
├── Ecommerce_Analysis_EDA.ipynb    # Main analysis notebook
└── README.md
```

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/pr1994/ecommerce-business-analysis.git
```

2. Install required libraries
```bash
pip install pandas numpy matplotlib seaborn scipy openpyxl
```

3. Open the notebook
```bash
jupyter notebook Ecommerce_Analysis_EDA.ipynb
```

---

## Author

**Pritam Biswas**
- GitHub: [pr1994](https://github.com/pr1994)
- Previous Project: [Telecom Churn Prediction](https://github.com/pr1994/telecom-churn-prediction)
