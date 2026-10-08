# TS-DM-02: Sign up

| Field | Details |
|-------|---------|
| **Suite ID** | TS-DM-02 |
| **Component** | My Account, Create an Account (MA.RGR) |
| **Priority** | High |
| **Type** | UI, Positive, Negative, Boundary, Layout |
| **Documentation** | FSD "My Account", section 2 |

## Objective
Verify that the Sign up pop-up opens and closes correctly, shows the right elements, creates an account with valid data, and rejects invalid usernames and passwords with the right messages.

## Preconditions
The user is not logged in. See the data dependencies in the [index](./README.md).

## Pop-up behaviour

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Source | Status |
|----|-----------|-------------------|-----------------|-----|--------|:------:|
| MA_RGR_001 | "Sign up" opens the pop-up | 1. Open the site<br>2. Click "Sign up" | Sign up pop-up is displayed | High | FSD 2.1 | ⬜ |
| MA_RGR_002 | Sign up pop-up has all required elements | 1. Click "Sign up" | Title "Sign up", "X" button, Username label and field, Password label and field, informative text, "Close" button, "Sign up" button | High | FSD 2.1 | ⬜ |
| MA_RGR_003 | Pop-up displays correctly on XL screens | 1. Open the site on an XL screen<br>2. Click "Sign up" | Pop-up is centered, all elements are visible, nothing overlaps, buttons are clickable | Medium | FSD 2.1 | ⬜ |
| MA_RGR_004 | Pop-up displays correctly on L screens | Same as above on an L screen | Same as above | Medium | FSD 2.1 | ⬜ |
| MA_RGR_005 | Pop-up displays correctly on M screens | Same as above on an M screen | Same as above | Medium | FSD 2.1 | ⬜ |
| MA_RGR_006 | Pop-up displays correctly on S screens | Same as above on an S screen | Same as above | Medium | FSD 2.1 | ⬜ |
| MA_RGR_007 | "X" closes the pop-up | 1. Click "Sign up"<br>2. Click "X" | Pop-up is closed and the home page is displayed | Medium | FSD 2.1 | ⬜ |
| MA_RGR_008 | "Close" closes the pop-up | 1. Click "Sign up"<br>2. Click "Close" | Pop-up is closed and the home page is displayed | Medium | FSD 2.1 | ⬜ |
| MA_RGR_009 | A click outside closes the pop-up | 1. Click "Sign up"<br>2. Click outside it | Pop-up is closed and the home page is displayed | Medium | FSD 2.1 | ⬜ |

## Account creation and password rules

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Source | Status |
|----|-----------|-------------------|-----------------|-----|--------|:------:|
| MA_RGR_010 | Account is created with valid data | Username `validUsername`, Password `validPass1!`<br>1. Enter the data<br>2. Click "Sign up" | Account is created and MSG-3 is shown | High | FSD 2.1 (D8) | ⬜ |
| MA_RGR_011 | An existing username is rejected | **Pre:** `validUsername` exists<br>Username `validUsername`, Password `validPass1!`<br>1. Click "Sign up" | MSG-4 is shown and the user stays in the pop-up | High | FSD 2.1 | ⬜ |
| MA_RGR_012 | A password shorter than 8 characters is rejected | Password `p@sS12` (6) | MSG-5 is shown and the user stays in the pop-up | High | FSD 2.1 | ⬜ |
| MA_RGR_013 | A password without an uppercase letter is rejected | Username `validUsername2`, Password `password1!` | MSG-5 is shown and the user stays in the pop-up | High | FSD 2.1 | ⬜ |
| MA_RGR_014 | A password without a lowercase letter is rejected | Username `validUsername2`, Password `PASSWORD1!` | MSG-5 is shown and the user stays in the pop-up (the message does not mention lowercase, D2) | High | FSD 2.1 | ⬜ |
| MA_RGR_015 | A password without a digit is rejected | Username `validUsername2`, Password `Password!!` | MSG-5 is shown and the user stays in the pop-up | High | FSD 2.1 | ⬜ |
| MA_RGR_016 | A password without a symbol is rejected | Username `validUsername2`, Password `Password11` | MSG-5 is shown and the user stays in the pop-up | High | FSD 2.1 | ⬜ |
| MA_RGR_017 | A password longer than 64 characters is rejected | Username `validUsername2`, Password of 71 characters: `StrongTestPassword1!StrongTestPassword2@StrongTestPassword3#ExtraPart4$` | MSG-5 is shown and the user stays in the pop-up | High | FSD 2.1 | ⬜ |
| MA_RGR_018 | A password of exactly 8 characters is accepted | Username `validUsername1`, Password `P@ssw0rd` | Account is created and MSG-3 is shown | High | FSD 2.1 | ⬜ |
| MA_RGR_019 | A password of exactly 64 characters is accepted | Username `validUsername2`, Password `StrongTestPassword1!StrongTestPassword2@StrongTestPassword3Extra` | Account is created and MSG-3 is shown | High | FSD 2.1 | ⬜ |
| MA_RGR_034 | *(added)* A password with Cyrillic letters is rejected (bug JQA1-82) | Username `validUsername4`, Password `Тест123@` | MSG-5 is shown and no account is created. Only Latin letters are supported | High | FSD 2.1 | ⬜ |
| MA_RGR_035 | *(added)* A password with spaces is rejected (bug JQA1-84) | Username `validUsername5`<br>1. Password `Test 1` (too short anyway)<br>2. Password `Test 1234!` | MSG-5 is shown for both and no account is created<br>⚠️ Spaces are not mentioned in the FSD for the second value (D6) | High | FSD 2.1 (D6) | ⬜ |
| MA_RGR_036 | *(added)* A password of 7 characters is rejected (boundary) | Username `validUsername6`, Password `P@ssw0r` | MSG-5 is shown and the user stays in the pop-up | High | FSD 2.1 | ⬜ |
| MA_RGR_037 | *(added)* A password of 65 characters is rejected (boundary) | Username `validUsername7`, Password `StrongTestPassword1!StrongTestPassword2@StrongTestPassword3ExtraA` | MSG-5 is shown and the user stays in the pop-up | High | FSD 2.1 | ⬜ |

## Username rules (assumptions, see gap D1)

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Source | Status |
|----|-----------|-------------------|-----------------|-----|--------|:------:|
| MA_RGR_020 | A username of exactly 5 characters is accepted | Username `User1`, Password `validPassword1!` | Account is created and MSG-3 is shown | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_021 | A username of exactly 30 characters is accepted | Username `UserName1234567890123456789012` | Account is created and MSG-3 is shown | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_022 | A lowercase Latin username is accepted | Username `username` | Account is created and MSG-3 is shown | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_023 | An uppercase Latin username is accepted | Username `USERNAME` | Account is created and MSG-3 is shown | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_024 | A username with letters and digits is accepted | Username `user1234` | Account is created and MSG-3 is shown | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_025 | A username with special characters is rejected | Username `user#1234` | An error message is shown (text not defined) | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_026 | A username with spaces between characters is rejected (bug JQA1-84) | Username `user 1234` | An error message is shown (text not defined) | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_027 | A username with a leading space is rejected | Username ` user1234` | An error message is shown (text not defined) | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_028 | A username with a trailing space is rejected | Username `user1234 ` | An error message is shown (text not defined) | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_029 | A username with Cyrillic characters is rejected (bug JQA1-83) | Username `потребител1` | An error message is shown (text not defined) | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_030 | A username with non-ASCII characters is rejected | Username `Userñ123` | An error message is shown (text not defined) | High | ⚠️ Not in FSD | ⬜ |
| MA_RGR_038 | *(added)* A username of 4 characters is rejected (boundary) | Username `Usr1`, Password `validPassword1!` | An error message is shown | High | ⚠️ Not in FSD (D1) | ⬜ |
| MA_RGR_039 | *(added)* A username of 31 characters is rejected (boundary) | Username `UserName12345678901234567890123` | An error message is shown | High | ⚠️ Not in FSD (D1) | ⬜ |
| MA_RGR_040 | *(added)* The same username in a different case | **Pre:** `Username2` exists<br>1. Sign up with `username2` | ⚠️ Not defined (D7). Record the behaviour and raise it with the product owner | Medium | ⚠️ Not in FSD (D7) | ⬜ |

## Mandatory fields and closing

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Source | Status |
|----|-----------|-------------------|-----------------|-----|--------|:------:|
| MA_RGR_031 | An empty Username is rejected | Password `validPassword1!`<br>1. Leave Username empty<br>2. Click "Sign up" | An error message is shown (text not defined) | High | FSD 2.1 (D4) | ⬜ |
| MA_RGR_032 | An empty Password is rejected | Username `validUsername3`<br>1. Leave Password empty<br>2. Click "Sign up" | An error message is shown (text not defined) | High | FSD 2.1 (D4) | ⬜ |
| MA_RGR_041 | *(added)* Both fields empty are rejected | 1. Leave both fields empty<br>2. Click "Sign up" | An error message is shown and no account is created (text not defined) | High | FSD 2.1 (D4) | ⬜ |
| MA_RGR_033 | No account is created when "Close" is clicked after entering valid data | Username `validUsername3`, Password `validPass1!`<br>1. Enter the data<br>2. Click "Close" | Pop-up is closed and no account is created | High | ⚠️ Not in FSD | ⬜ |