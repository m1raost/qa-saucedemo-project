# Run 01 – Checkout

**Date:** 10.–17.11.2026
**Browser:** Chrome 157.0.8103.51 (TC-CHK-17 to 19: Chrome 157.0.8103.79)
**OS:** macOS 14.8.9

### TC-CHK-01: Empty First Name shows its own error message
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name, so First Name cannot stay empty (#4)
  - performance_glitch_user: Pass
  - error_user: Blocked – "Last Name" field does not accept typing, so the other fields cannot be filled (#18)
  - visual_user: Pass
- **Bug:** #4, #18
- **Notes:** –


### TC-CHK-02: Empty Last Name shows its own error message
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Fail – checkout form is accepted with an empty Last Name (#19)
  - visual_user: Pass
- **Bug:** #19
- **Notes:** –


### TC-CHK-03: Empty Postal Code shows its own error message
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name, so Last Name cannot be filled (#4)
  - performance_glitch_user: Pass
  - error_user: Blocked – "Last Name" field does not accept typing, so Last Name cannot be filled (#18)
  - visual_user: Pass
- **Bug:** #4, #18
- **Notes:** –


### TC-CHK-04: Form with all fields empty is not submitted
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-CHK-05: Each field accepts typing and enters text only into itself
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – typing in Last Name enters text into First Name (#4)
  - performance_glitch_user: Pass
  - error_user: Fail – "Last Name" field does not accept typing (#18)
  - visual_user: Pass
- **Bug:** #4, #18
- **Notes:** –


### TC-CHK-06: First Name and Last Name do not accept numbers
- **Results:**
  - standard_user: Fail – First Name and Last Name accept numbers and special characters (#20)
  - problem_user: Blocked – typing in Last Name enters text into First Name (#4)
  - performance_glitch_user: Fail – First Name and Last Name accept numbers and special characters (#20)
  - error_user: Blocked – "Last Name" field does not accept typing (#18)
  - visual_user: Fail – First Name and Last Name accept numbers and special characters (#20)
- **Bug:** #4, #18, #20
- **Notes:** –


### TC-CHK-07: First Name and Last Name do not accept special characters
- **Results:**
  - standard_user: Fail – First Name and Last Name accept numbers and special characters (#20)
  - problem_user: Blocked – typing in Last Name enters text into First Name (#4)
  - performance_glitch_user: Fail – First Name and Last Name accept numbers and special characters (#20)
  - error_user: Blocked – "Last Name" field does not accept typing (#18)
  - visual_user: Fail – First Name and Last Name accept numbers and special characters (#20)
- **Bug:** #4, #18, #20
- **Notes:** –


### TC-CHK-08: Postal Code accepts letters and numbers
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name (#4)
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** #4
- **Notes:** error_user: tested with an empty Last Name, as the field does not accept typing (#18) but the form is accepted without it (#19).


### TC-CHK-09: A field with spaces only is treated as empty
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name (#4)
  - performance_glitch_user: Pass
  - error_user: Blocked – "Last Name" field does not accept typing (#18)
  - visual_user: Pass
- **Bug:** #4, #18, #23
- **Notes:** Found during this test: pressing Return submits the form with empty fields – see TC-CHK-20 (#23).


### TC-CHK-10: Item total, tax and total are calculated correctly
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name (#4)
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** #4
- **Notes:** error_user: tested with an empty Last Name, as the field does not accept typing (#18) but the form is accepted without it (#19).


### TC-CHK-11: Finish completes the order and empties the cart badge
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name (#4), and some products cannot be added (#3)
  - performance_glitch_user: Pass
  - error_user: Fail – "Finish" button does not respond (#21)
  - visual_user: Pass
- **Bug:** #3, #4, #21
- **Notes:** –


### TC-CHK-12: Back Home returns to the inventory page
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name (#4)
  - performance_glitch_user: Pass
  - error_user: Blocked – "Finish" button does not respond (#21)
  - visual_user: Pass
- **Bug:** #4, #21
- **Notes:** –


### TC-CHK-13: Cancel on the Your Information page returns to the cart
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-CHK-14: Cancel on the Overview page returns to the inventory page
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name (#4)
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** #4
- **Notes:** error_user: tested with an empty Last Name, as the field does not accept typing (#18) but the form is accepted without it (#19).


### TC-CHK-15: Checkout: Your Information cannot be opened by URL without login
- **Results:**
  - URL without login: Pass
- **Bug:** –
- **Notes:** –


### TC-CHK-16: Checkout: Overview cannot be opened by URL without login
- **Results:**
  - URL without login: Pass
- **Bug:** –
- **Notes:** –


### TC-CHK-17: First Name accepts a maximum of 50 characters
- **Results:**
  - standard_user: Fail – checkout fields accept more characters than the limit (#22)
  - problem_user: Fail – checkout fields accept more characters than the limit (#22)
  - performance_glitch_user: Fail – checkout fields accept more characters than the limit (#22)
  - error_user: Fail – checkout fields accept more characters than the limit (#22)
  - visual_user: Fail – checkout fields accept more characters than the limit (#22)
- **Bug:** #22
- **Notes:** –


### TC-CHK-18: Last Name accepts a maximum of 50 characters
- **Results:**
  - standard_user: Fail – checkout fields accept more characters than the limit (#22)
  - problem_user: Blocked – typing in Last Name enters text into First Name (#4)
  - performance_glitch_user: Fail – checkout fields accept more characters than the limit (#22)
  - error_user: Blocked – "Last Name" field does not accept typing (#18)
  - visual_user: Fail – checkout fields accept more characters than the limit (#22)
- **Bug:** #4, #18, #22
- **Notes:** –


### TC-CHK-19: Postal Code accepts a maximum of 10 characters
- **Results:**
  - standard_user: Fail – checkout fields accept more characters than the limit (#22)
  - problem_user: Fail – checkout fields accept more characters than the limit (#22)
  - performance_glitch_user: Fail – checkout fields accept more characters than the limit (#22)
  - error_user: Fail – checkout fields accept more characters than the limit (#22)
  - visual_user: Fail – checkout fields accept more characters than the limit (#22)
- **Bug:** #22
- **Notes:** –


### TC-CHK-20: Form with empty fields is not submitted with the Return key
- **Results:**
  - standard_user: Fail – pressing Return submits the form with empty fields (#23)
  - problem_user: Fail – pressing Return submits the form with empty fields (#23)
  - performance_glitch_user: Fail – pressing Return submits the form with empty fields (#23)
  - error_user: Fail – pressing Return submits the form with empty fields (#23)
  - visual_user: Fail – pressing Return submits the form with empty fields (#23)
- **Bug:** #23
- **Notes:** Test case added during this run, after the bug was found in TC-CHK-09.


