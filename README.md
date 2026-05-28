Power BI Sales & Profit Analysis Dashboard

 Project Overview
This project is an interactive **Power BI Dashboard** developed for analyzing retail sales and profit performance across different regions, customer segments, product categories, and yearly trends.

The dashboard provides business insights related to:
- Sales Performance
- Profit Analysis
- Regional Comparison
- Customer Contribution
- Category Performance
- Growth Tracking
- Segment Analysis

The dashboard is fully interactive with slicers and filters for dynamic business intelligence reporting.



 Tools & Technologies Used
- Power BI
- DAX (Data Analysis Expressions)
- Power Query
- Data Modeling
- Excel / CSV Dataset



 Dashboard Features

 KPI Cards
The dashboard contains important business KPIs:

| KPI | Value |
|------|------|
| Total Sales | 2.30M |
| Total Profit | 286.41K |
| Profit Margin | 0.12 |
| Growth Percentage | 1.00 |
| Total Orders | 5.009K |



Dashboard Visualizations

 1.  Sum of Sales by Month Name
- Line chart displaying monthly sales trends.
- Helps identify seasonal sales patterns.

 Insights
- Highest sales observed during November and December.
- Lowest sales recorded during January and February.



 2.  Sum of Profit by Category
Horizontal bar chart showing category-wise profit.

 Categories
- Technology
- Office Supplies
- Furniture

Insights
- Technology category generated maximum profit.
- Furniture generated the lowest profit.



  Sum of Sales by Region
Column chart comparing sales across regions.

 Regions
- West
- East
- Central
- South

 Insights
- West region recorded highest sales.
- South region showed comparatively lower sales.



 Sum of Sales by Segment
Donut chart showing contribution by customer segment.

 Segments
- Consumer
- Corporate
- Home Office

Insights
- Consumer segment contributed maximum revenue.
- Home Office contributed the least.



  Customer-wise Sales Table
Displays:
- Customer Name
- Total Sales

Used for identifying:
- Top customers
- Revenue contribution
- High-value customers



Interactive Slicers / Filters

The dashboard includes the following filters:

 Year Filter
- 2014
- 2015
- 2016
- 2017

 Month Filter
Used for monthly sales analysis.

 Region Filter
Filters visuals by region.

Category Filter
Filters visuals by product category.

 Segment Filter
Filters visuals by customer segment.



 Data Modeling & Relationships

The dashboard follows a relational data model in Power BI.

 Relationships Used

| Primary Table | Relationship | Secondary Table |
|------|------|------|
| Orders | Customer ID | Customers |
| Orders | Product ID | Products |
| Orders | Region ID | Region Table |
| Orders | Order Date | Calendar Table |

Relationship Type
- One-to-Many Relationships
- Star Schema Modeling

Benefits of Relationships
- Cross-filtering between visuals
- Faster dashboard performance
- Accurate KPI calculations
- Better time intelligence analysis



 DAX Measures & Formulas Used

 Total Sales
DAX
Total Sales = SUM(Orders[Sales])

Total Profit 
Total Profit = SUM(Orders[Profit])

Profit Margin
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales],
    0
)

Total Orders
Total Orders =
DISTINCTCOUNT(Orders[Order ID])

Growth Percentage 
Growth Percentage =
DIVIDE(
    [Current Year Sales] - [Previous Year Sales],
    [Previous Year Sales]
)

Previous Year's Sales 
Previous Year Sales =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Calendar'[Date])
)
