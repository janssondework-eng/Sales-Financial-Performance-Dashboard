# Data Model

The dashboard follows a star-schema structure.

## Tables

| Table | Role | Description |
|---|---|---|
| `Sales` | Fact table | transactional sales records used for revenue, cost, profit, order and time-based analysis |
| `Customers` | Dimension table | customer attributes, region and customer type |
| `Products` | Dimension table | product names and product categories |
| `Calendar` | Dimension table | date fields used for monthly trends and year filtering |
| `Data_Dictionary` | Documentation sheet | field descriptions in the source workbook |
| `README` | Documentation sheet | workbook-level notes |

## Model Logic

- `Sales` connects to `Customers` through a customer key.
- `Sales` connects to `Products` through a product key.
- `Sales` connects to `Calendar` through a date key.
- Measures aggregate from the fact table and are sliced by customer, product, region and date dimensions.

## Why This Model Works

The star-schema approach keeps the model readable and efficient:

- KPI measures are calculated from one fact table.
- Filters flow from dimensions into sales metrics.
- Region, category, customer type and date analysis stay consistent across dashboard pages.

## Review Notes

The public repository includes the `.pbix` and an `.xlsx` dataset workbook. The documentation intentionally describes the model at the business-logic level so reviewers can understand it without opening Power BI Desktop.
