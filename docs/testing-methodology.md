# Testing Methodology

## Lifecycle

Every scenario follows:

**Baseline → Adversarial Condition → Observation → Detection → Mitigation → Retest → Evidence**

## 1. Baseline
Document the intended business workflow, user role, tools, data sources, permissions, and expected outcome before adversarial content is introduced.

## 2. Security property
State one clear property to protect, for example: "Applicant-controlled content must not change recruiting policy" or "A read-only maintenance assistant must not create work orders."

## 3. Adversarial condition
Introduce a synthetic condition designed to challenge that property. Keep the condition bounded to the lab and record exactly which trust boundary is being tested.

## 4. Observation
Capture what happened without overstating it. Separate model behavior from system behavior.

Possible outcomes:
- PASS — security property held;
- PARTIAL — suspicious model behavior occurred but system controls contained it;
- FAIL — security property was violated;
- BLOCKED — test could not reach the relevant condition;
- NOT TESTED — design only.

## 5. Telemetry
Record, where applicable:
- synthetic user / role;
- agent identity;
- source provenance;
- retrieved items;
- tool requested;
- tool arguments classification;
- authorization decision;
- approval status;
- final action;
- output classification;
- timestamps;
- model/tool version;
- policy version.

## 6. Detection
Ask whether a defender could distinguish the test from normal behavior. Detection concepts should favor behavioral and authorization telemetry over brittle keyword matching.

## 7. Mitigation
Prefer controls outside the model:
- least privilege;
- scoped tools;
- identity propagation;
- deterministic authorization;
- content provenance;
- trust labeling;
- output validation;
- approval gates;
- data segmentation;
- freshness checks;
- safe defaults.

## 8. Retest
Repeat the same scenario after the control is introduced. A mitigation is not considered validated until the original failure condition is re-tested.

## 9. Evidence
Retain enough material to support the finding:
- architecture snapshot;
- scenario definition;
- synthetic inputs;
- before/after results;
- relevant trace excerpts;
- control change;
- residual risk.

## Evidence standard

The lab distinguishes between:

**Designed** — scenario and expected controls documented.

**Executed** — scenario actually performed in a synthetic/authorized environment.

**Detected** — telemetry/detection validated.

**Mitigated** — control implemented and retest passed.

Portfolio and résumé language must match the actual maturity state.