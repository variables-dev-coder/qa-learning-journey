# 🗄️ DAY 19 – SQL Subqueries

## ✅ What is a Subquery?

A subquery is a query written inside another query.
It is used to fetch data based on results of another query.

🧪 Sample Tables Used

users

| user_id | name  | city      | age |
| ------- | ----- | --------- | --- |
| 1       | Ravi  | Hyderabad | 25  |
| 2       | Anil  | Bangalore | 30  |
| 3       | Sunil | Pune      | 22  |
| 4       | Neha  | Delhi     | 28  |

orders

| order_id | user_id | amount |
| -------- | ------- | ------ |
| 101      | 1       | 15000  |
| 102      | 1       | 50000  |
| 103      | 3       | 2000   |

# 🎯 10 Subquery Problems (With Solutions)

1️⃣ Get users who placed at least one order

SELECT * 

FROM users

WHERE user_id IN (

    SELECT user_id FROM orders
    
);


3️⃣ Get users who placed orders worth more than 10,000

SELECT * 

FROM users

WHERE user_id IN (

    SELECT user_id FROM orders WHERE amount > 10000
    
);


4️⃣ Get users whose order amount is maximum

SELECT * 

FROM users

WHERE user_id IN (

    SELECT user_id FROM orders 
    
    WHERE amount = (SELECT MAX(amount) FROM orders)
    
);

5️⃣ Get user name who placed highest order

SELECT name 

FROM users

WHERE user_id = (

    SELECT user_id FROM orders 
    
    ORDER BY amount DESC LIMIT 1
    
);


6️⃣ Get users older than average age

SELECT * 

FROM users

WHERE age > (

    SELECT AVG(age) FROM users
    
);

7️⃣ Get users who ordered more than once

SELECT * 

FROM users

WHERE user_id IN (

    SELECT user_id FROM orders
    
    GROUP BY user_id
    
    HAVING COUNT(*) > 1
    
);


8️⃣ Get users from same city as Ravi

SELECT * 

FROM users

WHERE city = (

    SELECT city FROM users WHERE name = 'Ravi'
    
);

9️⃣ Get users who have orders but amount less than average order amount

SELECT * 

FROM users

WHERE user_id IN (

    SELECT user_id FROM orders
    
    WHERE amount < (SELECT AVG(amount) FROM orders)
    
);


🔟 Get users who never ordered expensive products (>20000)

SELECT * 

FROM users

WHERE user_id NOT IN (

    SELECT user_id FROM orders WHERE amount > 20000
    
);



## 🎯 INTERVIEW POWER POINTS
- Subquery executes inside-out
- Can be used with IN, NOT IN, =, >, <
- Used when JOIN is complex
- Slower than JOIN for large data (important interview point)






