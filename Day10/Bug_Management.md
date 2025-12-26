# 🐞 DAY 10 – Bug Life Cycle & Bug Management

## 🔄 1️⃣ Bug Life Cycle (Real-Time)

A Bug Life Cycle defines the stages a defect passes through from discovery to closure.

📌 Bug Life Cycle Flow

New

 ↓
 
Assigned

 ↓
 
Open

 ↓
 
Fixed

 ↓
 
Retest

 ↓
 
Verified

 ↓
 
Closed


## 🔁 Other Possible States
- Reopen (if bug still exists)
- Deferred (fix postponed)
- Rejected (not a bug)
- Duplicate (already reported)
- Cannot Reproduce

## 🎯 2️⃣ Bug Priority vs Severity (INTERVIEW FAVORITE)

| Aspect     | Severity         | Priority                   |
| ---------- | ---------------- | -------------------------- |
| Definition | Impact on system | Urgency to fix             |
| Decided by | Tester           | Product Owner / Manager    |
| Based on   | Technical impact | Business impact            |
| Example    | App crash        | Payment bug before release |
| Changeable | Rarely           | Frequently                 |

## 🔥 Real-Time Example
- Login button not working → High Severity + High Priority
- Logo alignment issue → Low Severity + Low Priority
- Crash on rarely used page → High Severity + Low Priority

## 🧪 3️⃣ Bug Report Template (REAL PROJECT FORMAT)

| Field              | Description              |
| ------------------ | ------------------------ |
| Bug ID             | Auto generated           |
| Title              | Clear summary            |
| Module             | Affected module          |
| Environment        | Browser, OS              |
| Steps to Reproduce | Step-by-step             |
| Expected Result    | Correct behavior         |
| Actual Result      | Bug behavior             |
| Severity           | Critical/High/Medium/Low |
| Priority           | P1/P2/P3                 |
| Status             | New/Open/Fixed           |
| Attachment         | Screenshot / Video       |


## 🐞 4️⃣ Write 10 Real-Time Bug Reports

BUG-01

Title: Login fails with valid credentials

Module: Login

Severity: Critical

Priority: P1

Steps:

1. Enter valid username & password

2. Click Login

Expected: User should login successfully

Actual: Error message displayed


BUG-02

Title: Forgot Password link not working

Module: Login

Severity: High

Priority: P2

BUG-03

Title: Cart item count not updating

Module: Cart

Severity: Medium

Priority: P2


BUG-04

Title: Checkout page crashes on refresh

Module: Checkout

Severity: Critical

Priority: P1


BUG-05

Title: Payment success page not displayed

Module: Payment

Severity: Critical

Priority: P1

BUG-06

Title: Order confirmation email not received

Module: Order

Severity: High

Priority: P2


BUG-07

Title: Search returns no result for valid keyword

Module: Search

Severity: High

Priority: P2



BUG-08

Title: Logout button misaligned

Module: Header

Severity: Low

Priority: P3

BUG-09

Title: Error message overlaps input field

Module: Login

Severity: Low

Priority: P3


BUG-10

Title: Session not expired after logout

Module: Security

Severity: Critical

Priority: P1



##🎯 INTERVIEW QUESTIONS
❓ What is a bug life cycle?

→ Process a defect follows from detection to closure.

❓ Who decides severity and priority?

→ Severity: Tester
→ Priority: Product Owner / Manager

❓ Difference between bug, defect, and error?

Error → Human mistake

Defect → Deviation in code

Bug → Defect found in testing
















