# 📝 DAY 8 – Test Scenario vs Test Case

## ✅ 1️⃣ What is a Test Scenario?

A Test Scenario is a high-level idea of what to test.

👉 It answers: “What functionality should be tested?”

🔹 Characteristics
- One-line statement
- Business/user focused
- Covers broad functionality
- Derived from requirements/use cases

🔹 Example

Verify login functionality.

## ✅ 2️⃣ What is a Test Case?

A Test Case is a detailed step-by-step instruction to test a scenario.

👉 It answers: “How to test?”

🔹 Characteristics

- Detailed steps
- Contains test data
- Expected result defined
- Easy to execute & repeat

🔹 Example

Enter valid username and password and click Login.

## ✅ 3️⃣ Test Scenario vs Test Case (Difference Table)

| Test Scenario         | Test Case              |
| --------------------- | ---------------------- |
| High-level            | Detailed               |
| What to test          | How to test            |
| One line              | Step by step           |
| Business oriented     | Execution oriented     |
| Covers multiple cases | Covers one condition   |
| Written first         | Written after scenario |

## 🧠 Simple Memory Trick

Scenario = WHAT

Test Case = HOW

## 🔐 Login Page – Test Cases
TC-01: Login with valid credentials
- Enter valid username
- Enter valid password

Click Login
Expected: User should login successfully.

TC-02: Login with invalid password

- Enter valid username
- Enter invalid password

Expected: Error message should be displayed.


TC-03: Login with invalid username

- Enter invalid username
- Enter valid password

Expected: Error message should be displayed.



TC-04: Login with both invalid credentials

Expected: Login should fail with error message.



TC-05: Login with empty username

Expected: Username required message.


TC-06: Login with empty password

Expected: Password required message.


TC-07: Login with empty username and password

Expected: Validation messages for both fields.


TC-08: Verify password masking

- Type password
Expected: Password should be masked (******).


TC-09: Login with leading and trailing spaces

- Enter " user@gmail.com "
Expected: Spaces should be trimmed or error shown.



TC-10: Login with uppercase username

Expected: Login should be case-insensitive (if applicable).


TC-11: Login with special characters in username

Expected: Proper validation message.



TC-12: Verify Login button without entering data

Expected: Validation errors shown.


TC-13: Verify Enter key submits login

Expected: Login triggered on pressing Enter.



TC-14: Account lock after multiple invalid attempts

Expected: Account should be locked after defined attempts.


TC-15: Login after account unlock

Expected: User should login successfully.


## 📌 Optional (Bonus for Interviews)

- Verify Remember Me checkbox
- Verify Forgot Password link
- Verify error message text



# ⭐ Bonus Test Cases – Login Page (Interview Ready)
##✅ 1️⃣ Verify “Remember Me” Checkbox

TC-16: Verify Remember Me functionality
- Enter valid username
- Enter valid password
- Select Remember Me checkbox
- Login successfully
- Close browser
- Reopen application

Expected Result:
- User should remain logged in OR username should be auto-filled (based on requirement).



TC-17: Verify login without selecting Remember Me
- Enter valid credentials
- Do NOT select Remember Me
- Login
- Close browser and reopen app

Expected Result:
- User should be logged out and login details should not be remembered.

## ✅ 2️⃣ Verify “Forgot Password” Link
TC-18: Verify Forgot Password link navigation
- Click Forgot Password link

Expected Result:
- User should be redirected to Reset Password page.



TC-19: Verify password reset with registered email
- Enter registered email
- Click Submit

Expected Result:
- Password reset link should be sent to registered email.



TC-20: Verify password reset with unregistered email
- Enter unregistered email
- Click Submit

Expected Result:
- Proper error message should be displayed.



## ✅ 3️⃣ Verify Error Message Text
TC-21: Verify error message for invalid login
- Enter invalid username/password

Expected Result:
- Correct, user-friendly error message should be displayed
- Example: “Invalid username or password”




TC-22: Verify error message consistency
- Trigger same error multiple times

Expected Result:
- Error message text should remain consistent.



TC-23: Verify error message UI
- Trigger error

Expected Result:
Error message should be:
- Clearly visible
- Proper color (red)
- Near the input field
- Not overlapping UI



TC-24: Verify error message disappears after correction
- Enter invalid credentials → see error
- Correct the input

Expected Result:
- Error message should disappear after valid input.



