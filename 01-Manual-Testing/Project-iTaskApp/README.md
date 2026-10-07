# iTaskApp - Manual Testing Project

## 📌 Overview
iTaskApp is a multi-role web platform where **Clients** post tasks, **iTaskers** (contractors and their teams) apply and complete them, and **Admins** manage users, finances and content. A community module called **Neighbourhood** adds groups, discussions and events.

| Item | Details |
|------|---------|
| **Company** | iTaskApp Inc. (Toronto, Canada) |
| **My Role** | QA Engineer Intern |
| **Testing Type** | Manual: functional, integration, regression, UI |
| **Platforms** | Chrome, Firefox, Edge, Mobile |
| **Requirements** | User Story iTaskApp Feb/26 and Neighbourhood Intern Feb/25 (see [Documentation](./01-Documentation/)) |
| **Tools** | Excel, Jira, Confluence, Git |

## 🌐 Application Under Test
| Item | Details |
|------|---------|
| **Application** | iTaskApp web platform |
| **URL** | [iTasker](https://itask.com/about/itasker) |
| **Access** | Test accounts are not published in this repository |
| **Screenshots** | [01-Documentation/screenshots](./01-Documentation/screenshots/) |

## 🎯 Scope
**In scope:** registration and sign-in, task lifecycle, teams, invoicing flow, notifications, chat, admin management, Neighbourhood groups, events and members.
**Out of scope:** performance, security testing, automation.

## 🔄 Agile Approach
- User story sections are reviewed for testability, and unclear points become open questions for the product owner.
- Every requirement is mapped to test cases that verify its acceptance criteria ([traceability](./05-Traceability/)).
- Smoke tests run on every build, new and changed stories are tested next, and regression runs at the end of each sprint.
- Details are in the [test plan](./01-Documentation/test-plan.md).

## 🧪 Techniques
Boundary Value Analysis (BVA), Equivalence Partitioning (EP), positive and negative testing, state-based testing (toggles, invoice statuses), cross-role testing, requirement-based review of the user story.

## 📂 Structure
| Folder | Content |
|--------|---------|
| [01-Documentation](./01-Documentation/) | Test plan, requirement summary, user story index, open questions, screenshots |
| [02-Test-Cases](./02-Test-Cases/) | Test suites, scenarios and test cases per role, smoke and regression suites |
| [03-Test-Execution](./03-Test-Execution/) | Execution report template |
| [04-Bug-Reports](./04-Bug-Reports/) | Defect process, bug report template and index |
| [05-Traceability](./05-Traceability/) | Requirement to test case mapping |

## 📊 Coverage
| Role / Module | Suites | Test Cases |
|---------------|:------:|:----------:|
| [Client](./02-Test-Cases/Client/) | 7 | 141 |
| [iTasker](./02-Test-Cases/iTasker/) | 7 | 134 |
| [Admin](./02-Test-Cases/Admin/) | 8 | 192 |
| [Neighbourhood](./02-Test-Cases/Neighbourhood/) | 4 | 78 |
| **Total** | **26** | **545** |
