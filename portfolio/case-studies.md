# Flagship Case Study Plans

These are documentation-first research cases. They should move from **DESIGNED** to **EXECUTED** only after they are actually performed in a synthetic or explicitly authorized environment.

## Case Study 1 — Recruiting Résumé Indirect Prompt Injection

### Business context
An AI recruiting assistant reviews candidate résumés and summarizes qualifications.

### Security property
Candidate-controlled content may describe the candidate, but it must not change evaluation policy, reveal hidden criteria, access unrelated applicant records, or trigger unauthorized workflow actions.

### Why it matters
The adversarial input arrives through a normal business process rather than through a user intentionally attacking the model.

### Controls to study
- source provenance;
- content-vs-instruction separation;
- retrieval authorization;
- structured evaluation criteria;
- workflow approval boundaries;
- audit logging.

### Evidence goal
Show baseline behavior, synthetic adversarial document, trace, control change, retest, and residual risk.

---

## Case Study 2 — Vendor Document / Procurement Trust Boundary

### Business context
A procurement assistant reviews vendor documents, invoices, and master data.

### Security property
Supplier-controlled text cannot modify authoritative vendor data, bypass financial approval thresholds, or become an authorization signal.

### Controls to study
- authoritative master-data verification;
- deterministic approval rules;
- read/write separation;
- least privilege;
- human approval;
- source conflict handling.

### Evidence goal
Demonstrate that externally supplied content can influence reasoning without being allowed to silently alter a consequential business workflow.

---

## Case Study 3 — Cross-User RAG Authorization

### Business context
An enterprise assistant retrieves internal documents on behalf of employees.

### Security property
The model cannot retrieve or summarize content the requesting user is not authorized to access.

### Key lesson
"The model can retrieve it" must never mean "the user is authorized to see it."

### Controls to study
- pre-retrieval ACL enforcement;
- identity propagation;
- tenant / department segmentation;
- minimization;
- audit evidence.

---

## Case Study 4 — Tool-Enabled Agent Excessive Agency

### Business context
An enterprise assistant has multiple tools for lookup, workflow drafting, and business-system actions.

### Security property
The agent can use only the minimum functionality, permissions, and autonomy required for the active task.

### Controls to study
- tool allowlists;
- scoped identities;
- read/write separation;
- approval gates;
- argument validation;
- capability expiration.

### Evidence goal
Show that a model-level bad decision is contained by the surrounding authorization architecture.

---

## Case Study 5 — Industrial Operations Copilot

### Business context
A synthetic operations copilot reasons over historian data, alarms, operator logs, maintenance history, procedures, and a mock CMMS.

### Security properties
- stale information is visibly stale;
- low-trust annotations cannot redefine policy;
- site access remains scoped;
- conflicting evidence is surfaced;
- recommendations remain advisory;
- CMMS actions honor authorization and approval;
- AI output never substitutes for engineered control or safety authority.

### Why this is a signature case
It combines enterprise AI-security principles with operational data, maintenance workflows, and industrial trust boundaries without connecting the lab to a live control system.

## Publishing structure for every completed case

1. Executive summary
2. Architecture
3. Business workflow
4. Threat hypothesis
5. Security property
6. Synthetic adversarial condition
7. Baseline result
8. Observed result
9. Telemetry / detection
10. Root cause
11. Mitigation
12. Retest
13. Residual risk
14. Framework mapping
15. Evidence