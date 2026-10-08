# DOC-003: The specification lists four user types but eight roles

| Field | Details |
|-------|---------|
| **ID** | DOC-003 |
| **Type** | Requirement defect (found in a requirements review, not in the application) |
| **Severity / Priority** | Major / Medium |
| **Status** | Open, waiting for the product owner |
| **Requirement** | User Story 2.3.3.1 (Users) and 2.3.3.2 (Workers) |
| **Related test cases** | TC-AD-02-006 |
| **Open question** | 8 |
| **Reported by** | Gabriela Nikolova |

## Description
The Users section says the system has four user types: Client, iTasker, Admin and Worker. The Role filter lists eight roles: Client, iTasker, Worker, Admin, Manager, Operator, Paymaster and Support. The Workers section says that a Worker is not a role.

## Expected
One clear definition of the roles, with the permissions of each.

## Impact on testing
Permissions of Manager, Operator, Paymaster and Support are not defined, so they cannot be tested. It is also unclear whether Worker is a role.

## Suggested resolution
List the roles, say which can sign in, and describe what each one can do.