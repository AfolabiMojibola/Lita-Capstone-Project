# Lita-Capstone-Project
___

## Table of Content (Project 1)
___
1. [Project Overview](#project-overview)
2. [Introduction](#introduction)
3. [Tools Used](#tools-used)
4. [Data Exploration](#data-exploration)
5. [SQL Queries](#sql-queries)
6. [PowerBI Dashboard](#powerbi-dashboard)
7. [Insights and Recommendations](#insights-and-recommendation)
8. [Conclusion](#conclusion)

### PROJECT 1 - Sales Performance Analysis for Lita Capstone Retail Store
___

#### Project Overview
___
This project shows the analysis of the sales performance of Lita Capstone retail store. This analysis was carried out by exploring the sales data to uncover key insights such as top-selling products, regional performance, and monthly sales end.  

#### Introduction
___
Lita Capstone Retail Store, a leading retail chain with multiple locations across the region, seeks to optimize its sales performance and improve customer engagement. With increasing competition in the market, the store's management recognizes the need for data-driven decision-making to stay ahead.


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
___
This project employs a combination of data exploration, SQL querying, and data visualization techniques using:
- Microsoft Excel for data exploration and calculation
- SQL Server for data querying and analysis
- Power BI for interactive dashboard creation

#### Data Exploration
___
- EXCEL PIVOT TABLE AND CHARTS
Total sales by product


    - Total sales by product.

     
    - Total sales by region.
   
   
    - Total sales by month.
     


- Calculated metrics:
    - Average sales per product.
     

    - Total revenue by region.
     

#### SQL Queries
___
 Query 1: Total Sales by Product Category.
  ```
SELECT * FROM [dbo].[LITA Capstone Datasets]
SELECT Product,SUM(Quantity)
as Total_Sales
FROM [LITA Capstone Datasets]
GROUP BY Product
```

 Query 2: Number of Sales Transactions by Region.
```
SELECT Region,SUM(Quantity)
as Total_Sales
FROM[LITA Capstone Datasets]
GROUP BY Region
```

 Query 3: Highest-Selling Product by Total Sales Value.
```
SELECT Product,SUM(Quantity)
as Total_Sales
FROM[LITA Capstone Datasets]
GROUP BY Product
Order By Total_Sales Desc
```

 Query 4: Total Revenue per Product.
```
SELECT Product,SUM(Quantity*UnitPrice)
as Total_Revenue
FROM[LITA Capstone Datasets]
GROUP BY Product
```

 Query 5: Monthly Sales Totals for Current Year.
```
SELECT OrderDate,
SUM(Quantity) as Total_Sales
FROM [dbo].[LITA Capstone Datasets]
WHERE OrderDate = 2024
GROUP BY OrderDate
```

 Query 6: Top 5 Customers by Total Purchase Amount.
 ```
SELECT Top 5
Customer_Id, SUM(Quantity) AS Total_Purchase
FROM [dbo].[LITA Capstone Datasets]
GROUP BY Customer_Id
ORDER BY Total_Purchase DESC
```

 Query 7: Percentage of Total Sales by Region.
```
SELECT Region, SUM(Revenue)/SUM(Quantity)*0.1 AS Percentage_of_Total_Sales
FROM [dbo].[LITA Capstone Datasets]
GROUP BY Region
ORDER BY Percentage_of_Total_Sales
```

 Query 8: Products with No Sales in Last Quarter.
```
SELECT Product,SUM(Quantity) AS Sales
FROM [dbo].[LITA Capstone Datasets]
WHERE MONTH(OrderDate)
BETWEEN 10 AND 12
GROUP BY Product
HAVING SUM(Quantity)=0
```

#### PowerBI Dashboard
___
- Dashboard screenshots:
    - Sales Overview.
      [Insert screenshot here]
    - Top-Performing Products.
      [Insert screenshot here]
    - Regional Breakdown.
      [Insert screenshot here]

- Description of visualizations and insights.




#### Insights and Recommendations 
___
Insights:
1. Product Performance
    - Top-selling products: [Hats, Shoes, Gloves and Shirt]
    - Underperforming products: [Socks and Jacket]

2. Regional Sales Trends
    - Regions with highest sales revenue : East(102500)and South(122500)
    - Regions with lowest sales revenue: North(62500) and West(57500)


Recommendations: 

* Short-Term (0-6 months):
1. Product Optimization
    - Discontinue underperforming products
    - Increase inventory of top-selling products
    - Introduce new products in high-growth categories
    
2. Regional Sales Strategies
    - Allocate targeted marketing budgets to high-growth regions
    - Adjust pricing strategies for regions with low sales revenue
    - Enhance customer engagement initiatives in key regions

* Medium-Term (6-18 months):
1. Sales Channel Optimization
    - Invest in e-commerce platform enhancements
    - Optimize online/offline channel integration
    - Explore new sales channels (e.g., social media, marketplaces)
    
2. Data-Driven Decision-Making
    - Establish regular sales data analysis and review processes
    - Develop predictive analytics capabilities
    - Integrate sales data with other business functions (e.g., marketing, supply chain)

* Long-Term (18+ months):
1. Strategic Partnerships
    - Explore partnerships with complementary businesses
    - Develop strategic relationships with key suppliers
    - Investigate opportunities for expansion into new markets
      
2. Innovative Sales Strategies
    - Explore emerging sales channels (e.g., AR/VR, social commerce)
    - Develop innovative sales formats (e.g., subscription services)
    - Invest in sales technology (e.g., AI-powered chatbots)

* Action Plan
1. Assign responsibilities to team members for implementation
2. Establish timelines and milestones for recommendations
3. Monitor progress and adjust strategies as needed


#### Conclusion
___
This sales performance analysis project has provided valuable insights into Lita Capstone Retail Store's sales trends, product performance, regional variations, and customer behavior. By leveraging data exploration, SQL querying, and data visualization techniques, we have identified opportunities for growth, optimization, and improvement.

* Key Takeaways
1. Data-driven decision-making is crucial for retail success.
2. Product optimization and regional sales strategies can drive revenue growth.
3. Customer engagement and retention are critical for long-term success.
4. Emerging sales channels and innovative strategies can foster competitive advantage.

* Recommendations Implementation
By implementing the recommended strategies, Lita Capstone Retail Store can:
1. Increase overall sales revenue by 10% within the next quarter.
2. Enhance customer satisfaction and loyalty.
3. Strengthen competitive positioning.

* Future Directions
1. Continuously monitor sales data to inform decision-making.
2. Explore predictive analytics and machine learning applications.
3. Investigate opportunities for expansion into new markets.
Limitations
1. Data quality and availability constraints.
2. Limited scope of analysis (e.g., excluding external factors like market trends).


* Final Thoughts
This project demonstrates the power of data analysis in driving business growth and improvement. By embracing data-driven decision-making, Lita Capstone Retail Store can unlock new opportunities, drive innovation, and maintain a competitive edge in the retail market.


## Table of Contents (Project 2)
___
1. [Project Overview 2](#project-overview-2)
2. [Tools Used 2](#tools-used-2)
3. [Excel Analysis 2](#excel-analysis-2)
4. [SQL Queries 2](#sql-queries-2)
5. [PowerBI Dashboard 2](#powerbi-dashboard-2)
6. [Appendices](#appendices)


### PROJECT 2  - Customer Segmentation for AME Subscription Service 

#### Project Overview 2
___
This project shows the analysis of customer segmentation for AME subscription service. This analysis was carried out by exploring the customer data for a subscription service to identify key trends in cancellation and renewals. The goal of the project is to understand customer behaviour, track subscription types and identity key trends in cancellation and renewals. 

#### Tools Used 2
___
This project employs a combination of data exploration, SQL querying, and data visualization techniques using:

- Microsoft Excel for data exploration and calculation
- SQL Server for data querying and analysis
- Power BI for interactive dashboard creation


#### Data Exploration 2
___
* Excel Analysis
-Analysis on customer data using pivot tables to find subscription patterns



-Average subscription duration and identification of the most popular 
subscription types


-Subscription type distribution by region


-Cancellation rates by subscription type



#### SQL Queries 2
- Total number of customers from each region
QUERY:
```
SELECT Region, COUNT(CustomerID) AS Total_No_of_Customers
FROM [dbo].[LITACAPSTONE CUSTOMER DATA]
GROUP BY Region
```

- Most popular subscription type by the number of customers
QUERY:
```
SELECT SubscriptionType, COUNT(CustomerID) AS No_of_Customer
FROM [dbo].[LITACAPSTONE CUSTOMER DATA]
GROUP BY SubscriptionType
```

- Customers who canceled their subscription within 6 months
QUERY:
```
SELECT CustomerName, Canceled, SubscriptionStart 
FROM [dbo].[LITACAPSTONE CUSTOMER DATA]
WHERE Canceled = 0 AND
MONTH(SubscriptionStart)
BETWEEN 1 AND 6
```

- Average subscription duration for all customers
QUERY:
```
SELECT Count(CustomerID) AS All_Customers, AVG(DATEDIFF(DAY,SubscriptionStart,SubscriptionEnd)) 
AS Average_Subscription_Duration 
FROM [dbo].[LITACAPSTONE CUSTOMER DATA]
WHERE SubscriptionEnd IS NOT NULL
```

- Customers with subscriptions longer than 12 months
QUERY:
```
SELECT CustomerName,SubscriptionType,SubscriptionStart,SubscriptionEnd 
FROM [dbo].[LITACAPSTONE CUSTOMER DATA]
WHERE DATEDIFF(MONTH, SubscriptionStart,SubscriptionEnd)>=12
```

- Total revenue by subscription type
QUERY:
```
SELECT SubscriptionType, SUM(Revenue) AS Total_Revenue
FROM [dbo].[LITACAPSTONE CUSTOMER DATA]
GROUP BY SubscriptionType
```

- Top 3 regions by subscription cancellations
QUERY:
```
SELECT TOP 3 Region, Canceled 
FROM [dbo].[LITACAPSTONE CUSTOMER DATA]
```

- Total number of active and canceled subscriptions
QUERY:
```
SELECT SUM(CASE WHEN Canceled=0 THEN 1 ELSE 0 END) AS ActiveSubscriptions,
SUM(CASE WHEN Canceled=1 THEN 1 ELSE 0 END) AS CanceledSubscriptions
FROM [dbo].[LITACAPSTONE CUSTOMER DATA] 
GROUP BY CustomerID
```


#### PowerBI Dashboard 2
___
- Create visualizations for:
    - Customer segmentation by region and subscription type
    [Insert screenshot here]

    - Cancellation rates by subscription type and region
    [Insert screenshot here]

    - Average subscription duration by subscription type
    [Insert screenshot here]

    - Total revenue by subscription type
    [Insert screenshot here]

    - Active and canceled subscription counts
    [Insert screenshot here]


*Interactive Analysis*
- Add slicers for region, subscription type, and date range.
- Enable drill-down capabilities for detailed analysis.

Final Deliverable
___
- A comprehensive Power BI dashboard showcasing customer segments, cancellations, and subscription trends.
- Accompanied by a report detailing findings and insights from Excel and SQL analyses.


#### Appendices
* Capstone Sales Dataset


























