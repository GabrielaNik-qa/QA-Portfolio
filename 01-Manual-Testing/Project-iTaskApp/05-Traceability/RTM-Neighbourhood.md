# Requirements Traceability Matrix: Neighbourhood

**Source:** Neighbourhood Intern Feb/25 | **Cases:** 78 

**Coverage:** ✅ covered | ❌ not covered<br>
**Execution:** | ✅ all passed | ❌ failures | ⚠️ blocked

| Section | Requirement | Key acceptance criteria | Test cases | Coverage | Exec |
|---------|-------------|-------------------------|------------|:--------:|:----:|
| NB-1 | Group list: filters and search | Filters by visibility, membership and status, search by name | TC-NB-01-001 to 005 | ✅ | ⬜ |
| NB-2 | Adding groups | Required fields incl. photo, 30MB photo limit, Private and Hidden toggles, optional location, Create saves | TC-NB-01-006 to 014, TC-NB-01-021 | ✅ | ⬜ |
| NB-3 | Editing, deleting and sharing groups | Edit with the same fields, Danger Zone delete, share to 4 platforms, copy link | TC-NB-01-015 to 020 | ❌ | ⬜ |
| NB-4 | Shortcuts submenu | 9 columns, View, Edit, Active/Inactive, Delete with confirmation, Add, Sort with Confirmation, search | TC-NB-04-011 to 025 | ❌ | ⬜ |
| NB-5 | Discussions tab | Default tab, post popup, photo and link, Private and Hidden post, Post | TC-NB-02-001 to 010 | ❌ | ⬜ |
| NB-6 | Events tab | Event creation with all fields, 30MB photo limit, Private, Hidden and Pin toggles, options menu | TC-NB-03-001 to 021 | ❌ | ⬜ |
| NB-7 | Members tab | Member list and status, copy profile link, block, delete membership request | TC-NB-04-001 to 006, TC-NB-04-026 | ❌ | ⬜ |
| NB-8 | Right sidebar calendar | Current month, event dates in bold red circles, click opens the event and its group | TC-NB-04-007 to 010 | ✅ | ⬜ |

## Summary
| Requirements | ✅ Covered | ❌ Not covered |
|:------------:|:---------:|:--------------:|
| 8 | 3 | 5 | 

## Coverage gaps and notes
- **NB-3:** the document does not say whether deleting a group asks for confirmation (open question 12).
- **NB-4:** the delete message shows "Undefined" in the document (open question 9).
- **NB-5 and NB-6:** the document does not say which post and event fields are mandatory (open question 11).
- **NB-7:** the member status values and the approval of membership requests are not described (open question 13).
