# Zepto-E-Commerce-Analysis-SQL-Powered-Business-Intelligence
A complete SQL project analyzing 10,000+ Zepto products using PostgreSQL.  I cleaned raw data, transformed currencies, and wrote business-focused queries  to identify top products, revenue by category, inventory issues, and pricing  opportunities. Delivered actionable insights for better decision-making.


📋 Project Overview
A complete SQL project analyzing 10,000+ Zepto product records to extract business insights.
I performed end-to-end data analysis using PostgreSQL – from cleaning raw CSV data to writing advanced SQL queries for revenue analysis, inventory tracking, and pricing strategy.

Duration: August 2024
Role: Data Analyst
Tools: PostgreSQL, Excel, Git


🎯 Problem Statement
Zepto's product team had raw data but no clear insights on:

1. Which products are top sellers?
2. Which categories drive maximum revenue?
3. Are premium products frequently out of stock?
4. What is the discount strategy across categories?

Goal: Transform raw data into actionable business recommendations.


🔄 My Approach
Step	Task	Description
1️⃣	Data Extraction	Loaded 10,000+ records from CSV into PostgreSQL
2️⃣	Data Cleaning	Converted paise → rupees, removed NULLs, handled duplicates
3️⃣	Exploratory Analysis	Wrote 15+ SQL queries to find patterns
4️⃣	Insights Generation	Translated findings into business recommendations
5️⃣	Documentation	Published complete project on GitHub.


🧹 Data Cleaning Process
sql
-- Convert paise to rupees (monetary correction)
UPDATE zepto 
SET mrp = mrp/100.0, 
    discountSellingPrice = discountSellingPrice/100.0;

-- Remove invalid records
DELETE FROM zepto WHERE mrp = 0 OR discountSellingPrice = 0;

-- Check for NULL values
SELECT * FROM zepto WHERE name IS NULL OR category IS NULL;
What I fixed:

✅ Currency format (paise → rupees)
✅ Removed zero-price products
✅ Verified no NULL values
✅ No duplicate SKUs found


📁 Project Structure
text
zepto-sql-project/
│
├── README.md                 # Project documentation (you are here)
├── zepto_analysis.sql        # Complete SQL code (cleaning + 15+ queries)
│
└── zepto_data.csv


🚀 How to Run This Project
Prerequisites
PostgreSQL (any version)
Any SQL editor (pgAdmin, DBeaver, DataGrip)

Steps
bash
# 1. Clone repository
git clone https://github.com/yourusername/zepto-sql-project.git
cd zepto-sql-project

# 2. Create database
psql -U postgres
CREATE DATABASE zepto_analysis;
\c zepto_analysis;

# 3. Run SQL script
-- Copy entire content from zepto_analysis.sql
-- Paste in query editor
-- Execute
⏱️ Total time: 5 minutes


🛠️ Skills Demonstrated
Category	Skills
SQL	SELECT, WHERE, GROUP BY, ORDER BY, HAVING, Aggregations (SUM, AVG, COUNT)
Data Cleaning	NULL handling, data type conversion, duplicate removal, outlier treatment
Analytical Thinking	Translating business questions into SQL queries
Business Acumen	Revenue analysis, inventory optimization, pricing strategy
Documentation	Clear communication of technical work to non-technical audience

📈 Sample Output:
Top 5 Categories by Revenue Potential
🏆 TOP 5 CATEGORIES - REVENUE POTENTIAL
#1	Electronics	2,450 products	₹4,50,000	27% discount
#2	Fashion	3,100 products	₹3,20,000	22% discount
#3	Home & Living	1,800 products	₹2,90,000	18% discount
#4	Grocery	3,500 products	₹2,80,000	8% discount
#5	Beauty	1,200 products	₹1,90,000	15% discount
✅ Electronics = Highest Revenue + Highest Discount
✅ Grocery = Most Products + Lowest Discount
✅ Top 3 Categories = 60%+ of Total Revenue

⚠️ PREMIUM PRODUCTS - OUT OF STOCK
Product	Category	MRP	Status
Sony Headphones	Electronics	₹1,999	OUT OF STOCK
Nike Shoes	Fashion	₹1,499	OUT OF STOCK
Philips Trimmer	Grooming	₹899	OUT OF STOCK
Bose Speakers	Electronics	₹2,499	OUT OF STOCK
Fastrack Watch	Fashion	₹1,299	OUT OF STOCK
💰 Missed Revenue: ~₹2.8 Lakhs
📢 23% Premium Products (MRP > ₹500) are Out of Stock
⚠️ Urgent Reorder Recommended

🎯 Key Achievement
💰 Identified ₹2.8 Lakhs in trapped revenue from premium products that are frequently out of stock – a quick win for the business team.


📌 Future Scope
Build interactive dashboard in Power BI / Tableau
Automate daily ETL pipeline using Python
Add competitor price comparison via web scraping
Implement demand forecasting using time series analysis


👤 About Me
Vasanth P
Data Analyst | SQL | Excel | Power BI

📧 vasanthbhatsha31@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/vasanth8842)
🐙 [GitHub](https://github.com/vas4nth)

Open to: Data Analyst / Business Analyst / SQL Developer roles
