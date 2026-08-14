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
     |
  Branches
