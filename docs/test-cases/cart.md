# Test Cases – Cart

### TC-CART-01: Prices in the cart match the inventory page
- **Requirement:** AR-CART-01
- **Priority:** High
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the products from Test data are in the cart.
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
- **Steps:**
  1. Check the price of every product on the inventory page.
  2. Click the cart icon.
  3. Check the price of every product in the cart.
- **Expected result:** Every price in the cart is the same as on the inventory page. Prices as shown for standard_user:
  - Sauce Labs Fleece Jacket – $49.99
  - Sauce Labs Backpack – $29.99
  - Sauce Labs Bolt T-Shirt – $15.99
  - Test.allTheThings() T-Shirt (Red) – $15.99
  - Sauce Labs Bike Light – $9.99
  - Sauce Labs Onesie – $7.99
- **Automated:** Planned


### TC-CART-02: Removing a product in the cart updates the cart badge
- **Requirement:** AR-CART-02
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the products from Test data are in the cart.
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
- **Steps:**
  1. Click the cart icon.
  2. Check the cart badge.
  3. Click "Remove" for one product and check the cart badge.
  4. Repeat step 3 for every product.
- **Expected result:** The badge shows 6 before the first removal and goes down by 1 after each "Remove".
  After the last removal, no number is shown.
- **Automated:** Planned


### TC-CART-03: Products stay in the cart after logout and login
- **Requirement:** AR-CART-03
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in, the inventory page is open and the cart is empty.
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
- **Steps:**
  1. Add every product to the cart.
  2. Check the cart badge.
  3. Click the menu icon and click "Logout".
  4. Log in with the same user.
  5. Check the cart badge.
  6. Click the cart icon and check the products in the cart.
- **Expected result:** The badge shows 6 before logout and after login. The same 6 products are in the cart after login.
- **Automated:** Planned


### TC-CART-04: "Continue Shopping" loads the inventory page in under 3 seconds
- **Requirement:** AR-CART-04
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the product from Test data is in the cart.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
  - Product: Sauce Labs Backpack
- **Steps:**
  1. Click the cart icon.
  2. Click "Continue Shopping".
  3. Measure the time until the inventory page is shown.
- **Expected result:** The inventory page is shown in under 3 seconds.
- **Automated:** Planned


### TC-CART-05: Browser Back button loads the inventory page in under 3 seconds
- **Requirement:** AR-CART-04
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the product from Test data is in the cart.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
  - Product: Sauce Labs Backpack
- **Steps:**
  1. Click the cart icon.
  2. Click the browser Back button.
  3. Measure the time until the inventory page is shown.
- **Expected result:** The inventory page is shown in under 3 seconds.
- **Automated:** Planned


### TC-CART-06: Checkout button is at the bottom of the page
- **Requirement:** AR-CART-05
- **Priority:** Low
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the product from Test data is in the cart.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
  - Product: Sauce Labs Backpack
- **Steps:**
  1. Click the cart icon.
  2. Check the position of the "Checkout" button.
- **Expected result:** The "Checkout" button is at the bottom of the page, next to "Continue Shopping".
- **Automated:** No


### TC-CART-07: Checkout with an empty cart is not possible
- **Requirement:** AR-CART-06
- **Priority:** Medium
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in and the cart is empty.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
  1. Click the cart icon.
  2. Click "Checkout".
- **Expected result:** An error message is shown and the user stays on the cart page.
- **Automated:** Planned