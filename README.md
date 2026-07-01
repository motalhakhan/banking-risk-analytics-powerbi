Banking Risk Analytics & Loan Approval Dashboard

An end-to-end credit risk analytics pipeline that identifies high-risk loan applicants and supports data-driven Approve/Reject decisions for a simulated banking entity — built on a normalized MySQL database, feature-engineered with Python, and visualized in an interactive Power BI dashboard.


🧭 Overview

This project simulates a real-world banking analytics workflow: raw client and relationship data is modeled into a relational database, enriched with engineered risk features in Python, and surfaced through a Power BI dashboard that consolidates key credit risk KPIs into a single decision-support view — reducing the manual effort needed to review loan applicants.


🛠️ Tech Stack

LayerToolsDatabaseMySQLData Processing / Feature EngineeringPython (Pandas)VisualizationPower BI


🗄️ Database Design

Architected a normalized relational schema in MySQL with Primary/Foreign key constraints across three interconnected tables, ensuring referential integrity across 1,000+ records:


Client — core applicant demographic and financial details
Banking Relationship — account tenure, product holdings, and engagement history
Investment Advisor — advisor assignment and portfolio management details


The tables are linked via foreign keys to maintain data consistency and support multi-table joins for risk analysis.

Client (1) ───< Banking_Relationship (M)
Client (1) ───< Investment_Advisor (M)

(Replace with your actual ER diagram / schema image once added — see Repository Structure below.)


⚙️ Feature Engineering

Using Python (Pandas), new features were engineered from raw relationship and client data to improve applicant risk profiling and predictive accuracy, including:


Engagement Timeframe — a derived metric capturing the duration/depth of a client's banking relationship, used as a signal for credit reliability
Additional derived fields supporting segmentation and risk scoring (e.g., tenure buckets, product usage ratios)



📊 Power BI Dashboard

An interactive Power BI dashboard consolidates 5+ credit risk KPIs into a single decision-support view, including:


Repayment Probability
Default Rate
Client Segmentation (risk tiers)
Loan Approve/Reject Distribution
Engagement Timeframe Trends


The dashboard reduces manual review complexity by giving credit teams a consolidated, filterable view of applicant risk instead of scanning raw records table by table.

(Add dashboard screenshots here once exported, e.g. /assets/dashboard-overview.png)


📁 Repository Structure

├── data/                   # Raw and processed datasets
├── notebooks/               # Python (Pandas) feature engineering notebooks/scripts
├── powerbi/                  # .pbix dashboard file
├── assets/                    # Screenshots, ER diagrams
└── README.md


🚀 How to Reproduce


Set up the database


bash   mysql -u <user> -p < sql/schema.sql


Load and process data


bash   pip install pandas mysql-connector-python
   python notebooks/feature_engineering.py


Open the dashboard

Open powerbi/loan_approval_dashboard.pbix in Power BI Desktop
Refresh the data source to point to your local MySQL instance


Ensured referential integrity across 1,000+ client records via normalized 3NF schema design
Reduced manual credit review effort through a single consolidated KPI view
Improved risk profiling accuracy with engineered features like Engagement Timeframe
