# TS-AD-04: Promo Codes & Finances

| Field | Details |
|-------|---------|
| **Suite ID** | TS-AD-04 |
| **Role** | Admin |
| **Priority** | High |
| **Type** | Functional, State-based, Integration (payments) |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.3.3.4 and 2.3.3.5 |

## Objective
Verify that an Admin can manage promo codes (fixed amounts only) and view, search, filter and operate on all invoices in the system.

## Preconditions
- Logged in as Admin
- At least one promo code exists
- Invoices exist in different statuses, including Payment pending, held funds and a paid invoice

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-AD-04.1 | Promo codes: view, edit, delete | 2.3.3.4 | 001-008 |
| SC-AD-04.2 | Promo codes: generate, rules, filter | 2.3.3.4 | 009-012 |
| SC-AD-04.3 | Finances: invoice list and data | 2.3.3.5 | 013-016 |
| SC-AD-04.4 | Finances: options | 2.3.3.5 | 017-021 |
| SC-AD-04.5 | Finances: search and filter | 2.3.3.5 | 022-023 |

---

## SC-AD-04.1 Promo codes: view, edit, delete

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-04-001 | "Promo Codes" opens the promo codes page | 1. Manage - Promo Codes | Page opens with the list of promo codes | High | ⬜⬜⬜⬜ |
| TC-AD-04-002 | Admin can view, edit and delete existing promo codes | 1. Check each row | View, Edit and Delete are available for each code | Med | ⬜⬜⬜⬜ |
| TC-AD-04-003 | "View" opens the promo code details | 1. Click "View" | Page shows Code, Amount CAD, Expired after, Codes Quantity | Med | ⬜⬜⬜⬜ |
| TC-AD-04-004 | "Edit" opens an editable form with the same fields | 1. Click "Edit"<br>2. Update the amount and the expiry date<br>3. Save | Fields are editable and the changes are saved | High | ⬜⬜⬜⬜ |
| TC-AD-04-005 | "Save" saves all changes, and nothing is saved without it | 1. Change a field, navigate away without saving | Change is not kept | High | ⬜⬜⬜⬜ |
| TC-AD-04-006 | "Delete" shows a confirmation | 1. Click "Delete" | Message: Do you want to delete this code "`<code>`"? with Yes and No | High | ⬜⬜⬜⬜ |
| TC-AD-04-007 | "Yes" permanently deletes the promo code | 1. Click "Yes" | Code no longer appears in the list | High | ⬜⬜⬜⬜ |
| TC-AD-04-008 | "No" closes the dialog and the code is not deleted | 1. Click "No" | Dialog closes. Code remains in the list | High | ⬜⬜⬜⬜ |

## SC-AD-04.2 Promo codes: generate, rules, filter

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-04-009 | "Add" opens the Generate Promo Codes page with all fields | 1. Click "Add" | Fields: Number of codes to generate, Amount CAD, Expired after, One code per client, Codes quantity | High | ⬜⬜⬜⬜ |
| TC-AD-04-010 | New promo codes are generated after filling all fields | Amount: `10` CAD, Expiry: any future date, Quantity: `5`<br>1. Save | The codes are generated and shown in the list | High | ⬜⬜⬜⬜ |
| TC-AD-04-011 | Promo codes are fixed amounts only | 1. Check the Add and Edit forms | No option for a percentage value exists | Med | ⬜⬜⬜⬜ |
| TC-AD-04-012 | The filter field searches promo codes by name and amount | 1. Search by code name<br>2. Search by amount | Correct results appear for both | Med | ⬜⬜⬜⬜ |

## SC-AD-04.3 Finances: invoice list and data

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-04-013 | "Finances" opens the invoices page with all invoices in the system | 1. Manage - Finances | Page lists invoices of all clients and iTaskers | High | ⬜⬜⬜⬜ |
| TC-AD-04-014 | A client invoice displays all its fields | 1. Open a client invoice row | Total amount, Received amount, Address, Service category, Task status, Payment status, Invoice status, Client, iTasker, Reference, Issued at, Last updated, Billing at | High | ⬜⬜⬜⬜ |
| TC-AD-04-015 | An iTasker invoice displays all its fields | 1. Open an iTasker invoice row | Total amount, Address, Service category, Task status, Invoice, Client, iTasker, Reference, Issued at, Last updated | High | ⬜⬜⬜⬜ |
| TC-AD-04-016 | "Options" is available for each invoice | 1. Check each row | Button is present for client and iTasker invoices | Med | ⬜⬜⬜⬜ |

## SC-AD-04.4 Finances: options

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-04-017 | Options - "View" opens the Task Details page | 1. Options, then View | Task Details page opens | Med | ⬜⬜⬜⬜ |
| TC-AD-04-018 | Options - "Download Invoice" saves the invoice as PDF | 1. Options, then Download Invoice | PDF file is saved and its content is correct | Med | ⬜⬜⬜⬜ |
| TC-AD-04-019 | Options - "Charge client" is available for eligible invoices and charges the client | 1. Open an invoice with task status Payment pending or Disputed<br>2. Options, then Charge client | Option is available. The client is charged and the status updates | High | ⬜⬜⬜⬜ |
| TC-AD-04-020 | Options - "Release" is available for held funds and releases the payment | 1. Open an invoice with reserved funds<br>2. Options, then Release | Option is available. Payment is released | High | ⬜⬜⬜⬜ |
| TC-AD-04-021 | Options - "Refund" returns a completed payment to the client | 1. Open a paid invoice<br>2. Options, then Refund | Refund is processed and the status updates | High | ⬜⬜⬜⬜ |

## SC-AD-04.5 Finances: search and filter

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-04-022 | The filter field searches invoices by ID, client name or iTasker name | Search by each of the 3 options | Correct results appear for each | Med | ⬜⬜⬜⬜ |
| TC-AD-04-023 | "Filter" filters invoices by status | Test: New, Rejected, Approved, Paid, Failed, Refund, Suspend | Only invoices with the selected status are shown | High | ⬜⬜⬜⬜ |