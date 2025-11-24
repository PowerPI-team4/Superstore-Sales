# Superstore Sales Dashboard (Power BI)

This repository contains a Power BI report built from two source datasets: **Superstore Sales Dataset.csv** and **Superstore.csv**. The resulting Power BI file (`Superstore Sales_Team4_Nov 24 2025.pbix`) includes a complete analytical dashboard and multiple report pages focusing on products, annual sales, units sold, sales by location, profit contribution, and customer analysis.

---

## 📊 Report Overview

The Power BI report provides a set of interactive visuals and pages that highlight performance across several business dimensions. The report typically includes:

### **1. Sales Overview Dashboard**

A consolidated dashboard with:

* Total Sales
* Total Profit
* Quantity Sold
* Top-performing and underperforming categories
* Trends over time

### **2. Category & Subcategory Analysis**

Breakdowns of sales and profit by:

* Product Category
* Product Sub-Category
* Product Name

### **3. Customer Insights**

Analysis of:

* Customer segments (Consumer, Corporate, Home Office)
* Contribution to revenue

### **4. Geographic Analysis**

A regional performance view that compares:

* Sales and profit across states
* High-density order cities

### **5. Order & Shipping Patterns**

Visuals showing:

* Order processing times
* Shipping modes and their impact on sales & returns

---

## 🗂 Data Model

The PBIX file combines both datasets into a unified analytical model. Key tables include:

* **Orders Table** – combines order details from the two CSV files
* **Products Table** – product metadata, categories, and subcategories
* **Customer Table** – customer profiles and segment information
* **Location Table** – country, state, region, and city information

Relationships follow a star-schema pattern:

* Customers, Products, Location → linked to → Fact Orders

The model also includes calculated columns and DAX measures such as:

* Total Sales
* Total Profit
* Profit Ratio
* Sales YoY
* Running Totals
* Category Contribution %
* Customer Gender Column
* Customer Age Column
* COGS
* Customer Staisfaction Column

---

## 📘 Data Dictionary

Below is a consolidated description of the main fields used in the report.

### **Order Fields**

| Field          | Description                                    |
| -------------- | ---------------------------------------------- |
| **Row ID**     | Unique row identifier in the dataset           |
| **Order ID**   | Unique identifier for each order transaction   |
| **Order Date** | Date the customer placed the order             |
| **Ship Date**  | Date the order was shipped                     |
| **Ship Mode**  | Shipping method (Standard, Second Class, etc.) |
| **Quantity**   | Number of units sold                           |
| **Sales**      | Total revenue generated from the order line    |
| **Profit**     | Profit earned on the transaction               |

### **Customer Fields**

| Field             | Description                                       |
| ----------------- | ------------------------------------------------- |
| **Customer ID**   | Unique identifier for each customer               |
| **Customer Name** | Full name of the customer                         |
| **Segment**       | Customer group (Consumer, Corporate, Home Office) |

### **Product Fields**

| Field            | Description                                         |
| ---------------- | --------------------------------------------------- |
| **Product ID**   | Unique identifier for the product                   |
| **Product Name** | Product description                                 |
| **Category**     | Main product category (Furniture, Technology, etc.) |
| **Sub-Category** | More detailed product classification                |

### **Geographic Fields**

| Field           | Description                          |
| --------------- | ------------------------------------ |
| **Country**     | Country of the customer/transaction  |
| **Region**      | Region within the country            |
| **State**       | State or province of the transaction |
| **City**        | City of the transaction              |
| **Postal Code** | ZIP/postal code                      |

---

## 📝 Notes

* The Power BI model merges two provided Superstore datasets for a richer, more complete analysis.
* All visuals are built using DAX measures tailored for sales analytics.
* This repository is suitable for learning, portfolio presentation, or demonstration purposes.
