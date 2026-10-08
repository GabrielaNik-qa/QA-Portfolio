# TS-AD-05: Pages & Categories

| Field | Details |
|-------|---------|
| **Suite ID** | TS-AD-05 |
| **Role** | Admin |
| **Priority** | Medium |
| **Type** | Functional, Negative, UI |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.3.3.6 and 2.3.3.7 |

## Objective
Verify that an Admin can manage information pages and service categories: list, view, edit, add, delete, search, sort.

## Preconditions
- Logged in as Admin
- At least one page and one category exist

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-AD-05.1 | Pages: list, view, edit | 2.3.3.6 | 001-006 |
| SC-AD-05.2 | Pages: delete, search, sort, add | 2.3.3.6 | 007-013 |
| SC-AD-05.3 | Categories: list, view, edit | 2.3.3.7 | 014-020 |
| SC-AD-05.4 | Categories: delete, add, sort, search | 2.3.3.7 | 021-028 |

---

## SC-AD-05.1 Pages: list, view, edit

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-05-001 | "Pages" opens the pages management list | 1. Manage - Pages | List of pages is shown | High | ⬜⬜⬜⬜ |
| TC-AD-05-002 | View, Edit and Delete buttons are available for each page | 1. Check each row | All 3 buttons are present | Med | ⬜⬜⬜⬜ |
| TC-AD-05-003 | "View" opens the page details | 1. Click "View" | Page shows Title, Slug, Status, Description, Short Description with correct data | Med | ⬜⬜⬜⬜ |
| TC-AD-05-004 | Quick preview shows how the page looks in the system | 1. Open the preview on the View page | Preview matches how the page appears to users | Low | ⬜⬜⬜⬜ |
| TC-AD-05-005 | "Edit" opens an editable form with the same fields as View | 1. Click "Edit"<br>2. Update Title and Status<br>3. Save | Fields are editable and the changes are saved | High | ⬜⬜⬜⬜ |
| TC-AD-05-006 | "Save" saves all changes, and nothing is saved without it | 1. Change a field, navigate away without saving | Change is not kept | High | ⬜⬜⬜⬜ |

## SC-AD-05.2 Pages: delete, search, sort, add

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-05-007 | "Delete" shows a confirmation | 1. Click "Delete" on a page | Message: Do you want to delete page "`<page title>`"? with Yes and No | High | ⬜⬜⬜⬜ |
| TC-AD-05-008 | "Yes" deletes the page | 1. Click "Yes" | Page no longer appears in the list | High | ⬜⬜⬜⬜ |
| TC-AD-05-009 | "No" closes the dialog and the page is not deleted | 1. Click "No" | Dialog closes. Page remains in the list | High | ⬜⬜⬜⬜ |
| TC-AD-05-010 | The Filter field searches pages by keywords from their content | 1. Enter a keyword from a page's content | Correct pages appear | Med | ⬜⬜⬜⬜ |
| TC-AD-05-011 | Pages can be sorted by ID, Title, Friendly URL, Status, Created, Updated | Test each sort option | The list is ordered by the selected column | Med | ⬜⬜⬜⬜ |
| TC-AD-05-012 | "Add" opens the Add Page form with all fields | 1. Click "Add" at the top right | Fields: Title, Slug, Status, Description, Short Description | High | ⬜⬜⬜⬜ |
| TC-AD-05-013 | A new page is created after filling all required fields | 1. Fill in all fields<br>2. Save | New page appears in the list | High | ⬜⬜⬜⬜ |

## SC-AD-05.3 Categories: list, view, edit

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-05-014 | "Categories" opens the categories list | 1. Manage - Categories | List of categories is shown | High | ⬜⬜⬜⬜ |
| TC-AD-05-015 | All columns are visible | 1. Check the table header | ID, Name, Description, Services Count, Position, Status, Created, Updated, Actions | Med | ⬜⬜⬜⬜ |
| TC-AD-05-016 | View, Edit and Delete buttons are available for each category | 1. Check each row | All 3 buttons are present | Med | ⬜⬜⬜⬜ |
| TC-AD-05-017 | "View" opens the category details | 1. Click "View"<br>2. Click "Preview Photo" | Page shows Name, Status, Description, Preview Photo. The photo opens in a new tab | Med | ⬜⬜⬜⬜ |
| TC-AD-05-018 | "Edit" opens an editable form and all fields can be modified | 1. Click "Edit"<br>2. Update Name and Status<br>3. Save | Changes are saved | High | ⬜⬜⬜⬜ |
| TC-AD-05-019 | Admin can set the category status to Active or Inactive | 1. Toggle the status<br>2. Save | Status change is saved and shown in the list | High | ⬜⬜⬜⬜ |
| TC-AD-05-020 | "Save" saves all changes, and nothing is saved without it | 1. Change a field, navigate away without saving | Change is not kept | High | ⬜⬜⬜⬜ |

## SC-AD-05.4 Categories: delete, add, sort, search

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-05-021 | "Delete" shows a confirmation | 1. Click "Delete" on a category | Message: Do you want to delete category "`<category name>`"? with Yes and No | High | ⬜⬜⬜⬜ |
| TC-AD-05-022 | "Yes" deletes the category | 1. Click "Yes" | Category no longer appears in the list | High | ⬜⬜⬜⬜ |
| TC-AD-05-023 | "No" closes the dialog and the category is not deleted | 1. Click "No" | Dialog closes. Category remains in the list | High | ⬜⬜⬜⬜ |
| TC-AD-05-024 | "+Add" opens the Add Category form with the required fields | 1. Click "+Add" | Required: Photo (max 30MB), Name, Description. Status can be set Active or Inactive | High | ⬜⬜⬜⬜ |
| TC-AD-05-025 | Photo upload rejects files larger than 30MB | 1. Upload `{FILE_OVER_30MB}`<br>2. Upload a valid photo *(added)* | Large file is rejected with an error message. Valid photo is accepted | Med | ⬜⬜⬜⬜ |
| TC-AD-05-026 | A new category is created after filling all required fields | 1. Fill in all fields<br>2. Save | New category appears in the list | High | ⬜⬜⬜⬜ |
| TC-AD-05-027 | "Sort" reorders categories by drag and drop | 1. Click "Sort"<br>2. Drag a category to a new position<br>3. Save the order | New order is saved and reflected on the Home page positions | Med | ⬜⬜⬜⬜ |
| TC-AD-05-028 | The search field filters categories by name | 1. Enter a category name | Correct results appear | Med | ⬜⬜⬜⬜ |