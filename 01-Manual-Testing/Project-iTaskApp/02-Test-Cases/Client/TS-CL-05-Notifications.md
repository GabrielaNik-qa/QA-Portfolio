# TS-CL-05: Notifications

| Field | Details |
|-------|---------|
| **Suite ID** | TS-CL-05 |
| **Role** | Client (receiver), iTasker (trigger) |
| **Priority** | Medium |
| **Type** | Functional, Integration, State-based (toggle ON/OFF) |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.1.6.2 and 2.1.8 |

## Objective
Verify that notifications reach the Client through the channels enabled in Preferences (Email, Push, Sound, SMS) and that nothing is sent when a channel is OFF. Also verify the in-app bell.

## Preconditions
- Client and iTasker test accounts exist, with an accepted task between them
- Client is logged in on a mobile device with push enabled (Push and SMS cases)
- Client's phone number is linked to the account (SMS cases)
- Access to the `{CLIENT_EMAIL}` inbox

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-CL-05.1 | Chat message notifications (group: Chat messages receiving) | 2.1.6.2 | 001-006 |
| SC-CL-05.2 | Task appointment change notifications | 2.1.6.2 | 007-012 |
| SC-CL-05.3 | Task status change notifications | 2.1.6.2 | 013-018 |
| SC-CL-05.4 | New follow up task notifications | 2.1.6.2 | 019-022 |
| SC-CL-05.5 | Finance (invoice) notifications | 2.1.6.2 | 023-030 |
| SC-CL-05.6 | In-app notifications (bell) | 2.1.8 | 031-036 |
| SC-CL-05.7 | Task Suggestion notifications | 2.1.6.2 | 037-040 |

---

## SC-CL-05.1 Chat message notifications

**Trigger:** iTasker sends a chat message to the Client.

| ID | Test Case | Steps | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------|-----------------|-----|:------------------:|
| TC-CL-05-001 | Email ON: Client receives an email | 1. Client: Email ON, Save<br>2. iTasker: send a chat message<br>3. Check `{CLIENT_EMAIL}` | Email notification arrives | Med | ⬜⬜⬜⬜ |
| TC-CL-05-002 | Email OFF: no email | 1. Client: Email OFF, Save<br>2. iTasker: send a message<br>3. Check inbox | No email arrives | Med | ⬜⬜⬜⬜ |
| TC-CL-05-003 | Push ON: Client receives a Push on mobile | 1. Client: Push ON, Save<br>2. iTasker: send a message | Push notification appears on the mobile | Med | ⬜⬜⬜⬜ |
| TC-CL-05-004 | Push OFF: no Push | 1. Client: Push OFF, Save<br>2. iTasker: send a message | No Push notification | Med | ⬜⬜⬜⬜ |
| TC-CL-05-005 | Push-Alert Sound ON: Push plays a sound | 1. Client: Push and Sound ON, Save<br>2. iTasker: send a message | Push arrives with sound | Low | ⬜⬜⬜⬜ |
| TC-CL-05-006 | Push-Alert Sound OFF: Push is silent | 1. Client: Push ON, Sound OFF, Save<br>2. iTasker: send a message | Push arrives without sound | Low | ⬜⬜⬜⬜ |

## SC-CL-05.2 Task appointment change notifications

**Trigger:** iTasker changes the agreed date or time of an accepted task.

| ID | Test Case | Steps | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------|-----------------|-----|:------------------:|
| TC-CL-05-007 | Email ON: Client receives an email | 1. Client: Email ON, Save<br>2. iTasker: change the date/time<br>3. Check inbox | Email arrives | Med | ⬜⬜⬜⬜ |
| TC-CL-05-008 | Email OFF: no email | 1. Client: Email OFF, Save<br>2. iTasker: change the date/time<br>3. Check inbox | No email arrives | Med | ⬜⬜⬜⬜ |
| TC-CL-05-009 | Push ON: Client receives a Push | 1. Client: Push ON, Save<br>2. iTasker: change the date/time | Push appears on the mobile | Med | ⬜⬜⬜⬜ |
| TC-CL-05-010 | Push OFF: no Push | 1. Client: Push OFF, Save<br>2. iTasker: change the date/time | No Push notification | Med | ⬜⬜⬜⬜ |
| TC-CL-05-011 | Push-Alert Sound ON: Push plays a sound | 1. Client: Push and Sound ON, Save<br>2. iTasker: change the date/time | Push arrives with sound | Low | ⬜⬜⬜⬜ |
| TC-CL-05-012 | Push-Alert Sound OFF: Push is silent | 1. Client: Push ON, Sound OFF, Save<br>2. iTasker: change the date/time | Push arrives without sound | Low | ⬜⬜⬜⬜ |

## SC-CL-05.3 Task status change notifications

**Trigger:** iTasker changes the status of an accepted task. 

| ID | Test Case | Steps | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------|-----------------|-----|:------------------:|
| TC-CL-05-013 | Push ON: Client receives a Push | 1. Client: Push ON, Save<br>2. iTasker: change the task status | Push appears on the mobile | Med | ⬜⬜⬜⬜ |
| TC-CL-05-014 | Push OFF: no Push | 1. Client: Push OFF, Save<br>2. iTasker: change the task status | No Push notification | Med | ⬜⬜⬜⬜ |
| TC-CL-05-015 | Push-Alert Sound ON: Push plays a sound | 1. Client: Push and Sound ON, Save<br>2. iTasker: change the status | Push arrives with sound | Low | ⬜⬜⬜⬜ |
| TC-CL-05-016 | Push-Alert Sound OFF: Push is silent | 1. Client: Push ON, Sound OFF, Save<br>2. iTasker: change the status | Push arrives without sound | Low | ⬜⬜⬜⬜ |
| TC-CL-05-017 | SMS ON: Client receives an SMS | 1. Client: SMS ON, Save<br>2. iTasker: change the agreed time<br>3. Check the phone | SMS arrives on the linked phone number | Med | ⬜⬜⬜⬜ |
| TC-CL-05-018 | SMS OFF: no SMS | 1. Client: SMS OFF, Save<br>2. iTasker: change the agreed time | No SMS is received | Med | ⬜⬜⬜⬜ |

## SC-CL-05.4 New follow up task notifications

**Trigger:** iTasker creates a Follow up task for the Client.

| ID | Test Case | Steps | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------|-----------------|-----|:------------------:|
| TC-CL-05-019 | Push ON: Client receives a Push | 1. Client: Push ON, Save<br>2. iTasker: create a Follow up task | Push appears | Med | ⬜⬜⬜⬜ |
| TC-CL-05-020 | Push OFF: no Push | 1. Client: Push OFF, Save<br>2. iTasker: create a Follow up task | No Push notification | Med | ⬜⬜⬜⬜ |
| TC-CL-05-021 | Push-Alert Sound ON: Push plays a sound | 1. Client: Push and Sound ON, Save<br>2. iTasker: create a Follow up task | Push arrives with sound | Low | ⬜⬜⬜⬜ |
| TC-CL-05-022 | Push-Alert Sound OFF: Push is silent | 1. Client: Push ON, Sound OFF, Save<br>2. iTasker: create a Follow up task | Push arrives without sound | Low | ⬜⬜⬜⬜ |

## SC-CL-05.5 Finance (invoice) notifications

**Trigger:** iTasker creates or updates an invoice.

| ID | Test Case | Steps | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------|-----------------|-----|:------------------:|
| TC-CL-05-023 | Email ON: email when an invoice is created | 1. Client: Email ON, Save<br>2. iTasker: generate and send an invoice for a completed task<br>3. Check inbox | Email arrives | Med | ⬜⬜⬜⬜ |
| TC-CL-05-024 | Email ON: email when an invoice is updated | 1. Client: Email ON, Save<br>2. iTasker: modify and resend an invoice<br>3. Check inbox | Email arrives | Med | ⬜⬜⬜⬜ |
| TC-CL-05-025 | Email OFF: no email on create or update | 1. Client: Email OFF, Save<br>2. iTasker: create/update an invoice<br>3. Check inbox | No email arrives | Med | ⬜⬜⬜⬜ |
| TC-CL-05-026 | Push ON: Push when an invoice is created | 1. Client: Push ON, Save<br>2. iTasker: send an invoice | Push appears | Med | ⬜⬜⬜⬜ |
| TC-CL-05-027 | Push ON: Push when an invoice is updated | 1. Client: Push ON, Save<br>2. iTasker: modify and resend an invoice | Push appears | Med | ⬜⬜⬜⬜ |
| TC-CL-05-028 | Push OFF: no Push on create or update | 1. Client: Push OFF, Save<br>2. iTasker: create/update an invoice | No Push notification | Med | ⬜⬜⬜⬜ |
| TC-CL-05-029 | Push-Alert Sound ON: Push plays a sound | 1. Client: Push and Sound ON, Save<br>2. iTasker: create/update an invoice | Push arrives with sound | Low | ⬜⬜⬜⬜ |
| TC-CL-05-030 | Push-Alert Sound OFF: Push is silent | 1. Client: Push ON, Sound OFF, Save<br>2. iTasker: create/update an invoice | Push arrives without sound | Low | ⬜⬜⬜⬜ |

## SC-CL-05.6 In-app notifications (bell)

| ID | Test Case | Steps | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------|-----------------|-----|:------------------:|
| TC-CL-05-031 | Bell icon is visible in the header | 1. Log in | Bell icon is visible in the header menu | Med | ⬜⬜⬜⬜ |
| TC-CL-05-032 | Clicking the bell opens the notification dropdown | 1. Click the bell | Dropdown with notifications opens | Med | ⬜⬜⬜⬜ |
| TC-CL-05-033 | Notification appears when an iTasker applies for a task | 1. iTasker: apply for the Client's task<br>2. Client: open the bell | New notification is listed | High | ⬜⬜⬜⬜ |
| TC-CL-05-034 | Notification appears when an iTasker changes the task status | 1. iTasker: change the status<br>2. Client: open the bell | New notification is listed | High | ⬜⬜⬜⬜ |
| TC-CL-05-035 | Notification appears when an iTasker sends an invoice | 1. iTasker: send an invoice<br>2. Client: open the bell | New notification is listed | High | ⬜⬜⬜⬜ |
| TC-CL-05-036 | Each notification links to the relevant task or invoice page | 1. Click each notification type | The correct task or invoice page opens | High | ⬜⬜⬜⬜ |

## SC-CL-05.7 Task Suggestion notifications

**Trigger:** an iTasker applies for the Client's task.

| ID | Test Case | Steps | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------|-----------------|-----|:------------------:|
| TC-CL-05-037 | Push ON: Client receives a Push | 1. Client: Push ON, Save<br>2. iTasker: apply for the Client's task | Push appears on the mobile | Med | ⬜⬜⬜⬜ |
| TC-CL-05-038 | Push OFF: no Push | 1. Client: Push OFF, Save<br>2. iTasker: apply for the task | No Push notification | Med | ⬜⬜⬜⬜ |
| TC-CL-05-039 | Push-Alert Sound ON: Push plays a sound | 1. Client: Push and Sound ON, Save<br>2. iTasker: apply | Push arrives with sound | Low | ⬜⬜⬜⬜ |
| TC-CL-05-040 | Push-Alert Sound OFF: Push is silent | 1. Client: Push ON, Sound OFF, Save<br>2. iTasker: apply | Push arrives without sound | Low | ⬜⬜⬜⬜ |