# Lita-Capstone-Project
___

## Table of Content
___
1. [Project Overview](#project-overview)
2. [Introduction](#introduction)
3. [Tools Used](#tools-used)
4. [Data Exploration](#data-exploration)
5. [Microsoft Excel](#microsoft-excel)
6. [SQL Queries](#sql-queries)
7. [PowerBI Dashboard](#powerbi-dashboard)
8. [Insights and Recommendations](#insights-and-recommendations)
9. [Conclusion](#conclusion)
10. [Appendices](#appendices)

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

#### Microsoft Excel
- EXCEL PIVOT TABLE AND CHARTS

  - Total sales by product.

![total sales by product](https://github.com/user-attachments/assets/2dff5b9d-bf64-4e1c-9f0b-c681a5a67084) ![total sales by product graph](https://github.com/user-attachments/assets/84f6e9d6-182f-4cde-a953-0fb873edb44a)


  - Total sales by Region

![total sales by region](https://github.com/user-attachments/assets/797d84a1-9fee-47ed-8a09-b2dd0f5e4944) ![total sales by region graph](https://github.com/user-attachments/assets/8669f615-b51c-4f66-8332-26e9b1c55ca9)

    
   - Total sales by month.
     
![total sales by month](https://github.com/user-attachments/assets/af519aa0-5927-434f-969f-ce152e13d39b) ![total sales by month graph](https://github.com/user-attachments/assets/c2562c4d-a611-4c38-ae86-3a2fea46252b)

- Calculated metrics:
    - Average sales per product.

![average sales per product](https://github.com/user-attachments/assets/b61e6edf-ac3c-45a8-8cf4-943efaca3253) ![average sales per product graph](https://github.com/user-attachments/assets/71298127-dc24-4eb9-b40f-bc6402322f83)

  - Total revenue by region.

 ![total revenue by region](https://github.com/user-attachments/assets/53540ea9-6edc-4707-91d9-28d771175f48) ![total revenue by region graph](https://github.com/user-attachments/assets/624e2c23-c360-4f7f-b42f-87e88f51bb82)


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


#### Appendices
___
* Capstone Sales Dataset


























