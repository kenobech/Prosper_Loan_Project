# Prosper Loan Project

## Table of Contents
- [Overview](#overview)
- [Objectives](#objectives)
- [Dataset Features](#dataset-features)
- [Data Cleaning Steps](#data-cleaning-steps)
- [Exploratory Data Analysis](#exploratory-data-analysis)
  - [Univariate Analysis](#univariate-analysis)
  - [Bivariate Analysis](#bivariate-analysis)
  - [Multivariate Analysis](#multivariate-analysis)
- [Key Insights](#key-insights)
- [Conclusion](#conclusion)
- [Files](#files)
- [Requirements](#requirements)
- [How to Run](#how-to-run)

## Overview
The **Prosper Loan Project** is an exploratory data analysis (EDA) of a loan dataset provided by Prosper Company Ltd. The dataset contains 113,937 loans with 81 variables, including loan amount, borrower rate (interest rate), loan status, borrower income, and more. The goal is to uncover patterns, relationships, and insights within the data to better understand borrower behavior and loan characteristics.

## Objectives
The project aims to:
1. Perform data cleaning and preprocessing to prepare the dataset for analysis.
2. Conduct univariate, bivariate, and multivariate exploratory data analysis.
3. Identify features that predict the borrower's Annual Percentage Rate (APR).
4. Explore relationships between employment status, debt-to-income ratio, and other metrics.

## Dataset Features
Key features analyzed include:
- **`listingnumber`**: Unique identifier for each loan listing.
- **`listingcreationdate`**: Date the loan listing was created.
- **`loanoriginalamount`**: Original loan amount.
- **`loanstatus`**: Current status of the loan.
- **`listingcategory (numeric)`**: Category of the loan.
- **`borrowerstate`**: State of the borrower.
- **`borrowerapr`**: Borrower's Annual Percentage Rate.
- **`borrowerrate`**: Borrower's interest rate.
- **`statedmonthlyincome`**: Borrower's stated monthly income.
- **`prosperrating (alpha)`**: Prosper's credit rating for the borrower.
- **`occupation`**: Borrower's occupation.
- **`term`**: Loan term in months.
- **`employmentstatus`**: Borrower's employment status.
- **`totalinquiries`**: Total credit inquiries.
- **`debttoincomeratio`**: Borrower's debt-to-income ratio.
- **`monthlyloanpayment`**: Monthly loan payment amount.
- **`totaltrades`**: Total number of trades.
- **`investors`**: Number of investors funding the loan.

## Data Cleaning Steps
1. Convert column names to lowercase for consistency.
2. Select a subset of important features for analysis.
3. Remove duplicate rows based on `listingnumber`.
4. Convert data types:
   - `totaltrades` and `totalinquiries` to integers.
   - `listingcreationdate` to datetime.
5. Handle missing values:
   - Remove rows without `prosperrating`.
   - Fill missing `occupation` values with "unknown".
   - Fill missing `debttoincomeratio` values with the column mean.
6. Split `listingcreationdate` into separate columns for year, month, day, and time.
7. Drop the original `listingcreationdate` column.

## Exploratory Data Analysis
### Univariate Analysis
- Distribution of loans listed per year, month, and day.
- Distribution of borrower APR, debt-to-income ratio, loan original amount, and stated monthly income.
- Distribution of categorical variables such as occupation, Prosper rating, and employment status.

### Bivariate Analysis
- Correlation between numerical variables.
- Relationships between borrower APR and loan original amount.
- Loan status vs. loan original amount.
- Occupation vs. loan term.

### Multivariate Analysis
- Borrower APR across Prosper rating and loan term.
- Borrower APR across employment status and loan term.
- Stated monthly income and loan original amount across Prosper rating and loan term.

## Key Insights
1. **Loan Listings**:
   - 2013 had the highest number of loans listed, while 2009 had the lowest.
   - January had the highest number of loans listed per month, and April had the lowest.
   - Day 17 had the highest number of loans listed per day.

2. **Borrower APR**:
   - The distribution is multimodal, with peaks at 0.1, 0.2, and 0.36.
   - Borrower APR decreases with an increase in loan term for borrowers with HR-C ratings but increases for those with B-AA ratings.

3. **Employment and Income**:
   - Most borrowers are employed or work full-time, with a stated monthly income around $6,000.
   - Students take the least loans, while borrowers in the "Other" occupation category take the highest number of loans with the longest terms.

4. **Loan Amount**:
   - Most loans are between $1,000 and $20,000.
   - Borrower APR and loan original amount are negatively correlated.

## Conclusion
The analysis provides valuable insights into borrower behavior, loan characteristics, and factors influencing borrower APR. These findings can help Prosper Company Ltd. optimize their loan offerings and better understand their customer base.

## Files
- **`Prosper Loan Project.ipynb`**: Jupyter notebook containing the full analysis.
- **`Prosper Loan Project Cleaned.csv`**: Cleaned dataset used for analysis.

## Requirements
- **Python 3.x**
- Libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`

## How to Run
1. Clone the repository:
   ```bash
   git clone <https://github.com/kenobech/Prosper_Loan_Project.git>
   ```
2. Navigate to the project directory:
   ```bash
   cd Prosper_Loan_Project
   ```
3. Install the required libraries:
   ```bash
   pip install numpy pandas matplotlib seaborn
   ```
4. Open the Jupyter notebook and run the cells sequentially:
   ```bash
   jupyter notebook "Prosper Loan Project.ipynb"
   ```
