# Retail Sales & Profitability Analytics | Power BI

An end-to-end Business Intelligence portfolio project built in **Microsoft Power BI** to analyze retail sales, profitability, products, regions, and customer segments. The project demonstrates dimensional modelling, DAX measures, interactive report design, and business-focused analysis.

> **Dataset notice:** This project uses synthetic demonstration data for learning and portfolio purposes. It does not represent a real company or actual customer transactions.

## Dashboard preview

### 1. Sales Performance Overview
![Sales Performance Overview](dashboard-screenshots/01-sales-performance-overview.png)

### 2. Product Performance Analytics
![Product Performance Analytics](dashboard-screenshots/02-product-performance-analytics.png)

### 3. Regional Sales & Performance Analytics
![Regional Sales & Performance Analytics](dashboard-screenshots/03-regional-sales-performance.png)

### 4. Customer Insights & Segmentation
![Customer Insights & Segmentation](dashboard-screenshots/04-customer-insights-segmentation.png)

## Key metrics shown in the report

| KPI | Dashboard value |
|---|---:|
| Total Sales | ₹134.21M |
| Total Profit | ₹38.73M |
| Total Orders | 5,000 |
| Profit Margin | 28.86% |
| Customers | 700 |
| Products | 195 |
| Average Discount | 8.79% |
| Repeat Customer Rate | 99.71% |

Values are taken from the supplied dashboard screenshots and represent the report's displayed baseline state with filters cleared where applicable.

## Report pages

- **Sales Dashboard:** KPI cards, sales by region, profit by category, and monthly sales trend.
- **Product Analytics:** Top and bottom products by profit, category/subcategory performance, and discount-versus-profitability analysis.
- **Regional Analysis:** Regional sales and profit contribution, state-level performance, and regional comparison.
- **Customer Insights:** Customer segments, top customers, city-level sales, repeat-customer metrics, and customer-level performance.

## Data model

The model follows a star-schema pattern with `FactOrders` as the central fact table and three dimensions:

- `FactOrders[CustomerID]` → `DimCustomers[CustomerID]`
- `FactOrders[ProductID]` → `DimProducts[ProductID]`
- `FactOrders[OrderDate]` → `DimDate[Date]`

Relationships are many-to-one from the fact table to each dimension, active, and single-direction. The date dimension covers 2023–2025.

## Dataset

The included Excel workbook contains the project tables:

- `FactOrders`: 5,000 order-line records
- `DimCustomers`: 700 customer records
- `DimProducts`: 195 product records
- `DimDate`: calendar dimension (1,096 dates)
- Currency: Indian Rupees (INR, ₹)

## Tools & skills demonstrated

- Microsoft Power BI Desktop
- Power Query for data preparation
- DAX measures and time intelligence
- Star-schema data modelling
- KPI design and interactive slicers
- Data visualization and business analysis

## Files

- `Retail_Sales_Performance_Dashboard.pbix` — editable Power BI report and model
- `Retail_Sales_Portfolio_Dataset.xlsx` — source workbook containing the dataset tables
- `dashboard-screenshots/` — screenshots of all four report pages

## How to explore

1. Download the `.pbix` file from this repository.
2. Open it with Power BI Desktop.
3. If Power BI prompts for data-source access, point it to the included Excel workbook or follow the data-source settings saved in the report.
4. Explore the four report pages and interact with the slicers and visuals.

## Analytical considerations

The dataset contains `Sales`, `Cost`, `ShippingCost`, and `Profit` fields; profit is defined in the source data as `Sales - Cost - ShippingCost`. The `OrderStatus` field includes Delivered, Returned, and Cancelled. Interpret results with that status mix in mind; a production analysis should define and document a business rule for cancelled and returned orders.

## Suggested GitHub topics

`power-bi` `data-analytics` `dax` `power-query` `business-intelligence` `sales-dashboard` `data-visualization`
