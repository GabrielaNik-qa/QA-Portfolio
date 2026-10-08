# TS-AD-02: Users & Workers

| Field | Details |
|-------|---------|
| **Suite ID** | TS-AD-02 |
| **Role** | Admin |
| **Priority** | High |
| **Type** | Functional, Negative, UI |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.3.3.1 and 2.3.3.2 |

## Objective
Verify that an Admin can list, filter, view, edit, add and delete users, and manage workers created by iTaskers.

## Preconditions
- Logged in as Admin
- Test users exist for each role, including a Client and an iTasker (one with a complete profile and one incomplete)
- At least one Worker exists

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-AD-02.1 | Users: list, filters and details | 2.3.3.1 | 001-012 |
| SC-AD-02.2 | Users: edit, sign as user, delete, add | 2.3.3.1 | 013-022 |
| SC-AD-02.3 | Workers: list, view, edit, remove | 2.3.3.2 | 023-032 |
| SC-AD-02.4 | Workers: filter and add | 2.3.3.2 | 033-035 |

---

## SC-AD-02.1 Users: list, filters and details

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-02-001 | "Users" opens the users list page | 1. Manage - Users | Users list page opens | High | ⬜⬜⬜⬜ |
| TC-AD-02-002 | All 15 columns are visible | 1. Check the table header | Columns: ID, iTasker, Approval, Avatar, First name, Last name, E-mail, Phone, Status, Role, Category, Created, Updated, Last Login, Actions. Actions has View, Edit, Sign as User, Delete | Med | ⬜⬜⬜⬜ |
| TC-AD-02-003 | iTasker column shows a green tick for complete profiles and a red X for incomplete ones | 1. Check a complete and an incomplete iTasker profile | Green tick for complete, red X for incomplete. Empty for other roles | Med | ⬜⬜⬜⬜ |
| TC-AD-02-004 | Approval column can be filtered by Approved, Pending, Rejected | Test each option | Only users with the selected approval are shown | Med | ⬜⬜⬜⬜ |
| TC-AD-02-005 | Status column can be filtered by Active, Inactive | Test each option | Only users with the selected status are shown | Med | ⬜⬜⬜⬜ |
| TC-AD-02-006 | Role column can be filtered by all roles | Test: Client, iTasker, Worker, Admin, Manager, Operator, Paymaster, Support<br>⚠️ See open question 8 | Only users with the selected role are shown | Med | ⬜⬜⬜⬜ |
| TC-AD-02-007 | Created, Updated and Last Login columns can be filtered by date | Filter each column by a date range | Results match the range | Med | ⬜⬜⬜⬜ |
| TC-AD-02-008 | "View" opens View User with the right sections | 1. Open a Client<br>2. Open an iTasker | Sections: Profile, Credentials, Documents. "iTasker Data" appears only for the iTasker role | High | ⬜⬜⬜⬜ |
| TC-AD-02-009 | Profile section displays all fields | 1. Open the Profile section | Name, Surname, Address, Phone number, Role, Approval, iTasker, Main service category, Description | Med | ⬜⬜⬜⬜ |
| TC-AD-02-010 | Credentials section displays Email and Status | 1. Open the Credentials section | Both fields are shown | Med | ⬜⬜⬜⬜ |
| TC-AD-02-011 | Documents section displays uploaded documents | 1. Open the Documents section | Documents the user uploaded are listed | Med | ⬜⬜⬜⬜ |
| TC-AD-02-012 | iTasker Data section displays business info, references, insurance and bank info | 1. Open an iTasker, then iTasker Data | All 4 groups of information are shown | Med | ⬜⬜⬜⬜ |

## SC-AD-02.2 Users: edit, sign as user, delete, add

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-02-013 | "Edit" opens the same page as View with editable fields | 1. Click "Edit"<br>2. Update a field | All fields are editable | High | ⬜⬜⬜⬜ |
| TC-AD-02-014 | "Save" saves all changes, and nothing is saved without it | 1. Change a field and click "Save"<br>2. Change another field, navigate away without saving | Saved change persists. Unsaved change is not kept | High | ⬜⬜⬜⬜ |
| TC-AD-02-015 | "Sign as User" shows a confirmation | 1. Click "Sign as User" | Message: Do you want to Sign As user "`<user name>`"? with Yes and No | Med | ⬜⬜⬜⬜ |
| TC-AD-02-016 | "Yes" logs the Admin in as the selected user | 1. Click "Yes" | Session switches to the selected user's account | High | ⬜⬜⬜⬜ |
| TC-AD-02-017 | "No" closes the dialog and no action is taken | 1. Click "No" | Dialog closes. The Admin session is unchanged | Med | ⬜⬜⬜⬜ |
| TC-AD-02-018 | "Delete" shows a confirmation | 1. Click "Delete" on a test user | Message: Do you want to delete user "`<user name>`"? with Yes and No | High | ⬜⬜⬜⬜ |
| TC-AD-02-019 | "Yes" permanently deletes the user | 1. Click "Yes" | User no longer appears in the Users list | High | ⬜⬜⬜⬜ |
| TC-AD-02-020 | "No" closes the dialog and the user is not deleted | 1. Click "No" | Dialog closes. User remains in the list | High | ⬜⬜⬜⬜ |
| TC-AD-02-021 | "Add" is available top right and opens the Add User page | 1. Click "Add" | Add User page opens with the same sections as View and Edit | High | ⬜⬜⬜⬜ |
| TC-AD-02-022 | A new user can be created with all required fields | 1. Fill in all fields<br>2. Click "Save" | New user appears in the list | High | ⬜⬜⬜⬜ |

## SC-AD-02.3 Workers: list, view, edit, remove

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-02-023 | "Workers" opens a page with all Workers in the system | 1. Manage - Workers | List of all Workers (created by all iTaskers) is shown | High | ⬜⬜⬜⬜ |
| TC-AD-02-024 | Name, email, phone, profile photo and status are visible for each Worker | 1. Check the list | All 5 items are shown for every Worker | Med | ⬜⬜⬜⬜ |
| TC-AD-02-025 | View, Edit and Remove buttons are available for each Worker | 1. Check each row | All 3 buttons are present | Med | ⬜⬜⬜⬜ |
| TC-AD-02-026 | "View" opens the Worker details page | 1. Click "View" | Page shows First name, Last name, Email, Phone Number, iTasker, Address, Description, Photo, Documents with correct data | High | ⬜⬜⬜⬜ |
| TC-AD-02-027 | "Edit" opens an editable form with the same fields as View | 1. Click "Edit"<br>2. Update fields | Fields are editable | High | ⬜⬜⬜⬜ |
| TC-AD-02-028 | Admin can change the status of a Worker from the Edit page | 1. Change the status<br>2. Save | Status is updated in the Workers list. A Worker must be approved by the Admin before an iTasker can assign them to a task | High | ⬜⬜⬜⬜ |
| TC-AD-02-029 | "Save" saves all changes, and nothing is saved without it | 1. Change a field and click "Save"<br>2. Change another field, navigate away without saving | Saved change persists. Unsaved change is not kept | High | ⬜⬜⬜⬜ |
| TC-AD-02-030 | "Remove" shows a confirmation | 1. Click "Remove" | Message: Are you sure you want to remove `<worker name>` worker? with Yes and No | High | ⬜⬜⬜⬜ |
| TC-AD-02-031 | "Yes" removes the Worker | 1. Click "Yes" | Worker no longer appears in the list | High | ⬜⬜⬜⬜ |
| TC-AD-02-032 | "No" closes the dialog and the Worker is not removed | 1. Click "No" | Dialog closes. Worker remains in the list | High | ⬜⬜⬜⬜ |

## SC-AD-02.4 Workers: filter and add

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-02-033 | The Filter field searches Workers by name | 1. Enter a worker name | Only matching Workers are shown | Med | ⬜⬜⬜⬜ |
| TC-AD-02-034 | "Add" opens the Add Worker page with all fields | 1. Click "Add" | Page shows: First name, Last name, Email, Phone number, iTasker (dropdown), Address, Description, Photo, Documents | High | ⬜⬜⬜⬜ |
| TC-AD-02-035 | A new Worker can be created with all required fields | 1. Fill in all fields<br>2. Save | New Worker appears in the list | High | ⬜⬜⬜⬜ |