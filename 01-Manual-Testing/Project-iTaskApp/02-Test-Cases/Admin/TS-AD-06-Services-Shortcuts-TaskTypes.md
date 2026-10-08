# TS-AD-06: Services, Shortcuts & Task Types

| Field | Details |
|-------|---------|
| **Suite ID** | TS-AD-06 |
| **Role** | Admin |
| **Priority** | Medium |
| **Type** | Functional, Negative, UI |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.3.3.8, 2.3.3.9, 2.3.3.10 |

## Objective
Verify that an Admin can manage services, home page shortcuts and the three task types.

## Preconditions
- Logged in as Admin
- At least one service, one shortcut and the 3 task types exist

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-AD-06.1 | Services: list, view, edit | 2.3.3.8 | 001-006 |
| SC-AD-06.2 | Services: delete, add, filter | 2.3.3.8 | 007-013 |
| SC-AD-06.3 | Shortcuts: list, view, edit | 2.3.3.9 | 014-019 |
| SC-AD-06.4 | Shortcuts: delete, add, sort, search | 2.3.3.9 | 020-027 |
| SC-AD-06.5 | Task Types | 2.3.3.10 | 028-034 |

---

## SC-AD-06.1 Services: list, view, edit

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-06-001 | "Services" opens the services list | 1. Manage - Services | List of services is shown | High | ⬜⬜⬜⬜ |
| TC-AD-06-002 | All columns are visible | 1. Check the table header | ID, Name, Assigned iTasker, Init. app. time, Price/Hr, Quote Fee, Category, Show Homepage, Status, Show discount, Created, Actions | Med | ⬜⬜⬜⬜ |
| TC-AD-06-003 | View, Edit and Delete buttons are available for each service | 1. Check each row | All 3 buttons are present | Med | ⬜⬜⬜⬜ |
| TC-AD-06-004 | "View" opens the service details | 1. Click "View"<br>2. Click "Preview Photo" | Page shows Name, Slug, Category, Show on homepage, Status, Enable Discounts, Initial Appointment Time, Description, Min. Time, Each Additional Hour, Quote Fee, Tags, Preview Photo. The photo opens in a new tab | Med | ⬜⬜⬜⬜ |
| TC-AD-06-005 | "Edit" opens an editable form and all fields can be modified | 1. Click "Edit"<br>2. Update Name and Status<br>3. Save | Changes are saved | High | ⬜⬜⬜⬜ |
| TC-AD-06-006 | "Save" saves all changes, and nothing is saved without it | 1. Change a field, navigate away without saving | Change is not kept | High | ⬜⬜⬜⬜ |

## SC-AD-06.2 Services: delete, add, filter

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-06-007 | "Delete" shows a confirmation | 1. Click "Delete" on a service | Message: Do you want to delete service "`<service name>`"? with Yes and No | High | ⬜⬜⬜⬜ |
| TC-AD-06-008 | "Yes" deletes the service | 1. Click "Yes" | Service no longer appears in the list | High | ⬜⬜⬜⬜ |
| TC-AD-06-009 | "No" closes the dialog and the service is not deleted | 1. Click "No" | Dialog closes. Service remains in the list | High | ⬜⬜⬜⬜ |
| TC-AD-06-010 | "+Add" opens the Add Service form with the required fields | 1. Click "+Add" | Required: Photo (max 30MB), Name, Slug (Friendly URL), Category | High | ⬜⬜⬜⬜ |
| TC-AD-06-011 | Photo upload rejects files larger than 30MB | 1. Upload `{FILE_OVER_30MB}`<br>2. Upload a valid photo *(added)* | Large file is rejected with an error message. Valid photo is accepted | Med | ⬜⬜⬜⬜ |
| TC-AD-06-012 | A new service is created after filling all required fields and saving | 1. Fill in all required fields<br>2. Click "Save" | New service appears in the list. It is not saved without "Save" | High | ⬜⬜⬜⬜ |
| TC-AD-06-013 | The filter field searches services by name | 1. Enter a service name | Correct results appear | Med | ⬜⬜⬜⬜ |

## SC-AD-06.3 Shortcuts: list, view, edit

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-06-014 | "Shortcuts" opens the shortcuts list | 1. Manage - Shortcuts | List of shortcuts is shown | High | ⬜⬜⬜⬜ |
| TC-AD-06-015 | All columns are visible | 1. Check the table header | ID, Title, Link, Description, Position, Status, Created, Updated, Actions | Med | ⬜⬜⬜⬜ |
| TC-AD-06-016 | View, Edit and Delete buttons are available for each shortcut | 1. Check each row | All 3 buttons are present | Med | ⬜⬜⬜⬜ |
| TC-AD-06-017 | "View" opens the shortcut details | 1. Click "View" | Page shows Photo, Title, Status, Link, Description with correct data | Med | ⬜⬜⬜⬜ |
| TC-AD-06-018 | "Edit" opens an editable form and all fields can be modified | 1. Click "Edit"<br>2. Update Title and Link<br>3. Save | Changes are saved | High | ⬜⬜⬜⬜ |
| TC-AD-06-019 | "Save" saves all changes, and nothing is saved without it | 1. Change a field, navigate away without saving | Change is not kept | High | ⬜⬜⬜⬜ |

## SC-AD-06.4 Shortcuts: delete, add, sort, search

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-06-020 | "Delete" shows a confirmation | 1. Click "Delete" on a shortcut | Message: Do you want to delete a shortcut "`<shortcut title>`"? with Yes and No<br>⚠️ The story's sample shows the title "Undefined". Check that the real message shows the actual title (open question 9) | Med | ⬜⬜⬜⬜ |
| TC-AD-06-021 | "Yes" deletes the shortcut | 1. Click "Yes" | Shortcut no longer appears in the list | High | ⬜⬜⬜⬜ |
| TC-AD-06-022 | "No" closes the dialog and the shortcut is not deleted | 1. Click "No" | Dialog closes. Shortcut remains in the list | High | ⬜⬜⬜⬜ |
| TC-AD-06-023 | "+Add" opens the Add Shortcut form with the required fields | 1. Click "+Add" | Required: Photo (max 30MB), Title, Link | High | ⬜⬜⬜⬜ |
| TC-AD-06-024 | Photo upload rejects files larger than 30MB | 1. Upload `{FILE_OVER_30MB}`<br>2. Upload a valid photo *(added)* | Large file is rejected with an error message. Valid photo is accepted | Med | ⬜⬜⬜⬜ |
| TC-AD-06-025 | A new shortcut is created after filling all required fields | 1. Fill in all fields<br>2. Click "Save" | New shortcut appears in the list | High | ⬜⬜⬜⬜ |
| TC-AD-06-026 | "Sort" reorders shortcuts and "Confirmation" saves the new order | 1. Click "Sort"<br>2. Drag a shortcut to a new position<br>3. Click "Confirmation" | New order is saved and shown on the Home page | Med | ⬜⬜⬜⬜ |
| TC-AD-06-027 | The search field filters shortcuts by keywords | 1. Enter a keyword | Correct results appear | Med | ⬜⬜⬜⬜ |

## SC-AD-06.5 Task Types

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-06-028 | "Task Types" opens the task types list | 1. Manage - Task types | List is shown | High | ⬜⬜⬜⬜ |
| TC-AD-06-029 | All columns are visible | 1. Check the table header | ID, Name, Title, Description, Suggestions, Actions | Med | ⬜⬜⬜⬜ |
| TC-AD-06-030 | The 3 task types are present | 1. Check the list | Pay per Task, Pay by Hour, Free Quote | High | ⬜⬜⬜⬜ |
| TC-AD-06-031 | View and Edit are available, with no Delete | 1. Check each row | View and Edit buttons only. There is no Delete button | Med | ⬜⬜⬜⬜ |
| TC-AD-06-032 | "View" opens the task type details | 1. Click "View" | Page shows Title and Description | Med | ⬜⬜⬜⬜ |
| TC-AD-06-033 | "Edit" opens an editable form and all fields can be modified | 1. Click "Edit"<br>2. Update Title or Description<br>3. Save | Changes are saved | High | ⬜⬜⬜⬜ |
| TC-AD-06-034 | "Save" saves all changes, and nothing is saved without it | 1. Change a field, navigate away without saving | Change is not kept | High | ⬜⬜⬜⬜ |