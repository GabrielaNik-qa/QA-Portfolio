# Test Plan - iTaskApp

| Field | Details |
|-------|---------|
| **Product** | iTaskApp web platform (Client, iTasker, Admin, Neighbourhood) |
| **Author** | Gabriela Nikolova |
| **Requirements** | User Story iTaskApp Feb/26, Neighbourhood Intern Feb/25 |


## 1. Objective
- Verify that the platform behaves as the user story describes for every role.


## 2. Scope
| In scope | Out of scope |
|----------|--------------|
| Registration and sign-in, task lifecycle, teams, invoicing flow, notifications, chat, admin management, Neighbourhood | Performance, security testing, automation, native mobile apps |

## 3. Approach (agile)
- **Refinement:** each user story section is reviewed for testability. 
- **Acceptance criteria:** every requirement gets test cases that verify its acceptance criteria (see the traceability matrices).
- **Risk-based priority:** High, Med, Low
- **Test cycle per sprint:** smoke tests on every build, then new and changed story cases, then regression at sprint end.
- **Techniques:** BVA, EP, positive and negative cases, cross-role testing.
- **Feedback:** defects are logged in Jira and retested after each fix. Results are shared at the sprint review.

## 4. Test types
Functional, integration (payment provider, email, SMS and push notifications), regression, UI and visual checks against the user story, cross-browser.

## 5. Environments and platforms
| Item | Details |
|------|---------|
| Application | [iTaskApp](https://itask.com/about/itasker) |
| Browsers | Chrome, Firefox, Edge (latest) |
| Mobile | Edge Device emulator |
| Environment | Test |

## 6. Test accounts and data
Client, iTasker and Admin test accounts, a dedicated test mailbox, a test payment card. See [02-Test-Cases](../02-Test-Cases/README.md).

## 7. Defect management
| Severity | Meaning |
|----------|---------|
| Critical | Core flow is blocked or data is lost (for example a task cannot be paid) |
| Major | Important feature is wrong, with no workaround |
| Minor | Feature works but with a problem or a workaround exists |
| Trivial | Cosmetic or wording issue |

**Workflow:** New → Open → Fixed → Retest → Closed (or Reopened). 

## 8. Deliverables
[Documentation](./README.md) · [Test cases](../02-Test-Cases/) · [Traceability](../05-Traceability/) · [Execution reports](../03-Test-Execution/) · [Bug reports](../04-Bug-Reports/)