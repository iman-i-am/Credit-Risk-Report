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

## Executive Summary

Nova Bank processed 32,851 loan applications across the USA, UK, and Canada, totaling $312 million in requested loan amounts. The average loan was $9,589 with an interest rate of 11%, and borrowers typically requested loans worth 17% of their income.

### Portfolio Health

- **Overall Default Rate**: 21.82%  
- **Non-Defaulted Loans**: 78.18%  
This indicates that roughly 4 in 5 borrowers repay their loans, but nearly 1 in 5 defaults — a meaningful risk exposure.

### Why People Borrow — and How They Repay

Borrowers take loans for a range of reasons. Here's how repayment varies by loan intent:

| Loan Purpose         | % of Defaults | % of Non-Defaults | Insight |
|----------------------|----------------|--------------------|---------|
| Medical              | 22.81%         | 17.47%             | Highest default rate — medical loans carry the most risk. |
| Debt Consolidation   | 20.96%         | 14.61%             | Common reason for borrowing, but repayment is below average. |
| Education            | 15.63%         | 20.97%             | Strong repayment — education borrowers are more reliable. |
| Personal             | 15.45%         | 17.36%             | Mid-range risk, slightly better than average. |
| Venture              | 11.92%         | 19.13%             | High repayment — venture loans show strong performance. |
| Home Improvement     | 13.24%         | 10.46%             | Lower volume, moderate risk. |

### Key Takeaways

- **Top reasons for borrowing**: Debt consolidation, education, and medical expenses.  
- **Highest risk**: Medical loans — borrowers may be financially strained or uninsured.  
- **Best repayment**: Education and venture loans — likely tied to long-term income potential.  
- These insights support Nova Bank’s goal to align loan policies with borrower intent and improve risk-adjusted returns.

### Regional Risk Highlights

### --- INSERT VISUAL HERE

- **UK**: 10,944 applications, 2,378 defaults (22%). Scotland and Manchester showed slightly higher risk than other regions.
- **USA**: 10,852 applications, 2,372 defaults (22%). California and Texas had the most defaults, especially in cities like Dallas and Los Angeles.
- **Canada**: 10,785 applications, 2,358 defaults (22%). Vancouver had the highest default rate across all cities.

### Key Takeaways

- Default rates are consistent across countries, averaging around 22%.
- Urban centers tend to carry more risk.
- Nova Bank may need to adjust lending policies in high-risk cities to reduce exposure.




