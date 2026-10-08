# DOC-002: Section numbers differ between the table of contents and the body

| Field | Details |
|-------|---------|
| **ID** | DOC-002 |
| **Type** | Requirement defect (found in a requirements review, not in the application) |
| **Severity / Priority** | Minor / Low |
| **Status** | Open, waiting for the product owner |
| **Requirement** | User Story 2.3.3 (Manage menu) |
| **Related test cases** | All Admin suites (traceability) |
| **Open question** | 7 |
| **Reported by** | Gabriela Nikolova |

## Description
The table of contents and the body of the user story number some sections differently. For example, Shortcuts is 2.3.3.11 in the contents but 2.3.3.9 in the body.

## Expected
One consistent numbering across the document.

## Impact on testing
Traceability links can point to the wrong requirement, and review comments can be misread.

## Workaround used
The traceability matrices use the section numbers of the body.

## Suggested resolution
Update the table of contents so that it matches the body, or the reverse.