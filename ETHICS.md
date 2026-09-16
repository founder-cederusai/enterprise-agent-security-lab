# Ethics & Responsible Use

This project exists to improve the security of AI-enabled systems.

## Authorized use only

All testing described here should be performed only against:

- systems you own;
- systems you are explicitly authorized to test;
- synthetic or intentionally vulnerable lab environments;
- local simulations and mock enterprise systems.

Do not use this project to access, alter, disrupt, or probe third-party systems without authorization.

## Research principles

1. **Defensive purpose** — scenarios are designed to identify failure modes and validate controls.
2. **Synthetic data first** — use fictional identities, records, documents, assets, and operational data.
3. **No real-world operational impact** — industrial scenarios remain advisory and simulated.
4. **Least privilege** — tests should demonstrate why capability and authorization boundaries matter.
5. **Reproducibility** — document conditions, observed behavior, controls, and retest results.
6. **Evidence over theatrics** — the goal is measurable assurance, not dramatic jailbreak demonstrations.
7. **Responsible disclosure** — if work uncovers a vulnerability in a real product under authorized conditions, follow the vendor's disclosure process.

## Explicitly out of scope

- unauthorized access;
- credential theft;
- persistence in third-party systems;
- malware deployment;
- destructive actions;
- evasion intended to defeat real-world monitoring;
- interference with live industrial control or safety systems;
- exploitation of real employees, applicants, customers, or vendors.

## Publication standard

Public case studies should remove sensitive details and focus on:

**security property → synthetic adversarial condition → observation → control → retest → lesson learned**.

The strongest outcome is not "the model was tricked." The strongest outcome is demonstrating that the surrounding system remained secure even when model behavior was imperfect.