# TS-NB-02: Discussions

| Field | Details |
|-------|---------|
| **Suite ID** | TS-NB-02 |
| **Role** | Admin |
| **Priority** | Medium |
| **Type** | Functional, Negative |
| **Documentation** | Neighbourhood Intern Feb/25, section NB-5 |

## Objective
Verify that an Admin can create posts in a group, with photos, links and the Private and Hidden options.

## Preconditions
- Logged in as Admin
- A group exists, with at least one member and one user who is not a member

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-NB-02.1 | Discussions tab and post creation | NB-5 | 001-010 |

---

## SC-NB-02.1 Discussions tab and post creation

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-NB-02-001 | "Discussions" is the default tab when a group opens | 1. Open a group | Discussions tab is loaded first | Med | ⬜⬜⬜⬜ |
| TC-NB-02-002 | The "Write something" field is clickable and opens the post popup | 1. Click anywhere in the field | The popup appears | High | ⬜⬜⬜⬜ |
| TC-NB-02-003 | The popup has all fields | 1. Open the popup | "What is in your mind" (text), "Add to your post" (photo and link), Private Post toggle, Hidden Post toggle, Post button | High | ⬜⬜⬜⬜ |
| TC-NB-02-004 | "What is in your mind" accepts text | Enter: `Test post for neighbourhood group` | Text is accepted | High | ⬜⬜⬜⬜ |
| TC-NB-02-005 | "Add to your post" allows attaching a photo | Upload a valid image | The photo is attached to the post | Med | ⬜⬜⬜⬜ |
| TC-NB-02-006 | "Add to your post" allows attaching a link | 1. Add a link | The link is attached to the post | Med | ⬜⬜⬜⬜ |
| TC-NB-02-007 | "Private Post" shows the post only to group members | 1. Publish a post with the toggle ON<br>2. Log in as a non-member | The post is not visible to the non-member. Members see it | High | ⬜⬜⬜⬜ |
| TC-NB-02-008 | "Hidden Post" shows the post only to the Admin | 1. Publish a post with the toggle ON<br>2. Log in as a member and as a Client | The post is visible only to the Admin | High | ⬜⬜⬜⬜ |
| TC-NB-02-009 | "Post" publishes the post in the group | 1. Click "Post" | The post appears in the Discussions tab | High | ⬜⬜⬜⬜ |
| TC-NB-02-010 | A post cannot be submitted without text | 1. Leave the text empty<br>2. Click "Post" |  post is not published | Med | ⬜⬜⬜⬜ |