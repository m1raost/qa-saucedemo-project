# Session 01 – Login

**Date:** 08.10.2026
**Duration:** 45 min
**Browser:** Chrome 154.0.8037.98
**Charter:** Explore the login page with all test users and invalid inputs to find errors.

## What I tried
- standard_user / secret_sauce – logged in, redirected to the inventory page.
- standard_user / 1234 – login rejected with the error "Epic sadface: 
Username and password do not match any user in this service".
- standard_user with an empty password – error "Epic sadface: Password is required".
- Empty username with secret_sauce – error "Epic sadface: Username is required".
- locked_out_user / secret_sauce – error "Epic sadface: Sorry, this user has been locked out."
- problem_user, performance_glitch_user, error_user and visual_user with secret_sauce -
- all logged in and redirected to the inventory page.
- Usernames in capital letters – login rejected with the "do not match" error.
- Space before or after the username – login rejected with the "do not match" error.
- Pressing Enter instead of clicking Login – works, redirected to the inventory page.
- Clicking X on the error message – the message closes and the red icons disappear.
- Opening /inventory.html directly without logging in – at first the page opened, 
but the earlier login session was still active. Retested in an Incognito window: 
redirected to the login page with the error "Epic sadface: You can only access '/inventory.html' when you are logged in."
- Browser Back button – at first it returned to the inventory page, but I had not logged out. 
Retested after logging out: no access to the inventory page.

## Bugs found
- The error message "Username and password do not match any user in this service" 
goes beyond the edge of the error box and is not fully readable.

## Questions
- Is secret_sauce the only valid password? All variations with capital letters or numbers are rejected.
- Should the username and password fields have a maximum length? Both accept unlimited characters.

## Ideas for test cases
- Valid login for all users
- Empty username with a valid password
- Empty password for each user
- Capital letters in username and password
- Numbers in the password
- Short and long passwords
- Spaces before and after the username
- Wrong symbol, e.g. "-" instead of "_"
- Direct URL access without login
- Back button after logout
