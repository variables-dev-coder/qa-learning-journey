# 🗄️ DAY 18 – SQL JOINs (INNER, LEFT, RIGHT)
## ✅ What is JOIN?

JOIN is used to combine rows from two or more tables based on a related column.

🧪 Sample Tables

users

| user_id | name  | city      |
| ------- | ----- | --------- |
| 1       | Ravi  | Hyderabad |
| 2       | Anil  | Bangalore |
| 3       | Sunil | Pune      |
| 4       | Neha  | Delhi     |

orders

| order_id | user_id | product    | amount |
| -------- | ------- | ---------- | ------ |
| 101      | 1       | Mobile     | 15000  |
| 102      | 1       | Laptop     | 50000  |
| 103      | 3       | Headphones | 2000   |


## 🔗 1️⃣ INNER JOIN

Returns only matching records from both tables.

Syntax

SELECT columns

FROM table1

INNER JOIN table2

ON table1.column = table2.column;

Example

SELECT users.name, orders.product, orders.amount

FROM users

INNER JOIN orders

ON users.user_id = orders.user_id;

📌 Output: Only users who placed orders.


## 🔗 2️⃣ LEFT JOIN

Returns all records from left table and matching records from right table.

Syntax

SELECT columns

FROM table1

LEFT JOIN table2

ON table1.column = table2.column;

Example

SELECT users.name, orders.product

FROM users

LEFT JOIN orders

ON users.user_id = orders.user_id;

📌 Output: All users + order info if available.


## 🔗 3️⃣ RIGHT JOIN

Returns all records from right table and matching records from left table.

Syntax

SELECT columns

FROM table1

RIGHT JOIN table2

ON table1.column = table2.column;

Example

SELECT users.name, orders.product

FROM users

RIGHT JOIN orders

ON users.user_id = orders.user_id;

📌 Output: All orders + user info if available.


## 🎯 JOIN PRACTICE QUERIES

🔹 INNER JOIN

1️⃣ Get user names and their products

SELECT u.name, o.product

FROM users u

INNER JOIN orders o

ON u.user_id = o.user_id;


2️⃣ Get orders with user city

SELECT o.order_id, u.city

FROM orders o

INNER JOIN users u

ON o.user_id = u.user_id;

🔹 LEFT JOIN

3️⃣ Get all users and their orders

SELECT u.name, o.product

FROM users u

LEFT JOIN orders o

ON u.user_id = o.user_id;


4️⃣ Get users who have not placed any order

SELECT u.name

FROM users u

LEFT JOIN orders o

ON u.user_id = o.user_id

WHERE o.order_id IS NULL;

🔹 RIGHT JOIN

5️⃣ Get all orders with user names

SELECT o.order_id, u.name

FROM users u

RIGHT JOIN orders o

ON u.user_id = o.user_id;


6️⃣ Get orders without user details (rare case)

SELECT o.order_id

FROM users u

RIGHT JOIN orders o

ON u.user_id = o.user_id

WHERE u.user_id IS NULL;

## 🎯 INTERVIEW QUESTIONS (VERY IMPORTANT)
Q1: Difference between INNER and LEFT JOIN?
- INNER → only matching rows
- LEFT → all left table rows

Q2: Which JOIN is mostly used in testing?

👉 INNER JOIN & LEFT JOIN

Q3: How to find unmatched records?

👉 Use LEFT JOIN + IS NULL










