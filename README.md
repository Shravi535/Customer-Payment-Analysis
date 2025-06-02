# Customer-Payment-Analysis
Project Title: Customer Payment Analysis
Goal: To analyze customer payment behavior and forecast overdue accounts to support AR decision-making.

🔧 Tools Used:
SQL – for querying and analyzing payment data

Excel – for data cleaning and trend analysis

Tableau – for dashboard visualization


📊** Step-by-Step Walkthrough:**
1. Data Collection (Mock Data)
I created a simulated dataset that included:

Customer_ID, Invoice_Date, Payment_Date, Invoice_Amount, Paid_Amount, Payment_Terms

This data reflected real-world AR scenarios from my experience.

2. Data Cleaning
Used Excel and SQL to:

Remove duplicates and null values

Calculate Payment Delay: DATEDIFF(Payment_Date, Invoice_Date)

Categorize overdue accounts into buckets (0–30 days, 31–60, etc.)

3. Analysis
Wrote SQL queries to:

Calculate DSO (Days Sales Outstanding) for each customer

Find customers with frequent late payments

Identify patterns in overdue payments based on customer type or region

SQL Query
SELECT customer_id,
       AVG(DATEDIFF(day, invoice_date, payment_date)) AS avg_payment_delay,
       COUNT(*) AS total_invoices
FROM payments
GROUP BY customer_id;
4. Visualization
Built a Tableau dashboard with:

AR aging buckets

Bar chart showing top 10 customers with highest payment delays

Line chart showing monthly DSO trends

5. Key Insights
Identified a set of customers with consistently overdue payments

Suggested a targeted follow-up process for high-risk accounts

Showed that customers with “Net 60” terms were more likely to delay

✅ Outcome
Though this was a simulated project, it reflects real AR insights that would help any collections team prioritize outreach and reduce overdue balances.

Helped me practice using SQL and Tableau in a business context, aligning with my AR background.

