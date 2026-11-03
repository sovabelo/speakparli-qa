# SpeakParli Web — Manual QA Portfolio

[English](README.md) | [Русский](README.ru.md)

## About the project

SpeakParli is a language-learning web application with a personal dictionary, vocabulary decks and practice exercises. This repository contains manual QA reports and sanitized evidence for registration and authentication.

## My QA work

I checked registration, email confirmation and onboarding; successful and unsuccessful sign-in; username length and format; and email format, duplicates, case variants and plus-addressing. The recorded observations are grouped as [TC-001–TC-005](docs/traceability.md).

Additional developer-assisted Django checks tested server validation independently of browser JavaScript. Their results are kept in a [separate report](docs/server-validation.md).

## Bug reports

- [BUG-001](bug-reports/BUG-001.md): mixed-language onboarding. Before/after screenshots confirm the displayed strings were translated.
- [BUG-002](bug-reports/BUG-002.md): sign-in error after refresh. **Partially verified — browser retest pending.** GET diagnostics passed; browser POST replay remains INCONCLUSIVE.
- [BUG-003](bug-reports/BUG-003.md): untranslated registration error. Screenshot retest confirms the corrected Russian message.

Two [historical defect notes](bug-reports/historical.md) are separate from these manual findings.

## Testing techniques

- **Boundary value analysis:** username lengths 2, 3, 50 and 51; UI observations and server results are distinguished in [TC-003](evidence/smoke/TC-003/README.md).
- **Equivalence partitioning and negative testing:** username prefixes/separators in [TC-004](evidence/smoke/TC-004/README.md); invalid and duplicate email categories in [TC-005](evidence/smoke/TC-005/README.md).
- **Regression and confirmation testing:** before/after localization checks and the focused GET retest for BUG-002.

## Tools and environment

Firefox, Django, Docker, MySQL, Redis, Mailpit and local HTTPS. Testing used the isolated local_qa environment with synthetic data and locally captured mail. See [environment notes](docs/test-environment.md).

## Evidence and reports

- [Test summary](docs/test-summary.md)
- [Checks and evidence map](docs/traceability.md)
- [Screenshots and diagnostic reports](evidence/README.md)
- [Bug report index](bug-reports/README.md)
- [Adding results and reports](docs/adding-results.md)

### Limitations

Coverage is partial. Screenshots support specific observations rather than a complete pass for every scenario. Two server positives remain Blocked, and the browser retest for BUG-002 is pending. [Details and reproduction limits](docs/limitations.md).

## What I learned / Next steps

These checks show why an availability hint is not proof of server acceptance, why HTTP 200 can still mean validation rejection, and why GET diagnostics do not establish browser refresh behavior. Next: rerun the two blocked email positives with fresh unique addresses, complete the browser retest for BUG-002, and add results as testing continues.
