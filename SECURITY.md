# Security Policy

## Purpose

This repository documents defensive testing methods for agentic AI systems. It is not a penetration-testing toolkit and does not contain live-target exploitation workflows.

## Lab boundary

All scenario execution should remain inside synthetic environments or explicitly authorized test systems.

Recommended lab characteristics:

- fictional organization and identities;
- dummy credentials and tokens;
- mock APIs and tools;
- synthetic documents and datasets;
- isolated networking;
- no production write access;
- no connection to real payment, HR, identity, safety, or control systems;
- auditable test traces;
- resettable state between scenarios.

## Security design assumptions

The project assumes that language models can misunderstand instructions, follow adversarial content, hallucinate, or make poor decisions. Therefore, controls should not rely on model obedience alone.

Important controls include:

- authorization outside the model;
- least-privilege tool scopes;
- explicit separation between trusted instructions and untrusted content;
- provenance and freshness metadata;
- human approval for consequential actions;
- deterministic validation before writes;
- identity propagation across agent/tool boundaries;
- complete audit logs;
- network and data segmentation;
- rate and cost controls;
- safe failure modes.

## Reporting a security concern

If you identify an issue in the documentation or a scenario that creates unnecessary real-world abuse risk, open a GitHub issue describing the concern without publishing sensitive exploit details.

If a finding involves a third-party product, use that vendor's responsible disclosure channel rather than publishing operational exploit details here.