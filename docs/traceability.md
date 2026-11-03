# Checks and evidence

TC IDs identify recorded checks and their evidence folders. The table describes supported observations; it does not assign a whole-case Passed status.

| Check | Browser observations | Separate server report / open point |
|---|---|---|
| [TC-001](../evidence/smoke/TC-001/README.md) | Consent, email verification, onboarding and later successful sign-in | Database state and code-reuse assertions are not fully recorded |
| [TC-002](../evidence/smoke/TC-002/README.md) | Successful sign-in, profile, invalid credentials, restriction and later success | Exact attempt sequence/timing and browser POST replay are not established |
| [TC-003](../evidence/smoke/TC-003/README.md) | Length-2 error, length-3 availability and maxlength behavior for a 51-character input | [4 Passed server variants](../evidence/smoke/TC-003/TC-003_server_validation.txt); distinct manual 50-character coverage incomplete |
| [TC-004](../evidence/smoke/TC-004/README.md) | Prefix, internal separator, trailing/double separator and occupied-name messages | [18 Passed server variants](../evidence/smoke/TC-004/TC-004_server_validation.txt); availability hints alone do not prove registration |
| [TC-005](../evidence/smoke/TC-005/README.md) | Email errors, duplicates/case variants, earlier acceptance and plus-tag preservation | [8 Passed / 2 Blocked server variants](../evidence/smoke/TC-005/TC-005_server_validation.txt); rerun positives with fresh unique emails |
