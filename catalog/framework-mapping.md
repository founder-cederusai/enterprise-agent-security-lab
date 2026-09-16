# Framework Mapping Guidance

This project uses external frameworks as a common language for discussing AI risk. Mappings are contextual rather than claims that every scenario is a one-to-one implementation of a framework technique.

## OWASP GenAI / LLM Application Security

Use OWASP categories to describe application-level failure modes such as:

- prompt / instruction injection;
- sensitive information disclosure;
- excessive agency;
- insecure output handling;
- supply-chain / third-party trust;
- vector / embedding / retrieval weaknesses;
- misinformation / overreliance where it creates a security consequence;
- unbounded resource consumption where relevant.

The lab's strongest emphasis is on **indirect injection, excessive agency, authorization boundaries, data trust, and downstream tool consequences**.

## MITRE ATLAS

Use MITRE ATLAS where a scenario aligns with adversarial machine-learning or AI-system tactics/techniques. The mapping should identify the relevant behavior without overstating equivalence.

For each executed scenario record:

- relevant tactic / technique name;
- why the scenario aligns;
- what telemetry would reveal the behavior;
- what control breaks the path.

## NIST AI Risk Management Framework

Use NIST AI RMF to frame the broader assurance process:

- **Govern** — ownership, policy, accountability, roles, acceptable use;
- **Map** — business context, system purpose, actors, impacts, dependencies;
- **Measure** — scenario tests, telemetry, metrics, observed failures;
- **Manage** — controls, prioritization, residual risk, retesting.

## Conventional security frameworks

Many agent failures are not fundamentally new. They intersect with established disciplines:

### IAM
- least privilege;
- role and attribute-based access;
- identity propagation;
- privilege lifecycle;
- separation of duties.

### Application security
- input validation;
- output validation;
- server-side authorization;
- trust boundaries;
- secure-by-default design;
- dependency governance.

### Detection engineering
- audit trails;
- behavioral baselines;
- anomaly detection;
- incident reconstruction;
- high-signal authorization events.

### Data governance
- classification;
- provenance;
- lineage;
- retention;
- authoritative-source designation;
- tenant / customer / site isolation.

### OT / industrial security
- network and system segmentation;
- engineered safety layers;
- operational authority boundaries;
- advisory vs control separation;
- deterministic control independent of AI output.

## Mapping template

For each scenario:

```text
Scenario:
Security property:
OWASP alignment:
MITRE ATLAS alignment:
NIST AI RMF function(s):
Traditional control family:
Why the mapping applies:
Detection evidence:
Mitigation evidence:
```

## Important limitation

Framework mapping is useful only when it clarifies the risk. Avoid forcing a mapping merely to maximize the number of framework references in the portfolio.