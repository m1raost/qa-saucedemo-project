# Test Plan – Sauce Demo

## 1. Introduction
Testing the e-commerce demo website https://www.saucedemo.com for QA practice.
The goal is to build a complete project from manual testing to test automation:
exploratory testing, assumed requirements, test cases, bug reports, test reports and a CI/CD pipeline.

## 2. Scope
### In scope
- Login
- Inventory and product pages
- Cart
- Checkout
- Menu
- Footer links


### Out of scope
- **External websites** (saucelabs.com, X, Facebook, LinkedIn) – owned by third parties.
  Only checked that the links open the correct page.
- **Performance and load testing** – the application is owned by a third party,
  and load testing it without permission is not allowed. Slow loading is only reported as an observation.
- **Security testing** – no permission to test a third-party application for security issues.
- **Backend / API** – the application runs in the browser and has no accessible backend API.
  API testing is done in a separate project.
- **Mobile devices** – testing is done on desktop browsers only.

## 3. Assumed Requirements

### General
- **AR-GEN-01:** The cart badge shows the correct number of items in the cart.
An empty cart shows no number on the badge.
- **AR-GEN-02:** The cart badge is in the correct position on every page, for every user.
- **AR-GEN-03:** The menu icon lines are straight on every page, for every user.
- **AR-GEN-04:** The user is not logged out unexpectedly while using the application.

### Login
- **AR-LOGIN-01:** A user with valid credentials is logged in and redirected to the inventory page.
- **AR-LOGIN-02:** A locked-out user cannot log in and sees an error message.
- **AR-LOGIN-03:** Username and password are case-sensitive.
- **AR-LOGIN-04:** An empty form is not accepted and an error message is shown.
- **AR-LOGIN-05:** An empty username with a valid password is not accepted and an error message is shown.
- **AR-LOGIN-06:** A valid username with an empty password is not accepted and an error message is shown.
- **AR-LOGIN-07:** Pressing Enter instead of clicking Login submits the form.
- **AR-LOGIN-08:** Clicking X on the error message closes the message and removes the red icons.
- **AR-LOGIN-09:** The error message stays inside its container and is fully readable.
- **AR-LOGIN-10:** A username with spaces before or after it is not accepted (assumption).
- **AR-LOGIN-11:** Username and password fields accept a maximum of 50 characters (assumption).
- **AR-LOGIN-12:** The inventory page cannot be opened by URL without login, or with the Back button after logout.

### Inventory
- **AR-INV-01:** The image, name, price and description of a product are the same
 on the inventory page and the product page.
- **AR-INV-02:** Every product has a description.
- **AR-INV-03:** Every product shows its own correct image on the inventory page.
- **AR-INV-04:** Prices stay the same after reload or Back/Forward navigation.
- **AR-INV-05:** Every product opens its own page, with no "ITEM NOT FOUND".
- **AR-INV-06:** A product that is not found cannot be added to the cart.
- **AR-INV-07:** Adding and removing works for every product.
- **AR-INV-08:** Sorting A–Z, Z–A, price low to high and price high to low works correctly, with no error message.
- **AR-INV-09:** The inventory page loads in under 3 seconds after login, Back navigation and sorting (assumption).
- **AR-INV-10:** The Remove button stays inside its boundaries.

### Cart
- **AR-CART-01:** Prices in the cart are the same as on the inventory page.
- **AR-CART-02:** Removing an item in the cart updates the cart badge.
- **AR-CART-03:** Items stay in the cart after logout and login.
- **AR-CART-04:** "Continue Shopping" and the Back button load the inventory page in under 3 seconds (assumption).
- **AR-CART-05:** The Checkout button is at the bottom of the page, next to "Continue Shopping".
- **AR-CART-06:** Checkout with an empty cart is not possible and an error message is shown (assumption).

### Checkout
- **AR-CHK-01:** Every field shows its own error message when left empty.
- **AR-CHK-02:** The form cannot be submitted when a required field is empty.
- **AR-CHK-03:** Each field accepts typing and enters text only into itself.
- **AR-CHK-04:** First Name and Last Name do not accept numbers or special characters (assumption).
- **AR-CHK-05:** Postal Code accepts letters and numbers (assumption).
- **AR-CHK-06:** A field with spaces only is treated as empty (assumption).
- **AR-CHK-07:** The item total equals the sum of the item prices, and the total equals item total + tax.
- **AR-CHK-08:** The Finish button completes the order and empties the cart badge.
- **AR-CHK-09:** Back Home returns to the inventory page.
- **AR-CHK-10:** The Cancel button works on the Your Information and Overview pages.
- **AR-CHK-11:** Checkout pages cannot be opened by URL without login.

### Menu
- **AR-MENU-01:** All Items returns to the inventory page from every page.
- **AR-MENU-02:** Dynamic Catalog – Lazy Load, Spinner and Slider show all items correctly.
- **AR-MENU-03:** Dynamic Catalog – Lazy Load shows each item only once and stops after the last item (assumption).
- **AR-MENU-04:** About opens the Sauce Labs home page without an error.
- **AR-MENU-05:** Logout returns to the login page from every page.
- **AR-MENU-06:** Reset App State removes all items,
  empties the cart badge and resets all product buttons to "Add to cart".
- **AR-MENU-07:** When Reset App State is used during checkout,
  the order cannot be completed with the removed items (assumption).
- **AR-MENU-08:** The footer social media icons open the correct pages.



## 4. Test Approach

### Testing process
1. **Exploratory testing** – five timeboxed sessions (login, inventory, cart, checkout, menu)
  to learn the application and define the assumed requirements.
2. **Manual test cases** – written from the assumed requirements and executed manually.
3. **Bug reporting** – every failed test case is reported as a GitHub Issue.
4. **Test automation** – high-priority test cases are automated with Java, Selenium and TestNG.

### Test types
- Functional testing – features work as expected.
- Negative testing – invalid input and wrong actions are handled correctly.
- UI testing – layout, images and text are displayed correctly.
- Regression testing – the automated test suite is run regularly (e.g. in a CI/CD pipeline)
  to detect changes in the application or the browser.

### Test design techniques
- **Equivalence partitioning** – valid and invalid input groups (e.g. valid and invalid usernames).
- **Boundary value analysis** – short and long input values.
- **Error guessing** – based on experience from the exploratory sessions.
- **Comparison with a reference user** – standard_user is used as the expected behaviour for the other users.

### Prioritisation
Test cases get a priority (High, Medium, Low) based on risk. Login, adding to cart and checkout are High priority,
because users cannot buy anything if they fail.

## 5. Test Environment

- **Application:** https://www.saucedemo.com
- **Operating system:** macOS 14.8.9
- **Manual testing:** Google Chrome 155.0.8059.40
- **Automated testing:** Google Chrome, Mozilla Firefox, Microsoft Edge (latest versions)
- **Screen:** desktop, browser window maximised

The browser version is recorded in every exploratory session and test run, because browsers update automatically.

## 6. Test Data

### Test users are
- standard_user – normal user, used as the reference
- locked_out_user – blocked user, for login error tests
- problem_user – user with broken images, product pages and checkout form
- performance_glitch_user – user with slow page loading
- error_user – user with errors when adding/removing items and in checkout
- visual_user – user with layout and price display issues

### Password for all users
secret_sauce

### Checkout form – valid data
- First Name: John
- Last Name: Smith
- Postal Code: 10115

### Checkout form – invalid and edge data
- Empty fields(each separately and all fields).
- Spaces only
- Numbers in First Name and Last Name, e.g. "John123"
- Letters in Postal Code, e.g. "ABC12"
- Special characters, e.g. "@#$%"
- Long text, e.g. 100+ characters

## 7. Entry and Exit Criteria

### Entry criteria
- The application https://www.saucedemo.com is available.
- All test users can be used (password secret_sauce).
- The test plan is written.
- Test cases are written and linked to the assumed requirements.
- Chrome is installed for manual testing; Chrome, Firefox and Edge for automated testing.

### Exit criteria
- All high-priority test cases have been executed.
- At least 90% of all test cases have been executed.
- Every failed test case has a bug report.
- All in-scope areas (login, inventory, cart, checkout, menu, footer links) have been tested.
- Test results are documented.

## 8. Risks

- **No official requirements.** The expected behaviour is based on assumptions, which may be wrong.
  Mitigation: assumptions are marked as (assumption) and listed as open questions.

- **The application is owned by a third party.** saucedemo.com can change or be unavailable at any time.
  Mitigation: the Chrome version and test date are recorded; results are valid for that date.

- **Browser updates.** Chrome updates automatically, which can change behaviour between test runs.
  Mitigation: the browser version is recorded in every session and test run.

- **Blocking defects.** Some bugs stop testing of later steps 
  (e.g. problem_user cannot complete the checkout form, so the overview page cannot be tested).
  Mitigation: the blocked steps are tested with other users and noted as not testable.

- **Slow responses.** performance_glitch_user has long loading times, 
  which can make tests slow or unstable, especially in automation.
  Mitigation: use explicit waits in automation, no fixed waiting times.

- **One tester.** All testing is done by one person, so some issues may be missed.
  Mitigation: exploratory sessions with every user and a structured set of test cases.


## 9. Deliverables

- Mind map of the application – docs/mind-map.png
- Exploratory session notes – docs/exploratory-sessions/
- Test plan – docs/test-plan.md
- Test cases – docs/test-cases/
- Bug reports – GitHub Issues
- UI automation framework (Java, Selenium, TestNG, Maven) – src/
- Test execution reports (Allure)
- README with project overview and instructions on how to run the tests