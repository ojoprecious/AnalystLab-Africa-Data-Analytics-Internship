# Week 3 — Advanced Analysis & Executive Dashboard

Building on my Week 2 Global Superstore BI Dashboard, this project takes the analysis deeper. Instead of just showing *what* happened, Week 3 investigates *why* profit margins remained flat despite sales doubling, and what management should do about it.

## What I Added to the Week 2 Foundation
- **Two-page dashboard:** "Executive Overview" (KPIs + headline charts) separated from "Advanced Analysis" (time trends, discount impact, product risk, customer value) to keep each page clean.
- **KPIs grew from 5 to 7:** added Total Customers and Loss-Making Orders.
- **DAX measures grew to 13,** including year-over-year growth.
- **Synced slicers** that filter both pages at once.

## DAX I Care About
I wrote an explicit year-offset measure:

```
Sales Last Year =
VAR CurrYear = YEAR(MAX('Sheet1'[Order Date]))
RETURN
CALCULATE([Total Sales],
    FILTER(ALL('Sheet1'[Order Date]),
        YEAR('Sheet1'[Order Date]) = CurrYear - 1))

Loss-Making Orders =
CALCULATE(COUNTROWS('Sheet1'), 'Sheet1'[Profit] < 0)
```

I also built a `Discount Bracket` calculated column (None / Low / Medium / High) with `SWITCH(TRUE())` , it made it possible to prove exactly where margin collapses.

## Three Business Problems Investigated
1. **The discount trap:** margin runs about +25% at zero discount, turns negative at 21–40%, and reaches around −60% above 40%. Routine deep discounts are buying revenue at the cost of profit.
2. **Hidden loss-makers:** Tables is the only sub-category in the red; the ten worst products (mostly Lesro, Bevis, Chromcraft furniture) lose up to ~$10K each; the sales-vs-profit scatter shows items with over $1M in sales that still end below zero.
3. **Growth without efficiency:** sales rose from ~$2.2M (2011) to ~$4.3M (2014) while margin never moved past 11.61% — the company is scaling its inefficiencies.

## Top Insight
My top 10 customers deliver ~$299K of sales at ~24.5% margin — more than double the company average. They rarely take heavy discounts. Disciplined pricing works; the data says to scale that behaviour.

