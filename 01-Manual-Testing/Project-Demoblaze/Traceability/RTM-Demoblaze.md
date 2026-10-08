# Requirements Traceability Matrix: Demoblaze

**Source:** FSD "My Account" (Feb 2026) | **Test cases:** 59 (all mapped)

**Coverage:** ✅ covered | ⚠️ partially covered or open gap | **None** = no requirement in the specification

| ID | Requirement | Source | Test cases | Coverage |
|----|-------------|--------|------------|:--------:|
| LGN-1 | Login pop-up opens, and is hidden for logged-in users | FSD 1.1 | MA_LGN_001, 009 | ✅ |
| LGN-2 | Login pop-up elements | FSD 1.2 | MA_LGN_002 | ✅ |
| LGN-3 | Login pop-up on XL, L, M, S screens | FSD 1.2 | MA_LGN_005 to 008 | ✅ |
| LGN-4 | Valid login: home page and "Welcome, `<name>`" | FSD 1.2 (a) | MA_LGN_010 | ✅ |
| LGN-5 | Both fields empty shows a message | FSD 1.2 (b) | MA_LGN_011, 012, 013 | ✅ |
| LGN-6 | Wrong or unknown credentials show a message | FSD 1.2 (c) | MA_LGN_014, 015 | ✅ |
| LGN-7 | Closing the login pop-up | None | MA_LGN_003, 004, 016, 017 | None |
| LGN-8 | Password is masked | None | MA_LGN_018 | None |
| RGR-1 | Sign up pop-up opens | FSD 2.1 | MA_RGR_001 | ✅ |
| RGR-2 | Sign up pop-up elements | FSD 2.1 | MA_RGR_002 | ✅ |
| RGR-3 | Sign up pop-up on XL, L, M, S screens | FSD 2.1 | MA_RGR_003 to 006 | ✅ |
| RGR-4 | Closing with X, Close, or a click outside | FSD 2.1 | MA_RGR_007 to 009, 033 | ✅ |
| RGR-5 | Username and Password are mandatory | FSD 2.1 | MA_RGR_031, 032, 041 | ⚠️ |
| RGR-6 | Password rules: 8-64, Latin only, upper, lower, digit, symbol | FSD 2.1 | MA_RGR_012 to 019, 034 to 037 | ✅ |
| RGR-7 | Valid sign up creates the account and shows the message | FSD 2.1 | MA_RGR_010 | ⚠️ |
| RGR-8 | A taken username shows a message | FSD 2.1 | MA_RGR_011, 040 | ⚠️ |
| RGR-9 | A weak password shows a message | FSD 2.1 | MA_RGR_012 to 017, 034 to 037 | ⚠️ |
| RGR-10 | Username rules | None | MA_RGR_020 to 030, 038, 039 | None |

## Summary
| Requirements | From the FSD | ✅ Covered | ⚠️ Partial | No source |
|:------------:|:------------:|:---------:|:----------:|:---------:|
| 18 | 15 | 11 | 4 | 3 |

## Bug reports and the test cases that found them

| Bug | Test case | Note |
|-----|-----------|------|
| [JQA1-81](../Bug-Reports/JQA1-81-signup-popup-missing-info-text.md) | MA_RGR_002 | Missing informative text |
| [JQA1-82](../Bug-Reports/JQA1-82-signup-accepts-cyrillic-password.md) | MA_RGR_034 | New case, there was none before |
| [JQA1-83](../Bug-Reports/JQA1-83-signup-accepts-cyrillic-username.md) | MA_RGR_029 | Expected result is an assumption (D1) |
| [JQA1-84](../Bug-Reports/JQA1-84-signup-accepts-spaces.md) | MA_RGR_026, MA_RGR_035 | Username part is an assumption (D1) |
| [JQA1-85](../Bug-Reports/JQA1-85-login-wrong-password-message.md) | MA_LGN_015 | Message matches the FSD |

## Gaps
See the specification gaps D1 to D9 in [Requirements](../Requirements/README.md). The biggest is D1: there are no username rules, so 14 test cases and two bug reports rely on assumptions.