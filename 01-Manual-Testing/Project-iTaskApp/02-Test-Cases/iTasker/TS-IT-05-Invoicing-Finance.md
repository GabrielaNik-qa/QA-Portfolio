# TS-IT-05: Invoicing & Finance

| Field | Details |
|-------|---------|
| **Suite ID** | TS-IT-05 |
| **Role** | iTasker (Client approves or rejects) |
| **Priority** | High |
| **Type** | Functional, State-based, Integration |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.2.13, 2.2.14, 2.2.15 |

## Objective
Verify the invoice approval and rejection flow with its status transitions, and invoice history, filtering and details.

## Preconditions
- A task is in status "Payment pending" in the iTasker's Active tasks
- A Client account is available to approve or reject invoices

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-IT-05.1 | Invoice flow and status transitions | 2.2.13 | 001-009 |
| SC-IT-05.2 | Access invoices | 2.2.14 | 010-016 |
| SC-IT-05.3 | Task details from invoice | 2.2.15 | 017-024 |

---

## SC-IT-05.1 Invoice flow and status transitions

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-05-001 | iTasker can generate an invoice for a completed task | 1. Open the task<br>2. Generate the invoice | Invoice is created with status New | High | ⬜⬜⬜⬜ |
| TC-IT-05-002 | Invoice is sent to the client for approval | 1. Check the Client account | Invoice appears for the Client | High | ⬜⬜⬜⬜ |
| TC-IT-05-003 | Client approves the invoice | 1. Client approves | Task: Completed. Invoice: Paid | High | ⬜⬜⬜⬜ |
| TC-IT-05-004 | Client rejects the invoice (1st time) | 1. Client rejects | Invoice returns to the iTasker. Task: Disputed (stays in Active tasks). Invoice: Rejected | High | ⬜⬜⬜⬜ |
| TC-IT-05-005 | iTasker revises and resends after the 1st rejection | Change the amount and resend | Invoice is sent again to the Client | High | ⬜⬜⬜⬜ |
| TC-IT-05-006 | Client approves the revised invoice | 1. Client approves | Task: Completed. Invoice: Paid | High | ⬜⬜⬜⬜ |
| TC-IT-05-007 | Client rejects the invoice (2nd time) | 1. Client rejects the revised invoice | Task: Disputed. Invoice: New. It returns to the iTasker | High | ⬜⬜⬜⬜ |
| TC-IT-05-008 | iTasker resends after the 2nd rejection, with or without changes | Test both: unchanged, and with an updated amount | Both are sent to the Client for the 3rd time | High | ⬜⬜⬜⬜ |
| TC-IT-05-009 | Client rejects the invoice (3rd time) | 1. Client rejects again | Task: Suspend and the money is held. Payment: Reserved. Invoice: Suspend | High | ⬜⬜⬜⬜ |

## SC-IT-05.2 Access invoices

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-05-010 | "Finance" is accessible via the Company menu | 1. Click Company, then Finance | Finance page opens | High | ⬜⬜⬜⬜ |
| TC-IT-05-011 | Finance page displays the invoice history | 1. Open the page | History is listed | High | ⬜⬜⬜⬜ |
| TC-IT-05-012 | "Filter" filters invoices by status | Test: New, Rejected, Approved, Paid, Failed, Refund, Suspend | Only invoices with the selected status are shown | High | ⬜⬜⬜⬜ |
| TC-IT-05-013 | Each invoice has an "Options" button | 1. Check each row | Button is present | Med | ⬜⬜⬜⬜ |
| TC-IT-05-014 | Options - invoice details opens correctly | 1. Options, then invoice details | Invoice details page opens | High | ⬜⬜⬜⬜ |
| TC-IT-05-015 | Options - task details opens correctly | 1. Options, then task details | Linked task details open | High | ⬜⬜⬜⬜ |
| TC-IT-05-016 | Invoice can be opened and saved as PDF | 1. Open the invoice<br>2. Save as PDF | PDF is saved and its content is correct | Med | ⬜⬜⬜⬜ |

## SC-IT-05.3 Task details from invoice

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-05-017 | Options - "Task Details" opens the Task Details page | 1. Options, then Task Details | Page opens | High | ⬜⬜⬜⬜ |
| TC-IT-05-018 | Task status, service name, creation date and task type are displayed | 1. Check the page | All 4 are shown | Med | ⬜⬜⬜⬜ |
| TC-IT-05-019 | Job details, special instructions and photos are displayed | 1. Check the page | All are shown | Med | ⬜⬜⬜⬜ |
| TC-IT-05-020 | Client info panel and message button are displayed | 1. Check the page | Both are shown | Med | ⬜⬜⬜⬜ |
| TC-IT-05-021 | Service price, address and scheduled date/time are displayed | 1. Check the page | All are shown | Med | ⬜⬜⬜⬜ |
| TC-IT-05-022 | "See Details" navigates to Task Requests | 1. Click "See Details" | Task Requests page opens with the iTaskers who applied for this task | Med | ⬜⬜⬜⬜ |
| TC-IT-05-023 | "See Invoice Details" navigates to Task Invoice | 1. Click the button | Task Invoice page opens with the invoice information | Med | ⬜⬜⬜⬜ |
| TC-IT-05-024 | Activity section shows all task phases | 1. Open Activity | The task's activity is listed | Med | ⬜⬜⬜⬜ |