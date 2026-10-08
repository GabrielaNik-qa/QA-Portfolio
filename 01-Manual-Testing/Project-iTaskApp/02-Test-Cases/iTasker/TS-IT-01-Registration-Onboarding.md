# TS-IT-01: Registration & Onboarding

| Field | Details |
|-------|---------|
| **Suite ID** | TS-IT-01 |
| **Role** | iTasker |
| **Priority** | High |
| **Type** | Functional, Negative, Boundary |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.2.1 and 2.2.2 |

## Objective
Verify that a user can register as an iTasker, sign in, and complete the 4-step business profile.

## Preconditions
- Application is reachable on the test environment
- Tester is logged out unless stated otherwise

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-IT-01.1 | Sign up as iTasker | 2.2.1 | 001-009 |
| SC-IT-01.2 | Sign in and first login | 2.2.2 | 010-012 |
| SC-IT-01.3 | Onboarding steps 1-4 | 2.2.2 | 013-020 |

---

## SC-IT-01.1 Sign up as iTasker

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-01-001 | "Become an iTasker" is available on the selection page | 1. Click "Create Account" | Selection page shows "Become an iTasker" | High | ⬜⬜⬜⬜ |
| TC-IT-01-002 | First name accepts 2-255 characters | `Jo` / `a` x 255 / `J` / `a` x 256  | 2 and 255 are accepted. 1 and 256 are rejected | High | ⬜⬜⬜⬜ |
| TC-IT-01-003 | Last name accepts 2-255 characters | `Li` / `a` x 255 / `L` / `a` x 256  | 2 and 255 are accepted. 1 and 256 are rejected | High | ⬜⬜⬜⬜ |
| TC-IT-01-004 | Email validates format, "@", real domain, 5-255 characters  | Valid: `{ITASKER_EMAIL}`<br>Invalid: `test`, `test@`, `test@com` | Valid email is accepted. Invalid formats are rejected | High | ⬜⬜⬜⬜ |
| TC-IT-01-005 | Phone requires "+1" prefix, max 15 digits | Valid: `{PHONE}`<br>Invalid: `234-567-8901` (no +1) | Valid number is accepted. Missing +1 is rejected | Med | ⬜⬜⬜⬜ |
| TC-IT-01-006 | "Main Service Category" dropdown is available and functional | 1. Open the dropdown<br>2. Select a category | List loads and the selection is saved in the field. It defines the main activity of the iTasker and the team | High | ⬜⬜⬜⬜ |
| TC-IT-01-007 | "Business Name" accepts text | 1. Enter `Test Services Ltd` | Text is accepted | Med | ⬜⬜⬜⬜ |
| TC-IT-01-008 | All fields are mandatory | Leave each field empty one at a time and submit | Form is not submitted and the empty field is flagged | High | ⬜⬜⬜⬜ |
| TC-IT-01-009 | Confirmation email with the password is sent | 1. Submit valid data<br>2. Check the inbox of `{ITASKER_EMAIL}`, also Spam and Promotions | An email with the user's password for the system arrives  | High | ⬜⬜⬜⬜ |

## SC-IT-01.2 Sign in and first login

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-01-010 | "Sign in" is available in the header | 1. Open the home page | Button is visible | High | ⬜⬜⬜⬜ |
| TC-IT-01-011 | After the first login the iTasker must complete the profile via Company - Profile - Edit | 1. Log in with a new iTasker account | The profile information steps are requested | High | ⬜⬜⬜⬜ |
| TC-IT-01-012 | On later logins the iTasker enters without filling the profile again | 1. Complete the profile<br>2. Log out and log in with email and password | Account opens directly. The profile fields are not requested again | Med | ⬜⬜⬜⬜ |

## SC-IT-01.3 Onboarding steps 1-4

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-01-013 | Step 1 "Basic Business Info" displays all 4 sections | 1. Open Step 1 | Sections: Fill in your info, Business Data, Business Address, Other | High | ⬜⬜⬜⬜ |
| TC-IT-01-014 | "Fill in your info" has First name, Last name, Email, Phone | Enter valid test values | All 4 fields are present and accept input | High | ⬜⬜⬜⬜ |
| TC-IT-01-015 | "Business Data" has Business name, Position, HST/GST Number, WSIB | `Test Services Ltd` / `Owner` / `123456789RT0001` | Fields are present. WSIB can stay empty | High | ⬜⬜⬜⬜ |
| TC-IT-01-016 | "Business Address" has Address, Street Name, Unit/Suite, Country, Province/State, City, ZIP Code | `123 Main St` / `ON` / `Toronto` / `M5V 3A8` | Fields are present. Unit/Suite can stay empty | High | ⬜⬜⬜⬜ |
| TC-IT-01-017 | "Other" has Website (optional) and "Where did you learn about iTask?" | Enter `www.example.com`, then leave both empty | Both fields are present and optional | Low | ⬜⬜⬜⬜ |
| TC-IT-01-018 | Step 2 "Insurance" displays the insurance fields | 1. Continue to Step 2 | Insurance fields are displayed | High | ⬜⬜⬜⬜ |
| TC-IT-01-019 | Step 3 "Direct Payments" redirects to Stripe and Stripe loads | 1. Continue to Step 3 | The Stripe page for payments and financial services loads correctly | High | ⬜⬜⬜⬜ |
| TC-IT-01-020 | Step 4 "My Professional References" has all fields | `John Smith` / `Former Employer` / `ABC Corp` / `john@example.com` / `+1-234-567-0000` / `Excellent professional` | Full name, Relationship, Company, Email, Phone number, Description are present and accept input | Med | ⬜⬜⬜⬜ |