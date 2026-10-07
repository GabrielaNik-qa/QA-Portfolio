# TS-CL-02: Task Creation & Dashboard

| Field | Details |
|-------|---------|
| **Suite ID** | TS-CL-02 |
| **Role** | Client |
| **Priority** | High (core business flow) |
| **Type** | Functional, Negative, Boundary, Integration (payment) |
| **Documentation** | User Story iTaskApp Feb/26, section 2.1.3 |

## Objective
Verify that a Client can navigate the Dashboard, create a task through the 4-step flow, pay, and cancel the task.

## Preconditions
- Client account exists and is logged in
- Test card is available (`{TEST_CARD}`)

## Scenarios

| ID | Scenario | Story section | TCs |
|----|----------|:-------------:|-----|
| SC-CL-02.1 | Header and Dashboard | 2.1.3 | 001-008 |
| SC-CL-02.2 | Service selection | 2.1.3 | 009-010 |
| SC-CL-02.3 | Step 1: Select Task Type | 2.1.3 | 011-013 |
| SC-CL-02.4 | Step 2: Task Detail | 2.1.3 | 014-016 |
| SC-CL-02.5 | Step 3: Time & Place | 2.1.3 | 017-021 |
| SC-CL-02.6 | Step 4: Review and Confirm | 2.1.3 | 022-024 |
| SC-CL-02.7 | Payment | 2.1.3 | 025-028 |
| SC-CL-02.8 | After creation | 2.1.3 | 029-030 |

---

## SC-CL-02.1 Header and Dashboard

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-02-001 | Header displays all menu items | 1. Log in | Header shows: Dashboard, Discount Club, Finance, Messages, Connections, Blog, +Create Task | High | ⬜⬜⬜⬜ |
| TC-CL-02-002 | "Dashboard" is visible in the sidebar and active only when logged in | 1. Log in and check the sidebar<br>2. Log out and check again | Logged in: button is visible and active. Logged out: button is inactive or hidden | High | ⬜⬜⬜⬜ |
| TC-CL-02-003 | Dashboard displays sections Active, Requests, Closed | 1. Open the Dashboard | All 3 sections are displayed | High | ⬜⬜⬜⬜ |
| TC-CL-02-004 | Active section lists new tasks with no iTasker assigned | 1. Open "Active" | List shows new tasks with no iTasker assigned | High | ⬜⬜⬜⬜ |
| TC-CL-02-005 | Requests section lists tasks with an assigned, approved iTasker and work in progress | 1. Open "Requests" | List shows tasks where an iTasker is assigned and approved and work is in progress | High | ⬜⬜⬜⬜ |
| TC-CL-02-006 | Closed section lists finished or cancelled tasks | 1. Open "Closed" | List shows finished and cancelled tasks | High | ⬜⬜⬜⬜ |
| TC-CL-02-007 | "New Task" button is visible in the top right of the Dashboard | 1. Open the Dashboard | Button is visible in the top right corner | Med | ⬜⬜⬜⬜ |
| TC-CL-02-008 | "New Task" redirects to "Select a Service from Categories" | 1. Click "New Task" | "Select a Service from Categories" page opens | High | ⬜⬜⬜⬜ |

## SC-CL-02.2 Service selection

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-02-009 | Client can select a service category and subcategory | 1. Select any available category<br>2. Select a subcategory | Category and subcategory are selected and the flow continues | High | ⬜⬜⬜⬜ |
| TC-CL-02-010 | Task creation flow contains 4 steps | 1. Proceed through the flow | Steps: Select Task Type, Task Detail, Time & Place, Review and Confirm | High | ⬜⬜⬜⬜ |

## SC-CL-02.3 Step 1: Select Task Type

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-02-011 | "Pay per Task (Book Now)" is available with details and cost | 1. Reach Step 1 | Option is displayed with task details and cost, and is selectable | High | ⬜⬜⬜⬜ |
| TC-CL-02-012 | "Pay by Hour (Start a Request)" is available with details and cost | 1. Reach Step 1 | Option is displayed with task details and cost, and is selectable | High | ⬜⬜⬜⬜ |
| TC-CL-02-013 | "Free Quote (Get a Quote)" is available with details and cost | 1. Reach Step 1 | Option is displayed with task details and cost, and is selectable | High | ⬜⬜⬜⬜ |

## SC-CL-02.4 Step 2: Task Detail

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-02-014 | Task details text field is mandatory | 1. Leave the description empty<br>2. Click "Continue" | User cannot continue. A validation message is shown | High | ⬜⬜⬜⬜ |
| TC-CL-02-015 | Photo upload: max 3 photos, max 30MB, formats png/jpg/svg/webp | 1. Upload 3 valid photos<br>2. Upload a 4th photo<br>3. Upload a `.pdf`<br>4. Upload `{FILE_OVER_30MB}`<br>5. Upload one file of each valid format *(added)* | 3 valid photos are accepted. The 4th, the PDF and the over-30MB file are rejected with a message | High | ⬜⬜⬜⬜ |
| TC-CL-02-016 | "Continue" navigates to the next step | 1. Fill in the description<br>2. Click "Continue" | Step 3 (Time & Place) opens | High | ⬜⬜⬜⬜ |

## SC-CL-02.5 Step 3: Time & Place

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-02-017 | Calendar allows date selection | 1. Select today's date<br>2. Select a future date | Both dates are selectable. Past dates are not selectable *(confirm in the story, open question 3)* | High | ⬜⬜⬜⬜ |
| TC-CL-02-018 | All 8 time range slots are selectable and required after choosing a date | Test each: 8-10AM, 10AM-12PM, 12-2PM, 2-4PM, 4-6PM, 6-8PM, 8-10PM, 10PM-12AM | Every slot is selectable. Continue is not possible without a slot | High | ⬜⬜⬜⬜ |
| TC-CL-02-019 | Address field and Map button are available and the map loads | 1. Check the Address field<br>2. Click the Map button | Address field is present. Map loads correctly | Med | ⬜⬜⬜⬜ |
| TC-CL-02-020 | Zip/Postal code field is available | 1. Check the Step 3 form | Field is present and accepts input | Med | ⬜⬜⬜⬜ |
| TC-CL-02-021 | Special instructions field accepts text | 1. Enter text in the field | Text is accepted | Low | ⬜⬜⬜⬜ |

## SC-CL-02.6 Step 4: Review and Confirm

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-02-022 | Review page displays all previously entered details | 1. Complete Steps 1-3<br>2. Open Step 4 | All entered data is displayed correctly | High | ⬜⬜⬜⬜ |
| TC-CL-02-023 | "Change" returns to the correct step | 1. Click "Change" on each section | Each button opens the matching step for editing | Med | ⬜⬜⬜⬜ |
| TC-CL-02-024 | Changes made in a previous step are applied on the Review page | 1. Click "Change" on the time slot<br>2. Select a different slot<br>3. Return to Step 4 | Review page shows the updated slot | High | ⬜⬜⬜⬜ |

## SC-CL-02.7 Payment

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-02-025 | "Complete Request" opens the Credit Card Confirmation modal | 1. Click "Complete Request" on Step 4 | Credit Card Confirmation modal opens | High | ⬜⬜⬜⬜ |
| TC-CL-02-026 | Credit Card modal contains PAN, Exp. date and CVC fields | PAN: `4242 4242 4242 4242`, Exp: any future date, CVC: `123` | All 3 fields are present and accept the test data | High | ⬜⬜⬜⬜ |
| TC-CL-02-027 | "Pay Now" charges 1 CAD and confirms the task | 1. Enter `{TEST_CARD}`<br>2. Click "Pay Now" | 1 CAD is charged and the task is confirmed | High | ⬜⬜⬜⬜ |
| TC-CL-02-028 | "Cancel" closes the modal without submitting | 1. Click "Cancel" in the modal | Modal closes. No payment is made and no task is created | High | ⬜⬜⬜⬜ |

## SC-CL-02.8 After creation

| ID | Test Case | Steps / Test Data | Expected Result | Pri | Ch · FF · Ed · Mob |
|----|-----------|-------------------|-----------------|-----|:------------------:|
| TC-CL-02-029 | Task details page is displayed after successful creation | **Pre:** TC-CL-02-027 passed | Task details page opens with the entered information | High | ⬜⬜⬜⬜ |
| TC-CL-02-030 | "Cancel Task" is available and cancels the task | 1. Click "Cancel Task" on the task details page<br>2. Confirm if asked<br>3. Open "Closed" on the Dashboard | Task is cancelled and appears in "Closed" | High | ⬜⬜⬜⬜ |