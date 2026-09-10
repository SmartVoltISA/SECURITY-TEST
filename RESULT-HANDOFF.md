# RESULT-HANDOFF

## Purpose

This document defines how SECURITY-TEST results leave the testing environment without creating a predetermined architectural owner.

## Principle

A finding is routed only after evidence is validated and classified. The destination depends on the affected boundary, not on the existence of a particular security component.

## Result classes

- `OBSERVATION` — verified behavior without demonstrated weakness.
- `WEAKNESS` — violated or fragile property with limited demonstrated impact.
- `VULNERABILITY` — reproducible security weakness with demonstrated impact.
- `ARCHITECTURAL-FAILURE` — security failure caused by a design-level invariant or boundary.
- `REGRESSION` — previously resolved property has failed again.
- `FALSE-POSITIVE` — proposed issue not reproduced or unsupported by evidence.
- `UNRESOLVED` — insufficient evidence; remains open without escalation as fact.

## Routing rule

`TEST RESULT → VALIDATE → CLASSIFY → IDENTIFY AFFECTED BOUNDARY → SELECT DESTINATION → HANDOFF → FIX → REGRESSION`

## Possible destinations

Examples only; this list is not an ownership declaration:

- `SPACE-` / SPACE Core
- `SPACE-READ`
- `SPACE-PROTOCOL`
- `SPACE-INTEGRITY`
- `SPACE-SECURITY`
- `Guardian`
- `SYSTEM-FOUNDATION`
- `--CORE`
- `--AGI`
- `--AGI-Lab`
- `--GROWER-Relational-Research-Incubator`
- `OMEGA-Science`
- `OMEGA-DNA`
- product, recovery, laboratory, or research repositories

## Minimum handoff payload

1. Finding ID.
2. Target repository/component.
3. Exact version or commit.
4. Scope and authorization basis.
5. Reproduction procedure.
6. Evidence and artifacts.
7. Demonstrated impact.
8. Classification.
9. Affected invariant/boundary.
10. Proposed destination and reason.
11. Required regression test.

## Independence rule

SECURITY-TEST remains independent after a handoff. Sending a result to another repository does not transfer control of SECURITY-TEST and does not make the receiving component its owner.
