# Demoblaze - Test Cases

**Source:** FSD "My Account" (Feb 2026) | **Tester:** Gabriela Nikolova | **Site:** https://www.demoblaze.com/

## Index

| Suite | Module | Test cases |
|-------|--------|:----------:|
| [TS-DM-01](./TS-DM-01-Login.md) | Login | 18 |
| [TS-DM-02](./TS-DM-02-Registration.md) | Sign up | 41 |
| | **Total** | **59** |

## Conventions
- **Priority:** High = core flow, Medium = important, Low = cosmetic.
- **Status:** ⬜ not run | ✅ pass | ❌ fail | ⚠️ blocked
- **Source:** the part of the specification the case verifies. 
- **Screen sizes:** XL, L, M, S as in the specification.

## Test data

| Key | Value |
|-----|-------|
| `validUsername`, `validUsername1`, `validUsername2`, `validUsername3` | Usernames created during the run |
| `validPass1!` | Valid password (8+ characters, upper, lower, digit, symbol) |
| `validPassword1!` | Valid password used for username tests |