# Business-Insights-360
Project-Business-Insights-360 (Data Analyst Challenge at Codebasics.io)

Link to my Dashboard
🔷https://mavenanalytics.io/project/26383

🔷Power BI Service -https://app.powerbi.com/groups/me/reports/baf6df26-9c30-46d4-a610-920f7953068b/bef85b9ab804e1bd87b7?experience=power-bi

Overview:
Project: Provide Insights on Finance,sales,Marketing,Supply Chain to the Management. Domain: Manufacturing Domain

AtliQ Hardware is a company that Sells and Manufactures Hardware.They have Customers all over the world and Products under various categories. AtliQ Team use MS excel for data analysis but as the business expands globally company's Top management decides to use Power BI for data analytics. So Top management wanted the analytics team to Provide insights through SQl to make decisions and as later part of the Project a dashboard to be created for various key departments, so they can get insights on important metrics and make data driven Decisions
  DATA MODEL ### Dataset **Understanding.**

Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get good understanding of what are data available.

Dimension table : It will have the static data like details of customer and products

Fact table : It will have the data about the transactions  

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, spain)
        - **75** distinct customers thorough out the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
        - There are 14 different categories, Like Internal HDD, keyboard
        - There are different variants available for the same product
    - fact_forecast_monthly
        - This table is used to forecast the customer’s need in advance, which can help in
            - Higher customer satisfaction
            - Reduced cost in warehouses for storage purpose
        - The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        - All the date of the month will be replaced by the start date of the month
        - It will have all the column names and in the end it will have the forecast quantity need of the customer
    - fact_sales_monthly
        - This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.
- gdb056
    - freight_cost
        - This table has details of travel cost and other cost for each market with fiscal year
    - gross_price
        - Has the details of gross prices with product code
    - manufacturing_cost
        - Has the details of manufacturing cost with product code with year
    - Pre_invoice_dedutions
        - Has the details of pre invoice deductions percentage for each cutomer with year
    - Post_invoice_deductions
        - Post invoice deductions and other deductions details

## Importing data into PowerBi

- As the database is MySQL in this project, we need to import the datasets from Mysql database to PowerBi by providing the Database access credential

## Data Model

- Data modeling plays a vital role and is considered as the basement of report. All the visuals will be build upon the data model.
- Poor data modeling affects the over all performance of the report.
- Following Good practices of data modeling is must. Refer this page to get to know the good practices [Blog](https://addendanalytics.com/blog/data-modelling-best-practices/)
- In this project, we have followed Snowfall data modeling method.

![Screenshot 2025-02-02 145615](https://github.com/user-attachments/assets/97ea5ba0-03bf-40e0-8d35-3b33a25daa31)


### Dashboard designing

Based on the mock ups received as requirement, the team will start designing the visuals and create measure as and when required

## Home view

In Home view, all the views button will be available. User will land on specific view page by clicking the button 

- Info
- Finance View
- Sales View
- Marketing View
- Supply chain View
- Executive View
- Products
- Support



## Finance View
![Screenshot 2025-02-02 163825](https://github.com/user-attachments/assets/0978df34-006a-42f1-9c61-8e5100c3f934)


## Sales View

![Screenshot 2025-02-02 163839](https://github.com/user-attachments/assets/7871cb74-df6d-4944-a3d5-c95828f4aede)


## Marketing View
![Screenshot 2025-02-02 163855](https://github.com/user-attachments/assets/fb0f35ee-373b-4428-a9e1-310fa65fc51a)



## Supply chain View


![Screenshot 2025-02-02 163909](https://github.com/user-attachments/assets/48ec8881-f7a6-42fa-bd48-123a9886aa47)

## Executive View

![Screenshot 2025-02-02 163933](https://github.com/user-attachments/assets/1622216e-10ba-4cdf-9b45-ba6b1cc4221f)


Task:
As an data analyst who has been provided with sample data and a mock-up dashboard to work on the following task.

Write Sql Queries to Generate important insights and reports for product owners to make an data driven decisions.*

Create Stored Procedures so that managers can extract the reports based on the filters.*

Create an fully functional Dashbord for Data Driven Decisiosn, which gives insights on various departments like Finance, sales, marketing, Supply chain.*

Tech stack used in the project:


MySQL*
MS Excel*
Power BI*


Work Flow:
SQL Workbench

Data was Loading into Mysql and database was designed by establishing relationships in a Snowflake schema format between the tables with ERD in MySQL.*
Data was ready for Data Analysis and key metrics were Derived, for all the requests from Product owners*
Stored Procedures were created for the comples Queries so that Product owners can extract reports by necessary filters*
An Data pipeline was established in deriving Metrics, with many Data Cleaning methods implemented in between.
Reports were generated for Profit and loss Metrics, Deriving Top Metrics, and Procedures to track Forecast Accuracy for Supply Chain Department.


PowerBI Dashboard

Connected Power BI to MySQL and Excel, transformed data by establishing a data pipeline (ETL) using Power Query, Data Modelling to establish relations by snowflake schema and initial Data validation was done against benchmark values.*
Utilized DAX to create calculated columns and measures, and built a dynamic dashboard with KPI’s for sales, finance, marketing, and supply chain.*
Published a report on Power BI service for user acceptance testing (UAT) and Data validation through Excel Analyze.*
Incorporated stakeholder feedback to create an Executive Dashboard, resolved quality issues, optimized dashboard performance, and deployed the dashboard to Power BI service with gateway setup to MySQL Database and local Excel files for Automatic Data Refresh.*
Various Project Management Skills like Project charter, stakeholder mapping analysis, Kanban board for task assignment to improve productivity.*
A Designed dashboard with up to three levels of analysis, was able to ask the stakeholders many why’s, to their top performing, product, markets, customers, % changes and trends in P&L metrics, supply chain forecast accuracy for inventory management has helped to improve overall business.*

Created intuitive dashboards(Views), specifically targeted to various departments to give an overview of the company's performance.*
✔ Finance View ✔ Sales View ✔ Marketing View ✔ Supply Chain View ✔ Executive View

Key Features in Finance View:

The profit and loss Statement, explains on varoius P&L Metrics form Gross Sales to Net Profit.BM indicates the bench,ark , which is Either Last year or the Target. which can be selected through Slicer Provided.
KPI’s for Net Sales, Gross Margin %, Net Profit %.*
Net sales Performance Trend in comparision with Target/Last Year which can be selected Dynamically.
Top / Bottom Product and Top / Bottom Customers based on Net Sales*


Key Features in Sales View:

Unit Economics 1: Net Sales vs Total Post Invoice Discount Amount and Pre-Invoice Discount Amount given by the Company*
Unit Economics 2: Total Cost of Goods Sold (COGS) spent by the Company and then finally got the actual Gross Margin*
Customer and Product Performance analysis based on Net Sales, Gross Margin and Gross Margin %*
Performance Matrix analysis for Market, Customer and Region based on Net Sales and Gross Margin %*
Sales Trend Tooltip for every single Customer based on Net Sales and Gross Margin %*


Key Features in Marketing View:
Unit Economics: There are some Operational Expenses spent for Product. After subtracting this Expenses got the actual scenario of Net Profit*
Performance Matrix analysis for Segment, Category and Product based on both “Net Sales & Net Profit %” and “Net Sales & Gross Margin %” by using a dynamic toggle button*
Key Features in Supply Chain View:
KPI’s for Forecast Accuracy, Net Error, ABS Error*
Risk Factor analysis*
Accuracy vs Net Error Trend analysis*
Key Metrics for both Customer and Products based on FA%, FA% LY, Net Error, Net Error%, Risk Factor*
Key Features in Executive View:
Report Page for the Top Level Management of the Company who want to check on all key metrics and KPI's.

Market Share Trend analysis for AtliQ and other competitors*
Revenue analysis by Division and Channel*
Top 5 Products and Top 5 Customers by Revenue*
Key Insights by Sub Zone with Revenue Contribution % analysis*

Key Learnings.
The most helpful measures for senior management are the Gross Margin and Net Profit (Gross Margin - Operational Costs).
Gross Margin and Net Sales are more significant to the sales team than Net Profit since, in most cases, they have little to no control over operating costs.
Understanding the changes in marketing spend over time and how those changes affect revenue and gross margin is crucial for the marketing team.
Forecast Accuracy & Risk (Out of Stock or Excess Inventory) and Net Error & Absolute Error are crucial KPIs for the supply chain team.
One of the most helpful abilities that aids in the creation of insightful visuals is the managing of stakeholder expectations.
Thank you.
