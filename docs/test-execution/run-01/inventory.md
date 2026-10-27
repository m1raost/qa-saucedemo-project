# Run 01 – Inventory

**Date:** 21.–23.10.2026
**Browser:** Chrome 156.0.8078.48
**OS:** macOS 14.8.9

### TC-INV-01: Cart badge shows the correct number of items
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – "Add to cart" and "Remove" do not work for some products (#3)
  - performance_glitch_user: Pass
  - error_user: Blocked – "Add to cart" and "Remove" do not work for some products (#3)
  - visual_user: Pass
- **Bug:** #3
- **Notes:** –


### TC-INV-02: Cart icon and badge are in the correct position on every page
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name, so Checkout: Overview cannot be reached (#4). Other pages: Pass.
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Fail – the cart icon and badge are out of place and overlap the page layout (#5)
- **Bug:** #4, #5
- **Notes:** –


### TC-INV-03: Menu icon lines are straight on every page
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name, so Checkout: Overview cannot be reached (#4). Other pages: Pass.
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Fail – the menu icon lines are slanted on every page (#6)
- **Bug:** #4, #6
- **Notes:** –


### TC-INV-04: User stays logged in while using the application
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name, so Checkout: Overview cannot be reached (#4). Other pages: Pass.
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** #4
- **Notes:** –


### TC-INV-05: Product image is the same on the inventory page and the product page
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – the inventory page shows a dog picture for every product, and clicking a product opens a different product (#7, #8)
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Fail – the first product on the inventory page shows a dog picture (#7)
- **Bug:** #7, #8
- **Notes:** –


### TC-INV-06: Product name is the same on the inventory page and the product page
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – clicking a product opens a different product (#8)
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** #8
- **Notes:** –


### TC-INV-07: Product price is the same on the inventory page and the product page
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – clicking a product opens a different product (#8)
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Fail – the inventory page shows a different price than the product page (#9)
- **Bug:** #8, #9
- **Notes:** –


### TC-INV-08: Product description is the same on the inventory page and the product page
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – clicking a product opens a different product (#8)
  - performance_glitch_user: Pass
  - error_user: Fail – product pages show no description (#10)
  - visual_user: Pass
- **Bug:** #8, #10
- **Notes:** –


### TC-INV-09: Every product has a description
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Fail – product pages show no description (#10)
  - visual_user: Pass
- **Bug:** #10
- **Notes:** problem_user: a description is shown, but it belongs to a different product – see #8.


### TC-INV-10: Every product shows its own image on the inventory page
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – every product shows a dog picture (#7)
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Fail – the product in first place shows a dog picture, all other images are correct (#7)
- **Bug:** #7
- **Notes:** –


### TC-INV-11: Prices stay the same after reload and Back/Forward navigation
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Fail – prices on the inventory page change after reload and Back/Forward navigation (#9)
- **Bug:** #9
- **Notes:** Step 5 does not say what to compare the product page price with – test case to be updated (compare with the price on the same product page before Back/Forward).


### TC-INV-12: Every product opens its own product page
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – clicking a product opens a different product (#8)
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** #8
- **Notes:** –


### TC-INV-13: A product that is not found cannot be added to the cart
- **Results:**
  - problem_user: Fail – the "ITEM NOT FOUND" product can be added to the cart (#11)
- **Bug:** #11
- **Notes:** –


### TC-INV-14: Adding and removing works for every product
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – "Add to cart" and "Remove" do not work for some products (#3)
  - performance_glitch_user: Pass
  - error_user: Fail – "Add to cart" and "Remove" do not work for some products (#3)
  - visual_user: Pass
- **Bug:** #3
- **Notes:** –


### TC-INV-15: Sorting by Name (A to Z)
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** problem_user and error_user pass only because "Name (A to Z)" is the default order – see #12 and #13.


### TC-INV-16: Sorting by Name (Z to A)
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – sorting does not work (#12)
  - performance_glitch_user: Pass
  - error_user: Fail – the alert "Sorting is broken!" appears (#13)
  - visual_user: Pass
- **Bug:** #12, #13
- **Notes:** –


### TC-INV-17: Sorting by Price (low to high)
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – sorting does not work (#12)
  - performance_glitch_user: Pass
  - error_user: Fail – the alert "Sorting is broken!" appears (#13)
  - visual_user: Fail – products are in the correct order, but the displayed prices are wrong, so the list does not look sorted (#9)
- **Bug:** #9, #12, #13
- **Notes:** –


### TC-INV-18: Sorting by Price (high to low)
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – sorting does not work (#12)
  - performance_glitch_user: Pass
  - error_user: Fail – the alert "Sorting is broken!" appears (#13)
  - visual_user: Fail – products are in the correct order, but the displayed prices are wrong, so the list does not look sorted (#9)
- **Bug:** #9, #12, #13
- **Notes:** –


### TC-INV-19: Inventory page loads in under 3 seconds
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – sorting does not work (#12), Other checks: Pass
  - performance_glitch_user: Fail - Inventory page takes more than 5 seconds to load (#14)
  - error_user: Blocked - the alert "Sorting is broken!" appears (#13), Other checks: Pass
  - visual_user: Pass
- **Bug:** #12, #13, #14
- **Notes:** –



### TC-INV-20: Remove button stays inside its boundaries
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – "Add to cart" does not work for some products, so their "Remove" button cannot be checked (#3). Other products: Pass.
  - performance_glitch_user: Pass
  - error_user: Blocked – "Add to cart" does not work for some products, so their "Remove" button cannot be checked (#3). Other products: Pass.
  - visual_user: Fail – the "Remove" button of "Test.allTheThings() T-Shirt (Red)" is outside its product card (#15)
- **Bug:** #3, #15
- **Notes:** –

