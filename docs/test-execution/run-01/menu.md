# Run 01 – Menu

**Date:** 17.–18.11.2026
**Browser:** Chrome 157.0.8103.79
**OS:** macOS 14.8.9

### TC-MENU-01: "All Items" returns to the inventory page from every page
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name, so Checkout: Overview and Complete cannot be reached (#4). Other pages: Pass.
  - performance_glitch_user: Pass
  - error_user: Blocked – "Finish" button does not respond, so Checkout: Complete! cannot be reached (#21). Other pages: Pass.
  - visual_user: Pass
- **Bug:** #4, #21
- **Notes:** –


### TC-MENU-02: Dynamic Catalog – Lazy Load shows all products correctly
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-MENU-03: Dynamic Catalog – Spinner shows all products correctly
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-MENU-04: Dynamic Catalog – Slider shows all products correctly
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-MENU-05: Dynamic Catalog – Lazy Load shows each product only once
- **Results:**
  - standard_user: Fail – Lazy Load repeats products and never stops loading (#24)
  - problem_user: Fail – Lazy Load repeats products and never stops loading (#24)
  - performance_glitch_user: Fail – Lazy Load repeats products and never stops loading (#24)
  - error_user: Fail – Lazy Load repeats products and never stops loading (#24)
  - visual_user: Fail – Lazy Load repeats products and never stops loading (#24)
- **Bug:** #24
- **Notes:** –


### TC-MENU-06: "About" opens the Sauce Labs home page
- **Results:**
  - standard_user: Pass
  - problem_user: Fail – "About" opens a "Page Not Found" page (#25)
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** #25
- **Notes:** –


### TC-MENU-07: Logout returns to the login page from every page
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name, so Checkout: Overview and Complete cannot be reached (#4). Other pages: Pass.
  - performance_glitch_user: Pass
  - error_user: Blocked – "Finish" button does not respond, so Checkout: Complete! cannot be reached (#21). Other pages: Pass.
  - visual_user: Pass
- **Bug:** #4, #21
- **Notes:** –


### TC-MENU-08: Reset App State empties the cart and resets the product buttons
- **Results:**
  - standard_user: Fail – "Reset App State" does not reset the product buttons (#26)
  - problem_user: Fail – "Reset App State" does not reset the product buttons (#26). Products that cannot be added were not checked (#3).
  - performance_glitch_user: Fail – "Reset App State" does not reset the product buttons (#26)
  - error_user: Fail – "Reset App State" does not reset the product buttons (#26). Products that cannot be added were not checked (#3).
  - visual_user: Fail – "Reset App State" does not reset the product buttons (#26)
- **Bug:** #3, #26
- **Notes:** –


### TC-MENU-09: Order cannot be completed after Reset App State during checkout
- **Results:**
  - standard_user: Fail – the order can be completed after "Reset App State" during checkout (#27)
  - problem_user: Blocked – typing in Last Name enters text into First Name, so Checkout: Overview cannot be reached (#4)
  - performance_glitch_user: Fail – the order can be completed after "Reset App State" during checkout (#27)
  - error_user: Blocked – "Finish" button does not respond (#21)
  - visual_user: Fail – the order can be completed after "Reset App State" during checkout (#27)
- **Bug:** #4, #21, #27
- **Notes:** –


### TC-MENU-10: Footer social media icons open the correct pages
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Pass
- **Bug:** –
- **Notes:** –


### TC-MENU-11: Menu opens with the menu icon and closes with X on every page
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – typing in Last Name enters text into First Name, so Checkout: Overview and Complete cannot be reached (#4). Other pages: Pass.
  - performance_glitch_user: Pass
  - error_user: Blocked – "Finish" button does not respond, so Checkout: Complete! cannot be reached (#21). Other pages: Pass.
  - visual_user: Pass
- **Bug:** #4, #21
- **Notes:** –
