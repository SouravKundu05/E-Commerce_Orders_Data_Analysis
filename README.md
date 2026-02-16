# E-Commerce_Orders_Data_Analysis(Power BI)
📌 Project Overview

This project analyzes an E-Commerce Orders dataset using Power BI to track sales performance, customer behavior, and target achievement across sales teams and managers.

The goal of the dashboard is to help business stakeholders:

Monitor sales performance vs targets

Identify top & underperforming sales managers

Understand customer purchasing patterns

Analyze geographic and category-wise order trends

Detect inactive customers

The dashboard provides interactive visual analytics for decision-making using data modeling, DAX calculations, and advanced visualizations.

🧠 Business Problem

E-commerce companies struggle to track:

Whether sales teams meet targets

Which sales manager performs best

Customer purchase behavior

Order trends across locations & categories

Percentage of inactive customers

This project solves these problems by building a performance monitoring dashboard.

🛠 Tools & Technologies

Power BI

Power Query (Data Cleaning & Transformation)

DAX (Calculated Columns & Measures)

Data Modeling (Relationships)

Interactive Visualizations

🔄 Data Preparation (Power Query)

Performed data cleaning & preprocessing:

Removed empty/null rows

Handled missing Order Source values using most frequent value (Website)

Merged columns to create Sales Manager

Created clean relational model

🧩 Data Modeling

Created relationships:

Orders ↔ Sales Targets (by Sales POC)

Orders ↔ Customers

Bidirectional filtering for accurate analysis

📐 DAX Calculations

Key calculations created:

Sales by Sales POC
SalesbyPOC =
SUMX(
    FILTER(Orders, Orders[Sales POC] = 'Sales Targets'[Sales POC]),
    Orders[Order Value]
)

Target Status Bucket

Target Not Met

Target Met

Target Exceeded

Target Difference

(Actual Sales − Target)

Customers Who Did Not Order %
% Customers Did Not Order =
DIVIDE(
    CALCULATE(SUM(Customers[DidNotOrder])),
    CALCULATE(COUNTROWS(Customers)),
    0
)

📊 Dashboard Features
1️⃣ Sales Performance Analysis

Target achievement classification

Sales vs Target comparison

Average shortfall for underperformers

Team-wise performance

2️⃣ Sales Manager Insights

Total sales by manager

Target completion %

Highest & lowest performers

3️⃣ Customer Analytics

Distinct customers vs orders

Customers who never ordered %

Category & gender segmentation

Average age by category

4️⃣ Order Trends

Monthly sales trend (Line chart)

Orders & average order value

Country-wise order distribution

5️⃣ Geographic Analysis

Map visualization (orders & revenue)

Sales manager performance by country

Drillthrough analysis

6️⃣ Interactive Features

Bookmarks for team-wise views

Drillthrough pages

Filters & slicers

Q&A visual

Mobile layout optimization

📈 Key Insights Derived

Identified top performing sales managers exceeding targets

Found underperforming managers and average shortfall

Measured inactive customer percentage

Detected geographic demand patterns

Observed category-wise customer preferences

👨‍💻 Author

Sourav Kundu
Aspiring Data Analyst | Power BI | SQL | Python | Excel
