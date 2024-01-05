# Data-Insights-Engine-Advance-SQL-Analytics-at-AtliQ-Hardware

## Finance Analytics

### User-Defined SQL Functions
1. **Grab Customer Codes for Croma India:**
   - Retrieves customer codes for Croma in India from the `dim_customer` table.

2. **Get Sales Transaction Data for Fiscal Year 2021:**
   - Retrieves sales transaction data for the customer 'Croma' (customer code: 90002002) in the fiscal year 2021 from `fact_sales_monthly`.

3. **Create 'get_fiscal_year' Function:**
   - Defines a function to calculate the fiscal year based on a calendar date.

4. **Replace Function in Sales Transaction Query:**
   - Replaces the function created in the previous step in the sales transaction query.

### Gross Sales Report: Monthly Product Transactions
1. **Perform Joins for Product Information:**
   - Joins `fact_sales_monthly` with `dim_product` to get product information.

2. **Perform Join with 'fact_gross_price':**
   - Extends the previous query by joining with `fact_gross_price` and calculates the gross sales for each product.

### Gross Sales Report: Total Sales Amount
- Generates a monthly gross sales report for Croma India for all years.

### Stored Procedures: Monthly Gross Sales Report
1. **Generate Monthly Gross Sales Report for Any Customer:**
   - Creates a stored procedure, `get_monthly_gross_sales_for_customer`, to generate a monthly gross sales report for any customer.

### Stored Procedure: Market Badge
1. **Retrieve Market Badge:**
   - Defines a stored procedure, `get_market_badge`, to retrieve a market badge (Gold/Silver) based on the total sold quantity for a given market in a given fiscal year.

## Top Customers, Products, Markets

### Problem Statement and Pre-Invoice Discount Report
- Generates a detailed report for Croma, including pre-invoice deductions, and a similar report for all customers.

### Performance Improvement #1
- Optimizes performance by creating a `dim_date` table and avoiding the use of the `get_fiscal_year()` function.

### Performance Improvement #2
- Enhances performance by adding the fiscal year directly to the `fact_sales_monthly` table.

### Database Views
- Creates database views for net invoice sales and utilizes them for improved data retrieval.

## Supply Chain Analytics

### Create a Helper Table
- Creates the `fact_act_est` table by combining sales and forecast data, handling missing values.

### Temporary Tables & Forecast Accuracy Report
1. **Forecast Accuracy Report using CTE:**
   - Utilizes a Common Table Expression (CTE) for a forecast accuracy report.

2. **Stored Procedure for Forecast Accuracy:**
   - Creates a stored procedure, `get_forecast_accuracy`, for generating the forecast accuracy report.

3. **Forecast Accuracy Report using Temporary Table:**
   - Uses a temporary table for a forecast accuracy report.

## Readme Instructions

1. **Database Setup:**
   - Ensure the required database schema and tables are set up in your database environment.

2. **Execution Order:**
   - Execute SQL scripts in the provided order for each section (Finance Analytics, Top Customers, Products, Markets, Supply Chain Analytics).

3. **Stored Procedures:**
   - Execute stored procedures mentioned in the scripts for customized reports.

4. **Views:**
   - Utilize the database views for net invoice sales and forecast accuracy.

5. **Disclaimer:**
   - Make necessary adjustments based on your database environment and data.

6. **Responsibility:**
   - Use responsibly and comply with applicable data protection regulations.

This SQL project provides comprehensive analytics solutions for finance, top customers/products/markets, and supply chain at AtliQ Hardware. Adjustments may be needed based on your specific data and environment.
