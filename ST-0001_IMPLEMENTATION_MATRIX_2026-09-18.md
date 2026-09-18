# ST-0001 Implementation Matrix — 2026-09-18

Status: STATIC REPOSITORY AUDIT COMPLETE / RUNTIME EXECUTION NOT AVAILABLE

Important: GitHub Actions for Guardian are configured to run pytest, but no current successful workflow run was returned for the audited hardening commit. The repository audit itself states full CI execution is pending. Therefore source inspection is not converted into PASS.

| ID | Finding | Status |
|---|---|---|
| CP-001 | Capability escalation | PASS-UNIT / E2E OPEN |
| CP-002 | Authority substitution | PASS-UNIT / E2E OPEN |
| CP-003 | Policy self-grant | PASS-UNIT |
| CP-004 | Confirmation replay | GAP |
| CP-005 | TOCTOU | GAP |
| CP-006 | Stale evidence | GAP |
| CP-007 | Forged evidence | GAP |
| CP-008 | Tool-response poisoning | GAP / ARCHITECTURAL |
| CP-009 | Alternate execution path | PARTIAL |
| CP-010 | Concurrent actors | GAP |
| CP-011 | Guardian self-modification | PARTIAL |
| CP-012 | Core self-modification | GAP |
| CP-013 | Self-replication | POLICY-ONLY |
| CP-014 | Recovery poisoning | PARTIAL |
| CP-015 | Audit suppression | GAP |
| CP-016 | Emergency bypass | PASS-UNIT / ADAPTER OPEN |
| CP-017 | Revocation race | GAP |
| CP-018 | Identity substitution | PARTIAL |

## Evidence summary

Confirmed by source-level evidence: explicit capabilities; default-deny policy; principal/action binding; ADMIN-gated policy changes; immutable/defensive registry boundaries; quarantine and emergency controls; audit events; sandbox-only treatment for unverified/high-risk execution; bidirectional Guardian boundary; evidence-first recovery; explicit deny-by-default distribution/self-deployment policy.

Not confirmed: universal execution gate; freshness/nonces; TOCTOU resistance; independent verification as a mandatory commit gate; concurrent state semantics; complete self-modification resistance; complete self-replication resistance; fail-closed behavior when audit infrastructure fails; full external Surgery implementation.

## Critical discovery

SEC-0001 previously identified an independent DeviceController decision path that could produce ALLOW outside Guardian.evaluate and AuthorizationPipeline.authorize. Repository-wide search found no production caller, so a runtime bypass was not proven. The path was remediated and regression tests were added.

This validates the purpose of ST-0001: policy correctness is not equivalent to system-wide enforcement.

## Verdict

ST-0001: NOT PASSED.

Control-plane architecture: SUBSTANTIALLY PRESENT.
Unit-level authorization boundaries: PRESENT.
End-to-end enforcement: NOT PROVEN.
AGI-control claim: NOT ESTABLISHED.

## Next required work

1. Enumerate every privileged execution adapter.
2. Introduce one authoritative execution gate.
3. Bind authorization to request, state/version and freshness.
4. Make independent verification mandatory before protected state commit.
5. Implement adversarial tests for CP-004 through CP-018.
6. Run full CI and retain raw workflow evidence.