# TS-CL-06: Client-iTasker Messaging

| Field | Details |
|-------|---------|
| **Suite ID** | TS-CL-06 |
| **Role** | Client |
| **Priority** | Medium |
| **Type** | Functional, Negative |
| **Documentation** | User Story iTaskApp Feb/26, section 2.1.6.3 |

## Objective
Verify that a Client can use the chat with iTaskers, with the correct restrictions.

## Preconditions
- Client is logged in
- Client has worked with at least one iTasker and has never worked with another

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-CL-06.1 | Chat page and messaging | 2.1.6.3 | 001-005 |

---

## SC-CL-06.1 Chat page and messaging

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-06-001 | Chat page shows Private and Group chats with title and participant names | 1. Click "Messages" | Both chat types are listed with title and participant names | Med | ⬜⬜⬜⬜ |
| TC-CL-06-002 | Text input and "Send" button are functional | 1. Open a chat<br>2. Send: `Hello, I have a question about my task.` | Message is sent and displayed in the conversation | High | ⬜⬜⬜⬜ |
| TC-CL-06-003 | "New Chat" allows selecting participants | 1. Click "New Chat"<br>2. Select an iTasker | Participant selection works and a chat can be started | Med | ⬜⬜⬜⬜ |
| TC-CL-06-004 | "New Chat" does not allow a chat with an iTasker the Client has not worked with | 1. Click "New Chat"<br>2. Look for an iTasker with no shared task | That iTasker cannot be selected or is not listed | High | ⬜⬜⬜⬜ |
| TC-CL-06-005 | Chat view options in the dropdown menu | 1. Click the box icon<br>2. Check the menu<br>3. Select: only Private; Private + Group; all; none | Menu shows "New Chat" and the options Private, Group and Closed Chats. The list matches each selection | Med | ⬜⬜⬜⬜ |

> The "Log out" case from the chat section of the source sheet is the same as [TC-CL-01-020](./TS-CL-01-Registration-Authentication.md), so the two are merged.