# 🛒 E-commerce Website Testing (Manual QA Project)

Manual functional and regression testing project covering the core purchase flow of a typical e-commerce website: **Login → Product Search → Cart → Checkout**.

## 🎯 Objective
Simulate a real QA cycle — designing test cases, executing them manually, logging defects in Jira-style format, and verifying fixes across regression cycles.

## 🧩 Scope
| Module | Coverage |
|---|---|
| Login | Valid/invalid credentials, empty fields, session handling |
| Product Search | Keyword search, filters, sorting, no-results state |
| Cart | Add/remove items, quantity updates, price calculation |
| Checkout | Address entry, payment step, order confirmation |

## 📁 Repository Structure
ecommerce-website-testing/
├── README.md
├── test-cases/
│ ├── login_test_cases.csv
│ ├── search_test_cases.csv
│ ├── cart_test_cases.csv
│ └── checkout_test_cases.csv
├── defect-log/
│ └── defect_log.csv
└── test-summary-report.md

## ✅ Sample Test Case Format
| TC ID | Module | Test Scenario | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TC_LOGIN_01 | Login | Login with valid credentials | 1. Go to login page 2. Enter valid email/password 3. Click Login | User redirected to homepage, logged in | As expected | Pass |
| TC_LOGIN_02 | Login | Login with invalid password | 1. Enter valid email 2. Enter wrong password 3. Click Login | Error message shown, login blocked | As expected | Pass |
| TC_CART_05 | Cart | Update quantity to 0 | 1. Add item to cart 2. Set quantity to 0 | Item removed from cart automatically | Item remained in cart with qty 0 | **Fail** |

Full test cases are in [`test-cases/`](./test-cases).

## 🐞 Defect Tracking
Defects were logged in a Jira-style format with severity, priority, steps to reproduce, and status. See [`defect-log/defect_log.csv`](./defect-log/defect_log.csv).

Example:
| Defect ID | Summary | Severity | Priority | Status |
|---|---|---|---|---|
| DEF-01 | Cart allows quantity = 0 without removing item | Medium | High | Fixed & Verified |
| DEF-02 | Search returns no results for valid product name with trailing space | Low | Medium | Open |

## 📊 Test Summary
See [`test-summary-report.md`](./test-summary-report.md) for pass/fail metrics and regression notes.

## 🛠️ Skills Demonstrated
- Manual test case design (positive & negative scenarios)
- Functional and regression testing
- Defect lifecycle management (Jira-style)
- Test documentation and reporting

---
**Author:** Priyanka Sahoo | SDET
