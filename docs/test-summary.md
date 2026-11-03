# Test summary

Recorded execution and diagnostics: 2026-11-02. Scope: registration, email confirmation, onboarding, sign-in, username/email validation and focused localization/refresh retests. Environment: isolated local_qa.

## Manual observations

[TC-001–TC-005](traceability.md) retain the observed browser flows and screenshots. They show successful steps and validation failures, but do not provide complete variant-by-variant execution records. No overall manual pass rate is calculated.

## Defects and retests

- BUG-001 and BUG-003: screenshot retests confirm the displayed localization fixes.
- BUG-002: **Partially verified — browser retest pending.** GET diagnostics passed; browser POST replay / refresh remains INCONCLUSIVE. A past tester decision to close the issue is retained as history, not evidence of a complete fix.
- SP-BUG-001/002: separate historical notes; current-version fixes have not been established by this portfolio review.

## Supplemental server checks

| Check | Passed | Failed | Blocked |
|---|---:|---:|---:|
| TC-003 | 4 | 0 | 0 |
| TC-004 | 18 | 0 | 0 |
| TC-005 | 8 | 0 | 2 |
| Total | 30 | 0 | 2 |

These counts describe server variants, not manual browser cases. [Methods and original report adaptations](server-validation.md).

The two TC-005 positives were blocked because their exact addresses were already occupied. Keep them Blocked until repeated with new unique test emails and independent usernames. Earlier successful browser screenshots do not change those server results.

Conclusion: the available evidence supports specific registration/authentication observations and two localization retests. Browser refresh verification and the two blocked positives remain open. [Other limitations](limitations.md).
