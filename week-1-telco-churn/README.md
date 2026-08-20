# Telco Customer Churn Analysis — ABC Communications Ltd

**AnalystLab Africa — Data Analytics Internship | Week 1: Business Analytics Case Study**
**Author:** Ojo Precious Mojolaoluwa

---

## Project Overview

This project investigates **customer churn** at ABC Communications Ltd, a telecommunications company seeking to understand why customers leave and how to retain them. Using the Telco Customer Churn dataset (7,043 customers × 21 features), I performed data cleaning, exploratory data analysis (EDA), and visualization to uncover churn drivers and deliver actionable business recommendations.

**Overall churn rate: 26.6%** — more than 1 in 4 customers leave the company.

---

## Business Questions Answered

1. **What does the customer base look like?** — 7,043 customers; near-even gender split; 16% seniors; ~48% have partners.
2. **Which segments have the highest churn?** — Month-to-month customers, Fiber optic users, and Electronic check payers.
3. **Does contract type influence retention?** — Yes, strongly. Month-to-month churn ≈ 43% vs ≈ 2% for two-year contracts.
4. **Does tenure affect loyalty?** — Yes. Tenure has a negative correlation with churn (−0.35); most churn happens in the first months.
5. **Which services influence churn?** — Fiber optic customers churn at ≈ 42% vs ≈ 19% for DSL.
6. **Which payment methods have higher churn?** — Electronic check (≈ 45% churn) vs ≈ 15–19% for automatic methods.
7. **What actions should management take?** — See Recommendations below.

---

## Tools Used

- **Python** — Pandas, NumPy, Matplotlib, Seaborn
- **Google Colab** — analysis environment
- **GitHub** — version control & portfolio hosting

---

## Dataset

- **Source:** [Kaggle — Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,043 rows × 21 columns
- **Key features:** demographics (gender, SeniorCitizen, Partner, Dependents), account info (tenure, Contract, PaymentMethod, MonthlyCharges, TotalCharges), and services (InternetService, OnlineSecurity, TechSupport, etc.)
- **Target:** `Churn` (Yes/No)

**Data quality notes:**
- `TotalCharges` was stored as text with 11 blank values (all tenure = 0 customers) → converted to numeric and handled.
- **0 duplicate rows**; `customerID` is unique.

---

## Visualizations Produced

| # | Chart | Purpose |
|---|-------|---------|
| 1 | Bar — Churn by Contract Type | Contract impact on retention |
| 2 | Bar — Churn by Internet Service | Service-level churn |
| 3 | Bar — Churn by Payment Method | Payment friction |
| 4 | Pie — Overall Churn Distribution | Churn rate |
| 5 | Pie — Customer Distribution by Partner Status | Base composition |
| 6 | Histogram — Monthly Charges | Billing distribution |
| 7 | Histogram — Tenure | Loyalty timeline |
| 8 | Box Plot — Monthly Charges vs Churn | Price sensitivity |
| 9 | Correlation Heatmap | Numeric relationships |

All charts are saved in the `visualizations/` folder.

---

## Key Insights

1. **Month-to-month contracts** are the biggest churn driver (≈ 43% churn vs ≈ 2% for two-year).
2. **Fiber optic customers** churn at more than double the rate of DSL customers.
3. **Electronic check payers** show the highest churn (≈ 45%).
4. **New customers (0–10 months)** are the most vulnerable; loyalty grows sharply after the first year.
5. **Churned customers pay higher median monthly charges** (~$80 vs ~$64 for retained customers).

## Business Risks

1. Revenue erosion from high-value Fiber optic churn.
2. Wasted acquisition spend on early-leaving customers.
3. Competitor poaching of flexible-contract, price-sensitive customers.

## Opportunities

1. Convert month-to-month customers to long-term contracts.
2. Migrate Electronic check users to auto-pay methods.
3. Launch a first-90-days onboarding program to cut early churn.

## Recommendations

1. **"Loyalty Lock-In" campaign** — discounts/add-ons for upgrading to 1-year contracts.
2. **Auto-pay incentive** — one-time credit for switching from Electronic check.
3. **First-90-Days success program** — proactive onboarding calls and support.
4. **Fiber optic service audit** — investigate pricing and service quality.
5. **Churn early-warning dashboard** — flag high-risk customers (low tenure + month-to-month + electronic check) for retention offers.
