# Test Cases – Checkout

### TC-CHK-01: Empty First Name shows its own error message
- **Requirement:** AR-CHK-01, AR-CHK-02
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout: 
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information:
        - First Name: *(empty)*
        - Last Name: Smith
        - Postal Code: 10115
- **Steps:**
    1. Leave First Name empty.
    2. Enter Last Name.
    3. Enter Postal Code.
    4. Click "Continue".
- **Expected result:** The form is not submitted. 
The error message "Error: First Name is required" is shown and the user stays on the Your Information page.
- **Automated:** Planned


### TC-CHK-02: Empty Last Name shows its own error message
- **Requirement:** AR-CHK-01, AR-CHK-02
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information:
        - First Name: John
        - Last Name: *(empty)*
        - Postal Code: 10115
- **Steps:**
    1. Enter First Name.
    2. Leave Last Name empty.
    3. Enter Postal Code.
    4. Click "Continue".
- **Expected result:** The form is not submitted. 
The error message "Error: Last Name is required" is shown and the user stays on the Your Information page.
- **Automated:** Planned


### TC-CHK-03: Empty Postal Code shows its own error message
- **Requirement:** AR-CHK-01, AR-CHK-02
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information:
        - First Name: John
        - Last Name: Smith
        - Postal Code: *(empty)*
- **Steps:**
    1. Enter First Name.
    2. Enter Last Name.
    3. Leave Postal Code empty.
    4. Click "Continue".
- **Expected result:** The form is not submitted. 
The error message "Error: Postal Code is required" is shown and the user stays on the Your Information page.
- **Automated:** Planned


### TC-CHK-04: Form with all fields empty is not submitted
- **Requirement:** AR-CHK-02
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout: 
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
- **Steps:**
    1. Leave all fields empty.
    2. Click "Continue".
- **Expected result:** The form is not submitted. 
The error message "Error: First Name is required" is shown and the user stays on the Your Information page.
- **Automated:** Planned


### TC-CHK-05: Each field accepts typing and enters text only into itself
- **Requirement:** AR-CHK-03
- **Priority:** High
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout: 
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information:
        - First Name: John
        - Last Name: Smith
        - Postal Code: 10115
- **Steps:**
    1. Enter First Name and check the First Name field.
    2. Enter Last Name and check the Last Name field.
    3. Enter Postal Code and check the Postal Code field.
- **Expected result:** Each field shows exactly the text entered into it. No text appears in another field.
- **Automated:** Planned


### TC-CHK-06: First Name and Last Name do not accept numbers
- **Requirement:** AR-CHK-04
- **Priority:** Medium
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout: 
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information:
        - First Name: John123
        - Last Name: Smith123
        - Postal Code: 10115
- **Steps:**
    1. Enter First Name.
    2. Enter Last Name.
    3. Enter Postal Code.
    4. Click "Continue".
- **Expected result:** The form is not submitted.
An error message is shown and the user stays on the Your Information page.
- **Automated:** Planned


### TC-CHK-07: First Name and Last Name do not accept special characters
- **Requirement:** AR-CHK-04
- **Priority:** Medium
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information:
        - First Name: @#$%
        - Last Name: @#$%
        - Postal Code: 10115
- **Steps:**
    1. Enter First Name.
    2. Enter Last Name.
    3. Enter Postal Code.
    4. Click "Continue".
- **Expected result:** The form is not submitted. 
An error message is shown and the user stays on the Your Information page.
- **Automated:** Planned


### TC-CHK-08: Postal Code accepts letters and numbers
- **Requirement:** AR-CHK-05
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information:
        - First Name: John
        - Last Name: Smith
        - Postal Code: ABC12
- **Steps:**
    1. Enter First Name.
    2. Enter Last Name.
    3. Enter Postal Code.
    4. Click "Continue".
- **Expected result:** The form is submitted and the Checkout: Overview page is shown.
- **Automated:** Planned


### TC-CHK-09: A field with spaces only is treated as empty
- **Requirement:** AR-CHK-06
- **Priority:** Medium
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout: 
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information (one field with spaces only per run):
        1. First Name: "   ", Last Name: Smith, Postal Code: 10115
        2. First Name: John, Last Name: "   ", Postal Code: 10115
        3. First Name: John, Last Name: Smith, Postal Code: "   "
- **Steps:**
    1. Enter the values from the first set.
    2. Click "Continue".
    3. Repeat for each set.
- **Expected result:** The form is not submitted. 
The error message for the field with spaces only is shown and the user stays on the Your Information page.
- **Automated:** Planned


### TC-CHK-10: Item total, tax and total are calculated correctly
- **Requirement:** AR-CHK-07
- **Priority:** High
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in, the products from Test data are in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Products:
        - Sauce Labs Backpack
        - Sauce Labs Bike Light
    - Checkout information:
        - First Name: John
        - Last Name: Smith
        - Postal Code: 10115
- **Steps:**
    1. Enter First Name, Last Name and Postal Code.
    2. Click "Continue".
    3. Check the item prices, Item total, Tax and Total on the Overview page.
- **Expected result:** The item total equals the sum of the item prices, and the total equals item total + tax. 
Prices as shown for standard_user:
    - Sauce Labs Backpack – $29.99
    - Sauce Labs Bike Light – $9.99
    - Item total: $39.98
    - Tax: $3.20
    - Total: $43.18
- **Automated:** Planned


### TC-CHK-11: Finish completes the order and empties the cart badge
- **Requirement:** AR-CHK-08
- **Priority:** High
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in, the products from Test data are in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Products:
        - Sauce Labs Backpack
        - Sauce Labs Bike Light
        - Sauce Labs Bolt T-Shirt
        - Sauce Labs Fleece Jacket
        - Sauce Labs Onesie
        - Test.allTheThings() T-Shirt (Red)
    - Checkout information:
        - First Name: John
        - Last Name: Smith
        - Postal Code: 10115
- **Steps:**
    1. Enter First Name, Last Name and Postal Code.
    2. Click "Continue".
    3. Check the cart badge.
    4. Click "Finish".
    5. Check the cart badge.
- **Expected result:** The badge shows 6 before "Finish" and no number after it. 
The Checkout: Complete! page is shown with the message "Thank you for your order!" and "Your order has been dispatched,
and will arrive just as fast as the pony can get there!"
- **Automated:** Planned


### TC-CHK-12: Back Home returns to the inventory page
- **Requirement:** AR-CHK-09
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout: 
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information:
        - First Name: John
        - Last Name: Smith
        - Postal Code: 10115
- **Steps:**
    1. Enter First Name, Last Name and Postal Code.
    2. Click "Continue".
    3. Click "Finish".
    4. Click "Back Home".
- **Expected result:** The inventory page is shown.
- **Automated:** Planned


### TC-CHK-13: Cancel on the Your Information page returns to the cart
- **Requirement:** AR-CHK-10
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
- **Steps:**
    1. Click "Cancel".
- **Expected result:** The cart page is shown and the product is still in the cart.
- **Automated:** Planned


### TC-CHK-14: Cancel on the Overview page returns to the inventory page
- **Requirement:** AR-CHK-10
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Checkout information:
        - First Name: John
        - Last Name: Smith
        - Postal Code: 10115
- **Steps:**
    1. Enter First Name, Last Name and Postal Code.
    2. Click "Continue".
    3. Click "Cancel".
- **Expected result:** The inventory page is shown and the product is still in the cart.
- **Automated:** Planned


### TC-CHK-15: Checkout: Your Information cannot be opened by URL without login
- **Requirement:** AR-CHK-11
- **Priority:** High
- **Type:** Negative
- **Preconditions:** A new Incognito window is open. The user is not logged in.
- **Test data:** URL: https://www.saucedemo.com/checkout-step-one.html
- **Steps:**
    1. Enter the URL in the address bar.
    2. Press Enter.
- **Expected result:** The login page is shown with the error message "Epic sadface: 
You can only access '/checkout-step-one.html' when you are logged in."
- **Automated:** Planned


### TC-CHK-16: Checkout: Overview cannot be opened by URL without login
- **Requirement:** AR-CHK-11
- **Priority:** High
- **Type:** Negative
- **Preconditions:** A new Incognito window is open. The user is not logged in.
- **Test data:** URL: https://www.saucedemo.com/checkout-step-two.html
- **Steps:**
    1. Enter the URL in the address bar.
    2. Press Enter.
- **Expected result:** The login page is shown with the error message 
"Epic sadface: You can only access '/checkout-step-two.html' when you are logged in."
- **Automated:** Planned


### TC-CHK-17: First Name accepts a maximum of 50 characters
- **Requirement:** AR-CHK-12
- **Priority:** Medium
- **Type:** Positive (49, 50 characters), Negative (51 characters)
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - First Name values:
        - 49 characters: johnabcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRS
        - 50 characters: johnabcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRST
        - 51 characters: johnabcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTU
- **Steps:**
    1. Enter the first value in First Name.
    2. Check how many characters were entered.
    3. Clear the field and repeat for each value.
- **Expected result:** With 49 and 50 characters, all characters are entered. With 51 characters, 
only the first 50 are entered.
- **Automated:** Planned


### TC-CHK-18: Last Name accepts a maximum of 50 characters
- **Requirement:** AR-CHK-12
- **Priority:** Medium
- **Type:** Positive (49, 50 characters), Negative (51 characters)
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Last Name values:
        - 49 characters: smithabcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQR
        - 50 characters: smithabcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRS
        - 51 characters: smithabcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRST
- **Steps:**
    1. Enter the first value in Last Name.
    2. Check how many characters were entered.
    3. Clear the field and repeat for each value.
- **Expected result:** With 49 and 50 characters, all characters are entered. With 51 characters, 
only the first 50 are entered.
- **Automated:** Planned


### TC-CHK-19: Postal Code accepts a maximum of 10 characters
- **Requirement:** AR-CHK-13
- **Priority:** Medium
- **Type:** Positive (9, 10 characters), Negative (11 characters)
- **Preconditions:** The user from Test data is logged in, the product from Test data is in the cart and the Checkout:
Your Information page is open.
- **Test data:**
    - Users (password secret_sauce):
        - standard_user
        - problem_user
        - performance_glitch_user
        - error_user
        - visual_user
    - Product: Sauce Labs Backpack
    - Postal Code values:
        - 9 characters: A1B2C3D4E
        - 10 characters: A1B2C3D4E5
        - 11 characters: A1B2C3D4E5F
- **Steps:**
    1. Enter the first value in Postal Code.
    2. Check how many characters were entered.
    3. Clear the field and repeat for each value.
- **Expected result:** With 9 and 10 characters, all characters are entered. With 11 characters,
only the first 10 are entered.
- **Automated:** Planned