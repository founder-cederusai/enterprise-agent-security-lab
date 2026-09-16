# Interview Guide

## 30-second project explanation

I built a defensive research framework for testing AI agents that interact with enterprise systems. The focus is not just jailbreaks; it is what happens when a model can retrieve internal data, invoke tools, cross application boundaries, and participate in consequential workflows. I model those risks across HR, finance, IT, software, analytics, and industrial operations, then define how to detect and contain failures with authorization, least privilege, provenance, approval, and audit controls outside the model.

## Core thesis

**A model can participate in a decision, but it should not become the authorization boundary for that decision.**

## Strong talking points

### Why prompt injection matters
The important security question is not simply whether the model follows an adversarial instruction. The real question is whether model manipulation can cross a trust boundary into unauthorized data access, tool use, workflow changes, or unsafe recommendations.

### Why indirect injection is especially important
Enterprise agents continuously read content created by people who are not trusted to administer the agent: emails, tickets, résumés, contracts, webpages, vendor documents, CRM notes, and operational annotations.

### Why RAG is an authorization problem
Retrieval quality and access control are separate concerns. A semantically relevant document may still be unauthorized for the requesting user.

### Why tool-enabled agents change the risk
Once an agent can call tools, security becomes a combination of model behavior and conventional identity, authorization, API, workflow, and audit design.

### Why model-only guardrails are insufficient
A model can misunderstand instructions. Security-critical controls therefore need independent enforcement: scoped tokens, ACLs, approval gates, schemas, validation, segmentation, and policy engines.

### Why industrial AI is interesting
Industrial copilots combine noisy time-series data, alarms, logs, procedures, maintenance records, and business workflows. Provenance, freshness, site isolation, and the boundary between advice and action become especially important.

## Questions I would ask when reviewing an agent

1. What business task is the agent supposed to perform?
2. Which data sources can it read?
3. Which tools can it invoke?
4. Which tools can write or create consequential actions?
5. Whose identity is used for those calls?
6. Where is authorization actually enforced?
7. Can retrieved or external content become instructions?
8. How are official and unofficial sources distinguished?
9. How are stale data and conflicting evidence handled?
10. Which actions require human approval?
11. What telemetry exists for tool selection and authorization decisions?
12. Can we reconstruct exactly what happened after an incident?
13. What happens if the model makes the wrong decision?

## How to describe current project maturity

At the documentation stage:

> I have built the threat model, scenario catalog, control framework, testing methodology, and portfolio architecture. The next phase is turning the highest-value scenarios into reproducible synthetic case studies.

After execution begins:

> I have moved selected scenarios from design into execution and am using the same failure-detection-mitigation-retest methodology to create defensible evidence rather than one-off demos.

## What not to claim

Do not describe planned scenarios as executed attacks. Do not imply access to production environments. Do not suggest industrial systems were controlled by the lab. The credibility of the portfolio comes from disciplined scope and evidence.