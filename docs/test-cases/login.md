# Test Cases – Login

### TC-LOGIN-01: Login with valid credentials
- **Requirement:** AR-LOGIN-01
- **Priority:** High
- **Type:** Positive
- **Preconditions:** The login page is open.
- **Test data:** Password secret_sauce with each user:
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login.
- **Expected result:** The user is logged in and the inventory page is shown.
- **Automated:** Planned


### TC-LOGIN-02: Locked-out user cannot log in
- **Requirement:** AR-LOGIN-02
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The login page is open.
- **Test data:** username: locked_out_user, password: secret_sauce
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login.
- **Expected result:** A locked-out user cannot log in and sees an error message:
  "Epic sadface: Sorry, this user has been locked out."
- **Automated:** Planned


### TC-LOGIN-03: Username is case-sensitive
- **Requirement:** AR-LOGIN-03
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The login page is open.
- **Test data:** Password secret_sauce with each user:
  - Standard_user
  - Locked_out_user
  - Problem_user
  - Performance_glitch_user
  - Error_user
  - Visual_user
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login.
- **Expected result:** Usernames with Upper-case letters are not accepted.
- **Automated:** Planned


### TC-LOGIN-04: Password is case-sensitive
- **Requirement:** AR-LOGIN-03
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The login page is open.
- **Test data:** Password Secret_sauce with each user:
  - standard_user
  - locked_out_user
  - problem_user
  - performance_glitch_user
  - error_user
  - visual_user
- **Steps:**
   1. Enter the username.
   2. Enter the password.
   3. Click Login.
- **Expected result:** Password with upper-case letters is not accepted.
- **Automated:** Planned


### TC-LOGIN-05: Empty form is not accepted
- **Requirement:** AR-LOGIN-04
- **Priority:** High 
- **Type:** Negative
- **Preconditions:** The login page is open.
- **Test data:** Empty username and password.
- **Steps:**
   1. Leave username empty.
   2. Leave password empty.
   3. Click Login.
- **Expected result:** An empty form is not accepted and an error message is shown: "Epic sadface: Username is required"
- **Automated:** Planned


### TC-LOGIN-06: Empty username with valid password
- **Requirement:** AR-LOGIN-05
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The login page is open.
- **Test data:** Empty username, password: secret_sauce
- **Steps:**
   1. Leave username empty.
   2. Enter the password.
   3. Click Login.
- **Expected result:** An empty username with a valid password is not accepted and an error message is shown:
 "Epic sadface: Username is required"
- **Automated:** Planned


### TC-LOGIN-07: Valid username with empty password
- **Requirement:** AR-LOGIN-06
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The login page is open.
- **Test data:** Empty password for each user:
 - standard_user
 - locked_out_user
 - problem_user
 - performance_glitch_user
 - error_user
 - visual_user
- **Steps:**
   1. Enter username.
   2. Leave password empty.
   3. Click Login.
- **Expected result:**  A valid username with an empty password is not accepted and an error message is shown:
 "Epic sadface: Password is required"
- **Automated:** Planned


### TC-LOGIN-08: Submit the form with Enter button
- **Requirement:** AR-LOGIN-07
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The Login page is open.
- **Test data:** Password secret_sauce for each user except locked_out_user:
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
   1. Enter the username.
   2. Enter the password.
   3. Press Enter.
- **Expected result:** Pressing Enter instead of clicking Login submits the form.
- **Automated:** No


### TC-LOGIN-09: Closing error message with x
- **Requirement:** AR-LOGIN-08
- **Priority:** Low
- **Type:** Positive
- **Preconditions:** The login page is open.
- **Test data:** Password is empty, for users:
   - standard_user
   - locked_out_user
   - problem_user
   - performance_glitch_user
   - error_user
   - visual_user
- **Steps:**
   1. Enter the username.
   2. Leave the password empty.
   3. Click Login.
   4. Click on "x" on the error message block.
- **Expected result:** Clicking X on the error message closes the message and removes the red icons.
- **Automated:** No


### TC-LOGIN-10: Readability of error message
- **Requirement:** AR-LOGIN-09
- **Priority:** Low
- **Type:** Negative
- **Preconditions:** The Login page is open.
- **Test data:** Password is wrong_password, for users:
    - standard_user
    - locked_out_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login.
- **Expected result:** The error message stays inside its container and is fully readable.
- **Automated:** No


### TC-LOGIN-11: Username with spaces
- **Requirement:** AR-LOGIN-10
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The Login page is open.
- **Test data:** Password secret_sauce for each user:
    - " standard_user"
    - "locked_out_user "
    - " problem_user"
    - "performance_glitch_user "
    - " error_user "
    - "visual_user "
- **Steps:**
   1. Enter the username.
   2. Enter the password.
   3. Click Login.  
- **Expected result:** A username with spaces before or after it is not accepted.
- **Automated:** Planned


### TC-LOGIN-12: Password with spaces
- **Requirement:** AR-LOGIN-13
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The Login page is open.
- **Test data:** Password " secret_sauce", "secret_sauce " for each user:
    - standard_user
    - locked_out_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login.
- **Expected result:** A password with spaces before or after it is not accepted.
- **Automated:** Planned


### TC-LOGIN-13: Username field maximum length (Valid Less Than Max)
- **Requirement:** AR-LOGIN-11
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The Login page is open.
- **Test data:** Username is: UserAccountIdentificationNumberZeroZeroZeroZeroOk (49 characters)
  Password is: secret_sauce
- **Steps:**
   1. Enter the username.
   2. Enter the password.
   3. Click Login.
- **Expected result:** All characters are entered in the field.
- **Automated:** Planned



### TC-LOGIN-14: Username field maximum length (Maximum Valid)
- **Requirement:** AR-LOGIN-11
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The Login page is open.
- **Test data:** Username is: UserAccountIdentificationNumberZeroZeroZeroZeroOut (50 characters)
  Password is: secret_sauce
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login.
- **Expected result:** All 50 characters are entered in the field.
- **Automated:** Planned


### TC-LOGIN-15: Username field maximum length (Over Max Limit)
- **Requirement:** AR-LOGIN-11
- **Priority:** Medium
- **Type:** Negative
- **Preconditions:** The Login page is open.
- **Test data:** Username is: UserAccountIdentificationNumberZeroZeroZeroZeroOver (51 characters)
  Password is: secret_sauce
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login.
- **Expected result:** Only the first 50 characters are entered, the 51st character is not accepted.
- **Automated:** Planned



### TC-LOGIN-16: Password field maximum length (Valid Less Than Max)
- **Requirement:** AR-LOGIN-11
- **Priority:** Medium
- **Type:** Positive 
- **Preconditions:** The Login page is open.
- **Test data:** Password is: ThisIsVeryLongPasswordWithAbsolutelyNoNumbersInIt (49 characters), for each user:
  - standard_user
  - locked_out_user
  - problem_user
  - performance_glitch_user
  - error_user
  - visual_user
- **Steps:** 
   1. Enter the username.
   2. Enter the password.
   3. Click Login.
- **Expected result:** All characters are entered in the field.
- **Automated:** Planned



### TC-LOGIN-17: Password field maximum length (Maximum Valid)
- **Requirement:** AR-LOGIN-11
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The Login page is open.
- **Test data:** Password is: ThisIsVeryLongPasswordWithAbsolutelyNoNumbersInItX (50 characters), for each user:
    - standard_user
    - locked_out_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login.
- **Expected result:** All 50 characters are entered in the field.
- **Automated:** Planned



### TC-LOGIN-18: Password field maximum length (Over Max Limit)
- **Requirement:** AR-LOGIN-11
- **Priority:** Medium
- **Type:** Negative
- **Preconditions:** The Login page is open.
- **Test data:** Password is: ThisIsVeryLongPasswordWithAbsolutelyNoNumbersInItXY (51 characters), for each user:
    - standard_user
    - locked_out_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login.
- **Expected result:** Only the first 50 characters are entered, the 51st character is not accepted.
- **Automated:** Planned


### TC-LOGIN-19: Entering direct URL without login
- **Requirement:** AR-LOGIN-12
- **Priority:** High
- **Type:** Negative
- **Preconditions:** New Incognito window is open. The Login page is open. Account is not logged in.
- **Test data:** URL: https://www.saucedemo.com/inventory.html
- **Steps:**
   1. Enter URL directly to the address bar.
   2. Press Enter.
- **Expected result:** The inventory page cannot be opened by URL without login.
- **Automated:** Planned



### TC-LOGIN-20: Entering inventory page with back button after logout
- **Requirement:** AR-LOGIN-12
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The Login page is open.
- **Test data:** Password secret_sauce for each user:
  - standard_user
  - problem_user
  - performance_glitch_user
  - error_user
  - visual_user
- **Steps:**
    1. Enter the username.
    2. Enter the password.
    3. Click Login
    4. Click on Menu icon
    5. Click on Logout
    6. Click on back button 
- **Expected result:** The inventory page cannot be opened with the Back button after logout.
- **Automated:** Planned
