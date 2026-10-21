# Run 01 – Login

**Date:** 20.10.2026-21.10.2026
**Browser:** Chrome 156.0.8078.48
**OS:** macOS 14.8.9


### TC-LOGIN-01: Login with valid credentials
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-02: Locked-out user cannot log in
- **Results:**
  - locked_out_user: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-03: Username is case-sensitive
- **Results:**
  - Standard_user: Pass
  - Locked_out_user: Pass
  - Problem_user: Pass
  - Performance_glitch_user: Pass
  - Error_user: Pass
  - Visual_user: Pass
- **Bug:** –
- **Notes:** Expected result does not mention the error message text. Actual: "Epic sadface: Username and password do not match any user in this service" – test case to be updated.


### TC-LOGIN-04: Password is case-sensitive
- **Results:**
  - standard_user: Pass
  - locked_out_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** Expected result does not mention the error message text. Actual: "Epic sadface: Username and password do not match any user in this service" – test case to be updated.


### TC-LOGIN-05: Empty form is not accepted
- **Results:**
  - Empty form: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-06: Empty username with valid password
- **Results:**
  - Empty username, secret_sauce: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-07: Valid username with empty password
- **Results:**
  - standard_user: Pass
  - locked_out_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-08: Submit the form with Enter button
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-09: Closing error message with x
- **Results:**
  - standard_user: Pass
  - locked_out_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-10: Readability of error message
- **Results:**
  - standard_user: Fail
  - locked_out_user: Fail
  - problem_user: Fail
  - performance_glitch_user: Fail
  - error_user: Fail
  - visual_user: Fail
- **Bug:** #1
- **Notes:** –


### TC-LOGIN-11: Username with spaces
- **Results:**
  - standard_user: Pass
  - locked_out_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** Expected result does not mention the error message text. Actual: "Epic sadface: Username and password do not match any user in this service" – test case to be updated.


### TC-LOGIN-12: Password with spaces
- **Results:**
  - standard_user: Pass
  - locked_out_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** Expected result does not mention the error message text. Actual: "Epic sadface: Username and password do not match any user in this service" – test case to be updated.


### TC-LOGIN-13: Username field maximum length (Valid Less Than Max)
- **Results:**
  - 49 characters: Pass
- **Bug:** –
- **Notes:** Step "Click Login" and the password are not needed – applies to TC-LOGIN-13 to 15, test cases to be updated.


### TC-LOGIN-14: Username field maximum length (Maximum Valid)
- **Results:**
  - 50 characters: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-15: Username field maximum length (Over Max Limit)
- **Results:**
  - 51 characters: Fail
- **Bug:** #2
- **Notes:** –


### TC-LOGIN-16: Password field maximum length (Valid Less Than Max)
- **Results:**
  - 49 characters: Pass
- **Bug:** –
- **Notes:** Step "Click Login", the users and "Enter the username" are not needed – applies to TC-LOGIN-16 to 18, test cases to be updated.


### TC-LOGIN-17: Password field maximum length (Maximum Valid)
- **Results:**
  - 50 characters: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-18: Password field maximum length (Over Max Limit)
- **Results:**
  - 51 characters: Fail
- **Bug:** #2
- **Notes:** –


### TC-LOGIN-19: Entering direct URL without login
- **Results:**
  - URL without login: Pass
- **Bug:** –
- **Notes:** –


### TC-LOGIN-20: Entering inventory page with back button after logout
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –