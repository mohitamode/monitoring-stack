# Sales Insights - Data Analysis using Tableau and SQL

This project provides a comprehensive analysis of sales for an India-based hardware company. It utilizes SQL for data extraction and transformation (ETL) and Tableau for advanced data visualization to derive actionable business insights.

### About Project

- Performed sales insights analysis for a hardware company based in India.
- Developed ETL mappings using SQL to extract data from unstructured sources and transformed it into a staging area for data cleaning.
- Designed a star schema data model within Tableau to facilitate efficient analysis.
- Developed a Tableau dashboard to perform quantitative visualizations, drawing valuable insights based on parameters affecting company performance year-over-year to provide business solutions.

## Technologies Used

- Advanced Excel: Used for initial data exploration and supplementary visualization.
- MySQL / SQL Server: Utilized for data storage, querying, and ETL processes.
- Tableau / Power BI: Employed for creating interactive dashboards and data storytelling.
- Statistics: Applied statistical principles to ensure data accuracy and meaningful analysis.

## Core Competencies and Analysis Framework

The project follows a structured data analysis workflow, ensuring that all business requirements are met through technical implementation.

- Data Visualization with Tableau
- Databases and SQL for Data Science
- Statistics for Data Science
- Data Visualization with Advanced Excel

## Project - India based Hardware company Sales Insights

### Problem Statements

The Sales Director requires visibility into the performance of the company across various Indian states to inform discount strategies and regional focus.

- Q1. Revenue breakdown by cities.
- Q2. Revenue breakdown by years and months.
- Q3. Top 5 customers by revenue and sales quantity.
- Q4. Top 5 Products by revenue.
- Q5. Net Profit and Profit Margin by Market.

### Approach - Project Planning and Aims Grid

#### 1. Purpose: What? Why? What do we want to achieve?
To unlock sales insights that were previously hidden from the sales team to support decision-making and automate manual data gathering processes.

#### 2. Stakeholders: Who will be involved?
- Sales Director
- I.T. Team
- Customer Service Team
- Data and Analytics Team

#### 3. End Result: What do we want to achieve?
An automated dashboard providing quick and current sales insights to support data-driven decision making.

#### 4. Success Criteria: What will be our success criteria?
- Dashboards uncovering sales order insights with the latest available data.
- Sales team enabled to make better decisions, aiming for a 10% cost saving of total spend.
- Sales analysts saving 20% of their business time by eliminating manual data gathering.

### Setup Process

Step 1: Download the database files (db_dump.sql or db_dump.xlsx).

Step 2: Import the data into MySQL and perform ETL (Extract, Transform, Load) as required.

Step 3: Use Tableau Public or Tableau Desktop to perform the data analysis.

Step 4: Connect Tableau to the MySQL database or Excel data source.

Step 5: Save the analysis file in .twb or .twbx format.

## Data Analysis Using SQL

1. Show all customer records
    `SELECT * FROM customers;`

2. Show total number of customers
    `SELECT count(*) FROM customers;`

3. Show transactions for Chennai market (market code for Chennai is Mark001)
    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distinct product codes that were sold in Chennai.
    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars.
    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 joined by date table.
    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in year 2020.
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`

8. Show total revenue in year 2020, January Month.
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

9. Show total revenue in year 2020 in Chennai.
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";`

## Data Analysis Using Tableau

The analysis includes a Star Schema implementation to optimize data relationships and dashboard performance.

### Key Dashboards:
- Revenue Analysis: Detailed breakdown of income streams across regions and timeframes.
- Profit Analysis: Insights into net profit margins and market-specific profitability.

## Project References

1. Tableau Project Dashboard: Sales Insights - Data Analysis using Tableau
2. MySQL Installation and Configuration Guides
3. OLTP and OLAP Architectural Differences
4. Star Schema Design: Fact Tables and Dimension Tables

## Related Data Projects

- Spotify Data Analysis using Python
- Statistics for Data Science using Python
- Python Libraries for Data Science

---

## Maintainer

**Mohit Shyam Amode**
Data Analyst

Mohit is a Data Analyst with over 4 years of professional experience in dashboard development, SQL, and structured data analysis. He specializes in data visualization, query optimization, and translating operational requirements into actionable insights.

### Contact Information

- Email: mohitshyamamode@gmail.com
- LinkedIn: linkedin.com/in/mohitamode
- GitHub: github.com/mohitamode

For any queries regarding this project or potential collaborations, please feel free to reach out via LinkedIn or Email.