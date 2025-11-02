🛍️ Customer Shopping Behavior Analysis

Using Python, PostgreSQL, and Power BI

📘 1. Project Overview

This project explores customer shopping behavior using transactional data from 3,900 purchases across multiple product categories.
The goal is to uncover actionable insights into spending patterns, customer segmentation, product preferences, and subscription trends — ultimately helping guide data-driven business decisions.

📊 2. Dataset Summary

Rows: 3,900

Columns: 18

Key Features:

Customer Demographics: Age, Gender, Location, Subscription Status

Purchase Details: Item Purchased, Category, Purchase Amount, Season, Size, Color

Shopping Behavior: Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

Missing Data: 37 missing values in the Review Rating column

🧮 3. Exploratory Data Analysis (Python)

Data preprocessing and cleaning were performed using pandas and NumPy in Python.

Steps:

Data Loading: Imported dataset using pandas.read_csv().

Initial Exploration: Used df.info() and df.describe() for structure and summary statistics.

Missing Data Handling: Imputed missing Review Rating values using the median rating per category.

Column Standardization: Converted column names to snake_case for clarity.

Feature Engineering:

Created age_group by binning customer ages.

Derived purchase_frequency_days from timestamps.

Data Consistency Check: Identified redundancy between discount_applied and promo_code_used; dropped the latter.

Database Integration: Connected to PostgreSQL and loaded the cleaned dataset for SQL-based analysis.

🧠 4. Data Analysis using SQL (Business Insights)

Structured SQL queries in PostgreSQL were used to answer key business questions:

Revenue by Gender – Compare total revenue from male vs. female customers.

High-Spending Discount Users – Identify customers who used discounts yet spent above average.

Top 5 Products by Rating – Rank products with the highest average reviews.

Shipping Type Comparison – Compare purchase amounts across Standard vs. Express shipping.

Subscribers vs. Non-Subscribers – Evaluate spending and total revenue by subscription status.

Discount-Dependent Products – Find products most often bought with discounts.

Customer Segmentation – Classify customers into New, Returning, and Loyal segments.

Top 3 Products per Category – Identify best-selling products within each category.

Repeat Buyers & Subscriptions – Examine correlation between purchase frequency and subscription.

Revenue by Age Group – Quantify revenue contribution across different age brackets.

📈 5. Power BI Dashboard

An interactive Power BI dashboard visualizes the insights derived from SQL and Python analysis.
It includes:

Customer segmentation by demographics and loyalty level

Revenue breakdown by category, age, and shipping type

Product ratings and discount dependency analysis

Subscription trends and profitability visualization

💡 6. Business Recommendations

Based on the analysis, the following actions are suggested:

Boost Subscriptions: Offer personalized incentives and exclusive perks.

Customer Loyalty Programs: Reward frequent buyers to encourage retention.

Review Discount Policies: Balance discount campaigns to maintain profit margins.

Product Positioning: Promote top-rated and best-selling items in marketing efforts.

Targeted Marketing: Focus on high-revenue demographics and express-shipping users.

🧰 7. Tech Stack

Python: pandas, numpy, matplotlib, seaborn, psycopg2, sqlalchemy

Database: PostgreSQL

Visualization: Power BI

Environment: Jupyter Notebook / VS Code

📂 8. Project Structure
Customer_Behavior_Analysis/
│
├── data/
│   └── customer_behavior.csv
│
├── notebooks/
│   └── data_cleaning_eda.ipynb
│
├── sql/
│   └── business_queries.sql
│
├── dashboard/
│   └── customer_behavior.pbix
│
├── src/
│   └── db_connection.py
│
└── README.md

🚀 9. How to Run

Clone the repository

git clone https://github.com/<your-username>/Customer-Behavior-Analysis.git
cd Customer-Behavior-Analysis


Install dependencies

pip install -r requirements.txt


Update PostgreSQL credentials in db_connection.py.

Run Jupyter Notebook for data cleaning and EDA.

Open Power BI file (.pbix) for dashboard visualization.

📢 10. Results Summary

Identified key customer segments driving 70% of total revenue.

Found discount usage increases purchase frequency but lowers margins.

Subscribers spend 1.4× more on average than non-subscribers.

Express shipping users have the highest average transaction value.
