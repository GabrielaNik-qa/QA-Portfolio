# TS-CL-04: Profile & Notification Preferences

| Field | Details |
|-------|---------|
| **Suite ID** | TS-CL-04 |
| **Role** | Client |
| **Priority** | Medium |
| **Type** | Functional, UI, State-based |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.1.6, 2.1.6.1, 2.1.6.2 |

## Objective
Verify that a Client can edit personal data, change the password, and configure notification preferences.

## Preconditions
- Client is logged in

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-CL-04.1 | Edit profile | 2.1.6.1 | 001-007 |
| SC-CL-04.2 | Notification preferences | 2.1.6.2 | 008-016 |

---

## SC-CL-04.1 Edit profile

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-04-001 | Username dropdown shows Profile, Preferences, Log out | 1. Click the username in the header | Dropdown shows all 3 options | High | ⬜⬜⬜⬜ |
| TC-CL-04-002 | First name, Last name, Email and Phone are editable | 1. Open Profile<br>2. Change first and last name (for example `Anna` to `Maria`) | Fields accept the new values | High | ⬜⬜⬜⬜ |
| TC-CL-04-003 | "Save changes" saves personal info | 1. Edit fields<br>2. Click "Save changes"<br>3. Log out, log in, reopen Profile | New values are persisted | High | ⬜⬜⬜⬜ |
| TC-CL-04-004 | New password, New password again and Current password fields are available | 1. Scroll to the password section | All 3 fields are displayed | Med | ⬜⬜⬜⬜ |
| TC-CL-04-005 | "Save password" saves the password change | 1. Fill in the 3 fields with valid values<br>2. Click "Save password"<br>3. Log out and log in with the new password | Password changes. The new password works and the old one is rejected | High | ⬜⬜⬜⬜ |
| TC-CL-04-006 | Address and Zip/Postal code are editable | 1. Edit both fields<br>2. Save | Values are accepted and saved | Med | ⬜⬜⬜⬜ |
| TC-CL-04-007 | Edit Profile window meets the visual requirements | 1. Compare the window with the user story | Layout and elements match | Low | ⬜⬜⬜⬜ |

## SC-CL-04.2 Notification preferences 

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-04-008 | "Preferences" opens the Notification preferences window | 1. Click "Preferences" in the dropdown | Notification preferences window opens | High | ⬜⬜⬜⬜ |
| TC-CL-04-009 | Notifications window meets the visual requirements | 1. Compare the window with the user story | Layout and elements match | Low | ⬜⬜⬜⬜ |
| TC-CL-04-010 | "Chat messages receiving" has Email, Push, Push-Alert Sound toggles | 1. Toggle each ON and OFF<br>2. Save and reopen | All 3 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-CL-04-011 | "Task Suggestion" has Push and Push-Alert Sound toggles | Same as above | Both toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-CL-04-012 | "Task appointment change" has Email, Push, Push-Alert Sound toggles | Same as above | All 3 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-CL-04-013 | "Task status changed" has Push, Push-Alert Sound, SMS toggles | Same as above | All 3 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-CL-04-014 | "New follow up Task" has Push and Push-Alert Sound toggles | Same as above | Both toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-CL-04-015 | "Finances" has Email, Push, Push-Alert Sound toggles | Same as above | All 3 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-CL-04-016 | "Save" saves all preference changes | 1. Change toggles in several groups<br>2. Click "Save"<br>3. Log out, log in, reopen Preferences | All changes are persisted | High | ⬜⬜⬜⬜ |