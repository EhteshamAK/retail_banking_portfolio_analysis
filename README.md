# Retail Banking Portfolio Analysis

## Project Overview

This project analyses a multi-table retail banking dataset using Python, Pandas and Matplotlib.

The goal was to understand customer behaviour, account balances, lending risk, transaction activity and branch performance, and turn the analysis into practical business insights.

The project also demonstrates how data stored across different banking tables can be cleaned, connected using common keys, and analysed together.

---

## Business Objective

The analysis focuses on five areas:

- Customer profile and activity
- Account and deposit performance
- Loan exposure and credit risk
- Transaction behaviour
- Branch performance

The main objective was to identify important patterns in the bank's portfolio and highlight areas that management should monitor or improve.

---

## Dataset

The project uses five related datasets:

### Customers
Contains customer-level information including:

- Age
- Gender
- Geography
- Estimated annual income
- Credit score
- Active-member status
- Customer exit status
- Branch ID

### Accounts
Contains account-level information including:

- Account type
- Current balance
- Overdraft limit
- Account status
- Customer ID

### Loans
Contains lending information including:

- Loan type
- Original loan amount
- Outstanding balance
- Interest rate
- Loan status

### Transactions
Contains monthly account activity including:

- Transaction count
- Inflow amount
- Outflow amount
- Fee revenue
- Digital transaction share

The transaction dataset contains 46,392 account-month records covering 12 months.

### Branches
Contains information for four branches:

- London Central
- Paris Central
- Frankfurt Central
- Madrid Central

---

## Data Preparation

I first inspected all datasets for:

- Dataset dimensions
- Missing values
- Duplicate records
- Data types
- Data-quality issues

A reusable Python loop was used to create a summary of data quality across the five datasets.

The main data-quality issues were found in the customer dataset.

Cleaning included:

- Removing duplicate customer records
- Investigating missing values
- Filling missing annual income using the median income of customers from the same geography
- Labelling unavailable geography as `Unknown`
- Keeping unknown Branch IDs missing rather than assigning unsupported values
- Correcting appropriate data types

---

## Data Integration

The datasets were connected using their common identifiers.

```text
Transactions
     |
  AccountID
     |
  Accounts
     |
 CustomerID
     |
 Customers
     |
  BranchID


## Analysis

### Customer Analysis

The analysis examined:

- Customer distribution by geography
- Average income by geography
- Average credit score by geography
- Active and inactive customers

### Account Analysis

The analysis examined:

- Number of accounts by type
- Total balance by account type
- Average balance by account type
- Account status
- Dormant-account rate

### Loan & Credit Risk Analysis

The analysis examined:

- Number of loans by type
- Outstanding lending exposure
- Average original loan amount
- Loan status
- Late-payment and default rates by loan type
- Average interest rates

### Transaction Analysis

The analysis examined:

- Monthly transaction volume
- Monthly inflows and outflows
- Total annual inflows
- Total annual outflows
- Fee revenue
- Digital transaction share

### Branch Analysis

Using the combined dataset, the analysis examined:

- Customers by branch
- Accounts by branch
- Transaction volume by branch
- Inflows by branch
- Fee revenue by branch
- Digital transaction share by branch

---

## Key Findings

- The UK represented the largest customer market with 996 customers.
- Current accounts were the most common account type.
- Savings accounts held the largest total customer balance.
- ISA accounts had the highest average balance despite having fewer accounts.
- Mortgages represented the largest outstanding lending exposure at approximately £28.8 million.
- Personal loans had the highest default rate at approximately 3.73%.
- Auto loans had the highest late-payment rate at approximately 10.13%.
- Mortgage loans showed the strongest repayment performance, with more than 91% classified as current.
- Total annual inflows were approximately £129.9 million compared with £101.3 million in outflows.
- Approximately 67% of transaction activity was digital.
- London Central was the largest branch by customers, accounts and transaction volume.

---

## Visualisations

Matplotlib was used to visualise:

- Customers by country
- Total balance by account type
- Loan status by loan type
- Monthly transaction volume
- Monthly inflows versus outflows
- Transaction volume by branch

---

## Business Recommendations

### 1. Monitor Personal Loan Risk

Personal loans showed the highest default rate. The bank should monitor this portfolio closely and investigate characteristics associated with higher-risk borrowers.

### 2. Investigate Auto Loan Delinquencies

Auto loans had the highest late-payment rate. Early identification of customers moving into late-payment status could help reduce future defaults.

### 3. Protect the Savings Deposit Base

Savings accounts hold a significant share of customer balances. Retention strategies should focus on protecting these deposits.

### 4. Increase Digital Engagement

Digital transactions represent approximately 67% of activity. Customers with lower digital usage could be targeted for digital-adoption initiatives.

### 5. Compare Branch Performance

London Central leads in customers, accounts and transaction activity. Management could investigate the drivers behind its higher activity and compare them with lower-volume branches.

---

## Tools & Techniques

### Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook / VS Code
- Git & GitHub

### Techniques

- Data inspection
- Missing-value handling
- Duplicate removal
- `groupby()`
- `agg()`
- `transform()`
- `value_counts()`
- `crosstab()`
- Multi-table `merge()`
- Data visualisation
- Business insight generation

---

## Repository Structure

The repository contains:

- `data/` — five source CSV datasets
- `retail_banking_portfolio_analysis.ipynb` — complete Python analysis
- `README.md` — project documentation
- `requirements.txt` — required Python packages

---

## How to Run

Install the required packages:

`pip install -r requirements.txt`

Then open `retail_banking_portfolio_analysis.ipynb` in VS Code or Jupyter Notebook and run the notebook from top to bottom.

---

## Author

Ehtesham Ali Khan
     |
  Branches
