# Enterprise Business Intelligence & Analytics Platform

A Power BI-based ecommerce analytics solution designed for performance analysis across sales, profitability, customer value, product trends, and geographic contribution.

## Overview

This project combines:

- transactional ecommerce sales data
- reusable DAX KPI measures
- a business-ready Power BI dashboard
- visual analysis for product, customer, region, and trend review

The solution is intended for executive reporting and operational decision-making, helping teams understand how revenue, profit, discounts, and customer behavior evolve over time.

## Business Questions Answered

- How much revenue and profit are generated over time?
- Which categories, products, and regions contribute the most?
- How do sales and profitability compare with prior periods?
- Which customers and segments create the highest value?
- How effective are discounts in driving sales versus margin?

## Repository Contents

| File / Folder | Description |
| --- | --- |
| `Ecommerce_Sales_Data_2024_2025.csv` | Source transaction dataset for ecommerce sales analysis |
| `Enterprise_BI_DAX_Measures.txt` | DAX definitions for core KPIs and analytical measures |
| `report.pbix` | Power BI report file with dashboard pages and visuals |
| `img/` | Images used for documentation and presentation |
| `README.md` | Project documentation and usage guide |

## Dataset Summary

The dataset contains one row per transaction and includes the following fields:

- Order details: `Order ID`, `Order Date`
- Customer & geography: `Customer Name`, `Region`, `City`
- Product hierarchy: `Category`, `Sub-Category`, `Product Name`
- Commercial metrics: `Quantity`, `Unit Price`, `Discount`, `Sales`, `Profit`
- Payment information: `Payment Mode`

The file name includes `2024_2025`, but the actual transaction dates should be used for time-based analysis. The dataset includes multiple years and is intended for year-over-year and period comparison reporting.

## Core Dashboard Views

The Power BI report includes the following business-focused pages:

- Executive KPI summary
- Sales trend and performance analysis
- Product performance insights
- Geographic sales and profit breakdown
- Customer analysis and ranking
- Discount and profitability review

### Dashboard Visuals

![Discount analysis](img/discount.png)

![Geographic analysis](img/geo.png)

![Product performance](img/product.png)

![Sales trends](img/Trends.png)

![Customer analysis](img/users.png)

## DAX Measures Included

The analytical model includes measures for the following areas:

### Core KPI Measures
- Total Sales
- Total Profit
- Total Orders
- Total Quantity
- Total Customers
- Average Order Value
- Profit Margin %

### Growth and Time Intelligence
- Sales YTD
- Profit YTD
- Sales LY
- Profit LY
- Sales YoY %
- Profit YoY %

### Customer and Product Measures
- Sales per Customer
- Profit per Customer
- Orders per Customer
- Sales per Product
- Product Sales Rank
- Customer Sales Rank

### Geographic and Pricing Measures
- Region Sales Rank
- Region Profit Rank
- Discount Amount
- Discount %
- Gross Sales

These measures are structured to support a star-schema style reporting model based on tables such as:

- `FactSales`
- `DimDate`
- `DimProduct`
- `DimCustomer`
- `DimLocation`

## Project Use Case

This platform supports business decisions in several areas:

- identifying high-value products and categories
- tracking growth across periods
- evaluating regional performance and contribution
- assessing customer profitability and segmentation
- measuring discount efficiency and margin health
- supporting executive performance reviews and business planning

## Getting Started

1. Open `report.pbix` in Power BI Desktop.
2. Confirm the dataset path points to `Ecommerce_Sales_Data_2024_2025.csv`.
3. Refresh the model so the latest sales data is loaded.
4. Verify all columns and table names match the definitions in `Enterprise_BI_DAX_Measures.txt`.
5. Review relationships and ensure the date table is correctly marked for time intelligence.
6. Use slicers and visuals to analyze performance by date, region, category, product, and customer.

## Notes

- The DAX formulas use `DIVIDE` to avoid divide-by-zero issues in ratios.
- Time-based measures depend on a valid `DimDate` table and working date relationships.
- Refresh the report after changing the source file or updating data.
- Images in the `img/` folder provide a visual summary of the dashboard setup and can be used for presentations or documentation.

## Summary

This project delivers a complete ecommerce sales intelligence solution that combines transactional data, DAX-based KPI logic, and an executive-ready Power BI dashboard. It is suitable for business reporting, trend analysis, product review, customer insights, and regional performance evaluation.

