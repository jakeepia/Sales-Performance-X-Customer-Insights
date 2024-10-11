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





