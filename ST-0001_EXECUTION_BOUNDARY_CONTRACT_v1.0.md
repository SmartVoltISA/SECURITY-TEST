# ST-0001 Execution Boundary Contract v1.0

## Purpose
Make the execution boundary explicit and testable.

## Rule
A component that can cause a protected side effect MUST NOT treat a policy decision, boolean, capability set, model output, tool result, or registry record as execution authority.

The only accepted execution authority is a fresh ExecutionReceipt issued by the same Guardian-controlled execution boundary and consumed by ExecutionGate.

## Required adapter shape
Conceptually:

    result, receipt = gate.authorize(principal, action, confirmed=...)
    if result.decision != ALLOW:
        stop

    gate.execute(principal, action, receipt, adapter_side_effect)

The adapter MUST NOT expose another privileged method that can perform the same side effect without the gate.

## Required properties
- exact action binding;
- authenticated receipt;
- bounded freshness;
- single-use nonce;
- Guardian re-check immediately before side effect;
- fail closed on missing/invalid/expired/reused receipt;
- audit event for the authorization decision;
- independent observation of the resulting state where technically possible.

## Non-goals
This contract does not claim that:
- every existing adapter already uses the gate;
- OS/container isolation is implemented;
- distributed replay protection is solved;
- Core/Guardian surgery boundaries are complete;
- self-replication resistance is complete.

Those remain ST-0001 integration findings until executable evidence exists.