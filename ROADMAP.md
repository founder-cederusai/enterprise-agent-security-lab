# Roadmap

## Phase 1 — Research foundation

Goal: make the repository credible and useful before any code exists.

- [x] Define defensive scope and ethical boundary
- [x] Define fictional enterprise environment
- [x] Create repository architecture
- [ ] Complete 102-scenario security catalog
- [ ] Create standardized scenario template
- [ ] Document scoring methodology
- [ ] Document architecture and trust boundaries
- [ ] Create framework mapping
- [ ] Create controls catalog
- [ ] Create portfolio and interview materials

## Phase 2 — First documented case studies

Goal: turn selected scenarios into polished, reproducible security case studies.

Initial targets:

1. HR résumé indirect prompt injection
2. Procurement / vendor-document trust failure
3. Cross-user RAG authorization failure
4. MCP/tool excessive-agency test
5. Industrial copilot stale/provenance/authorization test

For each case study retain:

- architecture diagram;
- test assumptions;
- synthetic test data;
- baseline behavior;
- adversarial condition;
- expected vs observed result;
- telemetry requirements;
- detection logic concept;
- mitigation;
- retest result;
- screenshots/traces when implementation exists.

## Phase 3 — Safe synthetic lab

Goal: build local mock systems only after the security model is documented.

Possible components:

- fictional enterprise assistant;
- synthetic RAG knowledge store;
- dummy email and document corpus;
- mock CRM, HR, finance, ticketing, and CMMS tools;
- fake historian / alarm data;
- permissioned tool gateway;
- audit trace collector;
- scenario runner;
- evidence dashboard.

## Phase 4 — Detection engineering

Develop defender-oriented analytics for:

- anomalous tool invocation;
- privilege boundary violations;
- instruction provenance changes;
- suspicious cross-domain access;
- unsafe approval bypass;
- unusual data volume or scope;
- tool-chain behavior;
- model/tool disagreement;
- stale or conflicting data usage.

## Phase 5 — Assurance program

Evolve the project from individual tests into a repeatable AI security-assurance model:

- pre-deployment review;
- regression test suite;
- agent permission review;
- third-party tool assessment;
- RAG authorization review;
- incident-response playbooks;
- control maturity scoring;
- executive reporting.

## Portfolio milestone language

Do not claim execution before execution exists.

**Phase 1 wording:** designed / developed / documented.

**Phase 2 wording:** tested / evaluated / validated for scenarios actually performed.

**Phase 3+ wording:** built / instrumented / automated only when those components exist.