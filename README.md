# HM_Sales_Performance_Analysis
"Data-driven analysis of H&amp;M's $63M global sales, focusing on category contributions, store ownership models, and month-over-month growth trends."
# H&M Global Sales Performance Analysis

## Project Overview
A comprehensive Power BI study of H&M's retail operations, analyzing a massive **$63M total sales** volume. This project identifies high-performing regions and product categories to optimize supply chain and marketing strategies.

## Key Insights
* **Massive Sales Scale:** Visualized a total revenue of $63M across 7.899K orders, maintaining a 1% MoM sales growth.
* **Product Category Balance:** Identified a near-equal revenue split between Kids (32.78%), Women (33.51%), and Men (33.71%), proving a diversified market appeal.
* **Price vs. Volume Analysis:** Developed a scatter plot to identify the 'Sweet Spot' for pricing, showing high sales volume clusters between 1500–2000 average price points.
* **Store Ownership Efficiency:** Compared 'Owned' vs. 'Rented' store types, finding consistent performance across both models with an average sales/sq.ft of 7.1.
<img width="1293" height="593" alt="Screenshot 2026-02-10 045518" src="https://github.com/user-attachments/assets/858f5a7f-d5d9-4cce-8b56-f95162bbbf13" />
<img width="1171" height="721" alt="Screenshot 2026-02-10 045453" src="https://github.com/user-attachments/assets/0a63ff35-93b1-4406-a840-63e944606d2b" />

## Strategic DAX Formulas Used
```dax
MoM% Sales Growth = 
VAR CurrentMonthSales = [Total Sales]
VAR PreviousMonthSales = CALCULATE([Total Sales], PREVIOUSMONTH('Date'[Date]))
RETURN
DIVIDE(CurrentMonthSales - PreviousMonthSales, PreviousMonthSales)

Average Order Value = DIVIDE([Total Sales], [Number of Orders])

