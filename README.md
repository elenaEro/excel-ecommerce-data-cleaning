# excel-ecommerce-data

# 🛒 Customer & Sales Data Cleaning, Transformation, and Analysis in Excel

## 📌 Overview

This project demonstrates how I cleaned, transformed, and analysed raw e-commerce sales, product, and customer data using Excel.

The objective was to prepare a clean, structured dataset that enables business insights on customers, products, sales trends, and delivery performance.

The final file includes:
* Cleaned and standardised customer and product records
* Derived columns for analysis (addresses, delivery dates, payment flags)
* PivotTables summarising sales performance
* Business insights relevant to marketing, product management, and operations

---

## 🔄 Process & Steps

### 1. Data Import & Preparation

* Imported multiple raw files: Orders.xlsx, Products.csv, Customers.txt.
* Converted formatted tables into ranges for easier manipulation.
* Standardised headers, applied filters, resized columns.

**Before**:


<img width="752" height="175" alt="Customers_raw_data" src="https://github.com/user-attachments/assets/65f497e9-655d-4b13-bdfb-ca5f951d1a82" />




**After**:


<img width="752" height="170" alt="Customers_cleaned_data" src="https://github.com/user-attachments/assets/72690f4f-543a-4105-83ac-9bf9deac0b78" />


### 2. Data cleaning

* Removed duplicates in Customers & Products to ensure unique IDs
* Combined first/last names into a Full Name column
* Created a Customer Address field (Street, City, ZIP) for segmentation
* Standardised states/countries (EE.UU. → USA)
* Applied TRIM() to clean trailing spaces in state codes

**Deduping**:

  <img width="800" height="465" alt="Customers_deduping" src="https://github.com/user-attachments/assets/9dbdaf85-1213-45a5-be96-7568d38f2172" />



**Concatenating**:

<img width="210" height="123" alt="Customers_name_before" src="https://github.com/user-attachments/assets/6b2a6b18-eb50-49ed-8cfe-96873f276c3c" />

<img width="606" height="65" alt="Customer_adress_before" src="https://github.com/user-attachments/assets/787e93f7-366b-4d48-8f28-a58551c8bbab" />


<img width="635" height="170" alt="Customers_cleaned_data" src="https://github.com/user-attachments/assets/350191c6-3086-4bff-a94c-17b3f0e3b4bb" />

---

### 3. Data Transformation & Enrichment 

Functions used: IFs, nested IFs, VLOOKUPs, WEEKDAY, TODAY, etc.

* Added to the Order sheet information about Product Category, Product Name and Day of Week, when the order was made, using the VLOOKUPs. They will be useful in future analysis and Pivot Tables.

<img width="698" height="386" alt="Orders_information_VLOOKUP" src="https://github.com/user-attachments/assets/bd5182bd-0eef-47f5-bc54-5c8ba710c835" />


* Added derived columns in Orders:
    Scheduled Delivery Date (calculated from shipping days),
    On-Time Priority Deliveries flag,
    Order Total Sales (corrected sales after discounts),
    Cash Payments categories (Cash Over 200, Cash Not Over 200, Non-Cash).

<img width="887" height="276" alt="Orders_added_columns" src="https://github.com/user-attachments/assets/92db916f-464f-44fe-b144-71f0749863b5" />

* Protected the final Customers sheet to preserve master data integrity

---

### 4. Analysis with Pivot Tables

Created PivotTables to answer key business questions:

* Orders by Market – total orders & quantities by region
* Average Quantity per Order per Market – operational KPI
  
<img width="630" height="160" alt="Pivot_table_regions" src="https://github.com/user-attachments/assets/8ae228c4-7d40-4c81-9c30-5a1c464fe687" />



* Sales by Day of Week – identified peak sales days (Saturday; Week starts from Sunday)
* Sales by Product Category – revealed top categories driving revenue

<img width="269" height="318" alt="Pivot_table_sales_category_weekday" src="https://github.com/user-attachments/assets/110f2f7e-6cce-43f1-8e92-10e34b9c998a" />

* Payments Breakdown – % of orders by payment type

<img width="344" height="171" alt="Pivot_table_payment_breakdown" src="https://github.com/user-attachments/assets/3958da80-edbb-4d11-a91c-f0678a772e64" />

---
## 📊 Business Insights

* Saturdays show peak sales, especially in electronics → opportunity for weekend promotions
* Footwear & Electronics drive a large share of revenue → focus categories for product strategy
* Cash Over $200 orders make up ~10% of transactions → highlight for finance/risk teams
* Same-Day Shipping has ~85% on-time delivery rate → operations performing well, but Standard Shipping lags

## 🛠 Excel Skills Demonstrated
| **Category**                        | **Skills Demonstrated**                                                                                                                                                                           |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Data Import & Preparation**       | Import from Excel & text/CSV files · Sheet structuring · Filters · Column formatting & auto-sizing                                                                                                |
| **Data Cleaning**                   | Remove duplicates · Flash Fill (Full Name) · TRIM() & LEN() for text cleanup · Find & Replace (country names) · Consolidated fields (Customer Address) · Convert formulas to values               |
| **Lookup & Relational Data**        | VLOOKUP / INDEX-MATCH · Linking Orders, Customers, Products, and Dates · Pulling Product Name & Category                                                                                          |
| **Date & Time Handling**            | Created Dates table with Fill Series · Weekday extraction · Scheduled Delivery Date calculation (weekday-only logic)                                                                              |
| **Logical & Conditional Functions** | IF() · AND() · NOT() · Nested IF() (Cash Payments) · Business flags (Expensive Product, On-Time Delivery, Payment Segmentation)                                                                   |
| **Formatting & Validation**         | Currency & Date formatting · Conditional formatting (duplicates, outliers) · Worksheet protection (passwords, locked/unlocked cells)                                                              |
| **PivotTables & Aggregations**      | PivotTables for Market Orders, Avg. Quantity per Order, Sales by Weekday, Category Sales (Saturday filter), Payment Method analysis (% of total) · Calculated fields (averages & % contributions) |
| **Business Metrics (KPIs)**         | Average Product Price · Expensive Product flag · Order Total Sales (factoring discounts) · Market-level performance · Customer & Payment segmentation                                             |


---

## 📁 Files in This Repository

before/ – contains sample raw input files

cleaned-data-ecommerce.xlsx – final cleaned dataset with PivotTables

screenshots/ – images of before/after data cleaning and analysis views

README.md – project documentation (this file)
