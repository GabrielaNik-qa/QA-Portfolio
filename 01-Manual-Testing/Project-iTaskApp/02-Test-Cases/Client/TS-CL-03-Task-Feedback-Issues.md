# TS-CL-03: Task Feedback & Problem Reporting

| Field | Details |
|-------|---------|
| **Suite ID** | TS-CL-03 |
| **Role** | Client |
| **Priority** | Medium |
| **Type** | Functional, UI, Negative |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.1.4 and 2.1.5 |

## Objective
Verify that a Client can rate completed tasks and report problems with a task.

## Preconditions
- Client is logged in
- At least one Completed task and one Active task exist

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-CL-03.1 | Rate a completed task | 2.1.4 | 001-006 |
| SC-CL-03.2 | Report a problem | 2.1.5 | 007-013 |

---

## SC-CL-03.1 Rate a completed task

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-03-001 | Rating is available only for tasks with status "Completed" | 1. Open an Active task<br>2. Open a Requests task<br>3. Open a Completed task | Active and Requests tasks show no rating option. Completed tasks do | High | ⬜⬜⬜⬜ |
| TC-CL-03-002 | "Rate & Write a Review" opens the rating window | 1. Open a Completed task<br>2. Click "Rate & Write a Review" | Rating window opens | High | ⬜⬜⬜⬜ |
| TC-CL-03-003 | Visual elements are present and positioned as in the user story | 1. Open the rating window<br>2. Compare it with the user story | All elements are present and positioned correctly | Med | ⬜⬜⬜⬜ |
| TC-CL-03-004 | Client can select "I'm satisfied" | 1. Select "I'm satisfied" | Option is selected and highlighted | High | ⬜⬜⬜⬜ |
| TC-CL-03-005 | Client can select "I'm disappointed" | 1. Select "I'm disappointed" | Option is selected and highlighted | High | ⬜⬜⬜⬜ |
| TC-CL-03-006 | Optional feedback field accepts text | 1. Enter: `Great job, very professional and punctual!`<br>2. Submit | Text is accepted and saved. Submitting with an empty field also works | Med | ⬜⬜⬜⬜ |

## SC-CL-03.2 Report a problem

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-03-007 | "Report a Problem" button is available on the Task Details page | 1. Open Task Details | Button is visible | High | ⬜⬜⬜⬜ |
| TC-CL-03-008 | Task Details page meets the visual requirements | 1. Compare the page with the user story | Layout and elements match | Med | ⬜⬜⬜⬜ |
| TC-CL-03-009 | Button opens a modal with description field and photo upload | 1. Click "Report a Problem" | Modal opens with a description field and a photo upload | High | ⬜⬜⬜⬜ |
| TC-CL-03-010 | Description field accepts text | 1. Enter: `The iTasker was late for the appointment.` | Text is accepted | High | ⬜⬜⬜⬜ |
| TC-CL-03-011 | Behaviour when submitting with an empty description | 1. Leave the description empty<br>2. Click "Submit" | ⚠️ The story does not say the description is mandatory (open question 1). Expected until confirmed: validation message and no report sent | High | ⬜⬜⬜⬜ |
| TC-CL-03-012 | Photo upload max 30MB | 1. Upload `{FILE_OVER_30MB}`<br>2. Upload a valid photo *(added)* | File over 30MB is rejected with a message. Valid photo is accepted | Med | ⬜⬜⬜⬜ |
| TC-CL-03-013 | "Submit" sends the report and shows a confirmation | 1. Enter: `The iTasker did not complete the full job as agreed.`<br>2. Attach 1 photo<br>3. Click "Submit" | Report is sent, the confirmation message is displayed, and the report reaches the Admin | High | ⬜⬜⬜⬜ |