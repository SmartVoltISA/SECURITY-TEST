# SECURITY-TEST Methodology

## 1. Scope first

Before any test, record the target, authorized assets, permitted techniques, prohibited actions, dates, and source of authorization.

## 2. Build a model

Describe the system as components, trust boundaries, inputs, outputs, identities, state transitions, and security invariants.

## 3. Form hypotheses

A hypothesis must state:

- what security property may be violated;
- under which preconditions;
- what observable result would support it;
- what result would falsify it.

Do not label an untested hypothesis as a vulnerability.

## 4. Test safely

Use the smallest controlled experiment capable of distinguishing the hypothesis from the null hypothesis. Prefer test accounts, synthetic data, local replicas, official sandboxes, or other explicitly authorized environments.

## 5. Capture evidence

Record commands or procedures at the minimum necessary level, inputs, outputs, timestamps, versions, logs, screenshots or other artifacts, and hashes where useful.

## 6. Validate

Repeat the test. Check alternative explanations and false positives. Separate observed facts from interpretation.

## 7. Report

A report should contain: summary, affected asset, prerequisites, reproduction at minimum safe detail, observed impact, evidence, severity rationale, and remediation suggestion.

## 8. Defensive transformation

Convert a confirmed finding into a reusable defensive pattern:

`precondition → violated invariant → observable signal → detection → response → regression test`

## 9. Regression

After mitigation, rerun the same safe test and verify that the original condition no longer produces the vulnerable result. Preserve both the original evidence and the regression result.

## 10. Reproducibility

Record environment and dependency versions. A result that cannot be reproduced should be marked accordingly rather than upgraded to a stronger claim.
