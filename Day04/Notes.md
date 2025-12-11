# ✅ DAY 4 – Boundary Value Analysis (BVA) (Expert Notes)

## 🔥 1. What is BVA?

Boundary Value Analysis is a black-box testing technique where test cases are designed using the boundary values of input ranges.

Because bugs occur mostly at boundaries, not in the middle — testers focus on minimum, maximum, just-below, just-above values.

## 🎯 2. Why BVA is Important? (Industry Level Explanation)

- 70% defects occur near boundaries
- Helps identify edge-case failures
- Reduces number of test cases
- Ensures stability of the input handling
- Critical for real-time systems, finance, forms, validations


## 🧠 3. How BVA Works
For any given range:

If valid range = a to b

Take values:

a - 1 (Just below).

a (Min).

a + 1 (Just above).

b - 1 (Just below max).

b (Max).

b + 1 (Just above).

You test just 6 values instead of testing 100s.



## 🧪 4. Types of BVA
✔ Normal BVA

Based on simple range boundaries

Example: 1–100

✔ Robust BVA

Includes invalid values (below min / above max)

✔ Worst Case BVA

Uses boundaries for multiple inputs

Example: Two fields: Range1 + Range2

Total test cases = 6 × 6 = 36.

✔ Special Value BVA

Systems with special critical values (0, -1, 100, 9999)




## 📌 5. When to Use BVA
- Forms with numeric limits
- Age, salary, OTP, PIN
- Pagination inputs
- File upload size validations
- Transaction limits
- Anywhere range exists



# ⭐ 10 BVA Examples

Below are 10 perfectly formatted examples you can directly copy to GitHub.

## Example 1: Age Input (18–60)

- Valid range = 18 to 60
- Test values:
- 17, 18, 19, 59, 60, 61


## Example 2: Password Length (6–12 chars)

- Range = 6 to 12
- Boundary values:
- 5, 6, 7, 11, 12, 13


## Example 3: Withdraw Limit (₹100–₹10,000)

- Boundary values:
- 99, 100, 101, 9999, 10000, 10001


## Example 4: Temperature Input (-10 to 50°C)

- Boundary values:
- -11, -10, -9, 49, 50, 51


## Example 5: Number of Login Attempts (1–3 attempts)

- Boundary values:
- 0, 1, 2, 3, 4


## Example 6: Product Quantity (1–99)

- Boundary values:
- 0, 1, 2, 98, 99, 100


## Example 7: Speed Limit (40–120 km/h)

- Boundary values:
- 39, 40, 41, 119, 120, 121


## Example 8: Marks Range (0–100)

- Boundary values:
- -1, 0, 1, 99, 100, 101


## Example 9: File Upload Size (1MB–50MB)

- Boundary values:
- 0.9, 1, 2, 49, 50, 51


## Example 10: Table Page Number (1–20)

- Boundary values:
- 0, 1, 2, 19, 20, 21

