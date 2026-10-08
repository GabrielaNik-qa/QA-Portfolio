# TS-AD-03: Teams

| Field | Details |
|-------|---------|
| **Suite ID** | TS-AD-03 |
| **Role** | Admin |
| **Priority** | High |
| **Type** | Functional, Negative |
| **Documentation** | User Story iTaskApp Feb/26, section 2.3.3.3 |

## Objective
Verify that an Admin can list, filter, view, edit, add and remove teams, and that a team always needs at least one worker and one service.

## Preconditions
- Logged in as Admin
- At least one iTasker with approved workers and services, and at least one existing team

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-AD-03.1 | Teams list and view | 2.3.3.3 | 001-006 |
| SC-AD-03.2 | Edit a team | 2.3.3.3 | 007-009 |
| SC-AD-03.3 | Remove a team | 2.3.3.3 | 010-012 |
| SC-AD-03.4 | Filter and add a team | 2.3.3.3 | 013-017 |

---

## SC-AD-03.1 Teams list and view

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-03-001 | "Teams" opens a page with all teams in the system | 1. Manage - Teams | List of all teams is shown | High | ⬜⬜⬜⬜ |
| TC-AD-03-002 | Team name, members, iTasker, status, working region and services are visible | 1. Check the list | All 6 items are shown for each team | Med | ⬜⬜⬜⬜ |
| TC-AD-03-003 | View, Edit and Remove buttons are available for each team | 1. Check each row | All 3 buttons are present | Med | ⬜⬜⬜⬜ |
| TC-AD-03-004 | "View" opens the team details page | 1. Click "View" | Page shows 4 sections: iTasker, Services, Members, Working area, each with correct data | High | ⬜⬜⬜⬜ |
| TC-AD-03-005 | Quick Edit and Remove buttons are available on the View page | 1. Open View | Quick Edit and Remove buttons are at the top right, and each section has an Edit button | Med | ⬜⬜⬜⬜ |
| TC-AD-03-006 | Admin can change the team status from the View page | 1. Change the status | Status is updated and shown in the list | High | ⬜⬜⬜⬜ |

## SC-AD-03.2 Edit a team

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-03-007 | "Edit" opens a 5-step editing flow | Go through all 5 steps | Step 1 iTasker and Team name, Step 2 Services, Step 3 Workers, Step 4 Working area, Step 5 Review (reached through "Edit info") | High | ⬜⬜⬜⬜ |
| TC-AD-03-008 | All changes are saved after "Save" on the final step | 1. Change data in each step<br>2. Click "Save" | Changes are reflected on the View page and in the list | High | ⬜⬜⬜⬜ |
| TC-AD-03-009 | "Save" saves all changes, and nothing is saved without it | 1. Change a field, navigate away without saving | Change is not kept | High | ⬜⬜⬜⬜ |

## SC-AD-03.3 Remove a team

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-03-010 | "Remove" shows a confirmation message | 1. Click "Remove" | Confirmation with Yes and No is shown | High | ⬜⬜⬜⬜ |
| TC-AD-03-011 | "Yes" removes the team | 1. Click "Yes" | Team no longer appears in the list | High | ⬜⬜⬜⬜ |
| TC-AD-03-012 | "No" closes the dialog and the team is not removed | 1. Click "No" | Dialog closes. Team remains in the list | High | ⬜⬜⬜⬜ |

## SC-AD-03.4 Filter and add a team

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-03-013 | The Filter field searches teams by name | 1. Enter a team name | Only matching teams are shown | Med | ⬜⬜⬜⬜ |
| TC-AD-03-014 | The second filter filters teams by status | Test each status option | Only teams with the selected status are shown | Med | ⬜⬜⬜⬜ |
| TC-AD-03-015 | "Add Team" opens a creation flow with the same 5 steps | Step 1: iTasker and team name / Step 2: Services / Step 3: Workers / Step 4: Working area / Step 5: Summary | All 5 steps work. Services and Workers lists contain only items of the selected iTasker | High | ⬜⬜⬜⬜ |
| TC-AD-03-016 | A newly created team appears in the Teams list | Team name: `Test Admin Team`<br>1. Complete the flow and save | Team is listed with the entered data | High | ⬜⬜⬜⬜ |
| TC-AD-03-017 | *(added)* A team cannot be created without a worker or without a service | 1. Try to continue Step 2 without a service<br>2. Try to continue Step 3 without a worker | Both are blocked, because each team needs at least one worker and one service | High | ⬜⬜⬜⬜ |