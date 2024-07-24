# Toman-Bike-shop-Business-performance-analysis
This project analyzes the year-over-year business performance of Toman Bike Shop, focusing on key metrics such as the number of riders, total revenue, total profit, and average price per rider. The analysis is performed using SQL queries to extract, transform, and load (ETL) data from multiple tables. Additionally, a Power BI dashboard is created to visualize the insights derived from the data, providing a comprehensive view of the company's growth dynamics and financial performance.

Common Table Expression (CTE): Combines data from two tables into a single dataset using a UNION ALL operation.

with cte as (
select * from bike_share_yr_0
union all
select * from bike_share_yr_1)

Data Selection: Extracts the following fields for analysis-
select 
dteday,
season,
a.yr,
weekday,
hr,
rider_type,
riders,
price,
COGS,

Revenue Calculation:
Calculates revenue as riders * 'price'

Profit Calculation:
Calculates profit as 'revenue-COGS * riders'.

Data Joining:
Performs a LEFT JOIN operation to combine the CTE with 'cost_table' on the year ('yr') to incorporate cost information.


Power Bi Dashboad preview
![Screenshot 2024-07-24 195429](https://github.com/user-attachments/assets/a6983209-81d0-4f61-b4cd-d9d1659b1394)

analize bussiness performance after price increase:
![analize ](https://github.com/user-attachments/assets/fe0edddc-ae31-483a-af3a-d94f649fdca5)

![recommendation ](https://github.com/user-attachments/assets/06f53809-7376-439b-b2f4-436becc25cfc)
