# 🗄️ DAY 16 – SQL Basics (SELECT & WHERE)

## ✅ 1️⃣ What is SQL?

SQL (Structured Query Language) is used to store, retrieve, update, and delete data from databases.
In testing, SQL is mainly used to validate backend data.

## ✅ 2️⃣ SELECT Statement

Used to fetch data from a table.

Syntax:

SELECT column_name FROM table_name;

Example:

SELECT * FROM users;

## ✅ 3️⃣ WHERE Clause

Used to filter records based on conditions.

Syntax:

SELECT column_name FROM table_name WHERE condition;


## 🧪 Sample Table: users

| id | name  | email                             | age | city      | status   |
| -- | ----- | --------------------------------- | --- | --------- | -------- |
| 1  | Ravi  | [r@gmail.com](mailto:r@gmail.com) | 25  | Hyderabad | Active   |
| 2  | Anil  | [a@gmail.com](mailto:a@gmail.com) | 30  | Bangalore | Inactive |
| 3  | Sunil | [s@gmail.com](mailto:s@gmail.com) | 22  | Pune      | Active   |
| 4  | Neha  | [n@gmail.com](mailto:n@gmail.com) | 28  | Delhi     | Active   |


🔹 Basic SELECT

1️⃣ Get all records from users

SELECT * FROM users;


2️⃣ Get only names from users

SELECT name FROM users;


3️⃣ Get name and email

SELECT name, email FROM users;

🔹 WHERE with Conditions

4️⃣ Get users with age = 25

SELECT * FROM users WHERE age = 25;


5️⃣ Get users from Hyderabad

SELECT * FROM users WHERE city = 'Hyderabad';


6️⃣ Get active users

SELECT * FROM users WHERE status = 'Active';


7️⃣ Get users older than 25

SELECT * FROM users WHERE age > 25;


8️⃣ Get users younger than 30

SELECT * FROM users WHERE age < 30;


🔹 WHERE with AND / OR

9️⃣ Active users from Pune

SELECT * FROM users WHERE status = 'Active' AND city = 'Pune';


🔟 Users from Hyderabad or Delhi

SELECT * FROM users WHERE city = 'Hyderabad' OR city = 'Delhi';

🔹 WHERE with IN / NOT IN

1️⃣1️⃣ Users from selected cities

SELECT * FROM users WHERE city IN ('Delhi','Pune');


1️⃣2️⃣ Users not from Bangalore

SELECT * FROM users WHERE city NOT IN ('Bangalore');



🔹 WHERE with BETWEEN

1️⃣3️⃣ Users aged between 22 and 28

SELECT * FROM users WHERE age BETWEEN 22 AND 28;

🔹 WHERE with LIKE

1️⃣4️⃣ Names starting with ‘R’

SELECT * FROM users WHERE name LIKE 'R%';


1️⃣5️⃣ Emails containing ‘gmail’

SELECT * FROM users WHERE email LIKE '%gmail%';


🔹 WHERE with NOT

1️⃣6️⃣ Users who are not active

SELECT * FROM users WHERE status != 'Active';


🔹 Multiple Conditions

1️⃣7️⃣ Active users above age 24

SELECT * FROM users WHERE status = 'Active' AND age > 24;


1️⃣8️⃣ Inactive users from Bangalore

SELECT * FROM users WHERE status = 'Inactive' AND city = 'Bangalore';


🔹 Specific Columns with WHERE

1️⃣9️⃣ Names of users from Delhi

SELECT name FROM users WHERE city = 'Delhi';


2️⃣0️⃣ Emails of active users

SELECT email FROM users WHERE status = 'Active';


## 🎯 INTERVIEW POWER POINTS
- WHERE filters rows
- AND → all conditions true
- OR → any condition true
- LIKE → pattern matching
- IN → multiple values check




