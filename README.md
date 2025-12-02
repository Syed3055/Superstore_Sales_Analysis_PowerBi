# Superstore Sales Analysis – Power BI Project

A complete Power BI dashboard analyzing sales, profit, customer segments, product containers, 
and category performance using the Global Superstore dataset.

## Dashboard Preview
*(Upload your PNG to GitHub and replace the path)*

## Project Overview
This Power BI report provides a comprehensive analysis of Sales Performance. KPIs include:
- Total Sales
- Total Profit
- Total Cost
- Profit %
- Segment Analysis
- Category-level Sales
- Container-level Profit %

## Key Metrics
- Total Sales: 1.92M  
- Total Profit: 224.08K  
- Total Cost: 25.31K  
- Profit %: 11.64%  

## DAX Measures

### Total Sales
```
Total Sales = SUM(Sales[Sales])
```

### Total Profit
```
Total Profit = SUM(Sales[Profit])
```

### Profit Percentage
```
Profit % = DIVIDE([Total Profit], [Total Sales])
```

### Month-over-Month %
```
MOM % =
VAR a = DIVIDE([Total Sales] - [Previous Month Sales], [Previous Month Sales])
VAR b = [icons] & " " & FORMAT(a, "0.0%")
RETURN b
```

### Revenue % by Category
```
Revenue % =
DIVIDE(
    [Total Sales],
    CALCULATE([Total Sales], ALL(Sales[Category]))
)
```

## Features Used
- Power Query for ETL  
- Data Modeling  
- DAX Time Intelligence  
- Custom Icons  
- Bookmarks & Interactions  
- Forecasting Models  

## Author
Syed  
GitHub: https://github.com/Syed3055  
