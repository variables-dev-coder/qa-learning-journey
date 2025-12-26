## 🗄️ DAY 20 – SQL Aggregate Functions
# ✅ What are SQL Functions?

SQL Aggregate Functions perform calculations on multiple rows and return one value.
Very important for data validation in testing.

🧪 Sample Table

employees

| emp_id | name  | department | salary |
| ------ | ----- | ---------- | ------ |
| 1      | Ravi  | IT         | 50000  |
| 2      | Anil  | HR         | 40000  |
| 3      | Sunil | IT         | 60000  |
| 4      | Neha  | Finance    | 55000  |
| 5      | Priya | IT         | 45000  |

## 🎯 Functions with Real Queries

1️⃣ COUNT()

Count total employees

SELECT COUNT(*) FROM employees;

Count employees in IT department

SELECT COUNT(*)

FROM employees

WHERE department = 'IT';

2️⃣ SUM()

Total salary of all employees

SELECT SUM(salary) FROM employees;

Total IT department salary

SELECT SUM(salary) 

FROM employees 

WHERE department = 'IT';

3️⃣ AVG()

Average salary of employees

SELECT AVG(salary) FROM employees;

Average IT salary

SELECT AVG(salary)

FROM employees 

WHERE department = 'IT';

4️⃣ MAX()

Highest salary

SELECT MAX(salary) FROM employees;

5️⃣ MIN()

Lowest salary

SELECT MIN(salary) FROM employees;

## 🎯 Functions with GROUP BY

Average salary per department

SELECT department, AVG(salary)

FROM employees

GROUP BY department;

Total salary per department

SELECT department, SUM(salary)

FROM employees

GROUP BY department;

Number of employees per department

SELECT department, COUNT(*)

FROM employees

GROUP BY department;

## 🔥 Functions with HAVING (INTERVIEW FAVORITE)

Departments with avg salary > 50000

SELECT department, AVG(salary)

FROM employees

GROUP BY department

HAVING AVG(salary) > 50000;

🧠 Real-Time Testing Use Cases

Validate report totals

Verify dashboard metrics

Cross-check API response vs DB

Salary / order / revenue validation

🎤 Interview Questions

Q: Difference between WHERE and HAVING

✔ WHERE filters rows

✔ HAVING filters grouped results

Q: Can we use aggregate functions in WHERE?

❌ No (except subquery)


