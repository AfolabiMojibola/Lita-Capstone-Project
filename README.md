# Lita-Capstone-Project
___

## Table of Content (Project 1)
___
1. [Project Overview](project-overview)
2. [Introduction](introduction)
3. [Tools Used](tools-used)
4. [Data Exploration](data-exploration)
5. [SQL Queries](sql-queries)
6. [PowerBI Dashboard](powerbi-dashboard)
7. [Insights and Recommendations](insights-and-recommendation)
8. [Conclusion](conclusion)

## Table of Contents (Project 2)
___
1. [Project Overview](project-overview)
2. [Tools Used](tools-used)
3. [Excel Analysis](excel-analysis)
4. [SQL Queries](sql-queries)
5. [PowerBI Dashboard](powerbi-dashboard)
6. [Final deliverables](final-deliverables)
7. [Appendices](appendices)

### PROJECT 1 - Sales Performance Analysis for Retail Store
___

#### Project Overview
___
This project shows the analysis of the sales performance of a retail store. This analysis was carried out by exploring the sales data to uncover key insights such as top-selling products, regional performance, and monthly sales end.  

#### Introduction
___
LITA Capstone Retail Store, a leading retail chain with multiple locations across the region, seeks to optimize its sales performance and improve customer engagement. With increasing competition in the market, the store's management recognizes the need for data-driven decision-making to stay ahead.


* Problem Statement
The store's current sales analysis process is manual, time-consuming, and limited in scope. The management team lacks a comprehensive understanding of sales trends, product performance, and regional variations, hindering strategic decision-making.


* Project Objectives
1. Analyze sales data to identify key insights such as top-selling products, regional performance, and monthly sales trends.
2. Develop a data-driven framework for sales performance evaluation.
3. Provide actionable insights to inform product optimization, regional sales strategies, and customer engagement initiatives.
4. Create a scalable and interactive sales dashboard for ongoing monitoring and analysis.


* Business Goals
1. Increase overall sales revenue by 10% within the next quarter.
2. Improve product mix and optimize inventory management.
3. Enhance customer satisfaction and loyalty through targeted marketing initiatives.
4. Strengthen competitive positioning through data-driven decision-making.


* Dataset Description

The project utilizes a comprehensive sales dataset spanning [January 2023- December 2024], encompassing:
- Sales transactions
- Product information
- Customer demographics
- Regional data
- Sales dates and times

#### Tools Used
This project employs a combination of data exploration, SQL querying, and data visualization techniques using:
- Microsoft Excel for data exploration and calculation
- SQL Server for data querying and analysis
- Power BI for interactive dashboard creation

#### Data Exploration
- EXCEL PIVOT TABLE AND CHARTS
Total sales by product


    - Total sales by product.

     
    - Total sales by region.
   
   
    - Total sales by month.
     


- Calculated metrics:
    - Average sales per product.
     

    - Total revenue by region.
     

SQL Queries
 Query 1: Total Sales by Product Category.
  ```
SELECT * FROM [dbo].[LITA Capstone Datasets]
SELECT Product,SUM(Quantity)
as Total_Sales
FROM [LITA Capstone Datasets]
GROUP BY Product
```

- Query 2: Number of Sales Transactions by Region.
```
SELECT Region,SUM(Quantity)
as Total_Sales
FROM[LITA Capstone Datasets]
GROUP BY Region
```







































