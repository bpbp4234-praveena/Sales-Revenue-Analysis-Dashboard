# Sales & Revenue Analysis Dashboard

An interactive dashboard built in **Power BI Desktop** to analyze sales and revenue data, track key performance indicators (KPIs), and generate business insights.

## Objective
To analyze sales data and visualize KPIs, revenue trends, and top-performing products using charts, filters, and slicers.

## Dataset
- **Source:** Superstore sales dataset (`train.csv`)
- **Period:** 2015 to 2018
- **Key columns:** Order Date, Region, Category, Product Name, Customer ID, Sales

## Tools Used
- Power BI Desktop
- Power Query (data cleaning and date conversion)
- DAX (measures)

## Data Preparation
- Imported the CSV file using Text/CSV connector
- Converted Order Date and Ship Date from text to Date type (English - United Kingdom locale)
- Applied changes using Close & Apply

## KPIs
| KPI | Value |
|---|---|
| Total Sales | 2.26M |
| Total Orders | 5K |
| Average Order Value | 459.48 |
| Total Customers | 793 |

## DAX Measures
```DAX
Total Sales = SUM(train[Sales])
Total Orders = DISTINCTCOUNT(train[Order ID])
Avg Order Value = DIVIDE([Total Sales], [Total Orders])
Total Customers = DISTINCTCOUNT(train[Customer ID])
```

## Visualizations
- **Line chart:** Revenue trend by Year and Month
- **Bar chart:** Top 10 products by Total Sales
- **Donut chart:** Sales share by Category
- **Column chart:** Sales by Region
- **Slicers:** Region, Category, and Year for interactive filtering

## Key Insights
- West region contributes the highest sales.
- Technology is the top category with about 36.59% of total sales.
- Sales show an upward trend, with peaks towards the end of 2018.
- A small group of top products generates a large share of revenue.

## Dashboard Preview
![Dashboard](dashboard.png)

## Files in this Repository
- `Sales_Dashboard.pbix` - Power BI dashboard file
- `Sales_Dashboard_Report.docx` - Project report
- `train.csv` - Dataset
- `dashboard.png` - Dashboard screenshot

## How to Open
Download `Sales_Dashboard.pbix` and open it with Power BI Desktop.
