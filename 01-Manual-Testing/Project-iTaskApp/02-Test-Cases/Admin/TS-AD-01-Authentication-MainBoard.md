# TS-AD-01: Authentication, Main Board & Manage Menu

| Field | Details |
|-------|---------|
| **Suite ID** | TS-AD-01 |
| **Role** | Admin |
| **Priority** | High |
| **Type** | Functional, Negative |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.3, 2.3.1, 2.3.2, 2.3.3 |

## Objective
Verify that an Admin can sign in, lands on the Main Board, manages tasks from it, and sees the full Manage menu.

## Preconditions
- An Admin account exists (`{ADMIN_EMAIL}`)
- At least one task exists in the system

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-AD-01.1 | Sign in as Admin | 2.3, 2.3.1 | 001-005 |
| SC-AD-01.2 | Main Board | 2.3.2 | 006-013 |
| SC-AD-01.3 | Manage menu | 2.3.3 | 014-015 |

---

## SC-AD-01.1 Sign in as Admin

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-01-001 | "Sign in" button is available in the header | 1. Open the home page | Button is visible | High | ⬜⬜⬜⬜ |
| TC-AD-01-002 | Email and Password fields are available on the login page | 1. Click "Sign in"<br>2. Enter `{ADMIN_EMAIL}` and the admin password | Both fields are present and accept input | High | ⬜⬜⬜⬜ |
| TC-AD-01-003 | "Continue" logs in and redirects the Admin directly to the Main Board | 1. Click "Continue" | Landing page is the Main Board, not the Dashboard | High | ⬜⬜⬜⬜ |
| TC-AD-01-004 | A regular user cannot self-register as Admin | 1. Try to register as an Admin from the registration pages | No Admin option exists. Registration as Admin is not possible | High | ⬜⬜⬜⬜ |
| TC-AD-01-005 | Admin can assign the Admin role via Manage - Users - Edit - Role | 1. Find a test user<br>2. Click Edit<br>3. Set Role to "Admin"<br>4. Save | Role is updated. The user can now sign in as Admin | High | ⬜⬜⬜⬜ |

## SC-AD-01.2 Main Board

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-01-006 | Main Board loads after login and lists all tasks in the system | 1. Log in as Admin | Page loads with a list of all tasks | High | ⬜⬜⬜⬜ |
| TC-AD-01-007 | All 12 columns are visible | 1. Check the table header | Columns: ID, Status, Task type, Applications, Service, Client, iTasker, Team, Address, Invoices, Created, Actions | Med | ⬜⬜⬜⬜ |
| TC-AD-01-008 | Search field filters tasks by task name | 1. Enter a task name | Only matching tasks are shown | Med | ⬜⬜⬜⬜ |
| TC-AD-01-009 | Filter button filters tasks by status: New, Active, Closed | Test each status | Only tasks with the selected status are shown | Med | ⬜⬜⬜⬜ |
| TC-AD-01-010 | "View" opens the Task Details page with full task information | 1. Click "View" on a task | Task Details page opens | High | ⬜⬜⬜⬜ |
| TC-AD-01-011 | "Delete" shows a confirmation message | 1. Click "Delete" on a task | Message: Do you want to delete task "`<task name>`"? with options Yes and No | High | ⬜⬜⬜⬜ |
| TC-AD-01-012 | "No" closes the dialog and the task is not deleted | 1. Click "No" | Dialog closes. Task still appears on the Main Board | High | ⬜⬜⬜⬜ |
| TC-AD-01-013 | "Yes" permanently deletes the task from the Main Board and the system | 1. Click "Yes"<br>2. Reload the page | Task no longer appears on the Main Board or anywhere in the system | High | ⬜⬜⬜⬜ |

## SC-AD-01.3 Manage menu

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-01-014 | "Manage" menu is available in the header | 1. Log in as Admin | Menu is visible in the header | High | ⬜⬜⬜⬜ |
| TC-AD-01-015 | "Manage" opens a dropdown with all 17 submenus | 1. Click "Manage" | Submenus: Users, Roles, Companies, Teams, Workers, Task Codes, Promo Codes, Finances, Pages, Categories, Services, Custom forms, Shortcuts, Task types, Statistics, Preferences, System Settings | Med | ⬜⬜⬜⬜ |