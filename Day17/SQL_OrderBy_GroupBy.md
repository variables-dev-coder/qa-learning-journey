## 🗄️ DAY 17 – SQL ORDER BY & GROUP BY

🧪 Sample Table Used: users

| id | name  | email                               | age | city      | status   |
| -- | ----- | ----------------------------------- | --- | --------- | -------- |
| 1  | Ravi  | [r@gmail.com](mailto:r@gmail.com)   | 25  | Hyderabad | Active   |
| 2  | Anil  | [a@gmail.com](mailto:a@gmail.com)   | 30  | Bangalore | Inactive |
| 3  | Sunil | [s@gmail.com](mailto:s@gmail.com)   | 22  | Pune      | Active   |
| 4  | Neha  | [n@gmail.com](mailto:n@gmail.com)   | 28  | Delhi     | Active   |
| 5  | Amit  | [a2@gmail.com](mailto:a2@gmail.com) | 30  | Pune      | Active   |


## ✅ 1️⃣ ORDER BY

Used to sort records.

Syntax

SELECT * FROM table_name ORDER BY column_name ASC|DESC;

ORDER BY Queries

1️⃣ Get users sorted by age (ascending)

SELECT * FROM users ORDER BY age;

2️⃣ Get users sorted by age (descending)

SELECT * FROM users ORDER BY age DESC;


3️⃣ Sort users by name

SELECT * FROM users ORDER BY name;


4️⃣ Sort users by city

SELECT * FROM users ORDER BY city;


5️⃣ Active users sorted by age

SELECT * FROM users WHERE status='Active' ORDER BY age;


6️⃣ Users sorted by city then age

SELECT * FROM users ORDER BY city, age;


7️⃣ Users sorted by age descending, name ascending

SELECT * FROM users ORDER BY age DESC, name ASC;


## ✅ 2️⃣ GROUP BY

Used to group rows and apply aggregate functions.

Aggregate Functions

- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()

GROUP BY Queries

8️⃣ Count users by city

SELECT city, COUNT(*) FROM users GROUP BY city;


9️⃣ Count users by status

SELECT status, COUNT(*) FROM users GROUP BY status;


🔟 Average age per city

SELECT city, AVG(age) FROM users GROUP BY city;


1️⃣1️⃣ Maximum age per city

SELECT city, MAX(age) FROM users GROUP BY city;


1️⃣2️⃣ Minimum age per city

SELECT city, MIN(age) FROM users GROUP BY city;


1️⃣3️⃣ Count users by city and status

SELECT city, status, COUNT(*) FROM users GROUP BY city, status;


1️⃣4️⃣ Count active users per city

SELECT city, COUNT(*) FROM users WHERE status='Active' GROUP BY city;


1️⃣5️⃣ Cities having more than one user

SELECT city, COUNT(*) 
FROM users 
GROUP BY city 
HAVING COUNT(*) > 1;


## 🎯 INTERVIEW POWER POINTS
- ORDER BY → sorts data
- GROUP BY → groups rows
- HAVING → filters groups
- WHERE → filters rows before grouping













