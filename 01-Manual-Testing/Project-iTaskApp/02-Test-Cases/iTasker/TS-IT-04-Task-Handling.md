# TS-IT-04: Applying, Assigning, Appointment & Status

| Field | Details |
|-------|---------|
| **Suite ID** | TS-IT-04 |
| **Role** | iTasker (Client observes) |
| **Priority** | High |
| **Type** | Functional, Negative, Integration |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.2.4, 2.2.5, 2.2.6, 2.2.7 |

## Objective
Verify that an iTasker can find and apply for tasks, assign them to a team, change the appointment, and update the status.

## Preconditions
- iTasker is logged in and has an approved team
- A Client account has an open task for a service the iTasker offers

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-IT-04.1 | Browse and apply for tasks | 2.2.4 | 001-010 |
| SC-IT-04.2 | Assign a task to own team | 2.2.5 | 011-013 |
| SC-IT-04.3 | Change day/time of an accepted task | 2.2.6 | 014-016 |
| SC-IT-04.4 | Change task status | 2.2.7 | 017-018 |

---

## SC-IT-04.1 Browse and apply for tasks

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-04-001 | iTasker can browse available tasks | 1. Open the Taskboard | Only tasks for services the iTasker offers are listed. Tasks of other services are not visible | High | ⬜⬜⬜⬜ |
| TC-IT-04-002 | Task information is visible before applying | 1. Check a task | Details, price and location are shown | High | ⬜⬜⬜⬜ |
| TC-IT-04-003 | iTasker can apply for a task | 1. Apply for an available task | Application is registered | High | ⬜⬜⬜⬜ |
| TC-IT-04-004 | Taskboard has all visual elements from the user story | 1. Compare the page with the story | Elements match | Med | ⬜⬜⬜⬜ |
| TC-IT-04-005 | "Details" opens the Task Details window | 1. Click "Details" | Window opens with the task details | High | ⬜⬜⬜⬜ |
| TC-IT-04-006 | Task Details has all visual elements from the user story | 1. Compare the window with the story | Elements match | Med | ⬜⬜⬜⬜ |
| TC-IT-04-007 | iTasker can change the day and hour when applying | 1. Select another day and time slot | New values are accepted | High | ⬜⬜⬜⬜ |
| TC-IT-04-008 | Calendar works for present and future dates | Select today, then a future date | Both are selectable. Past dates are not *(confirm in the story, open question 3)* | High | ⬜⬜⬜⬜ |
| TC-IT-04-009 | Applying without accepting the Terms and Conditions | 1. Leave Terms unchecked<br>2. Apply | ⚠️ The story is silent (open question 5). Expected until confirmed: application is blocked with a message | High | ⬜⬜⬜⬜ |
| TC-IT-04-010 | iTasker is notified of a successful application after clicking "Yes" | 1. Confirm the application | A message confirms the application was successful. This is the last step of applying | High | ⬜⬜⬜⬜ |

## SC-IT-04.2 Assign a task to own team

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-04-011 | iTasker can assign an accepted task to their own team | 1. Select an accepted task<br>2. Click "Assign a Team"<br>3. Select a team | Task is assigned to the selected team | High | ⬜⬜⬜⬜ |
| TC-IT-04-012 | Team members are selectable from the existing team list | 1. Open the selector | All teams and their members appear | Med | ⬜⬜⬜⬜ |
| TC-IT-04-013 | "Assign a Team" is inactive when the iTasker has no created or approved team | 1. Log in with an iTasker without an approved team | The button is inactive. New tasks are not visible and the iTasker cannot apply for them | Med | ⬜⬜⬜⬜ |

## SC-IT-04.3 Change day/time of an accepted task

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-04-014 | iTasker can change the scheduled date | 1. Open a task in Active Tasks<br>2. Click "Change Appointment"<br>3. Pick a future date | Date is changed | High | ⬜⬜⬜⬜ |
| TC-IT-04-015 | iTasker can change the scheduled time | Change from 8-10AM to 2-4PM | Time slot is changed | High | ⬜⬜⬜⬜ |
| TC-IT-04-016 | Client receives a notification when date/time is changed | 1. Check the Client account after the change | Notification is shown | High | ⬜⬜⬜⬜ |

## SC-IT-04.4 Change task status

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-04-017 | iTasker can change the status of an accepted task | Go through: On Route, On Site, On Materials Pick up, Completed | Each status can be set and is displayed | High | ⬜⬜⬜⬜ |
| TC-IT-04-018 | Client receives a notification for each status change | 1. Check the Client account after each change | A notification arrives for every change | High | ⬜⬜⬜⬜ |