# Measure Reference

This file documents the core metric logic used by the Power BI dashboard. Exact measure names in the `.pbix` may differ, but the business logic is represented here for portfolio review.

## KPI Measures

```DAX
Revenue KPI = SUM(Sales[Revenue])

Total Cost = SUM(Sales[Cost])

Profit KPI = SUM(Sales[Profit])

Profit Margin KPI = DIVIDE([Profit KPI], [Revenue KPI])

Orders KPI = DISTINCTCOUNT(Sales[Order_ID])

Customers KPI = DISTINCTCOUNT(Customers[Customer_ID])

Regions Count = DISTINCTCOUNT(Customers[Region])
```

## Trend Measures

```DAX
Revenue Trend = [Revenue KPI]

Profit Trend = [Profit KPI]
```

These measures are shown by the `Calendar` table month/year fields.

## Ranking Measures

Top products, top customers and regional rankings use the same base measures:

- revenue rankings use `[Revenue KPI]`
- profit rankings use `[Profit KPI]`
- margin rankings use `[Profit Margin KPI]`

## Suggested Next Measures

```DAX
Revenue Previous Period =
CALCULATE(
    [Revenue KPI],
    DATEADD(Calendar[Date], -1, MONTH)
)

Revenue Growth % =
DIVIDE(
    [Revenue KPI] - [Revenue Previous Period],
    [Revenue Previous Period]
)

Profit Previous Period =
CALCULATE(
    [Profit KPI],
    DATEADD(Calendar[Date], -1, MONTH)
)

Profit Growth % =
DIVIDE(
    [Profit KPI] - [Profit Previous Period],
    [Profit Previous Period]
)
```

These additions would make the dashboard stronger for management reporting because they explain not only current performance, but also direction of change.
