# Requirements Traceability Matrix: Client

**Source:** User Story iTaskApp Feb/26, section 2.1 | **Cases:** 141 (all mapped)

**Coverage:** ✅ covered | ⚠️ partially covered or open question | ❌ not covered
**Execution:** ⬜ not run | ✅ all passed | ❌ failures | ⚠️ blocked

| Section | Requirement | Key acceptance criteria | Test cases | Coverage | Exec |
|---------|-------------|-------------------------|------------|:--------:|:----:|
| 2.1.1 | Client registration | Form fields and limits (names 2-255, email, +1 phone), all fields mandatory, confirmation email | TC-CL-01-001 to 012 | ✅ | ⬜ |
| 2.1.2 | Client sign in | Email 5+ chars with "@", password 8+ chars, Continue opens the Dashboard, forgot password flow | TC-CL-01-013 to 019 | ✅ | ⬜ |
| 2.1.3 | Task creation | 4 steps, 3 task types, photos (max 3, 30MB), 8 time slots, review and change, card payment, cancel task | TC-CL-02-001 to 030 | ✅ | ⬜ |
| 2.1.4 | Rating a completed task | Only on Completed tasks, satisfied or disappointed, optional text | TC-CL-03-001 to 006 | ✅ | ⬜ |
| 2.1.5 | Reporting a problem | Button, modal with description and photo, submit sends the report | TC-CL-03-007 to 013 | ⚠️ | ⬜ |
| 2.1.6.1 | Profile | Edit personal data, address, change password | TC-CL-04-001 to 007 | ✅ | ⬜ |
| 2.1.6.2 | Preferences | 6 notification groups with their toggles, saved state, delivery by Email, Push, Sound, SMS | TC-CL-04-008 to 016, TC-CL-05-001 to 030, TC-CL-05-037 to 040 | ✅ | ⬜ |
| 2.1.6.3 | Chat Client - iTasker | Private and Group chats, send message, New Chat limited to iTaskers worked with | TC-CL-06-001 to 005 | ✅ | ⬜ |
| 2.1.6.4 | Log out | Redirect to Home page without a session | TC-CL-01-020 | ✅ | ⬜ |
| 2.1.7 | Client invoices | Finance with Invoices and Quotes tabs, filter by status | TC-CL-07-001 to 004 | ✅ | ⬜ |
| 2.1.7.1 | Invoice details | Task, payment and invoice statuses, Reference of 10 symbols, Issued at, Last updated, Billing at | TC-CL-07-005 to 012 | ✅ | ⬜ |
| 2.1.7.2 | Task details linked to invoice | Task information, See Details, Rate and Review, Activity | TC-CL-07-013 to 017 | ✅ | ⬜ |
| 2.1.8 | Client notifications | Bell, dropdown, 3 notification types, each links to the task or invoice | TC-CL-05-031 to 036 | ✅ | ⬜ |

## Summary
| Requirements | ✅ Covered | ⚠️ Partial | ❌ Not covered |
|:------------:|:---------:|:----------:|:--------------:|
| 13 | 12 | 1 | 0 |

## Coverage gaps and notes
- **2.1.5:** the story does not say whether the description is mandatory (open question 1).
- **2.1.2:** no negative sign-in cases (wrong password, unregistered email). Candidates for a later update.
- **2.1.3:** only the "Pay per Task" flow is tested through payment. Pay by Hour and Free Quote are only checked at Step 1.
- **2.1.3:** the header items Discount Club, Connections and Blog are checked for presence only.