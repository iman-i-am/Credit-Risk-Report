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

## Borrower Profile Insights  
**Do gender, age, and marital status affect loan repayment?**

### Gender  
- **Female applicants**: 49.72% of total loans, 3,580 defaults  
- **Male applicants**: 50.28% of total loans, 3,560 defaults  
**Insight**: Default rates are nearly identical across genders, suggesting gender is not a strong predictor of repayment behavior.

### Age Class  
- **Young Adults (20s–30s)**: Largest group for both genders (~50% of loans), with ~1,700 defaults each  
- **Youth (18–25)**: Second largest group, with ~1,400 defaults per gender  
- **Older age groups** (Adult, Middle-aged, Senior, Elderly): Combined share <15%, with lower default volumes  
**Insight**: Younger borrowers (Youth and Young Adults) account for the majority of defaults due to volume, but not necessarily higher risk. Older borrowers show lower default counts, likely due to fewer applications.

### Marital Status  
Across all age groups and genders:
- **Single borrowers** consistently represent ~50% of applications and defaults  
- **Married borrowers** show slightly lower default rates relative to their application share  
- **Divorced and Widowed** applicants have smaller volumes but slightly elevated default ratios in some age brackets  
**Insight**: Being single may correlate with higher default risk, especially among younger applicants. Married borrowers tend to repay more reliably.

### Key Takeaways  
- **Gender is neutral** in predicting default risk  
- **Age matters** — younger borrowers dominate both applications and defaults  
- **Marital status adds nuance** — single borrowers show higher default volumes, while married borrowers are more stable  
These insights support Nova Bank’s goal to identify borrower groups more or less likely to default and refine risk scoring models accordingly.

## Borrower Risk Drivers  
**How education, employment, and home ownership affect loan repayment**

### Education Level  
- **High School**: 13,185 loans, 2,909 defaults (22%)  
- **Bachelor’s**: 11,390 loans, 2,439 defaults (21%)  
- **Master’s**: 6,508 loans, 1,443 defaults (22%)  
- **PhD**: 1,498 loans, 317 defaults (21%)  
**Insight**: Default rates are consistent across education levels, but high school graduates represent the largest volume of defaults due to higher application counts.

### Employment Type  
Across all education levels:
- **Unemployed borrowers** show the highest default rates relative to volume.  
- **Self-employed and part-time workers** also carry elevated risk.  
- **Full-time employees** have the highest loan volumes but slightly lower default ratios.  
**Insight**: Employment stability is a key factor — full-time work correlates with better repayment, while unemployment and gig-based income increase risk.

### Home Ownership  
- **Renters** consistently show the highest default counts across all groups.  
- **Mortgage holders** have moderate risk.  
- **Homeowners (own outright)** show the lowest default rates.  
**Insight**: Renters are the riskiest group, likely due to lower asset security and financial volatility.

### Key Takeaways  
- **Default risk is driven more by employment and housing status than education level.**  
- **Renters and unemployed borrowers** are the most vulnerable segments.  
- Nova Bank should consider stricter affordability checks and risk scoring adjustments for these profiles.

## Loan Amount vs Other Debt  
**How loan size and existing debt levels affect repayment**

Most loan applications fall between **$0–$14,000**, with a peak at **$4,000**. Borrowers in this range tend to have **low to moderate other debt**, and their default rates are relatively low.

- **Moderate debt group** at $4,000: 3,354 applications, average other debt $10,028, default rate **14%**  
- **Low debt group** at $4,000: 1,547 applications, average other debt $3,273, default rate **32%**  
- **High debt group** at $4,000: 359 applications, average other debt $28,025, default rate **7%**

At higher loan amounts ($16,000–$35,000), applications drop, but **default rates increase**, especially for borrowers with **moderate debt**.

- Example: At $32,000, moderate debt group has a **60% default rate**

### Key Takeaways  
- Most borrowers request smaller loans and have manageable debt.  
- Borrowers with **moderate debt** become riskier as loan amounts increase.  
- Nova Bank should watch for high loan requests from moderate-debt applicants — they’re more likely to default.

## Employment Tenure & Income  
**How job experience and income levels impact loan repayment**

### Key Patterns

- **Default risk drops** as employment length increases — from **27%** for those with less than 2 years of experience to **13.4%** for those with 16–19 years.  
- **Median income rises** steadily with tenure, peaking at **$70,000** for borrowers with 11–19 years of experience.  
- **Exception**: Borrowers with **20+ years** of experience show a higher default rate (**24.5%**) despite earning nearly as much ($68,608).

### Key Takeaways

- **Stable employment = lower risk**: Borrowers with 6–19 years of experience are the most reliable.  
- **Newer employees (0–2 years)** are the riskiest group — likely due to income instability.  
- **Unexpected risk** among 20+ year workers may reflect retirement transitions, fixed incomes, or late-career financial strain.

Nova Bank should prioritize mid-tenure borrowers and apply extra scrutiny to both early-career and late-career applicants.

## Loan Risk by Age, Credit History & LTI  
**How borrower age, credit history, and loan-to-income ratio affect default risk**

### Key Patterns

- **Youth (18–25)**:  
  - Shortest credit history (2.99 years)  
  - Highest LTI ratio (0.18)  
  - Largest group: 12,315 applications, 2,860 defaults  
  - **Insight**: High volume and high risk — younger borrowers are more likely to default.

- **Young Adults (26–35)**:  
  - Moderate credit history (5.97 years), LTI ratio 0.17  
  - 16,185 applications, 3,393 defaults  
  - **Insight**: Still high risk due to volume, but slightly better credit behavior.

- **Adults (36–45)**:  
  - Stronger credit history (12.73 years), lower LTI (0.16)  
  - 3,326 applications, 684 defaults  
  - **Insight**: More stable — lower default rate despite fewer applications.

- **Older Age Groups (46+)**:  
  - Longest credit history (16–24 years), lowest LTI ratios (0.15–0.16)  
  - Very few applications, very low defaults  
  - **Insight**: Reliable borrowers, but small segment.

### Key Takeaways

- **Younger borrowers are the riskiest**, due to short credit history and higher LTI ratios.  
- **Older borrowers are more stable**, with longer credit histories and lower default rates.  
- Nova Bank should apply stricter checks for youth and young adult segments, and consider prioritizing mid-age applicants for safer lending.

## Loan Risk by Home Ownership  
**How income ratios affect repayment across housing types**

### Key Patterns

- **Renters**: Highest default count (5,192). They borrow more relative to income and carry more debt.  
- **Mortgage holders**: Lower loan and debt ratios, with fewer defaults (1,690).  
- **Homeowners (own outright)**: Small group, low defaults (193).  
- **Other housing**: Very small group, but defaults are high for their size.

### Key Takeaways

- **Renters are the riskiest group** — they borrow more and default more.  
- **Mortgage holders and homeowners are more stable**.  
- Nova Bank should be cautious with renters and check debt ratios closely before approving loans.

## Loan Grade & Term Impact  
**How loan quality and repayment duration influence default risk**

### Key Patterns

- **Grade A** loans are the safest across all terms — default rates stay around **10%**.  
- **Grades B and C** show moderate risk, with default rates between **15–22%**.  
- **Grades D to G** are high-risk:
  - **Grade D** defaults reach **60%+**  
  - **Grade G** defaults hit **100%** across all terms

- **Shorter terms (12–36 months)** tend to have slightly lower default rates, especially in riskier grades.  
- **Longer terms (60 months)** show higher risk in lower grades (D–G).

### Key Takeaways

- **Grade A loans are the most reliable**, regardless of term.  
- **Default risk rises sharply** from Grade D onward — especially for longer terms.  
- **Optimum term**: 12–36 months for riskier grades; longer terms are safer only for top-grade loans.  
Nova Bank should prioritize Grade A–C loans and apply stricter checks for longer-term loans in lower grades.





