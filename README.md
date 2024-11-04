# LITA_Class_Project
Documentation of my class projects while learning Data Analysis with Incubator Hub
## PROJECTS: LITA_Capstone_Project
### Project 1
### Outline
[Project Title](#Project-Title)

[Project Overview](#Project-Overview)

[Goals](#Goals)

[Data Sources](#Data-Sources)

[Tools Used](#Tools-Used)

[Data Cleaning and Preparation](#Data-Cleaning-and-Preparation)

[Exploratory Data Analysis](#Exploratory-Data-Anaysis)

[Data Analysis](#Data-Analysis)



#### Project Title: Sales Performance Analysis for a Retail Store
#### Project Overview
This Data Analysis project aims to analyze the sales performance of a retail store. By Using data analytics tecniques, we aim to explore sales data to uncover key insights such as top-selling products, regional performance, and monthly sales trends. The goal is to produce an interactive Power BI dashboard that highlights these findings.

#### Goals
- Assess sales trends: Analyze sales data to identify patterns over time
- Product Performance: Evaluate the performance of each product to determine which items bring in the most revenue
- Sales Forecasting: Develop predictive models to forecast futeure sales, helping the store to optimize inventory management

#### Data Sources
The Primary source of the data is from the Data Analysis Teachers at Incubator Hub

#### Tools Used
- Microsoft Excel
  1. Data Cleaning
  2. Data Analysis
  3. Data Visualization
- SQL (Structured Query Language) Server [Download Here](https://www.microsoft.com) for querying of data
- Power Bi Desktop for Visualization[Download Here](https://www.google.com/url?client=internal-element-cse&cx=012684331380167808104:oe5oj--md1a&q=https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads&sa=U&ved=2ahUKEwjQubqQr8GJAxUvUaQEHV7fEFkQFnoECBUQAQ&usg=AOvVaw1759XFBNl5AM71b9k88zga)
- GitHub for Portfolio Building

#### Data Cleaning and Preparation
In the initial phase of the data cleaning and preparations, I performed the following actions;
1. Data Loading and Inspection 
2. Data Assessment where a preliminary review of the data set was conducted to understand the structure, completeness and identify any potential issues as regards the data set.
3. Handling Missing Variables
4. Data Cleaning and Formatting
5. Data Consistency to ensure consistency in data formats across the data set and identify and eliminate duplicate records to enhance data integrity

#### Exploratory Data Analysis
EDA involved the exploring of data to answer some questions about the data such as:
- What are the top-selling products
- What are the monthly sales trends
- Regional performance of each product

#### Data Analysis
Here is included some basic lines of code or queries or some DAX expressions used during my analysis
##### Using Excel
- Use Excel formulas to calculate metrics such as average sales per product and total revenue by region.
```EXCEL
Total revenue for the North	=SUMIF(D2:D9922,D2,H2:H9922)
Total revenue for the South	=SUMIF(D2:D9922,D9906,H2:H9922)
Total revenue for the East	=SUMIF(D2:D9922,D9909,H2:H9922)
Total revenue for the West	=SUMIF(D2:D9922,D9913,H2:H9922)

Average sales for shirts	=AVERAGEIF(C2:C9922,C9898,I2:I9922)
Average sales for hats		=AVERAGEIF(C2:C9922,C9904,I2:I9922)
Average sales for shoes		=AVERAGEIF(C2:C9922,C9901,I2:I9922)
Average sales for socks		=AVERAGEIF(C2:C9922,C9905,I2:I9922)
Average sales for jacket	=AVERAGEIF(C2:C9922,C9917,I2:I9922)
Average sales for gloves	=AVERAGEIF(C2:C9922,C9918,I2:I9922)
```

Data Visualization
- Calculations

![Excel Sales Data ](https://github.com/user-attachments/assets/4bfd3aa2-28eb-4a70-9946-9de09e90b47f)
- Pivot Tables

![Excel Sales Data Pivot Table Sheet](https://github.com/user-attachments/assets/db7e5671-a5f9-4d66-8438-c0c29cca745b)
- Bar Charts

![Excel Sales Data Bar Chart Sheet](https://github.com/user-attachments/assets/16f0618a-66b2-45c8-a17c-50057c86368c)

  

##### Using SQL Server
Analysis:
- Sales Data data set was imported to the SQL Server Managemnt Server Studio
- The following analysis was done on the data with the corresponding queries
1. Retrieve the total sales for each product category.
```SQL
select PRODUCT, SUM(revenue) as Totalsales from [dbo].[Assignment2]
group by PRODUCT
```
  2. Find the number of sales transactions in each region.
```SQL
select Region, COUNT(*) as NumberOfSalesTransactions from [dbo].[Assignment2]
group by Region
```
  3. Find the highest-selling product by total sales value.
```SQL
select top 1 PRODUCT, SUM(sales) as HighestSellingProduct 
from [dbo].[Assignment2]
group by Product
```
  4. Calculate total revenue per product.
```SQL
select PRODUCT, SUM(revenue) as TotalRevenuePerProduct
from [dbo].[Assignment2]
group by PRODUCT
```
  5. Calculate monthly sales totals for the current year.
```SQL
select
      FORMAT(ORDERDATE, 'yyyy-MM') AS Sales_month,
	  SUM(Sales) as Monthhlysalestotal
from [dbo].[Assignment2]
where YEAR(orderdate) = 2024
group by FORMAT(orderdate, 'yyyy-MM')
ORDER BY FORMAT(ORDERDATE, 'yyyy-MM')
```
  6. Find the top 5 customers by total purchase amount.
```SQL
select top 5 customer_id, SUM(revenue) as Top5CustomersByPurchaseAmount 
from [dbo].[Assignment2]
group by customer_id
```

  7. Calculate the percentage of total sales contributed by each region.
```SQL
select
        Region, 
		SUM(sales) as Totalsalesinregion,
       (SUM(sales)*100.0) / (select SUM (Sales) from [dbo].[Assignment2]) as Sales_Percentage
from [dbo].[Assignment2]
group by Region
```
  8. Identify products with no sales in the last quarter.
```SQL
select PRODUCT as Productwithnosalesinlastquarter from [dbo].[Assignment2]
group by Product
having SUM(case When orderdate >= '2024-01-01' and orderdate < '2024-04-30' then 1 else 0 end) = 0
```
Data Visualozation
- SQL Queries

![SQL Sales Data](https://github.com/user-attachments/assets/0badc3b9-8471-4d6e-85dd-28750a82aaa2)

##### Power BI Desktop Analysis
The aim was to create an interactive dashboard which comprises the insights found in Excel and SQL. The dashboard includes
- Sales Overview
- Top-performing porducts
- Regional Breakdown

Data Visualization


