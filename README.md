# Credit Risk Analytics for Smarter Lending Decisions

## Project Overview  

This project analyzes loan application data from Nova Bank to uncover patterns in borrower behavior and default risk across the USA, UK, and Canada. The goal is to support fair, data-driven lending policies that balance accessibility with financial protection.

As a credit risk analyst, I cleaned and prepared a dataset of over 32,000 loan applications using Python in Google Colab, addressing missing values, outliers, and feature engineering. The cleaned dataset was then exported to Excel and modeled in Power BI using a star-schema structure for dashboard development. This semantic model enables executive-level insights into borrower behavior, loan performance, and geographic risk segmentation.

### Business Objectives
- Identify borrower groups more or less likely to default  
- Explore how loan size, income, interest rates, and repayment terms affect risk  
- Assess the impact of employment type, home ownership, and credit history  
- Compare risk patterns across countries (USA, UK, Canada)  
- Recommend policy adjustments to improve lending fairness and reduce exposure

## Nova Bank Key Metrics

**Default Risk Trends**  
Tracking the proportion of loans that default across borrower segments, loan types, and time periods to identify high-risk patterns and early warning signals.

**Loan Portfolio Performance**  
Analyzing loan amounts, interest rates, repayment terms, and total loan cost to assess profitability and exposure across different loan grades and purposes.

**Borrower Profile Insights**  
Evaluating demographic and financial indicators—such as age, income, employment type, and home ownership—to understand which borrower groups are more likely to repay or default.

**Credit History Evaluation**  
Measuring the impact of credit history length, past delinquencies, open accounts, and credit utilization on loan outcomes to refine risk scoring models.

**Geographic Risk Distribution**  
Comparing default rates and borrower behavior across the USA, UK, and Canada to uncover regional lending risks and opportunities for policy adjustment.

**Affordability Ratios**  
Monitoring loan-to-income and debt-to-income ratios to assess borrower repayment capacity and flag over-leveraged applicants.

**Loan Grade and Term Analysis**  
Identifying which loan grades and repayment terms correlate with safer lending outcomes, helping Nova Bank optimize its product offerings.

## Dataset Structure 
The database structure consists of five tables: FactLoan, DimClient, DimClientHistory, DimLoanDetails, and DimLocation, with a total of 32,581 records in the central fact table.



