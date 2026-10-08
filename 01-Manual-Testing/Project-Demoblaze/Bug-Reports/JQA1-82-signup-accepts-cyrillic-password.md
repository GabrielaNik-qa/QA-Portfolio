# JQA1-82: Sign up succeeds with a password containing Cyrillic characters

| Field | Details |
|-------|---------|
| **Bug ID** | JQA1-82 |
| **Priority / Severity** | High / Major |
| **Status** | To Do |
| **Label** | Signup |
| **Reported** | 19 Apr 2026, Gabriela Nikolova |
| **Environment** | https://www.demoblaze.com/ , browser and OS: `Safari,Windows` |
| **Requirement** | FSD My Account, MA.RGR 2.1 (password rules, Latin letters only). Test case MA_RGR_034 |

## Steps to Reproduce
1. Open https://www.demoblaze.com/
2. Click **Sign up** in the main menu
3. Enter an unused valid username: `GabrielaNiktest123`
4. Enter a password containing Cyrillic letters: `Тест123@`
5. Click **Sign up**

## Expected Result
An error message is shown: "The password is too weak! The password must contain at least 8 characters, an uppercase letter, a digit and a symbol. Please try again!"

## Actual Result
The message "Sign up successful." is shown and the account is created.

## Notes
The test password has 8 characters, an uppercase letter, a digit and a symbol. The rule it breaks is the **Latin-only** requirement, so the expected message should mention allowed characters.
