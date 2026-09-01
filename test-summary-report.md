# Test Summary Report — E-commerce Website Testing

## Overview
Two test cycles were executed covering Login, Search, Cart, and Checkout modules.

## Metrics

| Module | Total TCs | Passed | Failed | Pass % |
|---|---|---|---|---|
| Login | 10 | 9 | 1 | 90% |
| Search | 10 | 9 | 1 | 90% |
| Cart | 10 | 9 | 1 | 90% |
| Checkout | 10 | 9 | 1 | 90% |
| **Total** | **40** | **36** | **4** | **90%** |

## Defect Summary

| Severity | Count |
|---|---|
| High | 1 |
| Medium | 3 |
| Low | 1 |

## Regression Notes (Cycle 2)
- DEF-01 and DEF-05 were re-tested and verified as fixed.
- DEF-02 and DEF-03 remain open, carried forward to next cycle.
- DEF-04 fix is in progress; retest pending deployment.

## Key Observations
- Boundary condition handling (quantity = 0) was the most common defect pattern.
- Input sanitization for search worked well overall; edge case with whitespace trimming needs a fix.
- Security-related test (SQL injection attempt on login) passed — no vulnerability found.
- Recommend adding automated regression tests for the 4 failed scenarios to prevent future regressions (see companion `login-module-automation` repo).
