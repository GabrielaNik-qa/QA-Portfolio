# Requirements Traceability

Each requirement section of the user story is mapped to the acceptance criteria it contains and to the test cases that verify them. This shows what is covered, what is not, and what has been executed.

## Traceability matrices
| Role | Matrix | Requirements | ✅ Covered | ⚠️ Partial |
|------|--------|:------------:|:---------:|:----------:|
| Client | [RTM-Client](./RTM-Client.md) | 13 | 12 | 1 |
| iTasker | [RTM-iTasker](./RTM-iTasker.md) | 20 | 18 | 2 |
| Admin | [RTM-Admin](./RTM-Admin.md) | 21 | 20 | 1 |
| Neighbourhood | [RTM-Neighbourhood](./RTM-Neighbourhood.md) | 8 | 3 | 5 |
| **Total** | | **62** | **53** | **9** |

## How to read a matrix
- **Requirement:** section number from the [user story index](../01-Documentation/user-story-index.md).
- **Acceptance criteria:** the key rules stated in that section.
- **Test cases:** the IDs that verify them.
- **Coverage:** ✅ covered, ⚠️ partially covered, ❌ not covered.
- **Execution:** the status of the linked cases after a run.
