# Analyze-product-sales-and-revenue-performance.
analyzing product sales data to identify sales trends, customer purchasing behavior, top-performing products, and revenue opportunities.
# 📊 Product Sales Data Analytics Project

### Turning Raw Sales Data into Business Insights

## 🔍 Overview

This project analyzes product sales data to understand business performance, identify top-selling products, and discover opportunities to improve sales.

I worked on the complete data analytics process — from loading Excel data and cleaning it with Python to analyzing data using SQL and building an interactive Power BI dashboard.

The final results are presented through a business report and a professional sales presentation created using Gamma.

**Project Goal:** Help businesses understand their sales performance and make better data-driven decisions.

---

## 🎯 Business Questions

This project answers important business questions:

* How much total revenue did the business generate?
* How many transactions were completed?
* Which purchase channel generates the most sales?
* Which products are the top performers?
* What opportunities can help improve sales?
* How can data be used to support business decisions?

---

## 📁 Dataset

**Dataset:** Product Sales Data

**Format:** Excel (.xlsx)

The dataset contains product sales and customer transaction information.

### Main Columns

| Column          | Description                      |
| --------------- | -------------------------------- |
| Transaction ID  | Unique transaction identifier    |
| Customer Name   | Customer details                 |
| Email           | Customer email                   |
| Job Title       | Customer job title               |
| Product         | Purchased product                |
| Purchase Mode   | Website, App, In-store, or Phone |
| Purchase Date   | Date of purchase                 |
| Purchase Amount | Amount spent                     |
| Payment Status  | Payment status                   |

---

## 🛠️ Tools & Technologies

| Tool                 | Used For                            |
| -------------------- | ----------------------------------- |
| Microsoft Excel      | Data loading and initial inspection |
| Python               | EDA and data cleaning               |
| Pandas               | Data manipulation                   |
| NumPy                | Numerical analysis                  |
| Matplotlib / Seaborn | Data visualization                  |
| PostgreSQL           | SQL data analysis                   |
| MySQL                | SQL querying                        |
| SQL Server           | Business analysis                   |
| Power BI             | Interactive dashboard               |
| Gamma                | Business presentation               |
| GitHub               | Project documentation               |

---

## 🔄 Project Workflow

```text
Excel Dataset
     ↓
Data Loading
     ↓
Exploratory Data Analysis (Python)
     ↓
Data Cleaning
     ↓
SQL Analysis
     ↓
Power BI Dashboard
     ↓
Business Report
     ↓
Gamma Presentation
```

---

## 🐍 1. Data Loading & Exploratory Data Analysis

I loaded the Excel dataset using Python and explored the data to understand its structure and business meaning.

### Activities

* Load Excel dataset using Pandas.
* Review rows and columns.
* Understand data types.
* Analyze numerical and categorical data.
* Check missing values and duplicates.
* Explore product sales and purchase channels.
* Identify important sales patterns.

### Python Example

```python
import pandas as pd

# Load dataset
df = pd.read_excel("Product Sales Data.xlsx")

# View data
print(df.head())

# Dataset information
print(df.info())

# Summary statistics
print(df.describe())

# Missing values
print(df.isnull().sum())
```

---

## 🧹 2. Data Cleaning

The dataset was prepared for accurate analysis by checking and cleaning the raw data.

### Cleaning Activities

* Removed duplicate records.
* Handled missing values.
* Converted dates into the correct format.
* Converted purchase amounts into numeric values.
* Standardized column names.
* Checked data consistency.
* Validated the cleaned dataset.

### Python Example

```python
# Remove duplicates
df = df.drop_duplicates()

# Convert date column
df["Date"] = pd.to_datetime(df["Date"])

# Convert purchase amount
df["Purchase Amount"] = pd.to_numeric(
    df["Purchase Amount"],
    errors="coerce"
)

# Check missing values
print(df.isnull().sum())
```

---

## 🗄️ 3. SQL Business Analysis

The cleaned sales data was analyzed using SQL to answer business questions.

### Databases

* PostgreSQL
* MySQL
* SQL Server

### SQL Analysis

* Total sales revenue.
* Total transactions.
* Average purchase amount.
* Sales by purchase mode.
* Top-selling products.
* Monthly sales performance.
* Customer purchase analysis.

### Example SQL Query

**Total Sales**

```sql
SELECT
    SUM(purchase_amount) AS total_sales
FROM product_sales;
```

**Sales by Purchase Channel**

```sql
SELECT
    purchase_mode,
    SUM(purchase_amount) AS total_sales
FROM product_sales
GROUP BY purchase_mode
ORDER BY total_sales DESC;
```

**Top-Selling Products**

```sql
SELECT
    product,
    SUM(purchase_amount) AS total_sales
FROM product_sales
GROUP BY product
ORDER BY total_sales DESC
LIMIT 5;
```

---

## 📊 4. Power BI Dashboard

I created an interactive Power BI dashboard to present sales performance in a simple and visual format.

### Dashboard Includes

* Total Sales KPI.
* Total Transactions KPI.
* Average Order Value.
* Sales by Purchase Channel.
* Top-Selling Products.
* Monthly Sales Trends.
* Revenue Analysis.
* Interactive filters and slicers.

### Dashboard Purpose

The dashboard helps users quickly understand sales performance and identify areas for business growth.

---

## 📈 5. Business Report

A professional report was prepared to explain the analysis and business findings.

### Report Sections

1. Executive Summary
2. Business Problem
3. Dataset Overview
4. Data Cleaning
5. Exploratory Data Analysis
6. SQL Analysis
7. Power BI Dashboard
8. Key Insights
9. Business Recommendations
10. Conclusion

---

## 🎨 6. Sales Presentation Using Gamma

I created a professional sales presentation using Gamma to communicate the project results clearly to customers, recruiters, and business reviewers.

### Presentation Includes

* Project Overview.
* Sales Performance Overview.
* Revenue Analysis.
* Purchase Channel Analysis.
* Top-Selling Products.
* Key Business Insights.
* Sales Growth Recommendations.

The presentation focuses on attractive visuals, simple explanations, and business storytelling.

---

## 📌 Results & Key Insights

The following results are from the analyzed Product Sales dataset.

| KPI                  |   Result |
| -------------------- | -------: |
| Total Sales          | ₹213,550 |
| Total Transactions   |      326 |
| Average Order Value  |     ₹655 |
| Top Purchase Channel |  Website |
| Website Sales        |  ₹81,070 |

### Top-Selling Products

| Product              |   Sales |
| -------------------- | ------: |
| Organic Choco Syrup  | ₹12,110 |
| Spicy Special Slims  | ₹10,465 |
| Caramel Stuffed Bars |  ₹7,930 |
| Milk Bars            |  ₹7,505 |
| Mint Chip Choco      |  ₹7,390 |

### 💡 Business Insights

**1. Website is the leading purchase channel**

Website sales are ₹81,070, making it the strongest channel in the analyzed results.

**2. Top products contribute important revenue**

Organic Choco Syrup and Spicy Special Slims are the highest-revenue products among the listed top sellers.

**3. Opportunity to increase average order value**

Bundles, add-ons, and cross-selling can be considered to improve the value of each transaction.

---

## 🚀 Business Recommendations

* Focus marketing efforts on the strongest purchase channel.
* Promote top-selling products through targeted campaigns.
* Use bundles and cross-selling to increase order value.
* Monitor sales performance regularly using Power BI.
* Use SQL analysis to support business decisions.

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/product-sales-data-analytics.git
```

### 2. Open the Project Folder

```bash
cd product-sales-data-analytics
```

### 3. Install Python Libraries

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

### 4. Load the Dataset

Place the Excel file in the `data` folder.

```text
data/Product Sales Data.xlsx
```

### 5. Run Python Analysis

```bash
python python/eda.py
```

### 6. Run SQL Queries

Import the cleaned dataset into PostgreSQL, MySQL, or SQL Server.

Run the SQL scripts inside the `sql` folder.

### 7. Open Power BI Dashboard

Open the Power BI file:

```text
powerbi/Product_Sales_Dashboard.pbix
```

Refresh the data if required.

### 8. View the Report & Presentation

Open the files in the `report` and `presentation` folders.

---

## 📂 Project Structure

```text
product-sales-data-analytics/
│
├── data/
│   └── Product Sales Data.xlsx
│
├── python/
│   ├── eda.py
│   └── data_cleaning.py
│
├── sql/
│   ├── postgresql_queries.sql
│   ├── mysql_queries.sql
│   └── sql_server_queries.sql
│
├── powerbi/
│   └── Product_Sales_Dashboard.pbix
│
├── report/
│   └── Product_Sales_Report.pdf
│
├── presentation/
│   └── Product_Sales_Presentation.pptx
│
└── README.md
```

---

## 💼 Skills Demonstrated

* Excel
* Python
* Pandas
* NumPy
* Exploratory Data Analysis
* Data Cleaning
* SQL
* PostgreSQL
* MySQL
* SQL Server
* Power BI
* Data Visualization
* Business Intelligence
* Business Reporting
* Data Storytelling

---

## 👤 Author

**Your Name**

Aspiring Data Analyst | Python | SQL | Power BI | Excel

🔗 LinkedIn: [Your LinkedIn Profile](https://www.linkedin.com/)

🔗 GitHub: [Your GitHub Profile](https://github.com/)

---

## ⭐ Conclusion

This project demonstrates how raw sales data can be transformed into meaningful business insights using Python, SQL, and Power BI.

It showcases practical data analytics skills, business problem-solving, visualization, and communication.

**The project highlights my ability to work with data and present insights in a way that supports business decision-making.**

