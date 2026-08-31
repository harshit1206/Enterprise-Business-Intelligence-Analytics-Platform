# Enterprise Business Intelligence & Analytics Platform

An enterprise-style Power BI analytics solution for ecommerce sales performance, covering revenue, profit, discounts, customer behavior, product performance, regional contribution, and time-based trends.

## Project Overview

This project brings together:

- transaction-level sales data from an ecommerce dataset
- reusable DAX measures for KPI and performance analysis
- a Power BI report designed for executive and operational decision-making
- dashboard visuals for product, customer, geography, and trend analysis

The report is designed to help answer questions such as:

- How much revenue and profit are being generated over time?
- Which products, categories, and regions are contributing the most?
- How are sales and profitability tracking against prior periods?
- What is the impact of discounts and margin performance?
- Which customer segments and sales patterns deserve attention?

## Repository Contents

| File | Description |
| --- | --- |
| `Ecommerce_Sales_Data_2024_2025.csv` | Ecommerce sales dataset with transaction-level records |
| `Enterprise_BI_DAX_Measures.txt` | DAX definitions used in the report model |
| `report.pbix` | Power BI dashboard/report file |
| `img/` | Dashboard screenshots and visual assets |

## Data Snapshot

The dataset contains one row per sales transaction and includes fields such as:

- Order details: `Order ID`, `Order Date`
- Customer and geography: `Customer Name`, `Region`, `City`
- Product hierarchy: `Category`, `Sub-Category`, `Product Name`
- Commercial metrics: `Quantity`, `Unit Price`, `Discount`, `Sales`, `Profit`
- Payment method: `Payment Mode`

The sample data spans multiple years but is stored under the `2024_2025` filename. For accurate time analysis, use the actual `Order Date` values in the dataset rather than relying only on the file name.

## Report Modules and Dashboard Views

The report includes several business-focused views:

- Executive KPI dashboard
- Sales and trend analysis
- Product performance analysis
- Geographic sales and profit analysis
- Customer-level performance analysis
- Discount and profitability review

### Dashboard Illustrations

![Discount analysis](img/discount.png)

![Geographic analysis](img/geo.png)

![Product performance](img/product.png)

![Sales trends](img/Trends.png)

![Customer analysis](img/users.png)

## DAX Measures Included

The DAX logic currently covers core enterprise metrics such as:

- Total Sales
- Total Profit
- Total Orders
- Total Quantity
- Total Customers
- Average Order Value
- Profit Margin %
- Discount Amount and Discount %
- Sales YTD and Profit YTD
- Sales LY and Profit LY
- Sales YoY % and Profit YoY %
- Sales per Customer, Profit per Customer, Orders per Customer
- Sales per Product and Product Sales Rank
- Customer Sales Rank
- Region Sales Rank and Region Profit Rank

These measures align with a star-schema style model using fact and dimension tables such as:

- `FactSales`
- `DimDate`
- `DimProduct`
- `DimCustomer`
- `DimLocation`

## Business Use Case

This analytics platform supports strategic and operational decision-making for ecommerce performance, with a focus on:

- identifying top-performing categories and products
- tracking growth and profitability across periods
- evaluating regional and customer contributions
- measuring discount efficiency and margin health
- understanding the drivers behind sales and profit trends

## Getting Started

1. Open `report.pbix` in Power BI Desktop.
2. Confirm the CSV file path points to `Ecommerce_Sales_Data_2024_2025.csv`.
3. Refresh the model to load the full dataset.
4. Verify table and column names match the definitions in `Enterprise_BI_DAX_Measures.txt`.
5. Ensure the date table is marked correctly and relationships are active for time intelligence.
6. Use slicers and report pages to analyze performance by date, region, category, product, and customer.

## Notes

- The DAX measures use `DIVIDE` to prevent divide-by-zero errors in ratio-based calculations.
- Time intelligence measures depend on an accurate `DimDate` table and valid date relationships.
- Refresh the report after data updates or when changing source files.
- The visuals in the `img/` folder reflect the current dashboard layout and can be used for presentation or documentation purposes.

## Summary

This project provides a complete ecommerce sales intelligence solution that combines transactional data engineering, DAX-based analytics, and an executive-ready Power BI dashboard. It is suitable for performance review, trend evaluation, and business insight generation across sales, product, customer, and geographic dimensions.

