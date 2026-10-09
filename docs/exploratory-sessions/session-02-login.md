# Session 02 – Inventory

**Date:** 09.10.2026
**Duration:** 60 min
**Browser:** Chrome 155.0.8059.40
**Charter:** Explore the inventory page and product details with different users 
to find errors in sorting, product information and adding/removing items.

## What I tried
- standard_user / secret_sauce – sorting works, prices, images and descriptions are correct,
and the cart badge shows added and removed items correctly. Used as the reference for the other users.
- locked_out_user / secret_sauce – blocked on the login page, no access to the inventory.
- problem_user, performance_glitch_user, error_user and visual_user / secret_sauce – 
for each user I sorted by all 4 options, added and removed all items, and opened each product page.

## Bugs found

### problem_user
- All items on the inventory page show the same dog picture. 
- The product page shows a different picture than the inventory page.
- Opening "Sauce Labs Backpack" shows the product page of "Sauce Labs Fleece Jacket".
- Opening the Bike Light and the T-shirts shows a different product and name.
- Opening "Sauce Labs Fleece Jacket" shows "ITEM NOT FOUND" with the message 
  "We're sorry, but your call could not be completed as dialled".
- The "ITEM NOT FOUND" product can be added to the cart.
- Adding and removing items does not work correctly: 
  some items cannot be added again and some cannot be removed.
- None of the sorting options work.
- The user is logged out after going to the cart page.

### performance_glitch_user
- Pages take a long time to load after login, after pressing the Back button and when sorting.
- The cart badge shows 1 item when the cart is empty.

### error_user
- The cart badge shows 1 item when the cart is empty.
- Product pages have no descriptions.
- After adding an item to the cart, the Remove button does not respond.
- "Sauce Labs Backpack", "Sauce Labs Bike Light" and "Sauce Labs Onesie" cannot be removed from the cart.
- "Sauce Labs Bolt T-Shirt", "Sauce Labs Fleece Jacket" and "Test.allTheThings() T-Shirt (Red)"
  cannot be added to the cart.
- Sorting fails with the error "Sorting is broken! This error has been reported to Backtrace."

### visual_user
- The cart badge is out of place and overlaps the page layout.
- The menu icon lines are slanted.
- "Sauce Labs Backpack" shows a dog picture on the inventory page and
  the correct backpack picture on the product page.
- Prices on the inventory page are different from the prices on the product pages.
- Prices change after reloading the page or using Back/Forward. For example, "Sauce Labs Backpack"
  changed from $95.11 to $87.80, and "Sauce Labs Bike Light" from $2.19 to $75.01.
- Price sorting is not correct.
- After each sorting option, the item in first place shows a dog picture.
- The Remove button of "Test.allTheThings() T-Shirt (Red)" is shifted outside its boundaries.

## Questions
- Is the logout of problem_user after opening the cart caused by a session timeout or by a defect?
  Needs to be checked again in the cart session.

## Ideas for test cases
- The product picture is the same on the inventory page and the product page.
- The product name is the same on the inventory page and the product page.
- Every product page has a description.
- No product shows the dog picture.
- Prices are the same on the inventory page and the product page,
  and stay the same after reload or Back/Forward.
- Every product opens its own page, with no "ITEM NOT FOUND".
- An item that is not found cannot be added to the cart.
- Adding and removing works for every item.
- The cart badge number matches the items added and removed.
- An empty cart shows no number on the cart badge.
- The user is not logged out unexpectedly.
- Sorting A–Z, Z–A, price low to high and price high to low works correctly, with no error message.
- Pages load in an acceptable time after login, Back navigation and sorting.
- The cart badge is in the correct position.
- The menu icon lines are straight.
- The Remove button stays inside its boundaries.