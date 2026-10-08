# TS-DM-01: Login

| Field | Details |
|-------|---------|
| **Suite ID** | TS-DM-01 |
| **Component** | My Account, Login (MA.LGN) |
| **Priority** | High |
| **Type** | UI, Positive, Negative, Layout |
| **Documentation** | FSD "My Account", section 1 |

## Objective
Verify that the login pop-up opens, shows the right elements, logs a valid user in, and rejects invalid data with the right messages.

## Preconditions
A registered user exists (see the data dependencies in the [index](./README.md)).

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Source | Status |
|----|-----------|-------------------|-----------------|-----|--------|:------:|
| MA_LGN_001 | "Log In" opens the pop-up when the user is not logged in | 1. Open the site<br>2. Click "Log In" | Login pop-up is displayed | High | FSD 1.1 | ⬜ |
| MA_LGN_002 | Login pop-up has all required elements | 1. Open the site<br>2. Click "Log In" | Title "Log in", "X" button, Username label and field, Password label and field, "Close" button, "Log in" button | High | FSD 1.2 | ⬜ |
| MA_LGN_003 | "Close" closes the login pop-up | 1. Click "Log In"<br>2. Click "Close" | Pop-up is closed | High | ⚠️ Not in FSD | ⬜ |
| MA_LGN_004 | "X" closes the login pop-up | 1. Click "Log In"<br>2. Click "X" | Pop-up is closed | High | ⚠️ Not in FSD | ⬜ |
| MA_LGN_005 | Login pop-up displays correctly on XL screens | 1. Open the site on an XL screen<br>2. Click "Log In" | Pop-up is centered, all elements are visible, nothing overlaps, buttons are clickable | Medium | FSD 1.2 | ⬜ |
| MA_LGN_006 | Login pop-up displays correctly on L screens | Same as above on an L screen | Same as above | Medium | FSD 1.2 | ⬜ |
| MA_LGN_007 | Login pop-up displays correctly on M screens | Same as above on an M screen | Same as above | Medium | FSD 1.2 | ⬜ |
| MA_LGN_008 | Login pop-up displays correctly on S screens | Same as above on an S screen | Same as above | Medium | FSD 1.2 | ⬜ |
| MA_LGN_009 | Logged-in users do not see the "Log In" link | **Pre:** user is logged in<br>1. Check the menu | "Log In" link is not displayed | High | FSD 1.1 | ⬜ |
| MA_LGN_010 | Login succeeds with valid credentials | Username `validUsername`, Password `validPass1!`<br>1. Click "Log In"<br>2. Enter the data<br>3. Click "Log in" | User is redirected to the home page, "Welcome, `<name>`" is shown in the top right, and the "Log In" link is not displayed | High | FSD 1.2 (a) | ⬜ |
| MA_LGN_011 | Both fields empty are rejected | 1. Leave both fields empty<br>2. Click "Log in" | MSG-1 is shown and the user stays in the pop-up | High | FSD 1.2 (b) | ⬜ |
| MA_LGN_012 | Empty Username is rejected | Password `validPass1!`<br>1. Leave Username empty<br>2. Click "Log in" | MSG-1 is shown and the user stays in the pop-up | High | ⚠️ FSD defines MSG-1 only for both fields empty (D3) | ⬜ |
| MA_LGN_013 | Empty Password is rejected | Username `validUsername`<br>1. Leave Password empty<br>2. Click "Log in" | MSG-1 is shown and the user stays in the pop-up | High | ⚠️ FSD defines MSG-1 only for both fields empty (D3) | ⬜ |
| MA_LGN_014 | A non-existent Username is rejected | Username `nonExistentUser`, Password `validPass1!`<br>1. Click "Log in" | MSG-2 is shown and the user stays in the pop-up | High | FSD 1.2 (c) | ⬜ |
| MA_LGN_015 | An incorrect Password is rejected | Username `validUsername`, Password `incorrectPass`<br>1. Click "Log in" | MSG-2 is shown and the user stays in the pop-up | High | FSD 1.2 (c) | ⬜ |
| MA_LGN_016 | The user is not logged in when "Close" is clicked after entering valid data | Username `validUsername`, Password `validPass1!`<br>1. Enter the data<br>2. Click "Close" | Pop-up is closed and the user is not logged in | High | ⚠️ Not in FSD (D5) | ⬜ |
| MA_LGN_017 | *(added)* A click outside the login pop-up closes it | 1. Click "Log In"<br>2. Click outside the pop-up | Pop-up is closed, as for Sign up | Medium | ⚠️ Not in FSD (D5) | ⬜ |
| MA_LGN_018 | *(added)* The password is masked in both pop-ups | 1. Type a password in the login pop-up<br>2. Repeat in the Sign up pop-up | Characters are shown as dots or stars, not as text | Medium | ⚠️ Not in FSD (D9) | ⬜ |