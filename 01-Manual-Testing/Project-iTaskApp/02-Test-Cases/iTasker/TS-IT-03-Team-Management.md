# TS-IT-03: Team Management

| Field | Details |
|-------|---------|
| **Suite ID** | TS-IT-03 |
| **Role** | iTasker |
| **Priority** | High |
| **Type** | Functional, Negative |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.2.3, 2.2.10, 2.2.11, 2.2.12 |

## Objective
Verify team creation (5-step flow), editing, and removal of teams and team members.

## Preconditions
- iTasker is logged in with a completed profile
- At least one worker exists

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-IT-03.1 | Access and start | 2.2.3, 2.2.10 | 001-006 |
| SC-IT-03.2 | Step 1: Team name | 2.2.3 | 007-009 |
| SC-IT-03.3 | Step 2: Services | 2.2.3 | 010-012 |
| SC-IT-03.4 | Step 3: Workers | 2.2.3 | 013-015 |
| SC-IT-03.5 | Step 4: Working area | 2.2.3 | 016-018 |
| SC-IT-03.6 | Step 5: Completion | 2.2.3, 2.2.10 | 019-023 |
| SC-IT-03.7 | Edit and remove team members | 2.2.11 | 024-034 |
| SC-IT-03.8 | Edit and remove teams | 2.2.12 | 035-037 |

---

## SC-IT-03.1 Access and start

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-03-001 | "Company" is visible in the left sidebar | 1. Log in | Button is visible | High | ⬜⬜⬜⬜ |
| TC-IT-03-002 | "Company" opens a dropdown | 1. Click "Company" | Dropdown opens | High | ⬜⬜⬜⬜ |
| TC-IT-03-003 | "Teams" is in the Company dropdown | 1. Open the dropdown | "Teams" option is present | High | ⬜⬜⬜⬜ |
| TC-IT-03-004 | A default team exists after account setup | 1. Open Teams | The default team is listed | Med | ⬜⬜⬜⬜ |
| TC-IT-03-005 | "+Add" is available in the Teams menu | 1. Open Teams | Button is visible | High | ⬜⬜⬜⬜ |
| TC-IT-03-006 | "+Add" starts the team creation flow | 1. Click "+Add" | Step 1 opens | High | ⬜⬜⬜⬜ |

## SC-IT-03.2 Step 1: Team name

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-03-007 | Team name field is available | 1. Open Step 1 | Input is displayed | High | ⬜⬜⬜⬜ |
| TC-IT-03-008 | Team name is mandatory | 1. Leave empty<br>2. Continue | Error message or block | High | ⬜⬜⬜⬜ |
| TC-IT-03-009 | A valid team name is accepted and saved | Enter `Test Pro Team` | Name is accepted and kept through the flow | High | ⬜⬜⬜⬜ |

## SC-IT-03.3 Step 2: Services

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-03-010 | Services selection page is displayed | 1. Continue to Step 2 | Page lists the services the iTasker offers | High | ⬜⬜⬜⬜ |
| TC-IT-03-011 | iTasker can select one or more services | Select 2 services | Both are shown as selected | High | ⬜⬜⬜⬜ |
| TC-IT-03-012 | At least one service must be selected | Continue without a selection | Error message or block | High | ⬜⬜⬜⬜ |

## SC-IT-03.4 Step 3: Workers

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-03-013 | Workers selection page is displayed | 1. Continue to Step 3 | Page is displayed | High | ⬜⬜⬜⬜ |
| TC-IT-03-014 | iTasker can add one or more workers | Select available workers | Selected workers are shown | High | ⬜⬜⬜⬜ |
| TC-IT-03-015 | A team cannot be created without workers | Continue without selecting any worker | Continue is blocked with a message, because each team needs at least one worker  | High | ⬜⬜⬜⬜ |

## SC-IT-03.5 Step 4: Working area

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-03-016 | Map is displayed and functional | 1. Open Step 4 | Map loads and can be moved | High | ⬜⬜⬜⬜ |
| TC-IT-03-017 | iTasker can select a working area | Select an area around `Toronto, ON` | Area is highlighted | High | ⬜⬜⬜⬜ |
| TC-IT-03-018 | Working area is mandatory | Continue without an area | Error message or block | High | ⬜⬜⬜⬜ |

## SC-IT-03.6 Step 5: Completion

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-03-019 | Summary page shows all entered team details | 1. Complete Steps 1-4 | Name, services, workers and working area are shown correctly | High | ⬜⬜⬜⬜ |
| TC-IT-03-020 | "Create Team" is available on the final step | 1. Reach Step 5 | Button is visible | High | ⬜⬜⬜⬜ |
| TC-IT-03-021 | iTasker can create a new team | Team name: `Test Cleaning Team`<br>1. Click "Create Team" | Team is created | High | ⬜⬜⬜⬜ |
| TC-IT-03-022 | New team appears in the Teams list and is accessible | 1. Open Teams<br>2. Open the new team | Team is listed and opens | High | ⬜⬜⬜⬜ |
| TC-IT-03-023 | All entered details are saved correctly | 1. Open the new team | Name, services, workers and working area match what was entered | High | ⬜⬜⬜⬜ |

## SC-IT-03.7 Edit and remove team members

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-03-024 | List shows Email, Phone, Name, Team for each member | 1. Open the workers list | All 4 details are shown for every member | Med | ⬜⬜⬜⬜ |
| TC-IT-03-025 | View, Edit and Remove buttons are available per member | 1. Check each row | All 3 buttons are present | Med | ⬜⬜⬜⬜ |
| TC-IT-03-026 | "View" opens the member's details page | 1. Click "View" | Details page opens | Med | ⬜⬜⬜⬜ |
| TC-IT-03-027 | Details page shows first name, last name, email, phone, address, description and photo | 1. Open details | All fields are displayed | Med | ⬜⬜⬜⬜ |
| TC-IT-03-028 | Those fields are editable | 1. Click "Edit"<br>2. Change each field | All fields can be modified | Med | ⬜⬜⬜⬜ |
| TC-IT-03-029 | Changes are saved and reflected in the members list | 1. Save<br>2. Return to the Workers list | Updated details are shown | High | ⬜⬜⬜⬜ |
| TC-IT-03-030 | "Remove" shows a confirmation message | 1. Click "Remove" | Message: Are you sure you want to remove `<name>` worker? | High | ⬜⬜⬜⬜ |
| TC-IT-03-031 | "Yes" and "No" buttons are available in the dialog | 1. Check the dialog | Both buttons are present | Med | ⬜⬜⬜⬜ |
| TC-IT-03-032 | "Yes" removes the member | 1. Click "Yes" | Member no longer appears in the team | High | ⬜⬜⬜⬜ |
| TC-IT-03-033 |  "No" keeps the member | 1. Click "No" | Dialog closes and the member remains | Med | ⬜⬜⬜⬜ |
| TC-IT-03-034 | A removed member cannot be recovered | 1. Remove a member<br>2. Refresh the page | Member is still gone | Med | ⬜⬜⬜⬜ |

## SC-IT-03.8 Edit and remove teams

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-03-035 | iTasker can edit a team name and details | Rename to `Test Pro Team`, save | Changes are saved | High | ⬜⬜⬜⬜ |
| TC-IT-03-036 | iTasker can delete a team | 1. Delete a team | Team no longer appears in the list | High | ⬜⬜⬜⬜ |
| TC-IT-03-037 | A confirmation prompt appears before deleting a team | 1. Click delete | Confirmation dialog is shown before deletion | High | ⬜⬜⬜⬜ |