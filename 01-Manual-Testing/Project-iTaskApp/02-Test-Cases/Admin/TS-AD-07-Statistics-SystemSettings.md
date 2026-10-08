# TS-AD-07: Statistics & System Settings

| Field | Details |
|-------|---------|
| **Suite ID** | TS-AD-07 |
| **Role** | Admin |
| **Priority** | Medium |
| **Type** | Functional, UI, Configuration |
| **Documentation** | User Story iTaskApp Feb/26, sections 2.3.3.11 and 2.3.3.12 |

## Objective
Verify that visit statistics are shown correctly and that an Admin can change and save system settings: features, e-mail and SMTP, fees, applications and pages.

## Preconditions
- Logged in as Admin
- Visits by registered users and guests exist
- Original setting values are noted before testing, so they can be restored

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-AD-07.1 | Statistics | 2.3.3.11 | 001-006 |
| SC-AD-07.2 | System Settings: features, SMTP, fees, e-mail | 2.3.3.12 | 007-011 |
| SC-AD-07.3 | System Settings: applications, pages, saving | 2.3.3.12 | 012-018 |

---

## SC-AD-07.1 Statistics

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-07-001 | "Statistics" opens the statistics page | 1. Manage - Statistics | Page opens | Med | ⬜⬜⬜⬜ |
| TC-AD-07-002 | All columns are visible | 1. Check the table header | ID, Service, User, Postal Code, City, Step, IP, Referrer, Created, Updated | Med | ⬜⬜⬜⬜ |
| TC-AD-07-003 | Statistics show both registered users and guests | 1. Visit the booking flow logged in and logged out<br>2. Check the page | Both kinds of visits are listed | Med | ⬜⬜⬜⬜ |
| TC-AD-07-004 | "Step" shows the step reached in the service booking flow | 1. Start a booking and stop at a known step<br>2. Check the row | Step matches the last step reached | Med | ⬜⬜⬜⬜ |
| TC-AD-07-005 | "Referrer" shows the source site when applicable | 1. Open the app from a link on another site (for example a social network)<br>2. Check the row | Referrer shows the source | Low | ⬜⬜⬜⬜ |
| TC-AD-07-006 | The filter field searches and filters results | 1. Enter a search term | Matching rows are shown | Med | ⬜⬜⬜⬜ |

## SC-AD-07.2 System Settings: features, SMTP, fees, e-mail

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-07-007 | "System Settings" opens with all sections | 1. Manage - System Settings | Sections: Features, E-mail & SMTP, Applications, Pages | High | ⬜⬜⬜⬜ |
| TC-AD-07-008 | Admin can enable and disable the Features options | Toggle each ON and OFF, then Save: Skip Invoice Approving Flow By Clients, Set Dashboard/Task Board as Columns, Homepage Shortcuts, Homepage App Stores | Each change is saved and takes effect | High | ⬜⬜⬜⬜ |
| TC-AD-07-009 | Admin can update the SMTP settings | Update: Hostname, SMTP Port, SMTP Encrypt type, Authentication Username, Authentication Password, then Save | Changes are saved. The password is not shown in plain text | High | ⬜⬜⬜⬜ |
| TC-AD-07-010 | Admin can update all fee settings | Update one value at a time, then Save: Regular task fee, Follow up task fee, Related Clients fee, Client card confirmation, Client first task discount, iTasker quote application fee, Credit card processing fee | Each change is saved and used in new calculations | High | ⬜⬜⬜⬜ |
| TC-AD-07-011 | Admin can update the e-mail settings | Update: Mail Delivery Sender E-mail, Mail Delivery Sender Name, Contact Us Form Receiver E-mail, Contact Us Form Receiver Name, then Save | Changes are saved. A test e-mail uses the new sender | Med | ⬜⬜⬜⬜ |

## SC-AD-07.3 System Settings: applications, pages, saving

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-AD-07-012 | Admin can enable and disable the Applications options | Toggle each ON and OFF, then Save: Show Apps Chooser Page (non-Native/Web), Show Apps Chooser Screen (Native) | Each change is saved | Med | ⬜⬜⬜⬜ |
| TC-AD-07-013 | "New App" opens a form and a new app can be added | Fill in: Link, Title, App Title, Image (preferably SVG), then Save | New app is added and shown | Med | ⬜⬜⬜⬜ |
| TC-AD-07-014 | Admin can add new links in Pages via "+ New Link" | 1. Click "+ New Link"<br>2. Fill in and Save | New link appears in the list | Med | ⬜⬜⬜⬜ |
| TC-AD-07-015 | Admin can delete existing links in Pages | 1. Delete a link<br>2. Save | Link no longer appears | Med | ⬜⬜⬜⬜ |
| TC-AD-07-016 | "About Pages" contains About us, Terms and Conditions, Privacy Policy | 1. Open the "About Pages" subsection | All 3 entries are present | Low | ⬜⬜⬜⬜ |
| TC-AD-07-017 | "How to book a service" contains its 4 fields | 1. Open the subsection | Page, Button Label or Link Title, Short Steps, Email for new Clients | Low | ⬜⬜⬜⬜ |
| TC-AD-07-018 | "Save" saves all changes in each section, and nothing is saved without it | 1. In each section change a setting<br>2. Navigate away without saving | Changes are not kept | High | ⬜⬜⬜⬜ |