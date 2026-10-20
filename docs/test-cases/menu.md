# Test Cases – Menu

### TC-MENU-01: "All Items" returns to the inventory page from every page
- **Requirement:** AR-MENU-01
- **Priority:** Low
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
  - Product: Sauce Labs Backpack (all product pages use the same layout)
  - Checkout information:
    - First Name: John
    - Last Name: Smith
    - Postal Code: 10115
  - Pages:
    - Product page
    - Cart
    - Checkout: Your Information
    - Checkout: Overview
    - Checkout: Complete!
- **Steps:**
  1. Click the product name, open the menu and click "All Items".
  2. Add the product to the cart, click the cart icon, open the menu and click "All Items".
  3. Click the cart icon, click "Checkout", open the menu and click "All Items".
  4. Click the cart icon, click "Checkout", fill in the form, click "Continue", open the menu and click "All Items".
  5. Click the cart icon, click "Checkout", fill in the form, click "Continue", click "Finish", 
  open the menu and click "All Items".
- **Expected result:** After every "All Items" click, the inventory page is shown.
- **Automated:** Planned


### TC-MENU-02: Dynamic Catalog – Lazy Load shows all products correctly
- **Requirement:** AR-MENU-02
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
  1. Open the menu.
  2. Click "Dynamic Catalog" and then "Lazy Load".
  3. Scroll down and check the products.
- **Expected result:** All 6 products load while scrolling and are shown with their name, image, price and
- different sizes.
- **Automated:** No


### TC-MENU-03: Dynamic Catalog – Spinner shows all products correctly
- **Requirement:** AR-MENU-02
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
  1. Open the menu.
  2. Click "Dynamic Catalog" and then "Spinner".
  3. Wait until loading is finished and check the products.
- **Expected result:** A loading spinner is shown first. Then all 6 products are shown with their name, image and price.
- **Automated:** No


### TC-MENU-04: Dynamic Catalog – Slider shows all products correctly
- **Requirement:** AR-MENU-02
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
  1. Open the menu.
  2. Click "Dynamic Catalog" and then "Slider".
  3. Watch the slider until it has shown every product.
- **Expected result:** The slider shows one product at a time and moves to the next one in a loop. 
- All 6 products are shown.
- **Automated:** No


### TC-MENU-05: Dynamic Catalog – Lazy Load shows each product only once
- **Requirement:** AR-MENU-03
- **Priority:** Low
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
  1. Open the menu.
  2. Click "Dynamic Catalog" and then "Lazy Load".
  3. Scroll down to the end of the page.
- **Expected result:** Each product is shown only once. 
- Loading stops after the last product and no products are repeated.
- **Automated:** No


### TC-MENU-06: "About" opens the Sauce Labs home page
- **Requirement:** AR-MENU-04
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
  1. Open the menu.
  2. Click "About".
  3. Check the page that opens.
- **Expected result:** https://saucelabs.com/ opens without an error.
- **Automated:** Planned


### TC-MENU-07: Logout returns to the login page from every page
- **Requirement:** AR-MENU-05
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
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
  - Pages:
    - Inventory page
    - Product page
    - Cart
    - Checkout: Your Information
    - Checkout: Overview
    - Checkout: Complete!
- **Steps:**
  1. Open the page from Test data (add the product and fill in the form to reach the checkout pages).
  2. Open the menu and click "Logout".
  3. Check the page that opens.
  4. Log in with the same user and repeat for each page.
- **Expected result:** After every Logout click, the login page is shown.
- **Automated:** Planned


### TC-MENU-08: Reset App State empties the cart and resets the product buttons
- **Requirement:** AR-MENU-06
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
  1. Click "Add to cart" for every product.
  2. Check the cart badge and the product buttons.
  3. Open the menu and click "Reset App State".
  4. Close the menu with "X".
  5. Check the cart badge and the product buttons.
  6. Click the cart icon and check the cart.
- **Expected result:** Before the reset, the badge shows 6 and every button shows "Remove". 
- After the reset, the badge shows no number, every button shows "Add to cart" and the cart is empty.
- **Automated:** Planned


### TC-MENU-09: Order cannot be completed after Reset App State during checkout
- **Requirement:** AR-MENU-07
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in, the products from Test data are in the cart,
- Checkout information from Test Data is filled in, and the Checkout: Overview page is open.
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
  1. Open the menu and click "Reset App State".
  2. Close the menu with "X".
  3. Click "Finish".
- **Expected result:** The order is not completed and the Checkout: Complete! page is not opened.
- **Automated:** Planned


### TC-MENU-10: Footer social media icons open the correct pages
- **Requirement:** AR-MENU-08
- **Priority:** Low
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
  - Footer links:
    - X: https://x.com/saucelabs
    - Facebook: https://www.facebook.com/saucelabs
    - LinkedIn: https://www.linkedin.com/company/sauce-labs/
- **Steps:**
  1. Scroll down to the footer.
  2. Click a social media icon.
  3. Check the URL of the page that opens.
  4. Close the new tab.
  5. Repeat for each icon.
- **Expected result:** Each icon opens its URL from Test data in a new tab.
- **Automated:** Planned


### TC-MENU-11: Menu opens with the menu icon and closes with X on every page
- **Requirement:** AR-MENU-09
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
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
  - Pages:
    - Inventory page
    - Product page
    - Cart
    - Checkout: Your Information
    - Checkout: Overview
    - Checkout: Complete!
- **Steps:**
  1. Open the page from Test data (add the product and fill in the form to reach the checkout pages).
  2. Click the menu icon and check the menu.
  3. Click "X" and check the menu.
  4. Repeat for each page.
- **Expected result:** On every page, the menu opens with the menu icon and closes with "X".
- **Automated:** Planned