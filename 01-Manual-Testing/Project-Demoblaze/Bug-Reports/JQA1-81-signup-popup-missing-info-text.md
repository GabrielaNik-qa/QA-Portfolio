# JQA1-81: Sign-up pop-up is missing the informative text under the fields

| Field | Details |
|-------|---------|
| **Bug ID** | JQA1-81 |
| **Priority / Severity** | Low / Trivial |
| **Status** | To Do |
| **Label** | Signup |
| **Reported** | 19 Apr 2026, Gabriela Nikolova |
| **Environment** | https://www.demoblaze.com/ , browser and OS: `Safari,Windows` |
| **Requirement** | FSD My Account, MA.RGR 2.1 (Sign up pop-up elements). Test case MA_RGR_002 |

## Steps to Reproduce
1. Open https://www.demoblaze.com/
2. Click **Sign up** in the main menu
3. Check the modal for these elements:
   1. Static text "Sign up" at the top left
   2. Text field "Username"
   3. Text field "Password"
   4. "X" button at the top right
   5. Informative text under the text fields
   6. White "Close" button at the bottom right
   7. Blue button to the right of "Close"

## Expected Result
All listed elements are present.

## Actual Result
The informative text under the password field (element 5) is missing.