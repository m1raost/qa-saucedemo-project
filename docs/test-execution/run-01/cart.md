# Run 01 – Cart

**Date:** 10.11.2026
**Browser:** Chrome 157.0.8103.51
**OS:** macOS 14.8.9

### TC-CART-01: Prices in the cart match the inventory page
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – "Add to cart" does not work for some products, so their price in the cart cannot be checked (#3). Other products: Pass.
  - performance_glitch_user: Pass
  - error_user: Blocked – "Add to cart" does not work for some products, so their price in the cart cannot be checked (#3). Other products: Pass.
  - visual_user: Fail – prices in the cart are different from the prices on the inventory page (#9)
- **Bug:** #3, #9
- **Notes:** –


### TC-CART-02: Removing a product in the cart updates the cart badge
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – "Add to cart" does not work for some products, so their removal from the cart cannot be checked (#3). Other products: Pass.
  - performance_glitch_user: Pass
  - error_user: Blocked – "Add to cart" does not work for some products, so their removal from the cart cannot be checked (#3). Other products: Pass.
  - visual_user: Pass
- **Bug:** #3
- **Notes:** –


### TC-CART-03: Products stay in the cart after logout and login
- **Results:**
  - standard_user: Pass
  - problem_user: Blocked – "Add to cart" does not work for some products, so they cannot be checked after login (#3). Other products: Pass.
  - performance_glitch_user: Pass
  - error_user: Blocked – "Add to cart" does not work for some products, so they cannot be checked after login (#3). Other products: Pass.
  - visual_user: Pass
- **Bug:** #3
- **Notes:** –


### TC-CART-04: "Continue Shopping" loads the inventory page in under 3 seconds
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Fail – the inventory page takes more than 5 seconds to load (#14)
  - error_user: Pass
  - visual_user: Pass
- **Bug:** #14
- **Notes:** –


### TC-CART-05: Browser Back button loads the inventory page in under 3 seconds
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Fail – the inventory page takes more than 5 seconds to load (#14)
  - error_user: Pass
  - visual_user: Pass
- **Bug:** #14
- **Notes:** –


### TC-CART-06: Checkout button is at the bottom of the page
- **Results:**
  - standard_user: Pass
  - problem_user: Pass
  - performance_glitch_user: Pass
  - error_user: Pass
  - visual_user: Fail – the "Checkout" button is in the wrong position on the cart page (#16)
- **Bug:** #16
- **Notes:** –


### TC-CART-07: Checkout with an empty cart is not possible
- **Results:**
  - standard_user: Fail – checkout opens with an empty cart, no error message is shown (#17)
  - problem_user: Fail – checkout opens with an empty cart, no error message is shown (#17)
  - performance_glitch_user: Fail – checkout opens with an empty cart, no error message is shown (#17)
  - error_user: Fail – checkout opens with an empty cart, no error message is shown (#17)
  - visual_user: Fail – checkout opens with an empty cart, no error message is shown (#17)
- **Bug:** #17
- **Notes:** –


