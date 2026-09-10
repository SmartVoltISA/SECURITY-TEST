# ARCHITECTURE-MAP

## Purpose

This is the security-testing map of the SmartVoltISA ecosystem. It is a **test-context map**, not an ownership or dependency graph.

Naming a repository here means only that it is a known component that may be relevant to testing. A relationship is recorded as `VERIFIED` only when supported by repository documentation, code, or an explicit architectural decision.

## Core architectural contexts

```text
                         ┌──────────────────────┐
                         │    SECURITY-TEST     │
                         │ independent test lab │
                         └──────────┬───────────┘
                                    │ findings
                                    ▼
                         validate → classify → route
                                    │
             ┌──────────────────────┼──────────────────────┐
             ▼                      ▼                      ▼
        SPACE context          Research context       System context
             │                      │                      │
       ┌─────┼─────┐          ┌─────┼─────┐          ┌─────┼─────┐
       │     │     │          │     │     │          │     │     │
      Core  READ  organs     OMEGA  GROWER AGI      CORE FOUNDATION RECOVERY
             │
             ▼
       external interfaces
       / data / devices

Guardian is a security/control component that can be a test target or a destination for relevant defensive knowledge. SECURITY-TEST does not belong to Guardian.
```

## SPACE contexts

### Canonical / structural

- `SPACE-` — canonical SPACE repository/context.
- `SPACE-READ` — public read-only layer.
- `SPACE-PROTOCOL` — protocol context.
- `SPACE-INTEGRITY` — integrity context.
- `SPACE-SECURITY` — security context.
- `SPACE-PRODUCT` — product/build context.
- `Space---Recovery-` — recovery context.

### Perception and interaction organs

- `SPACE-VISION`
- `SPACE-HEARING`
- `SPACE-TOUCH`
- `SPACE-ENVIRONMENT`
- `SPACE-DOCUMENT`
- `SPACE-WEB`
- `SPACE-ACTION`
- `SPACE-COMPUTER`
- `SPACE-DEVICE`
- `SPACE-DATABASE`
- `SPACE-AFFECT`

### Interface / language / related

- `ORGANISM-INTERFACE`
- `CICADA-LANGUAGE`

## Independent security/control context

- `Guardian`

Guardian is listed as an independent component. No ownership relationship with SECURITY-TEST is implied.

## Intelligence and research contexts

- `--AGI`
- `--AGI-Lab`
- `--GROWER-Relational-Research-Incubator`
- `OMEGA-Science`
- `OMEGA-DNA`
- `OMEGA-RECOVERY`
- `Omega-lab-.--.-`
- `RELATION-LAB`
- `B-Lab`
- `instrument`
- `instrument-Open`
- `--Math-A-New-Language-of-Mathematics`

## System / memory / recovery contexts

- `--CORE`
- `SYSTEM-FOUNDATION`
- `--ARCHIVE`
- `ORISIK`
- `ORISIK-RECOVERY`
- `Life-Network-Core`
- `digital-legacy`
- `Recovery--`

## Product / business / resource contexts

- `--MARKET-1`
- `MARKET-RECOVERY`
- `BUSINESS-1`
- `TOOLS-1`
- `SEF-SmartVault`
- `SEF-Developments`
- `RESOURCE-ENGINE`
- `--Opportunity-Engine`
- `energy-conversion`

## Fundamental / physical research contexts

- `COSMOS-ARCHITECTURE`
- `LIGHT-`
- `MASSA-`
- `MATTER-`
- `Space---Time-`
- `FORCE--`
- `GRAVITY--`
- `MATTER-ENERGY-`
- `MOMENTUM-`
- `MOTION-`
- `TIME-`
- `ENERGY--`
- `FIELD-`
- `WAVE--`
- `CHARGE--`
- `ENTROPY--`
- `INFORMATION--`
- `STRUCTURE--`
- `INTERACTION--`
- `BOUNDARY-`
- `STATE--`

## Verification status

The connected GitHub interface currently exposes 50 repositories for this account. The owner has stated that the actual current GitHub total is **73**.

Therefore:

- `50` = currently verified through the connected repository index in this session.
- `73` = owner-declared current total.
- `23` = names still requiring reconciliation from the authoritative GitHub account view.

Those 23 names are intentionally **not invented**. Once retrieved, they must be added to `REPOSITORY-REGISTRY.md` with their actual names and status.

## Rule against memory drift

Do not rely on remembered repository lists. Before making claims about the ecosystem inventory, use `REPOSITORY-REGISTRY.md` and reconcile it against the current GitHub account. If the source exposes only a subset, say so explicitly.
