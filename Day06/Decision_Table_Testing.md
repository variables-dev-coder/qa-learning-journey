# 📝 DAY 6 – Decision Table Testing
## ✅ 1. What is Decision Table Testing?

Decision Table Testing is a black-box test design technique used when multiple conditions and business rules determine different outcomes.

It represents conditions and actions in a tabular format, making complex logic easy to test.

## ✅ 2. Why Decision Table Testing?

- Best for business rules
- Handles multiple conditions
- Avoids missing combinations
- Improves test coverage
- Common in banking, insurance, e-commerce

## ✅ 3. Components of a Decision Table

A decision table has 4 parts:
1. Conditions – Input factors (Yes/No, True/False)
2. Condition combinations – All possible combinations
3. Actions – Expected outputs
4. Rules – Mapping of conditions → actions

## ⭐ 4. Decision Table Structure
| Conditions / Rules | R1 | R2 | R3 | R4 |
| ------------------ | -- | -- | -- | -- |
| Condition 1        | Y  | Y  | N  | N  |
| Condition 2        | Y  | N  | Y  | N  |
| **Action**         | A1 | A2 | A3 | A4 |

## 🎯 5 Real-Life Decision Table Examples
## Example 1: Login System
Conditions
- Username valid?
- Password valid?
  
| Conditions     | R1            | R2             | R3             | R4           |
| -------------- | ------------- | -------------- | -------------- | ------------ |
| Username valid | Y             | Y              | N              | N            |
| Password valid | Y             | N              | Y              | N            |
| **Action**     | Login success | Password error | Username error | Login failed |


## Example 2: ATM Cash Withdrawal
Conditions
- Card valid?
- Sufficient balance?
  
| Conditions         | R1            | R2                   | R3           | R4                 |
| ------------------ | ------------- | -------------------- | ------------ | ------------------ |
| Card valid         | Y             | Y                    | N            | N                  |
| Balance sufficient | Y             | N                    | Y            | N                  |
| **Action**         | Dispense cash | Insufficient balance | Invalid card | Transaction failed |


## Example 3: Online Shopping Discount
Conditions
- Member?
- Purchase ≥ ₹5000?

| Conditions    | R1           | R2           | R3          | R4          |
| ------------- | ------------ | ------------ | ----------- | ----------- |
| Member        | Y            | Y            | N           | N           |
| Amount ≥ 5000 | Y            | N            | Y           | N           |
| **Action**    | 20% discount | 10% discount | 5% discount | No discount |


## Example 4: Exam Result System
Conditions
- Marks ≥ 35?
- Attendance ≥ 75%?

| Conditions       | R1   | R2                | R3           | R4   |
| ---------------- | ---- | ----------------- | ------------ | ---- |
| Marks ≥ 35       | Y    | Y                 | N            | N    |
| Attendance ≥ 75% | Y    | N                 | Y            | N    |
| **Action**       | Pass | Fail (attendance) | Fail (marks) | Fail |

## Example 5: Food Delivery Order
Conditions
- Restaurant open?
- Payment successful?

| Conditions         | R1           | R2             | R3                | R4           |
| ------------------ | ------------ | -------------- | ----------------- | ------------ |
| Restaurant open    | Y            | Y              | N                 | N            |
| Payment successful | Y            | N              | Y                 | N            |
| **Action**         | Order placed | Payment failed | Restaurant closed | Order failed |

## 🧠 When to Use Decision Table Testing
✔ Business rule validation

✔ Multiple condition scenarios

✔ Banking & finance apps

✔ Insurance workflows

✔ Approval systems







