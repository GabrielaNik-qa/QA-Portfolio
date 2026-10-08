# JQA1-83: Sign up succeeds with a Cyrillic username

| Field | Details |
|-------|---------|
| **Bug ID** | JQA1-83 |
| **Priority / Severity** | High / Major |
| **Status** | To Do |
| **Label** | Signup |
| **Reported** | 19 Apr 2026, Gabriela Nikolova |
| **Environment** | https://www.demoblaze.com/ , browser and OS: `Safari,Windows` |
| **Requirement** | ⚠️ The FSD does not define username rules. The expected result is an assumption. Test case MA_RGR_029 |

## Steps to Reproduce
1. Open https://www.demoblaze.com/
2. Click **Sign up** in the main menu
3. Enter an invalid username: `ГабриелаНик123`
4. Enter a valid password: `<password used>` *(not recorded in the original report, add it)*
5. Click **Sign up**

## Expected Result
An error message is shown: "Invalid username. Use 5-256 characters: Latin letters (a-z, A-Z) and digits (0-9). Spaces, special characters and Cyrillic are not allowed."

## Actual Result
The message "Sign up successful." is shown.
