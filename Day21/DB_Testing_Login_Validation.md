# 🗄️ DAY 21 – Database Testing Concepts

## ✅ What is Database Testing?
Database Testing ensures:
- Data is stored correctly
- Data is accurate & consistent
- Business rules are followed
- No data loss or duplication

QA verifies UI ↔ API ↔ DB consistency.

## 🎯 Why DB Testing is Important for Login?

Login is security-critical:
- Wrong data = unauthorized access
- Duplicate users = data corruption
- Password issues = security risk

## 🧪 Sample Login Table

users

| user_id | username | email                                     | password | status   |
| ------- | -------- | ----------------------------------------- | -------- | -------- |
| 1       | munna    | [munna@gmail.com](mailto:munna@gmail.com) | enc_pwd  | ACTIVE   |
| 2       | rahul    | [rahul@gmail.com](mailto:rahul@gmail.com) | enc_pwd  | INACTIVE |


## 🔍 DB Testing Types

| Type             | Purpose                |
| ---------------- | ---------------------- |
| Data Validation  | Correct data stored    |
| Data Integrity   | FK, PK rules           |
| CRUD Testing     | Insert, Update, Delete |
| Security Testing | Password encryption    |
| Performance      | Query response time    |

🧠 Login Flow (Real Time)

1️⃣ User enters credentials

2️⃣ App validates input

3️⃣ DB query executes

4️⃣ DB returns user record

5️⃣ App allows or blocks login


## 🧪 Login Validation Queries

✅ 1. Check if user exists

SELECT * 

FROM users 

WHERE username = 'munna';


✅ 2. Validate active user

SELECT * 

FROM users 

WHERE username = 'munna' AND status = 'ACTIVE';


✅ 3. Validate correct password (Encrypted)

SELECT * 

FROM users 

WHERE username = 'munna' AND password = 'enc_pwd';


❌ 4. Invalid login attempt

SELECT * 

FROM users 

WHERE username = 'munna' AND password = 'wrong_pwd';

Expected: No record returned


🚫 5. Block inactive user

SELECT * 

FROM users 

WHERE username = 'rahul' AND status = 'ACTIVE';

Expected: No login allowed

🔐 Security Validations

✔ Password should NOT be plain text

✔ Password should be encrypted or hashed

✔ No duplicate usernames

SELECT COUNT(*) 

FROM users 

GROUP BY username

HAVING COUNT(*) > 1;

## 🧪 Negative DB Test Cases

| Scenario       | Expected       |
| -------------- | -------------- |
| Blank username | No record      |
| Wrong password | Login denied   |
| Inactive user  | Access blocked |
| SQL Injection  | Query blocked  |

SELECT * FROM users WHERE username = 'admin' OR '1'='1';

Expected: ❌ No access

## 🧪 Data Consistency Validation

UI Username == DB Username

UI Status == DB Status

SELECT username, status FROM users WHERE username='munna';


🎤 Interview Questions

Q1: Difference between DB testing & Backend testing?

DB testing checks data, backend checks logic

Q2: Can tester update DB directly?

Yes, in test environment only

Q3: How to validate encrypted password?

Compare hash values, not plain text
















