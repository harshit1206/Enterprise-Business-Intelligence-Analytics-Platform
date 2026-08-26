# Enterprise Business Intelligence & Analytics Platform

## Project Overview

This project is an enterprise-style Power BI analytics solution for ecommerce sales performance. It combines transaction-level sales data, reusable DAX measures, and a Power BI report to support analysis of revenue, profitability, customers, products, categories, regions, and sales trends over time.

The solution is intended to help business users answer questions such as:

- How are sales, profit, orders, and quantity performing?
- Which products, categories, and regions contribute the most revenue and profit?
- How are current results tracking against prior periods?
- What are the average order value, profit margin, discount, and customer-level economics?
- Which products or categories should receive additional attention?

## Project Contents

| File | Description |
| --- | --- |
| `Ecommerce_Sales_Data_2024_2025.csv` | Transaction-level ecommerce sales data. |
| `Enterprise_BI_DAX_Measures.txt` | DAX measure definitions for the Power BI data model. |
| `report.pbix` | Power BI report containing the analytics experience. |

## Dataset

The CSV contains one row per sales transaction and includes fields for:

- Order and date information: `Order ID`, `Order Date`
- Customer and geography: `Customer Name`, `Region`, `City`
- Product hierarchy: `Category`, `Sub-Category`, `Product Name`
- Commercial metrics: `Quantity`, `Unit Price`, `Discount`, `Sales`, `Profit`
- Payment information: `Payment Mode`

The source filename references 2024-2025, while the sample data includes dates from multiple years. Date filtering and comparisons should therefore be driven by the actual `Order Date` values in the loaded data.

## Analytics Coverage

The included DAX measures cover:

- **Core KPIs:** total sales, total profit, orders, quantity, customers, average order value, profit margin, average price, and discounts.
- **Order and customer analytics:** orders per customer, items per order, sales per customer, profit per customer, and profit per order.
- **Time intelligence:** YTD, MTD, QTD, prior-year values, year-over-year changes, and rolling 30-day and 90-day performance.
- **Product analytics:** products sold, sales and profit per product, and product rankings.
- **Category analytics:** category and sub-category counts, rankings, and contribution percentages.

## Expected Data Model

The DAX definitions reference a star-schema style model with tables such as:

- `FactSales`: transaction-level sales records.
- `DimDate`: a dedicated calendar table used for time intelligence.
- `DimProduct`: product, category, and sub-category attributes.

For best results, relate the fact table to the date and product dimensions, mark `DimDate` as the model's date table, and use dimension fields for report slicers and grouping.

## Getting Started

1. Open `report.pbix` in Power BI Desktop.
2. Confirm that the CSV source path is valid for the current machine.
3. Refresh the data model.
4. Verify that the table and column names match the references in `Enterprise_BI_DAX_Measures.txt`.
5. If the measures are not already present, create them in the appropriate model table by copying the DAX definitions from the text file.
6. Check date relationships and validate the time-intelligence measures with a date slicer.

## Recommended Report Views

A useful report structure can include:

- **Executive Summary:** sales, profit, orders, customers, profit margin, and year-over-year KPIs.
- **Sales Trends:** daily or monthly sales and profit with YTD and prior-year comparisons.
- **Product Performance:** top and bottom products by sales, profit, quantity, and rank.
- **Category and Geography:** category contribution, regional performance, and city-level detail.
- **Customer and Order Analysis:** customer economics, average order value, and order composition.

## Notes

- The DAX measures use `DIVIDE` for ratio calculations, which protects the report from divide-by-zero errors.
- Time-intelligence measures require a complete, properly related date table.
- Refresh the report after changing the CSV or updating the DAX definitions.
