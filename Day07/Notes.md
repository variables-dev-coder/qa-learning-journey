# 📝 DAY 7 – Use Case Testing & State Transition Testing

## ✅ 1️⃣ Use Case Testing
🔹 What is a Use Case?

A use case describes how a user interacts with the system to achieve a goal.

Example:

User logs into the application.

🔹 What is Use Case Testing?

Use Case Testing is a black-box testing technique where test cases are derived from use cases (user flows).

➡ Focus is on end-to-end user behavior, not individual functions.

🔹 Why Use Use Case Testing?

- Tests real user scenarios
- Covers positive & negative flows
- Good for business-critical features
- Finds integration issues

🔹 Use Case Components

1. Actor (User)
2. Preconditions
3. Main Flow (Happy Path)
4. Alternate Flow
5. Exception Flow
6. Postconditions

🔹 Example: Login Use Case

Actor: User
Precondition: User is registered

Main Flow:
1. User enters username
2. User enters password
3. User clicks Login
4. System validates
5. User is logged in

Alternate Flow:
- Wrong password
- Invalid username

Exception Flow:
- System error
- Network failure

🔹 Sample Use Case Test Scenarios

- Login with valid credentials
- Login with invalid password
- Login with invalid username
- Login with empty fields
- Login when server is down

## ✅ 2️⃣ State Transition Testing
🔹 What is a State?

A state represents the current condition of the system.

Example states in login:
- Logged Out
- Logged In
- Locked
- Error

🔹 What is State Transition Testing?

State Transition Testing verifies that:
- System moves to the correct next state
- Based on events/actions

Used when behavior depends on previous state.

🔹 Why Use State Transition Testing?

- Best for workflow-based systems
- Detects invalid transitions
- Ensures system stability
- Common in login, payment, order, ATM systems

## 🔁 Login Flow – State Diagram (Concept)
States
1. Logged Out
2. Logged In
3. Login Failed
4. Account Locked

Events
- Enter valid credentials
- Enter invalid credentials
- Multiple failed attempts

## 🧠 Login State Transition Table

| Current State  | Event              | Next State     |
| -------------- | ------------------ | -------------- |
| Logged Out     | Valid login        | Logged In      |
| Logged Out     | Invalid login      | Login Failed   |
| Login Failed   | Retry valid        | Logged In      |
| Login Failed   | Retry invalid      | Login Failed   |
| Login Failed   | 3 invalid attempts | Account Locked |
| Account Locked | Admin unlock       | Logged Out     |

## 🎯 Task: Test Login Flow (State Transition)
✔ Test Scenarios

1. User logs in with valid credentials → Logged In
2. User enters wrong password → Login Failed
3. User retries with valid credentials → Logged In
4. User enters wrong password 3 times → Account Locked
5. Locked user tries login → Login blocked
6. Admin unlocks account → Logged Out
7. User logs in again successfully

## 🔄 Use Case vs State Transition

| Use Case Testing        | State Transition Testing |
| ----------------------- | ------------------------ |
| Focus on user flow      | Focus on system states   |
| End-to-end scenarios    | State-based behavior     |
| Good for business logic | Good for workflows       |
| Example: Login flow     | Example: Login attempts  |


🧩 When to Use Which?

- ✔ Use Case → User journey testing
- ✔ State Transition → State-dependent systems













