# Supplemental server validation
These are historical, controlled Django integration checks in local_qa, not a fully automated portfolio suite or a new test run during preparation. Real views/forms and CSRF-enforced clients were used. Application protections were not disabled. SQL test changes were rolled back; rollback did not undo normal mail capture or request quota consumption. No verification was completed for accepted pending requests.

| Bundle | Checks | Passed | Failed | Blocked |
|---|---:|---:|---:|---:|
| TC-003 | 4 | 4 | 0 | 0 |
| TC-004 | 18 | 18 | 0 | 0 |
| TC-005 | 10 | 8 | 0 | 2 |
| Total | 32 | 30 | 0 | 2 |

Each row counts server variants, not manual browser cases. TC-005 includes one direct-form regional investigation, so its 8 passes are not 8 successful registrations. HTTP 200 with validation errors is rejection, not successful signup.

The exact original reports remain private. Public English adaptations below retain verdicts and evidence limits while omitting cache keys, internal service coordinates, source excerpts and generated credentials. Historical acceptance screenshots do not clear later blocked server checks.

- [TC-003: length boundaries](../evidence/smoke/TC-003/TC-003_server_validation.txt)
- [TC-004: username syntax and uniqueness](../evidence/smoke/TC-004/TC-004_server_validation.txt)
- [TC-005: email validation](../evidence/smoke/TC-005/TC-005_server_validation.txt)

Next: rerun the two Blocked TC-005 positives with new unique test emails and independent usernames. Their status remains Blocked until that execution.
