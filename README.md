# excel-ecommerce-data

# 🛍 Excel Case Study: Preparing E-commerce Data for Marketing & Product Analytics

**Headline:**  
Cleaned and structured raw e-commerce product, customer, and order data in Excel to make it ready for analysis in SQL, Power BI, and other BI tools.

---

## 📌 Overview
This project simulates a real-world data preparation task for an e-commerce company.  
The goal was to consolidate and clean customer, product, and order data so it could be used for marketing and product analytics.  

The raw files came from different sources — an Excel workbook, csv, and a text file. They contained duplicates, inconsistent formats, and unnecessary columns.  
I imported the data into Excel, applied consistent formatting, removed duplicates, merged name fields, and created a complete date lookup table.  

By the end, the dataset was clean, easy to navigate, and ready to be analysed in Excel, SQL, or Power BI.

The process demonstrated skills in **data importing, cleaning, formatting, and structuring for analysis** — essential for analytics roles.

---

## 🔄 Process & Steps

### 1. Data Import & Formatting
- Imported product data from `1_1_importing_files.xlsx` and customer data from `DataCo_Customers.txt` (You can find them in the `Before` folder)
- Chose “No formatting” table style and converted tables to ranges
- Renamed sheets: `Products`, `Customers`
- Applied consistent formatting: bold yellow headers, filters, adjusted column widths

### 2. Duplicate Detection & Removal
- **Products sheet**: Highlighted duplicate `Product Id` values and removed 1210 duplicates using all columns
- **Customers sheet**: Highlighted duplicate `Customer Id` values and removed 231 duplicates using all columns

### 3. Merging Name Fields
- Combined `Customer Fname` and `Customer Lname` into a single `Full Name` column using Flash Fill
- Deleted redundant first/last name columns to reduce dataset width

### 4. Creating a Date Lookup Sheet
- Added a new sheet `Dates` containing every day from `1/1/2015` to `12/31/2018`
- Used Fill Series to generate the range
- Formatted header to match other sheets

---

## 🛠 Excel Skills Demonstrated
- Importing Excel & text data
- Table-to-range conversion
- Column formatting & filters
- Conditional formatting for duplicates
- Duplicate removal across datasets
- Flash Fill for quick text concatenation
- Creating lookup tables with Fill Series

---

## 📁 Files in This Repository
