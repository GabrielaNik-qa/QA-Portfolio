# Demoblaze - Test Cases

**Source:** FSD "My Account" (Feb 2026) | **Tester:** Gabriela Nikolova | **Site:** https://www.demoblaze.com/

## Index

| Suite | Module | Test cases |
|-------|--------|:----------:|
| [TS-DM-01](./TS-DM-01-Login.md) | Login | 18 |
| [TS-DM-02](./TS-DM-02-Registration.md) | Sign up | 41 |
| | **Total** | **59** |

49 cases come from the original Excel (`MA_LGN_001-016`, `MA_RGR_001-033`). 10 are new, marked *(added)*.

## Conventions
**Priority:** High = core flow, Medium = important, Low = cosmetic.
**Status:** ⬜ not run | ✅ pass | ❌ fail | ⚠️ blocked
**Source:** the part of the specification the case verifies. ⚠️ means the specification does not say, so the expected result is an assumption (see [Requirements](../Requirements/README.md)).
**Messages:** MSG-1 to MSG-5 are defined in [Requirements](../Requirements/README.md).
**Screen sizes:** XL, L, M, S as in the specification.

## Test data

| Key | Value |
|-----|-------|
| `validUsername`, `validUsername1`, `validUsername2`, `validUsername3` | Usernames created during the run |
| `validPass1!` | Valid password (8+ characters, upper, lower, digit, symbol) |
| `validPassword1!` | Valid password used for username tests |

## Data dependencies (read before running)
- The site is public and accounts stay forever, so a username may already be taken. Add a number or the date to each username (for example `validUsername_0810`) and use the same value in the dependent cases.
- Run `MA_RGR_010` before `MA_RGR_011` and `MA_LGN_010` to `015`, because they need an existing user.
- `MA_RGR_019` creates `validUsername2`, which `MA_RGR_013` to `017` and `034` to `037` expect not to exist. Run those first, or use a new username.
- `MA_RGR_022` (`username`) and `MA_RGR_023` (`USERNAME`) can collide if usernames are not case-sensitive (see `MA_RGR_040`).

## Corrections made to the original Excel

| Case | Issue | In this version |
|------|-------|-----------------|
| MA_LGN_016 | Step 3 says click "Log in", but the case checks the "Close" button | Step uses "Close" |
| MA_LGN_010 | Message says "Welcome `<Name>`" | "Welcome, `<name>`" as in the specification |
| MA_LGN_011 to 013 | Message has a comma after "Моля", the specification does not | Specification wording |
| MA_RGR_025 to 032 | Expected "Error message is displayed" without text | Marked ⚠️, message not defined (gaps D1, D4) |