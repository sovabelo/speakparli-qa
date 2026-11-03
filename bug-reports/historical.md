# Historical defects — separate provenance
Current-version fix status is **unverified**: this preparation did not inspect the current private implementation or rerun the relevant tests. A historical fix reference is not proof of the present behavior.

These are not discoveries from the current manual run and do not share IDs with BUG-001/002/003. Original notes reconstruct fixes from private Git history; original failing versions were not rerun for this portfolio. No private code or diffs are included.

## SP-BUG-001 — Registration password retained in browser draft storage
Environment/version: historical fix reference 72f7980 (2026-10-16); original browser/OS unknown.
Preconditions: historical isolated version; synthetic signup data only.
Steps: fill signup, submit, inspect draft field names without copying secret values, return to signup.
Expected: draft retains non-sensitive data only.
Actual, supported by historical analysis: credential fields were retained and restored.
Severity: High; priority P1, portfolio assessment. Status: historical fix reference; current-version fix unverified. No external compromise or production deployment claim.
Evidence: original historical analysis document and commit identity checked locally; no manual screenshots. Retest: original notes describe helper-level automated checks, but no fresh execution was performed during portfolio preparation.

## SP-BUG-002 — Account notices persisted after logout
Environment/version: historical fix reference 427eddf (2026-10-22); original browser/OS unknown.
Preconditions: historical isolated version with unread synthetic account notices.
Steps: sign out using POST, follow the sign-in redirect, inspect notices, reopen sign-in.
Expected: logged-out account notices are absent.
Actual, supported by historical analysis: pending notices could survive and appear after logout.
Severity: Medium; priority P2, portfolio assessment. Status: historical fix reference; current-version fix unverified.
Evidence: original historical analysis and checked commit identity; no manual screenshots. Retest: regression coverage is described in original notes; its execution was not rerun in this preparation task.
