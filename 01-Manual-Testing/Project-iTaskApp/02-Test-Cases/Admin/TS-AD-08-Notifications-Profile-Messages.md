# TS-AD-08: Notifications, Profile & Messaging

| Field | Details |
|-------|---------|
| **Suite ID** | TS-AD-08 |
| **Role** | Admin |
| **Priority** | Medium |
| **Type** | Functional, UI, State-based |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.3.4, 2.3.5, 2.3.5.1 to 2.3.5.4 |

## Objective
Verify the Admin notification bell, profile editing, notification preferences, chat and log out.

## Preconditions
- Logged in as Admin
- An iTasker and a Client test account are available to trigger notifications and reports

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-AD-08.1 | Notifications (bell) | 2.3.4 | 001-005 |
| SC-AD-08.2 | Profile | 2.3.5, 2.3.5.1 | 006-009 |
| SC-AD-08.3 | Notification preferences | 2.3.5.2 | 010-014 |
| SC-AD-08.4 | Messages | 2.3.5.3 | 015-021 |
| SC-AD-08.5 | Log out | 2.3.5.4 | 022 |

---

## SC-AD-08.1 Notifications (bell)

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-08-001 | Bell icon is visible in the header | 1. Log in as Admin | Icon is visible | Med | ⬜⬜⬜⬜ |
| TC-AD-08-002 | Clicking the bell opens the notifications list | 1. Click the bell | List opens | Med | ⬜⬜⬜⬜ |
| TC-AD-08-003 | Unread count is displayed on the bell | 1. Trigger a new notification | Counter updates | Med | ⬜⬜⬜⬜ |
| TC-AD-08-004 | Clicking a notification marks it as read | 1. Click a notification | It is marked read and the counter decreases | Med | ⬜⬜⬜⬜ |
| TC-AD-08-005 | Notifications can be viewed one by one | 1. Open notifications one at a time | Each opens separately | Low | ⬜⬜⬜⬜ |

## SC-AD-08.2 Profile

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-08-006 | Username dropdown shows Profile, Preferences, Messages, Log out | 1. Click the username | All 4 options are shown | High | ⬜⬜⬜⬜ |
| TC-AD-08-007 | All profile fields are editable | Update with test data: Photo (max 30MB), First Name, Last Name, Email, Phone Number, New Password, New Password (Confirm), Current Password, Address, Zip/Postal Code, then click "Save changes" | All fields accept input and the changes are saved | High | ⬜⬜⬜⬜ |
| TC-AD-08-008 | Photo upload rejects files larger than 30MB | 1. Upload `{FILE_OVER_30MB}`<br>2. Upload a valid photo *(added)* | Large file is rejected with an error message. Valid photo is accepted | Med | ⬜⬜⬜⬜ |
| TC-AD-08-009 | "Save changes" saves all updates, and nothing is saved without it | 1. Change a field, navigate away without saving | Change is not kept | High | ⬜⬜⬜⬜ |

## SC-AD-08.3 Notification preferences

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-08-010 | "Chat Messages Receiving" has Email, Push, Push-Alert Sound toggles | Toggle each ON and OFF, Save | 3 toggles exist and their state is saved. Sound can be muted by the device settings | Med | ⬜⬜⬜⬜ |
| TC-AD-08-011 | "Worker Changes" has Email, Push, Push-Alert Sound toggles | 1. Toggle each ON and OFF, Save<br>2. iTasker: add or change a worker | 3 toggles exist. A notification arrives only through the enabled channels | Med | ⬜⬜⬜⬜ |
| TC-AD-08-012 | "Team Changes" has Email, Push, Push-Alert Sound toggles | 1. Toggle each ON and OFF, Save<br>2. iTasker: add or change a team | 3 toggles exist. A notification arrives only through the enabled channels | Med | ⬜⬜⬜⬜ |
| TC-AD-08-013 | "Reports by iTaskers & Clients" has Email, Push, Push-Alert Sound toggles | 1. Toggle each ON and OFF, Save<br>2. Client or iTasker: submit a report on a task | 3 toggles exist. A notification arrives only through the enabled channels | Med | ⬜⬜⬜⬜ |
| TC-AD-08-014 | "Save" saves all preference changes, and nothing is saved without it | 1. Change toggles, navigate away without saving | Changes are not kept | High | ⬜⬜⬜⬜ |

## SC-AD-08.4 Messages

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-08-015 | Chat page opens with personal and group chat options | 1. Click "Messages" | Chat window opens with personal and group chats | Med | ⬜⬜⬜⬜ |
| TC-AD-08-016 | "Participants" opens a popup with the right options | 1. Click "Participants"<br>2. Add a participant | Popup shows the participant list, a search field, Add and Remove options, and a checkbox to show only new messages. The added participant appears in the chat | Med | ⬜⬜⬜⬜ |
| TC-AD-08-017 | "Confirm" in the Participants popup saves the changes | 1. Make a change and click "Confirm"<br>2. Make another change and click "Close" | Confirmed change is saved. Closing without confirming saves nothing | Med | ⬜⬜⬜⬜ |
| TC-AD-08-018 | "+New Chat" allows searching and adding participants via "+Add" and removing via "Remove" | 1. Click "+New Chat"<br>2. Search, add and remove a participant | Search works. Add and Remove update the participant list | Med | ⬜⬜⬜⬜ |
| TC-AD-08-019 | "Create a New Chat" creates the chat | 1. Click "Create a New Chat" | Chat is created and appears in the messages list | High | ⬜⬜⬜⬜ |
| TC-AD-08-020 | Files can be attached in the chat | 1. Attach a file<br>2. Send | File is sent and can be opened | Med | ⬜⬜⬜⬜ |
| TC-AD-08-021 | The emoji selector is available in the chat | 1. Open the emoji selector<br>2. Select an emoji | The emoji appears in the message | Low | ⬜⬜⬜⬜ |

## SC-AD-08.5 Log out

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-08-022 | "Log out" redirects to the Home page without a logged-in profile | 1. Click "Log out" | Home page opens without a logged-in profile | High | ⬜⬜⬜⬜ |