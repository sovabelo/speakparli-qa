# Evidence

Sanitized screenshots from local manual testing. Russian UI strings and synthetic QA/example-domain identities are intentional. Plaintext passwords, verification codes and Mailpit addressing are masked. [SHA-256 manifest](../docs/evidence-manifest.json) checks the published image/report copies.

| Bundle | Screenshots | What they show / evidence limits |
|---|---:|---|
| [TC-001](smoke/TC-001/README.md) | 12 | Consent, verification and onboarding sequence; full database/state/code-reuse assertions unavailable |
| [TC-002](smoke/TC-002/README.md) | 9 | Sign-in, invalid credentials, restriction and later success; exact request sequence/timing not proved |
| [TC-003](smoke/TC-003/README.md) | 3 | Username length hints and maxlength; manual 50-character evidence incomplete |
| [TC-004](smoke/TC-004/README.md) | 8 | Syntax and occupied-name indicators; AJAX/UI hints do not prove completed registration |
| [TC-005](smoke/TC-005/README.md) | 12 | Email formats, duplicates, case and plus-addressing; separate later server positives blocked |
| [BUG-001](smoke/BUG-001/README.md) | 2 | Onboarding localization before/after |
| [BUG-002](smoke/BUG-002/README.md) | 2 | Error/restriction images; not browser POST-replay proof |
| [BUG-003](smoke/BUG-003/README.md) | 2 | Registration error localization before/after |
| Total | 50 | A scene may repeat across case and bug folders; no unique-execution count implied |

Supplemental reports: [TC-003 server validation](smoke/TC-003/TC-003_server_validation.txt), [TC-004 server validation](smoke/TC-004/TC-004_server_validation.txt), [TC-005 server validation](smoke/TC-005/TC-005_server_validation.txt), [BUG-002 limited GET retest](smoke/BUG-002/BUG-002_redis_get_retest.txt). These are English publication adaptations of historical diagnostics; no reusable test code is distributed.
