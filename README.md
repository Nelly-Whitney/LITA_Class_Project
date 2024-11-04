# LITA_Class_Project
Documentation of my class projects while learning Data Analysis with Incubator Hub
## PROJECTS
### Project 1 
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

- Calculating the Average Sales per Product and Total Revenue By Region
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
- 



