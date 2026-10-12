# Session 05 – Menu

**Date:** 12.10.2026
**Duration:** 30 min
**Browser:** Chrome 155.0.8059.40
**Charter:** Explore the menu and footer with different users to find errors in navigation,
logout and resetting the app state.

## What I tried

### standard_user
- All Items returns to the inventory page from the product page, the cart and both checkout pages.
- Dynamic Catalog – Lazy Load loads the items in different sizes while scrolling.
- Dynamic Catalog – Spinner shows all items in a different visual layout.
- Dynamic Catalog – Slider shows one item at a time and moves to the next one in a loop.
- About opens https://saucelabs.com/.
- After logout, pressed Back and refreshed – redirected to the login page with the error
"Epic sadface: You can only access '/inventory.html' when you are logged in."
- Reset App State empties the cart badge.
- Footer: X opens https://x.com/saucelabs, Facebook opens https://www.facebook.com/saucelabs
and LinkedIn opens https://www.linkedin.com/company/sauce-labs/.
Each link opens in a new tab, so the Back button is not available there.
- Used as the reference for the other users.

### locked_out_user
- Blocked on the login page, the menu cannot be tested.

### problem_user, performance_glitch_user, error_user, visual_user
- Checked the same steps as with standard_user.

## Bugs found

### All users
- Reset App State empties the cart badge, but the products on the inventory page
still show the "Remove" button instead of "Add to cart".

### problem_user
- About opens a "404 - Page Not Found" page on saucelabs.com instead of the home page.
- The page offers "Go to homepage" and redirects to https://saucelabs.com/ automatically after 5 seconds.

### performance_glitch_user
- Navigation is slow, same as in Session 03. No new bugs found.

### error_user
- No bugs found.

### visual_user
- No bugs found.

## Questions
- Dynamic Catalog – Lazy Load repeats the same items again and again while scrolling and never finishes (all users).
- Is this endless loading expected?
- When Reset App State is used during checkout,
Finish still completes the order with the items that were reset (all users).
Should the order be completed, or should the user get an error?

## Ideas for test cases
- All Items returns to the inventory page from every page.
- Dynamic Catalog – Lazy Load, Spinner and Slider show all items correctly.
- About opens the Sauce Labs home page without an error.
- Logout returns to the login page from every page.
- After logout, protected pages cannot be opened with Back and refresh.
- Reset App State empties the cart badge and resets all product buttons to "Add to cart".
- Footer social media icons open the correct pages.