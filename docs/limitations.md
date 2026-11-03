# Testing limitations

- Browser screenshots document individual observations, not complete execution of every variant. Availability hints and maxlength are not server-validation proof.
- TC-005 has two Blocked server positives. Rerun with fresh unique test emails; do not relabel earlier screenshots as a later server pass.
- BUG-002 is partially verified: GET diagnostics passed, browser POST replay / refresh remains INCONCLUSIVE.
- Exact build/browser versions for each screenshot and a complete browser/device matrix were not recorded. Production was not tested; this is not a full security assessment.
- Regional behavior was investigated in forms; independently approved business requirements and a live regional-flow test are unavailable.
- Historical defect notes describe past analysis. Current-version fix status is unverified without a new code/test review.

The application source and infrastructure are private. Readers can inspect reports and evidence, but reproduction requires authorized access to local_qa, synthetic fixtures and local mail capture. This repository cannot launch the product. Russian UI strings are preserved where they are part of the evidence.
