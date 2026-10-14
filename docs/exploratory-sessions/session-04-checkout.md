# Session 04 – Checkout

**Date:** 11.10.2026
**Duration:** 60 min
**Browser:** Chrome 155.0.8059.40
**Charter:** Explore the checkout process with different users to find
errors in the information form, price calculation and order completion.

## What I tried

### standard_user
- Submitted the empty form - error "Error: First Name is required".
- Left Last Name and Postal Code empty – error "Error: Last Name is required".
- Left Postal Code empty – error "Error: Postal Code is required".
- The Zip field accepts letters, and the First Name and Last Name fields accept numbers.
- All fields accept special characters and spaces only.
- On the overview page, the item total and tax are calculated correctly.
- Finish completes the order, the cart badge is emptied, and Back Home returns to the inventory page.
- Used as the reference for the other users.

### locked_out_user
- Blocked on the login page, the checkout cannot be tested.

### problem_user
- Tested the form with numbers, letters, long text, empty fields and spaces only.

### performance_glitch_user, error_user, visual_user
- Tested the form with numbers, letters, long text, empty fields and spaces only.
- Checked the item total and tax on the overview page – calculated correctly for all three users.
- Clicked Finish to complete the order.

### All users
- The Cancel button works on the Your Information and Overview pages.
- Checkout with an empty cart goes through to the "Thank you for your order!"
page for all users that can complete the checkout.
- Opened checkout-step-two.html directly by URL – works when logged in.
Without login, the page is not accessible.

## Bugs found

### problem_user
- Typing in the Last Name field enters single letters into the First Name field instead.
Because of this, the form cannot be completed, and the overview page could not be tested.

### performance_glitch_user
- No bugs found.

### error_user
- The Last Name field does not accept typing.
- When Last Name and Postal Code are empty, only "Error: Postal Code is required" is shown.
- There is no error for the empty Last Name.
- The form is accepted without a Last Name and goes to the overview page.
- The Finish button does not respond, the order is not completed and the cart badge is not emptied.

### visual_user
- No bugs found.

## Questions
- Should the Zip field accept letters? Should First Name and Last Name accept numbers? 
- Should the fields accept special characters?
- Should the fields accept spaces only? This works for all users, including standard_user.
- Should an order with an empty cart be completed with "Thank you for your order!",

## Ideas for test cases
- Every field shows its own error message when left empty.
- The form cannot be submitted when a required field is empty.
- Each field accepts typing and enters text only into itself.
- Form validation with numbers, letters, special characters, spaces only and long text 
  (expected behaviour to be confirmed).
- The item total equals the sum of the item prices, and the total equals item total + tax.
- The Finish button completes the order and empties the cart badge.
- Back Home returns to the inventory page.
- The Cancel button works on the Your Information and Overview pages.
- Checkout pages cannot be opened by URL without login.
- Checkout with an empty cart (expected behaviour to be confirmed).