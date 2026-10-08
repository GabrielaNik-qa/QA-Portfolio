# TS-IT-07: Profile & Preferences

| Field | Details |
|-------|---------|
| **Suite ID** | TS-IT-07 |
| **Role** | iTasker |
| **Priority** | Medium |
| **Type** | Functional, UI, State-based |
| **Documentation** | User Story iTaskApp Feb/26, section 2.2.17 |

## Objective
Verify profile editing, password change, notification preferences, and log out.

## Preconditions
- iTasker is logged in with a completed profile

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-IT-07.1 | Profile | 2.2.17.1 | 001-008 |
| SC-IT-07.2 | Notification preferences | 2.2.17.2 | 009-017 |
| SC-IT-07.3 | Log out | 2.2.17.4 | 018 |

## Notification triggers (for future delivery tests)
Delivery of these notifications is not covered yet. The triggers below come from the story.

| Preference group | Trigger | Channels |
|------------------|---------|----------|
| Chat messages receiving | A new chat message arrives | Email, Push, Sound |
| New Suitable Tasks Appeared | A new suitable task is created | Email, Push, Sound |
| New Requested by Client Tasks | A client requests a new task | Email, Push, Sound |
| Task Hired | A client hires the iTasker for a task | Push, Sound |
| Task Canceled | A client cancels a task the iTasker was assigned to | Push, Sound |
| Task Rated | A client rates a task | Push, Sound |
| Follow up task confirmed | A client accepts a follow up task | Push, Sound |
| Follow up task canceled | A client cancels a follow up task | Push, Sound |
| Finances | A client approves or rejects an invoice | Email, Push, Sound |

---

## SC-IT-07.1 Profile

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-07-001 | Username dropdown shows the profile options | 1. Click the username | Options: Profile, Preferences, Log out<br>⚠️ Sections 2.2.8 and 2.2.17.3 also mention Messages (open question 10) | High | ⬜⬜⬜⬜ |
| TC-IT-07-002 | First name, Last name, Email, Phone are editable | Update the 4 fields with test values | Fields accept the new values | High | ⬜⬜⬜⬜ |
| TC-IT-07-003 | "Save changes" saves personal info | 1. Save<br>2. Log out and log in | New values are persisted | High | ⬜⬜⬜⬜ |
| TC-IT-07-004 | New password, New password (confirm), Current password fields are available | 1. Open the password section | All 3 fields are shown | Med | ⬜⬜⬜⬜ |
| TC-IT-07-005 | "Save password" saves the password change | New: `NewPass123!` / Confirm: same / Current: existing<br>1. Save<br>2. Log in again | New password works. The old one is rejected | High | ⬜⬜⬜⬜ |
| TC-IT-07-006 | Address (with Map button) and Zip/Postal code are editable | Edit both and click "Save changes" | Values are saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-007 | Main Service Category dropdown is available and changeable | Select a different category and save | New category is saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-008 | Business Information is displayed but not editable | Try to edit the fields | Fields are locked or read-only | Med | ⬜⬜⬜⬜ |

## SC-IT-07.2 Notification preferences

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-07-009 | "Chat messages receiving": Email, Push, Push-Alert Sound | Toggle each ON and OFF, Save, reopen | 3 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-010 | "New Suitable Tasks Appeared": Email, Push, Push-Alert Sound | Same as above | 3 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-011 | "New Requested by Client Tasks": Email, Push, Push-Alert Sound | Same as above | 3 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-012 | "Task Hired": Push, Push-Alert Sound | Same as above | 2 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-013 | "Task Canceled": Push, Push-Alert Sound | Same as above | 2 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-014 | "Task Rated": Push, Push-Alert Sound | Same as above | 2 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-015 | "Follow up task confirmed": Push, Push-Alert Sound | Same as above | 2 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-016 | "Follow up task canceled": Push, Push-Alert Sound | Same as above | 2 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |
| TC-IT-07-017 | "Finances": Email, Push, Push-Alert Sound | Same as above | 3 toggles exist and their state is saved | Med | ⬜⬜⬜⬜ |

## SC-IT-07.3 Log out

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-07-018 | "Log out" redirects to the Home page | 1. Click "Log out" | Home page opens without a logged-in profile | High | ⬜⬜⬜⬜ |