# TS-CL-07: Finance & Invoices

| Field | Details |
|-------|---------|
| **Suite ID** | TS-CL-07 |
| **Role** | Client |
| **Priority** | High |
| **Type** | Functional, UI, Data validation |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.1.7, 2.1.7.1, 2.1.7.2 |

## Objective
Verify that a Client can view and filter invoices and quotes and that invoice data and statuses are displayed correctly.

## Preconditions
- Client is logged in
- Invoices exist in different statuses, plus at least one quote

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-CL-07.1 | Finance page and filtering | 2.1.7 | 001-004 |
| SC-CL-07.2 | Invoice data and statuses | 2.1.7.1 | 005-012 |
| SC-CL-07.3 | Invoice actions and details | 2.1.7.2 | 013-017 |

---

## SC-CL-07.1 Finance page and filtering

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-07-001 | "Finance" opens a page with tabs Invoices and Quotes | 1. Click "Finance" in the sidebar | Page opens with both tabs | High | ⬜⬜⬜⬜ |
| TC-CL-07-002 | Invoices tab displays history of invoices and payments | 1. Open the Invoices tab | History is displayed | High | ⬜⬜⬜⬜ |
| TC-CL-07-003 | Quotes tab displays history of all quotes | 1. Open the Quotes tab | History is displayed | Med | ⬜⬜⬜⬜ |
| TC-CL-07-004 | "Filter" filters invoices by status | Test each status: Completed, Disputed, Payment pending, Suspend, Failed | List shows only invoices with the selected status | High | ⬜⬜⬜⬜ |

## SC-CL-07.2 Invoice data and statuses

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-07-005 | Invoice details display all fields | 1. Open an invoice | Task Status, Payment Status, Invoice Status, iTasker, Reference, Issued at, Last updated, Billing at are displayed | High | ⬜⬜⬜⬜ |
| TC-CL-07-006 | Task Status is one of the allowed values | Check each value | Only: Completed, Disputed, Payment pending, Suspend, Failed | Med | ⬜⬜⬜⬜ |
| TC-CL-07-007 | Payment Status is one of the allowed values | Check each value | Only: Received, Reserved, Sent | Med | ⬜⬜⬜⬜ |
| TC-CL-07-008 | Invoice Status is one of the allowed values | Check each value | Only: Paid, Suspend, Approved, Rejected, Failed | Med | ⬜⬜⬜⬜ |
| TC-CL-07-009 | iTasker field contains the iTasker's name | 1. Compare it with the assigned iTasker | Correct name is displayed | Med | ⬜⬜⬜⬜ |
| TC-CL-07-010 | Reference field contains a 10-symbol number | 1. Check the Reference on several invoices | Reference is a number of exactly 10 symbols | Med | ⬜⬜⬜⬜ |
| TC-CL-07-011 | "Issued at" keeps the issue date; "Last updated" changes | 1. Note both fields<br>2. Update the invoice<br>3. Reopen it | Issued at is unchanged. Last updated shows the new date | Low | ⬜⬜⬜⬜ |
| TC-CL-07-012 | "Billing at" shows the payment date | 1. Open a paid invoice | The date on which the payment was made is displayed | Med | ⬜⬜⬜⬜ |

## SC-CL-07.3 Invoice actions and details

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-07-013 | Options - "Task Details" shows full task information | 1. Open Options<br>2. Click "Task Details" | Page shows: task status, service name, date posted, task type, job details, special instructions, photos, iTasker profile panel, and a panel with price, address and date/time | Med | ⬜⬜⬜⬜ |
| TC-CL-07-014 | "See Details" navigates to the invoice details page | 1. On Task Details, click "See Details" | Invoice details page opens | High | ⬜⬜⬜⬜ |
| TC-CL-07-015 | Task Details window meets the visual requirements | 1. Compare the window with the user story | Layout and elements match | Low | ⬜⬜⬜⬜ |
| TC-CL-07-016 | "Rate & Write a Review" is available and functional | 1. Click the button<br>2. Enter: `Excellent service, would recommend!`<br>3. Submit | The rating window opens and the review is submitted successfully | Med | ⬜⬜⬜⬜ |
| TC-CL-07-017 | Activity section shows all task phases | 1. Open the Activity section | All task phases up to completion are listed in order | Med | ⬜⬜⬜⬜ |