# JQA1-84: Sign up succeeds with spaces in username and password

| Field | Details |
|-------|---------|
| **Bug ID** | JQA1-84 |
| **Priority / Severity** | Highest / Major |
| **Status** | To Do |
| **Label** | Signup |
| **Reported** | 19 Apr 2026, Gabriela Nikolova |
| **Environment** | https://www.demoblaze.com/ , browser and OS: `Safari,Windows` |
| **Requirement** | FSD MA.RGR 2.1 for the password. Test case MA_RGR_026, MA_RGR_035 |

## Steps to Reproduce
1. Open https://www.demoblaze.com/
2. Click **Sign up** in the main menu
3. Enter an invalid username containing a space: `Gabi Nik`
4. Enter an invalid password containing a space: `Test 1`
5. Click **Sign up**

## Expected Result
Two error messages are shown:
- "The password is too weak! The password must contain at least 8 characters, an uppercase letter, a digit and a symbol. Please try again!"
- "Invalid username. Use 5-256 characters: Latin letters (a-z, A-Z) and digits (0-9). Spaces, special characters and Cyrillic are not allowed."

## Actual Result
The message "Sign up successful." is shown.

## Notes
This report covers two defects (username and password validation). Consider splitting it into two reports, one defect per ticket.