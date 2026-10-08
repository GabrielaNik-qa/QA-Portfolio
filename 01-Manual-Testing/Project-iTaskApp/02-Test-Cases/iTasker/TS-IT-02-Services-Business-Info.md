# TS-IT-02: Services & Business Info

| Field | Details |
|-------|---------|
| **Suite ID** | TS-IT-02 |
| **Role** | iTasker |
| **Priority** | Medium |
| **Type** | Functional |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.2.2 and 2.2.9 |

## Objective
Verify that an iTasker can manage offered services and edit business information.

## Preconditions
- iTasker is logged in with a completed profile

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-IT-02.1 | My Services | 2.2.2 | 001-004 |
| SC-IT-02.2 | Business info | 2.2.9 | 005-007 |

---

## SC-IT-02.1 My Services

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-02-001 | "My Services" is accessible from the profile | 1. Navigate to My Services | Page loads correctly | High | ⬜⬜⬜⬜ |
| TC-IT-02-002 | iTasker can view the currently offered services | 1. Open My Services | All previously added services are listed | High | ⬜⬜⬜⬜ |
| TC-IT-02-003 | iTasker can add a new service | 1. Add a service<br>2. Save | Service appears in the list | High | ⬜⬜⬜⬜ |
| TC-IT-02-004 | iTasker can edit an existing service | 1. Edit a service<br>2. Save | Changes are saved and shown | Med | ⬜⬜⬜⬜ |

## SC-IT-02.2 Business info

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-02-005 | iTasker can access business info via Company - Profile | 1. Click Company, then Profile | Business info page opens | High | ⬜⬜⬜⬜ |
| TC-IT-02-006 | iTasker can edit the business activity information | 1. Update a field<br>2. Click "Save changes" | Change is accepted | High | ⬜⬜⬜⬜ |
| TC-IT-02-007 | Saved business data is updated | 1. After saving, reload and reopen the page | Updated data is displayed | High | ⬜⬜⬜⬜ |