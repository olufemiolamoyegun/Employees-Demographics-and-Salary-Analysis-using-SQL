#Employees-Demographics-and-Salary-Analysis-using-SQL
The data was analyzed using SQL and MySQL Bench and visualized in Power BI.

It shows the various ages of employees and the salary earned.

The data was cleaned using SQL and MYSQL, followed by an exploration of employee salaries and demographics.

The power BI shows that the count of employees is 12, and the salary total is 687,000 annually.

SELECT * FROM SQL.[dbo].[EmployeeDemographics] Left Outer Join SQL [dbo].[EmployeeSalary] ON EmployeeDemographics.EmployeeID = EmployeeSalary.EmployeeID

SELECT FirstName, LastName, Age, CASE WHEN Age > 30 THEN 'Old' ELSE 'Young' END

CASE STATEMENT SELECT FirstName, LastName, Age, CASE WHEN AGE > 30 THEN 'Old' ELSE 'Young' END FROM SQL.dbo.EmployeeDemographics WHERE Age is NOT NULL ORDER BY Age CREATE TABLE employee_salary ( employee_id INT NOT NULL, first_name VARCHAR(50) NOT NULL, last_name VARCHAR(50) NOT NULL, occupation VARCHAR(50), salary INT, dept_id INT );

INSERT INTO employee_demographics (employee_id, first_name, last_name, age, gender, birth_date) VALUES (1,'Leslie', 'Knope', 44, 'Female','1979-09-25'), (3,'Tom', 'Haverford', 36, 'Male', '1987-03-04'), (4, 'April', 'Ludgate', 29, 'Female', '1994-03-27'), (5, 'Jerry', 'Gergich', 61, 'Male', '1962-08-28'), (6, 'Donna', 'Meagle', 46, 'Female', '1977-07-30'), (7, 'Ann', 'Perkins', 35, 'Female', '1988-12-01'), (8, 'Chris', 'Traeger', 43, 'Male', '1980-11-11'), (9, 'Ben', 'Wyatt', 38, 'Male', '1985-07-26'), (10, 'Andy', 'Dwyer', 34, 'Male', '1989-03-25'), (11, 'Mark', 'Brendanawicz', 40, 'Male', '1983-06-14'), (12, 'Craig', 'Middlebrooks', 37, 'Male', '198'

INSERT INTO employee_salary (employee_id, first_name, last_name, occupation, salary, dept_id) VALUES (1, 'Leslie', 'Knope', 'Deputy Director of Parks and Recreation', 75000,1), (2, 'Ron', 'Swanson', 'Director of Parks and Recreation', 70000,1), (3, 'Tom', 'Haverford', 'Entrepreneur', 50000,1), (4, 'April', 'Ludgate', 'Assistant to the Director of Parks and Recreation', 25000,1), (5, 'Jerry', 'Gergich', 'Office Manager', 50000,1), (6, 'Donna', 'Meagle', 'Office Manager', 60000,1), (7, 'Ann', 'Perkins', 'Nurse', 55000,4), (8, 'Chris', 'Traeger', 'City Manager', 90000,3), (9, 'Ben', 'Wyatt', 'State Auditor', 70000,6), (10, 'Andy', 'Dwyer', 'Shoe Shiner and Musician', 20000, NULL), (11, 'Mark', 'Brendanawicz', 'City Planner', 57000, 3), (12, 'Craig', 'Middlebrooks', 'Parks Director', 65000,1);

CREATE TABLE parks_departments ( department_id INT NOT NULL AUTO_INCREMENT, department_name varchar(50) NOT NULL, PRIMARY KEY (department_id) );

INSERT INTO parks_departments (department_name) VALUES ('Parks and Recreation'), ('Animal Control'), ('Public Works'), ('Healthcare'), ('Library'), ('Finance'); 



CONCLUSION 

In 2016, the average age of the highest-paid occupation was 55 years old, and the average salary was $687,000. The occupation with the highest salary was Executive Director of Parks and Recreation, followed by Director of Police and Fire Services and City Manager. The occupation with the lowest salary was city clerk, with an average of $12,000. The occupation with the youngest average age was office manager, with 32 years old, and the occupation with the oldest average age was city manager, with 62 years old.

Solution

Young employees should be recruited and trained between the ages of 25 and 29 for maximum output. This is also the highest-paid occupation, so the age of 55 should be lower.
