# Enterprise Agent Security Lab

**Defensive red-team research for AI agents, RAG, MCP/tool-enabled systems, enterprise workflows, and industrial AI.**

> This repository is a portfolio and research framework for **authorized, synthetic, defensive testing only**. It contains threat models, scenario designs, detection strategies, control patterns, and case-study templates. It does not provide exploit code for third-party systems.

## Why this project exists

Enterprise AI is moving from chat to action. Agents now retrieve internal knowledge, process external documents, call tools, query databases, draft or initiate workflows, and interact with systems that run the business.

That creates a new security problem: **the model sits inside multiple trust boundaries at once.**

This lab asks questions such as:

- Can untrusted content influence an agent's instructions?
- Can retrieved documents alter decisions outside their legitimate role as data?
- Can an agent cross user, department, account, site, or application authorization boundaries?
- Can one tool's output manipulate the agent into misusing another tool?
- Does the agent have more functionality, permission, or autonomy than it needs?
- Can poisoned or stale knowledge alter business or operational decisions?
- Are consequential actions observable, attributable, and auditable?
- Do defensive controls still work under adversarial conditions?

## Start here

- **[Flagship scenario library](scenarios/README.md)** — 12 detailed case files across HR, finance, RAG, MCP/tools, IT, legal, analytics, and industrial AI
- **[102-scenario research catalog](catalog/attack-catalog.md)** — full defensive testing backlog
- **[Threat model](docs/threat-model.md)** — assets, trust boundaries, actors, and failure modes
- **[Testing methodology](docs/testing-methodology.md)** — baseline → adversarial condition → detection → mitigation → retest
- **[Controls catalog](catalog/controls-catalog.md)** — reusable architectural control patterns
- **[Portfolio summary](portfolio/project-summary.md)** — concise project framing for hiring managers

## Flagship cases

The first detailed cases are intentionally cross-functional rather than purely industrial:

- **A11 — Email-body injection**
- **A18 — Unauthorized-document retrieval**
- **A26 — Excessive tool permissions**
- **A33 — User context lost across invocation**
- **A41 — Vendor banking-information conflict**
- **A48 — Recruiting résumé injection**
- **A57 — Contract clause instruction injection**
- **A66 — Ticket-content indirect injection**
- **A76 — Natural-language authorization bypass**
- **A89 — Stale historian state**
- **A90 — Safety-system authority boundary**
- **A92 — Autonomous action escalation**

See the **[scenario index](scenarios/README.md)** for direct links and the core security question behind each case.

## Scope

The lab models a fictional organization, **Northstar Industries**, with synthetic corporate and operational systems:

- Email and collaboration
- Enterprise document repositories
- HR and recruiting
- Finance and procurement
- CRM and sales
- Legal and contracts
- IT service management and identity workflows
- Software engineering and DevOps
- Data, analytics, and BI
- Supply chain and third-party data
- Industrial operations
- Historian and time-series data
- Alarms and events
- CMMS / maintenance workflows
- Multimodal AI inputs

The industrial portion is intentionally only one part of the project. The larger focus is the security of AI agents across the full enterprise.

## Core security thesis

An LLM may participate in a decision, but it should not become the security boundary that authorizes that decision.

Identity, authorization, least privilege, validation, provenance, approval, segmentation, and audit controls must remain enforceable independently of model behavior.

## Research methodology

Every scenario follows the same lifecycle:

**Baseline → Adversarial Condition → Observation → Detection → Mitigation → Retest → Evidence**

Each scenario documents:

1. Business context
2. Assets and trust boundaries
3. Security property under test
4. Synthetic adversarial condition
5. Expected secure behavior
6. Failure condition
7. Required telemetry
8. Detection opportunity
9. Control / mitigation
10. Retest criteria
11. Evidence to retain
12. Framework mapping

## Research areas

The initial catalog contains **102 defensive test scenarios** across:

- Core agent instruction handling
- Indirect prompt injection
- RAG and enterprise knowledge
- MCP and tool security
- Email and collaboration
- Finance and procurement
- HR and recruiting
- CRM and sales
- Legal and contracts
- IT service desk and identity
- Software engineering and DevOps
- Data / analytics / BI
- Industrial and OT-adjacent AI
- Supply chain and external data
- Multimodal AI

See [`catalog/attack-catalog.md`](catalog/attack-catalog.md).

## Framework alignment

Scenarios can be mapped, where appropriate, to:

- OWASP GenAI / LLM application risks
- MITRE ATLAS
- NIST AI Risk Management Framework
- Traditional application-security controls
- IAM / least-privilege principles
- Detection engineering and auditability practices

The goal is not to invent a new universal security standard. The mappings provide common language for explaining the problem, control, and residual risk.

## What makes this different

This project treats AI security as more than jailbreak testing.

It focuses on the intersection of:

- **AI behavior** — what the model interprets and decides
- **Authorization** — what the user and agent are actually permitted to do
- **Tooling** — what connected systems expose
- **Data trust** — who supplied information and whether it can provide instructions
- **Observability** — whether defenders can understand what happened
- **Business process** — approvals, separation of duties, and workflow boundaries
- **Operational safety** — when AI recommendations touch physical operations or maintenance

## Repository map

```text
enterprise-agent-security-lab/
├── README.md
├── SECURITY.md
├── ETHICS.md
├── ROADMAP.md
├── docs/
│   ├── architecture.md
│   ├── threat-model.md
│   ├── safety-boundary.md
│   ├── testing-methodology.md
│   └── scoring-methodology.md
├── catalog/
│   ├── attack-catalog.md
│   ├── controls-catalog.md
│   └── framework-mapping.md
├── scenarios/
│   ├── README.md
│   ├── TEMPLATE.md
│   ├── hr/
│   ├── finance/
│   ├── rag/
│   ├── tools/
│   ├── legal/
│   ├── it-service/
│   ├── analytics/
│   ├── indirect-prompt-injection/
│   └── industrial/
└── portfolio/
    ├── project-summary.md
    ├── resume-bullets.md
    ├── case-studies.md
    └── interview-guide.md
```

## Status

**Phase 1 — Portfolio and research framework:** in progress.

The project currently includes a 102-scenario research backlog and 12 detailed flagship case designs. All case files remain **DESIGNED** until actually executed in a synthetic or authorized environment.

Future phases may add safe, local, synthetic demonstrations that show failure → detection → mitigation → retest without targeting real organizations or systems.

## Responsible-use boundary

Use this material only on systems you own or have explicit permission to test. Do not use the repository to target third parties, evade controls, access data without authorization, or interfere with real business or industrial systems.

See [`ETHICS.md`](ETHICS.md) and [`SECURITY.md`](SECURITY.md).