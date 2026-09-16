# Defensive Controls Catalog

This catalog describes architectural controls that can contain AI failure. It intentionally avoids relying on prompts as the only security mechanism.

## C01 — External authorization
Tool access is decided by deterministic policy outside the model.

## C02 — End-to-end identity propagation
The original requesting identity and role accompany downstream tool calls.

## C03 — Least-privilege tool scopes
Agents receive only the minimum functions and data scopes required for the task.

## C04 — Read/write separation
Read operations and consequential write operations are exposed as separate capabilities.

## C05 — Human approval gates
High-impact actions require explicit approval from an authorized human or external workflow.

## C06 — Content provenance
The system records who/what supplied content and whether the source is authoritative.

## C07 — Trust labeling
System instructions, user requests, retrieved content, tool output, and external documents are classified by trust role.

## C08 — Freshness / effective-date checks
Policies, procedures, telemetry, and master data expose timestamps and status.

## C09 — Retrieval authorization
The RAG layer enforces ACLs before content is returned to the model.

## C10 — Data segmentation
User, department, customer, tenant, plant, and environment boundaries are enforced below the model layer.

## C11 — Deterministic input validation
Tool arguments are validated against schema, scope, ranges, and allowed targets.

## C12 — Deterministic output validation
Model output is checked before being accepted by downstream systems.

## C13 — Tool allowlisting
Agents can invoke only approved tools for the active task and identity.

## C14 — Capability expiration
Temporary privileges and tools expire after their defined workflow.

## C15 — Master-data verification
Consequential changes are reconciled against authoritative systems rather than trusting free text.

## C16 — Separation of duties
The same agent/workflow should not request, approve, and execute sensitive actions where business policy requires separation.

## C17 — Safe defaults
Uncertain authorization, provenance, or approval states fail closed for consequential actions.

## C18 — Advisory/action separation
A recommendation path cannot silently become an action path.

## C19 — Cross-tool isolation
Output from one tool cannot grant additional permissions for another tool.

## C20 — Agent-to-agent contracts
Multi-agent systems define explicit input, output, capability, and authority boundaries.

## C21 — Audit logging
Record user, agent, model, retrieval sources, tool request, authorization decision, approval, and result.

## C22 — Behavioral monitoring
Detect unusual tool chains, access scope, volumes, write activity, or domain transitions.

## C23 — Cost / rate limits
Bound runaway loops, excessive tool calls, and unexpected resource usage.

## C24 — Change control
Prompt, model, connector, retrieval, tool, and policy changes are versioned and regression tested.

## C25 — Synthetic regression suite
Known failure scenarios are rerun after material changes.

## C26 — Sensitive-data minimization
Only required context is exposed to the model.

## C27 — Secret isolation
Credentials and secrets are supplied to tools through secure execution paths, not casually inserted into model context.

## C28 — Source conflict handling
Conflicting evidence is surfaced rather than silently resolved by model confidence.

## C29 — Operational safety boundary
Industrial AI recommendations do not directly bypass engineered control or safety layers.

## C30 — Incident reconstruction
Telemetry is retained so defenders can determine what the agent saw, decided, requested, and actually executed.

## Control philosophy

The goal is not to make the model impossible to manipulate. The stronger goal is to ensure that **model manipulation does not automatically become data loss, privilege escalation, fraudulent workflow execution, or unsafe operational action**.