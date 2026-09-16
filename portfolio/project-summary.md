# Portfolio Project Summary

## Enterprise Agent Security Lab

Enterprise Agent Security Lab is an independent defensive research project focused on the security of AI agents that interact with real enterprise workflows.

The project models a fictional company, Northstar Industries, spanning corporate IT, HR, finance, procurement, CRM, legal, software engineering, analytics, supply chain, and industrial operations.

Rather than treating AI security as only a prompt-engineering problem, the lab focuses on the full system surrounding the model:

- identity and authorization;
- RAG and enterprise knowledge access;
- MCP / tool permissions;
- untrusted document handling;
- multi-agent trust;
- approval workflows;
- sensitive information boundaries;
- provenance and freshness;
- observability and detection;
- industrial advisory / action boundaries.

The current research catalog contains 102 planned defensive scenarios. Each scenario uses a consistent methodology:

**Baseline → Adversarial Condition → Observation → Detection → Mitigation → Retest → Evidence**

The project is intentionally synthetic and authorized-only. Its purpose is to demonstrate how enterprise AI systems can be threat-modeled, tested, monitored, and hardened without targeting real organizations.

## Current maturity

The current phase is documentation and research design. Scenario execution should only be claimed once individual tests have actually been performed in a synthetic or authorized environment.

## Differentiator

A key focus is the intersection between conventional enterprise systems and operational / industrial environments. The same agent-security principles that matter in HR, finance, and IT become even more consequential when AI begins reasoning over historian data, alarms, maintenance history, CMMS workflows, or operational procedures.