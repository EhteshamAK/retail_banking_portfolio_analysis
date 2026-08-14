# Retail Banking Customer Value & Risk Analytics

## Executive summary
This project analyses customer value, engagement, churn, account balances, loan exposure, and transaction behaviour across a multi-table retail banking dataset.

The aim is to answer a management question:

> **Which customer segments create the most value, which segments show the highest risk, and where should the bank focus retention and cross-sell efforts?**

## Why this is portfolio-grade
This is not a single-table charting exercise. The project demonstrates:

- Multi-table data modelling and joins
- Data-quality assessment and cleaning
- KPI design
- Customer segmentation
- Churn and engagement analysis
- Loan risk/exposure analysis
- Transaction trend analysis
- Business recommendations
- Python/Pandas/Matplotlib workflow
- Recruiter-friendly documentation

## Data model
- `customers.csv` — demographic, credit, engagement and churn information
- `accounts.csv` — account products and balances
- `loans.csv` — lending exposure and status
- `transactions.csv` — monthly customer/account activity
- `branches.csv` — branch and region dimension

Primary keys and join keys:
- `CustomerID`
- `AccountID`
- `BranchID`

## Core business questions
1. What is the overall churn rate?
2. Which geographies and customer segments have the highest churn?
3. How does activity status relate to churn?
4. Which customers hold the highest balances and value?
5. Which loan segments create the highest exposure and delinquency risk?
6. How do inflows, outflows, transaction volumes and fee revenue change over time?
7. Does digital engagement vary by age or customer segment?
8. Which customer groups should management prioritise for retention or cross-sell?

## Core KPIs
- Total customers
- Churn rate
- Active-member rate
- Total deposits / account balances
- Average balance per customer
- Total loan outstanding
- Late/default loan rate
- Monthly transaction volume
- Monthly fee revenue
- Digital transaction share

## Recommended final deliverables
- Python notebook with reproducible analysis
- Power BI dashboard
- GitHub README and data dictionary
- Executive summary with 5–8 insights
- LinkedIn portfolio post
- Interview-ready 60-second project explanation

## Repository structure
```text
retail_banking_portfolio_project/
├── data/
│   ├── customers.csv
│   ├── accounts.csv
│   ├── loans.csv
│   ├── transactions.csv
│   └── branches.csv
├── docs/
│   ├── data_dictionary.csv
│   └── project_brief.md
├── notebooks/
│   └── retail_banking_analysis.ipynb
├── README.md
└── requirements.txt
```

## Tech stack
Python, Pandas, NumPy, Matplotlib, Jupyter, Power BI, Git/GitHub.

## Status
Portfolio build in progress.
