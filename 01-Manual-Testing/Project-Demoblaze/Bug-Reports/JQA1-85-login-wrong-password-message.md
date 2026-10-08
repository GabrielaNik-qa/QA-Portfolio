# JQA1-85: Incorrect error message on login with existing username and wrong password

| Field | Details |
|-------|---------|
| **Bug ID** | JQA1-85 |
| **Priority / Severity** | High / Minor |
| **Status** | To Do |
| **Label** | Login |
| **Reported** | 19 Apr 2026, Gabriela Nikolova |
| **Environment** | https://www.demoblaze.com/ , browser and OS: `Safari, Windows` |
| **Requirement** | FSD My Account, MA.LGN 1.2 (message for a wrong username or password). Test case MA_LGN_015 |

## Steps to Reproduce
1. Open https://www.demoblaze.com/
2. Click **Log in** in the main menu
3. Enter an existing username: `GabrielaNik`
4. Enter a wrong password: `Test123456789`
5. Click **Log in**

## Expected Result
A generic error message is shown: "Username or password is incorrect! Please try again!"

## Actual Result
The message "Wrong password." is shown.

## Notes
The actual message confirms that the username exists. A generic message for both a wrong username and a wrong password avoids this (user enumeration). The priority is High while the functional impact is a wording issue. Consider lowering it.