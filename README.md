# Sales & Financial Performance Dashboard

Interactive Power BI portfolio project for sales, profitability, customer and regional performance analysis.

The dashboard is designed for a management audience: it summarizes revenue, profit, margin, orders, customer segments, regions and top products in a small set of decision-ready pages.

## Executive Summary

- Total revenue: 24.95M
- Total profit: 10.50M
- Total cost: 14.45M
- Profit margin: 42.10%
- Orders: 5K
- Customers: 500
- Regions: 8
- Leading revenue region: Moscow
- Strongest categories: Skincare and Hair Care

## Business Questions

1. What are the current revenue, profit, cost and margin results?
2. How do revenue and profit change over time?
3. Which regions generate the most revenue and customers?
4. Which product categories and products drive performance?
5. How is the customer base segmented?
6. Which customer and product groups should management prioritize?

## Dashboard Pages

### Executive Dashboard

Management overview with high-level KPIs, revenue trend, revenue by region, revenue by product category and top products.

![Executive Dashboard](screenshots/executive_dashboard.png)

### Customer Analytics

Customer view with customer count, new customers, regional customer distribution, top customers by revenue and customer type segmentation.

![Customer Analytics](screenshots/customer_analytics.png)

### Financial Analytics

Profitability view with revenue, profit, cost, margin, revenue vs profit trend, margin by region, profit by category and top products by profit.

![Financial Analytics](screenshots/financial_analytics.png)

## Data Model

The dashboard uses a star-schema approach:

- `Sales` as the fact table
- `Customers` as the customer dimension
- `Products` as the product dimension
- `Calendar` as the date dimension

Supporting documentation:

- [docs/project_overview.md](docs/project_overview.md)
- [docs/data_model.md](docs/data_model.md)
- [docs/measure_reference.md](docs/measure_reference.md)
- [docs/dashboard_review_notes.md](docs/dashboard_review_notes.md)

## Core Measures

| Metric | Purpose |
|---|---|
| Revenue KPI | total sales performance |
| Profit KPI | profit generated after costs |
| Total Cost | cost base for profitability analysis |
| Profit Margin KPI | profit as a share of revenue |
| Orders KPI | order volume |
| Customers KPI | customer base size |
| Regions Count | market coverage |

## Key Insights

### 1. Moscow is the main revenue market

Moscow leads revenue by region, so it should remain a priority market for retention, assortment planning and high-value customer analysis.

### 2. Skincare and Hair Care drive category performance

These categories dominate revenue and profit views. They are natural candidates for product-level margin optimization and promotional planning.

### 3. Customer segmentation supports targeted actions

The customer page separates B2B Key Account, B2B Medium, B2B Small and Retail customers, which makes it suitable for differentiated commercial strategies.

### 4. Profitability needs to be read together with revenue

Financial analytics separates revenue and profit trends, helping management avoid focusing only on sales volume when margin changes matter.

## Files

- `dashboard/Sales & Financial Performance Dashboard (Power BI).pbix` - Power BI report
- `dataset/Sales_Financial_Performance_Dashboard_Dataset.xlsx` - source dataset workbook
- `screenshots/` - report page screenshots
- `docs/` - project documentation

## Tools And Skills

- Power BI
- DAX
- Data modeling
- KPI design
- Financial analysis
- Customer segmentation
- Dashboard storytelling
- Executive reporting

## Recommended Next Improvements

- Standardize visual labels to one language across all pages.
- Hide or resize visuals that show scrollbars in screenshots.
- Add explicit period-over-period measures, such as revenue growth and profit growth.
- Add tooltip pages or drillthrough pages for top products and key customers.
- Add a short data refresh note explaining whether the dataset is static or refreshable.
