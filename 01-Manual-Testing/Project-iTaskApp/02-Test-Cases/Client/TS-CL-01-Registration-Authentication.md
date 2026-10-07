# TS-CL-01: Registration & Authentication

| Field | Details |
|-------|---------|
| **Suite ID** | TS-CL-01 |
| **Role** | Client |
| **Priority** | High |
| **Type** | Functional, Negative, Boundary |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.1.1, 2.1.2, 2.1.6.4 |

## Objective
Verify that a Client can register, sign in, recover a password and log out, and that all input validation rules work.

## Preconditions
- Application is reachable on the test environment
- Tester is logged out unless stated otherwise

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-CL-01.1 | Sign up: navigation to the form | 2.1.1 | 001-003 |
| SC-CL-01.2 | Sign up: field validation | 2.1.1 | 004-009 |
| SC-CL-01.3 | Sign up: submission and confirmation email | 2.1.1 | 010-012 |
| SC-CL-01.4 | Sign in | 2.1.2 | 013-016 |
| SC-CL-01.5 | Forgot password | 2.1.2 | 017-019 |
| SC-CL-01.6 | Log out | 2.1.6.4 | 020 |

---

## SC-CL-01.1 Sign up: navigation to the form

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-01-001 | "Create Account" button is available on the home page | 1. Open the home page | "Create Account" button is visible and enabled | High | ⬜⬜⬜⬜ |
| TC-CL-01-002 | "Create Account" redirects to the selection page | 1. Click "Create Account" | Selection page opens with "Become a Client" and "Become an iTasker" | High | ⬜⬜⬜⬜ |
| TC-CL-01-003 | "Become a Client" displays the registration form | 1. Click "Create Account"<br>2. Click "Become a Client" | Form with first name, last name, email, phone and zip/postal code fields is displayed | High | ⬜⬜⬜⬜ |

## SC-CL-01.2 Sign up: field validation

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-01-004 | First name accepts 2-255 characters (BVA) | Open the form and enter:<br>- Min: `Ga` (2)<br>- Max: `a` x 255<br>- Invalid: `G` (1)<br>- Invalid: `a` x 256 *(added boundary)* | 2 and 255 characters are accepted. 1 and 256 characters are rejected with a validation message | High | ⬜⬜⬜⬜ |
| TC-CL-01-005 | Last name accepts 2-255 characters (BVA) | - Min: `Ni`<br>- Max: `a` x 255<br>- Invalid: `A`<br>- Invalid: `a` x 256 *(added boundary)* | 2 and 255 characters are accepted. 1 and 256 characters are rejected with a validation message | High | ⬜⬜⬜⬜ |
| TC-CL-01-006 | Email validates format, "@" symbol, real domain, 5-255 characters (EP) | - Valid: `{CLIENT_EMAIL}`<br>- Valid: an email in Cyrillic letters *(added, the story allows all supported languages)*<br>- Invalid: `test`, `test@`, `test@com` | Valid emails are accepted. Invalid formats are rejected with a validation message | High | ⬜⬜⬜⬜ |
| TC-CL-01-007 | Phone requires "+1" prefix, max 15 digits (BVA) | - Valid: `+1-234-567-8901` (11 digits)<br>- Valid boundary: 15 digits<br>- Invalid: 16 digits<br>- Invalid: `234-567-8901` (no +1)<br>⚠️ Confirm whether the "1" counts toward the 15 (open question 2) | Valid values are accepted. 16 digits and a missing +1 are rejected | Med | ⬜⬜⬜⬜ |
| TC-CL-01-008 | Zip/Postal code shows dropdown suggestions while typing | 1. Start typing a zip/postal code<br>2. Select a suggestion<br>*On mobile, check rendering on a small screen* | Suggestions appear while typing. Selecting one fills the field. Dropdown renders correctly on mobile | Med | ⬜⬜⬜⬜ |
| TC-CL-01-009 | All fields are mandatory | 1. Fill all fields except one<br>2. Click "Create Account"<br>3. Repeat, leaving a different field empty each time | Form is not submitted. A message points to the empty field (checked for every field) | High | ⬜⬜⬜⬜ |

## SC-CL-01.3 Sign up: submission and confirmation email

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-01-010 | "Create Account" submits the form when all fields are valid | First name: `Anna`, Last name: `Client`, Email: `{CLIENT_EMAIL}`, Phone: `{PHONE}`, valid zip<br>1. Fill the form<br>2. Click "Create Account" | Account is created and the user gets a success confirmation or is redirected. No further action is needed from the Client | High | ⬜⬜⬜⬜ |
| TC-CL-01-011 | Confirmation email with login credentials is sent | **Pre:** TC-CL-01-010 passed<br>1. Check the inbox of `{CLIENT_EMAIL}` | Email with the email address and password for the system arrives *(by design per the story, see open question 4)* | High | ⬜⬜⬜⬜ |
| TC-CL-01-012 | Confirmation email is displayed as in the user story | 1. Open the email from TC-CL-01-011<br>2. Compare it with the design in the document | Layout, text, logo and links match the design | Med | ⬜⬜⬜⬜ |

## SC-CL-01.4 Sign in

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-01-013 | "Sign in" button is available in the header | 1. Open the home page | "Sign in" button is visible in the header menu | High | ⬜⬜⬜⬜ |
| TC-CL-01-014 | Email field accepts min 5 characters and requires "@" | - Valid: `{CLIENT_EMAIL}`<br>- Invalid: `ab@c` (4 chars)<br>- Invalid: `testgmail.com` (no @) | Valid email is accepted. Invalid inputs show a validation message | High | ⬜⬜⬜⬜ |
| TC-CL-01-015 | Password requires min 8 characters (BVA) | - Valid: `Test1234` (8)<br>- Invalid: `Test12` (6)<br>- Invalid: 7 characters *(added boundary)* | 8 characters are accepted. Fewer than 8 are rejected | High | ⬜⬜⬜⬜ |
| TC-CL-01-016 | "Continue" logs in and redirects to the Dashboard | 1. Enter `{CLIENT_EMAIL}` and the valid password<br>2. Click "Continue" | User is logged in and the Dashboard is displayed | High | ⬜⬜⬜⬜ |

## SC-CL-01.5 Forgot password

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-01-017 | "Forgot Password" link is available on the sign-in page | 1. Open the sign-in page | Link is visible and clickable | Med | ⬜⬜⬜⬜ |
| TC-CL-01-018 | "Forgot Password" form contains an email input field | 1. Click "Forgot Password"<br>2. Enter `{CLIENT_EMAIL}` | Form opens with an email field that accepts input | Med | ⬜⬜⬜⬜ |
| TC-CL-01-019 | Password reset confirmation message is displayed | 1. Submit the form with `{CLIENT_EMAIL}`<br>2. Check the inbox | A message says that password recovery instructions were sent to the email, and the email arrives | High | ⬜⬜⬜⬜ |

## SC-CL-01.6 Log out

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-01-020 | "Log out" ends the session and redirects to the Home page | **Pre:** logged in<br>1. Open the username dropdown<br>2. Click "Log out"<br>3. Click the browser Back button *(added check)* | User is redirected to the Home page without a logged-in profile. Back does not restore the session | High | ⬜⬜⬜⬜ |