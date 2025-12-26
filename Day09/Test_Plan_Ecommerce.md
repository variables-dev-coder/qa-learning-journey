# 📝 DAY 9 – Test Plan (E-commerce Website)

## 1️⃣ Test Plan ID

TP-ECOM-001

## 2️⃣ Introduction

This document describes the testing strategy, scope, resources, and schedule for testing the E-commerce web application to ensure quality, reliability, and user satisfaction.

## 3️⃣ Objectives
- Verify that all functionalities work as expected
- Identify defects before production release
- Ensure system stability and performance
- Validate business requirements

## 4️⃣ Scope of Testing
## ✅ In Scope
- User Registration & Login
- Product Search & Filters
- Product Details Page
- Add to Cart / Remove from Cart
- Wishlist
- Checkout Process
- Payment Gateway (mock)
- Order Confirmation
- Order History
- Logout


## ❌ Out of Scope
- Third-party payment gateway internal testing
- Production data validation
- Mobile app testing (if web only)

## 5️⃣ Test Approach
- Manual Testing
- Black Box Testing
- Functional Testing
- Regression Testing
- Smoke & Sanity Testing
- Exploratory Testing


## 6️⃣ Types of Testing
- Functional Testing
- UI Testing
- Usability Testing
- Compatibility Testing
- Security Testing (basic)
- Performance Testing (basic)

## 7️⃣ Test Environment
- OS: Windows / Linux
- Browser: Chrome, Firefox, Edge
- Test URL: Staging environment
- Database: Test DB
- Devices: Desktop / Laptop


## 8️⃣ Test Deliverables
- Test Plan Document
- Test Scenarios
- Test Cases
- Defect Reports
- Test Execution Report
- Test Closure Report


## 9️⃣ Entry Criteria
- Requirements are approved
- Test environment ready
- Build deployed successfully


## 🔟 Exit Criteria
- All critical test cases executed
- No open critical defects
- Test summary report prepared


## 1️⃣1️⃣ Test Schedule

| Activity         | Duration |
| ---------------- | -------- |
| Test Planning    | 1 Day    |
| Test Case Design | 2 Days   |
| Test Execution   | 3 Days   |
| Bug Fix & Retest | 2 Days   |
| Regression       | 1 Day    |



## 1️⃣2️⃣ Roles & Responsibilities

| Role          | Responsibility                     |
| ------------- | ---------------------------------- |
| QA Tester     | Test case execution, bug reporting |
| QA Lead       | Planning, review, reporting        |
| Developer     | Bug fixing                         |
| Product Owner | Requirement clarification          |


## 1️⃣3️⃣ Defect Management
- Tool: JIRA / Excel
- Severity levels:
    - Critical
    - High
    - Medium
    - Low

## 1️⃣4️⃣ Risks & Mitigation

| Risk                | Mitigation                   |
| ------------------- | ---------------------------- |
| Requirement changes | Regular communication        |
| Environment issues  | Backup environment           |
| Time constraints    | Prioritize critical features |

## 1️⃣5️⃣ Approval

Test Plan is approved by QA Lead and Project Manager.


# ✅ DAY 9 – Task 2 (Practice Task)
Test Scenarios – E-commerce Website


## Task 2 (Practice Task) 
Write 5 Test Scenarios for: 
- Product Search 
- Add to Cart 
- Checkout 
- Payment 
- Order Confirmation


## Task 3 (Advanced – Optional) 
- Add a Test Plan Diagram in Day09/Images/ 
- Add Assumptions & Dependencies section


## 🔍 1️⃣ Product Search – Test Scenarios
- TS-PS-01: Verify product search with valid product name
- TS-PS-02: Verify search with partial keyword
- TS-PS-03: Verify search with invalid product name
- TS-PS-04: Verify search results using category filter
- TS-PS-05: Verify behavior when no search results found

## 🛒 2️⃣ Add to Cart – Test Scenarios
- TS-AC-01: Verify adding product to cart from product list page
- TS-AC-02: Verify adding product to cart from product details page
- TS-AC-03: Verify updating product quantity in cart
- TS-AC-04: Verify removing product from cart
- TS-AC-05: Verify cart persistence after page refresh


## 📦 3️⃣ Checkout – Test Scenarios
- TS-CO-01: Verify checkout with all mandatory fields filled
- TS-CO-02: Verify checkout with missing mandatory fields
- TS-CO-03: Verify checkout using saved address
- TS-CO-04: Verify checkout as guest user
- TS-CO-05: Verify navigation between checkout steps


## 💳 4️⃣ Payment – Test Scenarios
- TS-PAY-01: Verify payment using valid card details
- TS-PAY-02: Verify payment using invalid card details
- TS-PAY-03: Verify payment failure handling
- TS-PAY-04: Verify payment using different payment methods (UPI/Card/NetBanking)
- TS-PAY-05: Verify retry payment option after failure


## ✅ 5️⃣ Order Confirmation – Test Scenarios
- TS-OC-01: Verify order confirmation page after successful payment
- TS-OC-02: Verify order ID generation
- TS-OC-03: Verify confirmation email/SMS sent to user
- TS-OC-04: Verify order details accuracy
- TS-OC-05: Verify order appears in order history


## 📊 Test Plan Diagram (Text Representation)


Requirements
     ↓
Test Planning
     ↓
Test Design
     ↓
Test Execution
     ↓
Defect Reporting
     ↓
Retesting & Regression
     ↓
Test Closure













