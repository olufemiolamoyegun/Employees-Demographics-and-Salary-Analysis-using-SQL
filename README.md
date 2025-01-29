Employee Demographics and Salary Analysis Using SQL
Overview

This project analyzes employee demographics and salary data using SQL and MySQL Bench, with visualizations created in Power BI. The primary focus is on understanding employee age distribution, salaries, and related demographics. The analysis provides insights into the structure of employee compensation and age trends across occupations.

Objective

The primary goal is to:

Explore and clean employee demographic and salary data.
Examine relationships between age, salary, and occupation.
Identify key trends to optimize recruitment and training strategies.
Data Preparation

The dataset includes employee demographics (age, gender, birth date) and salary details, which were cleaned and analyzed using SQL. Power BI was used to visualize key metrics, including the total salary and the count of employees.

Key SQL queries:

-- Joining Data Tables
```sql
-- Joining Data Tables
SELECT * 
FROM SQL.[dbo].[EmployeeDemographics]
LEFT OUTER JOIN SQL.[dbo].[EmployeeSalary] 
ON EmployeeDemographics.EmployeeID = EmployeeSalary.EmployeeID;

-- Categorizing Age Groups
SELECT FirstName, LastName, Age, 
       CASE WHEN Age > 30 THEN 'Old' ELSE 'Young' END AS AgeGroup
FROM SQL.[dbo].[EmployeeDemographics]
WHERE Age IS NOT NULL
ORDER BY Age;

-- Creating Tables for Analysis
CREATE TABLE employee_salary (
    employee_id INT NOT NULL,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    occupation VARCHAR(50),
    salary INT,
    dept_id INT
);





Populating Tables
Demographic and salary details were inserted into employee_demographics and employee_salary tables. 

A separate parks_departments table was created for department information.

Key Insights from Power BI

Employee Count and Salary Total:
Total number of employees: 12.
Total annual salary: $687,000.
Salary and Age Trends:
Highest Paid Occupation: Executive Director of Parks and Recreation.
Lowest Paid Occupation: City Clerk, with an average annual salary of $12,000.
Average Age of Highest-Paid Employees: 55 years.
Youngest Average Age Occupation: Office Manager (32 years).
Oldest Average Age Occupation: City Manager (62 years).

Conclusion

In 2016, the average annual salary across all employees was $687,000, with a significant gap between the highest- and lowest-paid roles.
The youngest employees tended to occupy lower-paid roles, while the highest salaries were associated with older employees in senior positions.
Recommendations

Recruitment Strategy:
Focus on hiring and training younger employees, particularly between 25–29 years, to maximize productivity and future growth.

Retention Strategy:
Consider reducing the age of employees in the highest-paid roles to balance experience with innovation.

Future Analysis:
Examine other metrics, such as gender pay gaps, department-level performance, and employee satisfaction, to refine HR policies further.

This analysis underscores the value of SQL and Power BI in providing actionable insights into employee demographics and salary structures.





