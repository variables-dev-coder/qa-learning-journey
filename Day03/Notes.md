# ✅ DAY 3 – Software Testing Notes
## 1️⃣ Types of Testing

Testing can be categorized based on purpose, approach, or level.
Below are the main types:

## A. Based on Approach

1. Manual Testing
  - Tester executes test cases manually without automation tools.

2. Automation Testing
  - Tester uses tools/scripts to automate tests (Selenium, Playwright, Cypress).

## B. Based on Knowledge

3. Black Box Testing
  - Tester tests without seeing internal code.
  - Focus: Input → Output
  - Examples: Functional Testing, System Testing.

4. White Box Testing
  - Tester checks internal logic, code, loops, conditions.
  - Done by: Developers or SDET.

5. Grey Box Testing
  - Partial knowledge of internal structure + functional testing.

## C. Based on Purpose

6. Functional Testing
  - Validates business requirements.
  - Examples: Login, Signup, Payments.

7. Non-Functional Testing
  - Validates system quality attributes.

## D. Important Sub-Types

8. Smoke Testing
  - Quick check to ensure main features work after build deployment.

9. Sanity Testing
  - Quick check after minor changes to verify specific functionality.

10. Regression Testing
  - Ensures that new changes do not break existing functionality.

11. Retesting
  - Testing the defect fixes.

12. Exploratory Testing
  - Testing without test cases — learning while testing.

13. Ad-hoc Testing
  - Unstructured testing based on tester experience.

14. Usability Testing
  - Checks user experience and UI friendliness.

15. Performance Testing
  - Checks speed, load, stability:

-Load testing
-Stress testing
-Spike testing

16. Security Testing
  - Ensures application is safe from attacks.

17. Compatibility Testing
  - Testing across browsers, OS, devices, versions.

18. Accessibility Testing
  - Ensures specially-abled people can use the application (WCAG guidelines).


# 2️⃣ Functional vs Non-Functional Testing

# Functional Testing

Tests the business logic, features, and correctness of the application.

✔ Examples:
- Login
- Signup
- Search
- Add to cart
- Payment
- Form validation

✔ Validates:
- Requirements
- User journeys
- System behavior

# Non-Functional Testing

Tests how well the system works.

✔ Examples:
- Performance (speed, load)
- Security
- Usability
- Scalability
- Reliability
- Maintainability

✔ Validates:
- Quality attributes
- User experience
- System stability under load

# Functional vs Non-Functional (Table)

| Functional Testing               | Non-Functional Testing                |
| -------------------------------- | ------------------------------------- |
| Tests “**what**” the system does | Tests “**how well**” system works     |
| Based on business requirements   | Based on quality attributes           |
| Example: Login functionality     | Example: Login speed under load       |
| Black box techniques             | Specialized tools (JMeter, Loader.io) |
| Manual or automation             | Mostly tool-based                     |
| Ensures correctness              | Ensures performance & reliability     |


