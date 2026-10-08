# DOC-005: A team needs at least one worker, but an iTasker can work alone

| Field | Details |
|-------|---------|
| **ID** | DOC-005 |
| **Type** | Requirement defect (found in a requirements review, not in the application) |
| **Severity / Priority** | Major / High |
| **Status** | Open, waiting for the product owner |
| **Requirement** | User Story 2.2.3 and 2.3.3.3 (Teams) |
| **Related test cases** | TC-IT-03-015, TC-AD-03-017, TC-IT-04-013 |
| **Open question** | 6 |
| **Reported by** | Gabriela Nikolova |

## Description
The story says that each team needs at least one worker and one service. It also says that an iTasker can work alone without workers, and that a default team is created with the account. An iTasker without an approved team cannot see or apply for tasks.

## Expected
A clear rule for how a solo iTasker gets a team that can take tasks.

## Impact on testing
The expected result for creating a team without workers, and for solo iTaskers, cannot be decided. The core flow of applying for tasks depends on it.

## Suggested resolution
State whether the default team counts as a team without workers, or whether a solo iTasker is their own worker.