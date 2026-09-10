# SECURITY-TEST

RU: Открытый стенд для исследования безопасности, поиска и проверки уязвимостей, анализа атак и разработки защитных механизмов.

EN: An open environment for security research, vulnerability discovery and validation, attack analysis, and defensive mechanism development.

中文：用于安全研究、漏洞发现与验证、攻击分析及防御机制开发的开放环境。

## Mission

SECURITY-TEST is a controlled research organ for finding, validating, documenting, and learning from security weaknesses in explicitly authorized environments.

The repository is an evidence base. A claim is not a finding until its supporting evidence and reproducible test are recorded.

## Research loop

`SCOPE → MODEL → HYPOTHESIS → TEST → EVIDENCE → VALIDATION → REPORT → MITIGATION → REGRESSION`

## Evidence vocabulary

- **FACT** — directly observed information.
- **EVIDENCE** — artifact supporting an observation.
- **HYPOTHESIS** — proposed explanation or attack path.
- **TEST** — controlled procedure used to evaluate it.
- **RESULT** — observed outcome.
- **IMPACT** — demonstrated security consequence.
- **CONCLUSION** — statement supported by the evidence.
- **UNKNOWN** — unresolved point that must not be presented as fact.

## Safety boundary

Research stays inside the target's explicitly authorized scope and rules. No unrelated systems, third-party accounts or data, service disruption, destructive actions, persistence, or irreversible changes. Use the minimum-impact proof necessary to establish a finding.

## Guardian handoff

Validated findings may produce defensive knowledge for Guardian. The preferred handoff is an abstract security pattern: violated invariant, preconditions, observable indicators, detection logic, mitigation concept, and regression test. Operational exploit material is not required unless legitimately necessary for a controlled regression test.

## Case IDs

Use `ST-0001`, `ST-0002`, ... for research cases. Preserve target scope, version/commit, environment, timestamps, methodology, evidence, and relevant artifact hashes where practical.

## Status model

`DISCOVERED → HYPOTHESIS → TESTING → VALIDATED / REJECTED → REPORTED → CONFIRMED → MITIGATED → REGRESSION-PASSED`
