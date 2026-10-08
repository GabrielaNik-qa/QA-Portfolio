# Requirements Traceability Matrix: iTasker

**Source:** User Story iTaskApp Feb/26, section 2.2 | **Cases:** 134 

**Coverage:** ✅ covered | ❌ not covered
**Execution:** | ✅ all passed | ❌ failures | ⚠️ blocked

| Section | Requirement | Key acceptance criteria | Test cases | Coverage | Exec |
|---------|-------------|-------------------------|------------|:--------:|:----:|
| 2.2.1 | iTasker registration | Same fields as Client plus Main Service Category and Business Name, email with password | TC-IT-01-001 to 009 | ✅ | ⬜ |
| 2.2.2 | iTasker sign in and onboarding | First login requires the profile, later logins skip it, steps 1-4, Stripe, My Services | TC-IT-01-010 to 020, TC-IT-02-001 to 004 | ✅ | ⬜ |
| 2.2.3 | Team creation (flow) | Default team exists, +Add, 5 steps, name, services, workers, working area, completion | TC-IT-03-004, TC-IT-03-007 to 018 | ✅ | ⬜ |
| 2.2.4 | Applying for tasks | Taskboard shows only offered services, Details, change day and hour, success message | TC-IT-04-001 to 010 | ❌ | ⬜ |
| 2.2.5 | Assign a task to own team | Assign a Team, inactive without an approved team | TC-IT-04-011 to 013 | ✅ | ⬜ |
| 2.2.6 | Change day/time of an accepted task | Change Appointment from Active Tasks, client notified | TC-IT-04-014 to 016 | ✅ | ⬜ |
| 2.2.7 | Change status of an accepted task | On Route, On Site, On Materials Pick up, Completed, client notified | TC-IT-04-017, 018 | ✅ | ⬜ |
| 2.2.8 | Chat iTasker - Client | Only after assignment, Private and Group chats, send message, New Chat | TC-IT-06-006 to 010 | ✅ | ⬜ |
| 2.2.9 | Edit business information | Company - Profile - Edit, saved changes | TC-IT-02-005 to 007 | ✅ | ⬜ |
| 2.2.10 | Team creation (menu and completion) | Company menu, Teams, Create Team, saved details | TC-IT-03-001 to 003, TC-IT-03-019 to 023 | ✅ | ⬜ |
| 2.2.11 | Edit and remove team members | Members list, View, Edit, Remove with confirmation | TC-IT-03-024 to 034 | ✅ | ⬜ |
| 2.2.12 | Edit and remove teams | Edit name and details, delete with confirmation | TC-IT-03-035 to 037 | ✅ | ⬜ |
| 2.2.13 | Generate invoice for a task | Invoice flow with up to 3 rejections and the status of task, invoice and payment | TC-IT-05-001 to 009 | ✅ | ⬜ |
| 2.2.14 | Access invoices | Company - Finance, history, filter, Options, PDF | TC-IT-05-010 to 016 | ✅ | ⬜ |
| 2.2.15 | Task details linked to invoice | Task information, See Details, See Invoice Details, Activity | TC-IT-05-017 to 024 | ✅ | ⬜ |
| 2.2.16 | iTasker notifications | Bell, unread counter, mark as read, view one by one | TC-IT-06-001 to 005 | ✅ | ⬜ |
| 2.2.17.1 | Profile | Edit personal data, password, address, category, read-only business info | TC-IT-07-001 to 008 | ✅ | ⬜ |
| 2.2.17.2 | Preferences | 9 notification groups with their toggles | TC-IT-07-009 to 017 | ❌ | ⬜ |
| 2.2.17.3 | Messages | Chat between iTasker and Client (described in 2.2.8) | TC-IT-06-007, 009, 010 | ✅ | ⬜ |
| 2.2.17.4 | Log out | Redirect to Home page without a session | TC-IT-07-018 | ✅ | ⬜ |

## Summary
| Requirements | ✅ Covered | ❌ Not covered |
|:------------:|:---------:|:--------------:|
| 20 | 18 | 2 | 