# Guardian Handoff Contract

SECURITY-TEST may transfer validated defensive knowledge to Guardian through a controlled, reviewable record.

## Required fields

1. Finding ID
2. Vulnerability class
3. Security invariant
4. Preconditions
5. Observable indicators
6. Detection logic or defensive rule
7. Recommended response
8. Mitigation concept
9. Regression test
10. Evidence references
11. Validation status

## Principle

The offensive finding and defensive rule are related but are not identical artifacts. SECURITY-TEST proves that a security property can fail. Guardian uses the resulting security pattern to detect, prevent, isolate, or report the corresponding condition.

## Boundary

No automatic promotion of unvalidated hypotheses. No automatic transfer of secrets, credentials, private data, or unnecessary operational exploit details.

## Lifecycle

`FINDING → REVIEW → DEFENSIVE PATTERN → GUARDIAN RULE → REGRESSION TEST → VERIFIED`
