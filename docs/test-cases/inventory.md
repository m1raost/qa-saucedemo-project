# Test Cases – Inventory

### TC-INV-01: Cart badge shows the correct number of items
- **Requirement:** AR-GEN-01
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
    - Sauce Labs Bolt T-Shirt
- **Steps:**
  1. Click "Add to cart" for both products.
  2. Check the cart badge.
  3. Click "Remove" for the first product.
  4. Check the cart badge.
  5. Click "Remove" for the second product.
  6. Check the cart badge.
- **Expected result:** The badge shows 2 after step 2 and 1 after step 4. After step 6 no number is shown.
- **Automated:** Planned


### TC-INV-02: Cart icon and badge are in the correct position on every page
- **Requirement:** AR-GEN-02
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
  - Product in cart: Sauce Labs Backpack
  - Checkout form: First Name "John", Last Name "Smith", Postal Code "10115"
  - Pages:
    - Inventory page
    - Product page (one product – all product pages use the same layout)
    - Cart page
    - Checkout: Your Information
    - Checkout: Overview
- **Steps:**
  1. Add the product to the cart.
  2. Check the cart icon and badge on the inventory page.
  3. Open the product page and check the cart icon and badge.
  4. Open the cart and check the cart icon and badge.
  5. Click "Checkout" and check the cart icon and badge.
  6. Fill in the form, click "Continue" and check the cart icon and badge.
- **Expected result:** The cart icon and the number badge are in the correct position in the top right corner on every page.
- **Automated:** No


### TC-INV-03: Menu icon lines are straight on every page
- **Requirement:** AR-GEN-03
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
  - Product in cart: Sauce Labs Backpack
  - Checkout form: First Name "John", Last Name "Smith", Postal Code "10115"
  - Pages:
    - Inventory page
    - Product page (one product – all product pages use the same layout)
    - Cart page
    - Checkout: Your Information
    - Checkout: Overview
- **Steps:**
  1. Check the menu icon on the inventory page.
  2. Add the product to the cart.
  3. Open the product page and check the menu icon.
  4. Open the cart and check the menu icon.
  5. Click "Checkout" and check the menu icon.
  6. Fill in the form, click "Continue" and check the menu icon.
- **Expected result:** The three menu icon lines are straight and parallel on every page.
- **Automated:** No


### TC-INV-04: User stays logged in while using the application
- **Requirement:** AR-GEN-04
- **Priority:** High
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
  - Checkout form: First Name "John", Last Name "Smith", Postal Code "10115"
- **Steps:**
  1. Add the product to the cart.
  2. Open the product page.
  3. Open the cart.
  4. Click "Checkout".
  5. Fill in the form and click "Continue".
  6. After each step, check that the user is still logged in.
- **Expected result:** The user stays logged in on every page and is not redirected to the login page.
- **Automated:** Planned


### TC-INV-05: Product image is the same on the inventory page and the product page
- **Requirement:** AR-INV-01
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
  - Products:
    - Sauce Labs Backpack
    - Sauce Labs Bike Light
    - Sauce Labs Bolt T-Shirt
    - Sauce Labs Fleece Jacket
    - Sauce Labs Onesie
    - Test.allTheThings() T-Shirt (Red)
- **Steps:**
  1. Check the product image on the inventory page.
  2. Click the product name.
  3. Check the product image on the product page.
  4. Click "Back to products".
  5. Repeat for every product.
- **Expected result:** Each product shows the same image on the inventory page and the product page.
- **Automated:** No


### TC-INV-06: Product name is the same on the inventory page and the product page
- **Requirement:** AR-INV-01
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
  - Products:
    - Sauce Labs Backpack
    - Sauce Labs Bike Light
    - Sauce Labs Bolt T-Shirt
    - Sauce Labs Fleece Jacket
    - Sauce Labs Onesie
    - Test.allTheThings() T-Shirt (Red)
- **Steps:**
  1. Check the product name on the inventory page.
  2. Click the product name.
  3. Check the product name on the product page.
  4. Click "Back to products".
  5. Repeat for every product.
- **Expected result:** Each product shows the same name on the inventory page and the product page.
- **Automated:** Planned


### TC-INV-07: Product price is the same on the inventory page and the product page
- **Requirement:** AR-INV-01
- **Priority:** High
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
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
  1. Check the product price on the inventory page.
  2. Click the product name.
  3. Check the product price on the product page.
  4. Click "Back to products".
  5. Repeat for every product.
- **Expected result:** Each product shows the same price on the inventory page and the product page.
- **Automated:** Planned


### TC-INV-08: Product description is the same on the inventory page and the product page
- **Requirement:** AR-INV-01
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
  - Products:
    - Sauce Labs Backpack
    - Sauce Labs Bike Light
    - Sauce Labs Bolt T-Shirt
    - Sauce Labs Fleece Jacket
    - Sauce Labs Onesie
    - Test.allTheThings() T-Shirt (Red)
- **Steps:**
  1. Check the product description on the inventory page.
  2. Click the product name.
  3. Check the product description on the product page.
  4. Click "Back to products".
  5. Repeat for every product.
- **Expected result:** Each product shows the same description on the inventory page and the product page.
- **Automated:** Planned


### TC-INV-09: Every product has a description
- **Requirement:** AR-INV-02
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
  - Products:
    - Sauce Labs Backpack
    - Sauce Labs Bike Light
    - Sauce Labs Bolt T-Shirt
    - Sauce Labs Fleece Jacket
    - Sauce Labs Onesie
    - Test.allTheThings() T-Shirt (Red)
- **Steps:**
  1. Click the product name.
  2. Check the description on the product page.
  3. Click "Back to products".
  4. Repeat for every product.
- **Expected result:** Every product page shows a description.
- **Automated:** Planned


### TC-INV-10: Every product shows its own image on the inventory page
- **Requirement:** AR-INV-03
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
  - Products:
    - Sauce Labs Backpack
    - Sauce Labs Bike Light
    - Sauce Labs Bolt T-Shirt
    - Sauce Labs Fleece Jacket
    - Sauce Labs Onesie
    - Test.allTheThings() T-Shirt (Red)
- **Steps:**
  1. Check the image of every product on the inventory page.
  2. Compare each image with the product name.
- **Expected result:** Every image matches its product name (e.g. the Backpack shows a backpack). No product shows a placeholder or a dog picture.
- **Automated:** No


### TC-INV-11: Prices stay the same after reload and Back/Forward navigation
- **Requirement:** AR-INV-04
- **Priority:** High
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
  - Products: all products on the inventory page
- **Steps:**
  1. Write down the prices of all products.
  2. Reload the page and compare the prices.
  3. Click the name of any product and write down its price on the product page.
  4. Click the browser Back button and compare the prices.
  5. Click the browser Forward button and compare the price with step 3.
- **Expected result:** All prices stay the same after reload and after Back/Forward navigation.
- **Automated:** Planned


### TC-INV-12: Every product opens its own product page
- **Requirement:** AR-INV-05
- **Priority:** High
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in and the inventory page is open.
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
  1. Click the product name.
  2. Check the product name on the product page.
  3. Click "Back to products".
  4. Repeat for every product.
- **Expected result:** Every product opens the page of the same product. "ITEM NOT FOUND" is never shown.
- **Automated:** Planned


### TC-INV-13: A product that is not found cannot be added to the cart
- **Requirement:** AR-INV-06
- **Priority:** High
- **Type:** Negative
- **Preconditions:** The user from Test data is logged in, the inventory page is open and the cart is empty.
- **Test data:**
  - User: problem_user / secret_sauce (the only user where a product opens "ITEM NOT FOUND")
  - Product: Sauce Labs Fleece Jacket
- **Steps:**
  1. Click "Sauce Labs Fleece Jacket".
  2. On the "ITEM NOT FOUND" page, click "Add to cart".
  3. Check the cart badge.
- **Expected result:** The product cannot be added. The cart badge shows no number.
- **Automated:** Planned


### TC-INV-14: Adding and removing works for every product
- **Requirement:** AR-INV-07
- **Priority:** High
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
  1. Click "Add to cart" for the product.
  2. Check the button text and the cart badge.
  3. Click "Remove" for the same product.
  4. Check the button text and the cart badge.
  5. Repeat for every product.
- **Expected result:** After "Add to cart", the button changes to "Remove" and the badge goes up by 1. After "Remove", the button changes back to "Add to cart" and the badge goes down by 1.
- **Automated:** Planned


### TC-INV-15: Sorting by Name (A to Z)
- **Requirement:** AR-INV-08
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
  1. Open the sorting dropdown.
  2. Select "Name (A to Z)".
  3. Check the order of the products.
- **Expected result:** No error message is shown. The products are in this order:
  1. Sauce Labs Backpack
  2. Sauce Labs Bike Light
  3. Sauce Labs Bolt T-Shirt
  4. Sauce Labs Fleece Jacket
  5. Sauce Labs Onesie
  6. Test.allTheThings() T-Shirt (Red)
- **Automated:** Planned


### TC-INV-16: Sorting by Name (Z to A)
- **Requirement:** AR-INV-08
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
  1. Open the sorting dropdown.
  2. Select "Name (Z to A)".
  3. Check the order of the products.
- **Expected result:** No error message is shown. The products are in this order:
  1. Test.allTheThings() T-Shirt (Red)
  2. Sauce Labs Onesie
  3. Sauce Labs Fleece Jacket
  4. Sauce Labs Bolt T-Shirt
  5. Sauce Labs Bike Light
  6. Sauce Labs Backpack
- **Automated:** Planned


### TC-INV-17: Sorting by Price (low to high)
- **Requirement:** AR-INV-08
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
  1. Open the sorting dropdown.
  2. Select "Price (low to high)".
  3. Check the order of the products.
- **Expected result:** No error message is shown. The products are in this order (prices as shown for standard_user):
  1. Sauce Labs Onesie – $7.99
  2. Sauce Labs Bike Light – $9.99
  3. Sauce Labs Bolt T-Shirt – $15.99
  4. Test.allTheThings() T-Shirt (Red) – $15.99
  5. Sauce Labs Backpack – $29.99
  6. Sauce Labs Fleece Jacket – $49.99
- **Automated:** Planned


### TC-INV-18: Sorting by Price (high to low)
- **Requirement:** AR-INV-08
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
  1. Open the sorting dropdown.
  2. Select "Price (high to low)".
  3. Check the order of the products.
- **Expected result:** No error message is shown. The products are in this order (prices as shown for standard_user):
  1. Sauce Labs Fleece Jacket – $49.99
  2. Sauce Labs Backpack – $29.99
  3. Sauce Labs Bolt T-Shirt – $15.99
  4. Test.allTheThings() T-Shirt (Red) – $15.99
  5. Sauce Labs Bike Light – $9.99
  6. Sauce Labs Onesie – $7.99
- **Automated:** Planned


### TC-INV-19: Inventory page loads in under 3 seconds
- **Requirement:** AR-INV-09
- **Priority:** Medium
- **Type:** Positive
- **Preconditions:** The login page is open.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
- **Steps:**
  1. Log in and measure the time until the inventory page is shown.
  2. Click any product name to open the product page.
  3. Click the browser Back button and measure the time until the inventory page is shown.
  4. Select any sorting option and measure the time until the products are sorted.
- **Expected result:** The inventory page is shown in under 3 seconds after login, after Back navigation and after sorting.
- **Automated:** Planned


### TC-INV-20: Remove button stays inside its boundaries
- **Requirement:** AR-INV-10
- **Priority:** Low
- **Type:** Positive
- **Preconditions:** The user from Test data is logged in, the inventory page is open and the cart is empty.
- **Test data:**
  - Users (password secret_sauce):
    - standard_user
    - problem_user
    - performance_glitch_user
    - error_user
    - visual_user
  - Products: all products on the inventory page
- **Steps:**
  1. Click "Add to cart" for every product.
  2. Check the position of every "Remove" button.
- **Expected result:** Every "Remove" button is aligned like the others and stays inside its product card.
- **Automated:** No
