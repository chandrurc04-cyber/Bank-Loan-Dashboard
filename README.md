# Bank-Loan-Dashboard
📌 Project Overview

Banks need a reliable way to monitor loan applications, funded amounts, repayments, and overall portfolio risk. This project builds a 3-dashboard Power BI solution that gives management a complete view of lending operations — from high-level KPIs down to individual loan-level details.
    
Data pipeline: SQL Server (data storage & querying) → Power Query (cleaning & transformation) → Power BI (modeling, DAX, visualization)

🎯 Problem Statement

The bank required a reporting solution to answer:

  1. How many loan applications are we receiving, and how is that trending month over month?
  2. How much have we funded, and how much have we recovered from borrowers?
  3. What does our "Good Loan" vs "Bad Loan" split look like, and how healthy is our portfolio?
  4. Where are loans coming from geographically, and what drives borrowers to apply (purpose, employment length, home             ownership)?
  5. Can users drill into individual loan records for detailed analysis?

📊 Dashboards

  1️⃣ Summary Dashboard
  
  High-level KPIs for tracking overall lending performance:
  
  1. Total Loan Applications (with MTD and MoM change)
  2. Total Funded Amount (with MTD and MoM change)
  3. Total Amount Received (with MTD and MoM change)
  4. Average Interest Rate (with MTD and MoM change)
  5. Average Debt-to-Income Ratio (DTI) (with MTD and MoM change)
  6. Good Loan vs Bad Loan breakdown (application %, count, funded amount, received amount)
  7. Loan Status Grid View — metrics segmented by loan status
  
  2️⃣ Overview Dashboard
  
  Visual, trend-based analysis of the loan portfolio:
  
  1. Monthly Trends by Issue Date (Line Chart) — seasonality & long-term lending trends
  2. Regional Analysis by State (Filled Map) — geographic lending distribution
  3. Loan Term Analysis (Donut Chart) — distribution across loan term lengths
  4. Employee Length Analysis (Bar Chart) — impact of employment history on applications
  5. Loan Purpose Breakdown (Bar Chart) — primary reasons borrowers seek financing
  6. Home Ownership Analysis (Tree Map) — how home ownership status affects lending
  
  3️⃣ Details Dashboard
  
  A grid-based, drill-through view providing a consolidated, loan-by-loan snapshot of borrower profiles, loan terms, and repayment performance — a one-stop reference for detailed analysis.

🖼️ Dashboard Previews

Summary
<img width="1090" height="597" alt="loan_status_Summary" src="https://github.com/user-attachments/assets/ac2cfec0-97af-4350-8239-4a4ef31f58bb" />

Overview
<img width="1091" height="594" alt="loan_status_Overview" src="https://github.com/user-attachments/assets/e2937007-6958-4a6d-a40e-f32c294584c7" />

Details
<img width="1091" height="596" alt="loan_status_Details" src="https://github.com/user-attachments/assets/20895b6a-3c7f-4f1a-a51c-cf0c563e155b" />

🗂️ Dataset

File: financial_loan_bank.csv

Key fields include:

| Column | Description | 
| --------------- | --------------- |
| id, member_id	  | Unique loan and borrower identifiers  |
| loan_status   | Current status (Fully Paid, Charged Off, Current)  |
| loan_amount, funded_amount, total_payment  | Loan and repayment amounts  |
| int_rate  |	Interest rate on the loan  |
| dti  | Debt-to-Income ratio  |
| term  | Loan term (36/60 months)  |
| grade, sub_grade  |	Internal credit risk grading  |
| purpose  | Reason for the loan (car, credit card, home, etc.)  |
| emp_length, emp_title  | Borrower's employment details  |
| home_ownership  | Rent / Own / Mortgage |
| annual_income, verification_status  | Borrower income and verification  |
| address_state	 | Borrower's state, used for regional analysis  |
| issue_date, last_payment_date, next_payment_date  | Key loan lifecycle dates  |


🛠️ Tools & Skills Used

  SQL (MS SQL Server)
  
  1. Creating databases & tables
  2. Data cleaning and preprocessing
  3. Queries: SELECT, GROUP BY, ORDER BY, DISTINCT, COUNT, LIMIT
  4. Date functions: DATENAME, DATEPART, CAST
  5. Window functions: CTE, PARTITION BY
  
  Power BI
  
  1. Connecting to SQL Server as a data source
  2. Data modeling & Power Query transformations
  3. Date tables & Time Intelligence functions
  4. DAX: date functions, text functions, filter functions, CALCULATE, SUM/SUMX
  5. Building KPI cards, charts, and custom visual formatting
  6. Navigation buttons and page interactivity

   
📁 Repository Structure

├── Bank Loan.pbix &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                        # Power BI project file

├── financial_loan_bank.csv   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  # Source dataset

├── loan_status_Summary.jpg   &ensp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;  # Summary dashboard screenshot

├── loan_status_Overview.jpg  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Overview dashboard screenshot

├── loan_status_Details.jpg   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    # Details dashboard screenshot

└── README.md        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            # Project documentation

🚀 How to Use
  1. Clone this repository:
     git clone [https://github.com/your-username/bank-loan-analysis.git](https://github.com/chandrurc04-cyber/Bank-Loan-Dashboard)
  3. Open Bank Loan.pbix in Power BI Desktop (free download from Microsoft).
  4. If prompted, update the data source to point to financial_loan_bank.csv (or your own SQL Server instance).
  5. Explore the Summary, Overview, and Details pages using the in-report navigation.


📈 Key Insights
  1. Clear visibility into Good Loan vs Bad Loan performance to support risk assessment.
  2. Regional and purpose-based breakdowns highlight where lending activity is concentrated.
  3. Employment length and home ownership emerge as useful indicators when assessing borrower profiles.
  4. Monthly trend analysis helps identify seasonality in loan demand.

👤 Author
  
   Feel free to connect or reach out with any questions about this project.
