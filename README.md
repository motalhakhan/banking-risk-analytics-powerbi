📌 Project Overview

Financial institutions receive thousands of loan applications every day. Evaluating each applicant manually is time-consuming and prone to inconsistencies.

This project builds a complete analytics pipeline that:

Stores customer banking data in a normalized MySQL database
Cleans and transforms data using Python
Engineers additional business features for better risk profiling
Visualizes key banking and credit risk metrics in Power BI
Helps decision-makers identify whether an applicant should be Approved, Reviewed, or Rejected
🎯 Objectives
Analyze customer financial behavior
Identify high-risk loan applicants
Improve loan approval decisions using data
Monitor important banking KPIs
Build an interactive dashboard for stakeholders
🛠 Tech Stack
Technology	Purpose
Python (Pandas, NumPy)	Data Cleaning & Feature Engineering
MySQL	Relational Database
SQL	Data Extraction & Analysis
Power BI	Dashboard & Visualization
Excel/CSV	Source Dataset
📂 Project Structure
Banking-Risk-Analytics/
│
├── Dataset/
│   ├── Client.csv
│   ├── Banking_Relationship.csv
│   └── Investment_Advisor.csv
│
├── SQL/
│   ├── Database.sql
│   ├── Table_Creation.sql
│   ├── Constraints.sql
│   └── Analysis_Queries.sql
│
├── Python/
│   ├── Data_Cleaning.ipynb
│   ├── Feature_Engineering.ipynb
│   └── Export_Data.ipynb
│
├── PowerBI/
│   └── Banking_Risk_Dashboard.pbix
│
├── Images/
│   ├── Dashboard.png
│   └── ER_Diagram.png
│
└── README.md
🗄 Database Design

The project uses a normalized relational database consisting of three interconnected tables.

Tables
Client

Contains customer demographic and financial information.

Example columns

Client_ID (Primary Key)
Name
Age
Gender
Income
Occupation
Credit Score
Banking Relationship

Contains customer banking details.

Example columns

Relationship_ID
Client_ID (Foreign Key)
Account Type
Loan Amount
Loan Status
Balance
Repayment History
Investment Advisor

Contains investment and portfolio information.

Example columns

Advisor_ID
Client_ID (Foreign Key)
Investment Type
Portfolio Value
Risk Category
Database Relationships
Client
   │
   ├──────────────┐
   │              │
Banking      Investment
Relationship   Advisor
Primary Keys
Foreign Keys
Referential Integrity
Normalized Schema
🐍 Python Workflow
Data Cleaning
Removed duplicates
Handled missing values
Standardized column names
Converted data types
Corrected inconsistent values
Feature Engineering

Created additional business features such as:

Engagement Timeframe

Measures customer relationship duration with the bank.

Example:

Engagement Timeframe =
Current Date − Customer Joining Date

Additional engineered insights include:

Customer Age Groups
Income Segmentation
Loan Categories
Credit Risk Labels
📊 Power BI Dashboard

The dashboard provides an interactive overview of banking performance and loan risk.

Key KPIs
Total Clients
Total Loan Applications
Loan Approval Rate
Default Rate
Average Credit Score
Total Loan Amount
Repayment Probability
High-Risk Clients
Client Segmentation
Portfolio Value
Dashboard Features
Interactive Filters
Client Drill-down
Loan Risk Analysis
Regional Analysis
Customer Segmentation
Credit Score Distribution
Repayment Trends
Investment Overview
📈 Business Insights

The dashboard helps answer questions such as:

Which customers have the highest probability of default?
Which age groups receive the most loans?
Which customer segment has the highest repayment rate?
What factors influence loan approval?
Which clients require manual review?
Which investment categories carry higher risk?
📸 Dashboard Preview

Add your dashboard screenshot here.

Images/Dashboard.png
🚀 How to Run
1. Clone Repository
git clone https://github.com/yourusername/Banking-Risk-Analytics.git
2. Import Database

Run SQL scripts inside the SQL folder.

Database.sql
Table_Creation.sql
Constraints.sql
3. Run Python Scripts

Install required libraries.

pip install pandas numpy matplotlib

Execute:

Data_Cleaning.ipynb
Feature_Engineering.ipynb
4. Open Power BI

Open:

Banking_Risk_Dashboard.pbix

Refresh the data connection.

📊 Sample KPIs
KPI	Description
Total Clients	Number of banking customers
Loan Approval Rate	Percentage of approved loans
Default Rate	Percentage of customers likely to default
Average Credit Score	Mean customer credit score
Total Loan Amount	Sum of sanctioned loans
High-Risk Clients	Customers flagged as risky
Repayment Probability	Estimated likelihood of repayment
💡 Skills Demonstrated
Data Cleaning
Feature Engineering
SQL Queries
Database Design
Data Modeling
Power BI Dashboard Development
KPI Design
Business Intelligence
Credit Risk Analytics
Banking Analytics
Data Visualization
Relational Database Management
📚 Future Improvements
Add Machine Learning model for loan approval prediction
Integrate real-time banking data
Implement customer churn prediction
Deploy dashboard using Power BI Service
Add predictive credit scoring model
Automate ETL pipeline
📌 Project Highlights

✔ End-to-End Data Analytics Project

✔ Normalized MySQL Database (3 Tables)

✔ 1,000+ Banking Records

✔ Python-Based Data Cleaning & Feature Engineering

✔ Interactive Power BI Dashboard

✔ Credit Risk & Loan Approval Analytics

✔ Business-Oriented KPIs

✔ Decision Support for Banking Institutions
