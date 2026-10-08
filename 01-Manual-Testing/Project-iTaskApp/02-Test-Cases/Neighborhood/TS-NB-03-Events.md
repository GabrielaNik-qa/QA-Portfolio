# TS-NB-03: Events

| Field | Details |
|-------|---------|
| **Suite ID** | TS-NB-03 |
| **Role** | Admin |
| **Priority** | Medium |
| **Type** | Functional, Negative, UI |
| **Documentation** | Neighbourhood Intern Feb/25, section NB-6 |

## Objective
Verify that an Admin can create events in a group with all their options, and manage them from the event menu.

## Preconditions
- Logged in as Admin
- A group exists, with a Client account and a non-member available
- At least one event with a confirmed participant exists

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-NB-03.1 | Events tab and creating an event | NB-6 | 001-015 |
| SC-NB-03.2 | Event options menu | NB-6 | 016-021 |

---

## SC-NB-03.1 Events tab and creating an event

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-NB-03-001 | The "Events" tab shows all created events | 1. Open the Events tab | All events of the group are listed | High | ⬜⬜⬜⬜ |
| TC-NB-03-002 | The "Create an event" field is clickable and opens the Add event popup | 1. Click anywhere in the field | The popup opens | High | ⬜⬜⬜⬜ |
| TC-NB-03-003 | The Add event popup has all fields | 1. Open the popup | Event name, Description, Date (calendar), Hour, Event URL, Location (map and search), Photo, Private Event, Hidden Event, Pin Event | High | ⬜⬜⬜⬜ |
| TC-NB-03-004 | Event name is mandatory | 1. Leave the name empty<br>2. Click "Create" | ⚠️ The document does not say which fields are mandatory (open question 11). Expected until confirmed: the event is not created | Med | ⬜⬜⬜⬜ |
| TC-NB-03-005 | The Date field opens a calendar | 1. Click the Date field | A calendar opens and a date can be selected | High | ⬜⬜⬜⬜ |
| TC-NB-03-006 | The Hour field accepts a time | Enter `14:00` | The time is accepted | Med | ⬜⬜⬜⬜ |
| TC-NB-03-007 | Event URL allows adding several URLs with "+" | 1. Add 2 URLs | Both are listed | Low | ⬜⬜⬜⬜ |
| TC-NB-03-008 | Event URL entries can be deleted with the delete icon | 1. Delete one entry | The entry is removed | Low | ⬜⬜⬜⬜ |
| TC-NB-03-009 | Location has a map and a search field | Enter `123 Main St, Toronto, ON` | The location is shown on the map | Med | ⬜⬜⬜⬜ |
| TC-NB-03-010 | Photo upload accepts files up to 30MB | 1. Upload a valid photo close to 30MB | The photo is accepted | Med | ⬜⬜⬜⬜ |
| TC-NB-03-011 | Photo upload rejects files larger than 30MB | 1. Upload `{FILE_OVER_30MB}` | An error message appears | Med | ⬜⬜⬜⬜ |
| TC-NB-03-012 | "Private Event" shows the event only to members | 1. Create an event with the toggle ON<br>2. Log in as a non-member | The event is not visible to non-members | High | ⬜⬜⬜⬜ |
| TC-NB-03-013 | "Hidden Event" shows the event only to the Admin | 1. Create an event with the toggle ON<br>2. Log in as a Client | The event is not visible to the Client. The Admin sees it | High | ⬜⬜⬜⬜ |
| TC-NB-03-014 | "Pin Event" is visible only to the Admin | 1. Open the popup as Admin<br>2. Open it as a non-Admin | The toggle is shown only to the Admin | Med | ⬜⬜⬜⬜ |
| TC-NB-03-015 | "Create" saves the event and it appears in the Events tab | 1. Fill in the fields<br>2. Click "Create" | The event appears in the Events tab | High | ⬜⬜⬜⬜ |

## SC-NB-03.2 Event options menu

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-NB-03-016 | Each event has an additional options menu | 1. Open the menu on an event | All 5 options are present: copy link, see participants, hide, edit, delete | Med | ⬜⬜⬜⬜ |
| TC-NB-03-017 | "Copy link" copies the event link | 1. Click "Copy link"<br>2. Paste it in the browser | The correct event opens | Low | ⬜⬜⬜⬜ |
| TC-NB-03-018 | "See participants" shows the users who confirmed attendance | 1. Click "See participants" | The users who confirmed attendance are listed | Med | ⬜⬜⬜⬜ |
| TC-NB-03-019 | "Hide event" hides the event | 1. Click "Hide event" | The event is hidden from the list | Med | ⬜⬜⬜⬜ |
| TC-NB-03-020 | "Edit event" opens the form with all existing data pre-filled | 1. Click "Edit event"<br>2. Change the event name<br>3. Save | The form is pre-filled. The change is saved | High | ⬜⬜⬜⬜ |
| TC-NB-03-021 | "Delete event" removes the event | 1. Click "Delete event" | The event no longer appears in the Events tab | High | ⬜⬜⬜⬜ |