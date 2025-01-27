# Tableau Data Analysis

## Bank Loan Dashboard
### Table of Contents

- [Project Description](#project-description)
- [Data Source](#data-source)
- [Data Cleaning](#data-cleaning)
- [Tools](#tools)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results/Findings](#resultsfindings)
  

### Project Description
The project aims to create a comprehensive dashboard to analyze the loans distributed by the bank. In this project, we have created 3 different dashboards that give an in-depth analysis of the loan distribution by various factors.



### Data Source
- Bank Loan Data: The data is available in the "financial_loan.csv" file which contains all the information about the financial loan provided by the bank.

### Tools
- Tableau Public: For data cleaning and visualization.

### Data Cleaning
- In the Tableau Public, we have inserted the csv data. I have checked each column for missing values and formatting issues. I have also checked whether the datatypes assigned to each column are correct.

### Exploratory Data Analysis
Performed some exploratory data analysis to find some information about key questions like
- Total amount funded by the bank and how the funded amount changes every month.
- Total amount received by the bank and how the received amount changes every month.
- What are the different reasons for which customers are asking for a loan?
- What is the status of each loan and whether it can be categorized as a good or bad loan?
- How is the loan distributed by factors like employee length, house ownership, application term, region, and others?

### Data Analysis
To find the answer to the key questions, I have created some calculated fields in the Tableau as
```Tableau
MTD FUNDED AMOUNT = SUM(IF 
DATEDIFF('month', [Issue Date],{MAX([Issue Date])}) = 0 THEN [Loan Amount]
END)
```

### Results/Findings
[Dashboard View](https://public.tableau.com/app/profile/manjeet.kumar8420/viz/Loan_17379546179610/Overview)

- Total loan applications is around 38.6K. Out of which, 5.3K loan applications are bad.
- Most of the customers who are taking loans are working employees with 10+ years of job experience.
- The major purpose for taking the loan is to settle the debt.
- The loan applications are applied by customers who live in rented houses or mortgage.
- Around 77% of loan applications are issued for 36 months.
- California and New York are the 2 states where most applications are issued.
