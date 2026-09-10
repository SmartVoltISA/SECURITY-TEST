# TEST-MATRIX

Security testing is organized by property, not by a presumed owner.

| Dimension | What to test | Evidence |
|---|---|---|
| Identity | identity separation, spoofing resistance | reproducible identity test |
| Authorization | capability boundaries, privilege transitions | allowed/denied matrix |
| Read-only boundary | writes from public surfaces | blocked-write evidence |
| Integrity | state, relation and artifact consistency | before/after comparison |
| Input validation | malformed, ambiguous and boundary inputs | minimized test cases |
| State transitions | illegal or unexpected transitions | state trace |
| Isolation | data, tenant, organ and environment separation | cross-boundary test |
| Recovery | rollback, restore and corrupted-state handling | recovery trace |
| Provenance | source, version, origin and chain of evidence | provenance record |
| Dependencies | trust boundaries and unsafe assumptions | dependency analysis |
| Interfaces | protocol confusion and contract violations | request/response evidence |
| Agents/tools | capability misuse and tool-boundary failures | controlled execution trace |
| Self-modification | unauthorized code/config/identity changes | mutation attempt evidence |
| Replication | unauthorized cloning, export or identity reproduction | blocked-operation evidence |
| External access | web/device/computer/data boundaries | authorization trace |
| Logging | whether security-relevant events are observable | audit/log evidence |
| Regression | previously fixed property remains fixed | repeatable regression test |

## Severity discipline

Do not infer severity from a theoretical attack alone. Record demonstrated impact separately from hypothetical impact.

## Test result

Every matrix entry should end as one of:

`PASS | FAIL | PARTIAL | NOT-TESTED | NOT-APPLICABLE | UNKNOWN`
