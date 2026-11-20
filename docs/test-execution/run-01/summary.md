# Run 01 – Summary

**Date:** 20.10.–18.11.2026
**Tester:** m1raost
**Browser:** Chrome 156.0.8078.48 – 157.0.8103.79
**OS:** macOS 14.8.9
**Application:** https://www.saucedemo.com

## Scope
All five areas from the test plan were executed manually: Login, Inventory, Cart, Checkout and Menu.
Each test case was run with every user in its test data.

## Results by area

### Executions
An execution is one test case run with one user.

| Area | Test cases | Executions | Pass | Fail | Blocked |
|---|---|---|---|---|---|
| [Login](login.md) | 20 | 67 | 59 | 8 | 0 |
| [Inventory](inventory.md) | 20 | 96 | 60 | 27 | 9 |
| [Cart](cart.md) | 7 | 35 | 20 | 9 | 6 |
| [Checkout](checkout.md) | 20 | 92 | 46 | 28 | 18 |
| [Menu](menu.md) | 11 | 55 | 33 | 14 | 8 |
| **Total** | **78** | **345** | **218 (63%)** | **86 (25%)** | **41 (12%)** |

### Test cases
A test case counts as Fail if it failed for at least one user, and as Blocked if it was blocked for at least one user and failed for none.

| Area | Pass | Fail | Blocked |
|---|---|---|---|
| Login | 17 | 3 | 0 |
| Inventory | 1 | 17 | 2 |
| Cart | 0 | 5 | 2 |
| Checkout | 4 | 9 | 7 |
| Menu | 4 | 4 | 3 |
| **Total** | **26** | **38** | **14** |

## Bugs found

| Severity | Count | Issues |
|---|---|---|
| Critical | 2 | #4, #21 |
| High | 8 | #3, #8, #9, #11, #18, #19, #23, #27 |
| Medium | 5 | #7, #14, #17, #20, #26 |
| Low | 12 | #1, #2, #5, #6, #10, #12, #13, #15, #16, #22, #24, #25 |
| **Total** | **27** | |

[All bug reports on GitHub](https://github.com/m1raost/qa-saucedemo-project/issues)

## Bugs by user

| User | Bugs | User-specific bugs |
|---|---|---|
| standard_user | 9 | – |
| problem_user | 14 | #3, #4, #7, #8, #11, #12, #25 |
| performance_glitch_user | 10 | #14 |
| error_user | 13 | #3, #10, #13, #18, #19, #21 |
| visual_user | 15 | #5, #6, #7, #9, #15, #16 |

9 bugs affect every user, including the reference user standard_user: #1, #2, #17, #20, #22, #23, #24, #26, #27.

## Key findings
- **Two users cannot complete an order:** problem_user cannot fill in the checkout form (#4), and for error_user the "Finish" button does not respond (#21).
- **Form validation can be bypassed:** pressing Return submits the checkout form with empty fields for all users (#23), and error_user can submit the form without a Last Name (#19).
- **Wrong product data:** problem_user opens the wrong product pages (#8), and visual_user sees random prices on the inventory page (#9).
- **Order logic:** checkout is possible with an empty cart (#17), and an order can be completed after "Reset App State" (#27).
- **Many test cases were blocked** (41 executions), mainly by #3, #4 and #21. They should be retested once these bugs are fixed.

## Test case updates
- Login: exact error message added to TC-LOGIN-03, 04, 11 and 12; unnecessary steps and test data removed from TC-LOGIN-13 to 18.
- Inventory: steps 3 and 5 of TC-INV-11 clarified.
- Checkout: TC-CHK-20 added for the Return key bug found during TC-CHK-09.

## Exit criteria
- [x] All high-priority test cases have been executed.
- [x] At least 90% of all test cases have been executed (78 of 78; 41 single-user executions were blocked).
- [x] Every failed test case has a bug report.
- [x] All in-scope areas have been tested.
- [x] Test results are documented.

## Conclusion
standard_user can use the shop, but 9 bugs affect every user, including form validation and order logic. The other test users show critical defects, and two of them cannot complete an order at all. The critical and high-severity bugs (#4, #21, #3, #23, #27) should be fixed first, followed by a second test run to retest the 41 blocked executions.