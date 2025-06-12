# 📊 North Wind Trades Analysis

## 📌 Project Overview

This project presents a detailed,Power BI dashboard built on data from **North Wind Trades**, a fictional international trading company. The primary objective of this dashboard is to visualize company-wide performance metrics, including sales distribution, employee productivity, customer demographics, and shipping efficiency. The tool enables stakeholders to quickly explore and assess critical performance indicators across multiple dimensions.

It is designed with interactivity, usability, and business decision-making in mind. Slicers and dynamic charts allow real-time filtering by year and shipping company, helping users identify patterns and trends effortlessly.

📁 Dataset Source

The dataset used in this project is inspired by the sample database Northwind Traders, commonly used for demonstration and training purposes. It simulates a global trading company, containing sales, shipping, and customer data.

🗂️ Originally published by Microsoft and adapted by various open data communities, this dataset mimics real-world business transactions across departments like orders, employees, shipping, and product suppliers.

You can also find similar versions of this dataset hosted publicly on Kaggle:

Northwind Sample Dataset – Kaggle

## ⚙️ Tools and Technologies Used

* **Microsoft Power BI**
* **Slicers for filtering**
* **Treemap, Bar, and Line Graphs**
* **Dashboard Layout & Power Query**

## 📊 Dashboard Components & Visuals

| Section                       | Description                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------ |
| **KPI Tiles**                 | Displays key metrics: Total Sales, Orders, Stock, Countries, etc.              |
| **Employee Sales Chart**      | Highlights sales volume per employee – identifies top contributors             |
| **Shipping Company Filter**   | Allows filtering by shipment provider (e.g., Federal Shipping, Speedy Express) |
| **Year Selector**             | Enables dynamic year-based filtering for 2015, 2016, 2017                      |
| **Top 10 Customer Countries** | Treemap showing countries ranked by sales revenue                              |
| **Sales & Shipping Trend**    | Line chart comparing monthly sales vs shipping charges                         |

## Workflow and Methodology
**Data Inspection**
-Inspected the all tables of the dataset and identify required columns for the analysis.

-Identified the data types and issues with few columns and tables.

**Data Loading**

-Using the GET DATA tab in the Power Bi have uploaded the excel file of the Northwind Traders.

-Loaded the file to the Power Query for further Data Manipulation and Transforming.

-Removed the Columns which are not needed for the analysis, promoted the columns as headers.

-Checked for missing values, Nulls, Duplicates.

**Data Transformation**

-Transformation is needed to get a picture of what story data is trying to tell.

-Merged the Orders and Order details tables using the Order ID.

-Then Merged Orders and Product tables using the Product ID.

-Both tables got merged as Orders table only and removed the columns, duplicated which are not needed for the analysis.

**Data Modelling**

-The goal to model the tables in star schema as it provides better performance, scalability and the path is clear, simple to read for the end user.

-The Fact table is orders table and the remaining tables are Dimension Tables

-Order details table has been not loaded into the desktop as it already got merged with the orders table.

-Products table is loaded as only few required columns are merged with the orders table.


**Key Metrics**

**1.** **Total Sales** **:** Calculate the total sales of all categories across the countries using the function SUM () from the Orders table.

**2. **Customer Countries**:** Calculates the total countries which are customers using the aggregate function COUNT (DISTINCT) from the customers table.

**3. Supplier Countries:** Calculates the total countries which are suppliers using the aggregate function COUNT (DISTINCT) from the suppliers table.

**4. Quantity Ordered:** Calculates the total ordered quantity of all types of categories using the aggregate function SUM () from the orders table.

**5. Quantity in Stock:** Calculates the total quantity of all types of categories in stock using the SUM () from the orders table.

**6. Quantity in order:** Calculates the total quantity ordered from the suppliers of all types of categories in stock using the SUM () from products table.


**Visuals**

**1. **Employees sales**:** The Stacked bar chart represents the employees in descending order of sales for all types of categories. It has a drill down data that shows the individual employee sales for all the categories separately.

**2. **TOP 10 customer countries**:** The tree map shows the countries who are the top customers. Here I have made a drill through to a report showing the geographical map with a pie chart show casing the individual sales for all the categories for each country from the top 10 customers.

**3. Sales and Shipping Over years:** The Area chart presents the trends of the sales over time along with the average shipping charges shipping the good across the countries.

**4. Year and Shipping Company:** The Slicers are used to showcase trends happening across the sales, shipping charges, top 10 customers over the years and by using the different shipping companies.
**5. Cards: **The different cards are showcasing the numbers which has a tooltip to show the sales of individual of the categories, along with the customer countries buying the quantity of the categories.
Model:


## 🔍 Key Insights & Findings
* **Total Sales**: \$348.51K
* **Customer Countries**: 21
* **Supplier Countries**: 16
* **Order Quantity**: 14,000
* **Products in Stock**: 3018
* **Products on Order**: 780

* The **USA** is the leading customer country with over \$80K in sales.
* **Germany** and **Austria** follow as significant contributors.
* **Leverling Janet** is the top-performing employee in total sales volume.
* **Federal Shipping** is the most utilized logistics partner.
* **Sales volume peaks** in **May and December**, with corresponding shipping charges increasing during those months.

These findings can be used to:

* Optimize staffing and marketing during high-sale months
* Reassess shipping partnerships
* Strengthen supplier networks in top-performing countries


