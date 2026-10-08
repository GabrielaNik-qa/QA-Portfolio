# Demoblaze - Requirements

**Source:** Functional specification "My Account" (FSD, Feb 2026). The document is not published here.

## What the specification covers

| Area | Requirement |
|------|-------------|
| **Login (MA.LGN)** | A user who is not logged in sees the "Log In" link, which opens a pop-up. Logged-in users do not see the link |
| | The pop-up has: title "Log in", a Username field, a Password field, an "X" button, a "Close" button and a "Log in" button |
| | Valid data: the user is logged in, returns to the home page and sees "Welcome, `<name>`" in the top right |
| | Both fields empty: an error message asks to fill in username and password |
| | Wrong or unknown username or password: an error message says the username or password is wrong |
| **Sign up (MA.RGR)** | The "Sign up" link opens a pop-up with: title "Sign up", Username, Password, "X", an informative text, "Close" and "Sign up" |
| | The pop-up closes with "X", "Close", or a click outside it |
| | Username and Password are mandatory |
| | Password: 8 to 64 characters, Latin letters only, at least one uppercase letter, one lowercase letter, one digit and one symbol |
| | Valid data: the account is created and a success message is shown |
| | Taken username: an error message says the account already exists |
| | Invalid password: an error message says the password is too weak |
| **Screen sizes** | The pop-ups work on XL, L, M and S screens |

## Messages used in the test cases

| Key | Message (as in the specification) | English meaning |
|-----|-----------------------------------|-----------------|
| MSG-1 | Моля попълнете Потребителско име и Парола | Please fill in Username and Password |
| MSG-2 | Потребителското име или парола е грешно! Моля, опитайте отново! | The username or password is wrong! Please try again! |
| MSG-3 | Вашият акаунт беше създаден успешно! Добре дошли! | Your account was created successfully! Welcome! |
| MSG-4 | Акаунт с това потребителско име вече съществува! | An account with this username already exists! |
| MSG-5 | Въведената парола е прекалено слаба! Паролата трябва да съдържа минимум 8 символа, главна буква, цифра и символ. Моля опитайте отново! | The entered password is too weak! It must contain at least 8 characters, an uppercase letter, a digit and a symbol. Please try again! |

## Gaps found in the specification

| # | Gap | Affected test cases |
|---|-----|---------------------|
| D1 | **No username rules**: no length, no allowed characters, no message. The tests assume 5-30 characters and Latin letters and digits only. The bug reports assume 5-256 | MA_RGR_020 to 031, 038, 039; bugs JQA1-83, JQA1-84 |
| D2 | The weak-password message does not mention lowercase, the 64-character limit or Latin-only, although the rules require them | MA_RGR_012 to 017, 034 to 037 |
| D3 | The empty-field message is defined only when **both** login fields are empty | MA_LGN_012, 013 |
| D4 | The sign up empty-field messages are not defined | MA_RGR_031, 032, 041 |
| D5 | Closing the login pop-up (X, Close, outside) is not described | MA_LGN_003, 004, 016, 017 |
| D6 | Spaces in a password are not mentioned | MA_RGR_035 |
| D7 | It is not stated whether usernames are case-sensitive | MA_RGR_040 |
| D8 | It is not stated whether the user is logged in automatically after signing up | MA_RGR_010 |
| D9 | Password masking is not mentioned | MA_LGN_018 |