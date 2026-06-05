# power-bi-dashboard-of-superstore-dataset
# Sales Performance & Profit Analytics Dashboard

An interactive Power BI dashboard built to analyze sales performance, profitability, customer behavior, product trends, and shipping efficiency using the Superstore dataset.

## Project Overview

This dashboard helps stakeholders monitor key business metrics and identify opportunities for growth by providing insights into:

- Sales performance
- Profitability trends
- Customer segments
- Product performance
- Regional sales distribution
- Shipping and delivery efficiency

The project demonstrates practical use of Power BI for business intelligence and data visualization.

## Dataset Information

The dataset contains transactional sales data with the following fields:

Field	                Description
Order ID	            Unique order identifier
Order Date	          Date of order placement
Ship Date	            Date of shipment
Ship Mode	            Shipping method
Customer ID	          Unique customer identifier
Customer Name	        Customer name
Segment	              Customer segment
Country	              Customer country
City	                Customer city
State	                Customer state
Region	              Business region
Product ID	          Product identifier
Category	            Product category
Sub-Category	        Product sub-category
Product Name	        Product name
Sales	                Revenue generated
Quantity	            Quantity sold
Discount	            Discount applied
Profit	              Profit earned or loss incurred

## Tools & Technologies
- Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Data Cleaning
- Data Visualization

## Dashboard Pages

### Executive Overview

Provides a high-level summary of overall business performance.

KPIs
-Total Sales
-Total Profit
-Total Orders
-Total Customers
-Profit Margin %
Visuals
-Sales Trend Analysis
-sales by year
-Sales by Region
-Profit by Category
-Sales by Customer Segment

### Product Analytics

Analyzes product performance and profitability.

Visuals
- Top 10 Products by Sales
- Top 10 Products by Profit
- Category-wise Performance
- Sub-Category Analysis
- Discount vs Profit Analysis
Business Questions Answered
- Which products generate the highest revenue?
- Which categories are most profitable?
- How do discounts impact profits?

### Customer Analytics

Provides insights into customer behavior and purchasing patterns.

Visuals
- Top Customers by Sales
- Sales by Customer Segment
- Geographic Sales Distribution
- Customer Contribution Analysis
Business Questions Answered
- Who are the most valuable customers?
- Which customer segment contributes the most revenue?
- Which regions have the highest customer activity?

### Shipping & Delivery Analysis

Evaluates shipping performance and delivery timelines.

Visuals
-Average Delivery Days by Ship Mode
-Ship Mode Usage Distribution
-Profit by Ship Mode
Calculated Metric
 Days to ship =
DATEDIFF(
    Orders[Order Date],
    Orders[Ship Date],
    DAY
  )
Business Questions Answered
-Which shipping mode is used most frequently?
-Which shipping method delivers fastest?
-Does shipping mode affect profitability?

### DAX Measures Used

Total Sales
    Total Sales =
    SUM(Orders[Sales])
Total Profit
    Total Profit =
    SUM(Orders[Profit])
Total Orders
    Total Orders =
    DISTINCTCOUNT(Orders[Order ID])
Total Customers
    Total Customers =
    DISTINCTCOUNT(Orders[Customer ID])
Profit Margin %
   Profit Margin % =
   DIVIDE(
    SUM(Orders[Profit]),
    SUM(Orders[Sales]),
    0
   )
Average Order Value
   Average Order Value =
   DIVIDE(
    SUM(Orders[Sales]),
    DISTINCTCOUNT(Orders[Order ID])
   )


## Data Preparation

The dataset was cleaned and transformed using Power Query.

Steps Performed
- Checked for missing values
- Removed duplicate records
- Corrected data types
- Created delivery duration metric
- Formatted date fields for time analysis

## Key Insights

- Certain regions consistently generate higher sales revenue.
- Technology products contribute significantly to overall profit.
- Higher discounts often lead to reduced profitability.
- Consumer segment contributes the largest share of sales.
- Standard Class is the most commonly used shipping method.
- Delivery performance varies across different shipping modes.

## Skills Demonstrated

- Data Cleaning
- Data Transformation
- DAX Calculations
- KPI Development
- Business Intelligence Reporting
- Dashboard Design
- Interactive Visualizations
- Data Storytelling

## Dashboard Preview

- Executive Overview
- Product Analytics
- Customer Analytics
- Shipping & Delivery Analysis

## Project Structure

Sales-Performance-Dashboard
│
├── Dataset
│   └── Superstore.csv
│
├── Dashboard
│   └── Sales_Performance_Dashboard.pbix
│
├── Screenshots
│   ├── executive-overview.png
│   ├── product-analytics.png
│   ├── customer-analytics.png
│   └── shipping-analysis.png
│
└── README.md

## Project Outcome

This dashboard transforms raw sales data into actionable business insights, enabling better decision-making through interactive reporting and visual analytics.

## Author

Apshara Parvin

Aspiring Data Analyst
