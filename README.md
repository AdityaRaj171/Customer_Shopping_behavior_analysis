# 🛍️ Customer Shopping Behavior Analysis

**An end-to-end data analytics project** — from raw data to business recommendations — using Python, MySQL, and Power BI to uncover what drives customer spending, loyalty, and revenue across 3,900 retail transactions.

![Python](https://img.shields.io/badge/Python-pandas-blue)
![SQL](https://img.shields.io/badge/SQL-MySQL-orange)
![Power BI](https://img.shields.io/badge/Dashboard-Power%20BI-yellow)

---

## 🎯 Why This Project

Retailers sit on huge amounts of transactional data but often struggle to turn it into decisions. This project simulates a real business analyst workflow: **clean messy data → answer stakeholder questions with SQL → present findings in a dashboard non-technical stakeholders can use.**

**What this project demonstrates:**
- Data cleaning and feature engineering in **Python (pandas)**
- Writing and interpreting **business-driven SQL queries**
- Designing an **interactive Power BI dashboard**
- Translating analysis into **clear, actionable business recommendations**

---

## 📊 The Dashboard

![Customer Behavior Dashboard](./dashboard.png)

An interactive Power BI view combining KPIs, category performance, subscription mix, and age-group trends — filterable by subscription status, gender, category, and shipping type.

---

## 💡 Key Findings

| Insight | Business Implication |
|---|---|
| Male customers generate **~2x the revenue** of female customers (₹157.9K vs ₹75.2K) | Reassess marketing spend allocation across gender segments |
| **839 customers** spent above average *despite* using a discount | Discounts aren't the only lever — quality/brand may matter more than price for this group |
| Non-subscribers outnumber subscribers **2.7x** (2,847 vs 1,053) | Clear opportunity to grow the subscriber base |
| **Hats, Sneakers & Coats** rely on discounts for ~48–50% of sales | Discount dependency may be eroding margin on these SKUs |
| **80% of customers are "Loyal"** (3,116 of 3,900) | Strong retention base — a loyalty program could compound this advantage |
| **Young Adults** are the top revenue-generating age group | Prioritize this cohort in targeted campaigns |

*(Full breakdown of all 10 SQL analyses and supporting query outputs in the [written report](./Customer_Shopping_Behavior_Analysis.docx).)*

---

## 🛠️ How It Was Built

**1. Data Cleaning & Feature Engineering** — `Customer.ipynb` (Python / pandas)
- Profiled 3,900 rows × 18 columns; identified and handled missing values
- Standardized all column names to `snake_case`
- Engineered new features: `age_group` (quartile-based customer cohorts), `purchase_frequency_days` (numeric conversion of purchase cadence)
- Identified and removed a fully redundant column (`promo_code_used` duplicated `discount_applied`)
- Loaded the cleaned dataset into **MySQL** via `SQLAlchemy` for structured querying

**2. Business Analysis** — SQL
- Wrote 10 targeted queries answering real business questions: revenue drivers, customer segmentation, discount dependency, shipping behavior, subscription impact, and more

**3. Visualization** — Power BI
- Built an interactive dashboard translating query results into a stakeholder-ready view with filters and KPI cards

---

## 🧰 Tech Stack

`Python` · `pandas` · `MySQL` · `SQLAlchemy` · `pymysql` · `SQL` · `Power BI` · `Jupyter Notebook`

---

## 📁 Repository Structure

```
├── Customer.ipynb                                # Data cleaning & feature engineering
├── customer_shopping_behavior.csv                # Raw dataset
├── Customer_Shopping_Behavior_Analysis.docx       # Full written report (SQL outputs + insights)
├── dashboard.png                                  # Power BI dashboard screenshot
└── README.md
```

---

## 🚀 Run It Yourself

```bash
# 1. Clone the repo
git clone https://github.com/AdityaRaj171/<repo-name>.git
cd <repo-name>

# 2. Install dependencies
pip install pandas mysql-connector-python sqlalchemy pymysql

# 3. Point the notebook at your own MySQL instance
# (update the connection string inside Customer.ipynb)
engine = create_engine("mysql+pymysql://<username>:<password>@localhost:3306/customer")

# 4. Run the notebook
jupyter notebook Customer.ipynb
```

---

## 👤 About Me

**Aditya Raj**
B.Tech Mechanical Engineering, SVNIT Surat — actively building a portfolio in data analytics, business analysis, and finance.

🔗 [GitHub — @AdityaRaj171](https://github.com/AdityaRaj171)

*If you're a recruiter or hiring manager reviewing this project — thanks for stopping by! Feel free to reach out with any questions about my approach or thought process.*
