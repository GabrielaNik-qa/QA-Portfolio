# TS-NB-04: Members, Calendar & Shortcuts

| Field | Details |
|-------|---------|
| **Suite ID** | TS-NB-04 |
| **Role** | Admin |
| **Priority** | Medium |
| **Type** | Functional, Negative, UI |
| **Documentation** | Neighbourhood Intern Feb/25, sections NB-4, NB-7, NB-8 |

## Objective
Verify the Members tab, the right sidebar calendar, and the management of Neighbourhood shortcuts.

## Preconditions
- Logged in as Admin
- A group with members and a pending membership request exists
- At least one event exists in the current month
- At least one shortcut exists

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-NB-04.1 | Members tab | NB-7 | 001-006, 026 |
| SC-NB-04.2 | Right sidebar calendar | NB-8 | 007-010 |
| SC-NB-04.3 | Shortcuts submenu | NB-4 | 011-025 |

---

## SC-NB-04.1 Members tab

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-NB-04-001 | The "Members" tab shows all group members | 1. Click the Members tab | All members are listed | High | ⬜⬜⬜⬜ |
| TC-NB-04-002 | Each member has a visible status | 1. Check the list | A status is shown for every member | Med | ⬜⬜⬜⬜ |
| TC-NB-04-003 | Each member has an options menu | 1. Open the menu on a member | Menu opens | Med | ⬜⬜⬜⬜ |
| TC-NB-04-004 | "Copy link to profile" copies the member's profile link | 1. Click the option<br>2. Paste it in the browser | The member's profile opens | Low | ⬜⬜⬜⬜ |
| TC-NB-04-005 | "Block" blocks the selected member | 1. Block a test member | The member no longer has access to the group | High | ⬜⬜⬜⬜ |
| TC-NB-04-006 | "Delete membership request" removes the member's request | 1. Delete a pending request | The request is removed from the list | Med | ⬜⬜⬜⬜ |
| TC-NB-04-026 | The member status reflects the membership state | 1. Check the status of a pending membership request<br>2. Check the status of an active member | The statuses differ and match each member's state<br>⚠️ The document names the field but does not list its values (open question 13) | Med | ⬜⬜⬜⬜ |

## SC-NB-04.2 Right sidebar calendar

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-NB-04-007 | The calendar is shown in the right sidebar with the current month | 1. Open Neighbourhood | The current month is displayed | Med | ⬜⬜⬜⬜ |
| TC-NB-04-008 | Dates with events are highlighted in bold red circles | 1. Check a month with events | Event dates are bold in red circles | Med | ⬜⬜⬜⬜ |
| TC-NB-04-009 | Clicking a highlighted date shows the event of that day | 1. Click a bold date | The event for that day is displayed | Med | ⬜⬜⬜⬜ |
| TC-NB-04-010 | Clicking the event opens the group where it was created | 1. Click the event | The correct group page opens | Med | ⬜⬜⬜⬜ |

## SC-NB-04.3 Shortcuts submenu

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-NB-04-011 | The Shortcuts submenu is accessible from the Neighbourhood admin area | 1. Open the Shortcuts submenu | List of shortcuts is shown | High | ⬜⬜⬜⬜ |
| TC-NB-04-012 | All columns are visible | 1. Check the table header | ID, Title, Link, Description, Position, Status, Created, Updated, Actions | Med | ⬜⬜⬜⬜ |
| TC-NB-04-013 | View, Edit and Delete buttons are available for each shortcut | 1. Check each row | All 3 buttons are present | Med | ⬜⬜⬜⬜ |
| TC-NB-04-014 | "View" opens the shortcut details | 1. Click "View" | Page shows Photo, Title, Category, Status, Link, Description with correct data | Med | ⬜⬜⬜⬜ |
| TC-NB-04-015 | "Edit" opens an editable form and all fields can be modified | 1. Click "Edit"<br>2. Update Title and Link | All fields are editable | High | ⬜⬜⬜⬜ |
| TC-NB-04-016 | "Save" saves all changes, and nothing is saved without it | 1. Change a field and click "Save"<br>2. Change another, navigate away without saving | Saved change persists. Unsaved change is not kept | High | ⬜⬜⬜⬜ |
| TC-NB-04-017 | "Delete" shows a confirmation | 1. Click "Delete" on a shortcut | Message: Do you want to delete a shortcut "`<shortcut title>`"? with Yes and No<br>⚠️ The document's sample shows "Undefined" as the title (open question 9) | Med | ⬜⬜⬜⬜ |
| TC-NB-04-018 | "Yes" deletes the shortcut | 1. Click "Yes" | Shortcut no longer appears in the list | High | ⬜⬜⬜⬜ |
| TC-NB-04-019 | "No" closes the dialog and the shortcut is not deleted | 1. Click "No" | Dialog closes. Shortcut remains in the list | High | ⬜⬜⬜⬜ |
| TC-NB-04-020 | "+Add" opens the Add Shortcut form with the required fields | 1. Click "+Add" | Required: Photo (max 30MB), Title, Link | High | ⬜⬜⬜⬜ |
| TC-NB-04-021 | Photo upload rejects files larger than 30MB | 1. Upload `{FILE_OVER_30MB}`<br>2. Upload a valid photo *(added)* | Large file is rejected with an error message. Valid photo is accepted | Med | ⬜⬜⬜⬜ |
| TC-NB-04-022 | A new shortcut is created after filling all required fields | 1. Fill in all fields<br>2. Click "Save" | New shortcut appears in the list. It is not saved without "Save" | High | ⬜⬜⬜⬜ |
| TC-NB-04-023 | "Sort" reorders shortcuts and "Confirmation" saves the new order | 1. Click "Sort"<br>2. Drag a shortcut to a new position<br>3. Click "Confirmation" | New order is saved | Med | ⬜⬜⬜⬜ |
| TC-NB-04-024 | The search field filters shortcuts by keywords | 1. Enter a keyword | Correct results appear | Med | ⬜⬜⬜⬜ |
| TC-NB-04-025 | A shortcut can be activated or temporarily restricted | 1. Edit a shortcut and set the status to Inactive, Save<br>2. Check the shortcut for a Client<br>3. Set it back to Active, Save | The Inactive shortcut is not available to users. The Active shortcut is available again | Med | ⬜⬜⬜⬜ |