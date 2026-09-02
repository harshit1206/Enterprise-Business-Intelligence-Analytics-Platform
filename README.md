# Enterprise Business Intelligence & Analytics Platform

A complete **Power BI Business Intelligence and Analytics Platform** built on an e-commerce sales dataset. The project transforms raw transactional data into a structured analytical data model and an interactive multi-page dashboard for monitoring sales, profitability, customers, products, geography, payments, discounts, and business trends.

## Project Overview

**Raw E-commerce Data → Power Query Transformation → Dimensional Data Model → DAX Measures → Interactive Power BI Dashboards**

The platform provides a centralized view of business performance and supports data-driven decision-making.

## Business Objectives

The platform helps answer:

- How much revenue and profit is being generated?
- What is the overall profit margin?
- How are sales and profit changing over time?
- Which categories, sub-categories, and products perform best?
- Which customers contribute the most revenue?
- Which regions and cities perform best?
- Which payment methods are most commonly used?
- How do discounts affect sales and profitability?
- How does performance compare across years?

## Technologies Used

| Technology | Purpose |
|---|---|
| **Power BI** | Dashboard development, data modeling, visualization |
| **Power Query** | Data cleaning, transformation, merging and preparation |
| **DAX** | KPIs, calculations, rankings and time intelligence |
| **CSV** | Source transactional dataset |

## Dataset

### Source File

`Ecommerce_Sales_Data_2024_2025.csv`

The source data contains:

- Order ID
- Order Date
- Customer Name
- Region
- City
- Category
- Sub Category
- Product Name
- Quantity
- Unit Price
- Discount
- Sales
- Profit
- Payment Mode

## Data Model

The project uses a **star-schema-oriented dimensional model**.

### Fact Table

**FactSales**

Contains transaction-level sales information and foreign keys connecting the fact table to the dimensions.

Key fields include:

- Order ID
- Order Date
- Quantity
- Unit Price
- Discount
- Sales
- Profit
- Customer Key
- Product Key
- Location Key
- Payment Key
- Date Key

### Dimension Tables

#### `DimCustomer`
Customer attributes and unique customer keys.

#### `DimProduct`
Product information including:

- Product Key
- Product Name
- Category
- Sub-Category
- Product attributes

#### `DimLocation`
Geographic information including:

- Location Key
- Region
- City

#### `DimPayment`
Payment-related information and payment keys.

#### `DimDate`
Date dimension used for time-based analysis and DAX time intelligence.

## Power Query Transformation

Power Query was used to:

1. Import the raw CSV dataset.
2. Clean and standardize columns.
3. Create dimension tables.
4. Remove duplicate dimension records.
5. Create unique dimension keys.
6. Build the `FactSales` fact table.
7. Merge dimension keys into the fact table.
8. Create the Date dimension and Date Key.
9. Validate the dimensional structure.
10. Load the final model into Power BI.

Special attention was given to maintaining unique dimension keys so merges did not create duplicate fact rows.

## DAX Measures

The DAX measures for core KPIs, sales and order analytics, time intelligence,
profitability, products, customers, and geography are documented in
`Enterprise_BI_DAX_Measures.txt`.

## Power BI Report Structure

The final report contains six main pages:

1. **Home**
2. **Executive Overview**
3. **Sales Analytics**
4. **Product & Category**
5. **Customer & Geography**
6. **Profitability & Discount**

The report uses a consistent dark-themed design with navigation between analytical pages.

## 1. Home

The Home page acts as the landing page and provides navigation cards for:

- Executive Overview
- Sales Analytics
- Product & Category
- Customer & Geography
- Profitability & Discount

## 2. Executive Overview

Provides a high-level view of overall business performance.

### KPI Cards

- Total Sales
- Total Orders
- Total Profit
- Profit Margin %
- Average Order Value
- Total Customers

### Visuals

- **Monthly Sales Trend** — Line Chart
- **Sales by Category** — Bar Chart
- **Sales by Region** — Donut Chart
- **Sales vs Profit Trend** — Line Chart
- **Top 5 Products by Sales** — Funnel Chart
- **Discount vs Sales by Category** — Scatter Chart
- **Sales per Customer vs Target** — Gauge

## 3. Sales Analytics

Focuses on transaction and sales behavior.

### Visuals

- **Sales by Sub-Category** — Bar Chart
- **Sales by Payment Method** — Donut Chart
- **Sales by Quantity Range** — Funnel Chart
- **Annual Sales Comparison** — Column Chart
- **Discount vs Sales by Category** — Scatter Chart
- **Payment Method Performance** — Matrix

## 4. Product & Category

Focuses on product-level and category-level performance.

### Visuals

- **Category Sales Contribution (%)** — Pie Chart
- **Sales Trend by Category (YoY)** — Line Chart
- **Top 10 Products by Profit** — Bar Chart
- **Products by Category** — Treemap
- **Category Profitability Heatmap** — Matrix

## 5. Customer & Geography

Analyzes customer and geographic performance.

### Visuals

- **Top 10 Customers by Sales**
- **Sales by City** — Map
- **Customer & Sales Distribution** — Scatter Chart
- **Sales Contribution by Region** — Waterfall Chart
- **Regional Sales Ranking by Month** — Ribbon Chart

## 6. Profitability & Discount

Focuses specifically on profitability and discount behavior.

### Visuals

- **Monthly Profit Trend** — Area Chart
- **Profit by Sub-Category** — Column Chart
- **Discount Contribution by Category** — Pie Chart
- **Profit by Discount Band** — Funnel Chart
- **Profit Margin vs Target** — Gauge


## Key Business Analysis Enabled

### Sales Performance
Monitor total revenue, annual performance and monthly sales trends.

### Profitability
Monitor total profit, profit margin, profit per order and profit contribution across categories and sub-categories.

### Product Performance
Identify top-selling and most profitable products and compare category performance.

### Customer Performance
Find high-value customers and analyze customer contribution to revenue.

### Geographic Performance
Compare regions and cities to identify strong and weak markets.

### Payment Behavior
Understand customer payment preferences and compare payment-method performance.

### Discount Effectiveness
Analyze discount contribution and examine relationships between discounts, sales and profitability.

## Project Highlights

- Built a structured dimensional data model.
- Used Power Query for data transformation and preparation.
- Created reusable DAX measures for business KPIs.
- Implemented time-intelligence calculations.
- Added product, customer and regional ranking logic.
- Built a six-page interactive Power BI report.
- Designed separate analytical pages to reduce visual repetition.
- Added interactive navigation through the Home page.
- Used KPI cards, charts, maps, matrices and advanced Power BI visuals.
- Created a management-focused Executive Overview.
- Added dedicated profitability and discount analysis.


## How to Use

1. Open the Power BI `.pbix` file.
2. Refresh the dataset if required.
3. Start from the **Home** page.
4. Use the navigation cards to move between report sections.
5. Use Power BI filters and visual interactions to explore the data.
6. Review KPI cards for high-level performance.
7. Drill into product, customer, geographic and profitability pages for deeper analysis.

## Project Purpose

This project demonstrates an end-to-end **Business Intelligence and Analytics solution** using Power BI.

It combines:

**Data Cleaning + Data Modeling + DAX + Visualization + Business Analytics**

The project demonstrates practical skills in:

- Business Intelligence
- Data Analytics
- Power BI
- Power Query
- DAX
- Data Modeling
- Dashboard Design
- Business Reporting

