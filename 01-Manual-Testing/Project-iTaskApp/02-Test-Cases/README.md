# iTaskApp - Test Cases

**Sources:** User Story iTaskApp Feb/26, Neighbourhood Intern Feb/25 | **Tester:** Gabriela Nikolova

## 📚 Index

| Role | Suite | Module | TCs |
|------|-------|--------|:---:|
| Client | [TS-CL-01](./Client/TS-CL-01-Registration-Authentication.md) | Registration & Authentication | 20 |
| Client | [TS-CL-02](./Client/TS-CL-02-Task-Creation.md) | Task Creation & Dashboard | 30 |
| Client | [TS-CL-03](./Client/TS-CL-03-Task-Feedback-Issues.md) | Rating & Problem Reporting | 13 |
| Client | [TS-CL-04](./Client/TS-CL-04-Profile-Preferences.md) | Profile & Preferences | 16 |
| Client | [TS-CL-05](./Client/TS-CL-05-Notifications.md) | Notifications | 40 |
| Client | [TS-CL-06](./Client/TS-CL-06-Messaging.md) | Messaging | 5 |
| Client | [TS-CL-07](./Client/TS-CL-07-Finance-Invoices.md) | Finance & Invoices | 17 |
| iTasker | [TS-IT-01](./iTasker/TS-IT-01-Registration-Onboarding.md) | Registration & Onboarding | 20 |
| iTasker | [TS-IT-02](./iTasker/TS-IT-02-Services-Business-Info.md) | Services & Business Info | 7 |
| iTasker | [TS-IT-03](./iTasker/TS-IT-03-Team-Management.md) | Team Management | 37 |
| iTasker | [TS-IT-04](./iTasker/TS-IT-04-Task-Handling.md) | Applying, Assigning, Appointment, Status | 18 |
| iTasker | [TS-IT-05](./iTasker/TS-IT-05-Invoicing-Finance.md) | Invoicing & Finance | 24 |
| iTasker | [TS-IT-06](./iTasker/TS-IT-06-Notifications-Messaging.md) | Notifications & Messaging | 10 |
| iTasker | [TS-IT-07](./iTasker/TS-IT-07-Profile-Preferences.md) | Profile & Preferences | 18 |
| Admin | [TS-AD-01](./Admin/TS-AD-01-Authentication-MainBoard.md) | Authentication, Main Board & Manage Menu | 15 |
| Admin | [TS-AD-02](./Admin/TS-AD-02-Users-Workers.md) | Users & Workers | 35 |
| Admin | [TS-AD-03](./Admin/TS-AD-03-Teams.md) | Teams | 17 |
| Admin | [TS-AD-04](./Admin/TS-AD-04-PromoCodes-Finances.md) | Promo Codes & Finances | 23 |
| Admin | [TS-AD-05](./Admin/TS-AD-05-Pages-Categories.md) | Pages & Categories | 28 |
| Admin | [TS-AD-06](./Admin/TS-AD-06-Services-Shortcuts-TaskTypes.md) | Services, Shortcuts & Task Types | 34 |
| Admin | [TS-AD-07](./Admin/TS-AD-07-Statistics-SystemSettings.md) | Statistics & System Settings | 18 |
| Admin | [TS-AD-08](./Admin/TS-AD-08-Notifications-Profile-Messages.md) | Notifications, Profile & Messaging | 22 |
| Neighbourhood | [TS-NB-01](./Neighbourhood/TS-NB-01-Groups-Management.md) | Groups Management | 21 |
| Neighbourhood | [TS-NB-02](./Neighbourhood/TS-NB-02-Discussions.md) | Discussions | 10 |
| Neighbourhood | [TS-NB-03](./Neighbourhood/TS-NB-03-Events.md) | Events | 21 |
| Neighbourhood | [TS-NB-04](./Neighbourhood/TS-NB-04-Members-Calendar-Shortcuts.md) | Members, Calendar & Shortcuts | 26 |
| | | **Total** | **545** |


## 🧭 Conventions
- **ID format:** `TC-<role>-<suite>-<number>`, for example `TC-IT-03-014`. 
- **Roles:** CL = Client, IT = iTasker, AD = Admin, NB = Neighbourhood.
- **Priority:** High = core flow or blocker, Med = important feature, Low = cosmetic.
- **Status:** ⬜ Not run | ✅ Pass | ❌ Fail | ⚠️ Blocked
- **Platform column:** `Ch · FF · Ed · Mob` = Chrome, Firefox, Edge, Mobile.

## 🧪 Test Data
| Key | Value |
|-----|-------|
| `{CLIENT_EMAIL}`, `{ITASKER_EMAIL}`, `{ADMIN_EMAIL}` | Dedicated test mailboxes |
| `{PASSWORD}` | `Test1234` (8 characters) |
| `{PHONE}` | `+1-234-567-8901` |
| `{TEST_CARD}` | PAN `4242 4242 4242 4242`, any future expiry, CVC `123` |
| `{FILE_OVER_30MB}` | any file larger than 30MB |