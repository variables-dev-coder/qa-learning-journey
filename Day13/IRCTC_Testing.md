# 🚆 DAY 13 – IRCTC Website Testing

## ✅ PART 1: Write 15 Test Cases (IRCTC Website)

🔐 Login / Registration

TC-01: Verify login with valid username and password

TC-02: Verify login with invalid password

TC-03: Verify login with invalid captcha

TC-04: Verify error message for empty login fields

TC-05: Verify logout functionality

🔍 Train Search

TC-06: Verify train search with valid source and destination

TC-07: Verify train search with same source and destination

TC-08: Verify train search with past travel date

TC-09: Verify train availability for selected class

TC-10: Verify train search without entering mandatory fields

🎫 Ticket Booking

TC-11: Verify seat selection during booking

TC-12: Verify passenger details validation

TC-13: Verify booking with invalid passenger age

TC-14: Verify payment initiation after booking

TC-15: Verify ticket confirmation after successful payment

## 🐞 PART 2: Write 5 Bug Reports (Sample – Real-Time)

BUG-01

Title: Login fails with valid credentials during peak hours

Module: Login

Severity: Critical

Priority: P1

Steps:

1. Enter valid username & password

2. Enter captcha

Click Login

Expected: User should login successfully

Actual: Login fails with error message

BUG-02

Title: Captcha refresh not working

Module: Login

Severity: High

Priority: P2

BUG-03

Title: Train availability not displayed for valid route

Module: Train Search

Severity: High

Priority: P1

BUG-04

Title: Passenger age validation allows negative values

Module: Passenger Details

Severity: Medium

Priority: P2

BUG-05

Title: Payment success but ticket not generated

Module: Payment

Severity: Critical

Priority: P1


