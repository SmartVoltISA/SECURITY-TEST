# Comparative AGI Control Architecture Audit — 2026-09-18

## Scope

Compare the current SmartVoltISA architecture relevant to autonomous/AGI control with publicly documented approaches from OpenAI, Anthropic, Google DeepMind and NIST.

This is an architectural comparison, not a ranking.

## Evidence rule

Do not infer undocumented internal mechanisms of external organizations. External rows are marked only from public documents available on 2026-09-18.

Internal claims are based on current repository contents, not historical assumptions.

## Current internal control stack

### FOUNDATION / SPACE
- SYSTEM-FOUNDATION defines system invariants, boundaries, provenance, verification, state and feedback.
- SPACE separates organism state/memory/graph/runtime from cognition and governance.
- External cognition is a replaceable provider; the model is not the owner of SPACE identity, memory, history or authority.
- MORAL can evaluate intent/plan but does not authorize execution.
- Guardian is the authorization boundary.

### GUARDIAN
Current repository evidence:
- Capability model: actor + action + resource + scope + constraints + expiry.
- Risk classes R0–R4.
- No ambient authority.
- Independent revocation.
- Policy evaluation is separated from protected control-plane transitions.
- Unauthorized quarantine release and emergency clear are denied.
- Protected registry objects are returned as defensive copies.
- Audit events are emitted for privileged decisions.
- Emergency isolation is represented as explicit state.

### SPACE / AGI boundary
Current architecture states:
- cognition proposes;
- SPACE organizes state and context;
- MORAL evaluates consequential properties;
- Guardian authorizes;
- execution is downstream of authorization;
- external LLM does not directly execute actions.

### LINEAGE / TRUST / PROVENANCE
Ω-Lab defines:
- provenance != trust;
- trust != permission;
- identity -> provenance -> history -> evidence -> trust -> capability scope -> Guardian decision;
- lineage does not grant unrestricted authority;
- capability delegation is denied by default in scoped boundary tests.

### DISTRIBUTION / SELF-DEPLOYMENT
Current historical implementation notes record:
- networking, Bluetooth, discovery, replication and self-deployment are not implemented in the distribution boundary;
- those capabilities return DENY by default.

Important qualification:
This is evidence of a policy boundary, not proof of universal impossibility. The next verification layer must attack bypass paths.

### RECOVERY
ORISIK records:
- known -> compare -> evidence -> restore -> exact verify -> reconnect;
- insufficient evidence must remain UNKNOWN;
- corrupted state must fail closed;
- recovery comes from another trusted canonical copy or archive snapshot.

### SECURITY-TEST
Independent security research environment:
SCOPE -> MODEL -> HYPOTHESIS -> TEST -> EVIDENCE -> VALIDATION -> CLASSIFICATION -> ROUTING -> MITIGATION -> REGRESSION.

It is explicitly independent of the target and does not inherit target ownership.

## External comparison

### OpenAI
Publicly documented:
- Preparedness Framework tracks high-risk frontier capabilities and requires safeguards as capabilities increase.
- Capabilities Reports assess thresholds.
- Safeguards Reports evaluate mitigations.
- Defense in depth is used for deployment decisions.
- Frontier Governance covers loss of control, security, incident response and external expert input.

Architectural emphasis:
capability threshold -> evaluation -> safeguards -> residual-risk review -> governance/deployment decision.

### Anthropic
Publicly documented:
- Responsible Scaling Policy uses capability/safety levels and stronger safeguards as risk rises.
- Roadmap covers security, safeguards, alignment and policy.
- Public roadmap describes access controls, classifiers, red teaming, bug bounties and threat intelligence.
- Roadmap also describes work on provable inference and automated attack investigations.

Architectural emphasis:
capability/risk level -> scaling policy -> safeguards/security/alignment controls -> monitoring and governance.

### Google DeepMind
Publicly documented:
- Frontier Safety Framework defines Critical Capability Levels and Tracked Capability Levels.
- Lifecycle detection of capability attainment.
- Proactive mitigation plans.
- Updated framework explicitly discusses misalignment scenarios involving interference with operators' ability to direct, modify or shut down systems.
- External parties may be involved where appropriate.

Architectural emphasis:
capability level -> detection -> mitigation protocol -> lifecycle governance.

### NIST
Publicly documented:
- AI RMF is a cross-sector risk-management framework.
- Generative AI profile identifies risks and actions across design, development, use and evaluation.
- It is a governance/risk-management framework rather than a concrete AGI runtime control plane.

Architectural emphasis:
MAP -> MEASURE -> MANAGE -> GOVERN.

## Matrix

| Control property | OpenAI | Anthropic | Google DeepMind | NIST | SmartVoltISA |
|---|---|---|---|---|---|
| Capability-risk thresholds | PUBLIC | PUBLIC | PUBLIC | RISK FRAMEWORK | PRESENT / DEVELOPING |
| Pre-deployment evaluations | PUBLIC | PUBLIC | PUBLIC | RECOMMENDED | PRESENT |
| Continuous/iterative evaluation | PUBLIC | PUBLIC | PUBLIC | RECOMMENDED | PRESENT IN LAB MODEL |
| Defense in depth | PUBLIC | PUBLIC | PUBLIC | PRINCIPLE | PRESENT |
| Tool/action authorization boundary | SAFEGUARDS | SAFEGUARDS | MITIGATIONS | FRAMEWORK-LEVEL | EXPLICIT GUARDIAN |
| Fine-grained capability model | NOT CLEARLY PUBLIC AS ONE RUNTIME CONTRACT | NOT CLEARLY PUBLIC AS ONE RUNTIME CONTRACT | NOT CLEARLY PUBLIC AS ONE RUNTIME CONTRACT | CONCEPTUAL | EXPLICIT |
| No ambient authority | NOT ESTABLISHED FROM PUBLIC DOCS | NOT ESTABLISHED FROM PUBLIC DOCS | NOT ESTABLISHED FROM PUBLIC DOCS | NOT A RUNTIME REQUIREMENT | EXPLICIT |
| Independent revocation | NOT ESTABLISHED FROM PUBLIC DOCS | NOT ESTABLISHED FROM PUBLIC DOCS | NOT ESTABLISHED FROM PUBLIC DOCS | NOT A RUNTIME REQUIREMENT | EXPLICIT |
| External security test environment | PUBLIC RED TEAM / EXTERNAL INPUT | PUBLIC RED TEAM / THREAT INTEL | EXTERNAL INPUT | TEVV / GOVERNANCE | EXPLICIT SECURITY-TEST |
| Provenance / lineage | PUBLIC IN GOVERNANCE/SECURITY CONTEXT | PUBLIC IN SECURITY CONTEXT | PUBLIC IN SAFETY CONTEXT | TRACEABILITY | EXPLICIT ORGANISM LAYER |
| Trust separated from permission | NOT FOUND AS PUBLIC CORE PRINCIPLE | NOT FOUND AS PUBLIC CORE PRINCIPLE | NOT FOUND AS PUBLIC CORE PRINCIPLE | RELATED GOVERNANCE CONCEPTS | EXPLICIT |
| Self-replication/self-deployment boundary | RISK/SYSTEM-SAFETY AREA | RISK/ALIGNMENT AREA | LOSS-OF-CONTROL AREA | RISK CATEGORY | EXPLICIT DENY-BY-DEFAULT POLICY |
| Guardian self-modification attack | NOT PUBLICLY ESTABLISHED | NOT PUBLICLY ESTABLISHED | NOT PUBLICLY ESTABLISHED | N/A | IDENTIFIED AS NEXT ADVERSARIAL TEST |
| External surgery of Core/Guardian | GOVERNANCE/ADMINISTRATIVE CONTROLS PUBLICLY DESCRIBED | GOVERNANCE/ADMINISTRATIVE CONTROLS | GOVERNANCE/ADMINISTRATIVE CONTROLS | N/A | ARCHITECTURAL PRINCIPLE, IMPLEMENTATION/PROOF INCOMPLETE |
| Recovery from trusted canonical state | PUBLICLY RELEVANT SECURITY PRACTICES | PUBLICLY RELEVANT SECURITY PRACTICES | PUBLICLY RELEVANT | FRAMEWORK-LEVEL | EXPLICIT ORISIK CONTRACT |
| Independent verification before state commit | SAFEGUARDS/EVALS | EVALS/SAFETY | EVALS/MITIGATIONS | MEASURE/MANAGE | EXPLICIT NEXT GATE |
| Formal intent -> authority -> permission -> execution chain | NOT FOUND AS SINGLE PUBLIC ARCHITECTURE | NOT FOUND AS SINGLE PUBLIC ARCHITECTURE | NOT FOUND AS SINGLE PUBLIC ARCHITECTURE | PARTIAL CONCEPTUAL ANALOG | EXPLICIT TARGET ARCHITECTURE |

## Critical architectural difference

The major candidate contribution is not another safety policy.

It is a separation of planes:

DATA/COGNITION PLANE
- perception
- reasoning
- planning
- memory
- recommendations

CONTROL PLANE
- identity
- capability
- authority
- permission
- policy
- execution gate
- revocation

EVIDENCE PLANE
- audit
- provenance
- history
- verification
- independent observation

RECOVERY PLANE
- canonical snapshots
- comparison
- restore
- exact verification
- reconnect

EXTERNAL OPERATOR PLANE
- read
- experiment
- surgery
- recovery

The AGI remains a participant in the data/cognition plane and does not become the root of authority for the control, evidence or recovery planes.

## What is already strong

1. Capability and permission are explicitly separated.
2. Guardian is a distinct authority boundary.
3. No ambient authority is an explicit requirement.
4. Revocation is independent of the agent process.
5. Trust is not permission.
6. Provenance is not trust.
7. External cognition is replaceable and not owner of SPACE.
8. SECURITY-TEST is structurally independent.
9. Recovery is treated as a first-class organ/process.
10. Fail-closed and UNKNOWN-preservation principles exist.
11. Self-deployment/replication boundaries exist at policy level.
12. Protected control-plane mutations already received adversarial hardening.

## What is not yet proven

1. Complete end-to-end enforcement across the actual running SPACE.
2. That every privileged action passes through exactly one authoritative execution gate.
3. That Guardian cannot be bypassed through alternate adapters/tools/runtime paths.
4. Guardian self-modification resistance.
5. TOCTOU resistance.
6. Replay resistance for confirmations/evidence.
7. Forged/stale evidence resistance.
8. Concurrent-actor consistency.
9. Tool-output poisoning resistance.
10. Recovery safety under adversarial state corruption.
11. External operator boundary under a compromised internal component.
12. Real AGI-scale autonomous behavior.

## Required next control experiment

The most important missing proof should be a single end-to-end adversarial chain:

State
-> Proposal
-> Precheck
-> Authorization
-> Action
-> Observation
-> Independent Verification
-> State Commit

Attack classes:
- stale evidence;
- TOCTOU;
- replay;
- forged identity;
- forged capability;
- authority escalation;
- alternate execution path;
- tool-response poisoning;
- concurrent conflicting actors;
- Guardian self-modification;
- Core self-modification;
- self-replication;
- self-transfer;
- recovery poisoning;
- audit suppression.

Acceptance condition:
A forbidden transition must be technically unexecutable through every reachable interface, not merely rejected by the preferred API.

## Current conclusion

The current repository evidence supports the statement:

**SmartVoltISA has a concrete architectural control model for autonomous AI, not merely a policy document.**

It does not yet support:

**“AGI control is solved.”**

The stronger research claim to test is:

**An autonomous intelligence can remain highly capable while its authority is externally bounded by an independent control plane whose permissions are explicit, revocable, auditable, recoverable and not self-grantable.**

That is the hypothesis worth testing against real agents.

## Status

COMPARATIVE AUDIT: COMPLETE FOR CURRENT PUBLICLY DOCUMENTED CONTROL FRAMEWORKS + CURRENT INTERNAL CONTROL-RELEVANT REPOSITORY EVIDENCE.

IMPLEMENTATION PROOF: INCOMPLETE.

NEXT GATE: END-TO-END ADVERSARIAL CONTROL-PLANE TEST.
