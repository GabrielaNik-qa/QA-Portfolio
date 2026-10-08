# DOC-001: Shortcut delete message in the specification shows the title "Undefined"

| Field | Details |
|-------|---------|
| **ID** | DOC-001 |
| **Type** | Requirement defect  |
| **Severity / Priority** | Trivial / Low |
| **Status** | Open, waiting for the product owner |
| **Requirement** | User Story 2.3.3.9 and Neighbourhood NB-4 |
| **Related test cases** | TC-AD-06-020, TC-NB-04-017 |
| **Reported by** | Gabriela Nikolova |

## Description
The example confirmation message for deleting a shortcut shows the title "Undefined" in both documents. The Neighbourhood document also describes the same action as deleting a *category*.

## Expected
The documents show the real message with the shortcut's title, for example: Do you want to delete a shortcut "`<shortcut title>`"?

## Impact on testing
The expected result of the delete confirmation cannot be written precisely. Testers could accept a wrong message, or report a defect that does not exist.

## Suggested resolution
Replace the example with a real title and fix the wording in the Neighbourhood document.