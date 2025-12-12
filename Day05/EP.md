# 📝 DAY 5 – Equivalence Partitioning (EP)
## ✅ 1. What is Equivalence Partitioning (EP)?

Equivalence Partitioning (EP) is a Black-Box Test Design Technique where input values are divided into groups (partitions), and one value from each group is enough for testing.

Because all values in a group behave the same, one test case covers the entire partition.

## 👍 2. Why Use EP?

- Reduces total test cases
- Ensures full coverage
- Useful in forms, validation ranges, text fields
- Identifies invalid inputs quickly
- Very effective with BVA

## 📌 3. How EP Works

For any input range:

Valid Partition  
Invalid Partition 1 (below range)  
Invalid Partition 2 (above range)

# Example: Age (18–60)

Invalid: age < 18

Valid: 18 → 60

Invalid: age > 60

# Pick one value from each:

10 (invalid)

30 (valid)

80 (invalid)

Only 3 cases cover everything.

## 📦 4. Types of EP
✔ Valid Partition

Normal working values.

✔ Invalid Partitions

Values outside the valid range.

✔ Multiple Partitions

When multiple conditions exist
(Example: Length + Type + Range)

## ⭐ 10 Equivalence Partitioning Examples (Expert Level)

## Example 1: Age Input (18–60)

Partition 1: < 18 → 10

Partition 2: 18–60 → 30

Partition 3: > 60 → 75

## Example 2: Password Length (6–12 chars)

< 6 → "abc"

6–12 → "welcome"

12 → "abcdefghijkl"

## Example 3: Marks (0–100)

< 0 → -5

0–100 → 75

100 → 120

## Example 4: File Upload Size (1MB–50MB)

< 1MB → 0.5MB

1MB–50MB → 25MB

50MB → 60MB

## Example 5: Username Characters (only alphabets allowed)

Invalid: numbers → "munna123"

Invalid: symbols → "munna@@"

Valid: alphabets → "Munna"

## Example 6: Login Attempts (1–3 tries)

<1 → 0

1–3 → 2

3 → 5

## Example 7: Phone Number (10 digits only)

<10 digits → 12345

10 digits → 9876543210

10 digits → 123456789012

## Example 8: Email Format

Valid: "test@gmail.com
"

Invalid: missing @ → "testgmail.com"

Invalid: missing domain → "test@"


## Example 9: Product Quantity (1–99)

<1 → 0

1–99 → 50

99 → 120

## Example 10: Transaction Amount (₹100–₹10,000)

<100 → 50

100–10,000 → 5000

10,000 → 15000




# ❌ BVA ≠ EP
## ✅ How They Are Different
# ⭐ 1. What they test
EP (Equivalence Partitioning)

Tests groups of inputs
One value from each group is enough.

# Example: Age 18–60

Invalid (<18)

Valid (18–60)

Invalid (>60)

# BVA (Boundary Value Analysis)

Tests boundaries (edges) only
# Example:
17, 18, 19
59, 60, 61

# ⭐ 2. Number of Test Cases
# EP

3 test cases (one per partition)

# BVA

6 test cases (min, min+1, min-1, max, max-1, max+1)

# ⭐ 3. Focus Area
# EP

Focus:
✔ Validation of ranges
✔ Correct grouping
✔ Checking all partitions

# BVA

Focus:
✔ Edge values
✔ Where bugs occur most
✔ Min/Max boundaries

# ⭐ 4. When to Use
# EP

Use when range is big
Example: 1–1000 → only 3 cases

# BVA

Use when boundaries are critical
Example:

ATM withdrawal

Age limit

File size

# 🧠 Example Comparison: Age 18–60
✔ EP test values:

10 (invalid)

30 (valid)

70 (invalid)

✔ BVA test values:

17

18

19

59

60

61

👉 EP tests partitions.
👉 BVA tests boundaries.

## 🏁 Final Simple Difference
| Feature        | EP                  | BVA                    |
| -------------- | ------------------- | ---------------------- |
| What it tests  | Partitions (groups) | Boundaries (edges)     |
| Test cases     | 3                   | 6                      |
| Focus          | Range coverage      | Edge-case coverage     |
| Example values | 10, 30, 70          | 17, 18, 19, 59, 60, 61 |
| When used      | Large ranges        | Limit validations      |


## 💡 Easy Way to Remember

EP = Groups
BVA = Edges


