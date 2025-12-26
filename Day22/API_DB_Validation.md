# 🧪 DAY 22 – Practical Database Testing
## 🎯 Validate API Response with Database

## ✅ What is API–DB Validation?

It means verifying that data returned by API is exactly the same as data stored in the Database.

UI → API → DB

Tester validates:
- API response correctness
- Data consistency
- Business rules
- No data mismatch

🔥 Why This is IMPORTANT?

✔ Used in real projects

✔ Mandatory for SDET / Automation roles

✔ Asked in interviews

## 🧠 Real-Time Example (Login API)

API:

POST /api/login

Request Body:

{
  "username": "munna",
  
  "password": "password123"
  
}

✅ Expected API Response

{

  "status": "SUCCESS",
  
  "userId": 101,
  
  "username": "munna",
  
  "email": "munna@gmail.com"
  
}

## 🗄️ Database Table

| user_id | username | email                                     | password | status |
| ------- | -------- | ----------------------------------------- | -------- | ------ |
| 101     | munna    | [munna@gmail.com](mailto:munna@gmail.com) | enc_pwd  | ACTIVE |


## 🧪 STEP-BY-STEP API ↔ DB VALIDATION

🔹 Step 1: Hit API in Postman

- Method: POST
- Endpoint: /api/login
- Body: JSON credentials

✔ API returns SUCCESS

🔹 Step 2: Capture API Response Values

From response:

- userId
- username
- email

🔹 Step 3: Validate DB Data

SELECT user_id, username, email, status

FROM users

WHERE username = 'munna';

🔹 Step 4: Compare API vs DB

| Field    | API                                       | DB                                        | Result |
| -------- | ----------------------------------------- | ----------------------------------------- | ------ |
| user_id  | 101                                       | 101                                       | ✅      |
| username | munna                                     | munna                                     | ✅      |
| email    | [munna@gmail.com](mailto:munna@gmail.com) | [munna@gmail.com](mailto:munna@gmail.com) | ✅      |
| status   | SUCCESS                                   | ACTIVE                                    | ✅      |


❌ Negative API–DB Test Cases

❌ Invalid Password

API Response:

{

  "status": "FAIL",
  
  "message": "Invalid credentials"
  
}

DB Query:

SELECT * FROM users WHERE username='munna';

✔ DB should not change

❌ Inactive User

SELECT status FROM users WHERE username='rahul';

If status = INACTIVE

✔ API should block login

✔ API should reject

✔ DB should remain safe

🔐 Security Validations

✔ Password not returned in API

✔ Password stored encrypted

✔ No sensitive data exposed

SELECT password FROM users WHERE username='munna';

Should return encrypted value

## 🧪 API–DB Insert Validation (Signup)

API:

POST /api/register

After success response:

SELECT * FROM users WHERE email='newuser@gmail.com';

✔ Record must exist in DB

## 🎤 Interview Questions (Must Know)

Q1. What is API–DB testing?

Validating API response with database records.

Q2. Tools used?

Postman + SQL + DB client

Q3. What do you validate most?

Data accuracy, security, consistency

Q4. Can tester access DB?

Yes, in test environment




