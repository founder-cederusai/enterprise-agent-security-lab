# Résumé Bullets by Project Maturity

Use only wording that accurately reflects work completed.

## Phase 1 — Design / research framework

- Designed a defensive AI-security research framework for evaluating agentic AI, RAG, MCP/tool integrations, and enterprise copilots across corporate and industrial environments.
- Developed a 100+ scenario threat catalog spanning indirect prompt injection, authorization failures, excessive agency, retrieval poisoning, data exposure, cross-agent trust, and consequential workflow abuse.
- Defined a repeatable assurance methodology covering baseline behavior, adversarial conditions, telemetry, detection, mitigation, and control retesting.
- Created a synthetic enterprise threat model spanning HR, finance, procurement, CRM, legal, IT service management, software engineering, analytics, and industrial operations.
- Mapped AI-security risks to OWASP GenAI, MITRE ATLAS, NIST AI RMF, and conventional IAM / AppSec controls.

## Phase 2 — Once specific scenarios have actually been executed

- Executed reproducible AI red-team scenarios in a synthetic enterprise environment and documented failure conditions, telemetry, mitigations, and retest results.
- Evaluated indirect prompt-injection and authorization boundaries across enterprise documents, RAG workflows, and tool-enabled agents.
- Validated least-privilege, provenance, and human-approval controls through before/after adversarial testing.

## Phase 3 — Once a synthetic lab is implemented

- Built a synthetic enterprise AI-security lab with mock business systems, RAG, permissioned tools, audit telemetry, and repeatable defensive test scenarios.
- Instrumented agent and tool workflows to capture provenance, authorization decisions, tool calls, approvals, and final actions for incident reconstruction.
- Automated regression testing of previously identified agent-security failure modes after changes to models, prompts, tools, retrieval, or policy.

## Phase 4 — Once detection content is actually validated

- Developed and validated detection logic for anomalous AI-agent tool use, cross-domain access, authorization failures, and suspicious workflow escalation.
- Built defender-oriented telemetry and investigation patterns linking user identity, retrieved content, agent decisions, policy checks, tool activity, and downstream outcomes.

## Rule

Never convert **designed** into **executed**, **executed** into **mitigated**, or **planned** into **built** until the evidence exists in the repository.