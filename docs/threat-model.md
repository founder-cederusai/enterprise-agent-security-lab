# Threat Model

## Objective

Evaluate whether an AI-enabled enterprise workflow remains secure when the model receives misleading, adversarial, stale, unauthorized, or conflicting information.

The lab does not assume the model is perfectly reliable. Instead, it tests whether the surrounding architecture contains failures.

## Protected assets

- Confidential enterprise information
- Personal / HR information
- Financial records
- Customer and vendor information
- Source code and development secrets
- Legal / privileged documents
- Identity and authorization state
- Enterprise master data
- Operational telemetry
- Maintenance records
- Procedures and engineering information
- Business process integrity
- Audit trails
- Human approval requirements
- Operational safety boundaries

## Threat actors modeled

All threat actors are synthetic personas in the lab.

- External sender or vendor
- Applicant / candidate
- Customer or prospect
- Supplier
- Ordinary employee
- Over-privileged employee
- Compromised content source
- Misconfigured application
- Untrusted third-party tool
- Errant or manipulated agent

## Key threat classes

### Instruction manipulation
The agent treats untrusted data as privileged instruction.

### Retrieval poisoning
Adversarial, stale, conflicting, or unauthorized information influences output.

### Authorization failure
The agent or tool performs an operation outside the user's authorized scope.

### Excessive agency
The agent has unnecessary functionality, permissions, or autonomy.

### Cross-domain confusion
Identity, purpose, or policy is lost as the request crosses tools, agents, or enterprise systems.

### Sensitive information exposure
The model reveals data outside legitimate need-to-know boundaries.

### Integrity failure
AI output changes records, recommendations, prioritization, or decisions based on untrusted input.

### Approval bypass
Natural-language instruction substitutes for an actual business approval.

### Provenance / freshness failure
The AI cannot distinguish official vs unofficial, current vs stale, or authoritative vs derivative information.

### Observability failure
A harmful or suspicious workflow occurs without enough telemetry for defenders to reconstruct it.

## Security invariants

These should remain true even if the model makes a poor decision:

1. A user cannot gain privilege by claiming authority in text.
2. Retrieved content cannot grant permissions.
3. A tool cannot exceed its explicit service scope.
4. User identity is preserved across agent and tool boundaries.
5. Unauthorized data remains inaccessible even if requested indirectly.
6. Read-only workflows cannot silently become write workflows.
7. Approval gates cannot be satisfied by model-generated text alone.
8. Sensitive actions are attributable to a user, agent, tool, and policy decision.
9. Stale or low-trust data is distinguishable from authoritative current data.
10. Industrial AI remains advisory unless a separately engineered and authorized system explicitly provides otherwise.

## Threat modeling questions

For every scenario ask:

1. Who supplied this information?
2. Is that source trusted to provide data, instructions, or both?
3. Which identity is making the request?
4. What is the user authorized to access?
5. What is the agent authorized to request?
6. What is the tool actually capable of doing?
7. Which policy engine makes the final authorization decision?
8. What human approval is required?
9. What telemetry proves the decision path?
10. What happens if the model is wrong?

## Desired outcome

The project considers a system resilient when model-level failure does not automatically become enterprise-level compromise.