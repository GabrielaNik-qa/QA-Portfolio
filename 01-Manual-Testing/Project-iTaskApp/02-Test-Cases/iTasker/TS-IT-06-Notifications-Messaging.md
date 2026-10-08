# TS-IT-06: Notifications & Messaging

| Field | Details |
|-------|---------|
| **Suite ID** | TS-IT-06 |
| **Role** | iTasker |
| **Priority** | Medium |
| **Type** | Functional |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.2.8 and 2.2.16 |

## Objective
Verify the in-app notification bell and the chat between iTasker and Client.

## Preconditions
- iTasker is logged in
- A Client account with an assigned task is available

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-IT-06.1 | Notifications (bell) | 2.2.16 | 001-005 |
| SC-IT-06.2 | Chat with Client | 2.2.8 | 006-010 |

---

## SC-IT-06.1 Notifications (bell)

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-06-001 | Bell icon is visible in the header | 1. Log in | Icon is visible in the header menu | Med | ⬜⬜⬜⬜ |
| TC-IT-06-002 | Clicking the bell opens the notifications list | 1. Click the bell | List opens | Med | ⬜⬜⬜⬜ |
| TC-IT-06-003 | Unread count is displayed on the bell | 1. Trigger a new notification | The counter above the bell updates | Med | ⬜⬜⬜⬜ |
| TC-IT-06-004 | Clicking a notification marks it as read | 1. Click a notification | It is marked read and the counter decreases | Med | ⬜⬜⬜⬜ |
| TC-IT-06-005 | Notifications can be viewed one by one | 1. Open notifications one at a time | Each opens separately | Low | ⬜⬜⬜⬜ |

## SC-IT-06.2 Chat with Client

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-IT-06-006 | Chat is available only after the iTasker is assigned to a task | 1. Check the chat option before assignment<br>2. Check after | Not available before assignment. Available after | High | ⬜⬜⬜⬜ |
| TC-IT-06-007 | Messages page shows Private and Group chats | 1. Click "Messages" | Both types are listed | Med | ⬜⬜⬜⬜ |
| TC-IT-06-008 | Chat displays title and participant names | 1. Open a chat | Title and participant names are shown | Med | ⬜⬜⬜⬜ |
| TC-IT-06-009 | Text input and "Send" are functional | Send: `Hello, I am on my way to complete your task.` | Message is sent and shown in the conversation | High | ⬜⬜⬜⬜ |
| TC-IT-06-010 | "New Chat" allows selecting participants | 1. Click "New Chat" | Participants can be selected | Med | ⬜⬜⬜⬜ |

> The three "Messages" cases in the profile section of the source sheet repeat TC-IT-06-007, 009 and 010, so they are merged.