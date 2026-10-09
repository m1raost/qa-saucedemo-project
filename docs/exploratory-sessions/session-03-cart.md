# Session 03 – Cart

**Date:** 09.10.2026
**Duration:** 45 min
**Browser:** Chrome 155.0.8059.40
**Charter:** Explore the cart page with different users to find errors in the item list,
removing items, navigation and the cart badge.

## What I tried
- standard_user / secret_sauce – prices on the inventory page and in the cart are the same, 
  the cart badge updates when items are added or removed, Remove buttons work, items stay in the cart after logout,
  and "Reset App State" removes all items from the cart. Used as the reference for the other users.
- locked_out_user / secret_sauce – stays on the login page with the error 
  "Epic sadface: Sorry, this user has been locked out."
- problem_user, performance_glitch_user, error_user and visual_user / secret_sauce – 
  for each user I compared prices with the inventory page, removed items from the cart, checked the cart badge,
  used Continue Shopping, Checkout and the Back button, logged out and in again,
  opened an empty cart and used "Reset App State".
- problem_user – opened the cart several times to recheck the logout from Session 02: 
  [logout time out after 10 min of no-activity].

## Bugs found

### problem_user
- No bugs found.

### performance_glitch_user
- "Continue Shopping" and the browser Back button take a long time to load the inventory page.

### error_user
- No bugs found.

### visual_user
- Prices in the cart are different from the prices on the inventory page for all items.
- The Checkout button is in the top right corner next to the cart badge instead of at the bottom of the page.
- The cart badge is out of place and overlaps the page layout (same as Session 02, also visible on the cart page).
- The menu icon lines are slanted (same as Session 02, also visible on the cart page).

## Questions
- Should checkout be possible with an empty cart? All users can go to checkout with no items.

## Ideas for test cases
- Prices in the cart are the same as on the inventory page.
- The cart badge updates correctly when items are removed in the cart.
- Items stay in the cart after logout and login.
- "Reset App State" removes all items and resets the cart badge.
- "Continue Shopping" and the Back button load the inventory page in an acceptable time.
- The Checkout button is at the bottom of the page next to "Continue Shopping".
- The cart badge is in the correct position.
- The menu icon lines are straight.
- Checkout with an empty cart (behaviour to be confirmed).