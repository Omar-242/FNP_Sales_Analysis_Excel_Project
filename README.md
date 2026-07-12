# 🌸 Ferns N Petals (FNP) Sales Analysis Dashboard | Excel Data Analysis Project

## 📌 Project Overview

This project analyzes sales data from **Ferns N Petals (FNP)**, India's largest gifting and floral retailer specializing in flowers, cakes, plants, and personalized gifts.

The objective of this project is to transform raw sales data into meaningful business insights using **Microsoft Excel**, **Power Query**, **Power Pivot**, **Data Modeling**, **DAX**, **Pivot Tables**, and **Interactive Dashboards**.

The final dashboard helps business stakeholders understand customer behavior, product performance, revenue trends, delivery efficiency, and seasonal demand.

---

# 🎯 Project Objectives

The project aims to answer the following business questions:

1. What is the total revenue generated?
2. What is the average order-to-delivery time?
3. How do monthly sales vary throughout the year?
4. Which products generate the highest revenue?
5. How much do customers spend on average?
6. How do the top 5 products perform in terms of sales?
7. Which cities place the highest number of orders?
8. Does order quantity affect delivery time?
9. How does revenue vary across different occasions?
10. Which products are most popular for different occasions?

Additional business insights:

* Revenue by Day of the Week
* Top 5 Ordering Hours

---

# 📂 Dataset

The project uses three different datasets.

## Customer Table

Contains customer information.

| Column         |
| -------------- |
| Customer_ID    |
| Name           |
| City           |
| Contact_Number |
| Email          |
| Gender         |
| Address        |

Example

| Customer_ID | Name          | City        | Gender |
| ----------- | ------------- | ----------- | ------ |
| C001        | Tara Krishnan | Panchkula   | Female |
| C002        | Myra Edwin    | Bulandshahr | Female |
| C003        | Jayesh Lanka  | Bilaspur    | Male   |

---

## Orders Table

Contains order-level transaction data.

| Column              |
| ------------------- |
| Order_ID            |
| Customer_ID         |
| Product_ID          |
| Quantity            |
| Order_Date          |
| Order_Time          |
| Delivery_Date       |
| Delivery_Time       |
| Location            |
| Occasion            |
| Month               |
| Hour                |
| Diff_Order_Delivery |
| Price (INR)         |
| Revenue             |
| Day Name            |

---

## Product Table

Contains product information.

| Column       |
| ------------ |
| Product_ID   |
| Product_Name |
| Category     |
| Price (INR)  |
| Occasion     |
| Description  |

---

# 🛠 Tools Used

* Microsoft Excel
* Power Query Editor
* Power Pivot
* Data Model
* DAX
* Pivot Tables
* Pivot Charts
* Slicers

---

# 🔄 Data Extraction

The datasets were imported using **Power Query**.

```
Data
   → Get Data
      → From Folder
         → Power Query Editor
```

Using Power Query makes the workflow dynamic, allowing new data files to be refreshed automatically without rebuilding the dashboard.

---

# 🧹 Data Transformation (Power Query)

Several data cleaning and transformation steps were performed before analysis.

### Data Cleaning

* Converted **Contact_Number** to Text datatype
* Changed date format from **DD-MM-YYYY** to **MM-DD-YYYY**
* Standardized data types

### Feature Engineering

Created several new columns:

* Month (from Order_Date)
* Order Hour (from Order_Time)
* Delivery Time Taken (Delivery_Date − Order_Date)

### Data Merge

Performed a **Left Outer Join** between:

* Orders Table
* Product Table

This merge added the **Price (INR)** column into the Orders table, enabling revenue calculation.

Finally, the cleaned data was loaded into the Excel Data Model.

---

# 🏗 Data Modeling

Instead of creating Pivot Tables directly from worksheets, the project uses Excel's **Data Model**.

### Why Data Model?

Creating Pivot Tables from the Data Model allows combining multiple related tables, similar to relational databases.

The following steps were performed:

* Loaded tables into the Data Model
* Opened Power Pivot
* Created relationships using Diagram View
* Built a **Star Schema**

### Data Model

```
             Customer
                 |
                 |
Orders ---------------- Product
```

Orders acts as the **Fact Table**, while Customer and Product are Dimension Tables.

---

# 📈 DAX

A calculated column was created to compute revenue.

```
Revenue = Quantity × Price
```

This DAX calculation allows revenue to update automatically whenever the dataset changes.

---

# 📊 Data Analysis

Ten Pivot Tables were created to answer key business questions.

| Analysis                            | Visualization              |
| ----------------------------------- | -------------------------- |
| Total Revenue                       | KPI Card                   |
| Average Delivery Time               | KPI Card                   |
| Monthly Sales Performance           | Bar Chart                  |
| Top Products by Revenue             | Bar Chart                  |
| Customer Spending Analysis          | Bar Chart                  |
| Sales Performance of Top 5 Products | Bar Chart                  |
| Top 10 Cities by Orders             | Bar Chart                  |
| Order Quantity vs Delivery Time     | KPI + Correlation Analysis |
| Revenue by Occasion                 | Bar Chart                  |
| Product Popularity by Occasion      | Bar Chart                  |

---

# 📌 Additional Insights

Two additional business analyses were performed:

### Revenue by Day

Shows which weekday generates the highest revenue.

### Peak Ordering Hours

Identifies the top five hours during which customers place the most orders.

These insights can help optimize staffing, inventory management, and marketing campaigns.

---

# 📉 Correlation Analysis

To determine whether larger orders require longer delivery times, a correlation analysis was performed between:

* Order Quantity
* Delivery Time Taken

**Correlation Coefficient**

```
0.0034
```

### Interpretation

The correlation coefficient is extremely close to **0**, indicating **no meaningful relationship** between order quantity and delivery time.

This suggests that FNP's delivery operations remain efficient regardless of order size.

---

# 🎛 Interactive Dashboard

The dashboard includes the following interactive slicers:

* Category
* Occasion
* City
* Gender
* Month

These filters allow users to dynamically explore the data from different perspectives.

---

# 📌 Dashboard Features

* KPI Cards
* Interactive Slicers
* Pivot Charts
* Dynamic Filtering
* Business Insights
* Revenue Analysis
* Customer Analysis
* Product Performance
* Delivery Performance
* Occasion-wise Analysis

---

# 📷 Dashboard Preview

> Add your dashboard screenshot here.

```
Dashboard.png
```

---

# 📚 Key Excel Skills Demonstrated

* Power Query (ETL)
* Data Cleaning
* Data Transformation
* Data Modeling
* Star Schema
* Power Pivot
* DAX Calculations
* Pivot Tables
* Pivot Charts
* KPI Cards
* Interactive Dashboard Design
* Business Analysis
* Correlation Analysis
* Slicers

---

# 💼 Business Insights

* Identified the overall revenue generated by the business.
* Measured average delivery time to evaluate operational efficiency.
* Analyzed monthly sales trends throughout the year.
* Identified the highest revenue-generating products.
* Examined average customer spending behavior.
* Evaluated the sales performance of the top five products.
* Identified the cities contributing the highest number of orders.
* Confirmed that order quantity has almost no impact on delivery time.
* Compared revenue across different occasions.
* Determined the most popular products for each occasion.
* Identified the weekdays generating the highest revenue.
* Found the peak hours when customers place the most orders.

---

# 🚀 Conclusion

This project demonstrates an end-to-end Excel data analysis workflow, starting from raw data extraction using Power Query, followed by data transformation, relational data modeling, DAX calculations, business analysis, and interactive dashboard creation. It showcases practical skills in Excel that are widely used in real-world data analyst roles and highlights how raw transactional data can be transformed into actionable business insights for decision-making.

---

## 👨‍💻 Author

**Omar Faruque Chowdhury**

Aspiring Data Analyst

### Skills

* Excel
* Power Query
* Power Pivot
* DAX
* Data Visualization
* Business Analysis
