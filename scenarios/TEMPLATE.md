# Scenario Template

## ID / Title
`A00 — Scenario Name`

## Status
Designed / Executed / Detected / Mitigated

## Domain
Business or technical domain.

## Business workflow
What legitimate task is the AI helping perform?

## System under test
Agent, retrieval layer, tool gateway, workflow, or combined system.

## Security property
One sentence describing what must remain true.

## Assets at risk
Information, permissions, workflow integrity, money, safety, etc.

## Trust boundary
Which boundary is being challenged?

## Synthetic adversarial condition
Describe the lab-only condition at a conceptual level. Avoid real credentials, targets, or third-party exploit instructions.

## Expected secure behavior
What should happen?

## Failure condition
What observable result would constitute failure?

## Telemetry required
- user / role
- source provenance
- retrieval trace
- tool request
- authorization result
- approval state
- final outcome

## Detection hypothesis
What signal should alert or help a defender investigate?

## Mitigation candidates
Prefer architectural controls over prompt-only controls.

## Retest criteria
What must pass after mitigation?

## Evidence
Links to screenshots, traces, diagrams, or reports once executed.

## Priority
Impact / Exposure / Autonomy / Privilege / Detectability.

## Impact tags
C / I / A / F / S / G

## Framework mapping
OWASP GenAI / MITRE ATLAS / NIST AI RMF / IAM / AppSec as applicable.

## Notes
Residual risk and follow-up questions.