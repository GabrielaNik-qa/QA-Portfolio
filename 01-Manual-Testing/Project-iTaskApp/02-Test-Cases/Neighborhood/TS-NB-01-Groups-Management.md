# TS-NB-01: Groups Management

| Field | Details |
|-------|---------|
| **Suite ID** | TS-NB-01 |
| **Role** | Admin |
| **Priority** | High |
| **Type** | Functional, Negative, UI |
| **Documentation** | Neighbourhood Intern Feb/25, sections NB-1, NB-2, NB-3 |

## Objective
Verify that an Admin can find, filter, create, edit, delete and share Neighbourhood groups, and that the Private and Hidden settings work.

## Preconditions
- Logged in as Admin
- Public, Private, Hidden, active and inactive groups exist
- A Client account and a second user who is not a member are available

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-NB-01.1 | Browse, search and filter groups | NB-1 | 001-005 |
| SC-NB-01.2 | Add a group | NB-2 | 006-014, 021 |
| SC-NB-01.3 | Edit, delete and share a group | NB-3 | 015-020 |

---

## SC-NB-01.1 Browse, search and filter groups

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-NB-01-001 | The Neighbourhood page is accessible for the Admin | 1. Log in as Admin<br>2. Open Neighbourhood | Page opens with the list of groups | High | ⬜⬜⬜⬜ |
| TC-NB-01-002 | The search field in the header finds a group by name | Enter a group name | Only matching groups are shown | Med | ⬜⬜⬜⬜ |
| TC-NB-01-003 | The filter works by Visibility: Public, Private | Test each option | Only groups with the selected visibility are shown | Med | ⬜⬜⬜⬜ |
| TC-NB-01-004 | The filter works by Membership: Member, Owner | Test each option | Only groups where the Admin is a member, or the owner, are shown | Med | ⬜⬜⬜⬜ |
| TC-NB-01-005 | The filter works by Status: Active, Inactive | Test each option | Only groups with the selected status are shown | Med | ⬜⬜⬜⬜ |

## SC-NB-01.2 Add a group

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-NB-01-006 | "+Add" is available in the header and in the left sidebar | 1. Click "+Add" in the header<br>2. Click "+Add" in the sidebar | Both lead to the same Add Group form | High | ⬜⬜⬜⬜ |
| TC-NB-01-007 | The Add Group form has all fields | 1. Open the form | Photo, Group name, Description ("Write more information about group"), Private Group toggle, Hidden Group toggle, Location (optional) | High | ⬜⬜⬜⬜ |
| TC-NB-01-008 | Photo upload rejects files larger than 30MB | 1. Upload `{FILE_OVER_30MB}`<br>2. Upload a valid photo *(added)* | Large file is rejected with an error message. Valid photo is accepted | Med | ⬜⬜⬜⬜ |
| TC-NB-01-009 | Group name is mandatory | 1. Leave Group name empty<br>2. Click "Create" | Group is not created and an error is shown | High | ⬜⬜⬜⬜ |
| TC-NB-01-010 | Description is mandatory | 1. Leave Description empty<br>2. Click "Create" | Group is not created and an error is shown | High | ⬜⬜⬜⬜ |
| TC-NB-01-011 | "Private Group" requires Admin approval for new members | 1. Create a group with the toggle ON<br>2. As another user, try to join | A membership request is sent and waits for Admin approval | High | ⬜⬜⬜⬜ |
| TC-NB-01-012 | "Hidden Group" makes the group visible only to the Admin | 1. Create a group with the toggle ON<br>2. Log in as a Client | The group is not visible to the Client. The Admin sees it | High | ⬜⬜⬜⬜ |
| TC-NB-01-013 | Location is optional | 1. Leave Location empty<br>2. Click "Create" | Group is created successfully | Med | ⬜⬜⬜⬜ |
| TC-NB-01-014 | "Create" saves the group and it appears in the list | 1. Fill in the required fields<br>2. Click "Create"<br>3. Repeat but leave without clicking "Create" | The group appears in the list. Without "Create" it is not saved | High | ⬜⬜⬜⬜ |
| TC-NB-01-021 | A group cannot be created without a photo | 1. Fill in Group name and Description<br>2. Leave the photo empty<br>3. Click "Create" | The group is not created and an error is shown, because the photo is a required field | Med | ⬜⬜⬜⬜ |

## SC-NB-01.3 Edit, delete and share a group

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-NB-01-015 | "Edit" is available in the top right of each group header | 1. Open a group | Button is visible | Med | ⬜⬜⬜⬜ |
| TC-NB-01-016 | "Edit" opens the Edit a Group page with the same fields as Add Group | 1. Click "Edit"<br>2. Change the name and description<br>3. Save | Fields match the Add Group form. Changes are saved | High | ⬜⬜⬜⬜ |
| TC-NB-01-017 | A group can be deleted from the "Danger Zone" menu | 1. Open the Danger Zone dropdown<br>2. Delete the group | Group is deleted and no longer in the list<br>⚠️ The document does not say whether a confirmation appears (open question 12) | High | ⬜⬜⬜⬜ |
| TC-NB-01-018 | "Share" is available for each group | 1. Open a group | Button is visible | Med | ⬜⬜⬜⬜ |
| TC-NB-01-019 | A group can be shared to Facebook, LinkedIn, Pinterest and Reddit | Click each platform | The correct sharing page opens for each | Low | ⬜⬜⬜⬜ |
| TC-NB-01-020 | "Copy link" copies the group link | 1. Click "Copy link"<br>2. Paste it in the browser | The correct group page opens | Low | ⬜⬜⬜⬜ |