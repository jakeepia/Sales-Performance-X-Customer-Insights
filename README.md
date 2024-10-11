# Sales Performance and Customer Insights Analysis

![](img/intro.JPG)

## Introduction
In this project, I developed a Sales Performance and Customer Insights Dashboard to visualize key sales metrics and analyze customer behavior. Below is a breakdown of the workflow, data model, dashboard design, and insights derived from the analysis.

#### Tool Used: Power BI

## 1. Data Preparation and Modeling
#### Fact Table: Sales
This table stores key transactional data related to sales, including:

- **ProductKey:** Links sales to products.
- **OrderDate:** The date of the transaction.
- **CustomerKey:** Links sales to customers.
- **SalesTerritoryKey:** Links sales to specific regions.
- **SalesOrderNumber:** Unique identifier for each order.
- **SalesAmount, DiscountAmount, OrderQuantity, ProductStandardCost:** Key metrics for each transaction.
- **Territories.Region, Territories.Country, Territories.Continent:** Information about the geographical region for each sale.

#### Dimension Tables:
- **Products:** Contains detailed information about each product, such as the product name, category, color, size, and pricing data.
- **ProductCategories:** Categorizes products into meaningful groups (e.g., Bikes, Accessories, Clothing).
- **Customers:** Captures customer demographics, income level, purchase history, and other key attributes.

#### Lookup Table: Calendar
I created a Calendar table for time intelligence that includes:

- **Date, Month, Quarter, Year:** These columns enable detailed time-based analysis, like comparing sales by month or calculating year-over-year changes. The Calendar table is marked as a date table in Power BI to optimize time intelligence functions.

#### Data Transformation (Power Query)
- **Column Cleanup:** Removed irrelevant columns that did not add value to the analysis.
- **Missing Values:** Checked for and handled missing data to ensure the integrity of the final dashboard.

## 2. Data Model and Relationships


The data model connects the fact and dimension tables based on primary and foreign keys. This star schema design enabled efficient data retrieval and optimal performance in Power BI.

- **Sales** is connected to **Customers** via the **CustomerKey**, to **Products** via the **ProductKey**, and to **ProductCategories** through the product hierarchy.
- **Calendar** is linked to **Sales** using the **OrderDate** field, enabling time-based calculations like year-over-year sales, monthly growth, and seasonal trends.


