# Bug Reports

Defects found in the iTaskApp project are logged here. Each report links to the test case or requirement it relates to.

## Defect Summary
| Total | Critical | Major | Minor | Trivial | Open | Closed |
|:-----:|:--------:|:-----:|:-----:|:-------:|:----:|:------:|
| 5 | 0 | 2 | 2 | 1 | 5 | 0 |

## Requirement Defects (found in a requirements review)
These were found while turning the user story into test cases. They are not application bugs.

| ID | Title | Severity | Priority | Related test case | Status |
|----|-------|----------|----------|-------------------|--------|
| [DOC-001](./DOC-001-shortcut-delete-message-undefined.md) | Shortcut delete message shows "Undefined" | Trivial | Low | TC-AD-06-020, TC-NB-04-017 | Open |
| [DOC-002](./DOC-002-section-numbering-mismatch.md) | Section numbers differ between contents and body | Minor | Low | Traceability | Open |
| [DOC-003](./DOC-003-user-roles-inconsistent.md) | Four user types but eight roles | Major | Medium | TC-AD-02-006 | Open |
| [DOC-004](./DOC-004-itasker-menu-messages-option.md) | iTasker menu described with and without Messages | Minor | Medium | TC-IT-07-001 | Open |
| [DOC-005](./DOC-005-team-minimum-vs-solo-itasker.md) | Team needs a worker, but an iTasker can work alone | Major | High | TC-IT-03-015 | Open |

## Application Defects (found during test execution)
| ID | Title | Severity | Priority | Test case | Status |
|----|-------|----------|----------|-----------|--------|
| – | – | – | – | – | – |

## Process
1. Execute a test case. If the actual result differs from the expected one, mark it ❌.
2. Log the defect in Jira and create a report from the [template](./bug-report-template.md).
3. Link the test case and the requirement section.
4. Retest after the fix. Close the defect or reopen it.

Severity and priority definitions are in the [test plan](../01-Documentation/test-plan.md).

*Practice defect reports from a separate project on a public demo shop are in [Project-Demoblaze](../../Project-Demoblaze/Bug-Reports/). They are not part of iTaskApp.*