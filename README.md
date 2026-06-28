🏦 Banking Client Analytics Dashboard — Power BI

A 4-page interactive Power BI dashboard analysing 3,000 banking clients across loans, deposits, risk profiling, and loyalty segmentation. Built as a portfolio project to demonstrate end-to-end data analyst skills including data transformation, DAX, and visual storytelling.


📁 Repository Structure

banking-client-analytics/
│
├── Banking_Dashboard.pbix        # Power BI report file
├── BankEDA (Version 2)           # Insights
├── BankEDA (Version 1)           # Insights
├── banking-clients.csv           # Raw dataset (3,000 clients, 25 columns)
├── README.md                     # Project documentation
│
└── screenshots/
    ├── home.png
    ├── loan_deposit.png
    ├── deposit_analysis.png
    └── summary.png


📊 Dashboard Pages

Page 1 — Home (Executive Overview)

High-level snapshot of the entire client portfolio for quick business decisions.

VisualPurposeKPI Cards (×5)Total clients, Avg. income, Total deposits, Total loans, Avg. risk scoreDonut chartLoyalty tier distribution (Jade / Silver / Gold / Platinum)Clustered barClients by nationality split by genderTreemapFee structure (High/Mid/Low) cross-referenced with loyalty tierLine chartClient acquisition trend from 1995–2021GaugeAverage risk weighting across all clientsSlicersYear range, Nationality filter

Page 2 — Loan & Deposit (Product Portfolio)

Deep-dive into how clients hold debt and liquidity across different segments.

VisualPurposeKPI Cards (×4)Total loans, Total deposits, Avg. CC balance, Avg. properties ownedScatter plotIncome vs. loan amount (colored by fee structure, sized by risk)Clustered columnLoans vs. deposits by loyalty tierStacked barAccount types (Checking/Saving/Foreign Currency) by fee structure100% Stacked columnCredit card count distribution by loyalty tierMatrix tableAvg. loans, deposits and business lending by nationality (with heatmap)SlicerRisk weighting filter (1–5)

Page 3 — Deposit Analysis (Savings Behaviour)

Focused analysis on how deposits, savings and superannuation are distributed.

VisualPurposeKPI Cards (×3)Total superannuation, Avg. saving accounts, Total depositsFunnel chartAvg. deposits by loyalty tierColumn chartDeposit amount distribution (bucketed: 0–200K / 200K–500K / 500K–1M / 1M+)Area chartDeposit and savings trend by client join yearClustered barSuperannuation savings by age group (20s / 30s / 40s / 50s+)

Page 4 — Summary (Risk & Client Insights)

Boardroom-style summary with risk analysis and AI-powered influencer detection.

VisualPurposeKPI Cards (×5)Avg. risk score, Total business lending, Total properties, Medium/High risk client countKey Influencers (AI visual)Automatically identifies what drives changes in bank depositsClustered barAvg. risk score by fee structure, split by loyalty tierStacked columnBusiness lending by nationality, segmented by fee structure


🔧 Technical Details

Tools Used


Power BI Desktop — report building, visuals, slicers
Power Query (M) — data transformation and calculated columns
DAX — custom measures and KPIs


Power Query Transformations

Calculated ColumnLogicJoin YearExtracted year from Joined Bank date columnAge GroupBucketed Age into 20s / 30s / 40s / 50s+Deposit BucketBanded Bank Deposits into 0–200K / 200K–500K / 500K–1M / 1M+Has Foreign AccountBinary Yes/No flag from Foreign Currency Account > 0Risk CategoryMapped Risk Weighting 1–2 = Low, 3 = Medium, 4–5 = High

DAX Measures

daxTotal Bank Loans = SUM('banking-clients'[Bank Loans])

Total Bank Deposits = SUM('banking-clients'[Bank Deposits])

Avg Estimated Income = AVERAGE('banking-clients'[Estimated Income])

High Risk Clients = 
    COUNTROWS(FILTER('banking-clients', 'banking-clients'[Risk Weighting] >= 4))

Medium Risk Clients = 
    COUNTROWS(FILTER('banking-clients', 'banking-clients'[Risk Weighting] = 3))

Low Risk Clients = 
    COUNTROWS(FILTER('banking-clients', 'banking-clients'[Risk Weighting] <= 2))

Clients w/ Foreign Acct = 
    COUNTROWS(FILTER('banking-clients', 'banking-clients'[Foreign Currency Account] > 0))

Deposit Ratio = 
    DIVIDE(SUM('banking-clients'[Bank Deposits]), SUM('banking-clients'[Estimated Income]))

Loan to Deposit Ratio = 
    DIVIDE(SUM('banking-clients'[Bank Loans]), SUM('banking-clients'[Bank Deposits]))


📂 Dataset Overview

ColumnDescriptionClient IDUnique client identifierAgeClient ageGenderIdClient genderNationalityAfrican / American / Asian / Australian / EuropeanOccupationClient professionLoyalty ClassificationJade / Silver / Gold / PlatinumFee StructureHigh / Mid / LowRisk Weighting1 (low risk) to 5 (high risk)Estimated IncomeAnnual income estimateBank DepositsTotal deposit balanceBank LoansTotal loan balanceSaving AccountsSavings account balanceChecking AccountsChecking account balanceCredit Card BalanceOutstanding CC balanceAmount of Credit CardsNumber of credit cards heldBusiness LendingBusiness loan balanceForeign Currency AccountForeign currency account balanceSuperannuation SavingsRetirement savings balanceProperties OwnedNumber of propertiesJoined BankDate client joined the bank

Total rows: 3,000 | Total columns: 25


💡 Key Insights


European clients account for the largest share of total business lending across all nationalities
Jade tier holds the highest average deposits despite being the largest client segment (44.37%)
High fee structure clients carry a higher average risk weighting than Low fee clients
Superannuation savings are highest in the 30s age group, peaking before the 40s
Risk Weighting ≤ 1 is the strongest influencer for a decrease in bank deposits (Key Influencers visual)



🚀 How to Open


Download and install Power BI Desktop (free)
Clone or download this repository
Open Banking_Dashboard.pbix in Power BI Desktop
If prompted to locate the data source, point it to banking-clients.csv in the same folder



👤 About

Talha — Aspiring Data Analyst | B.Tech Information Technology (2026)

Skilled in SQL, Python, Power BI, Excel and data storytelling. Actively seeking entry-level Data Analyst roles.

Show Image


📄 License

This project is open for viewing and learning purposes. Dataset used for educational/portfolio purposes only.
