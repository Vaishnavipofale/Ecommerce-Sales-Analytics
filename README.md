# E-Commerce Sales & Profit Analytics

End-to-end analysis of e-commerce transaction data using Python, SQL Server, and Power BI.

This project analyzes sales performance, profitability, customer behavior, product performance, regional trends, and the impact of discounts on profitability to generate business-oriented insights.

---

## Project Summary

**Dataset:** Sample Superstore Dataset

### Key Metrics

- **Total Sales:** $2,297,200.86
- **Total Profit:** $286,397.02
- **Profit Margin:** 12.47%
- **Total Orders:** 5,009
- **Unique Customers:** 793
- **Unique Products:** 1,862
- **Total Quantity Sold:** 37,873
- **Average Order Value:** $458.61
- **Average Discount:** 15.62%

---

## Project Structure

```text
ecommerce-sales-profit-analysis/

├── data/
│   ├── dictionary/
│   │   └── data_dictionary.csv
│   ├── raw/
│   │   └── ecommerce_raw.csv
│   └── processed/
│       └── ecommerce_clean.csv
│
├── notebooks/
│   ├── ecommerce_sales_profit_analysis.ipynb
│   └── import_data_mssql.ipynb
│
├── powerbi_dashboard/
│   └── powerbi_dashboard.pbix
│
├── screenshots/
│
├── sql/
│   ├── 01_Database_and_Table_setup/
│   ├── 02_Data_cleaning_sql/
│   ├── 03_KPI_Analysis/
│   ├── 04_Customer_Analysis/
│   ├── 05_Product_Analysis/
│   ├── 06_Time_Series_Analysis/
│   ├── 07_Advanced_Business_Question/
│   ├── 08_ETL_Star_Schema/
│   └── ER_Diagram.png
│
├── .gitignore
├── requirements.txt
└── README.md
Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Plotly
SciPy
Jupyter Notebook
SQL Server
T-SQL
SQLAlchemy
Power BI
Requirements
Python 3.7+
Jupyter Notebook
SQL Server
Power BI Desktop
Installation

Install the required Python dependencies using:

pip install -r requirements.txt
Data Description

The project uses the Sample Superstore dataset containing e-commerce transaction-level data.

Primary Columns
Order ID
Order Date
Ship Date
Customer ID
Customer Name
Segment
Region
Category
Sub-Category
Product Name
Sales
Quantity
Discount
Profit
Derived Features

The analysis uses derived features such as:

Year
Quarter
Month
Week
Order-to-Ship Days
Profit Margin
Sales per Quantity
Discount Band
Analysis Components
Python Analysis

The main Jupyter Notebook performs:

Data loading and preprocessing
Data cleaning
Exploratory Data Analysis (EDA)
KPI analysis
Sales trend analysis
Profitability analysis
Category and sub-category analysis
Customer segment analysis
Regional analysis
Product performance analysis
Discount impact analysis
Business insight generation
Interactive Plotly visualizations

Main notebook:

notebooks/ecommerce_sales_profit_analysis.ipynb
SQL Analysis

The SQL component contains analysis covering:

Database and table creation
Data cleaning and validation
KPI analysis
Customer analysis
Product analysis
Time-series analysis
Advanced business questions
ETL processes
Star schema and dimensional modeling

SQL analysis is organized into separate folders under:

sql/
Power BI Dashboard

The Power BI dashboard contains five analytical pages:

Dashboard
Sales
Profit
Customer
Region

The dashboard provides interactive analysis of:

Sales
Profit
Profit Margin
Orders
Customers
Average Order Value
Sales trends
Profit trends
Category performance
Sub-category performance
Product performance
Regional performance

Power BI file:

powerbi_dashboard/powerbi_dashboard.pbix
Additional Business Analysis

Additional analysis was added to investigate specific business problems.

1. Discount & Profitability Analysis

The analysis groups transactions into discount bands and compares their profitability.

Discount Band	Profit Margin
0%	29.51%
1–10%	16.61%
11–20%	11.58%
21–30%	-10.05%
31–40%	-19.44%
40%+	-77.40%

The analysis shows that profit margins decline substantially as discount levels increase.

Business implication: High discounts should be evaluated carefully because aggressive discounting can increase sales activity while significantly reducing profitability.

2. Customer Segment Profitability

Customer segments were analyzed using:

Total Sales
Total Profit
Total Orders
Average Discount
Profit Margin

Key findings:

Consumer generates the highest sales and total profit.
Corporate has a higher profit margin than Consumer.
Home Office has the highest profit margin among the three segments.

Business implication: Customer segments should be evaluated using both revenue and profitability rather than sales volume alone.

3. Product Sub-Category Profitability

Product sub-categories were evaluated using sales, profit, orders, discount levels, and profit margin.

Key findings:

Copiers generate a strong profit margin of 37.20%.
Paper generates a profit margin of 43.39%.
Machines generate approximately $189K in sales but only a 1.79% profit margin.
Supplies have a negative profit margin of -2.55%.
Bookcases have a negative profit margin of -3.02%.
Tables have a negative profit margin of -8.56%.

Business implication: High sales volume does not necessarily mean high profitability. Product-level margin analysis helps identify both profitable and loss-making areas.

Key Findings
Sales Performance
Total Sales: $2.30M
Technology is the highest-performing category by sales.
The West region is a major contributor to overall sales.
California is one of the strongest-performing states by sales.
Profitability
Total Profit: $286.40K
Overall Profit Margin: 12.47%
Profitability varies significantly across categories and product sub-categories.
Some high-sales products and sub-categories generate relatively low or negative profit margins.
Customer Insights
Consumer is the largest customer segment by sales and total profit.
Home Office has the highest profit margin among the three customer segments.
Customer segmentation provides a clearer view of revenue and profitability differences.
Discount Impact
Average Discount: 15.62%
Profit margin decreases as discount levels increase.
Discounts above 20% are associated with negative profit margins in the analyzed discount bands.
The 40%+ discount band has a -77.40% profit margin.
Business Questions Addressed

The project investigates questions such as:

What are the overall sales and profit levels?
What is the overall profit margin?
Which categories generate the highest sales?
Which categories generate the highest profit?
Which product sub-categories are most profitable?
Which product sub-categories generate losses?
How does discounting affect profitability?
Which customer segment generates the most revenue?
Which customer segment has the highest profit margin?
How does sales performance vary by region?
How does sales performance change over time?
Which products contribute most to sales and profit?
Where are potential profitability issues?
How can sales performance be evaluated alongside profitability?

Detailed SQL business questions are available under:

sql/07_Advanced_Business_Question/
Data Pipeline
Raw CSV
   ↓
Data Cleaning
   ↓
Processed Dataset
   ↓
SQL Server Import
   ↓
Dimensional Modeling / Analysis
   ↓
Python Analysis
   ↓
Power BI Visualization
   ↓
Business Insights
Database Schema

The SQL component includes a dimensional/star-schema structure containing:

Dimension Tables
dim_customer
dim_product
dim_date
dim_location
Fact Table
fact_sales

An analytical ecommerce_sales table is also used for analysis.

ER Diagram
sql/ER_Diagram.png
How to Run the Project
Run the Python Analysis
jupyter notebook notebooks/ecommerce_sales_profit_analysis.ipynb
Import Data into SQL Server
jupyter notebook notebooks/import_data_mssql.ipynb
Execute SQL Analysis

Open the SQL files located inside:

sql/

and execute them using SQL Server Management Studio (SSMS) or another compatible SQL environment.

Open the Power BI Dashboard

Open the following file using Power BI Desktop:

powerbi_dashboard/powerbi_dashboard.pbix
Visualizations

The project includes visual analysis using Python and Power BI.

Power BI Dashboard

The Power BI report contains:

Executive Dashboard
Sales Analysis
Profit Analysis
Customer Analysis
Regional Analysis
Python Visualizations

The notebook includes visualizations for:

Monthly Sales Trends
Monthly Profit Trends
Sales by Category
Profit by Category
Sales by Region
Top Products by Sales
Discount vs Profitability
Profit Margin by Customer Segment
Profit Margin by Product Sub-Category
Project Note
